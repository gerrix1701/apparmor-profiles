# apparmor-profiles

Not all Linux distributions which support apparmor come with profiles for Firefox or Thunderbird. I copied the profiles from Ubuntu's packages and modified them slightly to make them work for my environment. You're welcome to make use of them as well.

## Firefox-ESR
The firefox-esr profile is for Debian 10/11. Run `sudo touch /etc/apparmor.d/local/usr.bin.firefox-esr` first, then copy _usr.bin.firefox-esr_ from this repository to `/etc/apparmor.d/` and activate the profile.

## Firefox
The firefox profile was tested with Manjaro Linux. I've added support for KeePassXC plugin, Yubikeys and widevine video plugin.
Copy _firefox_ to `/etc/apparmor.d/abstractions/ubuntu-browsers.d/` and _usr.bin.firefox-esr_ to `/etc/apparmor.d/`. Also run `sudo touch /etc/apparmor.d/local/usr.bin.firefox`, then activate the profile.

## Thunderbird
The thunderbird profile was tested with Manjaro Linux. Run `sudo touch /etc/apparmor.d/local/usr.bin.thunderbird` and copy _usr.bin.thunderbird_ to `/etc/apparmor.d/` before activating the profile.
