# Metadata

=========== Herramientas relacionadas con metadata ===========
-exiftool
-exiv2
-pdfinfo
-mediainfo
-strings
-file

=========== Antes de inicar ===========
* Todos los archivos a analizar colocarlos en el directorio /data


=========== Crear imagen ===========
Dentro de /metadata
docker build -t metadata .


=========== Inicar contenedor ===========
docker run -it --rm -v "$PWD/data:/data" metadata
