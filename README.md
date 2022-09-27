# Curso Supercómputo IA-UNAM 2022

Este repositorio se ha creado para ayudar a los estudiantes del curso de supercómputo de la maestría de astrofísica, curso 2022, a poner a punto el ambiente de Conda que les permitirá aprender a usar la herramienta "yt" para cargar y analizar simulaciones numéricas.

Antes de empezar se asume que el estudiante tiene un ambiente [anaconda3](https://www.anaconda.com/distribution/) funcional en su ordenador. Si no es el caso, sigan la liga e instalen la distribución anaconda 3 en sus ordenadores.
Se asume también que el estudiante tiene instalado en su ordenador el programa "Git".

## Instalación del ambiente "Conda"

Clonen el repositorio:

```console
$ git clone https://github.com/Santiastro1/SC_UNAM_2022.git
```

Cambien al directorio que acaban de crear:

```console
$ cd SC_UNAM_2022
```
Cree el nuevo ambiente de conda:

```console
$ conda env create -f SC_UNAM_2022_env.yml
```
Activen el nuevo ambiente conda:

```console
$ conda activate SC2022
```
Verifiquen que el ambiente está bien instalado:

```console
$ conda env list
```
El nombre del ambiente, ```SC2022```, debería aparecer en la lista. 

## testeando el ambiente de conda

Antes de empezar a usar el ambiente de conda ```SC2022``` recomendamos que lo testeen.
Para hacerlo, intenten abrir el ```jupyter notebook``` en su servidor web.

```console
$ jupyter notebook
```

Ahora, para comprobar que las librerías de python están bien instaladas deberéis descargar algunos nuevos archivos:

### 1- Usado por ```yt```: Archivos de simulaciones N-cuerpos obtenidas usando gran variedad de códigos numéricos: https://yt-project.org/data/.

Para empezar intetaremos leer y visualizar los resultados de simulaciones obtenidas usando ART y RAMSES. Descargaremos pués algunos archivos y los moveremos a nuestra carpeta de trabajo:

http://yt-project.org/data/sizmbhloz-clref04SNth-rs9_a0.9011.tar.gz

```console
$ mv ~/Downloads/sizmbhloz-clref04SNth-rs9_a0.9011.tar.gz ~/SC_UNAM_2022/
```

```console
$ cd ~/SC_UNAM_2022/
```

```console
$ tar -zxvf sizmbhloz-clref04SNth-rs9_a0.9011.tar.gz

```
```console
$ rm sizmbhloz-clref04SNth-rs9_a0.9011.tar.gz
```

http://yt-project.org/data/output_00080.tar.gz

```console
$ mv ~/Downloads/output_00080.tar.gz ~/SC_UNAM_2022/
```

```console
$ cd ~/SC_UNAM_2022/
```

```console
$ tar -zxvf output_00080.tar
```

```console
$ rm output_00080.tar
```

Ahora pueden abrir el script de jupyter ```SC_UNAM_2022_envtest.ipynb``` en su navegador de internet preferido y correr cada una de las celdas para ver que las librerías de yt funcionan, así como el resto de librerías de ``Python3.7```.

Si consiguen que corran todas las celdas del jupyter notebook ya están preparados para empezar a trabajar bajo el ambiente conda que han creado.

En el caso que hayan tenido problemas corriendo alguna de las celdas contacten con sroca(at)astro.unam.mx


## Actualizar la instalación

Probablemente necesitarán actualizar el ambiente conda que han creado y sus librerías```Athens2022```, para hacerlo tienen que:

```console
$ conda env update --name SC2022 -f SC_UNAM_2022_env.yml --prune
```
