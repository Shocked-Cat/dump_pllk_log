# dump_pllk

Dumps pre-loader and LK UART logs from MediaTek devices via fastboot.

Works by sending `oem dump_pllk_log` over raw USB and reassembling the
chunked responses into a single log file.

## Setup
```
pip install -r requirements.txt
```

On Linux you may need a udev rule or to run as root.

On Windows you need a libusb-compatible driver bound to the fastboot
interface (e.g. via Zadig), or the `libusb-package` pip package which
is already included in the requirements.

## Usage
```
python dump_pllk.py                     # saves to log.txt, prints to screen
python dump_pllk.py -o boot_log.txt     # custom output file
python dump_pllk.py -s                  # silent, no log output to screen
```
