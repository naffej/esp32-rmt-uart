# ESP32 RMT UART

Component for Espressif ESP32 ESP-IDF framework.

This components uses ESP32's RMT peripheral as an UART port. It can send and receive UART frames as well.

## Supported versions of frameworks and devices

| Chip           | Framework          | Versions   |   Number of UART    
|----------------|--------------------|------------|----------
| ESP32-S2 | ESP-IDF            | v4.3 and above  |   2
| ESP32-C3 | ESP-IDF            | v4.3 and above  |   2
| ESP32-S3 | ESP-IDF            | v4.3 and above  |   4

## How to Use
Clone this repository to your project components directory.

## Restrictions
Due to hardware limitations ESP32-S2 can only receive 12 bytes at once. In RX only mode this limit is 24 bytes. Transmit has no restriction.
