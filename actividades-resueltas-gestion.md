# Desafío del líder — Modelar la situación problema [source: 1]

## Consigna y resolución

### 1. Consigna
**Modelar la situación problema. (15 min)**
Cada grupo recibió una ficha detallando la situación del proyecto que deben liderar. Se pide armar una propuesta de abordaje realizando lo siguiente:
* **Analizar el caso:** leer la ficha y entender qué éxito espera el cliente.
* **Repartir el esfuerzo:** se dispone de 100 puntos de esfuerzo para repartir entre las 4 actividades de la ficha. ¿A qué se le dedicará más esfuerzo y a qué menos?
* **Priorizar:** enumerar las actividades del 1 al 4, según cuál iría primero y cuál después.
* **Entregable:** los 3 puntos resueltos y listos para defenderse.
* **Defensa intermedia:** se elige a alguno para que presente y defienda lo hecho.

#### Ficha A — Clínica privada (chatbot con IA)
* **Contexto:** una clínica privada quiere reducir un 40% las consultas administrativas. No quieren un buscador de turnos tradicional, sino un chatbot con IA que entienda lenguaje natural y resuelva gestiones.
* **Alcance (lo pactado):**
  * **Chatbot con LLM:** integración de una IA (tipo GPT) que responda dudas sobre cobertura y requisitos médicos.
  * **Triaje automático:** un sistema que analice síntomas básicos del paciente y sugiera la especialidad médica adecuada.
  * **Agendamiento por voz/texto:** el bot debe poder reservar el turno directamente en la base de datos de la clínica.
  * **Validación biométrica:** registro del paciente mediante reconocimiento facial o foto de DNI para evitar fraudes.
* **Recursos:** 1 especialista en IA/Prompt Engineering y 2 desarrolladores Fullstack. **Tiempo:** 12 semanas. **Presupuesto:** $8.500 USD (sueldos + créditos de API de OpenAI + infraestructura cloud).

#### Ficha B — Tienda online (recomendador de productos)
* **Contexto:** una tienda online quiere una IA que recomiende productos según lo que el cliente compró antes para subir las ventas.
* **Alcance (lo pactado):**
  * Limpieza y ordenamiento de la base de datos de ventas histórica.
  * Algoritmo de recomendación (Machine Learning).
  * Integración del recomendador en la Home de la web.
  * Panel de métricas para ver si las ventas subieron.
* **Recursos:** 1 Data Scientist y 1 Ingeniero de Datos. **Tiempo:** 10 semanas. **Presupuesto:** $5.500 USD (créditos en la nube + sueldos).

#### Ficha C — Academia de manejo (simulador 3D)
* **Contexto:** una academia quiere un simulador 3D básico para que los alumnos practiquen antes de usar un auto real.
* **Alcance (lo pactado):**
  * Escenario urbano de 4 manzanas con señales de tránsito.
  * Física de conducción básica (acelerar, frenar, doblar).
  * Sistema de detección de infracciones (chocar, pasarse en rojo).
  * Soporte para volante y pedales físicos.
* **Recursos:** 1 Desarrollador Unity y 1 Artista 3D. **Tiempo:** 14 semanas. **Presupuesto:** $7.000 USD (licencias + sueldos).

---

### 2. Resolución
A continuación se resuelven los 3 puntos (análisis del caso, reparto de 100 puntos de esfuerzo y priorización del 1 al 4) para cada una de las fichas. El criterio general es concentrar el esfuerzo en lo que define el éxito del cliente y ordenar las actividades según sus dependencias técnicas (lo que es base va primero; lo periférico o de mayor riesgo, al final).

#### Ficha A — Clínica privada (chatbot con IA)
**Análisis del caso**
El éxito del cliente radica en reducir un 40% las consultas administrativas. Los elementos clave son el motor conversacional y el agendamiento automatizado. El triaje y la validación biométrica son complementarios y de mayor riesgo técnico.

**Reparto de esfuerzo y priorización**

| Actividad | Puntos | Prioridad |
| :--- | :--- | :--- |
| Chatbot con LLM | 35 | 1 |
| Agendamiento por voz/texto | 30 | 2 |
| Triaje automático | 20 | 3 |
| Validación biométrica | 15 | 4 |
| **TOTAL** | **100** | **—** |

**Justificación de la prioridad**
* **Chatbot con LLM:** es la base sobre la que se apoya todo lo demás; sin el motor conversacional no existen ni el triaje ni el agendamiento. Además es lo que más aporta al objetivo de reducir consultas.
* **Agendamiento:** una vez que el bot entiende al usuario, reservar turnos por sí mismo es lo que produce la mayor caída de tareas administrativas. Requiere la integración crítica con la base de datos de la clínica.
* **Triaje automático:** extiende la conversación con valor agregado, pero es sensible (necesita disclaimers y prompts cuidados) y no es imprescindible para lograr el 40%.
* **Validación biométrica:** lo más complejo y de mayor riesgo legal/técnico, y lo menos ligado al objetivo. Se deja para el final y, si el tiempo aprieta, se entrega en su versión mínima (foto de DNI en lugar de reconocimiento facial).

#### Ficha B — Tienda online (recomendador de productos)
**Análisis del caso**
El objetivo principal es incrementar las ventas mediante personalización. La calidad del recomendador depende críticamente de la limpieza de datos históricos. El algoritmo y su integración en la Home son los motores del valor de negocio.

**Reparto de esfuerzo y priorización**

| Actividad | Puntos | Prioridad |
| :--- | :--- | :--- |
| Limpieza de base de datos histórica | 30 | 1 |
| Algoritmo de recomendación (ML) | 35 | 2 |
| Integración en la Home | 20 | 3 |
| Panel de métricas de ventas | 15 | 4 |
| **TOTAL** | **100** | **—** |

**Justificación de la prioridad**
* **Limpieza de datos:** va primero sí o sí. Ningún modelo funciona bien sobre datos sucios o desordenados; es la fundación de todo el proyecto (recibe mucho esfuerzo aunque no sea lo "vistoso").
* **Algoritmo de recomendación:** es el entregable central, el "cerebro" que genera las sugerencias. Recibe el mayor esfuerzo y depende de tener los datos ya limpios.
* **Integración en la Home:** despliega el algoritmo justo donde se traduce en ventas. Sin este paso el modelo no aporta valor real al negocio.
* **Panel de métricas:** se construye al final porque necesita el sistema ya funcionando y datos reales para medir si las ventas efectivamente subieron. Prueba el ROI, pero no genera ventas por sí mismo.

#### Ficha C — Academia de manejo (simulador 3D)
**Análisis del caso**
El éxito se mide en la efectividad del aprendizaje. Los pilares son una física de conducción realista y un sistema de detección de infracciones preciso. El escenario y el soporte de hardware son elementos de inmersión secundaria.

**Reparto de esfuerzo y priorización**

| Actividad | Puntos | Prioridad |
| :--- | :--- | :--- |
| Física de conducción básica | 30 | 1 |
| Escenario urbano con señales | 25 | 2 |
| Detección de infracciones | 25 | 3 |
| Soporte para volante y pedales | 20 | 4 |
| **TOTAL** | **100** | **—** |

**Justificación de la prioridad**
* **Física de conducción:** es la mecánica central; se construye primero porque es lo que hace que "manejar" se sienta creíble y útil para practicar. Recibe el mayor esfuerzo.
* **Escenario urbano:** es el mundo donde se prueba y ejercita la física, y donde viven las señales de tránsito. El artista 3D puede avanzarlo en paralelo mientras el desarrollador Unity trabaja la física.
* **Detección de infracciones:** aporta el valor pedagógico (aprender del error), pero depende de tener antes el escenario con señales y la física funcionando para poder detectar choques o cruces en rojo.
* **Soporte volante/pedales:** capa de hardware sobre una simulación que ya funciona. Va al final porque es lo más periférico y la integración de periféricos suele ser delicada; sin ella el simulador igualmente es usable.

---

# Dinámica Scrum — "La campaña del famoso"

## La situación
Un influencer con llegada directa a uno de sus inversores se ofreció a protagonizar una campaña de su proyecto. La oportunidad es ahora. El equipo tiene que organizarse rápido y entregar una campaña de marketing:
* Un afiche digital para la vía pública.
* Un video corto, reel o carrusel de imágenes para la pata de redes sociales de la campaña.
* Una presentación de 2-3 slides presentando la campaña a los inversores.

Usen IA generativa, Canva, o lo que tengan a mano.

### 1) Setup en Jira (10 min)
Todos se hacen usuario en Jira. Un integrante crea el proyecto (template Scrum), invita al resto del equipo y arrancan.

### 2) Backlog y Sprint Planning 1 (10 min)
Les acercamos un backlog propuesto. Agreguen lo que crean conveniente. Definan y asignen las tareas que formarán parte del Sprint 1.

**Épica — Estrategia creativa**
1. Definir el mensaje central de la campaña para que todas las piezas comuniquen lo mismo.
2. Definir el diseño del afiche para captar la atención del público.
3. Decidir el tono y estética visual de la campaña de redes para que sea coherente con la identidad del proyecto.
4. Definir la estrategia de comunicación a los inversores de la campaña.
5. Cualquier otra tarea que les surja.

**Épica — Producción de piezas**
6. Generar una imagen del afiche con IA para tener la pieza estática lista.
7. Definir el guión del video/carrusel (cuántas imágenes, qué dice cada una) para guiar la producción.
8. Generar las imágenes del carrusel con IA y ensamblarlas para tener la pieza animada lista.
9. Armar 2-3 slides presentando la campaña para obtener la aprobación de los inversores.
10. Cualquier otra tarea que les surja.

**Épica — Presentación de la campaña**
11. Pulir las piezas según haga falta.
12. Revisar la coherencia entre el afiche, el carrusel y los slides para que todo comunique lo mismo.
13. Cerrar el sprint en Jira y documentar el tablero final para dejar registro del proceso.
14. Cualquier otra tarea que les surja.

### Pasos 3, 4 y 5 — Sprint 1 / Sprint 2 / Sprint 3 (cada uno: 15 min trabajo + 3 min ceremonia)
Cada sprint sigue el mismo esquema:
* **Planning (1 min):** Cada uno confirma qué hace en este sprint.
* **Desarrollo (15 min):** Trabajen. Muevan las tarjetas en el tablero.
* **Review + Retro (2 min):** ¿Qué cerraron? ¿Qué ajustan para el próximo?

### Paso 6 — Cierre (2-3 equipos voluntarios, 4 min c/u)
Cada equipo muestra:
* Captura del tablero Jira al final.
* Los 2-3 slides de presentación a inversores (mostrando el afiche y reel producido).

---

## Solución

### Concepto de campaña
Definimos primero un proyecto concreto para que todas las piezas tengan sentido y sean coherentes.

| Elemento | Definición |
| :--- | :--- |
| **Proyecto / producto** | Órbita — app de inversiones para principiantes (fintech). |
| **Influencer** | Nico Vega, creador de contenido de finanzas y lifestyle (llegada a público joven). |
| **Público objetivo** | Jóvenes de 18 a 30 años, primerizos en inversión, con miedo o desconocimiento del tema. |
| **Mensaje central** | "Invertir ya no es cosa de expertos. Empezá con lo que tengas." |
| **Tono** | Cercano, optimista, desmitificador. Nada de tecnicismos ni solemnidad. |
| **Estética visual** | Colores vibrantes (violeta + verde menta), tipografía sans-serif redondeada, fondos limpios, ilustraciones flat y capturas de la app. |
| **Objetivo de negocio** | Sumar descargas y primeras inversiones + validar la campaña ante los inversores. |

### Paso 1 — Setup en Jira
* **Proyecto creado:** Campaña Órbita (clave CAMP), template Scrum.
* **Tablero:** columnas To Do → In Progress → In Review → Done.
* **Equipo e roles:**

| Integrante | Rol | Responsabilidad principal |
| :--- | :--- | :--- |
| Ana | Scrum Master / Product Owner | Prioriza backlog, facilita ceremonias, comunica con inversores. |
| Bruno | Diseño / IA generativa | Afiche e imágenes del carrusel. |
| Caro | Redes / contenido | Guión del carrusel, copies, coherencia de marca. |
| Diego | Presentación | Slides para inversores, cierre y documentación. |

### Paso 2 — Backlog y Sprint Planning
Al backlog propuesto le agregamos algunas tareas propias (marcadas con ➕). Estimamos con story points simples (escala 1-2-3-5) y distribuimos en 3 sprints.

| # | Tarea | Épica | Estimación | Responsable | Sprint |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Definir el mensaje central de la campaña | Estrategia creativa | 3 | Ana + todos | 1 |
| 2 | Definir el diseño del afiche | Estrategia creativa | 2 | Bruno | 1 |
| 3 | Decidir tono y estética visual de redes | Estrategia creativa | 2 | Caro | 1 |
| 4 | Definir estrategia de comunicación a inversores | Estrategia creativa | 2 | Diego | 1 |
| 5 | Definir paleta de colores y tipografía (guía de marca) ➕ | Estrategia creativa | 1 | Bruno + Caro | 1 |
| 6 | Generar imagen del afiche con IA | Producción de piezas | 3 | Bruno | 2 |
| 7 | Definir guión del carrusel (cantidad de imágenes y textos) | Producción de piezas | 2 | Caro | 2 |
| 8 | Generar imágenes del carrusel con IA y ensamblar | Producción de piezas | 5 | Bruno + Caro | 2 |
| 9 | Armar 2-3 slides de presentación | Producción de piezas | 3 | Diego | 2 |
| 11 | Pulir las piezas según haga falta | Presentación | 2 | Todos | 3 |
| 12 | Revisar coherencia entre afiche, carrusel y slides | Presentación | 2 | Ana | 3 |
| 13 | Cerrar el sprint en Jira y documentar el tablero final | Presentación | 1 | Diego | 3 |
| 14 | Preparar el discurso/pitch de 4 min para el cierre ➕ | Presentación | 2 | Ana + Diego | 3 |

### Paso 3 — Sprint 1: Estrategia creativa
* **Planning:** El equipo define las bases conceptuales. Sin esto, las piezas no pueden producirse.
* **Desarrollo — resultados del sprint:**
  * **Mensaje central (tarea 1):** "Invertir ya no es cosa de expertos. Empezá con lo que tengas." Todas las piezas deben reforzar esta idea de accesibilidad.
  * **Diseño del afiche (tarea 2):** foto de Nico Vega mirando a cámara sosteniendo el celular con la app abierta; fondo violeta; el mensaje central en grande; logo de Órbita abajo a la derecha.
  * **Tono y estética de redes (tarea 3):** cercano y conversacional, primera persona ("yo empecé así"), formato vertical para stories/reels, textos cortos.
  * **Estrategia hacia inversores (tarea 4):** mostrar la campaña como una palanca de crecimiento de descargas usando la credibilidad del influencer; foco en alcance esperado y bajo costo de producción (IA).
  * **Guía de marca (tarea 5):** violeta #6C4AB6 + verde menta #3DDC97, tipografía sans-serif redondeada, uso consistente del logo.
* **Review + Retro:**
  * **Cerramos:** las 5 tarjetas de la épica Estrategia creativa.
  * **Ajuste:** el mensaje quedó un poco largo para el afiche; en Sprint 2 usamos una versión corta ("Empezá con lo que tengas") como titular y la completa en el copy de redes.

### Paso 4 — Sprint 2: Producción de piezas
* **Planning:** Con la estrategia cerrada, se producen las tres piezas en paralelo.
* **Desarrollo — resultados del sprint:**
  * **Afiche digital (tarea 6)** Pieza vertical generada con IA:
    * Titular: "Empezá con lo que tengas."
    * Imagen: Nico Vega con el celular mostrando la app.
    * Bajada: "Invertí desde $1.000. Sin comisiones ocultas."
    * Logo Órbita + CTA "Descargá la app".
  * **Guión del carrusel (tarea 7) — 4 imágenes**

| Slide | Contenido visual | Texto |
| :--- | :--- | :--- |
| 1 | Nico mirando a cámara | "¿Cuánto pensás que necesitás para empezar a invertir?" |
| 2 | Ilustración de un café | "Menos de lo que gastás en un café por semana." |
| 3 | Captura de la app Órbita | "Yo empecé con $1.000. En serio." |
| 4 | Fondo violeta + logo | "Descargá Órbita. Tu primera inversión te espera. " |

  * **Producción del carrusel (tarea 8):** las 4 imágenes se generan con IA respetando la paleta y se ensamblan como carrusel/reel vertical con la música y los textos superpuestos.
  * **Slides para inversores (tarea 9) — 3 slides**
    * Portada: "Campaña Órbita × Nico Vega" + mensaje central.
    * La estrategia: público objetivo, tono, y las 3 piezas producidas (afiche + carrusel + presencia en redes).
    * Proyección y cierre: alcance estimado del influencer, costo bajo por producción con IA, y CTA de aprobación.
* **Review + Retro:**
  * **Cerramos:** afiche, guión, carrusel ensamblado y slides.
  * **Ajuste:** el color de una imagen del carrusel salió más azul que violeta; queda pendiente corregir la coherencia cromática en Sprint 3.

### Paso 5 — Sprint 3: Presentación de la campaña
* **Planning:** Sprint de pulido, control de coherencia y cierre.
* **Desarrollo — resultados del sprint:**
  * **Pulido de piezas (tarea 11):** se corrige el tono violeta del carrusel y se ajusta el interlineado del afiche.
  * **Revisión de coherencia (tarea 12):** se verifica que afiche, carrusel y slides usen el mismo mensaje, la misma paleta y el mismo logo. ✔️ Consistente.
  * **Cierre y documentación (tarea 13):** se pasan todas las tarjetas a Done y se toma captura del tablero final.
  * **Pitch de cierre (tarea 14):** discurso de 4 min preparado para presentar ante los inversores.
* **Review + Retro final:**
  * **Cerramos:** todo el backlog comprometido.
  * **Qué funcionó:** dividir por roles desde el Sprint 1 evitó cuellos de botella; usar IA aceleró muchísimo la producción.
  * **Qué mejoraríamos:** definir la guía de marca (colores exactos) antes de generar imágenes nos habría ahorrado el retrabajo del Sprint 3.

### Paso 6 — Cierre: tablero final
Estado del tablero de Jira al finalizar los 3 sprints (todo en Done):

| Columna | Tarjetas |
| :--- | :--- |
| To Do | (vacío) |
| In Progress | (vacío) |
| In Review | (vacío) |
| Done | Tareas 1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 12, 13, 14 |

**Entregables presentados:**
* Captura del tablero Jira con todas las tarjetas en Done.
* Afiche digital de la campaña.
* Carrusel/reel de 4 imágenes para redes.
* Presentación de 3 slides a los inversores (mostrando el afiche y el reel producidos).

*Nota: el proyecto "Órbita", el influencer "Nico Vega" y los datos son ficticios, creados a modo de ejemplo para resolver la dinámica. Se pueden reemplazar por el producto real de tu equipo.*

---

# Actividad — Negociación Ganar-Ganar (Hábito 4 de Covey)
**Taller de Gestión de Proyectos Digitales · Clase 13 · "Negociar para ganar… juntos"**

## Consigna
**Contexto: el divorcio de los Fullstack**
Dos personas se enamoraron en un hackathon. Cinco años después se divorcian. El problema no es el depto ni el auto: fundaron juntos una startup y ninguno se quiere ir.
* Ella reclama el repo, el gato Bytecode y el GitHub.
* Él quiere el código, el gato y la cafetera de US$900.
* Día 1: él cambia la contraseña del server. Día 2: ella le corta el Notion. La app se cae.
* El viernes vence una oferta para comprar la startup… pero solo si firman los dos.

**Parte A — Analizá el caso**
Respondé, usando el marco del Hábito 4:
1. ¿Qué paradigma juegan al cambiarse las contraseñas?
2. Posición vs. interés: ¿qué piden y qué quieren en realidad?
3. ¿Dónde está la "torta más grande" que no ven?
4. ¿"No hay trato"… o Ganar-Ganar antes del viernes?
5. ¿Cómo está su cuenta bancaria emocional?

**Parte B — Dinámica: negociá contra una IA**
Abrí Claude (u otra IA) y pegá el prompt que arranca la simulación.
La IA será tu contraparte difícil (cliente, dev o proveedor).
Negociá 6–8 turnos buscando Ganar-Ganar.
Al final, pedile que puntúe tu desempeño Win-Win.
Tip: si no hay buen acuerdo, "no hay trato" también es ganar.

*Prompt sugerido para iniciar la simulación con la IA:*
> Vas a hacer de contraparte difícil en una negociación.
> Sos una de las dos partes del "divorcio de los Fullstack":
> dos ex socios que fundaron una startup y ahora se divorcian.
> Hay una oferta para comprar la startup que vence el viernes,
> pero solo es válida si firman los dos.
> Elegí un rol (yo soy el otro socio) y defendé tus intereses
> con firmeza, sin ceder gratis. No me hagas fácil el acuerdo.
> Negociemos por turnos. Cuando yo diga "cerramos", puntuá mi
> desempeño Ganar-Ganar del 1 al 10 y decime qué hice bien y
> qué podría mejorar.

## Solución

### Parte A — Análisis del caso
**1) Paradigma al cambiarse las contraseñas** → Perder–Perder. Es la guerra de egos: nadie cede, cada uno saca de las ruedas al otro y la app se cae. Empezó como Ganar–Perder ("te dejo afuera del server") pero, al responder con la misma moneda (cortar el Notion), degeneró en Perder–Perder. Mientras se sabotean, destruyen el activo que ambos quieren vender.

**2) Posición vs. interés.**

| | Posición (lo que piden) | Interés (lo que quieren de verdad) |
| :--- | :--- | :--- |
| **Ella** | El repo, el GitHub, el gato | Que no la borren de lo que construyó, seguridad económica, cerrar el capítulo con dignidad |
| **Él** | El código, la cafetera de US$900, el gato | Reconocimiento de su trabajo, retorno económico, cerrar sin sentirse estafado |
| **Ambos** | "El gato es mío" | Vínculo afectivo con el gato (interés emocional, no económico) |

El error es pelear por objetos (una cafetera, un repo) cuando el interés común real es sacar el máximo valor de la venta y poder seguir con sus vidas.

**3) La "torta más grande" que no ven** → la venta de la startup. Están peleando por una cafetera de US$900 mientras hay sobre la mesa una oferta de compra que vale muchísimo más. Ganar-Ganar no es repartir la torta: es agrandarla. La torta grande = firmar la venta el viernes y repartir la plata. Al lado de eso, el gato y la cafetera son detalles que se resuelven aparte.

**4) ¿"No hay trato" o Ganar-Ganar antes del viernes?** → Ganar-Ganar. "No hay trato" es la opción liberadora solo cuando no existe un acuerdo bueno para ambos. Acá sí existe: firmar les conviene a los dos. Si dejan pasar el viernes, pierden los dos la oferta (eso sí sería Perder–Perder). Entonces: Ganar-Ganar antes del viernes. "No hay trato" se reservaría únicamente para un acuerdo malo, no para este.

**5) Cuenta bancaria emocional** → en rojo (saldo negativo). Vienen de puros retiros: sabotaje de contraseñas, cortar accesos, promesas rotas. Con saldo bajo, negociar es durísimo. Antes de sentarse a acordar necesitan depósitos: restaurar accesos como gesto de buena fe, escucharse, reconocer el aporte del otro, cumplir lo que prometan.

### Parte B — Estrategia y acuerdo Ganar-Ganar
**Jugadas del PM negociador aplicadas al caso:**
* **Separar persona del problema.** El problema no es "el ex", es "cómo cerramos la startup sin perder la oferta". Bajar la temperatura.
* **Escuchar el interés, no la posición.** Ninguno quiere realmente una cafetera: quieren plata, reconocimiento y cierre digno.
* **Estabilizar primero (depósito emocional).** Restaurar accesos mutuos y levantar la app, porque es el activo que están por vender. Sin app funcionando, la oferta se cae.
* **Agrandar la torta.** Correr el foco de los objetos a la venta: eso multiplica lo que hay para repartir.
* **Criterios objetivos para repartir.** Dividir según el equity / participación (o 50-50 si es parejo), no según quién grita más.
* **Poner el acuerdo por escrito y firmarlo antes del viernes.**
* **Cuidar la relación para el cierre:** sin rencor, cláusula de no difamación.

**Acuerdo Win-Win propuesto:**
* **Hoy:** ambos restauran accesos y vuelven a poner la app en línea (protege el activo que van a vender).
* **Viernes:** firman la oferta de compra. (Este es el verdadero "ganar" de los dos.)
* **Plata:** se reparte según participación en la sociedad (o 50-50).
* **El gato Bytecode:** queda con quien tenga vínculo más fuerte, con visitas / custodia compartida acordada; o se compensa al otro con un ítem equivalente. Es emocional, se resuelve fuera del dinero.
* **La cafetera de US$900:** se la queda él (es quien más la quiere); ella recibe un ítem o crédito de valor equivalente. Se trata como intercambio menor, no como batalla.
* **Cierre:** acuerdo escrito + compromiso de no sabotearse ni difamarse.

Resultado esperado: los dos salen con dinero de la venta, el activo se preserva, la dignidad queda intacta y la relación no termina incendiada. Eso es agrandar la torta en vez de repartir cenizas.

**Autoevaluación Win-Win (modelo de referencia)**
Al pedirle a la IA que puntúe, un buen desempeño Ganar-Ganar debería mostrar:
* **Puntaje alto (8–10):** priorizaste la venta sobre los objetos, escuchaste intereses, hiciste al menos un depósito emocional (restaurar accesos), propusiste criterios objetivos y cerraste por escrito antes del viernes.
* **Puntaje medio (5–7):** llegaste a un acuerdo pero cediendo de más (Perder–Ganar) o imponiendo (Ganar–Perder), o dejaste el gato/cafetera sin resolver.
* **Puntaje bajo (1–4):** te enganchaste en la guerra de egos, seguiste peleando por objetos y se venció la oferta del viernes (Perder–Perder).

Frase para cerrar (S. Covey): *"Buscá primero entender, después ser entendido."*

---

# Actividad en Clase: "Un Colaborador Digital"
**Objetivo:** Lograr una breve introducción a la inteligencia artificial y sus usos. Comprender los niveles de la Inteligencia Artificial, aprender a diseñar un asistente personalizado (Gema en IA Gemini) que actúe como tutor durante el cuatrimestre.

## Parte 1: Formas de conectarse con la IA
**Consigna:** La IA no es solo una "caja de chat". Vamos a identificar sus diferentes presentaciones.
**Instrucción a la IA:** *"Explícame de forma esquemática y breve qué diferencia hay entre usar una IA a través de: 1) Un Chat generalista, 2) Una Gema o asistente personalizado, 3) IA Nativa integrada en aplicaciones (como en Notion o Canva), 4) Agentes de IA, 5) Utilizar IA mediante APIs"*

### Resolución
Las cinco formas se pueden ordenar de la más simple y abierta a la más técnica y automatizada:
1. **Chat generalista (ChatGPT, Gemini, Claude en su versión de chat):** Es una conversación abierta con un modelo de propósito general. No tiene un rol fijo ni contexto propio: cada vez que abrís una conversación, "parte de cero". Ideal para consultas puntuales, exploración y tareas variadas.
2. **Gema o asistente personalizado (Gems de Gemini, GPTs personalizados):** Es el mismo modelo de base, pero pre-configurado con un rol, instrucciones fijas y, opcionalmente, archivos de referencia estables. Mantiene una "personalidad" y un contexto que se repiten en todas las conversaciones. Ideal para una tarea recurrente y bien definida (por ejemplo, un tutor de una materia).
3. **IA nativa integrada en aplicaciones (Notion AI, Canva, etc.):** La IA vive dentro de una herramienta que ya usás y opera sobre el contenido de esa herramienta (tu documento, tu diseño, tu base de datos). No cambiás de entorno: la IA es una función más de la app. Ideal para asistencia contextual dentro de un flujo de trabajo concreto.
4. **Agentes de IA:** Un sistema que no solo responde, sino que ejecuta tareas de varios pasos de forma autónoma: planifica, usa herramientas, busca información, navega, escribe archivos, etc., con mínima intervención humana. Ideal para automatizar procesos complejos de principio a fin.
5. **IA mediante APIs:** Es el acceso programático al modelo: en lugar de una interfaz visual, se conecta el modelo a un software propio mediante código. Permite integrar la IA dentro de aplicaciones a medida y a gran escala. Ideal para desarrollo y automatización personalizada.

En síntesis, la progresión va de conversación abierta → asistente configurado → función embebida en una app → sistema autónomo → integración por código.

**Preguntas de profundización**
* **¿Cuál es la diferencia entre utilizar el chat principal y utilizar una gema? ¿Y cuándo se recomendaría usar cada uno?**
  El chat principal es de propósito general y no conserva instrucciones ni contexto entre conversaciones: es un lienzo en blanco cada vez. La gema, en cambio, arranca ya "cargada" con un rol, instrucciones y material de referencia fijos.
  Usá el chat principal para consultas puntuales, variadas o exploratorias, donde no necesitás repetir siempre el mismo contexto.
  Usá una gema cuando repetís la misma tarea con las mismas reglas (por ejemplo, un tutor de la materia): te ahorra tener que explicar el contexto una y otra vez y mantiene un comportamiento consistente.
* **¿Cuándo tiene sentido subir un archivo directamente mediante el chat y cuándo hacerlo mediante el repositorio estable de la gema o asistente?**
  Directo al chat: cuando el archivo es de uso único o puntual para esa consulta específica (revisar un PDF una sola vez, resumir un texto suelto). Una vez cerrada la conversación, deja de estar disponible.
  Repositorio de la gema: cuando el archivo es una referencia permanente que querés que la IA tenga siempre presente (el programa de la materia, el cronograma, un apunte base). Se carga una vez y queda disponible en todas las conversaciones con esa gema, sin volver a subirlo.
* **¿En qué situaciones se recomienda mantener la conversación siempre sobre un mismo hilo de chat y cuándo sería recomendable abrir nuevas conversaciones?**
  Mismo hilo: cuando las preguntas forman parte de un mismo tema o proyecto y necesitás que la IA recuerde lo dicho antes (ir refinando un trabajo, corregir en varias pasadas, sostener un contexto acumulado).
  Nueva conversación: cuando cambiás de tema por completo. Los hilos muy largos o con temas mezclados hacen que la IA se "distraiga" con contexto irrelevante y pierda calidad. Empezar de nuevo mantiene las respuestas más enfocadas.
* **De manera sintética, ¿qué conceptos debería tener en claro para poder sacar buen provecho en el uso de una IA?**
  * **Contexto:** la IA solo sabe lo que le das; cuanto mejor le explicás la situación, mejor responde.
  * **Prompt claro:** pedidos específicos, con rol, objetivo, formato y ejemplos, rinden mucho más que preguntas vagas.
  * **Iteración:** rara vez la primera respuesta es la definitiva; conviene corregir y repreguntar.
  * **Ventana de contexto / memoria:** la IA "olvida" fuera del hilo actual (salvo memoria o repositorio configurados).
  * **Verificación:** puede equivocarse o inventar datos ("alucinar"); hay que contrastar lo importante.
  * **Herramienta elegida:** elegir la forma adecuada (chat, gema, integración, agente, API) según la tarea.

## Parte 2: Un asistente personalizado
**Consigna:** Ahora vas a utilizar la IA para que ella misma te enseñe a configurarla como un tutor experto.
**El Prompt Maestro:** *"Quiero crear una Gema (o equivalente) que me sirva como tutor para la materia 'Taller de Gestión de Proyectos Digitales'. Enséñame a crear una gema bien hecha. ¿Qué aspectos debería tener en cuenta? Dame ejemplos de cómo podría llenar los campos de 'Instrucciones' y 'Rol' para que sea realmente útil. Hazme las preguntas que creas convenientes si lo necesitas."*

### Resolución
**Aspectos a tener en cuenta para una gema bien hecha:**
* **Rol definido:** dejar claro quién es la IA (un tutor experto en gestión de proyectos digitales) y para quién trabaja (un estudiante del cuatrimestre).
* **Objetivo claro:** qué debe lograr (ayudarte a comprender los temas, no darte todo resuelto).
* **Tono y estilo:** cercano, claro, con lenguaje accesible y ejemplos concretos.
* **Método pedagógico:** que explique paso a paso, que haga preguntas para verificar que entendiste, que proponga ejemplos y analogías.
* **Límites:** qué NO hacer (no resolver los trabajos por vos, no inventar datos, avisar cuando no está seguro).
* **Material de referencia:** subir el programa y el cronograma al repositorio para que responda alineado a la materia real

**Preguntas que la IA podría hacerte (y que conviene tener respondidas):**
* ¿Qué nivel de conocimiento previo tenés sobre el tema?
* ¿Preferís explicaciones breves o desarrolladas?
* ¿Querés que te haga preguntas de repaso o solo que responda?
* ¿Tenés el programa y el cronograma para cargar como referencia?

**Ejemplo de campo "Rol":**
Sos un tutor experto en Gestión de Proyectos Digitales, con experiencia en metodologías ágiles y tradicionales, planificación, roles de equipo y herramientas digitales. Acompañás a un estudiante universitario durante todo el cuatrimestre de la materia "Taller de Gestión de Proyectos Digitales".

**Ejemplo de campo "Instrucciones":**
* Tu objetivo es ayudarme a comprender los temas de la materia, no resolver mis trabajos por mí.
* Explicá con lenguaje claro, ejemplos concretos y analogías simples.
* Cuando te pregunte algo, verificá primero mi nivel de comprensión y ajustá la explicación.
* Después de explicar un tema, hacéme una o dos preguntas de repaso para asegurar que lo entendí.
* Guiáte siempre por el programa y el cronograma que cargué en el repositorio.
* Si no estás seguro de un dato o no figura en el material, decilo con honestidad en lugar de inventarlo.
* Mantené un tono cercano, paciente y motivador.

**Tarea de configuración (pasos realizados):**
1. Leer los consejos que dio la IA.
2. Entrar a la sección "Crear Gema".
3. Completar los campos "Rol" e "Instrucciones" con los ejemplos anteriores.
4. Subir el Programa de la Materia y el Cronograma al repositorio de la Gema (si están a mano).

## Parte 3: Cierre — El "Test de Estrés"
**Consigna:** Para verificar a tu asistente personalizado, hacé esta prueba:
* En un Chat común preguntá: "¿Qué temas vamos a ver en esta materia?"
* Luego, preguntá lo mismo pero esta vez en tu gema o asistente personalizado.

### Resolución
**Resultado esperado:**
* **En el chat común**, al no tener contexto de la materia, la IA responde con una respuesta genérica: enumera temas típicos que suele incluir una materia de gestión de proyectos digitales (planificación, metodologías ágiles, roles, herramientas, etc.), pero aclarando que no conoce el programa específico. Puede acertar en parte por sentido común, pero no representa la materia real.
* **En la gema con el programa cargado**, la IA responde con los temas concretos de esta materia, tomados del programa y el cronograma subidos al repositorio. La respuesta es precisa, ordenada según las unidades del cuatrimestre y adaptada al curso real.

**Conclusión:** la diferencia demuestra el valor del contexto persistente. La misma tecnología de base pasa de una respuesta genérica a una respuesta útil y específica solo por haberla configurado y darle material de referencia estable.

## Parte 4: Entregable
**Consigna:** Como persona que decidió emprender el desafío de estudiar, compartí 3 o 4 observaciones (ideas, consideraciones, reflexiones, desafíos, etc.) sobre el impacto que la IA tendrá en tu forma de aprender.

### Resolución
* **De receptor pasivo a diseñador de mi aprendizaje.** La IA me permite configurar herramientas a medida (como una gema tutora) en lugar de solo consumir contenido. Aprender ahora incluye también aprender a construir mis propios asistentes, lo que cambia mi rol de estudiante que recibe a estudiante que diseña cómo estudia.
* **El desafío de no delegar el pensamiento.** La misma facilidad que ofrece la IA para resolver tareas puede volverse una trampa: si le pido que haga todo por mí, dejo de ejercitar el razonamiento. El reto real es usarla para comprender mejor (explicaciones, ejemplos, repaso) y no para saltear el proceso de aprender.
* **La verificación como nueva habilidad clave.** Como la IA puede equivocarse o inventar datos, ya no alcanza con leer la respuesta: parte de estudiar es aprender a contrastar, dudar y confirmar la información. El pensamiento crítico se vuelve más importante, no menos.
* **Aprendizaje personalizado y disponible siempre.** Tener un tutor configurado con el programa de la materia, que responde a mi ritmo y a cualquier hora, baja mucho la barrera para consultar dudas. Esto puede hacer el estudio más constante y menos frustrante, siempre que lo use como apoyo y no como reemplazo del esfuerzo propio.

---

# Actividad: "Un acta de Constitución preliminar"

## Consigna
**Objetivo:** Ubicarse en los zapatos de los emprendedores de Tienda Nube / Ualá y transformar los insights de las entrevistas en una estructura de proyecto real, identificando quiénes están interesados (Mapa Político) y qué debemos lograr (Ciclo de Vida).

### 1. Bloque Mapa Político y Roles
Antes de planificar tareas, se debe entender el Entorno.
* Basándose en la empresa que les tocó (Ualá o Tienda Nube), en lo visto en clase y en la entrevista, armen una matriz de Poder/Interés ubicando a los diversos stakeholders que identifiquen en su proyecto.
* Definan las acciones y estrategias particulares que utilizarán para abordar la comunicación con los actores de cada uno de los cuadrantes.
* Identifiquen en particular algún "Saboteador Potencial" (mucho poder y poco interés en que el proyecto avance) y también algún "Promotor" (actor que deberían mantener de su lado dado su poder y su interés), y comenten si utilizarían alguna estrategia en particular con esa persona.

### 2. Bloque Ciclo de Vida y Metas
* Enuncien de manera SMART los objetivos que rescataron de la entrevista.
* Incluyan un primer listado y organización de las Metas intermedias con las tareas que identifican como necesarias.
* Definan al menos 3 Hitos (Milestones) críticos que marquen el paso de una fase a otra (ej.: de Diseño de Producto a Lanzamiento MVP).
* ¿Consideran a priori que su proyecto será Predictivo (cascada), Adaptativo (ágil) o un híbrido entre estos modelos?

### 3. Entregable
Redactar todo lo producido en los puntos 1 y 2 como un acta de constitución preliminar del proyecto: quiénes están involucrados, qué se busca lograr, y qué y cómo se hará para lograrlo.

---

## Resolución
**Empresa seleccionada:** Tienda Nube (Nuvemshop). **Fase del proyecto analizada:** etapa temprana, desde el Diseño de Producto hasta el Lanzamiento del MVP de la plataforma SaaS de e-commerce (proyecto que nació como práctica universitaria en el ITBA y derivó en la empresa fundada en 2011 por Santiago Sosa, Martín Palombo, Alejandro Vázquez, Alejandro Alfonso y José Abuchaem).
*Nota: si el caso asignado fuese Ualá, la estructura es la misma; solo hay que reemplazar los stakeholders (BCRA como regulador clave, redes de tarjetas, bancos, comercios adheridos) y los objetivos por los rescatados de esa entrevista.*

### 1. Mapa Político y Roles

**Matriz Poder / Interés (Mendelow)**

| | Poco Interés | Mucho Interés |
| :--- | :--- | :--- |
| **Mucho Poder** | **Mantener satisfechos**<br>• Reguladores (AFIP, BCRA / normativa de medios de pago, Defensa del Consumidor)<br>• Grandes proveedores de pasarela de pago y bancos<br>• Plataforma/marketplace dominante del sector (competidor con poder de mercado) | **Gestionar de cerca (actores clave)**<br>• Socios fundadores (CEO, CPO, CCO)<br>• Inversor/VC líder de la ronda<br>• Aceleradora que respalda el proyecto |
| **Poco Poder** | **Monitorear (mínimo esfuerzo)**<br>• Público general<br>• Medios de comunicación (interés bajo al inicio)<br>• Competidores pequeños | **Mantener informados**<br>• Comerciantes/emprendedores usuarios (clientes)<br>• Equipo de desarrollo y primeros empleados<br>• Comunidad de desarrolladores del ecosistema de apps |

**Estrategias de comunicación por cuadrante**
* **Gestionar de cerca (alto poder / alto interés):** son los dueños de las decisiones. Involucrarlos en la definición del alcance y las prioridades. Comunicación frecuente y de alta calidad: reuniones semanales de avance, tableros compartidos y reportes de métricas clave. Buscar consenso antes de decisiones críticas.
* **Mantener satisfechos (alto poder / bajo interés):** no abrumarlos con detalle, pero no descuidarlos, porque pueden frenar el proyecto. Comunicación formal y puntual: cumplimiento normativo, contratos claros con proveedores de pago, y contacto proactivo ante cambios que los afecten. El objetivo es evitar sorpresas y convertir su indiferencia en apoyo (o al menos en neutralidad).
* **Mantener informados (bajo poder / alto interés):** son la base de usuarios y el equipo; su feedback es oro. Canales abiertos y accesibles: newsletters, centro de ayuda, comunidad, encuestas y entrevistas de usuario. Escuchar y mostrar que sus aportes impactan en el producto.
* **Monitorear (bajo poder / bajo interés):** esfuerzo mínimo. Seguimiento pasivo de medios y del mercado, comunicación general (redes, blog) sin dedicarles recursos específicos, atentos a que alguno "escale" de cuadrante.

**Saboteador Potencial (mucho poder / poco interés)**
Gran proveedor de pasarela de pagos / plataforma dominante del sector. Controla una dependencia crítica (el cobro online) pero no tiene incentivo en que un competidor pequeño despegue; puede demorar la integración, cambiar condiciones o priorizar a otros.
*Estrategia:* no depender de un único proveedor. Diseñar la integración de pagos de forma modular para poder sumar alternativas, negociar acuerdos por escrito con hitos claros, y a mediano plazo desarrollar una solución de pagos propia para reducir la dependencia. En paralelo, mostrarle el valor del volumen de transacciones que aporta la plataforma para alinear intereses (convertir al saboteador en aliado).

**Promotor (alto poder / alto interés)**
Inversor/VC líder (o la aceleradora que respalda el proyecto). Aporta capital, red de contactos y reputación, y gana si el proyecto crece.
*Estrategia:* mantenerlo cerca y bien informado con reportes periódicos de métricas y aprendizajes (buenos y malos), transparencia total y aprovechamiento de su red para conseguir talento, clientes y próximas rondas. Es un aliado a cultivar activamente, no solo a rendirle cuentas.

### 2. Ciclo de Vida y Metas

**Objetivos SMART**
Ajustar los números a lo que efectivamente se dijo en la entrevista; a continuación, formulación de ejemplo coherente con el caso.
* **O1 (Producto):** Lanzar un MVP funcional de la plataforma SaaS que permita a un comerciante crear y publicar una tienda online operativa en menos de 30 minutos, en un plazo de 6 meses desde el inicio del proyecto.
* **O2 (Validación de mercado):** Alcanzar 50 comercios activos usando la plataforma dentro de los 3 meses posteriores al lanzamiento del MVP, como prueba de que existe demanda real.
* **O3 (Modelo de negocio):** Validar la conversión a plan pago logrando que al menos el 20 % de los comercios activos abone una suscripción antes del cierre del primer año.
*(SMART: cada uno es eSpecífico, Medible, Alcanzable, Relevante y acotado en el Tiempo.)*

**Metas intermedias y tareas**
* **Descubrimiento y validación del problema**
  * Entrevistar comerciantes/emprendedores para relevar dolores.
  * Analizar la competencia y definir la propuesta de valor.
* **Diseño del producto**
  * Definir el alcance funcional mínimo (MVP).
  * Diseñar la experiencia de usuario (wireframes y prototipos).
* **Desarrollo del MVP**
  * Construir el motor de creación de tiendas.
  * Integrar una pasarela de pagos y medios de envío básicos.
* **Lanzamiento y adquisición**
  * Programa beta con un grupo inicial de comercios.
  * Puesta en producción, marketing de lanzamiento y soporte.
* **Medición y financiamiento**
  * Definir e instrumentar métricas clave (activación, retención, conversión).
  * Preparar el pitch y cerrar la ronda de inversión inicial.

**Hitos (Milestones) críticos**
* **Cierre del Diseño de Producto:** alcance del MVP validado y prototipo aprobado → habilita el desarrollo.
* **Lanzamiento del MVP (beta):** primera versión operativa en manos de comercios reales → pasa de construcción a validación de mercado.
* **Integración de pagos operativa + primeros comercios pagos:** flujo de cobro funcionando y primeras suscripciones → valida el modelo de negocio.
* **Cierre de la ronda de inversión inicial:** capital asegurado → habilita la fase de escalamiento.

**Enfoque: Predictivo, Adaptativo o Híbrido**
Híbrido, con predominio adaptativo (ágil).
* **Componente adaptativo/ágil:** el desarrollo del producto y la validación con usuarios exigen iterar rápido sobre feedback e incertidumbre alta. Se trabaja por sprints, con MVP y mejora continua.
* **Componente predictivo/cascada:** las piezas con requisitos rígidos y externos —cumplimiento normativo, contratos con bancos y pasarelas, integraciones de pago— conviene planificarlas de forma secuencial y anticipada, porque los cambios son costosos y dependen de terceros.
La combinación permite ser flexible donde el mercado lo exige y ordenado donde el riesgo regulatorio y financiero lo requiere.

### 3. Acta de Constitución preliminar (síntesis)
* **Proyecto:** Diseño y lanzamiento del MVP de la plataforma SaaS de e-commerce (Tienda Nube).
* **Quiénes están involucrados:** socios fundadores (roles de CEO/CPO/CCO) como responsables del proyecto; inversor/VC y aceleradora como promotores; comerciantes usuarios y equipo de desarrollo como principales interesados; reguladores y proveedores de pago como actores de alto poder a mantener satisfechos.
* **Qué se busca lograr:** validar que existe demanda de una herramienta simple para que cualquier emprendedor abra su tienda online, lanzando un MVP en 6 meses, alcanzando 50 comercios activos a los 3 meses del lanzamiento y un 20 % de conversión a plan pago en el primer año.
* **Qué y cómo se hará:** avanzar por fases (descubrimiento → diseño → desarrollo → lanzamiento → medición/financiamiento), atravesadas por hitos que marcan el paso de una fase a otra, con un enfoque híbrido (ágil para el producto, predictivo para pagos y regulación) y un plan de comunicación diferenciado según el cuadrante de cada stakeholder.

---

# Actividad: Negociación Ganar-Ganar contra una IA
Vas a practicar una negociación real contra una IA que hará de tu contraparte difícil. Tu meta: lograr un acuerdo Ganar-Ganar (o un honesto "No hay trato").

## Cómo jugar (10 minutos)
1. Abrí Claude (o tu IA preferida).
2. Copiá y pegá el prompt de abajo. Elegí tu personaje: A, B o C.
3. Negociá durante 6 a 8 turnos. Escuchá el interés del otro antes de proponer.
4. Pedí el feedback final y anotá tu puntaje.
5. Compartí con el grupo: ¿lograste Ganar-Ganar? ¿qué te costó?

**Prompt para copiar y pegar**
> Vas a ser mi contraparte en una negociación de un proyecto de tecnología. Yo soy el/la Project Manager.
> Tu personaje (elijo A, B o C):
> A) Lucía, clienta exigente: querés 3 funcionalidades nuevas para la demo del viernes, sin mover la fecha ni el presupuesto.
> B) Beto, dev senior del equipo: decís que el plazo es imposible y estás a punto de pedir licencia.
> C) MegaSoft, proveedor: subiste el precio de las licencias un 40% a último momento.
> Reglas del juego:
> Mantenete SIEMPRE en personaje. Tenés intereses reales y dos límites ocultos: un punto en el que SÍ podés ceder y otro en el que NO.
> No aceptes mi primera propuesta. Negociá con firmeza, pero no seas imposible: si entiendo tu interés y propongo algo creativo, aflojá.
> Respondé en turnos cortos, como una conversación real.
> Después de 6 a 8 intercambios, cortá y dame un FEEDBACK así:
> - ¿Entendí tu interés antes de proponer? (1-10)
> - ¿Busqué agrandar la torta o me quedé en el regateo? (1-10)
> - ¿Cuidé la relación? (1-10)
> - Resultado: Ganar-Ganar / Ganar-Perder / Perder-Ganar / No hay trato
> - Un consejo concreto para mejorar.
> Empezá vos: presentá el conflicto en tu primer mensaje y esperá mi respuesta. 
> ¡Arranquemos!

**¿Cómo se ve un buen Ganar-Ganar?**
* Preguntaste por qué el otro pedía eso (su interés), no solo qué pedía (su posición).
* Propusiste opciones creativas que agrandan la torta (ej: mover features al sprint 2, sumar un recurso, ajustar el alcance del MVP).
* Cerraste un acuerdo claro y cuidaste la relación para la próxima.
* Si no había acuerdo bueno para ambos, dijiste "no hay trato" sin pelear.

*"Buscá primero entender, después ser entendido." — S. Covey*

## Solución (ejemplo resuelto)
**Personaje elegido: A) Lucía, clienta exigente.**
A continuación, una partida completa de referencia. Las líneas de Lucía son la IA en personaje; las de PM son las respuestas del Project Manager (vos).

* **Turno 1 — Lucía (abre el conflicto)**
  Hola, necesito hablarte del viernes. Para la demo tienen que estar sí o sí las tres funcionalidades que pedí: el login con Google, el dashboard de métricas y la exportación a Excel. Y ojo, no muevo la fecha ni te sumo un peso al presupuesto. Ya me comprometí con esto puertas adentro. ¿Cómo venimos?
* **Turno 2 — PM (indaga el interés, no ataca la posición)**
  Gracias por la claridad, Lucía. Antes de decirte qué se puede y qué no, quiero entender bien el viernes: ¿ante quién es la demo y qué necesitás que esa gente se lleve puesto? ¿El objetivo es que vean el producto funcionando de punta a punta, o que se convenzan de que el proyecto avanza y vale la pena seguir bancándolo?
* **Turno 3 — Lucía (revela el interés real)**
  Es ante el comité de dirección. De esa reunión depende que aprueben el presupuesto del próximo trimestre. No necesito que todo ande perfecto: necesito que se vea sólido y que no quede la sensación de que estamos flojos. Si el comité ve algo a medias, me comen viva.
* **Turno 4 — PM (agranda la torta con una opción creativa)**
  Perfecto, eso cambia todo. Si el objetivo es que el comité vea algo sólido y apruebe el presupuesto, no hace falta que las tres estén 100% productivas el viernes. Te propongo esto: dejamos el dashboard de métricas terminado y funcionando de verdad, que es lo más vistoso y lo que más impacta en una demo. El login con Google y la exportación a Excel los mostramos como prototipos navegables, con datos de ejemplo, y los dejamos comprometidos para el sprint siguiente con fecha concreta. Así el comité ve algo real, ve el roadmap claro, y no arriesgamos que se rompa algo en vivo. Fecha del viernes intacta, presupuesto intacto.
* **Turno 5 — Lucía (negocia con firmeza, no afloja del todo)**
  El dashboard funcionando me gusta. Pero "prototipo navegable" me suena a humo, y si el comité pregunta "¿esto anda?" y le digo que no, quedo mal. El login por lo menos lo necesito funcionando, es lo primero que van a querer tocar.
* **Turno 6 — PM (cede en lo cedible, cuida el límite del otro)**
  Te escucho, y tenés razón con el login: es lo primero que tocan. Hagamos así: dashboard funcionando + login con Google funcionando. Son las dos que garantizan que "anda". La exportación a Excel la mostramos como preview real (un botón que genera un archivo de ejemplo ya armado), y vos podés decir con total honestidad "la exportación llega en dos semanas, acá está cómo se va a ver". Nada de humo: es un compromiso con fecha. Para llegar a esas dos bien probadas sin reventar al equipo, corro la exportación completa al sprint 2. ¿Te cierra?
* **Turno 7 — Lucía (acepta)**
  Sí, así sí. Dashboard y login funcionando, exportación como preview con fecha comprometida. Con eso el comité queda tranquilo y yo también. Cerrámelo por escrito así lo tengo para la reunión.
* **Turno 8 — Feedback final (de la IA)**
  **FEEDBACK**
  * **¿Entendí tu interés antes de proponer? 9/10** — Preguntaste ante quién era la demo y qué necesitaba llevarse el comité antes de tirar cualquier solución. Eso destrabó todo.
  * **¿Busqué agrandar la torta o me quedé en el regateo? 9/10** — En vez de pelear "3 features sí / 3 features no", separaste "qué anda" de "qué se muestra" y sumaste el roadmap del sprint 2 como valor. Eso es agrandar la torta.
  * **¿Cuidé la relación? 9/10** — Reconociste el punto del login cuando tenía razón y le diste a Lucía argumentos honestos para defenderse frente al comité. Quedó como socio, no como obstáculo.
  * **Resultado:** Ganar-Ganar
  * **Consejo concreto:** La próxima, cerrá siempre con un mini-resumen escrito del acuerdo (qué entra, qué se pospone, con qué fecha) dentro de la misma conversación. Ya lo insinuaste al final; hacelo explícito como paso de cierre para que no queden interpretaciones distintas.

**Por qué este acuerdo es Ganar-Ganar**
* **Interés vs. posición:** La posición de Lucía era "3 features el viernes". Su interés real era "que el comité apruebe el presupuesto y no quedar mal". Al descubrir el interés, aparecieron soluciones que la posición cerrada escondía.
* **Se agrandó la torta:** No se repartió un pastel fijo (3 features). Se redefinió el problema (qué necesita anda de verdad vs. qué necesita mostrarse) y se sumó valor nuevo: un roadmap con fecha para el sprint 2.
* **Se respetaron los límites de ambos:** Lucía no movió fecha ni presupuesto (sus líneas rojas). El PM no reventó al equipo entregando tres features a medias (su calidad y su gente).
* **Se cuidó la relación:** El PM cedió en el login cuando el argumento del otro era válido, y le dio a Lucía munición honesta para su reunión. Eso construye confianza para la próxima negociación.

**Alternativa honesta: "No hay trato"**
Si Lucía se hubiera plantado en "las tres funcionando o nada", el PM debería haber dicho, sin pelear: "Con las tres al 100% para el viernes, sin mover fecha ni presupuesto, no puedo comprometerme sin arriesgar la calidad de la demo y quemar al equipo. Prefiero decirte que no ahora, a fallarte el viernes en vivo." Un buen "no hay trato" también es un buen resultado.
