# Interfacing-an-Oscilloscope-Using-Python

This project creates a GUI for interfacing with an oscilloscope using PyQt5, PyVISA, and Matplotlib. The Oscilloscope class manages communication with the device, handling connections, settings, and data retrieval. MplCanvas provides a custom Matplotlib canvas for waveform display. The MainWindow class builds the main application window, including UI elements and interaction logic. Key features include dynamic UI updates, real-time waveform display, and customizable settings (channel, timebase, voltage scale, trigger). The application allows users to connect to an oscilloscope, adjust settings, retrieve waveform data, and visualize it in real time. Error handling is implemented throughout to manage potential issues. The code is structured for extensibility, allowing for future additions like multi-channel support or advanced oscilloscope features. Overall, it provides a user-friendly interface for oscilloscope control and data visualization.

The oscilloscope used in this project is the RIGOL Model DS1202.

![image](https://github.com/user-attachments/assets/1d24674a-4955-46fa-abea-284619cb2ec7)

![image](https://github.com/user-attachments/assets/87220f73-7532-4243-b44b-71cc1cc6f070)

## Features

- Connect to and disconnect from an oscilloscope using VISA resource names
- Set oscilloscope parameters such as channel, timebase, voltage scale, and trigger settings
- Retrieve waveform data from the oscilloscope
- Display waveform data in real-time using Matplotlib
- Customizable waveform color

## Requirements

- Python 3.6+
- PyQt5
- PyVISA
- NumPy
- Matplotlib

> **No oscilloscope?** Enable **Simulation Mode (no hardware)** in the GUI to run the app and plot waveforms without any physical device.

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/oscilloscope-interface.git
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

## Run Locally (Windows)

```powershell
# 1. Install dependencies
pip install -r requirements.txt

# 2. Launch the GUI
python oscilloscope-interface.py
```

### Without a physical oscilloscope

1. Launch the app with the command above.
2. Check **"Simulation Mode (no hardware)"** at the top of the window.
3. Click **Connect** — the app connects to a built-in simulator (`SIM::RIGOL_DS1202`).
4. Click **Get Waveform** to plot a simulated 1 kHz sine wave with noise.
5. Adjust **Voltage Scale (V/div)** and click **Get Waveform** again to see the amplitude change.

## Usage

1. Run the script:
   ```
   python oscilloscope-interface.py
   ```

2. Enter the VISA resource name for your oscilloscope (e.g., "USB0::0x1AB1::0x0517::DS1ZE242906834::INSTR").

3. Click "Connect" to establish a connection with the oscilloscope.

4. Use the GUI controls to set the desired channel, timebase, voltage scale, and trigger settings.

5. Click "Get Waveform" to retrieve and display the current waveform data.

6. Use the "Select Color" button to customize the waveform color.

## Class Overview

- `Oscilloscope`: Handles communication with the oscilloscope using PyVISA.
- `MplCanvas`: A custom Matplotlib canvas for displaying waveforms.
- `MainWindow`: The main application window, containing all UI elements and logic.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
