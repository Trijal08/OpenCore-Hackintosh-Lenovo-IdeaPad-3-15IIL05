# OpenCore Hackintosh EFI for Lenovo IdeaPad 3 15IIL05
*Based on the OpenCore bootloader; off of the [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg) made by [acidanthera](https://github.com/acidanthera) hosted on GitHub. Followed the [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/) to get everything working from scratch for the best stability and compatibility!*

**WARNING/DISCLAIMER (VERY IMPORTANT)**: This EFI only supports running macOS Big Sur (11) to macOS Sequoia (15)! 	~~**IT CURRENTLY DOES NOT SUPPORT TOUCHPAD IN MACOS SEQUOIA (15); BUT I WILL FIND A FIX SHORTLY!**~~ Fix has been found! I found the fix thanks to this [issue](https://github.com/VoodooI2C/VoodooI2C/issues/552) in the official VoodooI2C GitHub made by [dreamwhite](https://github.com/dreamwhite); he explains that using a [specific artifact/release](https://github.com/1Revenger1/VoodooInput/actions/runs/9475484687) of VoodooInput.kext solves the problem :)! The fixed version of this EFI will be in the latest release ([v1.0.1_r4](https://github.com/Trijal08/OpenCore-Hackintosh-Lenovo-IdeaPad-3-15IIL05/releases/tag/v1.0.1_r4))!


# Prequisites
In order for Wi-Fi to work on macOS Sequoia (15), you MUST download & install an application named HeliPort.dmg from the [HeliPort](https://github.com/OpenIntelWireless/HeliPort/releases/latest) GitHub repository. It is also recommended that you install the latest release version of an app named YogaSMC from the [YogaSMC](https://github.com/zhen-zen/YogaSMC/releases/latest) GitHub repository. Double click the "YogaSMCPane.prefPane" file in the "YogaSMC-App-Release.dmg" file and drag the "YogaSMCNC.app" file to "Applications" folder.

## Specifications/Specs

![About my Mac](images/system-inf.png)


| | |
|-|-|
|**CPU**|Intel® Core™ i3-1005G1 Processor @ 1.2GHz (Ice Lake)|
|**RAM**|8GB DDR4 2667MHz|
|**iGPU**|Intel® UHD Graphics G1|
|**SSD**|NVMe M.2 SKHynix-HFM512GDHTNI-87A0B 512GB SSD|
|**WLAN+BT**|Intel® Wireless-AC 9560 (A BCM card natively supported by macs will work more stable)|
|**Audio**|Realtek ALC230|
|**Ports**|2xUSB3.0, 1xUSB2.0, HDMI (does not work at all on Ice Lake devices), SD card reader, Headphone Jack, and DC charging port|
|**OpenCore Bootloader**|V1.0.1 MOD (Will constantly be updated, including the kexts/drivers, so all you have to do is come back after a month or so and look for a commit along the lines of "Updated OpenCore to X.X.X MOD!" or check the latest release for something like that!)

## Not Working

- HDMI (which will probably never be fixed. BTW, this issue is exclusive to only Ice Lake.)
- Hibernation (won't cause a problem though, as I disabled it in OpenCore)
- You tell me?!

## Working

- **Everything else that is not in the Not Working section :D**
- Bluetooth (works natively on all macOS)
- WLAN (works natively on all macOS except Sequoia; read [this section](#prequisites) for easy instructions on how to fix for macOS Sequoia (15).
- USB ports mapped precisely (working after sleep)
- ELAN Precision HID Touchpad with fully working gestures
- Audio (and the keys for it), with speaker, microphone, and headphone jack support
- Graphics Acceleration (QI/CI)
- Sleep
- SDHC/SDXC card reader
- Brightness (and the keys for it)

## Conclusion

In conclusion, I hope there are no issues to your very own hackintosh quest. If there are issues; pull requests or suggestions are welcome! :). Here is the [official forum](https://www.olarila.com/topic/37423-perfect-vanilla-efi-for-lenovo-ideapad-3-15iil05-only-for-macos-big-sur-to-sonoma-trijintosh/) where my EFI was always hosted for another contact source!
