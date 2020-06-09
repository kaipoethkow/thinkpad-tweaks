# thinkpad-tweaks
Tweaks and fixes for running Linux on specific Thinkpads

### T460s

The trackpoint sensitivity can not only make it too hard to use it with sufficient precision. It can
also interfere with the touchpad as slight movements of the trackpoint (due to vibrations) apparently 
override touchpad input. The `rc.local` file fixes this by adapting the trackpoint sensitivity. The
file must be placed in `/etc/` and given `x` permission.

### E590

The WIFI adapter on the E590 can crash the respective kernel module and disrupt connectivity
repeatedly. The related bug report is

https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1848921

A more stable connection was observed when setting `11n_disable`. Please note that this trades
off stability for lower speed (still acceptable, though). To apply the setting replace
`/etc/modprobe.d/iwlwifi.conf` with `e590/iwlwifi.conf` or modify your version to include the
`option` line.
