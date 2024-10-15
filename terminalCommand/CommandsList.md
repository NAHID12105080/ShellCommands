# Change File Extensions from .nix to .mp4 in Ubuntu Terminal

To rename multiple files with a `.nix` extension to a `.mp4` extension in the terminal on Ubuntu, you can use the following command:

```bash
for file in *.nix; do mv -- "$file" "${file%.nix}.mp4"; done
```
## Unzip and Remove Files

### Option 1: Unzip all .zip files in the current directory

```bash
for file in *.zip; do
    unzip -o "$file"
done
```
## Option 2: Unzip each .zip file into its own directory and remove the .zip files
```fish
for file in *.zip; do
    dir="${file%.*}"
    mkdir -p "$dir"
    unzip "$file" -d "$dir"
done
```
## Remove all .zip files permanently
```fish
rm *.zip
```
## Remove all .zip files interactively(will ask for confirmation before deletion each time)
```bash
rm -i *.zip
```
## How to flash usb drive:
### locate the usb drive name 
```fish
df -h
```
### then, unmount 
```fish
sudo unmount /dev/sdc1(drive name)
```
### to format,
```fish
sudo mkfs.vfat /dev/sdc1
```
## Increase sound:
```bash
pactl set-sink-volume @DEFAULT_SINK@ +10%

```
## to enable wifi-hotspot
```bash
    sudo ufw disable
```
