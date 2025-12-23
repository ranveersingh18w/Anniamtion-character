# Animation Character - CYBERFICTION

A stunning scroll-based animation project that brings characters to life using sequential image frames. Create smooth, cinematic animations that respond to user scrolling.

![Project Demo](https://img.shields.io/badge/demo-live-brightgreen)

## 🌟 Features

- **Scroll-based Animation**: 300 frames of smooth animation triggered by scrolling
- **Responsive Design**: Works seamlessly across different screen sizes
- **Customizable**: Easy to replace images with your own animation sequence
- **Smooth Scrolling**: Powered by Locomotive Scroll for buttery-smooth experience
- **Modern Tech Stack**: Built with HTML5 Canvas, GSAP, and ScrollTrigger

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- A local web server (optional, but recommended for development)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ranveersingh18w/Anniamtion-character.git
cd Anniamtion-character
```

2. Open `index.html` in your web browser or use a local server:
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

3. Navigate to `http://localhost:8000` in your browser

## 🎨 Customizing Your Animation

### How to Replace Images with Your Own

1. **Prepare Your Images**:
   - Create a sequence of images for your animation (e.g., 300 frames)
   - Export them as PNG files (recommended for transparency)
   - Use consistent dimensions (current images are 1920x1080)
   - Name them sequentially (see naming convention below)

2. **Image Naming Convention**:
   ```
   yourname0001.png
   yourname0002.png
   yourname0003.png
   ...
   yourname0300.png
   ```
   - Use 4-digit numbering with leading zeros
   - Keep the prefix consistent (e.g., "yourname", "character", "animation")

3. **Update the Code**:
   
   Open `script.js` and modify the `files()` function (starting at line 49):
   
   ```javascript
   function files(index) {
     var data = `
        ./yourname0001.png
        ./yourname0002.png
        ./yourname0003.png
        // ... add all your image paths
        ./yourname0300.png
     `;
     return data.split("\n")[index];
   }
   ```
   
   Replace all the image paths in the `data` string (lines 50-351) with your own image paths.

4. **Adjust Frame Count** (if needed):
   
   If you have more or fewer than 300 frames, update line 355:
   ```javascript
   const frameCount = 300; // Change to your number of frames
   ```

5. **Replace the Image Files**:
   - Delete the existing `male0001.png` through `male0300.png` files
   - Add your new image sequence to the project directory

### Image Requirements

- **Format**: PNG, JPG, or WebP (PNG recommended for quality and transparency)
- **Dimensions**: Consistent across all frames (e.g., 1920x1080)
- **File Size**: Optimize images to keep them under 500KB each for better performance
- **Count**: Minimum 30 frames recommended; 300 frames for smooth animation

### Tips for Creating Animation Sequences

- **Video to Frames**: Use video editing software (Adobe After Effects, Premiere Pro) or tools like FFmpeg to export video frames
- **3D Animation**: Export frames from Blender, Maya, or Cinema 4D
- **Stop Motion**: Capture sequential photos and export them
- **Sprite Sheets**: Convert sprite sheets to individual frames using tools

**FFmpeg Example** (convert video to frames):
```bash
ffmpeg -i your_video.mp4 -vf fps=30 yourname%04d.png
```

## 🛠️ Technology Stack

- **HTML5**: Structure and Canvas element
- **CSS3**: Styling and animations
- **JavaScript**: Animation logic and interactivity
- **GSAP (GreenSock Animation Platform)**: Professional-grade animation
- **ScrollTrigger**: Scroll-based animations
- **Locomotive Scroll**: Smooth scrolling effects

## 📁 Project Structure

```
Anniamtion-character/
├── index.html          # Main HTML file
├── style.css           # Styling
├── script.js           # Animation logic
├── male0001.png        # Animation frame 1
├── male0002.png        # Animation frame 2
├── ...
└── male0300.png        # Animation frame 300
```

## 🎯 How It Works

1. **Image Loading**: All 300 frames are preloaded into memory
2. **Scroll Detection**: Locomotive Scroll detects user scrolling
3. **Frame Calculation**: ScrollTrigger calculates which frame to display based on scroll position
4. **Canvas Rendering**: The current frame is drawn on the HTML5 Canvas
5. **Smooth Transition**: GSAP ensures smooth transitions between frames

## 🎮 Usage

Simply scroll down the page to see the character animation come to life! The animation is synchronized with your scrolling speed.

## 🔧 Customization Options

### Adjust Animation Speed

Modify the `scrub` value in `script.js` (line 373):
```javascript
scrollTrigger: {
  scrub: 0.15,  // Lower = faster, Higher = slower
  // ...
}
```

### Change Animation Length

Modify the `end` value in `script.js` (line 376):
```javascript
scrollTrigger: {
  // ...
  end: `600% top`,  // Adjust percentage for longer/shorter scroll
}
```

### Modify Content

Edit the text content in `index.html` to match your project theme.

## 📝 License

This project is open source and available for personal and educational use.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 👨‍💻 Author

Created with ❤️ by the community

## 🙏 Acknowledgments

- GSAP for the amazing animation library
- Locomotive Scroll for smooth scrolling
- Original concept inspiration from CYBERFICTION

---

**Happy Animating! 🎬✨**
