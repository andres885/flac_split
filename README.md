[Versión en español](./README.es.md)  
# FLAC splitter and tagger Bash scripts

A set of Bash scripts to split FLAC files into individual tracks using a CUE sheet and optionally remove the original files once the split tracks are detected.

## Scripts included

### **flac_split**
Splits a single FLAC file into individual tracks using a CUE sheet.

Some CUE sheets may be malformed, causing errors during script execution. These sheets can be easily fixed with a plain text editor. The script displays the entire process on screen, so you’ll know if any file failed.

### **rmflac**
Checks if a directory contains already-split tracks (based on the CUE sheet).  
If split tracks are found, it prompts the user to confirm whether to delete the original FLAC file.

---

## Install dependencies
```bash
sudo apt install cuetools shntool flac
```

## Download the scripts
```bash
wget https://github.com/andres885/flac_split/raw/main/flac_split
wget https://github.com/andres885/flac_split/raw/main/rmflac
chmod +x flac_split rmflac
```

## Configure your music library path
Edit both scripts and replace the path to your music library:

Change
```bash
MUSIC_LIBRARY="/home/usuario/Música/Metal/$1"
```
to
```bash
MUSIC_LIBRARY="/path/to/your/library/$1"
```

## Move scripts to a directory in your PATH
```bash
mv flac_split rmflac ~/.local/bin/
```

## Run the scripts
Split FLACs:
```bash
flac_split <directory>
```

Remove originals (if tracks are already split):
```bash
rmflac <directory>
```

Replace `<directory>` with a directory from your music library.

![Script screenshot](./screenshot.png)

---

## License
MIT License – see the full license here:  
https://opensource.org/licenses/MIT


