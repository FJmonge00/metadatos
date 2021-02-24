<!-- <img src="./imagenes/MI-LICENCIA88x31.png" style="float: left; margin-right: 10px;" /> -->

# Exiftool

## Instalar Exiftool

```bash
apt-get install libimage-exiftool-perl
```

## Ver Metadatos

```bash
wget https://github.com/FJmonge00/metadatos/blob/master/objetos/Ejemplo1Canarias.jpg
exiftool Ejemplo1Canarias.jpg
```

### Ver Ubicación

```bash
exiftool Ejemplo1Canarias.jpg | grep -i "GPS"
```


## Modificar metadatos (Copyrigh)

```bash
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