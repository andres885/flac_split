# FLAC Splitter and Tagger Bash Scripts

A set of **Bash scripts** to split **FLAC files** into individual tracks using a **CUE sheet** and optionally remove the original files once the split tracks are detected.

![Script screenshot](./screenshot.png)

---

## 🚀 Features

- **flac_split**: Splits a single FLAC file into individual tracks using a CUE sheet.  
  - Malformed CUE sheets can cause errors, but they can be easily fixed with a plain text editor.  
  - The script displays the entire process on screen so you can monitor if any file failed.  

- **rmflac**: Checks if a directory contains already-split tracks (based on the CUE sheet).  
  - Prompts the user to confirm whether to delete the original FLAC file if split tracks are found.  

---

## 🧩 Requirements

- `cuetools`  
- `shntool`  
- `flac`  

Install with:

```bash
sudo apt install cuetools shntool flac
```

---

## 🧰 Setup

### 1. Download the scripts

```bash
wget https://github.com/andres885/flac_split/raw/main/flac_split
wget https://github.com/andres885/flac_split/raw/main/rmflac
chmod +x flac_split rmflac
```

### 2. Configure your music library path

Edit both scripts and replace the path to your music library:

```bash
# Change this
MUSIC_LIBRARY="/home/usuario/Música/Metal/$1"

# To your path
MUSIC_LIBRARY="/path/to/your/library/$1"
```

### 3. Move scripts to a directory in your PATH

```bash
mv flac_split rmflac ~/.local/bin/
```

---

## 🧰 Usage

- **Split FLACs**:

```bash
flac_split <directory>
```

- **Remove original files** (if tracks are already split):

```bash
rmflac <directory>
```

Replace `<directory>` with a directory from your music library.

---

## 🧾 License

This project is licensed under the **MIT License**.  
See the full license here: [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

---

## 🧑‍💻 Author

Developed by [**X Software**](https://xsoftware.es)  
Linux software development, web solutions, and system automation.
