# Auditoría ASG y Refactorización Sostenible

## Inventario y Dimensión Ambiental (A)

Analiza el peso y consumo de la web elegida.

1. **Medición inicial**. Utiliza herramientas gratuitas como *Website Carbon Calculator* o *Lighthouse* (pestaña de rendimiento en Chrome/Edge) para obtener la huella de carbono estimada por visita.

La herramienta que vamos a utilizar para obtener la huella de carbono estimada por visita es Lighthouse, que es una pestaña de rendimiento en Chrome/Edge.

2. **Identificación de Bloatware**. Inspecciona la red (Network) en las herramientas de desarrollador del navegador. Identifica los 3 recursos más pesados que se descargan al abrir la web (imágenes sin comprimir, vídeos de fondo, librerías JavaScript pesadas, etc.).

Se descargan los siguientes recursos que vemos en la captura. De ellos, los más pesados son un documento de 443kB y dos scripts, el más pesado de 226kB y el menos pesado de 12.9 kB.

<div align="center">
  <img width="700" height="600" alt="Captura de pantalla 2026-05-12 112758" src="https://github.com/user-attachments/assets/7fa4007f-13ce-4266-aa6e-85b323d3c865"/>
</div>

3. **Análisis**. ¿Crees que la web sufre de "inflación de software"? Justifica tu respuesta.
