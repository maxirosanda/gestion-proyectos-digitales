# Resumen de Repaso - Gestión de Proyectos Digitales

## 1. Estructura de Desglose del Trabajo (EDT / WBS) y Regla 8/80
* **EDT (Estructura de Desglose del Trabajo)** = WBS (Work Breakdown Structure, en inglés).
* Es una descomposición jerárquica y orientada a entregables de todo el alcance del trabajo del proyecto.
* Organiza el trabajo por QUÉ hay que entregar, no por fechas ni orden de ejecución (eso es el cronograma).
* Se descompone en niveles cada vez más chicos hasta llegar a los paquetes de trabajo (el nivel más bajo).
* **Regla del 8/80:** un paquete de trabajo bien dimensionado debe representar entre 8 y 80 horas de trabajo.
  * **Menos de 8 hs** -> sobre-descomposición, overhead innecesario.
  * **Más de 80 hs** -> difícil de estimar y controlar bien.

## 2. Competencias del PM (Triángulo de Talento)
Las tres competencias del Director de Proyecto (PMI Talent Triangle):
* **Conocimiento** - saber de gestión de proyectos (procesos, herramientas, terminología).
* **Desempeño** - aplicar ese conocimiento y lograr resultados reales.
* **Liderazgo** - guiar, motivar e influir en equipo y stakeholders.

## 3. Triángulo de Hierro
Las tres variables en tensión permanente que el PM debe equilibrar:
**Calidad - Costos - Duración**
* Si tocas una punta, las otras se ven afectadas (más alcance/calidad sin más tiempo ni costo = algo se rompe).

## 4. Enfoques de Ciclo de Vida
Reconocidos por el PMBOK 7:
* **Predictivo (Cascada)** - todo planificado de antemano, fases secuenciales.
* **Ágil** - iteraciones cortas (sprints), entrega incremental, se adapta sobre la marcha.
* **Híbrido** - combina ambos (ej: planificación macro predictiva + ejecución ágil por sprints).

## 5. Cadena de Procesos del Cronograma (Predictivo/Cascada)
Secuencia de 4 procesos, cada uno alimenta al siguiente:

| Proceso | Salida principal |
| :--- | :--- |
| 1. Definir Actividades | Lista de actividades, atributos, lista de hitos |
| 2. Secuenciar Actividades | Diagrama de red del cronograma |
| 3. Estimar Duración de Actividades | Estimaciones de duración + base de estimaciones |
| 4. Desarrollar el Cronograma | Cronograma con fechas (línea base) |

Pertenece al enfoque predictivo/cascada (en Ágil no se secuencia todo de entrada; se trabaja con Product Backlog y sprints).

**Notación: Lead vs. Lag**
* **Lead (adelanto)** = valor negativo, permite solapar actividades y comprimir el cronograma.
* **Lag (retraso)** = valor positivo, introduce espera obligatoria entre actividades.

**Cono de incertidumbre**
* Al inicio del proyecto, una estimación puede variar respecto al valor real en un factor de hasta +/-4x. El cono se va cerrando (más precisión) a medida que avanza el proyecto y se conoce más el alcance.

## 6. Tipos de Dependencias

| Tipo | Descripción | Riesgo típico |
| :--- | :--- | :--- |
| **Obligatoria** | Técnicamente necesaria, no hay otra opción | Bloqueos si no se resuelve |
| **Discrecional** | Elegida por el equipo (buena práctica/conveniencia), no obligatoria técnicamente | Alargar innecesariamente el cronograma |
| **Externa** | Depende de un tercero fuera del proyecto | Retrasos imprevistos de terceros |
| **Obligatoria contractual** | Obligatoria por un contrato/norma legal | Incumplimiento legal |

*Ejemplo discrecional:* "implementar primero el login porque facilita las pruebas" - se podría hacer en otro orden, es una elección del equipo.

## 7. Objetivo y Meta
* **Objetivo** = el QUÉ. Fin último, más abstracto y de largo alcance.
* **Metas** = el CÓMO. Pasos intermedios, concretos y medibles, que llevan al objetivo.
*(SMART se usa típicamente para definir bien las metas - ver punto 19)*

## 8. Paquete de Trabajo vs. Actividad
* **Paquete de trabajo** -> vive en la EDT, es un entregable/componente del alcance (qué hay que producir). No tiene duración por sí mismo.
* **Actividad** -> vive en el cronograma, es una acción específica con duración (cómo se ejecuta). Se obtiene descomponiendo cada paquete de trabajo.

## 9. Tres Pilares de la Gestión de Proyectos (PMBOK 7, 2021)
* **Principios** - 12 reglas/valores generales que guían el comportamiento del PM y del equipo.
* **Dominios de Desempeño** - 8 áreas de trabajo interconectadas (incluye el Dominio de Financiamiento, desde donde se gestionan costos).
* **Modelos, Métodos y Artefactos** - caja de herramientas práctica (técnicas, plantillas, documentos).

*Nota: el PMBOK 7 es la última edición, publicada en 2021, y marcó el cambio de un enfoque por "procesos y áreas de conocimiento" (ediciones previas) a este de principios/dominios/valor.*

## 10. Gestión del Valor Ganado (EVM)

### Glosario de siglas

| Sigla | Nombre completo | Qué significa |
| :--- | :--- | :--- |
| **PV** | Planned Value | Lo que debería haberse gastado a esta altura, según el plan (visión PREVISTO) |
| **AC** | Actual Cost | Lo que realmente se gastó hasta hoy (visión ACTUAL) |
| **EV** | Earned Value | Valor del trabajo realmente completado, en términos de presupuesto |
| **CV** | Cost Variance | Diferencia en dinero entre valor ganado y gastado |
| **CPI** | Cost Performance Index | Eficiencia del costo (ratio) |
| **SV** | Schedule Variance | Diferencia en dinero entre avance real y planeado |
| **SPI** | Schedule Performance Index | Eficiencia del cronograma (ratio) |
| **BAC** | Budget at Completion | Presupuesto total aprobado del proyecto (un número fijo) |
| **EAC** | Estimate at Completion | Proyección de cuánto se va a terminar gastando (visión FINAL) |

### Fórmulas
* **CV** = EV - AC -> positivo = bajo presupuesto (bueno)
* **CPI** = EV / AC -> mayor a 1 = eficiente
* **SV** = EV - PV -> positivo = adelantado en cronograma
* **SPI** = EV / PV -> mayor a 1 = adelantado en tiempo

### Línea base de costo (Cost Baseline)
Es el plan completo de costo distribuido en el tiempo (la Curva S: empieza en $0, llega al 100% del presupuesto al cierre). El desempeño de costos se mide contra esta línea base, no contra el BAC (que es solo el número final/destino, no el mapa completo del camino).

### Curva S - fases
* **Inicio:** gasto lento (planificación).
* **Fase intermedia:** pendiente pronunciada, ejecución intensa, máximo gasto.
* **Cierre:** desaceleración, lecciones aprendidas.

### Reservas
* **Reservas de contingencia** -> cubren riesgos conocidos, van dentro de la línea base de costo.
* **Reservas de gestión** -> cubren riesgos desconocidos, van fuera de la línea base (requieren aprobación especial).

### Costos directos vs. indirectos
* **Directos** -> atribuibles a un solo proyecto; los controla principalmente el PM.
* **Indirectos** -> benefician a más de un proyecto/organización; se asignan como % sobre los directos; se gestionan a nivel organizacional.

### Rolling Wave (planificación gradual)
La estimación de costos se refina progresivamente a medida que se conocen más detalles del alcance (conectado con el cono de incertidumbre).

## 11. Fórmula para Comunicar Información (DCD)
**Dato -> Contexto -> Decisión**
* **Dato** - el hecho concreto y objetivo.
* **Contexto** - qué significa, por qué importa.
* **Decisión** - qué se va a hacer al respecto.
*Para mensajes cortos / actualizaciones rápidas.*

## 12. Estructura Narrativa de un Informe (CSAD)
**Contexto -> Situación -> Análisis -> Decisión**

| Paso | Responde a | Ejemplo (login caído) |
| :--- | :--- | :--- |
| **Contexto** | ¿Dónde estamos? ¿Qué esperábamos? | "El login funciona estable hace 3 sprints, sin incidentes" |
| **Situación** | ¿Qué pasó? ¿Hay desvíos? | "Desde ayer falla para el 30% de usuarios" |
| **Análisis** | ¿Por qué? ¿Qué impacto tiene? | "Fue un cambio en el servidor; si no se resuelve, se pierden ventas" |
| **Decisión** | ¿Qué hacemos? ¿Qué pedimos? | "Revertir el cambio o sumar 2 devs hoy" |

*Para informes/documentos más largos (no confundir con la fórmula DCD, que es para mensajes cortos).*

## 13. Resumen Ejecutivo de una Página con Semáforos (Cascada)
Documento breve con indicadores tipo semáforo (verde/amarillo/rojo) para que dirección/sponsor vean el estado general sin leer el detalle. Típico de proyectos predictivos/cascada - en Scrum se reemplaza por la demo del Sprint Review.

## 14. Matrices de Riesgo

### Matriz de Probabilidad e Impacto (3x3) - clasifica la gravedad

| | Impacto BAJO | Impacto MEDIO | Impacto ALTO |
| :--- | :--- | :--- | :--- |
| **Prob. ALTA** | Atención | Inaceptable | Inaceptable |
| **Prob. MEDIA** | Aceptable | Atención | Inaceptable |
| **Prob. BAJA** | Aceptable | Aceptable | Atención |

### Matriz de Decisión - recomienda la estrategia de respuesta

| | Impacto BAJO | Impacto ALTO |
| :--- | :--- | :--- |
| **Prob. ALTA** | Mitigar | Evitar/Mitigar (máxima prioridad) |
| **Prob. BAJA** | Aceptar con contingencia y monitorear | Transferir (seguros/terceros) |

*(Confirmar con el apunte de la Clase 9 el criterio exacto para los casos de impacto/probabilidad MEDIA, ya que no estaba 100% especificado en el material).*

### Exposición Residual
La clasificación final del riesgo se basa en la Exposición Residual (después de aplicar la acción de contingencia), no en la inherente.

### Human-in-the-Loop (IA + gestión de riesgos)
La IA genera el 80% del análisis; el PM aporta el 20% crítico: contexto político, relaciones interpersonales, restricciones no documentadas.

## 15. Roles

### Roles en SCRUM (Ágil) - sin jefe interno, poder distribuido
| Rol | Función |
| :--- | :--- |
| **Product Owner (PO)** | Gestiona y prioriza el Product Backlog; decide QUÉ se construye |
| **Scrum Master (SM)** | Facilita, remueve impedimentos; no es jefe. Único que puede cancelar un sprint |
| **Development Team** | Construye el producto; autoorganizado, sin líder interno - cada uno elige sus tareas |

### Roles en Cascada (Predictivo) - jerárquico
| Rol | Función |
| :--- | :--- |
| **Sponsor** | Financia y autoriza a alto nivel |
| **Director de Proyecto / PM** | Autoridad centralizada: planifica, ejecuta, controla, asigna tareas (es el "jefe de grupo") |
| **Equipo** | Ejecuta lo que le asigna el PM |
| **Stakeholders** | Reciben informes de estado formales |

## 16. Jerarquía JIRA
De mayor a menor granularidad:
**Tema -> Iniciativa -> Épica -> Historia -> Tarea**

* **Historia de Usuario:** "Como [usuario], quiero [funcionalidad], para [beneficio]." Es exclusiva de metodologías Ágiles (en Cascada se usan requisitos formales, no historias).

## 17. Planning Poker
Técnica que usa el equipo para estimar el esfuerzo relativo de cada historia (story points, típicamente escala Fibonacci).
* Exclusivo de Ágil.
* Flujo del caso práctico: estimar con Planning Poker -> aprobar presupuesto -> el cliente/PO reprioriza la pila según urgencia.

## 18. Scrum: Roles, Eventos/Ceremonias y Artefactos

### Artefactos
| Artefacto | Qué es |
| :--- | :--- |
| **Product Backlog** | Lista completa de todo lo que el producto podría necesitar, priorizada por el PO |
| **Sprint Backlog** | Subconjunto del Product Backlog elegido para el sprint actual + plan |
| **Incremento** | Producto funcionando, resultado acumulado hasta ahora |

### Eventos/Ceremonias (en orden)
| Evento | Cuándo | Produce |
| :--- | :--- | :--- |
| **Sprint Planning** (2 reuniones) | Inicio del sprint | 1ra: Objetivo del Sprint / 2da: Sprint Backlog (decidido por el equipo) |
| **Daily Scrum** | Diario, 15 min | Sincronización entre pares (NO reporte al SM, NO resuelve problemas ahí) |
| **Sprint Review** | Fin del sprint | Demo del incremento al cliente; lo no terminado no se presenta |
| **Sprint Retrospective** | Después del Review | El equipo mejora su propio proceso de trabajo |

**Duración de tareas del Sprint Backlog:**
Entre 4 y 16 horas (equivalente a la regla 8/80 pero a escala de sprint).

## 19. SMART
Técnica para definir objetivos/metas claros. Antídoto contra la falta de definición clara de objetivos.
* **S**pecific (Específico)
* **M**easurable (Medible)
* **A**chievable (Alcanzable)
* **R**elevant (Relevante)
* **T**ime-bound (con tiempo definido)
*Transversal a Cascada (objetivo general del proyecto) y Ágil (Objetivo del Sprint, criterios de aceptación de historias).*

## 20. Fases del Modelo Cascada
5 fases, en orden:
1. Análisis
2. Diseño
3. Implementación
4. Pruebas
5. Despliegue y Mantenimiento

*Truco: entender QUÉ hacer -> planear CÓMO -> CONSTRUIR -> CHEQUEAR que funcione -> ENTREGAR y sostener.*
