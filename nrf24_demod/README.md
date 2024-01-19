Clone and make the NRF24-BTLE-Decoder program from [Github](https://github.com/omriiluz/NRF24-BTLE-Decoder)
```bash
git clone https://github.com/omriiluz/NRF24-BTLE-Decoder
cd NRF24-BTLE-Decoder
make
cd bin
```

The nrf24-btle-decoder software is designed to get sample at 2Msps via the standard input. To get data from gnuradio instead we create a fifo and cat this fifo in nrf24-btle-decoder:

```bash
mkfifo /tmp/fifo
cat /tmp/fifo | ./nrf24-btle-decoder -d 1
```
