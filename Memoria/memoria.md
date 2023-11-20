# Examen de Despliegue de Aplicaciones Web
## Resumen
Este documento proporciona una guía detallada y paso a paso de dos actividades fundamentales realizadas como parte del curso "Despliegue de Aplicaciones Web". La primera actividad implica el uso de SSH y la línea de comandos para interactuar con una máquina remota. En esta tarea, se accede remotamente a un servidor, donde se crea un archivo de texto nombrado con el nombre y apellido del usuario, seguido de la extensión `.txt`. Dentro de este archivo, se registra el resultado del comando `whoami` para identificar al usuario activo. Posteriormente, se añade al mismo archivo la información sobre quién está conectado al servidor a través de SSH mediante un comando específico de concatenación.

La segunda actividad se centra en la configuración de un Virtualhost. En esta parte, se establece un dominio ficticio `daw.ejercicio3.com` que, cuando se accede a él, redirige al usuario a una página web local. Esta página contiene únicamente el nombre del usuario. La configuración implica ajustes en el servidor y modificaciones en el archivo de hosts para asegurar una redirección correcta. Este ejercicio demuestra la habilidad para configurar y administrar un entorno de servidor web, así como para manipular el sistema de nombres de dominio a nivel local.
## Palabras Clave
- SSH
- Command Line
- Virtualhost
- Web Hosting
- Configuración de Servidor
## Índice
1. [Introducción](#introducción)
   1. [Contexto](#contexto)
   2. [¿Qué es?](#qué-es)
   3. [Alternativas](#alternativas)
   4. [Motivación](#motivación)
2. [Desarrollo](#desarrollo)
   1. [SSH + Command line](#ssh--command-line)
   2. [Virtualhost](#virtualhost)
   3. [Banco de Pruebas](#banco--de--pruebas)
3. [Conclusiones](#conclusiones)
4. [Bibliografía](#bibliografía)
5. [Anexos](#anexos)

## Introducción

### Contexto
Estas actividades se llevaron a cabo en el aula, un entorno controlado y diseñado para fomentar el aprendizaje práctico y la experimentación en el campo del despliegue de aplicaciones web. En este espacio, los estudiantes tienen la oportunidad de aplicar teorías y conceptos en situaciones prácticas, utilizando herramientas y tecnologías reales que se encuentran en el ámbito profesional. La realización de estas tareas en el aula permite un enfoque práctico, donde los errores y los descubrimientos se convierten en una parte fundamental del proceso de aprendizaje.

La razón principal para realizar estas actividades específicas, que incluyen la manipulación de SSH y la configuración de un Virtualhost, es doble. En primer lugar, proporcionan una experiencia directa y práctica de conceptos y herramientas esenciales en la administración de sistemas y el despliegue de aplicaciones web. En segundo lugar, estas actividades forman parte integral de la evaluación del curso, donde demostrar competencia y comprensión en estas áreas es crucial para obtener una calificación satisfactoria y, en última instancia, aprobar el examen. Este enfoque práctico y orientado a resultados en el aula es esencial no solo para el éxito académico sino también para preparar a los estudiantes para los desafíos reales en el ámbito profesional.

### ¿Qué es?
Un examen es una herramienta de evaluación estructurada y formal utilizada en contextos educativos para medir el conocimiento, las habilidades y la competencia de los estudiantes en un área de estudio específica. En este caso, el examen se centra en el "Despliegue de Aplicaciones Web", donde los estudiantes demuestran su comprensión y habilidad práctica en el uso de SSH, la línea de comandos y la configuración de servidores web a través de Virtualhost. El formato del examen combina elementos teóricos y prácticos, requiriendo no solo el conocimiento conceptual sino también la capacidad de aplicar ese conocimiento en situaciones prácticas. Este enfoque asegura una evaluación integral del aprendizaje del estudiante, abarcando tanto la comprensión teórica como la competencia técnica.

### Alternativas
Una alternativa al examen tradicional es el "aprendizaje basado en proyectos". Este enfoque involucra a los estudiantes en proyectos complejos y basados en la realidad que abarcan períodos de tiempo extendidos. A diferencia de los exámenes convencionales que a menudo se enfocan en tareas específicas y en el conocimiento a corto plazo, el aprendizaje basado en proyectos permite a los estudiantes explorar problemas y desafíos en profundidad, desarrollando soluciones creativas y prácticas. Este método fomenta el pensamiento crítico, la resolución de problemas y las habilidades de colaboración, y proporciona una aplicación más realista y holística del conocimiento y las habilidades adquiridas. En el contexto del "Despliegue de Aplicaciones Web", el aprendizaje basado en proyectos podría implicar el desarrollo de una aplicación web completa, desde la concepción hasta el despliegue, proporcionando a los estudiantes una experiencia de aprendizaje más integrada y aplicada.

### Motivación
La realización de este examen en el curso "Despliegue de Aplicaciones Web" es motivada por varias razones clave. Principalmente, el examen sirve como una medida concreta y objetiva para evaluar la competencia y el conocimiento de los estudiantes en aspectos fundamentales del despliegue de aplicaciones web, incluyendo el uso efectivo de SSH y la configuración de servidores web a través de Virtualhost. Esta evaluación no solo refleja el grado de comprensión teórica del estudiante, sino también su habilidad para aplicar prácticamente estos conocimientos en escenarios reales, un aspecto crítico en el campo de la tecnología de la información y la programación web.

Además, el examen actúa como un catalizador para el aprendizaje autodirigido y la investigación. Prepararse para el examen anima a los estudiantes a revisar y consolidar su aprendizaje, identificar áreas de debilidad y buscar recursos adicionales para reforzar su comprensión. Este proceso de preparación es en sí mismo una parte valiosa del viaje educativo, impulsando a los estudiantes a asumir la responsabilidad de su propio aprendizaje y desarrollo.

Finalmente, el examen proporciona una oportunidad para que los estudiantes demuestren su progreso y logros, no solo para sí mismos y sus instructores, sino también como una evidencia de sus habilidades y conocimientos para futuros empleadores o para estudios avanzados en el campo. En resumen, este examen es una parte esencial del curso, diseñado para evaluar y fomentar el crecimiento integral del estudiante en el ámbito del despliegue de aplicaciones web.

## Desarrollo

Este segmento del documento se divide en dos actividades principales: SSH + Command line y Virtualhost. Cada actividad representa un aspecto único y esencial del curso "Despliegue de Aplicaciones Web", demostrando habilidades prácticas y técnicas en el manejo de servidores y en la configuración de sitios web.

### SSH + Command line
El objetivo de esta actividad es demostrar la habilidad para conectarse y operar en una máquina remota utilizando SSH y la línea de comandos. Los pasos realizados son los siguientes:

1. **Acceso Remoto a la Máquina:**
   - Conectar a la máquina remota utilizando el comando SSH.
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/ssh/conexion%20al%20servidor.png)

2. **Creación de Archivo de Texto:**
   - Navegar al escritorio de la máquina remota.
   - Crear un archivo de texto con el nombre y apellido, sin espacios y con extensión `.txt` (ejemplo: `ArnoldSchwarzenegger.txt`).
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/ssh/creando%20el%20txt%20en%20el%20escritorio.png)

3. **Registro de Usuario Activo:**
   - Ejecutar el comando `whoami` y escribir el resultado en el archivo creado anteriormente.
   ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/ssh/escribiendo%20whoaim%20dentro%20del%20txt.png)

4. **Registro de Conexiones SSH:**
   - Utilizar un comando de concatenación para añadir al archivo de texto información sobre quién está conectado a la máquina mediante SSH.
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/ssh/concatenando%20al%20final%20del%20archivo.png)

### Virtualhost
Esta actividad se centra en la creación y configuración de un Virtualhost en la máquina del estudiante. Los pasos incluyen:

1. **Editar el Archivo Hosts:**
   Para que el dominio `daw.ejercicio3.com` se resuelva localmente a la dirección IP deseada, es necesario editar el archivo hosts del sistema.
   - Se abre el archivo con el comando `sudo nano /etc/hosts`.
   - Se añade la línea `127.0.0.1 daw.ejercicio3.com` al archivo para establecer la resolución local del dominio.
      ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/1%20sudo%20nano%20etchosts.png)
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/2%20configurando%20el%20archivo%20host.png)

2. **Configuración del Virtualhost:**
   Se procede a crear el archivo de configuración del Virtualhost para Apache.
   - Con `sudo nano /etc/apache2/sites-available/daw.ejercicio3.com.conf`, se configura el Virtualhost especificando el `ServerName`, `DocumentRoot`, y las rutas para los archivos de log.
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/3.0.png)
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/3%20conf%20el%20virtual%20host.png)
     
3. **Creación del Directorio de la Web y Página Inicial:**
   Se crea el directorio que albergará los archivos web y se escribe un archivo HTML básico.
   - Se utiliza `sudo mkdir /var/www/daw.ejercicio3.com` para crear el directorio.
   - Luego, `sudo nano /var/www/daw.ejercicio3.com/index.html` para crear la página inicial con contenido HTML básico.
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/creando%20el%20directorio%20y%20la%20pagina.png)
     ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/mi%20pagina.png)

4. **Activación del Virtualhost y Reinicio de Apache:**
   Finalmente, se activa el Virtualhost y se reinicia Apache para aplicar los cambios.
   - Se deshabilita el sitio predeterminado con `sudo a2dissite 000-default.conf`.
   - Se habilita el nuevo sitio con `sudo a2ensite daw.ejercicio3.com.conf`.
   - Se recarga la configuración de Apache con `sudo systemctl reload apache2`.
   ![imagen](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/deshabilitando%20el%20sitio%20por%20defecto.png)

5. **Verificación del Virtualhost:**
   Al acceder al dominio `daw.ejercicio3.com` desde un navegador, se muestra la página inicial creada, confirmando que el Virtualhost ha sido configurado correctamente.
   ![Verificación del Virtualhost](https://github.com/arcielnavarro/examen-1era-evaluaci-n/blob/main/Im%C3%A1genes/apache/pagina.png)

## Banco de Pruebas

Para asegurar que el Virtualhost ha sido configurado correctamente y funciona según lo esperado, se llevan a cabo las siguientes pruebas:

1. **Prueba de Resolución de DNS:**
   - **Objetivo:** Verificar que el dominio `daw.ejercicio3.com` resuelve a la dirección IP local `127.0.0.1`.
   - **Método:** Utilizar el comando `ping daw.ejercicio3.com` y asegurarse de que la respuesta proviene de `127.0.0.1`.
   - **Resultado Esperado:** El dominio debe resolver al loopback local.

2. **Prueba de Carga del Sitio Web:**
   - **Objetivo:** Confirmar que el sitio web se carga correctamente al visitar `daw.ejercicio3.com` en un navegador web.
   - **Método:** Abrir un navegador y escribir la URL `daw.ejercicio3.com`.
   - **Resultado Esperado:** La página de inicio que contiene el texto "Hola, soy Arciel." se muestra en el navegador.

3. **Prueba de Configuración del Servidor Web:**
   - **Objetivo:** Comprobar que Apache está sirviendo el sitio web desde el directorio correcto.
   - **Método:** Revisar los archivos de configuración de Apache y los logs de acceso para asegurarse de que las solicitudes a `daw.ejercicio3.com` están siendo dirigidas al directorio `/var/www/daw.ejercicio3.com`.
   - **Resultado Esperado:** Los logs deben indicar que las solicitudes HTTP se sirven desde el directorio especificado.

4. **Prueba de Archivos de Log:**
   - **Objetivo:** Asegurar que los logs de error y acceso están siendo escritos correctamente.
   - **Método:** Generar tráfico al sitio y luego revisar `error.log` y `access.log` en `/var/log/apache2/` para cualquier actividad reciente.
   - **Resultado Esperado:** Los logs deben reflejar las solicitudes recientes y cualquier error, si lo hubiera.


