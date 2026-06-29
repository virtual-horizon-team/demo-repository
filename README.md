# Virtual Horizon

Virtual Horizon is a next-generation, immersive VR training and creator platform. It allows instructors, creators, and trainees to build, edit, and interact in virtual reality with the help of a multimodal AI assistant and advanced simulation tools.

---

## 🎬 Project Pitch & Demo Video

▶️ **[Watch the Pitch & Demo Video](./Virtual_Horizon_Hackathon_Pitch_Comp.mp4)**

This video showcases the platform's vision, system architecture, core workflows (including voice/vision assistant interactions), and live gameplay demo in virtual reality.

---

## 🚀 Key Features

* **Multimodal AI Assistant:** Offline, zero-latency wake word detection ("Horizon") running locally on the VR headset, paired with real-time WebSocket audio/video streaming to a FastAPI backend powered by Gemini LLM.
* **Unity Creator SDK & Level Editor:** Author and script custom interactive scenarios using our Unity SDK, complete with a Unity-to-Lua bridge for script execution.
* **Milestone Escrow & Checkout:** Fully integrated Stripe checkout and secure milestone funding escrow flow for marketplace assets.
* **Automated Builds & Uploads:** Dedicated background services for compiling Unity AssetBundles and uploading training session records.
* **Instructor Dashboard:** A Next.js web application for instructors to manage environments, monitor user progress, and configure metadata.

---

## 🏗️ System Architecture & Repository Structure

The complete Virtual Horizon platform is split into the following main components:

1. **`VR-App/`**
   * The Meta Quest Pro VR client application built in Unity.
   * Handles local speech recognition (Vosk), mic recording, frame capture, and WebSocket networking.
2. **`front-end/`**
   * Next.js web portal for dashboard administration, scenario monitoring, and creator marketplaces.
3. **`backend/`**
   * The main .NET 9 API backend handling authentication, database storage, Stripe checkouts, and escrow logic.
4. **`rag-system/`**
   * The Python FastAPI microservice that drives the AI assistant's Ear (STT), Brain (Gemini RAG), and Mouth (TTS) modules.
5. **`com.virtualhorizon.creatorsdk/` & `Level-Editor/`**
   * Unity Creator SDK package and level editing tools, including the Lua scripting engine.
6. **`AssetBundle-BackgroundService/` & `VideoUploader-BackgroundService/`**
   * Background workers managing high-throughput assets packaging and session recordings processing.

---

## ⚙️ Development Setup

Refer to individual directories for detailed configuration steps:
* For local AI configuration and WebSocket setup, see the [rag-system README](https://github.com/virtual-horizon-team/demo-repository/tree/main/rag-system/README.md).
* For Next.js client setups, see [front-end README](https://github.com/virtual-horizon-team/demo-repository/tree/main/front-end/README.md).
* For VR client setup and deployment, see the [VR App setup guides](https://github.com/virtual-horizon-team/demo-repository/tree/main/rag-system/VR_ARCHITECTURE.md).
