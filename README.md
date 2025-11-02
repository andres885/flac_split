[Versión en español](./README.es.md)
# Bash Script to split FLAC files

A Bash script that splits FLAC files into individual tracks using a CUE sheet.

Some CUE sheets may be malformed, causing errors during script execution. These sheets can be easily fixed with a plain text editor. The script displays the entire process on screen, so you’ll know if any file failed.

Install dependencies:
```bash
sudo apt install cuetools shntool flac
```

Download the script:
```bash
wget https://github.com/andres885/flac_split/raw/main/flac_split
chmod +x flac_split
```
Replace the path to your music library in the script:

Change
```MUSIC_LIBRARY="/home/usuario/Música/Metal/$1"```
to
```MUSIC_LIBRARY="/path/to/your/library/$1"```

Move script to a directory in your PATH:
```bash
mv flac_split ~/.local/bin/
```

Run script:
```bash
flac_split <directory>
```
Replace <directory> with a directory from your music library.

![Captura del script](./screenshot.png)

That's all, folks!
