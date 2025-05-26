# 📸 Arduino OV7670 Camera Viewer

<div align="center">
  <img src="https://via.placeholder.com/800x400.png?text=OV7670+Real-time+Video+Capture" alt="Demo">
  <br>
  <img src="https://img.shields.io/badge/Arduino-Mega%202560-blue?logo=arduino" alt="Arduino">
  <img src="https://img.shields.io/badge/Camera-OV7670-green" alt="OV7670">
  <img src="https://img.shields.io/badge/OpenCV-4.5+-orange?logo=opencv" alt="OpenCV">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="License">
</div>

## 🌟 Features

<div align="center">
  <table>
    <tr>
      <td><img width="200" src="https://via.placeholder.com/200x150.png?text=Real-time+Capture" alt="Real-time"></td>
      <td><img width="200" src="https://via.placeholder.com/200x150.png?text=Multiple+Formats" alt="Formats"></td>
      <td><img width="200" src="https://via.placeholder.com/200x150.png?text=OpenCV+Processing" alt="Processing"></td>
    </tr>
    <tr>
      <td align="center"><b>30FPS Capture</b></td>
      <td align="center"><b>RGB565/YUV422</b></td>
      <td align="center"><b>Computer Vision</b></td>
    </tr>
  </table>
</div>

- **Real-time video** at QVGA (320x240) resolution
- **Multiple color formats** supported
- **On-screen controls** for camera adjustment
- **OpenCV processing pipeline** with filters
- **Cross-platform** compatibility

## 🛠 Hardware Setup

```mermaid
graph TD
    A[Arduino Mega] -->|3.3V| B(OV7670)
    A -->|GND| B
    A -->|D0-D7| B
    A -->|XCLK| B
    A -->|PCLK| B
    A -->|VSYNC| B
    A -->|HREF| B
    A -->|SIOC| B
    A -->|SIOD| B
```

**Component List**:
- Arduino Mega 2560
- OV7670 Camera Module
- 3.3V Voltage Regulator
- 8MHz Crystal Oscillator
- 10kΩ Resistors (x4)
- 0.1µF Capacitors (x10)

## 💻 Software Installation

```bash
# Clone repository
git clone https://github.com/yourusername/arduino-camera-viewer.git
cd arduino-camera-viewer

# Install dependencies
pip install -r requirements.txt  # Python
# OR
mkdir build && cd build && cmake .. && make  # C++
```

## 🎮 Usage

```python
python viewer.py \
    --port COM3 \
    --resolution 320 240 \
    --format RGB565 \
    --fps 30
```

**Keyboard Controls**:
| Key | Function |
|-----|----------|
| `+/-` | Adjust brightness |
| `r` | Reset camera |
| `s` | Save frame |
| `p` | Toggle processing |

## 📊 Performance

```mermaid
pie
    title Frame Rate by Resolution
    "160x120" : 45
    "320x240" : 30
    "640x480" : 15
```

## 🖼️ Sample Outputs

<div align="center">
  <img width="30%" src="https://via.placeholder.com/320x240.png?text=Raw+Capture" alt="Raw">
  <img width="30%" src="https://via.placeholder.com/320x240.png?text=Edge+Detection" alt="Edge">
  <img width="30%" src="https://via.placeholder.com/320x240.png?text=Color+Threshold" alt="Threshold">
</div>

## 🚀 Quick Start Guide

1. [Download Arduino IDE](https://www.arduino.cc/en/software)
2. Upload `arduino/ov7670_capture.ino`
3. Connect camera as per wiring diagram
4. Run the viewer application:
   ```bash
   python viewer.py --port YOUR_PORT
   ```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---

<div align="center">
  <img src="https://img.shields.io/github/stars/yourusername/arduino-camera-viewer?style=social" alt="GitHub Stars">
  <br>
  <sub>Built with ❤️ by <a href="https://github.com/yourusername">Your Name</a></sub>
</div>
```
