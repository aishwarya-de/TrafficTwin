# TrafficTwin 🚦

**TrafficTwin** is a software-based traffic digital twin. A **digital twin** is a virtual replica of a physical system. In this project, TrafficTwin simulates urban traffic flows, road intersections, vehicles, and traffic signals in real time to analyze congestion, test scenarios, and optimize signal timing.

---

## 🎯 Project Goal

To build an end-to-end digital twin system that combines:
1. **Microscopic Traffic Simulation**: High-fidelity traffic movement using Eclipse SUMO.
2. **Real-Time Simulation Control**: Python interfacing with SUMO via TraCI (Traffic Control Interface).
3. **Machine Learning & Analytics**: Predicting congestion and testing intelligent signal timing strategies.
4. **Interactive Dashboard**: A user-friendly web interface to observe and interact with the twin.

---

## 🧭 Key Concepts (For Beginners)

* **Eclipse SUMO (Simulation of Urban MObility)**:
  An open-source, highly portable, microscopic road traffic simulation package. "Microscopic" means every single vehicle and traffic light has its own identity, speed, and route.
* **TraCI (Traffic Control Interface)**:
  A TCP-based client/server library that connects Python code directly to a running SUMO simulation. It allows Python to query simulation state (e.g., vehicle speeds, waiting times) and modify behaviors on the fly (e.g., change traffic light phases).
* **Digital Twin**:
  A software model continuously synchronized with data from the real or simulated environment, enabling prediction, what-if analysis, and automated decision-making.

---

## 📁 Project Structure

```text
TrafficTwin/
├── .venv/               # Python virtual environment (isolated libraries)
├── .gitignore           # Ignores virtual env, cache, and SUMO output files
├── README.md            # Project documentation and beginner guide
├── simulations/         # SUMO network files (.net.xml), routes (.rou.xml), and configs (.sumocfg)
├── src/                 # Python source code for simulation logic and controllers
├── data/                # Datasets, logs, and simulation output data
└── docs/                # Architecture diagrams, research notes, and setup guides
```

---

## 🛠️ Prerequisites & Status

| Tool | Purpose | Current Status |
| :--- | :--- | :--- |
| **Python (3.11+)** | Programming language for logic, TraCI, and ML | Installed & Verified |
| **Git** | Source control and version tracking | Installed & Initialized |
| **Eclipse SUMO** | Physics and traffic simulation engine | **Pending Installation** (See below) |

---

## 🚀 Getting Started

### 1. Activating the Python Virtual Environment

On Windows (PowerShell):
```powershell
.\.venv\Scripts\Activate.ps1
```

If you encounter an execution policy restriction in PowerShell, you can run:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```
Or use the Command Prompt (`cmd`):
```cmd
.\.venv\Scripts\activate.bat
```

To deactivate when finished:
```powershell
deactivate
```

---

## ⚙️ SUMO Installation Note

SUMO is required to run traffic simulations. Since automatic installation is disabled:

1. Download the official installer from the [Eclipse SUMO Downloads page](https://eclipse.dev/sumo/).
2. Run the Windows installer (e.g. `sumo-win64-<version>.msi`).
3. Ensure the environment variable `SUMO_HOME` is set to your SUMO directory (e.g., `C:\Program Files (x86)\Eclipse\Sumo`).
4. Ensure `<SUMO_HOME>\bin` is added to your system `PATH`.
5. Verify in a terminal by running:
   ```powershell
   sumo --version
   ```

---

## 🗺️ Project Roadmap

- [x] **Stage 0: Project Setup & Environment Baseline** (Current)
- [ ] **Stage 1: Basic SUMO Road Network & Scenario Setup**
- [ ] **Stage 2: TraCI & Python Real-time Controller**
- [ ] **Stage 3: Data Logging & Machine Learning Analytics**
- [ ] **Stage 4: Interactive Web Dashboard**
