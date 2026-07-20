# Documentación de Requisitos - Sistema de Gestión de Activos con Códigos QR
## Historial de Versiones
| Versión | Fecha | Descripción | Autor |
| :--- | :--- | :--- | :--- |
| 1.0.0 | 20/07/2026 | Creación de historias de usuario iniciales | Darío |

---

## Funcionalidad 1: Autenticación de Usuarios (Login)
### 1. Historia de Usuario
* **ID:** HU-001
* **Título:** Inicio de sesión para administradores y técnicos
* **Prioridad:** Alta
* **Estimación:** 5 puntos
> **Como** Usuario del sistema (Administrador o Técnico)  
> **Quiero** Ingresar mi correo electrónico y contraseña en la interfaz de inicio de sesión  
> **Para** Acceder de forma segura al panel de control y gestionar el inventario de activos  

### 2. Criterios de Aceptación (Sintaxis Gherkin)
#### Escenario 1: Inicio de sesión exitoso
* **Given** El usuario se encuentra en la pantalla de login del sistema
* **When** Ingresa credenciales válidas y hace clic en "Iniciar Sesión"
* **Then** El sistema valida las credenciales y redirige al panel principal (Dashboard)

#### Escenario 2: Error por credenciales inválidas
* **Given** El usuario se encuentra en la pantalla de login del sistema
* **When** Ingresa una contraseña incorrecta y hace clic en "Iniciar Sesión"
* **Then** El sistema muestra un mensaje de error indicando que las credenciales son incorrectas y no permite el acceso

### 3. Ciclo de Vida y Estado de la Funcionalidad
Marca con una `X` el estado actual en el que se encuentra esta funcionalidad en tu proyecto:
- [X] **Por hacer (To Do):** Requisito documentado y aprobado.
- [ ] **En Desarrollo (In Progress):** El código se está escribiendo actualmente.
- [ ] **En Pruebas (Testing):** Verificando los criterios de aceptación.
- [ ] **Desplegado/Listo (Done):** Funcionalidad terminada y funcional.

---

## Funcionalidad 2: Generación de Códigos QR para Activos
### 1. Historia de Usuario
* **ID:** HU-002
* **Título:** Generación de etiqueta QR para nuevos activos registrados
* **Prioridad:** Alta
* **Estimación:** 8 puntos
> **Como** Administrador del sistema  
> **Quiero** Generar y visualizar un código QR único al registrar un nuevo activo de hardware o mobiliario  
> **Para** Imprimir la etiqueta y adherirla físicamente al bien para su posterior rastreo  

### 2. Criterios de Aceptación (Sintaxis Gherkin)
#### Escenario 1: Generación exitosa de código QR
* **Given** El administrador ha completado el formulario de registro de un nuevo activo con datos válidos
* **When** Hace clic en el botón "Guardar y Generar QR"
* **Then** El sistema almacena el activo en la base de datos y genera una imagen de código QR vinculada a su ID único

#### Escenario 2: Intento de generación con campos vacíos
* **Given** El administrador está registrando un activo nuevo
* **When** Deja campos obligatorios (como el código de serie o nombre) en blanco y presiona generar
* **Then** El sistema bloquea la acción y muestra un mensaje indicando que se deben completar todos los campos obligatorios

### 3. Ciclo de Vida y Estado de la Funcionalidad
- [X] **Por hacer (To Do):** Requisito documentado y aprobado.
- [ ] **En Desarrollo (In Progress):** El código se está escribiendo actualmente.
- [ ] **En Pruebas (Testing):** Verificando los criterios de aceptación.
- [ ] **Desplegado/Listo (Done):** Funcionalidad terminada y funcional.
