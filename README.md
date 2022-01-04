# Async_ConfigOnDRD_FS_MQTT_Ptr_Medium
 
 Add this to platformio.ini
 monitor_speed = 115200
lib_deps = 
	khoih-prog/ESPAsync_WiFiManager@^1.10.0
	bblanchon/ArduinoJson@^6.18.5
	adafruit/Adafruit MQTT Library@^2.4.2

OR
Via Platformio library manager add
    ESPAsync_WiFiManager
    ArduinoJson
    Adafruit MQTT

NB!!!!!!!!!!!!!!!!!!
Adafruit MQTT causes problems with duplicate definitions. To get over this:
Check this folder in your project .pio/libdeps/esp32doit-devkit-v1 and delete the folder WiFi101
OR
Add lib_ignore = WiFi101 to platformio.ini

NOTE the credentials are held in NVR and the only way to totally remove them is to manually clear the NVR on the ESP
        i: Start CLI ... To get to CLI in LHS menu select PIO (Ant Icon)
        then in "QUICK ACCESS MENU" select under Miscellaneous PlatformIO Core CLI
        ii: pio run --target erase
        iii: (may take more than one attempt)