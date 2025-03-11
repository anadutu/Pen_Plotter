# Pen Plotter

A pen plotter is an output device that draws vector lines on paper using the X and Y axes.

- **Precision**: Depends on motor accuracy.
- **Common Uses**: Technical drawings, blueprints, circuit layouts.
- **Models**: Two-axis or more complex three-axis models (with pen lifting).
![image](https://github.com/user-attachments/assets/ccbb3a41-8fdf-4a77-aa31-25965edb712d)


### How It Works

Pen plotters interpret data from a computer (typically in the form of vector graphics) and translate that into physical movements using motors and controllers. The result is a tangible rendering of a digital design.

### Mechanical Design

The pen plotter operates on a Cartesian coordinate system, moving the pen along X and Y axes. Key components include:

- **Frame/Chassis**: Typically made of aluminum, steel, or acrylic, providing stability and reducing vibrations.
- **Motors**: Stepper motors control movement on the X and Y axes for precision, with some designs including a Z-axis motor for pen lifting.
- **Guide Rails and Bearings**: Linear rails ensure smooth, accurate motion along the axes.
- **Timing Belts and Pulleys**: GT2 belts convert stepper motor rotation into linear movement.
- **Pen Holder and Lift Mechanism**: A Z-axis servo motor or solenoid lifts the pen to prevent unwanted marks.
  ![image](https://github.com/user-attachments/assets/e5e9b525-6d5a-4d5f-94d1-8a39240d50c9)

# Project Analysis

The Arduino-based pen plotter is designed to autonomously draw 2D images on a flat surface by following specific vector paths. This analysis outlines the functional, non-functional, hardware, and software requirements necessary to build a precise, cost-effective plotter that is user-friendly and adaptable for various drawing or plotting needs.

The plotter will operate using two stepper motors to control the X and Y axes, while a servo motor will control the pen’s up and down movement. The system will interpret drawing instructions, such as G-code, from a computer interface or preloaded script, and execute these instructions on the drawing surface.

### System Constraints

- **Budget Constraints**: The design should use affordable, readily available components to keep the project accessible.
- **Power Consumption**: The plotter must operate efficiently within a limited power supply to avoid excessive power usage or the need for frequent recharging.
- **Size Constraints**: The device’s frame and drawing surface must fit within a standard workspace, such as a desk or table.

# Functional Requirements

### User Interface Requirements

- **Load Design File**  
  The system should allow the user to load a vector-based drawing file, such as SVG or G-code, through a graphical user interface (GUI) or preloading onto the Arduino.

- **Start/Stop Plotting**  
  The user must be able to initiate and terminate the drawing process from the GUI or by pressing a physical button on the plotter.

- **Pause/Resume Plotting**  
  The system should support pausing and resuming the plotting operation without loss of data, ensuring continuity in drawing.

- **Manual Control of Pen Position**  
  Users should have the option to manually adjust the pen position along the X and Y axes to fine-tune alignment before initiating the plot.

### Plotter Operation Requirements

- **Coordinate Control**  
  The plotter should accurately interpret and execute X, Y coordinate instructions for precise pen movement.

- **Pen Up/Down Control**  
  The plotter must control the pen’s vertical position using a servo motor to allow drawing and lifting movements in response to plotting commands.

### File Compatibility

- **G-code Compatibility**  
  The system should interpret G-code for plotting to ensure compatibility with common drawing software.

- **SVG Interpretation**  
  If possible, the GUI should accept SVG files and convert them into G-code for the plotter to execute.


# Hardware Components (Arduino, Motors, etc.)

The hardware implementation of this Arduino-based pen plotter will require the following components:

### Mechanical Parts

- 4 pcs 40 cm 8mm Threaded Rod ~ 4 x 15 RON ~ 60 RON
- 4 pcs 30 cm 8mm Mild Steel Rod ~ 20 RON
- 6 pcs LM8UU Bearings ~ 6 x 5 RON ~ 30 RON
- 4 pcs 623ZZ Bearings ~ 4 x 6 RON ~ 24 RON
- 2 pcs GT2 20 Teeth Pulley ~ 2 x 5 RON ~ 10 RON
- 1 pcs GT2 6mm 150 cm long Belt ~ 20 RON

### Electric Parts

- 1 pcs Arduino Uno ~ 50 RON
- 1 pcs V3 CNC Shield ~ 20 RON
- 2 pcs Nema17 Stepper Motors ~ 2 x 50 RON ~ 100 RON
- 1 pcs MG90 Servo Motor ~ 20 RON
- 2 pcs A4988 Stepper Motor Drivers ~ 2 x 7 RON ~ 14 RON
- 6 pcs Short Circuit Jumpers ~ 6 x 1 RON ~ 6 RON
- 1 pcs 12V 1A Adapter ~ 15 RON
- 1 pcs 1.5 meter A to B USB Cable ~ 10 RON

**Total estimated cost: ~399 RON**
# Construction of the Plotter

The plotter's construction was meticulously planned and handcrafted to ensure precision and functionality. Here are the key details:

### Frame and Structural Components

- The plotter’s structure was made using 10 custom-cut wooden pieces, specifically measured and designed for this project.
- These wood pieces formed the base and support arms, providing stability and alignment for all components.

### Guiding and Movement System

- **Linear Guides**: 4 steel rods were used to ensure smooth and precise movement of the plotter arms.
- **Mechanical Actuation**: 4 threaded rods were implemented to provide controlled linear motion along the X and Y axes.
- **Motion Transmission**: 2 toothed pulleys, driven by the stepper motors, were used to transmit motion.

### Bearings for Smooth Operation

A total of 6 bearings were strategically placed:
- **Plotter Arms**: Four bearings supported the plotter arms, enabling seamless horizontal movement.
- **Pen Support Mechanism**: Two bearings were integrated into the pen support mechanism, ensuring smooth vertical movement when raising or lowering the pen.

### Pen Support Mechanism

- The pen support was designed to move vertically, controlled by a servo motor.
- A precise combination of bearings and structural support was used to ensure stable and accurate pen placement during operation.

This carefully constructed design ensured the plotter operated with high accuracy and reliability, reflecting the thoughtful integration of handcrafted components and mechanical systems.

![image](https://github.com/user-attachments/assets/b98cd766-18d8-4f1b-9589-3b8cb3827c07)


![image](https://github.com/user-attachments/assets/ec41bfc2-2126-4bf5-b946-91511116f530)


# Electronics of the Plotter

The electronic setup of the plotter was designed to control its precise movements and pen positioning. The main components included:

### Microcontroller

- **Arduino Uno**: Served as the central control unit, coordinating the movements of the motors and processing G-code commands.

### Motors and Drivers

- **Stepper Motors**: Two 28BYJ-48 stepper motors, each paired with ULN2003 driver boards, controlled the X and Y axis movements of the plotter arms.
- The stepper motors and their drivers ensured accurate positioning by translating digital signals into precise rotational or linear motion.

### Pen Mechanism

- **Servo Motor (MG90)**: Used to raise and lower the pen, providing precise vertical movement essential for drawing and stopping without damaging the surface.

### Power Supply and Connections

- **External Power Supply**: Powered all components, ensuring the motors received sufficient voltage and current for smooth operation.
- **Wiring**: All power and signal connections were routed through a breadboard for organized and secure wiring.

This robust electronic configuration worked seamlessly with the mechanical design, enabling precise control over the plotter's functions.
![image](https://github.com/user-attachments/assets/7091c740-b846-4c34-b593-b2fa6792dd71)

