# Bash Script to split FLAC files

Un script en Bash que divide archivos FLAC en pistas independientes utilizando una hoja CUE.

Algunas hojas pueden estar mal formadas produciendo errores en la ejecución del script. Estas hojas pueden corregirse fácilmente con un editor de texto plano. El script muestra en pantalla todo el proceso, así sabremos si ha fallado algún archivo.

Instalar dependencias
```bash
sudo apt install cuetools shntool flac
```

Clonar repositorio
```bash
git clone https://github.com/andres885/flac_split.git
```

Mover script a un directorio en el PATH
```bash
mv flac-splitter/flac_split ~/.local/bin/
```

Ejecutar script
```bash
flac_split <directorio>
```
