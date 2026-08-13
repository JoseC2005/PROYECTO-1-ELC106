# PROYECTO-1-ELC106
INTEGRANTES:
  JOSE CARLOS JUSTINIANO MONTAÑO,
  ROYER CARRASCO ROMERO.

# 🍸 STAFF BAR - Sistema de Gestión para Barras Móviles

**Brief v0.1 - Proyecto de Interacción Humano-Computador (IHC)**

---

## 📌 Descripción del Proyecto
Sistema integral para empresas de coctelería a domicilio (open bar). 
Separa la experiencia del **cliente que cotiza** (Web) de la **herramienta operativa** (PWA/App) para bartenders y administradores.

---

## 🔍 Contexto y Problema
**¿Qué dificultad queremos comprender?**
Los bartenders en eventos con alta demanda (horas pico) pierden eficiencia porque reciben órdenes a gritos, olvidan quién pidió qué, y los invitados se aglomeran preguntando por los ingredientes o el estado de su trago.

**¿Dónde y cuándo ocurre?**
- **Pre-evento:** El coordinador arma presupuestos.
- **Durante el evento:** En el salón, con música alta, poca luz y el bartender con las manos mojadas atendiendo a decenas de personas.

---

## 👥 Usuarios (Actores)
| Usuario | Descripción |
| :--- | :--- |
| **Bartender** (App Móvil) | Usa la PWA en su celular. Recibe pedidos en tiempo real con vibración. Marca "Listo" con un toque. |
| **Admin/Dueño** (Panel Web) | Gestiona el catálogo de tragos, arma paquetes y activa el menú del evento del día. |
| **Invitado** (Kiosco Tablet) | Usa la tablet anclada en la barra para ver el menú (fotos grandes), checar ingredientes y enviar su pedido. |
| **Cliente Corporativo** (Web) | Visualiza los paquetes en la web para cotizar, sin necesidad de descargar nada. |

---

## 🎯 Tarea Principal
**¿Qué intenta hacer el usuario?**
1. **Bartender:** Ver la cola de pedidos (FIFO) y marcarlos como entregados sin soltar la botella.
2. **Invitado:** Pedir un trago en 3 segundos sin hacer fila larga.
3. **Admin:** Actualizar el menú disponible para el evento de hoy.

---

## 🧪 Hipótesis del Proyecto
> *"Si digitalizamos la cola de pedidos en una app que vibra al recibir nuevas órdenes y muestra botones táctiles gigantes, el tiempo de espera del invitado se reducirá significativamente y el estrés del bartender disminuirá, mejorando la experiencia global del evento."*

---

## 🧠 Modalidades de Implementación

### 🔵 Versión CON IA
- **Predictor de Stock:** La IA (Gemini) analiza el ritmo de consumo y sugiere al admin cuándo promocionar un trago para evitar que falte el más popular.
- **Voz a Texto (Hands-Free):** El bartender puede decir *"Orden 12 lista"* y la app la marca sin tocarla (Web Speech API).
- **Recomendación en Kiosco:** Si el invitado pide un trago con vodka, la IA sugiere otro similar para agilizar la decisión.

### 🟠 Versión SIN IA (Base funcional)
- **CRUD Clásico:** Admin gestiona tragos con formularios simples.
- **Filtros manuales:** En el Kiosco, se filtran tragos por categoría (Ron, Vodka, Sin Alcohol) con botones.
- **Firebase Realtime Database:** Sincroniza los pedidos entre el Kiosco y la App del Bartender sin necesidad de servidor propio. El bartender solo toca "✅ Completado" para actualizar el estado.

---

## 📐 Alcance del MVP (Primera entrega)
1. **Panel Admin:** ABM (Altas, Bajas, Modificaciones) de tragos + creación de un "Evento" (activar/desactivar tragos disponibles).
2. **Kiosco (Tablet):** Visualización del menú del evento activo y envío de pedidos a la base de datos.
3. **App Bartender (PWA):** Recepción en tiempo real de pedidos en cola y botón de "Completado" (con feedback háptico/vibración).

---

## 🛠️ Stack Tecnológico Propuesto
- **Frontend:** HTML5, CSS3, JavaScript (Vanilla) o React (si se animan).
- **Backend / DB:** Firebase Firestore (tiempo real y sin servidor).
- **IA:** Gemini Flash API (para sugerencias) y Web Speech API (para voz).
- **Despliegue:** Netlify / Vercel para la Web, y PWA instalable para el Kiosco y Bartender.

---

## 📝 Registro de Uso de IA (Clase 1)
> *"Utilicé DeepSeek para estructurar el flujo de trabajo de los 3 actores (Admin, Kiosco, Bartender) y definir la hipótesis centrada en la reducción del tiempo de espera. Además, usé Copilot para investigar cómo implementar la sincronización en tiempo real con Firebase y el manejo del API de vibración en dispositivos móviles para notificar al bartender sin que mire la pantalla."*

---

## 📎 Enlaces y Entregables
- [Repositorio del Proyecto](#) *(Pega aquí el link de tu repo cuando esté listo)*
- [Prototipo en Figma](#) *(Opcional)*
- [Demo en Vivo](#) *(Opcional)*
