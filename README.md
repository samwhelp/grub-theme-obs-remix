

# Home

| Link | GitHub |
| ---- | ------ |
| [grub-theme-obs-remix](https://samwhelp.github.io/grub-theme-obs-remix/) | [GitHub](https://github.com/samwhelp/grub-theme-obs-remix) |
| [grub-theme-remix](https://samwhelp.github.io/grub-theme-remix) | [GitHub](https://github.com/samwhelp/grub-theme-remix) |
| [grub-theme-remix-select](https://samwhelp.github.io/grub-theme-remix-select/) | [GitHub](https://github.com/samwhelp/grub-theme-remix-select) |




## Subject

* [Theme Source](#theme-source)
* [Theme File](#theme-file)
* [Install](#install)
* [Apply](#apply)
* [Docs](#docs)




## Theme Source

| Theme Source |
| ------ |
| [Pling](https://www.pling.com/p/1577873/) |
| [GitHub](https://github.com/sandesh236/obs-grub-theme) |





## Theme File

| Theme File                       |
| -------------------------------- |
| [theme.txt](https://github.com/samwhelp/grub-theme-obs-remix/blob/main/theme.txt)           |
| [background.jpg](https://github.com/samwhelp/grub-theme-obs-remix/blob/main/background.jpg) |




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

| Block          | Block      | Block          |
| ---------------| ---------- | -------------- |
| Northwest (nw) | North (n)  | Northeast (ne) |
| West (w)       | Center (c) | East (e)       |
| Southwest (sw) | South (s)  | Southeast (se) |




## Branch

| Branch |
| --- |
| [main](https://github.com/samwhelp/grub-theme-obs-remix/tree/main) |
| [gh-pages](https://github.com/samwhelp/grub-theme-obs-remix/tree/gh-pages) |
