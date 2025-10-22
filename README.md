import 'package:flutter/material.dart';

class FormationScreen extends StatelessWidget {
  final List<List<Map<String, String>>> formation = [
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

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.green[900],
      appBar: AppBar(
        backgroundColor: Colors.green[900],
        elevation: 0,
        centerTitle: true,
        title: const Text(
          "🔵 ترکیب رئال مادرید",
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
                children: formation.map((line) {
                  return Row(
                    mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                    children: line.map((player) {
                      return _buildPlayer(player['name']!, player['photo']!);
                    }).toList(),
                  );
                }).toList(),
              ),
            ),
          ],
        ),
      ),
    );
  }

  Widget _buildPlayer(String name, String photoUrl) {
    return Column(
      children: [
        Container(
          decoration: BoxDecoration(
            shape: BoxShape.circle,
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
            onBackgroundImageError: (_, __) {}, // جلوگیری از خطا در صورت نبود عکس
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