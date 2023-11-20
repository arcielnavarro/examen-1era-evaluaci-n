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

