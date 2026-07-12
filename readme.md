# VR Architectural Walkthrough

## Overview

This project is an interactive, high fidelity architectural walkthrough built entirely in Unreal Engine using Blueprints. It is optimized for PCVR desktop platforms utilizing the OpenXR framework. The experience focuses on immersion, offering a comfortable teleportation navigation system, dynamic environmental controls, and interactive smart home features.

## Core Features

* **Custom VR Navigation:** A smooth teleportation system utilizing the Enhanced Input System and custom NavMesh bounds to ensure comfortable seated or standing traversal.
* **Dynamic Time of Day:** Users can manually rotate the sun using the right thumbstick. The Directional Light is linked to a Sky Atmosphere to create photorealistic sunsets and real time lighting changes.
* **Smart Home Automation:** Ceiling spotlights are programmed to automatically toggle visibility when the sun dips below the horizon by calculating the Forward Vector of the Directional Light.
* **Interactive Architecture:** Raycast interaction logic allows the user to point and click physical objects to trigger events, such as swapping out material elements on furniture or manually toggling light fixtures.
* **Spatial Audio:** Looping background music initializes on level load through a custom Sound Cue to enhance the atmospheric immersion.
* **Seated Experience Support:** Custom Z axis offsets applied to the VROrigin component to maintain an accurate standing height while the user is physically seated.

## Controls

* **Right Thumbstick Forward:** Cast teleportation arc
* **Right Thumbstick Release:** Execute teleportation
* **Right Thumbstick Left / Right:** Rotate time of day
* **Laser Pointer Click:** Interact with smart lights and furniture materials

## Technical Architecture

* **Engine:** Unreal Engine 5
* **Target Platform:** Windows PCVR
* **Rendering:** Forward Shading, MSAA Anti Aliasing, Screen Space Reflections
* **Logic:** 100% Visual Scripting (Blueprints)
* **Framework:** OpenXR
