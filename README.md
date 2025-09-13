import 'dart:async';
import 'dart:convert';
import 'package:flutter_bloc/flutter_bloc.dart';
import 'package:http/http.dart' as http;
import 'data_event.dart';
import 'data_state.dart';

class DataBloc extends Bloc <DataEvent,DataState>{
  DataBloc():super(DataInitial()){
    on<FetchDataEvent>(_fetchData);

  }

  FutureOr<void> _fetchData(FetchDataEvent event, Emitter<DataState> emit) async{
    emit(DataLoading());
    
    try{
      
      var response =await http.get(Uri.parse("https://raw.githubusercontent.com/Alirezash123/RealApp/refs/heads/main/heder.txt"));
      var newsrespons=await http.get(Uri.parse("https://raw.githubusercontent.com/Alirezash123/RealApp/refs/heads/main/news.txt"));
      var tabledata=await http.get(Uri.parse("https://api.football-data.org/v4/competitions/PD/standings"),headers: {'X-Auth-Token':'9a90bafca7a84ab0afcdb13b014ac2fe'});
      var nextmatch=await http.get(Uri.parse("https://raw.githubusercontent.com/Alirezash123/RealApp/refs/heads/main/nextmatch"));
      var prematch=await http.get(Uri.parse("https://raw.githubusercontent.com/Alirezash123/RealApp/refs/heads/main/Prematch"));
      if(response.statusCode==200){
        var data =jsonDecode(response.body);
        var news=jsonDecode(newsrespons.body);
        var table=jsonDecode(tabledata.body);
        var Next_match=jsonDecode(nextmatch.body);
        var Pre_match=jsonDecode(prematch.body);
        List newslentch=news;
        var reverseNews=newslentch.reversed.toList();
        List table1 =table['standings'][0]['table'];
        print(table1);

        emit(DataLoaded(data,news,newslentch.length,reverseNews,table1,Next_match,Pre_match,[]));
        Timer _timer;

        _timer=Timer.periodic(Duration(seconds: 10), (Timer timer)async {

          var livematch=await http.get(Uri.parse("https://api.football-data.org/v4/teams/86/matches"),headers: {'X-Auth-Token':'9a90bafca7a84ab0afcdb13b014ac2fe'});
          var live=jsonDecode(livematch.body);
          var matches=live['matches'];
          var inplaymatch=matches.firstWhere((record)=>record['status']=='FINISHED',orElse:()=>null);
          if(inplaymatch!=null){
            var inplaygoal=inplaymatch['score']['fullTime'];
            emit(DataLoaded(data,news,newslentch.length,reverseNews,table1,Next_match,Pre_match,inplaygoal));
          }

        });


      }else{
        print('eror');
        emit(DataEror(response.statusCode));
      }
      
    }catch(e){
      print(e.toString());
      emit(DataEror(e.toString()));
    }
    
    
  }
}
