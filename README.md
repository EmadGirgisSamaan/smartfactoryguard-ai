# SmartFactoryGuard  
*Building AI course project*

## Summary  
SmartFactoryGuard is an AI-powered system for gold factories that enhances security (detecting unauthorized access, suspicious behavior) and optimizes energy use (automating lighting/ventilation based on occupancy), using computer vision and anomaly detection — *Building AI course project*.

## Background  
Gold manufacturing facilities face critical challenges:  
- 🔒 **Security risks**: theft, unauthorized access to high-value zones.  
- 💡 **High energy consumption**: 24/7 lighting, ventilation, and precision equipment.  

As an Information Systems Director in a gold factory in Egypt, I see an urgent need for *proactive*, not just *reactive*, systems. Current surveillance records footage but rarely *acts*.

## How is it used?  
- **Real-time monitoring**: Cameras + sensors feed data to edge devices.  
- **Automated actions**:  
  - Person in restricted zone? → Alert + lock doors.  
  - No motion in area for >30 min? → Dim lights & reduce HVAC.  
- **Daily reports**: Energy saved vs. security incidents prevented — sent to management.

## Data sources and AI methods  
| Source | Use |
|--------|-----|
| CCTV feeds | Object detection (YOLOv8), behavior classification |
| PIR/motion sensors | Occupancy detection |
| Employee access logs | Ground truth for authorized presence |
| Power meters | Energy consumption patterns |

**AI techniques**:  
- Computer Vision (OpenCV + YOLO)  
- Anomaly Detection (Isolation Forest)  
- Time-series forecasting (Prophet) for energy optimization  

## Challenges  
- Privacy concerns with facial recognition → requires explicit consent & local processing.  
- Low-light conditions → solved with IR-enabled cameras.  
- False positives → mitigated by multi-sensor fusion (e.g., motion + badge scan).  
⚠️ *Does not replace physical security — augments it intelligently.*

## What next?  
1. 🧪 Prototype in one workshop (e.g., melting room).  
2. 📦 Integrate with existing access control & power systems.  
3. 🌐 Scale to multi-site deployment.  
Skills needed: OpenCV, TensorFlow Lite, IoT integration (MQTT), edge computing.

## Acknowledgments  
- [YOLOv8](https://github.com/ultralytics/ultralytics) / [GPL-3.0](https://github.com/ultralytics/ultralytics/blob/main/LICENSE)  
- [scikit-learn](https://scikit-learn.org) for anomaly detection  
- Inspiration: Field observations in Egyptian gold factories  
- Image (example IR sensor): [Thermal Camera by FLIR](https://commons.wikimedia.org/wiki/File:Thermal_camera_FLIR.jpg) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
