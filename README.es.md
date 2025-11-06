[English version](./README.md)  
# Scripts Bash para dividir y etiquetar archivos FLAC

Un conjunto de scripts Bash para dividir archivos FLAC en pistas individuales usando una hoja CUE y, opcionalmente, eliminar los archivos originales una vez detectadas las pistas divididas.

## Scripts incluidos

### **flac_split**
Divide un archivo FLAC único en pistas individuales utilizando una hoja CUE.

Algunas hojas CUE pueden estar mal formadas, lo que puede causar errores durante la ejecución del script. Estas hojas pueden corregirse fácilmente con un editor de texto plano.  
El script muestra todo el proceso en pantalla, por lo que sabrás si algún archivo ha fallado.

### **rmflac**
Comprueba si un directorio contiene pistas ya divididas (según la hoja CUE).  
Si encuentra las pistas, pregunta al usuario si desea eliminar el archivo FLAC original.

---

## Instalar dependencias
```bash
sudo apt install cuetools shntool flac
```

## Descargar los scripts
```bash
wget https://github.com/andres885/flac_split/raw/main/flac_split
wget https://github.com/andres885/flac_split/raw/main/rmflac
chmod +x flac_split rmflac
```

## Configurar la ruta de tu biblioteca musical
Edita ambos scripts y reemplaza la ruta de tu biblioteca musical:

Cambia
```bash
MUSIC_LIBRARY="/home/usuario/Música/Metal/$1"
```
por
```bash
MUSIC_LIBRARY="/ruta/a/tu/biblioteca/$1"
```

## Mover los scripts a un directorio en tu PATH
```bash
mv flac_split rmflac ~/.local/bin/
```

## Ejecutar los scripts
Dividir archivos FLAC:
```bash
flac_split <directorio>
```

Eliminar los originales (si las pistas ya están divididas):
```bash
rmflac <directorio>
```

Sustituye `<directorio>` por un directorio de tu biblioteca musical.

![Captura del script](./screenshot.png)

¡Eso es todo, amigos!
