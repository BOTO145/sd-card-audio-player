```markdown
# sd-card-audio-player

A simple ESP32-based audio player that plays WAV files from an SD card.

## Short Description

This project demonstrates a basic audio player application on an ESP32 microcontroller. It utilizes the SD card library and the TMRpcm library to play WAV files stored on an SD card connected to the ESP32.

## Setup Instructions

**Components:**

* ESP32 Development Board
* SD Card (at least 4GB)
* SD Card adapter for ESP32
* Jumper wires

**Libraries:**

* **SD.h:**  For SD card interaction.  Download from the Arduino Library Manager.
* **TMRpcm.h:** For playing audio. Download from the Arduino Library Manager.
* **SPI.h:** Needed by TMRpcm.  (Usually included automatically.)

**Wiring:**

1. Connect the SD card to the ESP32 using the SD card adapter.
2.  Connect the SD card's chip select pin to digital pin 10 of the ESP32.  (This is important and defaults to pin 10.)
3. Connect the speaker to digital pin 9 of the ESP32.

**Important Notes:**

* Ensure your SD card is properly formatted.
* Place a `music.wav` file on the root directory of the SD card.


## Uploading and Running Instructions

1. **Install Libraries:**
   Open the Arduino IDE, navigate to `Sketch > Include Library > Manage Libraries`. Search for "SD" and "TMRpcm" and install them.  You will typically see those installed already in ESP32-specific Arduino environments.
2. **Upload the Code:**
   Copy the provided Arduino code into a new sketch in the Arduino IDE.
3. **Connect to ESP32:** Ensure your ESP32 board is connected to your computer via USB.
4. **Verify and Upload:**  Verify your code to catch any potential errors before uploading.  Click the Upload button in the Arduino IDE to upload the code to your ESP32.
5. **File Placement:**  Make sure you have a `music.wav` file on the root directory of your SD card.

## Expected Output

Upon successful upload and execution, the ESP32 should play the audio file `music.wav` from the SD card.


## Troubleshooting Tips

* **SD Card Not Recognized:**
    * **Verify Wiring:** Double-check the SD card adapter and wiring to digital pin 10.
    * **SD Card Format:** Ensure the SD card is properly formatted and not corrupted. Try a different SD card.
    * **SD Library Compatibility:** Check for compatibility issues between your SD card and the installed SD library.
* **No Sound:**
    * **Speaker Connection:** Ensure the speaker is correctly connected to digital pin 9.
    * **`music.wav` File:** Verify that the `music.wav` file exists on the SD card.
    * **Volume Settings:** Verify that the volume setting in the code is correct (tmrpcm.setVolume(6)).
* **Error Messages:**
    * Carefully review any error messages in the Serial Monitor.  Common errors include issues mounting or reading the SD card.

## Additional Considerations


* **Error Handling:** The provided code has basic error handling for the SD card.  Consider adding more robust error handling to catch specific issues (e.g., file not found).  This will help with more stable operation.

* **File Management:** If you want to play multiple files, you'll need more sophisticated code for file selection, playlist management, and potentially file browsing.

* **Memory Management:** For larger projects, pay attention to memory usage to avoid potential issues.

* **Robustness:** For real-world use cases, consider error-checking (e.g., ensure the SD card is present), input validation, and other aspects of robust software development.

## Contributing

Feel free to contribute to this project by adding new features or improving the existing code.


```