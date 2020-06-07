# thinkpad-tweaks
Tweaks and fixes for running Linux on specific Thinkpads

### T460s

The trackpoint sensitivity can not only make it too hard to use it with sufficient precision. It can
also interfere with the touchpad as slight movements of the trackpoint (due to vibrations) apparently 
override touchpad input. The `rc.local` file fixes this by adapting the trackpoint sensitivity. The
file must be placed in `/etc/` and given `x` permission.

### E590

TODO
