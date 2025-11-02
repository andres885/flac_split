# flac-splitter, a Bash Script to split FLAC files

Un script en Bash que divide archivos FLAC en pistas independientes utilizando una hoja CUE.

Algunas hojas pueden estar mal formadas produciendo errores en la ejecución del script. Estas hojas pueden corregirse fácilmente con un editor de texto plano. El script muestra en pantalla todo el proceso, así sabremos si ha fallado algún archivo.

Instalar dependencias
```sudo apt install cuetools shntool flac```

Clonar repositorio
```git clone https://github.com/andres885/flac-splitter.git```

Mover script a un directorio en el PATH
```mv flac-splitter/flac_split.sh ~/.local/bin/```

Ejecutar script
```split_flac.sh <directorio>```
