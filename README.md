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
Teniendo en cuenta que cada minuto que pasa va creciendo el número de recursos, pasando desde que lo abrimos por primera vez, de 49 hasta 56 en cuestión de minutos.
Decimos que sí hay inflación de software, aunque no a gran escala porque la cantidad de procesos, aunque aumenta, no consideramos que sea excesiva. El rendimiento en dispositivos móviles es más bajo, con una puntuación de 41 y en ordenadores con una puntuación de 69, un poco más alta, pero aún así sigue muy lejos del 100.
<img width="959" height="788" alt="Captura de pantalla 2026-05-12 115700" src="https://github.com/user-attachments/assets/2e870d03-f090-4f3c-87a2-bea8121153b6" />
<img width="960" height="794" alt="Captura de pantalla 2026-05-12 115723" src="https://github.com/user-attachments/assets/64f72c0c-d706-4325-a617-f96de90afc82" />
