## 📌 **Introducción al Diseño Orientado a Objetos**  
📝 **Definición del paradigma orientado a objetos**  
La Programación Orientada a Objetos (POO) es un enfoque de desarrollo basado en la creación de entidades llamadas **objetos**, que agrupan datos y comportamiento en una sola unidad. Su importancia radica en la reutilización de código, modularidad y escalabilidad.

---

## 🎯 **Los Cuatro Fundamentos de POO**  

✅ **Encapsulamiento**  
👉 *Ejemplo:* Un automóvil tiene un motor encapsulado. Desde afuera, los usuarios pueden acelerar o frenar sin conocer el funcionamiento interno del motor.  

✅ **Herencia**  
👉 *Ejemplo:* Un "Auto Deportivo" hereda propiedades de la clase "Auto", pero añade nuevas características como mayor velocidad.  

✅ **Polimorfismo**  
👉 *Ejemplo:* Un "pago" puede realizarse con tarjeta de crédito, débito o en efectivo. Aunque la acción es la misma (pagar), el comportamiento varía según el método utilizado.  

✅ **Abstracción**  
👉 *Ejemplo:* Un usuario de una app de delivery solo ve opciones para pedir comida, sin preocuparse por la lógica interna del sistema.  

---

## ✅ **Requisitos del Sistema**  
1️⃣ Debe permitir a los usuarios agendar turnos.  
2️⃣ Debe enviar recordatorios automáticos.  
3️⃣ Debe permitir la cancelación y reprogramación de turnos.  
4️⃣ Debe gestionar diferentes tipos de usuarios (pacientes, médicos, administradores).  
5️⃣ Debe almacenar historiales de turnos.  

---

## 🔍 **Casos de Uso**  

### 📌 **Caso 1: Agendar turno**  
**Actor(es):** Paciente  
**Descripción:** El paciente solicita un turno.  
**Flujo principal:**  
1. El usuario ingresa al sistema.  
2. Selecciona fecha y hora.  
3. Confirma el turno.  

### 📌 **Caso 2: Cancelar turno**  
**Actor(es):** Paciente  
**Descripción:** El paciente decide cancelar un turno previamente agendado.  
**Flujo principal:**  
1. El usuario inicia sesión.  
2. Busca el turno en su historial.  
3. Cancela el turno y recibe una confirmación.  

### 📌 **Caso 3: Registrar un nuevo usuario**  
**Actor(es):** Administrador  
**Descripción:** Un administrador registra un nuevo usuario en el sistema.  
**Flujo principal:**  
1. El administrador accede al sistema.  
2. Ingresa los datos del nuevo usuario.  
3. Confirma la creación del usuario.  

### 📌 **Caso 4: Notificación de recordatorio**  
**Actor(es):** Sistema  
**Descripción:** El sistema envía un recordatorio de turno.  
**Flujo principal:**  
1. El sistema verifica los turnos del día siguiente.  
2. Envía una notificación al paciente.  

### 📌 **Caso 5: Modificar horario de turno**  
**Actor(es):** Paciente  
**Descripción:** El paciente desea cambiar la fecha u hora de su turno.  
**Flujo principal:**  
1. El usuario accede a su historial.  
2. Selecciona el turno que desea modificar.  
3. Elige una nueva fecha/hora y confirma el cambio.  

---

## 📌 **Boceto Inicial del Diseño de Clases**  
🖼️ ![Boceto del diseño de clases](diagrams/boceto.png)  
🔗 [Ver en línea](https://link-a-diagrama.com)  
