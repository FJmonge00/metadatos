<!-- <img src="./imagenes/MI-LICENCIA88x31.png" style="float: left; margin-right: 10px;" /> -->

# Exiftool

## Instalar Exiftool

```bash
apt-get install libimage-exiftool-perl
```

## Ver Metadatos

```bash
wget https://netting.files.wordpress.com/2013/09/example.jpg
exiftool example.jpg
```

### Ver Ubicación

```bash
exiftool example.jpg | grep -i "GPS"
```


## Modificar metadatos (Copyrigh)

```bash
wget https://i.blogs.es/5efe2c/cap_001/450_1000.jpg
exiftool -exif:Copyright="www.vozidea.com" Ejemplo2.jpg
exiftool example.jpg | grep -i Copyright
```

## Modificar fecha (Restar 1 hora)

```bash
exiftool -alldates-=1 -if '$CreateDate ge "2012-:12:13"' Ejemplo2.jpg
```

## Limpiar Metadatos

```bash
exiftool -alldates-=1 -if '$CreateDate ge "2012-:12:13"' Ejemplo2.jpg
```