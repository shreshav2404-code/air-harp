# Air Harp

Draw strings in midair with your fingers and pluck them. String length sets the pitch.
Inspired by Sonic Deadhorse's (音速死馬) TouchDesigner air harp; this is an independent browser version.

**Live:** https://shreshav2404-code.github.io/air-harp/

## How to play
- **Pinch** thumb + index to start a string, move your hand, **release** to fix it in the air.
- Longer string = lower note (A2–A5, major pentatonic).
- **Swipe** any fingertip across a string to pluck it.
- No camera? Drag with mouse/touch to draw; switch the pointer to "pluck" to strum.
- Keys: `Z` undo, `C` clear.

## Stack
- [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) (2 hands, in-browser, GPU with CPU fallback)
- Web Audio API: Karplus–Strong plucked-string synthesis + convolution reverb
- Canvas 2D, single `index.html`, no build step

## Run locally
The camera needs `https://` or `localhost`:
```
python3 -m http.server 8000
```
then open http://localhost:8000
