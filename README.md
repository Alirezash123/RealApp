import 'package:flutter/material.dart';
import 'package:video_player/video_player.dart';
import 'package:chewie/chewie.dart';
import 'package:flutter_cache_manager/flutter_cache_manager.dart';

class SimpleCachedVideoPlayer extends StatefulWidget {
  const SimpleCachedVideoPlayer({super.key});

  @override
  State<SimpleCachedVideoPlayer> createState() => _SimpleCachedVideoPlayerState();
}

class _SimpleCachedVideoPlayerState extends State<SimpleCachedVideoPlayer> {
  ChewieController? _chewieController;

  @override
  void initState() {
    super.initState();
    _initPlayer();
  }

  Future<void> _initPlayer() async {
    // 1️⃣ لینک ویدیو (می‌تونی از API بگیری)
    const videoUrl = "https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4";

    // 2️⃣ دانلود و کش ویدیو
    final file = await DefaultCacheManager().getSingleFile(videoUrl);

    // 3️⃣ ساخت کنترلر ویدیو از فایل کش‌شده
    final videoController = VideoPlayerController.file(file);
    await videoController.initialize();

    // 4️⃣ ساخت کنترلر Chewie با کنترل‌های سفارشی
    _chewieController = ChewieController(
      videoPlayerController: videoController,
      autoPlay: false,
      looping: false,
      allowFullScreen: true,
      allowMuting: false,
      allowPlaybackSpeedChanging: false,
      showControls: false, // ❌ کنترل‌های پیش‌فرض Chewie غیرفعال می‌شن
    );

    setState(() {});
  }

  @override
  void dispose() {
    _chewieController?.dispose();
    super.dispose();
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text("ویدیوپلیر ساده و کش‌دار")),
      body: Center(
        child: _chewieController == null
            ? const CircularProgressIndicator()
            : Stack(
                alignment: Alignment.bottomCenter,
                children: [
                  Chewie(controller: _chewieController!),

                  // 🎛 کنترل‌های سفارشی
                  Positioned(
                    bottom: 10,
                    left: 10,
                    right: 10,
                    child: Row(
                      mainAxisAlignment: MainAxisAlignment.center,
                      children: [
                        // پلی / پاز
                        IconButton(
                          iconSize: 40,
                          color: Colors.white,
                          icon: Icon(
                            _chewieController!.videoPlayerController.value.isPlaying
                                ? Icons.pause_circle
                                : Icons.play_circle,
                          ),
                          onPressed: () {
                            final player = _chewieController!.videoPlayerController;
                            setState(() {
                              player.value.isPlaying ? player.pause() : player.play();
                            });
                          },
                        ),

                        const SizedBox(width: 20),

                        // تمام‌صفحه
                        IconButton(
                          iconSize: 35,
                          color: Colors.white,
                          icon: const Icon(Icons.fullscreen),
                          onPressed: () {
                            _chewieController!.enterFullScreen();
                          },
                        ),
                      ],
                    ),
                  ),
                ],
              ),
      ),
      backgroundColor: Colors.black,
    );
  }
}