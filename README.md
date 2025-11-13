AI Farm Land Sentry

An interactive project dashboard for an AI-powered autonomous turret designed to humanely protect farm lands from animal pests.

This repository contains the web-based project explorer and dashboard for the AI Farm Land Sentry. This system is a non-lethal, automated deterrent that removes the need for manual patrols or hazardous electric fences, offering an intelligent, humane, and safe solution for crop protection.

📖 Table of Contents

About The Project

✨ Key Features

🏗️ System Architecture

🚀 Technologies Used

🛡️ Safety & Ethical Protocols

🏁 Getting Started

License

Contact

About The Project

The AI Farm Land Sentry is an autonomous system that uses real-time object detection to identify specific animal pests and deter them with a harmless projectile (like a paintball). A primary design principle is safety, with a robust "Safe Mode" that immediately activates upon detecting a human.

Primary Targets:

Formosan Macaque (Macaca cyclopis)

Formosan Muntjac (Muntiacus reevesi micrurus)

Formosan Black Bear (Ursus thibetanus formosanus)

Formosan Wild Boar (Sus scrofa taivanus)

Critical Avoidance:

Human: The system enters a complete "Safe Mode" on human detection.

This web interface serves as a complete guide to the project, from its high-level architecture to the individual components and build steps.

✨ Key Features

This project dashboard provides a comprehensive overview of the AI Sentry:

Interactive 3D Model: Explore a detailed, 360° 3D model of the turret's mechanical design.

System Architecture: An interactive diagram explaining the "Perception-Decision-Actuation" loop.

Live Visual Feed: A mock-up of the real-time 360° video feed from the tri-camera array, complete with compass headings.

System Monitoring: A dashboard to simulate monitoring shot count, HPA gas level, and ammo hopper status, with functional controls.

Interactive Bill of Materials (BOM): A complete, filterable, and searchable list of all hardware components. Includes a breakdown of component categories by cost or quantity and details the software stack.

Interactive Build Guides: A step-by-step guide through the four phases of the project:

Mechanical Assembly

Electronics & Wiring

AI Model & Software

Calibration & Testing

Safety Protocols: A dedicated section outlining the mandatory, non-negotiable safety features of the system.

🏗️ System Architecture

The sentry operates on a classic Perception-Decision-Actuation loop:

Perception: A 360° panoramic view is created by stitching feeds from a tri-camera array (3x Logitech C615 webcams).

Decision: The NVIDIA Jetson Orin Nano processes all video feeds in real-time, running a custom-trained YOLO AI model to detect and classify objects.

Actuation: If a target is identified (and no human is present), the Jetson commands NEMA 23 stepper motors to aim the turret. It then fires a projectile via a 24V solenoid.

🚀 Technologies Used

This project is divided into two main parts: the web dashboard and the physical sentry system.

1. Project Dashboard (This Repository):

HTML5

Tailwind CSS

JavaScript (ES6+)

Chart.js: For the component category chart.

Google <model-viewer>: For the interactive 3D model.

2. Core Sentry System (Physical Build):

Computing: NVIDIA Jetson Orin Nano

AI Framework: Ultralytics YOLO (v8+)

Core Language: Python 3

Key Libraries: OpenCV, TensorRT, RPi.GPIO

Hardware: NEMA 23 Motors, DM542S Drivers, 24V Solenoid, 12V PSU

🛡️ Safety & Ethical Protocols

Safety is the highest priority for this system. These protocols are mandatory and non-negotiable.

🛑 Physical E-Stop: A large, red, physical "Emergency Stop" button is wired to cut all power to the motors and firing solenoid, providing a foolproof hardware-level override.

🛡️ Robust Human Detection: The "Safe Mode" is the primary software defense. The confidence threshold for human detection is set conservatively low to prioritize avoiding false negatives.

🗺️ Geofencing: The turret's operational range is programmatically limited to prevent it from aiming or firing outside the designated protected area.

👀 Supervised Operation: The system must never be left completely unattended. A human operator must always be present and able to intervene.

🏁 Getting Started

To explore this project dashboard, no installation is needed. Simply open the index.html file in any modern web browser.

# Clone the repository (optional)
git clone [https://github.com/brianhexer/AI-Farm-Land-Sentry.git](https://github.com/brianhexer/AI-Farm-Land-Sentry.git)

# Navigate to the directory
cd AI-Farm-Land-Sentry-main

# Open the main file
# (On most systems, you can just double-click index.html)


License

This project is licensed under the MIT License - see the LICENSE.md file for details.

Contact

Brian - https://github.com/brianhexer
