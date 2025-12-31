# Medved's ESP32 Rainmaker 

I created this repo to experiment with the ESP32 framework because I haven't had expsoure to it in my professional environments, but there are a lot of articles/posts about the platform.

Goals
- [x] Create a basic ESP32 demo with Rainmaker
- [x] Utilize some GH features I've not used like projects
- [ ] Build a simple, but reasonable release workflow in GH and Rainmaker.
- [ ] Enhance basic example to perform garage door management (requirements coming soon)

> [!NOTE]
> I used the rainmaker switch example as a good starter project.  I've left the below text from this example.

# Switch Example

## Build and Flash firmware

Follow the ESP RainMaker Documentation [Get Started](https://rainmaker.espressif.com/docs/get-started.html) section to build and flash this firmware. Just note the path of this example.

## What to expect in this example?

- This example uses the BOOT button and RGB LED on the ESP32-S2-Saola-1/ESP32-C3-DevKitC board to demonstrate a switch.
- The LED state (green color) indicates the state of the switch.
- Pressing the BOOT button will toggle the state of the switch and hence the LED. This will also reflect on the phone app.
- Toggling the button on the phone app should toggle the LED on your board, and also print messages like these on the ESP32-S2 monitor:

```
I (16073) app_main: Received value = true for Switch - power
```

### LED not working?

The ESP32-S2-Saola-1 board has the RGB LED connected to GPIO 18. However, a few earlier boards may have it on GPIO 17. Please use `CONFIG_WS2812_LED_GPIO` to set the appropriate value.

### Reset to Factory

Press and hold the BOOT button for more than 3 seconds to reset the board to factory defaults. You will have to provision the board again to use it.
