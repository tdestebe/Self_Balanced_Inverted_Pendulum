# Self_Balanced_Inverted_Pendulum

Self Balanced Inverted Pendulum

This project aims to build an inverted pendulum stabilized by a single reaction wheel. The position of the pendulum is detected by a 3-axis analog gyroscope sensor (MPU6050 module). The position is analyzed inside an Arduino Uno that sends appropriate signals to a motor (Nidec 24H404H160). 

## 3D CAD Model

The assembly of the CAD models and parts are designed with FreeCAD. Following worbenchs are used:

- **Part design** to design 3D mechanical parts

- **Assembly 4.1** based on local axis systems

- **Fasteners** for all screws and nuts

- **Mesh** to create and export STL files

<img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/pictures/inverted_pendulum_3D_view.png" />

**Inverted pendulum - FreeCAD mesh export**

FreeCAD files are available at [freeCad](https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/tree/main/freeCad)

STL 3D files are at [STL_files](https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/tree/main/STL_files)

## Simulation with openModelica

Simulation is performed through an openModelica implementation into the package SelfBalancedWheelPackage. Main Modelica model **SingleWheelRobot** calls model **Dynamics** in which PID, Motor, etc are implemented and calls model **Animation** to display rotation of 3D models of the reaction wheel and the arm. 

<img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/pictures/SingleWheelRobot.svg" />

**Inverted pendulum - Modelica main model**

<table border="0" style="width: 100%;">
  <!-- Current Row -->
  <tr>
    <th style="border: none; text-align: center; font-weight: bold;"><img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/pictures/Dynamics.svg" /></th>
    <th style="border: none; text-align: center; font-weight: bold;"><p>    </p></th>
    <th style="border: none; text-align: center; font-weight: bold;"><img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/pictures/Animation.svg" /></th>
  </tr>
  <!-- Header Rows -->
  <tr>
    <td style="border: none;"><b>Inverted pendulum - Modelica Dynamics model</b></td>
    <td style="border: none; text-align: center; font-weight: bold;"><p>    </p></td>
    <td style="border: none;"><b>Inverted pendulum - Modelica Animation model</b></td>
  </tr>
</table>

Source files are available at [Self Balaced Wheel Package](https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/tree/main/SelfBalancedWheelPackage)

## Arduino code and circuits

### Code (.ino)

The source code for Arduino is provided at [code](https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/tree/main/code). It is similar to the code written by **Remigijus** (see [remrc - One-Axis-Reaction-Wheel-Stick](https://github.com/remrc/One-Axis-Reaction-Wheel-Stick)).

### Fritzing schema

The schema is also identical to the original one posted by Remigijus. I just rewrote it with Fritzing, including a breadboard and stored the source at [circuit](https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/tree/main/circuit).

<table border="0" style="width: 100%;">
  <!-- Current Row -->
  <tr>
    <th style="border: none; text-align: center; font-weight: bold;"><img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/circuit/schema.png" /></th>
    <th style="border: none; text-align: center; font-weight: bold;"><p>    </p></th>
    <th style="border: none; text-align: center; font-weight: bold;"><img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/circuit/schema_breadboard.png" /></th>
  </tr>
  <!-- Header Rows -->
  <tr>
    <td style="border: none;"><b>Fritzing schema - Original</b></td>
    <td style="border: none; text-align: center; font-weight: bold;"><p>    </p></td>
    <td style="border: none;"><b>Fritzing schema - Breadboard</b></td>
  </tr>
</table>

### KiCad circuit

In addition to Fritzing schema, I implemented KiCad schematic circuit and generated a KiCad PCB for visualisation into the 3D CAD assembly. 

Kicad project is stored at [kiCAD](https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/tree/main/kiCAD).

<table border="0" style="width: 100%;">
  <!-- Current Row -->
  <tr>
    <th style="border: none; text-align: center; font-weight: bold;"><img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/kiCAD/schema.png" /></th>
    <th style="border: none; text-align: center; font-weight: bold;"><p>    </p></th>
    <th style="border: none; text-align: center; font-weight: bold;"><img width="298" height="500" alt="thumbnail" src="https://github.com/tdestebe/Self_Balanced_Inverted_Pendulum/blob/main/kiCAD/PCB_3D_view.png" /></th>
  </tr>
  <!-- Header Rows -->
  <tr>
    <td style="border: none;"><b>KiCad circuit - Schema</b></td>
    <td style="border: none; text-align: center; font-weight: bold;"><p>    </p></td>
    <td style="border: none;"><b>KiCad circuit - PCD 3D view</b></td>
  </tr>
</table>
