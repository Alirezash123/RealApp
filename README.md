[ERROR:flutter/runtime/dart_vm_initializer.cc(41)] Unhandled Exception: 'package:bloc/src/emitter.dart': Failed assertion: line 114 pos 7: '!_isCompleted': 
E/flutter (31985): 
E/flutter (31985): emit was called after an event handler completed normally.
E/flutter (31985): This is usually due to an unawaited future in an event handler.
E/flutter (31985): Please make sure to await all asynchronous operations with event handlers
E/flutter (31985): and use emit.isDone after asynchronous operations before calling emit() to
E/flutter (31985): ensure the event handler has not completed.
E/flutter (31985): 
E/flutter (31985):   **BAD**
E/flutter (31985):   on<Event>((event, emit) {
E/flutter (31985):     future.whenComplete(() => emit(...));
E/flutter (31985):   });
E/flutter (31985): 
E/flutter (31985):   **GOOD**
E/flutter (31985):   on<Event>((event, emit) async {
E/flutter (31985):     await future.whenComplete(() => emit(...));
E/flutter (31985):   });
E/flutter (31985): 
E/flutter (31985): #0      _AssertionError._doThrowNew (dart:core-patch/errors_patch.dart:51:61)
E/flutter (31985): #1      _AssertionError._throwNew (dart:core-patch/errors_patch.dart:40:5)
E/flutter (31985): #2      _Emitter.call (package:bloc/src/emitter.dart:114:7)
E/flutter (31985): #3      DataBloc._fetchData.<anonymous closure> (package:real/bloc/data_block.dart:46:17)
E/flutter (31985): #4      _Timer._runTimers (dart:isolate-patch/timer_impl.dart:398:19)
E/flutter (31985): #5      _Timer._handleMessage (dart:isolate-patch/timer_impl.dart:429:5)
E/flutter (31985): #6      _RawReceivePort._handleMessage (dart:isolate-patch/isolate_patch.dart:189:12)
E/flutter (31985): 

