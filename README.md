# OnBoard LED component

This repository contains an ESP-IDF component for the OnBoard LED. It runs on
any ESP32 processor and is built using the ESP-IDF build system in version 6.0.

The component is implemented as C++ class `OnBoardLed`.

## Connecting the component

The constructor of class `OnBoardLed` has six parameters:

| Parameter    | Type of Parameter | Usage                                                   |
|:-------------|:------------------|:--------------------------------------------------------|
| tag          | std::string       | the tag to be used in the ESP log                       |
| ledPin       | gpio_num_t        | the gpio number of the onboard LED                      |
| ledType      | std::string       | the LED type: "GPIO" or "LED strip"                     |
| colorOrder   | std::string       | for type "LED strip": the color order: "RGB" or "GRB"   |
| stripBackend | std::string       | for type "LED strip": the strip backend: "RMT" or "SPI" |
| ledModel     | led_model_t       | the LED model type |
| blinkPeriod  | int               | the blink period in ms                  |

The component uses the GPIO pin of the onboard LED of the SoC.

# Usage

## API
The API of the component is located in the include directory ```include/onboard_led.hpp``` and defines the
C++ class ```OnBoardLed```

```C
class OnBoardLed {
public:
	OnBoardLed(std::string tag, gpio_num_t ledPin, std::string ledType, std::string colorOrder, std::string stripBackend, led_model_t ledModel, int blinkPeriod);
	virtual ~OnBoardLed();
    void setLedPixelColor(uint32_t index, uint32_t red, uint32_t green, uint32_t blue);
    void show(void);
    void setLedState(bool state);
    bool getLedState();
    void blink();

private:	
    std::string tag = "OnBoardLed";
    gpio_num_t ledPin; // the pin number for this LED
    std::string ledType; // the LED type {"GPIO"|"LED strip"}
    std::string colorOrder; // the LED color_order {"RGB"|"GRB"}
    std::string stripBackend; // the LED strip backend {"RMT"|"SPI"}
    led_model_t ledModel; the LED model { LED_MODEL_WS2812 | LED_MODEL_SK6812 }
    int blinkPeriod; // blinking period in milliseconds
	
    // LedPixelColor settings
    uint32_t index;
    uint32_t red;
    uint32_t green;
    uint32_t blue;
	
    // Led State {ON|OFF}
    uint8_t state = 0;   
    
    led_strip_handle_t led_strip;
    led_strip_config_t strip_config;
    led_strip_rmt_config_t rmt_config;
    led_strip_spi_config_t spi_config;
};
```

# License

This component is provided under the Apache 2.0 license.
