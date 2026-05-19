# Auditoría ASG y Refactorización Sostenible

# I. Inventario y Dimensión Ambiental (A)

Analiza el peso y consumo de la web elegida.

### 1.1. **Medición inicial**. Utiliza herramientas gratuitas como *Website Carbon Calculator* o *Lighthouse* (pestaña de rendimiento en Chrome/Edge) para obtener la huella de carbono estimada por visita.

La herramienta que vamos a utilizar para obtener la huella de carbono estimada por visita es Lighthouse, que es una pestaña de rendimiento en Chrome/Edge.

### 1.2. **Identificación de Bloatware**. Inspecciona la red (Network) en las herramientas de desarrollador del navegador. Identifica los 3 recursos más pesados que se descargan al abrir la web (imágenes sin comprimir, vídeos de fondo, librerías JavaScript pesadas, etc.).

Se descargan los siguientes recursos que vemos en la captura. De ellos, los más pesados son un documento de 443kB y dos scripts, el más pesado de 226kB y el menos pesado de 12.9 kB.

<div align="center">
  <img width="700" height="600" alt="Captura de pantalla 2026-05-12 112758" src="https://github.com/user-attachments/assets/7fa4007f-13ce-4266-aa6e-85b323d3c865"/>
</div>

### 1.3. **Análisis**. ¿Crees que la web sufre de "inflación de software"? Justifica tu respuesta.
Teniendo en cuenta que cada minuto que pasa va creciendo el número de recursos, pasando desde que lo abrimos por primera vez, de 49 hasta 56 en cuestión de minutos.
Decimos que sí hay inflación de software, aunque no a gran escala porque la cantidad de procesos, aunque aumenta, no consideramos que sea excesiva. El rendimiento en dispositivos móviles es más bajo, con una puntuación de 41 y en ordenadores con una puntuación de 69, un poco más alta, pero aún así sigue muy lejos del 100.
<img width="959" height="788" alt="Captura de pantalla 2026-05-12 115700" src="https://github.com/user-attachments/assets/2e870d03-f090-4f3c-87a2-bea8121153b6" />
<img width="960" height="794" alt="Captura de pantalla 2026-05-12 115723" src="https://github.com/user-attachments/assets/64f72c0c-d706-4325-a617-f96de90afc82" />
# Dimensión Social y Equidad (S)

La web debe ser utilizable por todos. Evalúa la accesibilidad (Sostenibilidad Social):

## 2.1. **Test de Accesibilidad**. Pasa una herramienta como *WAVE Web Accessibility Evaluation Tool* o el propio *Lighthouse* (pestaña *Accessibility*).

| Herramienta | Métrica / Resultado General | Observaciones Clave |
| :---- | :---- | :---- |
| **Lighthouse** | Puntuación (0-100) | Analiza la estructura semántica y mejores prácticas de ARIA. |
| **WAVE** | Número de Errores y Alertas | Detecta fallos de contraste y errores en el orden de los encabezados. |

## 2.2. **Identificación de barreras**. Documenta al menos 2 problemas graves que impidan a personas con diversidad funcional usar la web correctamente (ej. falta de atributos *alt* en imágenes clave, bajo contraste de colores en botones, formularios sin etiquetas).

### 2.2.1. Problema A: Ausencia de Texto Alternativo (alt) en Imágenes Funcionales

Este es un fallo crítico de **Sostenibilidad Social**, ya que excluye directamente a los usuarios de lectores de pantalla (personas con ceguera o baja visión).

* **Descripción:** Si una imagen que transmite información (como un icono de "Carrito" o un gráfico de datos) no tiene el atributo alt, el lector de pantalla dirá simplemente "Imagen" o leerá el nombre del archivo (ej. IMG\_5432.jpg), dejando al usuario sin contexto.  
* **Impacto:** El usuario no puede completar procesos de navegación o compra porque no entiende qué acción representa el elemento visual.  
* **Solución:** Implementar descripciones claras: \<img src="check.png" alt="Pedido completado con éxito"\>.

### 2.2.2. Problema B: Insuficiente Contraste de Color en Textos y Botones

El bajo contraste es una barrera que afecta a personas con daltonismo, visión reducida o incluso a usuarios en condiciones de mucha luz solar.

* **Descripción:** Ocurre cuando la relación de contraste entre el color del texto y el fondo es inferior a **4.5:1** (según las pautas WCAG 2.1). Por ejemplo, un texto gris claro sobre un fondo blanco.  
* **Impacto:** Fatiga visual y falta de legibilidad. En botones de llamada a la acción (CTA), esto puede causar que el usuario ni siquiera perciba que existe un botón.  
* **Solución:** Ajustar la paleta de colores para asegurar que todos los elementos interactivos cumplan con los estándares de ratio de contraste.

Para elevar la equidad de la web de forma inmediata, se recomienda asegurar la **Navegación por Teclado**. Muchas webs olvidan el "foco" (el recuadro que indica dónde estás al pulsar Tab). Sin un indicador de foco visible, los usuarios con diversidad funcional motriz no pueden saber qué elemento están seleccionando. 
