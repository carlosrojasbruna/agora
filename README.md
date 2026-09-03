Ágora

Maqueta de una plataforma donde estudiantes universitarios responden preguntas de selección múltiple, las valoran con una rúbrica y dejan retroalimentación escrita para quien las diseñó.

Versión para prueba de usabilidad con un curso de Álgebra Lineal (MAT1219), Pontificia Universidad Católica de Chile. Proyecto Fondedoc. No es la versión final del sistema.

Demo: https://<usuario>.github.io/AGORA/ Para estudiantes: https://<usuario>.github.io/AGORA/?piloto=1 — oculta la barra de controles de demostración.

Qué hace

Cada estudiante entra con un código individual (EST-001 … EST-016), sin correo ni contraseña, y recorre ocho preguntas. En cada una:

Responde y ve de inmediato si acertó, con la solución comentada.
Valora la pregunta en cuatro criterios de tres niveles: claridad del enunciado, dificultad, calidad de las alternativas incorrectas y utilidad de la solución.
Comenta para quien diseñó la pregunta, con un mínimo de 120 caracteres.

Al completar los tres pasos gana una estrella. Hay cuatro insignias por hitos y no hay ranking entre compañeros. La recompensa depende solo de completar el ciclo: nunca de acertar ni de valorar alto.

Al final responde una encuesta de salida de cinco preguntas sobre la plataforma.

Panel docente

Ocho pestañas de solo lectura: diagnóstico automático, resultados por pregunta, vista general de participación, comentarios, carga de preguntas, rúbrica y ajustes, telemetría y exportación.

El diagnóstico cruza lo que los estudiantes hicieron (qué alternativa eligieron, cuánto tardaron) con lo que dijeron (la rúbrica), y levanta desajustes: un distractor que supera a la clave, una pregunta valorada como difícil que casi todos aciertan, distractores que nadie elige.

Exporta ocho archivos CSV: respuestas, valoraciones, comentarios, ciclos y tiempos, bitácora de eventos, encuesta de salida, asistente de escritura y diagnóstico.

La IA es simulada

No hay ningún modelo detrás. Los cinco chatbots —bienvenida, valoración, comentario, encuesta y panel docente— funcionan con reglas sobre el texto y sobre los datos ya recogidos. Responden con la alternativa que el estudiante eligió, la clave real, su propia valoración y el mínimo de caracteres configurado, y por eso suenan razonables. Ante una pregunta fuera de alcance dicen que no saben en lugar de inventar.

Es un Wizard of Oz, un método estándar en investigación de usabilidad. Si se usa con estudiantes, corresponde decírselo en el cierre de la sesión.

Los datos se quedan en cada dispositivo

La maqueta guarda todo en localStorage del navegador. No hay servidor. Las respuestas de cada estudiante se quedan en su teléfono y no llegan al panel de la docente: cada quien ve solo su propia sesión.

Para llenar el panel en una demostración, usa «Simular el curso completo» en la barra superior.

Para recoger datos reales del piloto hace falta resolverlo antes: que cada estudiante exporte su CSV al terminar, o conectar un backend.

Privacidad

Las respuestas, valoraciones y comentarios viajan solo con el código del estudiante. Ningún archivo exportado contiene nombres. Los comentarios los lee únicamente la docente: no son visibles entre pares, porque con un grupo de dieciséis personas que se conocen la visibilidad pública produce comentarios corteses y poco críticos.

Fuera de alcance

No incluye creación de preguntas por parte de estudiantes, evaluación automática, calificaciones, hilos de discusión, integración con LMS ni cuentas con correo y contraseña.

Detalles técnicos

Un solo archivo HTML sin dependencias de compilación. Actualizar es reemplazar index.html.

KaTeX para la notación matemática, desde cdnjs.
Kit Digital UC (kitdigital.uc.cl) para la paleta, la tipografía (Roboto y Roboto Slab), los radios y las sombras.
Diseño responsivo, pensado para el celular, que es como los estudiantes lo usarán en clase.

Requiere conexión para las tipografías, KaTeX y el logo institucional. Si el logo no carga, la cabecera se ajusta sola.
