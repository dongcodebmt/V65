## CIDOO V65 QMK/VIA
*WIP*

MCU: AT32F415RBT7-7_128K

Space+B or FN+R_SHIFT+R: to enter DFU(Device Firmware Upgrade) mode. Long press "Space" + "B" or FN+R_SHIFT+R and then plug in USB cable ultil FN LED flash to enter DFU mode.

### CLI

```sh
% dfu-util -l
Found DFU: [2e3c:df11] ver=0200, devnum=12, cfg=1, intf=0, path="1-1", alt=1, name="@Option Byte   /0x1FFFF800/02*016 e", serial="AT32"
Found DFU: [2e3c:df11] ver=0200, devnum=12, cfg=1, intf=0, path="1-1", alt=0, name="@Internal Flash  /0x08000000/ 128*1Kg", serial="AT32"

# backup firmware
% dfu-util -a 0 -d 2e3c:df11 -s 0x8000000 -U backup.bin

% fwupdmgr get-devices
To be filled by O.E.M.
│
├─DFU in FS Mode:
│     Device ID:          <REDACTED>
│     Current version:    2.0
│     Vendor:             Artery-Tech (USB:0x2E3C)
│     GUIDs:              <REDACTED>
│                         <REDACTED>
│     Device Flags:       • Updatable
│                         • Is in bootloader mode
│

````

