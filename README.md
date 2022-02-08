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

## Configuration

```c
typedef struct {
    int baud_rate;                        /*!< UART baud rate*/
    rmt_uart_mode_t mode;                 /*!< UART mode*/  
    rmt_uart_word_length_t data_bits;     /*!< UART byte size*/
    rmt_uart_parity_t parity;             /*!< UART parity mode*/
    rmt_uart_stop_bits_t stop_bits;       /*!< UART stop bits*/
    gpio_num_t tx_io_num;                 /*!< UART TX GPIO num*/
    gpio_num_t rx_io_num;                 /*!< UART RX GPIO num*/
    size_t buffer_size;                   /*!< UART buffer size/*>
} rmt_uart_config_t;
```

Mode can be TX only, RX only or both TX and RX.  
Buffer size must be 20 times of the length of transmit/receive data.
If you want to send 10 bytes maximum then buffer_size = 200.


## Restrictions
Due to hardware limitations ESP32-S2 can only receive 12 bytes at once. In RX only mode this limit is 24 bytes. Transmit has no restriction.
