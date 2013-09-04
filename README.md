Modification of the teensy code so it can send any of the keycodes from the consumer page to an Android device.

Original source for Teensyduino 1.17 downloaded here: http://www.pjrc.com/teensy/teensyduino.html
After installation of Teensyduino, source is located here (on OS X):
/Applications/Arduino.app/Contents/Resources/Java/hardware/teensy

Replace that folder with a symlink to this project.

## Example

    uint16_t KEY_AC_HOME = 0x223; // Home button
    uint16_t KEY_AC_BACK = 0x224; // Back button
    uint8_t KEY_POWER = 0x30;     // Lock/power button

    // Press Home button
    Keyboard.set_consumer(KEY_AC_HOME);
    // Send keyboard data now
    Keyboard.send_now();

    // Release Home button
    Keyboard.set_consumer(0);
    // Send keyboard data now
    Keyboard.send_now();