## Onboard LED Example

This example demonstrates how to utilize the `onboard_led` component to use the onboard led.

## Hardware

* The GPIO of the Onboard LED on any development board can be used in this example.

## Build and Flash

Build the project and flash it to the board, then run the monitor tool to view the serial output:

* Run `. <directory with ESP-IDF version>/export.sh` to set IDF environment
* Run `idf.py set-target esp32xx` to set target chip
* Run `idf.py -p PORT flash monitor` to build, flash and monitor the project

(To exit the serial monitor, type `Ctrl-]` (or on a Mac `Ctrl-Option-6`).

See the Getting Started Guide for all the steps to configure and use the ESP-IDF to build projects.

## Example Output

```
I (271) main_task: Calling app_main()
I (271) ESP32-C6-DevKitM-1 V1.0 onBoardLed: configured to use addressable LED strip!
I (271) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (1281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (1781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (2281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (2781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (3281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (3781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (4281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (4781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (5281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (5781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (6281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (6781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (7281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (7781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (8281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (8781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (9281) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED ON!
I (9781) ESP32-C6-DevKitM-1 V1.0 onBoardLed: Turning the LED OFF!
I (10281) main_task: Returned from app_main()
```