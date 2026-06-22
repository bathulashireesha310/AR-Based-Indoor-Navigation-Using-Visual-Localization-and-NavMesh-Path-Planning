# AR-Based Indoor Navigation Using Visual Localization and NavMesh Path Planning

An immersive, real-time Augmented Reality (AR) indoor navigation system developed using the **Unity Engine**. This project addresses the limitations of traditional GPS-based tracking in enclosed structures by leveraging advanced computer vision and spatial mapping to provide clear, 3D path guidance overlaid directly on the physical environment.

---

## 📄 Abstract & Overview
Traditional navigation systems relying heavily on GPS perform poorly or fail entirely in indoor environments due to signal attenuation and structural obstructions. To solve this, this system integrates the **Immersal SDK** for multi-frame visual localization, **AR Foundation** for robust device tracking, and Unity’s **NavMesh** algorithm for efficient, real-time path planning. 

To enhance visual feedback, the raw waypoints are smoothed dynamically via **Catmull-Rom spline interpolation** and generated into a continuous 3D ribbon-style mesh overlay, creating an intuitive path for users to follow.

---

## 🛠️ Key Features
* **Visual Localization:** High-precision positioning using multi-image feature matching with the Immersal SDK, eliminating reliance on satellite signals.
* **Optimal Route Computation:** Utilizes Unity's NavMesh algorithm for fast, efficient path planning and automatic obstacle avoidance.
* **Smooth Path Rendering:** Implements Catmull-Rom spline interpolation and procedural mesh generation to produce fluid, natural navigation graphics.
* **Interactive UI:** Intuitive target management and UI screens for seamless destination selection (e.g., Electronics, Tools, Emergency Exits).
* **Modular Architecture:** Clean, decoupled C# modules managing state control, coordinate alignment, rendering, and localization independently[cite: 1].

---

## 🏗️ System Architecture
The application is strictly divided into functional modules ensuring scalability:
1. **Localization Module (`CustomLocalization.cs`):** Captures/buffers camera frames to align virtual space with real-world positioning.
2. **XR Coordinate Alignment Module:** Maps coordinates between the custom `XRSpace` root and local Unity space (`XRSpaceToUnity` / `UnityToXRSpace`).
3. **Navigation Module (`NavigationManager.cs`):** Manages path calculations via NavMesh and checks target distance thresholds for arrival detection.
4. **Path Rendering Module (`NavigationPath.cs`):** Generates and updates the 3D procedural path mesh at runtime.
5. **Target Management Module:** Populates destination selection tools dynamically based on preset points of interest.

---

## 💻 Tech Stack & Requirements

### Software Components
* **Development Engine:** Unity Engine
* **AR Framework:** AR Foundation (ARCore / ARKit)
* **Localization SDK:** Immersal SDK & Immersal Cloud Services
* **Language:** C#
* **IDE:** Visual Studio / VS Code

### Hardware Specifications
* **Device:** Android or iOS smartphone natively supporting ARCore or ARKit features.
* **Memory:** Minimum 4 GB RAM recommended.
* **Sensors:** High-resolution camera, gyroscope, and accelerometer for reliable motion tracking.

---

## 📊 Performance & Testing Results
The framework has been vigorously tested across multiple deployment stages—covering basic pathing, minimal-length routes, and complex environments containing structural obstacles. 
* **High Accuracy:** Validated with an average arrival positional error margin of approximately **0.18 meters**.
* **Route Optimality:** The generated paths closely track theoretical shortest paths, minimizing unnecessary detours while ensuring low computational execution times.

---

## 🔮 Future Enhancements
* **Multi-Floor Navigation:** Expanding capabilities to accommodate vertical pathfinding using stairs, elevators, and floor transitions.
* **Dynamic Obstacle Avoidance:** Integration of real-time computer vision or sensor fusion to re-route on the fly around moving barriers or crowds.
* **Voice-Based Assistance:** Audio commands to support accessibility and hands-free wayfinding.

---

## 👥 Contributors & Acknowledgements
This project was carried out as a partial fulfillment of the Bachelor of Technology in Computer Science and Engineering[cite: 1]:
* **Team Members:** Bathula Shireesha, Kovuri AnilKumar, V Vinay[cite: 1]
* **Project Supervisor:** G Anusha (Assistant Professor, VCE)[cite: 1]
* **Institution:** Vardhaman College of Engineering, Department of Computer Science and Engineering[cite: 1]