[ 🇬🇧 English Version ](README.en.md)

# Scripts Bash para Dividir y Etiquetar FLAC

Un conjunto de **scripts en Bash** para dividir archivos **FLAC** en pistas individuales utilizando una hoja **CUE** y, opcionalmente, eliminar los archivos originales una vez que se detectan las pistas divididas.

![Captura del script](./screenshot.png)

---

## 🚀 Características

- **flac_split**: Divide un único archivo FLAC en pistas individuales utilizando su hoja CUE correspondiente.
  - Las hojas CUE mal formadas pueden causar errores, pero son fáciles de corregir con un editor de texto plano.
  - El script muestra todo el proceso en pantalla para que puedas monitorear si algún archivo falla.

- **rmflac**: Comprueba si un directorio contiene pistas ya divididas (basándose en la hoja CUE).
  - Solicita confirmación al usuario para eliminar el archivo FLAC original (el archivo imagen completo) si se encuentran las pistas divididas.

---

## 🧩 Requisitos

- `cuetools`
- `shntool`
- `flac`

Instalación en Debian/Ubuntu:

```bash
sudo apt install cuetools shntool flac
```

---

## 🧰 Instalación y Configuración

### 1. Descargar los scripts

```bash
wget [https://github.com/andres885/flac_split/raw/main/flac_split](https://github.com/andres885/flac_split/raw/main/flac_split)
wget [https://github.com/andres885/flac_split/raw/main/rmflac](https://github.com/andres885/flac_split/raw/main/rmflac)
chmod +x flac_split rmflac
```

### 2. Configurar la ruta de tu biblioteca musical

Edita ambos scripts y reemplaza la ruta hacia tu biblioteca de música:

```bash
# Cambia esto
MUSIC_LIBRARY="/home/usuario/Música/Metal/$1"

# A tu ruta real
MUSIC_LIBRARY="/ruta/a/tu/biblioteca/$1"
```

### 3. Mover los scripts a un directorio en tu PATH

```bash
mv flac_split rmflac ~/.local/bin/
```

---

## 🧰 Uso

- **Dividir FLACs**:

```bash
flac_split <directorio>
```

- **Eliminar archivos originales** (si las pistas ya están divididas):

```bash
rmflac <directorio>
```

Reemplaza `<directorio>` con el nombre del directorio dentro de tu biblioteca musical.

---

## 🧾 Licencia

Este proyecto está licenciado bajo la **Licencia MIT**.
Consulta la licencia completa aquí: [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

---

## 🧑‍💻 Autor

Desarrollado por [**X Software**](https://xsoftware.es)
Desarrollo de software Linux, soluciones web y automatización de sistemas.