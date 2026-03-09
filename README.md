## What is it?

White Skeleton Laser is a browser-based app that uses your webcam and AI to track your hand in real time. It draws a white skeleton over your hand and lets you paint glowing red laser trails in the air using just your finger — no mouse, no touch, no controller needed.

## How it works

Your webcam feed is captured silently in the background and sent frame by frame to MediaPipe Hands, a Google AI library that detects 21 exact points on your hand — every joint, every fingertip. These points are used to draw the white skeleton grid you see on screen.

Every frame, the app reads your hand position and checks which gesture you are making. If only your index finger is up, it starts drawing a glowing red laser trail at your fingertip using the Canvas 2D API. Fire-like spark particles burst from the tip as you draw. If you open all five fingers, everything is erased. If you pinch your thumb and index finger together, you can grab any drawing and drag it around the screen.

The canvas is mirrored horizontally so it feels like a selfie camera — natural and intuitive.

## How it is made

Built with three languages — HTML, CSS, and JavaScript. No frameworks, no build tools, no install. Just files you open in a browser.

MediaPipe Hands runs entirely in the browser using WebAssembly, so no data ever leaves your device. The drawing engine uses the native Canvas 2D API. The spark effect is a custom particle system written from scratch — each spark has its own velocity, gravity, friction, and fade lifecycle.
