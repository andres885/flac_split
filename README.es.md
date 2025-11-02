[English version](./README.md)
# Bash Script para dividir archivos FLAC

Un script en Bash que divide archivos FLAC en pistas independientes utilizando una hoja CUE.

Algunas hojas pueden estar mal formadas produciendo errores en la ejecución del script. Estas hojas pueden corregirse fácilmente con un editor de texto plano. El script muestra en pantalla todo el proceso, así sabremos si ha fallado algún archivo.

El script también colocará los nombres apropiados en cada pista además de etiquetarlas correctamente haciedo uso de los datos en la hoja CUE.

Instalar dependencias:
```bash
sudo apt install cuetools shntool flac
```

Clonar repositorio:
```bash
git clone https://github.com/andres885/flac_split.git
```
Sustituir la ruta a tu biblioteca musical en el script:

Cambia ```MUSIC_LIBRARY="/home/usuario/Música/Metal/$1"``` por MUSIC_LIBRARY="/ruta/a/tu/biblioteca/$1"```

Mover script a un directorio en el PATH:
```bash
mv flac_split/flac_split ~/.local/bin/
```

Ejecutar script:
```bash
flac_split <directorio>
```

Reemplaza ```<directorio>``` por un directorio de tu biblioteca musical

Eso es todo amigos!!
