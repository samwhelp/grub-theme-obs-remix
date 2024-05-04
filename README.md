

# grub-theme-obs-remix

| Link | GitHub |
| ---- | ------ |
| [grub-theme-obs-remix](https://samwhelp.github.io/grub-theme-obs-remix/) | [GitHub](https://github.com/samwhelp/grub-theme-obs-remix) |
| [grub-theme-remix](https://samwhelp.github.io/grub-theme-remix) | [GitHub](https://github.com/samwhelp/grub-theme-remix) |
| [grub-theme-remix-select](https://samwhelp.github.io/grub-theme-remix-select/) | [GitHub](https://github.com/samwhelp/grub-theme-remix-select) |




## Subject

* [Theme Source](#theme-source)
* [Background Source](#background-source)
* [Theme File](#theme-file)
* [Install](#install)
* [Apply](#apply)
* [Docs](#docs)




## Theme Source

| Theme Source |
| ------------ |
| GitHub / obster-y / [grub-theme-obs](https://github.com/obster-y/grub-theme-obs) |
| [grub-theme-obs-refactoring](https://github.com/samwhelp/grub-theme-obs-refactoring) |




## Background Source

* [iron man](https://www.reddit.com/r/wallpaper/comments/olengo/3840x2160_iron_man/)
* [https://i.redd.it/1ai3l6g54kb71.jpg](https://i.redd.it/1ai3l6g54kb71.jpg)




## Theme File

| Theme File                       |
| -------------------------------- |
| [theme.txt](theme.txt)           |
| [background.jpg](background.jpg) |




## Install

run

``` sh

mkdir -p "./tmp"

wget -c "https://github.com/samwhelp/grub-theme-obs-remix/archive/refs/heads/main.tar.gz" -O "./tmp/grub-theme-obs-remix-main.tar.gz"


tar xf "./tmp/grub-theme-obs-remix-main.tar.gz" -C "./tmp"


sudo mkdir -p "/boot/grub/themes"

sudo cp -rf "./tmp/grub-theme-obs-remix-main/." "/boot/grub/themes/grub-theme-obs-remix"

```

or run remote script [fetch.sh](https://github.com/samwhelp/grub-theme-obs-remix/blob/main/helper/theme-installer/fetch.sh)

``` sh
bash <(curl -L 'https://raw.githubusercontent.com/samwhelp/grub-theme-obs-remix/main/helper/theme-installer/fetch.sh')
```




## Apply

edit `/etc/default/grub`

```
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-obs-remix/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-obs-remix/theme.txt"
```

or create file `/etc/default/grub.d/theme.cfg`, run

``` sh
cat << EOF | sudo tee /etc/default/grub.d/theme.cfg
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-obs-remix/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-obs-remix/theme.txt"

EOF
```


then run

``` sh
sudo update-grub
```

or run

``` sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```




## Docs

| Grub Docs |
| ---- |
| [Theme file format](https://www.gnu.org/software/grub/manual/grub/html_node/Theme-file-format.html) |




## Styled Boxes

| Region              | Region          | Region              |
| ------------------- | --------------- | ------------------- |
| 1. Northwest (`nw`) | 2. North (`n`)  | 3. Northeast (`ne`) |
| 4. West (`w`)       | 5. Center (`c`) | 6. East (`e`)       |
| 7. Southwest (`sw`) | 8. South (`s`)  | 9. Southeast (`se`) |

> menu-box file name

| Region               | Region              | Region               |
| -------------------- | ------------------- | -------------------- |
| 1. `menu-box-nw.png` | 2. `menu-box-n.png` | 3. `menu-box-ne.png` |
| 4. `menu-box-w.png`  | 5. `menu-box-c.png` | 6. `menu-box-e.png`  |
| 7. `menu-box-sw.png` | 8. `menu-box-s.png` | 9. `menu-box-se.png` |
