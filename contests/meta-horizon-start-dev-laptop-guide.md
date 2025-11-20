# Meta Horizon Start Developer – Laptop Setup Guide

This guide outlines the recommended hardware and software configuration for building the Quest app for the Meta Horizon Start Developer Competition.  
We recommend splitting tasks across **two laptops** to streamline development and testing.

## Laptop Q – Quest app / Start Developer Competition

This machine is dedicated to Unity development and Quest device deployment.

### 1. Unity + Android toolchain

- **Install Unity Hub** and choose a **Long‑Term Support (LTS)** version of Unity.
- Install Unity with **Android Build Support**, which includes the Android SDK/NDK and **OpenJDK**.
- **Enable OpenXR** in Project Settings once you create your project.
- Use either the **Meta XR SDK (All‑in‑One)** or the **Unity XR Interaction Toolkit** (plus **XR Hands** if you want hand‑tracking).

### 2. Quest + device tools

- Install the **Meta Quest Developer Hub (MQDH)** for device management, logs and easy installs.
- Ensure **ADB / Android platform tools** are available (verify with `adb devices`).
- Set up your **Quest headset**:
  - Enable **Developer Mode**.
  - Allow **USB debugging**.
  - Optionally enable **ADB over Wi‑Fi** for cable‑free building.

### 3. Project & repo

- Clone or create the **Quest app repository**; it can live alongside the Horizon repo.
- Ensure **Git** is installed and configured for this project.
- Optionally set up **VS Code** or **JetBrains Rider** for C# editing.

## Suggested split of responsibilities

To maximise efficiency, we recommend a two‑machine workflow:

- **Laptop H (Windows)**
  - Horizon Desktop Editor for world building, NPC setup, **Noesis/UI**, and Generative AI tools.
  - Mobile footage capture for the Creator Competition video.

- **Laptop Q (Unity‑friendly)**
  - Unity LTS with Android build support, MQDH and ADB.
  - Quest hand‑tracking & passthrough work.
  - Builds, profiling and Start Developer submission video.

---

*This guide is adapted from the internal file “Recommended ‘build’ for Alienware2.docx” and captures the essential steps to set up your hardware and software environment for the Quest side of the project.*
