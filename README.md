# Gifole Job

<!-- Etiquetas Cabecera -->

![Contributors][contributors-shield]
![Version][version-shield]
[![Download][download-shield]][download-url]

<!-- Cuerpo de Readme -->

## Comenzando 🚀

_Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas._

### Pre-requisitos 📋

_A continuación se detallan las herramientas que son necesarias._

💻 [OpenJDK 11.0.2]
```
📢 Acceder a la página de descarga
    🚨 https://jdk.java.net/archive/
    🚨 Ir a la sección 11.0.2 (build 11.0.2+9)
```
💻 [Eclipse IDE]
```
📢 Acceder a la página de descarga
    🚨 https://www.eclipse.org/downloads/
📢 Versión usada con este material
    🚨 Eclipse IDE Foundation 2019-12 R
    🚨 https://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/2019-12/R/eclipse-jee-2019-12-R-win32-x86_64.zip&mirror_id=576
```
💻 [JBoss EAP 7.2.0]
```
📢 Acceder a la página de descarga
    🚨 https://developers.redhat.com/products/eap/download
📢 Seleccionar la versión "Versión 7.2" y descargar
📢 Link directo de descarga
    🚨 https://developers.redhat.com/download-manager/file/jboss-eap-7.2.0.zip
```
💻 [Apache Maven 3.6.2]
```
📢 Acceder a la página de descarga
    🚨 https://maven.apache.org/download.cgi
📢 Versión usada con este material
    🚨 Maven 3.6.2
    🚨 http://apache.dattatec.com/maven/maven-3/3.6.2/binaries/apache-maven-3.6.2-bin.zip
```
💻 [Oracle Database Express Edition (XE)]
```
📢 Acceder a la página de descarga
    🚨 https://www.oracle.com/database/technologies/xe-downloads.html
📢 Versión usada con este material
    🚨 Release 18.4.0.0.0 (18c)
```
💻 [DBeaver]
```
📢 Acceder a la página de descarga
    🚨 https://dbeaver.com/download/
📢 Versión usada con este material
    🚨 DBeaver Enterprise Edition 7.0
    🚨 https://dbeaver.com/files/dbeaver-ee-latest-x86_64-setup.exe
```

### Configurando Ambiente 🔧

_Una serie de ejemplos paso a paso que te dice lo que debes ejecutar para tener un entorno de desarrollo ejecutandose_

🔨 [Importar la Base de Datos]

```
📢 Ejecutar los script en el siguiente orden
```
_💿📀 Creación de tablespaces - [script][script1]._

_💿📀 Creación de directorios - [script][script2]._

_💿📀 Creación de usuarios - [script][script3]._

_💿📀 Creación de secuencias - [script][script4]._

_💿📀 Creación de tablas de Gifole - [script][script5]._

_💿📀 Creación de data para tablas de Gifole - [script][script6]._

_💿📀 Creación de índices para Gifole - [script][script7]._

_💿📀 Creación de tablas de Gifpri - [script][script8]._

_💿📀 Creación de data para tablas Gifpri - [script][script9]._

_💿📀 Creación de índices para Gifpri - [script][script10]._

_💿📀 Creación de tablas de Gifole(Job) - [script][script11]._

_💿📀 Creación de data para tablas de Gifole(Job) - [script][script12]._

_💿📀 Creación de tablas de Gifole(Quartz) - [script][script13]._

🔨 [Descargar fuentes]

```
📢 GifoleWeb
```

_📡📡 Clonar las fuentes y configurarlo de acuerdo a las instrucciones del [repositorioscript][repositorio-gifoleweb]._

```
📢 GifoleJob
```

_📡📡 Clonar las fuentes del [repositorioscript][repositorio-gifolejob]._


🔨 [Importar Proyecto con Eclipse]

```
📢 Verificar que la versión sea JDK11 antes de iniciar el IDE.
📢 Importar como proyecto Maven.
📢 Verificar que exista el artefacto de GifoleWeb creado ([Ver Instrucciones de GifoleWeb][repositorio-gifoleweb]).
    Nombre: gifole-web-0.8.1-classes.jar
    Ruta: C:\Users\TU-USUARIO\.m2\repository\pe\com\bbva\gifole-web\0.8.1
📢 Cambiar de nombre al artefacto cada vez que GifoleWeb genere uno nuevo.
    Original: gifole-web-0.8.1-classes.jar
    Nuevo: gifole-web-0.8.1.jar
📢 Generar el artefacto de GifoleJob (mvn clean install).
📢 Actualizar el proyecto Maven en el IDE (Alt+F5).
```

🔨 [Configurar Jboss]

## Ejecutando las pruebas ⚙️

_Explica como ejecutar las pruebas automatizadas para este sistema_

### Analice las pruebas end-to-end 🔩

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

### Y las pruebas de estilo de codificación ⌨️

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

## Despliegue 📦

_Agrega notas adicionales sobre como hacer deploy_

## Construido con 🛠️

_Menciona las herramientas que utilizaste para crear tu proyecto_

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - El framework web usado
* [Maven](https://maven.apache.org/) - Manejador de dependencias
* [ROME](https://rometools.github.io/rome/) - Usado para generar RSS

## Contribuyendo 🖇️

Por favor lee el [CONTRIBUTING.md](https://gist.github.com/villanuevand/xxxxxx) para detalles de nuestro código de conducta, y el proceso para enviarnos pull requests.

## Wiki 📖

Puedes encontrar mucho más de cómo utilizar este proyecto en nuestra [Wiki](https://github.com/tu/proyecto/wiki)

## Versionado 📌

Usamos [SemVer](http://semver.org/) para el versionado. Para todas las versiones disponibles, mira los [tags en este repositorio](https://github.com/tu/proyecto/tags).

## Autores ✒️

_Menciona a todos aquellos que ayudaron a levantar el proyecto desde sus inicios_

* **Andrés Villanueva** - *Trabajo Inicial* - [villanuevand](https://github.com/villanuevand)
* **Fulanito Detal** - *Documentación* - [fulanitodetal](#fulanito-de-tal)

También puedes mirar la lista de todos los [contribuyentes](https://github.com/your/project/contributors) quíenes han participado en este proyecto. 

## Licencia 📄

Este proyecto está bajo la Licencia (Tu Licencia) - mira el archivo [LICENSE.md](LICENSE.md) para detalles

## Expresiones de Gratitud 🎁

* Comenta a otros sobre este proyecto 📢
* Invita una cerveza 🍺 o un café ☕ a alguien del equipo. 
* Da las gracias públicamente 🤓.
* etc.

<!-- Recursos Link/Imagenes -->

[contributors-shield]: https://img.shields.io/static/v1?label=contributors&message=LEGO%20TEAM&color=GREEN
[version-shield]: https://img.shields.io/static/v1?label=version&message=1.0.0&color=GREEN
[download-shield]: https://img.shields.io/static/v1?label=download&message=clic&color=GREEN
[download-url]: https://globaldevtools.bbva.com/bitbucket/rest/api/latest/projects/BD_CS_DT_L/repos/gifole-job/archive?format=zip

[script1]: https://www.google.com
[script2]: https://www.google.com
[script3]: https://www.google.com
[script4]: https://www.google.com
[script5]: https://www.google.com
[script6]: https://www.google.com
[script7]: https://www.google.com
[script8]: https://www.google.com
[script9]: https://www.google.com
[script10]: https://www.google.com
[script11]: https://www.google.com
[script12]: https://www.google.com
[script13]: https://www.google.com
[repositorio-gifoleweb]: https://globaldevtools.bbva.com/bitbucket/projects/BD_CS_DT_L/repos/gifole-web
[repositorio-gifolejob]: https://globaldevtools.bbva.com/bitbucket/projects/BD_CS_DT_L/repos/gifole-job/browse

<!-- Pie de Página -->


⌨️ con 🥊 por LEAM-LEGO 🥇
