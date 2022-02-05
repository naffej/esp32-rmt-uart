# ESP32 RMT UART

Component for Espressif ESP32 ESP-IDF framework.

This components uses ESP32's RMT peripheral as an UART port. It can send and receive UART frames as well.

## Supported versions of frameworks and devices

| Chip           | Framework          | Versions
|----------------|--------------------|-----------------------
| ESP32-S2 | ESP-IDF            | v4.3 and above
| ESP32-C3 | ESP-IDF            | v4.3 and above
| ESP32-S3 | ESP-IDF            | v4.3 and above

## How to Use
Clone this repository to your project compoments directory.

## Restrictions
In ESP32-S2 this driver can only receive 12 bytes at once. In RX only mode this limit is 24 bytes. Transmit has no restriction.