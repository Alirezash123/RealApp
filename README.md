import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: FormationScreen(),
    );
  }
}

class FormationScreen extends StatelessWidget {
  const FormationScreen({super.key});

  // ترکیب رئال مادرید (بالا)
  final List<List<Map<String, String>>> realMadridFormation = const [
    [
      {"name": "Joselu", "photo": "https://i.imgur.com/fake1.jpg"},
      {"name": "Vinícius", "photo": "https://i.imgur.com/fake2.jpg"},
      {"name": "Rodrygo", "photo": "https://i.imgur.com/fake3.jpg"},
    ],
    [
      {"name": "Bellingham", "photo": "https://i.imgur.com/fake4.jpg"},
      {"name": "Tchouaméni", "photo": "https://i.imgur.com/fake5.jpg"},
      {"name": "Valverde", "photo": "https://i.imgur.com/fake6.jpg"},
    ],
    [
      {"name": "Mendy", "photo": "https://i.imgur.com/fake7.jpg"},
      {"name": "Nacho", "photo": "https://i.imgur.com/fake8.jpg"},
      {"name": "Rüdiger", "photo": "https://i.imgur.com/fake9.jpg"},
      {"name": "Carvajal", "photo": "https://i.imgur.com/fake10.jpg"},
    ],
    [
      {"name": "Courtois", "photo": "https://i.imgur.com/fake11.jpg"},
    ],
  ];

  // ترکیب تیم حریف (پایین)
  final List<List<Map<String, String>>> opponentFormation = const [
    [
      {"name": "Player1", "photo": "https://i.imgur.com/fake12.jpg"},
      {"name": "Player2", "photo": "https://i.imgur.com/fake13.jpg"},
      {"name": "Player3", "photo": "https://i.imgur.com/fake14.jpg"},
    ],
    [
      {"name": "Player4", "photo": "https://i.imgur.com/fake15.jpg"},
      {"name": "Player5", "photo": "https://i.imgur.com/fake16.jpg"},
      {"name": "Player6", "photo": "https://i.imgur.com/fake17.jpg"},
    ],
    [
      {"name": "Player7", "photo": "https://i.imgur.com/fake18.jpg"},
      {"name": "Player8", "photo": "https://i.imgur.com/fake19.jpg"},
      {"name": "Player9", "photo": "https://i.imgur.com/fake20.jpg"},
      {"name": "Player10", "photo": "https://i.imgur.com/fake21.jpg"},
    ],
    [
      {"name": "Goalkeeper", "photo": "https://i.imgur.com/fake22.jpg"},
    ],
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.green[900],
      appBar: AppBar(
        backgroundColor: Colors.green[900],
        elevation: 0,
        centerTitle: true,
        title: const Text(
          "ترکیب دو تیم",
          style: TextStyle(
              color: Colors.white, fontWeight: FontWeight.bold, fontSize: 20),
        ),
      ),
      body: Container(
        decoration: const BoxDecoration(
          gradient: LinearGradient(
            colors: [Color(0xFF136A2D), Color(0xFF0A431B)],
            begin: Alignment.topCenter,
            end: Alignment.bottomCenter,
          ),
        ),
        child: Stack(
          children: [
            // خطوط زمین
            Positioned.fill(
              child: CustomPaint(
                painter: FieldPainter(),
              ),
            ),

            // بازیکن‌ها
            Padding(
              padding: const EdgeInsets.all(12.0),
              child: Column(
                mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                children: [
                  // تیم رئال - بالا
                  ...realMadridFormation.map((line) {
                    return Row(
                      mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                      children: line
                          .map((player) =>
                              _buildPlayer(player['name']!, player['photo']!, Colors.blue))
                          .toList(),
                    );
                  }).toList(),

                  // فاصله وسط زمین
                  const SizedBox(height: 50),

                  // تیم حریف - پایین
                  ...opponentFormation.map((line) {
                    return Row(
                      mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                      children: line
                          .map((player) =>
                              _buildPlayer(player['name']!, player['photo']!, Colors.red))
                          .toList(),
                    );
                  }).toList(),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }

  // ویجت بازیکن با حاشیه رنگ تیم
  Widget _buildPlayer(String name, String photoUrl, Color color) {
    return Column(
      children: [
        Container(
          decoration: BoxDecoration(
            shape: BoxShape.circle,
            border: Border.all(color: color, width: 3),
            boxShadow: [
              BoxShadow(
                color: Colors.black.withOpacity(0.3),
                blurRadius: 6,
                offset: const Offset(2, 2),
              ),
            ],
          ),
          child: CircleAvatar(
            radius: 30,
            backgroundColor: Colors.white,
            backgroundImage: NetworkImage(photoUrl),
          ),
        ),
        const SizedBox(height: 6),
        Text(
          name,
          style: const TextStyle(
            color: Colors.white,
            fontSize: 13,
            fontWeight: FontWeight.bold,
            shadows: [
              Shadow(
                blurRadius: 4,
                color: Colors.black54,
                offset: Offset(1, 1),
              ),
            ],
          ),
        ),
      ],
    );
  }
}

// خطوط زمین فوتبال
class FieldPainter extends CustomPainter {
  @override
  void paint(Canvas canvas, Size size) {
    final paint = Paint()
      ..color = Colors.white.withOpacity(0.6)
      ..strokeWidth = 2
      ..style = PaintingStyle.stroke;

    final center = Offset(size.width / 2, size.height / 2);

    // خط وسط زمین
    canvas.drawLine(Offset(0, center.dy), Offset(size.width, center.dy), paint);

    // دایره وسط
    canvas.drawCircle(center, 50, paint);

    // محوطه جریمه بالا و پایین
    canvas.drawRect(Rect.fromLTWH(size.width / 4, 20, size.width / 2, 60), paint);
    canvas.drawRect(Rect.fromLTWH(size.width / 4, size.height - 80, size.width / 2, 60), paint);
  }

  @override
  bool shouldRepaint(CustomPainter oldDelegate) => false;
}