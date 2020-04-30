# Gifole Job

<!-- Etiquetas Cabecera -->

![Contributors][contributors-shield]
![Version][version-shield]
[![Download][download-shield]][download-url]

<!-- Cuerpo de Readme -->

## Comenzando 🚀

_Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas._

## Pre-requisitos 📋

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

## Configurando Ambiente 🔧

_Estas instrucciones te permitirán configurar las herramientas necesarias para levantar el aplicativo._

🔨 [Importar la Base de Datos]

```
📢 Ejecutar los script en el siguiente orden
```
_>>>> Creación de tablespaces - [script][script1]._

_>>>> Creación de directorios - [script][script2]._

_>>>> Creación de usuarios - [script][script3]._

_>>>> Creación de secuencias - [script][script4]._

_>>>> Creación de tablas de Gifole - [script][script5]._

_>>>> Creación de data para tablas de Gifole - [script][script6]._

_>>>> Creación de índices para Gifole - [script][script7]._

_>>>> Creación de tablas de Gifpri - [script][script8]._

_>>>> Creación de data para tablas Gifpri - [script][script9]._

_>>>> Creación de índices para Gifpri - [script][script10]._

_>>>> Creación de tablas de Gifole(Job) - [script][script11]._

_>>>> Creación de data para tablas de Gifole(Job) - [script][script12]._

_>>>> Creación de tablas de Gifole(Quartz) - [script][script13]._

🔨 [Descargar fuentes Gifole]

```
📢 Clonar las fuentes y configurarlo de acuerdo a las instrucciones del repositorio._
    🚨 https://globaldevtools.bbva.com/bitbucket/projects/BD_CS_DT_L/repos/gifole-web
```

🔨 [Descargar fuentes Job]

```
📢 Clonar las fuentes._
    🚨 https://globaldevtools.bbva.com/bitbucket/projects/BD_CS_DT_L/repos/gifole-job/browse
```

🔨 [Importar Proyecto con Eclipse]

```
📢 Verificar que la versión sea JDK11 antes de iniciar el IDE.
📢 Importar como proyecto Maven.
📢 Verificar que exista el artefacto de GifoleWeb creado ([Ver Instrucciones de GifoleWeb][repositorio-gifoleweb]).
    🚨 Nombre: gifole-web-0.8.1-classes.jar
    🚨 Ruta: C:\Users\TU-USUARIO\.m2\repository\pe\com\bbva\gifole-web\0.8.1
📢 Cambiar de nombre al artefacto cada vez que GifoleWeb genere uno nuevo.
    🚨 Original: gifole-web-0.8.1-classes.jar
    🚨 Nuevo: gifole-web-0.8.1.jar
📢 Generar el artefacto de GifoleJob (mvn clean install).
📢 Actualizar el proyecto Maven en el IDE (Alt+F5).
```

🔨 [Configurar Jboss]

```
📢 Descargar e instalar el adaptador de servidor de aplicaciones Jboss para el IDE.
    🚨 Install New Software.
    🚨 Ingresar en Work With: http://download.jboss.org/jbosstools/updates/webtools/photon/
    🚨 Seleccionar: Jboss Application Server Adapters.
📢 Agregar el servidor al IDE.
    🚨 Red Hat Jboss Middleware.
    🚨 Seleccionar la versión de Java11 antes de finalizar.
📢 Agregar JNDI.
    🚨 Ingresar a la carpeta en el servidor "jboss-eap-7.2\standalone\configuration".
    🚨 Abrir el archivo "standalone.xml".
    🚨 Dentro de la etiqueta "<datasources>" agregar el JNDI de GIFPRI
        <datasource jndi-name="java:jboss/datasources/APP_GIFPRI" pool-name="jdbc/APP_GIFPRI" enabled="true">
            <connection-url>jdbc:oracle:thin:@localhost:1521:xe</connection-url>
            <driver-class>oracle.jdbc.driver.OracleDriver</driver-class>
            <driver>oraclethin</driver>
            <security>
                <user-name>APP_GIFPRI</user-name>
                <password>APP_GIFPRI</password>
            </security>
            <validation>
                <valid-connection-checker class-name="org.jboss.jca.adapters.jdbc.extensions.oracle.OracleValidConnectionChecker"/>
                <background-validation>true</background-validation>
                <stale-connection-checker class-name="org.jboss.jca.adapters.jdbc.extensions.oracle.OracleStaleConnectionChecker"/>
                <exception-sorter class-name="org.jboss.jca.adapters.jdbc.extensions.oracle.OracleExceptionSorter"/>
            </validation>
        </datasource>
    🚨 En la misma etiqueta <datasources> agregar el JNDI de GIFOLE
        <datasource jndi-name="java:jboss/datasources/APP_GIFOLE" pool-name="jdbc/APP_GIFOLE" enabled="true">
            <connection-url>jdbc:oracle:thin:@localhost:1521:xe</connection-url>
            <driver-class>oracle.jdbc.driver.OracleDriver</driver-class>
            <driver>oraclethin</driver>
            <security>
                <user-name>APP_GIFOLE</user-name>
                <password>APP_GIFOLE</password>
            </security>
            <validation>
                <valid-connection-checker class-name="org.jboss.jca.adapters.jdbc.extensions.oracle.OracleValidConnectionChecker"/>
                <background-validation>true</background-validation>
                <stale-connection-checker class-name="org.jboss.jca.adapters.jdbc.extensions.oracle.OracleStaleConnectionChecker"/>
                <exception-sorter class-name="org.jboss.jca.adapters.jdbc.extensions.oracle.OracleExceptionSorter"/>
            </validation>
        </datasource>
    🚨 Dentro de la etiqueta "<datasources>" en la etiqueta <drivers> agregar el driver de Oracle.                
        <driver name="oraclethin" module="com.oracle.ojdbc18">
                <driver-class>oracle.jdbc.driver.OracleDriver</driver-class>
                <xa-datasource-class>oracle.jdbc.xa.client.OracleXADataSource</xa-datasource-class>
        </driver>
📢 Agregar módulo.
    🚨 Ingresar a la carpeta en el servidor "jboss-eap-7.2\modules\system\layers\base\com\oracle\ojdbc18\main".
    🚨 Si no existe, crear las carpetas necesarias.
    🚨 En esa carpeta colocar el "ojdbc6.jar" y crear el archivo "module.xml" con lo siguiente:
        <?xml version="1.0" encoding="UTF-8"?>
        <module xmlns="urn:jboss:module:1.1" name="com.oracle.ojdbc18">
          <resources>
            <resource-root path="ojdbc6.jar"/>
          </resources>
          <dependencies>
            <module name="javax.api"/>
            <module name="javax.transaction.api"/>
          </dependencies>
        </module>
```

## Despliegue 📦

_Estas instrucciones fueron usadas para desplegar el aplicativo con integración continua._

🔨 [Jenkins]

```
📢 Agregar el archivo Jenkinsfile en la carpeta raiz y agregar las siguientes líneas.

    @Library("workflow-spring") _

    spring {
        country = 'pe'
        group = 'generic_maven_java_11_deploy'
        uuaa = 'bnet-zonapublica-pe-mvn'
        vars = [
            path_pom: '.',
            artifactory_id: 'bot-bnet',
            include_files: './target/gifole-job.war'
        ]
    }
    
📢 Agregar el artefacto de Gifole de la carpeta ".m2" con el nombre "gifole-web-0.8.1.jar".
📢 Ingresar a la siguiente página para subirlo.
    https://globaldevtools.bbva.com/piaas-pe/job/Tools/job/deploy_artifactory_whithout_pom/build?delay=0sec
📢 Ingresar los datos solicitados
    -> GROUP_ID: pe.com.bbva
    -> ARTIFACT_ID: gifole-web
    -> VERSION: 0.8.1
📢 Crear una segunda rama en base a "master" con nombre "develop".
📢 Empujar un cambio en "develop" para que reconozca que hay un cambio y despliegue en JBoss.
📢 Solo los cambios en "develop" generan despliegue en JBoss.
```

## Construido con 🛠️

_Menciona las herramientas que utilizaste para crear tu proyecto_

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - El framework web usado
* [Maven](https://maven.apache.org/) - Manejador de dependencias
* [ROME](https://rometools.github.io/rome/) - Usado para generar RSS

## Team Lego ✒️

* **Diego Clemente** - *scrum Master* - [villanuevand](https://github.com/villanuevand)
* **Gian Carlo Quiroz** - *Team Member* - [fulanitodetal](#fulanito-de-tal)

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
