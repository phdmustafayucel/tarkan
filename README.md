# TARKAN

TARKAN is a Python-based client–server control framework for laboratory instrumentation.
It provides a modular architecture to remotely control, synchronize, and automate
multiple hardware devices through a unified interface and graphical user interface (GUI).

The project was developed in a research context and is structured to support
reproducible experiments, device abstraction, and scalable instrument control.

---

## Overview

TARKAN implements a distributed control system where:
- A central server manages hardware resources
- Clients send commands and receive data
- A GUI layer allows interactive experiment control
- Each instrument is encapsulated in its own Python module

Supported devices include:
- SuperK laser systems
- WinSpec spectrometers
- Thorlabs motorized stages
- HMP4040 power supplies

---

## Architecture

The project follows a layered design:

- Server layer: device management and command execution
- Client layer: communication with the server
- GUI layer: experiment control and visualization
- Device modules: hardware-specific logic

Communication is handled via Python sockets and multiprocessing.

---

## Repository Structure

tarkan/
├── server/
│   ├── server.py            # Main server entry point
│   ├── worker.py            # Worker processes for command handling
│   ├── loggingProc.py       # Centralized logging
│   ├── utils.py             # Server utilities
│   └── server.config        # Server configuration file
│
├── client/
│   ├── client.py            # Client entry point
│   └── clientClass.py       # Client communication logic
│
├── gui/
│   ├── gui_run.py           # GUI launcher
│   ├── measurement.py      # Measurement logic
│   ├── optimization.py     # Optimization routines
│   └── test_folder/        # Stored experimental data and plots
│
├── SuperK/
│   ├── superkClass.py       # SuperK laser control
│   ├── SuperKControlFrame.py# GUI frame for SuperK
│   ├── comClass.py          # Communication helpers
│   └── utility.py           # Utility functions
│
├── WinSpec/
│   ├── WinSpecClass.py      # Spectrometer control
│   └── WinSpecControlFrame.py# GUI frame for WinSpec
│
├── HMP4040/
│   ├── hmp4040Class.py      # Power supply control
│   └── hmp4040ControlFrame.py# GUI frame
│
├── m30xy/
│   ├── m30xyClass.py        # Thorlabs stage control
│   └── m30xyControlFrame.py # GUI frame
│
└── __init__.py

---

## Server–Client Model

- The server maintains exclusive access to hardware devices
- Clients send structured commands to the server
- Worker processes handle commands asynchronously
- Results and data are returned to the client or GUI

This design prevents device conflicts and allows multiple clients.

---

## Running the Server

From the project root:

python server/server.py

Ensure all required hardware drivers and Python dependencies
are installed before starting the server.

---

## Running the Client

python client/client.py

The client connects to the server using the configuration
defined in server.config.

---

## Running the GUI

python gui/gui_run.py

The GUI provides:
- Device control panels
- Measurement execution
- Data acquisition
- Real-time plotting and saved results

---

## Data Handling

Experimental results are stored as:
- Pickle (.pkl) files for raw data
- PNG files for plotted outputs

Data is organized by timestamp and experiment type.

---

## Development Notes

- Each device is encapsulated in its own Python class
- GUI control frames mirror device classes
- Multiprocessing is used to isolate hardware access
- The server is the single point of truth for device state

---

## Intended Use

This project is intended for:
- Research laboratories
- Experimental automation
- Multi-device synchronization
- Rapid prototyping of control software

It is not a plug-and-play consumer application.

---

## Authors

PhD Student, Mustafa Yücel  
MSc, Berkin Binbas  

---

## License

This project is currently unlicensed.
All rights reserved.
