# Here (Nightcore) x Arch

Syrex

## Update

`sudo pacman -Syu`

## Error

List of errors resolved

### No Update package

#### ... signature " " is unknown trust

[LINK](https://bbs.archlinux.org/viewtopic.php?id=244976)

```txt
# rm -R /etc/pacman.d/gnupg/
# rm -R /root/.gnupg/ 
# gpg --refresh-keys
# pacman-key --init && pacman-key --populate archlinux
```

`sudo pacman -S archlinux-keyring`
