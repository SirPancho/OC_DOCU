Open Commissioning is an open-source virtual commissioning framework that combines **Unity** for 3D simulation, **TwinCAT** for real-time device emulation, and an **Assistant Application** for engineering and project generation. Its goal is to enable soft-/hardware-in-the-loop testing with minimal differences between virtual and real commissioning environments.

# 1. Introduction

## What is Open Commissioning?

Open Commissioning provides a framework for creating digital twins and testing PLC programs against virtual machine models before physical commissioning. The platform is built around three core components:

1. **Unity Package**
    
    - Models machine geometry, kinematics, sensors, actuators, and material flow. [[github.com]](https://github.com/OpenCommissioning)
2. **TwinCAT Library**
    
    - Represents industrial devices and provides real-time simulation and communication. [[github.com]](https://github.com/OpenCommissioning), [[doc.realvirtual.io]](https://doc.realvirtual.io/components-and-scripts/interfaces/opencommissioning)
3. **Assistant Application**
    
    - Generates projects, scans configurations, and manages communication between Unity, TwinCAT, and external interfaces. [[github.com]](https://github.com/OpenCommissioning)

---

# 2. Prerequisites

Before starting, install:

- Unity Editor
- TwinCAT 3
- Open Commissioning Unity Package
- Open Commissioning TwinCAT Libraries
- Open Commissioning Assistant Application [[github.com]](https://github.com/OpenCommissioning), [[doc.realvirtual.io]](https://doc.realvirtual.io/components-and-scripts/interfaces/opencommissioning)

Recommended knowledge:

- Unity scene creation
- PLC programming
- TwinCAT engineering
- Industrial automation concepts

---

# 3. Tutorial Roadmap

The official Open Commissioning tutorial series covers the following topics: [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

|Tutorial|Topic|
|---|---|
|1|Getting Started|
|2|Material Flow Introduction|
|3|Generating TwinCAT Project|
|4|Modeling a Linear Drive|
|5|Connecting Siemens PLCSIM Advanced|
|6|Connecting ABB RobotStudio|
|7|Connecting KUKA OfficeLite|
|8|Modeling a Transport Line|

---

# 4. Getting Started

## Step 1: Install the Unity Package

Open Unity Package Manager and add the Open Commissioning package from GitHub. The package contains the core framework required for simulation and communication. [[doc.realvirtual.io]](https://doc.realvirtual.io/components-and-scripts/interfaces/opencommissioning), [[github.com]](https://github.com/OpenCommissioning)

## Step 2: Create a New Scene

Create a new Unity scene representing your machine or production cell.

Typical structure:

```
Machine  

├── Drives  

├── Sensors  

├── Conveyors  

├── Products  

└── Controllers
```

The Unity scene becomes the digital twin that interacts with PLC logic. [[github.com]](https://github.com/OpenCommissioning)

## Step 3: Configure Communication

Add the Open Commissioning communication component (TcAdsClient) to the top-level scene object and configure the TwinCAT ADS connection parameters. [[doc.realvirtual.io]](https://doc.realvirtual.io/components-and-scripts/interfaces/opencommissioning)

---

# 5. Material Flow Modeling

Material flow is introduced in Tutorial 2 and forms the basis for conveyor and transport simulations. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

## Workflow

1. Create conveyor objects.
2. Define product objects.
3. Configure movement paths.
4. Add sensors along transport routes.
5. Connect sensors to TwinCAT variables.

Typical use cases:

- Pallet handling
- Packaging systems
- Production lines
- Logistics automation

---

# 6. Generating a TwinCAT Project

Tutorial 3 demonstrates automated TwinCAT project generation. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

## Process

### Scan Unity Scene

Open Commissioning reads the hierarchy of sensors, actuators, and machine elements. [[github.com]](https://github.com/OpenCommissioning)

### Generate Device Structure

A matching structure is created inside TwinCAT so PLC variables correspond directly to Unity components. [[github.com]](https://github.com/OpenCommissioning)

### Build PLC Interface

The generated interface establishes communication between:

- Unity simulation
- TwinCAT runtime
- PLC logic

This significantly reduces manual engineering effort. [[github.com]](https://github.com/OpenCommissioning)

---

# 7. Modeling a Linear Drive

Tutorial 4 shows how to create a simple linear axis model from scratch. [[youtube.com]](https://www.youtube.com/watch?v=R3KGJ8bpJMY), [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos)

## Steps

### Create Mechanical Geometry

Build the moving carriage and guide components in Unity.

### Define Motion Behavior

Configure:

- Position
- Speed
- Acceleration
- Travel limits

### Add Sensors

Typical sensors include:

- Home sensor
- End-position sensor
- Safety limits

### Connect to TwinCAT

Map motion commands and feedback signals to PLC variables.

Result:

The virtual drive behaves similarly to a physical axis under PLC control. [[youtube.com]](https://www.youtube.com/watch?v=R3KGJ8bpJMY), [[github.com]](https://github.com/OpenCommissioning)

---

# 8. Connecting External Controllers

## Siemens PLCSIM Advanced

Tutorial 5 demonstrates integration with Siemens PLCSIM Advanced. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

Purpose:

- Validate Siemens PLC programs
- Test logic without physical hardware
- Perform virtual commissioning

---

## ABB RobotStudio

Tutorial 6 covers ABB RobotStudio integration. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

Benefits:

- Robot simulation
- Motion testing
- Digital twin validation

---

## KUKA OfficeLite

Tutorial 7 explains KUKA OfficeLite controller connectivity. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

Benefits:

- Virtual robot commissioning
- Program validation
- Cell-level simulation

---

# 9. Building a Transport Line

Tutorial 8 combines previously learned concepts into a complete transport system. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)

## Recommended Approach

### Design Layout

Create:

- Conveyors
- Transfer stations
- Buffers
- Sensors

### Configure Product Flow

Define:

- Entry points
- Routing logic
- Exit points

### Generate TwinCAT Integration

Use the Assistant to create the corresponding PLC structure. [[github.com]](https://github.com/OpenCommissioning)

### Validate Operation

Test:

- Product movement
- Sensor triggering
- PLC response
- Error scenarios

---

# 10. Best Practices

### Keep Naming Consistent

Use descriptive names:

```
Conveyor_01  

Sensor_Infeed  

Drive_MainAxis
```

### Build Modular Models

Create reusable machine modules rather than monolithic scenes.

### Test Incrementally

Validate:

1. Mechanics
2. Sensors
3. Communication
4. PLC functions

### Maintain One-to-One Mapping

Keep Unity objects aligned with TwinCAT structures whenever possible. [[github.com]](https://github.com/OpenCommissioning)

---

# 11. Architecture Overview

```
+--------------------+  

| Unity Digital Twin |  

+----------+---------+  

|  

| ADS / Shared Data  

|  

+----------v---------+  

| Open Commissioning |  

| Communication |  

+----------+---------+  

|  

+----------v---------+  

| TwinCAT Runtime |  

+----------+---------+  

|  

+----------v---------+  

| PLC / Robot Ctrl |  

+--------------------+
```

This architecture enables virtual commissioning with realistic PLC and controller interaction before deploying to real equipment. [[github.com]](https://github.com/OpenCommissioning), [[doc.realvirtual.io]](https://doc.realvirtual.io/components-and-scripts/interfaces/opencommissioning)

---

# References

- Open Commissioning GitHub Organization and documentation. [[github.com]](https://github.com/OpenCommissioning), [[github.com]](https://github.com/orgs/OpenCommissioning/repositories)
- Open Commissioning YouTube Tutorial Series. [[youtube.com]](https://www.youtube.com/@OpenCommissioning/videos), [[youtube.com]](https://www.youtube.com/playlist?list=PL4wm_B3zATQavAq8Ec7PO-u7in6N0FjUg)
- Open Commissioning Interface Documentation (realvirtual.io). [[doc.realvirtual.io]](https://doc.realvirtual.io/components-and-scripts/interfaces/opencommissioning)

**Note:** The YouTube series provides demonstrations rather than exhaustive written instructions. For a production-grade manual, combining the tutorial videos with the GitHub repositories and source code documentation is recommended.

