# ESP32 HID Keyboard

Bluetooth Low Energy (BLE) Keyboard library for ESP32 boards.

This library allows an ESP32 to emulate a Bluetooth HID Keyboard. Once paired with a computer, smartphone, or tablet, the ESP32 can send keyboard input, text strings, special keys, and multimedia keys.

---

## Features

- Bluetooth HID Keyboard
- Send text
- Send individual key presses
- Modifier keys (CTRL, ALT, SHIFT)
- Multimedia keys
- Simple API
- Compatible with Arduino IDE
- Compatible with ESP32 Arduino Core

---

## Supported Boards

- ESP32
- ESP32-S2
- ESP32-S3
- ESP32-C3
- ESP32-C6

---

## Installation

### Arduino Library Manager

Search

ESP32 BLE Keyboard

and click Install.

or

### ZIP Installation

Sketch → Include Library → Add ZIP Library

---

## Example

```cpp
#include <BleKeyboard.h>

BleKeyboard bleKeyboard;

void setup() {
  bleKeyboard.begin();
}

void loop() {
  if (bleKeyboard.isConnected()) {
    bleKeyboard.print("Hello World!");
    delay(5000);
  }
}
```

---

## API

### begin()

Starts BLE keyboard service.

```cpp
bleKeyboard.begin();
```

---

### isConnected()

Returns true if a device is connected.

```cpp
bleKeyboard.isConnected();
```

---

### print()

Sends text.

```cpp
bleKeyboard.print("Hello");
```

---

### write()

Sends a key.

```cpp
bleKeyboard.write(KEY_RETURN);
```

---

### press()

Press a key.

```cpp
bleKeyboard.press(KEY_LEFT_CTRL);
```

---

### release()

Release a key.

```cpp
bleKeyboard.release(KEY_LEFT_CTRL);
```

---

### releaseAll()

Release every pressed key.

```cpp
bleKeyboard.releaseAll();
```

---

## License

MIT License

---

## Author

Gaurav Sharma

GitHub

https://github.com/gsgaurav0