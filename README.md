# React + TypeScript + Vite

# Face Tracking Application

A real-time face tracking application built with React, TypeScript, and MediaPipe.

## 🚀 Features

- Real-time face detection
- Facial landmark visualization
- Face mesh overlay
- Eye and lip tracking
- GPU-accelerated processing

## 🛠️ Tech Stack

- React 18 + TypeScript
- Vite (Build tool)
- MediaPipe (Face detection)
- Three.js (3D rendering)
- Tailwind CSS (Styling)

## 📁 Project Structure

```
Face Tracking/
├── src/
│   ├── App.tsx           # Main application component
│   ├── main.tsx         # Entry point
│   └── index.css        # Global styles
├── public/              # Static assets
├── package.json        # Dependencies
└── vite.config.ts      # Vite configuration
```

## 🏃‍♂️ Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Modern web browser with WebGL support
- Webcam
- GPU acceleration enabled

### Installation

1. Clone the repository:
```bash
git clone [your-repository-url]
cd face-tracking
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## 💡 How It Works

### Camera Setup
The application requests camera access and initializes a video stream with optimal settings for face tracking:

```typescript
const stream = await navigator.mediaDevices.getUserMedia({
  video: {
    width: { ideal: 1280 },
    height: { ideal: 720 },
    facingMode: "user",
    frameRate: { ideal: 30 }
  }
});
```

### Face Detection Features
- Real-time facial landmark detection
- Color-coded tracking:
  - Green markers for left eye features
  - Red markers for right eye features
  - White outline for face oval
  - Semi-transparent mesh overlay

## 🔧 Troubleshooting

### Common Issues

1. **Camera Not Working**
   - Check browser permissions
   - Allow camera access when prompted
   - Ensure no other application is using the camera

2. **Performance Issues**
   - Check if GPU acceleration is enabled
   - Close resource-intensive applications
   - Try reducing video resolution

3. **Black Screen**
   - Refresh the page
   - Check camera connection
   - Ensure proper lighting

## 🌐 Browser Support

- Chrome (recommended)
- Firefox
- Edge
- Safari (limited support)

## 💻 Development

### Configuration Options

Modify face tracking behavior in `App.tsx`:

```typescript
const faceLandmarkerConfig = {
  baseOptions: {
    modelAssetPath: `https://storage.googleapis.com/mediapipe-models/face_landmarker/face_landmarker/float16/1/face_landmarker.task`,
    delegate: "GPU"
  },
  outputFaceBlendshapes: true,
  outputFacialTransformationMatrixes: true,
  runningMode: "VIDEO"
};
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Submit issues
- Propose new features
- Send pull requests

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- MediaPipe team for the face detection models
- React community
- Three.js community

## 📧 Contact

[YUVI] - [yubrajmahanat@gmail.com]
Project Link: [https://github.com/yuvi-Apk/FACE-LANDMARK-DETECTION]
