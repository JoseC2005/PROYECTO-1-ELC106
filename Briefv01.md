
### BRIEF V0.1 - PROYECTO PROPIO

**Nombre del Proyecto:** STAFF BAR (Sistema de Gestión para Barras Móviles)

---

#### PROBLEMA
**¿Qué dificultad queremos comprender?**

Los bartenders en eventos de *open bar* (tragos ilimitados) pierden eficiencia y se estresan en la hora pico. Reciben órdenes a gritos entre el ruido ambiental, olvidan quién pidió qué, y los invitados se aglomeran preguntando los ingredientes de los cócteles. Esto genera cuellos de botella, desperdicio del tiempo limitado del evento y mala experiencia para el invitado.

---

#### CONTEXTO
**¿Dónde y cuándo ocurre?**

Ocurre en dos momentos clave:

1. **Pre-evento:** El administrador/dueño arma los paquetes y presupuestos desde su oficina o celular.
2. **Durante el evento:** En salones de fiestas o corporativos, con música alta, iluminación tenue, y los bartenders con las manos mojadas/ocupadas atendiendo a 50+ personas ansiosas por su trago.

---

#### IDEA INICIAL
**¿Qué solución imaginamos por ahora?**

Una **suite digital 3 en 1** basada en PWA (Progressive Web App) para evitar descargas forzadas en los operadores:

- **Kiosco Digital (Tablet):** En la barra, los invitados ven un menú con fotos grandes, ingredientes y piden su trago con 1 toque.
- **App del Bartender (Celular PWA):** Recibe los pedidos en tiempo real como una cola (FIFO). Vibra al llegar una nueva orden. Tiene un botón gigante "✅ LISTO" para marcar entregado sin soltar la botella.
- **Panel Admin (Web):** El dueño gestiona el catálogo de tragos, arma paquetes y activa qué menú estará disponible para el evento de hoy.
- *(Además, una web estática para que los clientes corporativos vean los paquetes sin necesidad de descargar nada).*

---

#### USUARIO
**¿Quién vive esa dificultad?**

- **Usuario Principal (App Móvil):** El bartender (20-40 años). Está de pie, con ritmo acelerado, manos mojadas y necesita interacciones de 1 toque o por voz.
- **Usuario Secundario 1 (Panel Admin):** El dueño del negocio (35-50 años). Necesita actualizar precios y disponibilidad desde cualquier lado.
- **Usuario Secundario 2 (Kiosco):** El invitado al evento (25-55 años). Quiere pedir rápido y volver a su mesa sin hacer fila larga.

---

#### TAREA
**¿Qué intenta hacer el usuario?**

- **Bartender:** Visualizar la cola de pedidos activos y marcarlos como "Entregados" con un solo toque o deslizamiento, recibiendo alertas hápticas (vibración) para no tener que mirar el celular constantemente.
- **Invitado (Kiosco):** Encontrar visualmente su trago favorito en una cuadrícula de imágenes, ver sus ingredientes y presionar "¡Pedir!" para que el bartender lo preparen al instante.
- **Admin:** Crear/modificar tragos y asignar rápidamente un set de tragos específicos para el evento del día.

---

#### ALCANCE (MVP)
**¿Qué parte pequeña abordaremos primero?**

Construiremos el **ciclo completo en tiempo real**:

1. **Panel Admin:** ABM (Altas, Bajas, Modificaciones) de tragos (nombre, foto, ingredientes, categoría) y creación de un "Evento Activo" (seleccionar checkboxes para activar/desactivar qué tragos estarán disponibles en el kiosco).
2. **Kiosco (Tablet):** Visualización del menú del evento activo con botones de filtro (Ron, Vodka, etc.) y envío de la orden a la base de datos.
3. **App Bartender (PWA móvil):** Recepción en tiempo real de la cola de pedidos, con botón "Completado" que elimina la orden de la cola.

---

#### 🧪 HIPÓTESIS DEL PROYECTO

> *"Si digitalizamos la cola de pedidos en una app que vibra al recibir nuevas órdenes y muestra botones táctiles gigantes (mínimo 60px), el tiempo de espera del invitado en la barra se reducirá al menos un 40% y el bartender podrá atender el doble de personas en hora pico sin aumentar su estrés percibido."*

---

#### 🧠 MODALIDAD DE IMPLEMENTACIÓN

| Versión | Tecnologías | Interacción |
| :--- | :--- | :--- |
| **🔵 CON IA** | Gemini Flash API (sugerencias de stock), Web Speech API (comandos de voz para el bartender) | El bartender dice *"Orden 12 lista"* y la app la marca sin tocarla. La IA predice si un trago se va a acabar y avisa al admin. |
| **🟠 SIN IA** | Firebase Firestore (tiempo real), JavaScript Vanilla, HTML/CSS | El bartender solo toca el botón verde "✅ Listo". El admin usa formularios estáticos. El kiosco filtra por categorías con botones duros. |

---

#### 📝 REGISTRO DE USO DE IA (CLASE 1)

> *"Utilicé DeepSeek para estructurar el flujo de trabajo de los 3 actores (Admin, Kiosco, Bartender) y para definir la hipótesis centrada en la reducción del tiempo de espera y la fatiga cognitiva. También usé Copilot para investigar cómo implementar la sincronización en tiempo real con Firebase (onSnapshot) y el manejo del API de vibración (navigator.vibrate) en dispositivos móviles para notificar al bartender sin necesidad de que mire la pantalla."*

---

**📌 Estado actual:** Listo para revisión y corrección en clase.
