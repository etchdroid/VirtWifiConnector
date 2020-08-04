# VirtWifiConnector
Simple "as small as possible" app to connect to QEMU's VirtWifi in application tests

The app targets API 16 since the "app was built for a old version dialog" can be easily be dismissed with `input keyboard keyevent KEYCODE_ESCAPE`, while the dynamic permissions dialog requires more interaction.

The app just connects to a `VirtWifi` open network, it's as small as I could get it and it's intended to be shoved over the serial console into an unmodified Android x86 image running on QEMU.

This is required since Android x86 images appear to show emulated ethernet adapters as a `VirtWifi` network, and they won't connect to it automatically (and therefore TCP ADP doesn't work).
