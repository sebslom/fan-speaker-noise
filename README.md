# Speaker Blower / Fan Simulator 🌬️🔊

A simple, browser-based web application that simulates the sound and physical effect of a fan using your device's speakers. It uses the Web Audio API to generate synthetic noise and sub-bass frequencies right in your browser—no downloads or installations required.

## Features

This app features two distinct modes separated by tabs:

### 1. Classic Noise Mode 💤
Generates a soothing, synthesized fan noise perfect for sleeping, studying, or drowning out background noise.
* **Power (Volume):** Adjusts the overall loudness.
* **Fan Speed (Tone):** Adjusts the frequency filter to make the "fan" sound like it's spinning faster (higher pitch) or slower (deeper rumble).

### 2. Physical Blower Mode 💨
Uses extremely low-frequency square waves (sub-bass) to physically force your speaker cones to their maximum excursion, actually pushing air out of your speakers. It mixes this with the fan noise for the ultimate simulator.
* **Master Power:** Controls the total volume of the output.
* **Air Push Power:** Controls the intensity of the physical speaker vibration.
* **Push Frequency (Hz):** Adjusts the pulse rate of the vibration (typically 10-40Hz works best for moving air).
* **Fan Sound Level:** Controls the volume of the synthetic fan noise mixed over the vibration.

## How to Use
1. Clone or download this repository.
2. Open `index.html` in any modern web browser (Chrome, Firefox, Safari, Edge).
3. Select your desired tab.
4. Click **"Turn On"**.
5. Adjust the sliders to your liking!

*Note: For the physical blowing effect to work, you may need to turn your device's system volume up high.*

## How it Works
The application relies entirely on JavaScript and the native **Web Audio API**.
* **White Noise:** Generated mathematically by filling an audio buffer with random values.
* **Filtering:** A `BiquadFilterNode` (Lowpass) shapes the harsh white noise into a smooth rushing sound that mimics wind or a fan.
* **Air Pushing:** An `OscillatorNode` playing a low-frequency square wave causes the speaker driver to pull all the way back and push all the way forward rapidly, displacing physical air just like water-eject apps on modern smartphones.

## ⚠️ Disclaimer
**Use at your own risk.** The "Physical Blower" mode generates extremely low frequencies at maximum amplitude to maximize physical speaker excursion. Playing this at maximum volume for extended periods of time on sensitive or small speakers could potentially cause hardware damage or reduce the lifespan of your audio equipment. 
