# Mockups de UI (Conceptual)

Este documento define la estructura y organización de las pantallas principales de la webapp mediante representaciones conceptuales de baja fidelidad.

## 1. Pantalla de Login
**Objetivo:** Acceso rápido y seguro vía PIN.

```text
+--------------------------------+
|                                |
|          TERROR GYM            |
|      Entrena sin límites       |
|                                |
|  [ Email o Teléfono          ] |
|                                |
|  PIN de acceso:                |
|  [ * ] [ * ] [ * ] [ * ] [ * ] |
|                                |
|  [      ENTRAR (BTN)         ] |
|                                |
|       ¿Olvidaste tu PIN?       |
|                                |
+--------------------------------+
```

### Elementos:
*   **Logo/Título:** Centrado en la parte superior.
*   **Input Identificador:** Único campo para email o teléfono.
*   **Input PIN:** 6 casillas separadas para fácil digitación en móvil.
*   **Botón Principal:** Acción de login (Color de énfasis).
*   **Link Recuperación:** Texto discreto al pie.

---

## 2. Dashboard Alumno (Pantalla Principal)
**Objetivo:** Visión inmediata del calendario y acceso a clases con visualización de participantes.

```text
+--------------------------------+
| Hola, Javier           (Avatar)|
| Alumno                         |
+--------------------------------+
| < LUN  MAR  [MIE]  JUE  VIE >  |
|   10   11    12    13   14     |
+--------------------------------+
| SESIONES DE HOY                |
|                                |
| +----------------------------+ |
| | 18:00 - 19:00    RESERVADO | |
| | CrossFit WOD               | |
| | Participantes:             | |
| | (Yo)(A)(B)(C)(_)(_)  4/6   | |
| +----------------------------+ |
|                                |
| +----------------------------+ |
| | 19:00 - 20:00     8 LIBRES | |
| | Halterofilia               | |
| | Participantes:             | |
| | (A)(B)(_)(_)(_)(_)   2/6   | |
| +----------------------------+ |
|                                |
+--------------------------------+
| (Menú Inferior: Home | Perfil) |
+--------------------------------+
```

### Elementos:
*   **Cabecera:** Saludo personalizado y rol. Avatar clicable que lleva al Perfil.
*   **Selector de Día (Strip Calendar):** Barra horizontal scrolleable para seleccionar el día de la semana.
*   **Lista de Sesiones:** Tarjetas con la información clave de cada clase:
    *   Hora y Nombre de la clase.
    *   **Visualización de Plazas:** Fila de avatares circulares representando los alumnos apuntados. Los huecos libres se muestran como círculos vacíos. Permite ver rápidamente quién va y cuánto falta para llenar.

---

## 3. Perfil del Alumno
**Objetivo:** Gestión de datos personales y consulta de estado del bono.

```text
+--------------------------------+
| < Volver                       |
|          PERFIL                |
+--------------------------------+
|        (Avatar Grande)         |
|         Javier León            |
|           Alumno               |
+--------------------------------+
| MI BONO                        |
| [=======-------] 3/12 Sesiones |
| Estado: Activo                 |
| Renueva: 01/Nov                |
+--------------------------------+
| DATOS PERSONALES               |
| Email: javier@example.com      |
| Tel: +34 600 000 000           |
|                                |
|       [ Editar Datos ]         |
+--------------------------------+
|       [ Cerrar Sesión ]        |
+--------------------------------+
```

### Elementos:
*   **Info Usuario:** Foto grande, nombre y rol.
*   **Tarjeta de Bono:** Estado detallado del consumo de clases y fecha de renovación.
*   **Datos Personales:** Información de contacto editable.
*   **Acciones:** Botones para editar perfil y cerrar sesión.

---

## 4. Detalle de Sesión & Reserva
**Objetivo:** Información completa de la clase, participantes y acción de reservar.

```text
+--------------------------------+
|  < Volver                      |
|                                |
|      [ IMAGEN DE PORTADA ]     |
|                                |
+--------------------------------+
| Functional Training            |
| Mie 12 Oct • 18:00 - 19:00     |
+--------------------------------+
| (Avatar) Carlos H.             |
|          Instructor            |
+--------------------------------+
| PARTICIPANTES (12/15)          |
| (A)(B)(C)(D)(E)(F)(G)(H)       |
| (I)(J)(K)(L)(_)(_)(_)          |
+--------------------------------+
| DESCRIPCIÓN                    |
| Entrenamiento de alta intensi- |
| dad enfocado en fuerza...      |
+--------------------------------+
| [    RESERVAR AHORA (BTN)    ] |
|(Fijo en la parte inferior)     |
+--------------------------------+
```

### Elementos:
*   **Navegación:** Botón simple de "Volver".
*   **Info Principal:** Título grande, fecha y hora visibles.
*   **Instructor:** Quién imparte la clase.
*   **Participantes:** Grid de avatares mostrando quiénes asisten y visualizando los huecos libres.
*   **Descripción:** Detalles de la clase.
*   **Botón de Acción (Sticky):** Siempre visible abajo. Cambia de estado según situación:
    *   "RESERVAR" (Si hay cupo).
    *   "UNIRSE A LISTA DE ESPERA" (Si está lleno).
    *   "CANCELAR RESERVA" (Si ya está reservado).

---

## 5. Dashboard Administración (iPad Horizontal)
**Objetivo:** Control operativo completo y gestión de asistencia en pantalla grande.

```text
+----------------------+--------------------------------------------------+
| PANEL ADMIN          | Hola, Administrador (Avatar)            [Salir]  |
|                      +--------------------------------------------------+
| [ INICIO           ] | ESTADÍSTICAS HOY                                 |
| [ Usuarios         ] | +-------------+  +-------------+  +-------------+|
| [ Clases           ] | | 8 SESIONES  |  | 142 USERS   |  | (!) ALERTAS ||
| [ Pagos (Manual)   ] | | (Ver Todo)  |  | (+2 hoy)    |  | 3 Pendientes||
| [ Configuración    ] | +-------------+  +-------------+  +-------------+|
|                      |                                                  |
|                      | GESTIÓN DE SESIONES                              |
|                      | <  Miércoles 12 Octubre  >         [ + NUEVA ]   |
|                      |                                                  |
|                      | +----------------------------------------------+ |
|                      | | 09:00 - Yoga Hatha             15/15 (FULL)  | |
|                      | | (Monitor: Ana)      [ LISTA ASISTENCIA ]     | |
|                      | +----------------------------------------------+ |
|                      | +----------------------------------------------+ |
|                      | | 10:00 - Pilates Reformer        8/15 (OK)    | |
|                      | | (Monitor: Luis)     [ LISTA ASISTENCIA ]     | |
|                      | +----------------------------------------------+ |
|                      | +----------------------------------------------+ |
|                      | | 18:00 - CrossFit WOD           12/20 (OK)    | |
|                      | | (Monitor: Carlos)   [ LISTA ASISTENCIA ]     | |
|                      | +----------------------------------------------+ |
+----------------------+--------------------------------------------------+
```

### Elementos:
*   **Layout:** Disposición de dos columnas (Sidebar y Contenido Principal).
*   **Sidebar:** Navegación rápida entre módulos (Usuarios, Clases, etc.).
*   **KPIs:** Tarjetas informativas alineadas horizontalmente.
*   **Gestión de Sesiones:**
    *   Listado amplio con más detalles (Nombre completo, monitor).
    *   Botón directo "Lista Asistencia" para el control rápido al inicio de la clase.
    *   Botón "Nueva" destacado.

---

## 6. Admin: Lista de Asistencia (Check-in)
**Objetivo:** Control en tiempo real de quién ha llegado a la clase.

```text
+----------------------+--------------------------------------------------+
| PANEL ADMIN          | < Volver a Dashboard                    [Salir]  |
|                      +--------------------------------------------------+
| [ INICIO           ] | ASISTENCIA: CrossFit WOD (18:00 - 19:00)         |
| [ Usuarios         ] | Monitor: Carlos H.   |   Aforo: 12 / 20 Presentes|
| [ Clases           ] |                                                  |
| [ Pagos (Manual)   ] | LISTADO DE INSCRITOS                             |
| [ Configuración    ] | +----------------------------------------------+ |
|                      | | [?] Javier León (Bono 3/12)      [ CONFIRMAR ] | |
|                      | +----------------------------------------------+ |
|                      | | [OK] Ana García (Bono 5/12)      [ CANCELAR  ] | |
|                      | | (Llegó a las 17:55)                            | |
|                      | +----------------------------------------------+ |
|                      | | [?] Pedro S. (Bono 1/12)         [ CONFIRMAR ] | |
|                      | +----------------------------------------------+ |
|                      | | [X] María L. (NO PRESENTADA)     [ PENALIZAR ] | |
|                      | +----------------------------------------------+ |
|                      |                                                  |
|                      | LISTA DE ESPERA (3 Personas)                     |
|                      | 1. Juan P. [ AVISAR HUECO ]                      |
+----------------------+--------------------------------------------------+
```

### Elementos:
*   **Cabecera de Clase:** Resumen de la sesión y contador de asistencia en tiempo real.
*   **Lista de Inscritos:**
    *   Estado visual: `[?]` Pendiente, `[OK]` Presente, `[X]` No presentado.
    *   Botón de acción rápida: `CONFIRMAR` (Check-in).
*   **Gestión de Lista de Espera:** Acciones para cubrir huecos de cancelaciones o incomparecencias.

---

## 7. Admin: Directorio de Usuarios
**Objetivo:** Gestión centralizada de pagos y bonos.

```text
+----------------------+--------------------------------------------------+
| PANEL ADMIN          | Usuarios                                [Salir]  |
|                      +--------------------------------------------------+
| [ Inicio           ] | BUSCAR USUARIO                                   |
| [ USUARIOS (Activo)] | [ Buscar por nombre, email o tlf...            ] |
| [ Clases           ] |                                                  |
| [ Pagos (Manual)   ] | RESULTADOS (142 Total)        [ + NUEVO ALUMNO ] |
| [ Configuración    ] |                                                  |
|                      | NOMBRE           | BONO ACTIVO      | ESTADO     |
|                      | -----------------|------------------|------------|
|                      | Javier León      | 3 Clases/Sem     | [ AL DÍA ] |
|                      |                  | Renueva: 01/Nov  | [ Editar ] |
|                      | -----------------|------------------|------------|
|                      | Lucía Méndez     | -- SIN BONO --   | [ INACTIVO]|
|                      |                  |                  | [ Asignar ]|
|                      | -----------------|------------------|------------|
|                      | Carlos Ruiz      | 2 Clases/Sem     | [ PENDIENTE]|
|                      |                  | Caducó: ayer     | [ RENOVAR ]|
|                      | -----------------|------------------|------------|
+----------------------+--------------------------------------------------+
```

### Elementos:
*   **Buscador Global:** Filtrado rápido para encontrar alumnos en recepción.
*   **Tabla de Estado:** Vista rápida de si el alumno está "Al día", "Pendiente de pago" o "Inactivo".
*   **Acciones Rápidas:** Botones directos para Renovar/Asignar bono sin entrar al detalle profundo.

---

## 8. Admin: Registro Manual de Pagos (Modal)
**Objetivo:** Registrar el pago de un bono (efectivo/transferencia) y activarlo.

```text
+--------------------------------------------------+
|  REGISTRAR PAGO Y RENOVAR BONO                   |
+--------------------------------------------------+
|  Alumno: Carlos Ruiz                             |
|                                                  |
|  SELECCIONAR BONO:                               |
|  ( ) 2 Clases/Semana (20 EUR)                    |
|  (X) 3 Clases/Semana (30 EUR)                    |
|  ( ) Ilimitado (50 EUR)                          |
|                                                  |
|  MÉTODO DE PAGO (Registro Interno):              |
|  [ Efectivo ] [ Transferencia ] [ Bizum ]        |
|                                                  |
|  VIGENCIA:                                       |
|  Desde: [ 12/10/2023 ]  Hasta: [ 11/11/2023 ]    |
|                                                  |
|  [ CANCELAR ]           [ CONFIRMAR PACO (30€) ] |
+--------------------------------------------------+
```

### Elementos:
*   **Selección de Producto:** Tipos de bonos predefinidos.
*   **Registro de Método:** Solo informativo para caja (no procesa pago real).
*   **Fechas:** Calculadas automáticamente pero editables.
*   **Confirmación:** Activa el bono inmediatamente en el perfil del alumno.

---

## 9. Crear / Restablecer PIN
**Objetivo:** Establecer un código de acceso seguro de 6 dígitos.

```text
+--------------------------------+
| < Volver                       |
|                                |
|        CREA TU PIN             |
|                                |
| Para proteger tu cuenta,       |
| define un código de 6 dígitos. |
|                                |
|  NUEVO PIN:                    |
|  [ * ] [ * ] [ * ] [ * ] [ * ] |
|                                |
|  OSCURO:                       |
|  [ * ] [ * ] [ * ] [ * ] [ * ] |
|                                |
|                                |
| [      GUARDAR PIN (BTN)     ] |
|                                |
+--------------------------------+
```

### Elementos:
*   **Instrucciones claras:** Breve explicación de seguridad.
*   **Doble validación:** Dos filas de inputs para asegurar que el PIN es el deseado (Nuevo PIN y Confirmar PIN).
*   **Feedback visual:** Indicadores de coincidencia (verde/rojo) antes de guardar.

---

## 10. Dashboard Monitor & Registro WOD
**Objetivo:** Gestión de clases asignadas y registro del entrenamiento del día.

```text
+--------------------------------+
| Hola, Coach Carlos     (Avatar)|
| Monitor                        |
+--------------------------------+
| MIS CLASES HOY                 |
|                                |
| 18:00 - CrossFit WOD           |
| (12/15 Alumnos)    [ DETALLE ] |
|                                |
| 19:30 - Halterofilia           |
| (8/10 Alumnos)     [ DETALLE ] |
+--------------------------------+
| REGISTRAR ENTRENAMIENTO (WOD)  |
| Clase: [ 18:00 - CrossFit WOD v]
|                                |
| Título: "Murph"                |
|                                |
| Descripción / Ejercicios:      |
| [ Run 1 mile                 ] |
| [ 100 Pull-ups               ] |
| [ 200 Push-ups               ] |
| [ 300 Squats                 ] |
| [ Run 1 mile                 ] |
|                                |
|         [ PUBLICAR WOD ]       |
+--------------------------------+
```

### Elementos:
*   **Agenda Personal:** Solo muestra las clases donde el usuario es monitor.
*   **Acceso a Detalle:** Para ver quiénes asisten (similar a la vista de admin pero solo lectura).
*   **Editor WOD:** Textarea simple o lista para definir qué se hará en la clase. Esto se mostrará luego a los alumnos en el detalle de sesión.

---

## 11. Admin: Editor de Sesión
**Objetivo:** Crear o modificar una clase en el calendario.

```text
+--------------------------------+
| < Cancelar      NUEVA SESIÓN   |
+--------------------------------+
| ACTIVIDAD:                     |
| [ CrossFit WOD               v]|
|                                |
| FECHA Y HORA:                  |
| [ 12 / Oct / 2023 ]  [ 18:00 ] |
| Duración: [ 60 min ]           |
|                                |
| MONITOR ASIGNADO:              |
| [ Carlos H.                  v]|
|                                |
| AFORO MÁXIMO:                  |
| [ - ]  15  [ + ]               |
|                                |
| NOTAS INTERNAS (Opcional):     |
| [                            ] |
|                                |
|      [ CREAR SESIÓN ]          |
|      [ ELIMINAR SESIÓN ]       |
+--------------------------------+
```

### Elementos:
*   **Selectores:** Dropdowns para actividad y monitor para evitar errores.
*   **Control de Aforo:** Stepper numérico para ajuste rápido.
*   **Acciones:** Crear/Guardar cambios y, si es edición, opción de Eliminar (con confirmación por si hay reserva).

---

## 12. Edición de Perfil (Alumno)
**Objetivo:** Actualizar datos personales y preferencias.

```text
+--------------------------------+
| < Cancelar      EDITAR PERFIL  |
+--------------------------------+
| FOTO:                          |
| (Avatar Actual)  [ CAMBIAR ]   |
|                                |
| NOMBRE COMPLETO:               |
| [ Javier León                ] |
|                                |
| TELÉFONO (Para contacto):      |
| [ +34 600 000 000            ] |
|                                |
| EMAIL (Login):                 |
| [ javier@example.com         ] |
|                                |
| SEGURIDAD:                     |
| [ CAMBIAR PIN DE ACCESO ]      |
|                                |
|      [ GUARDAR CAMBIOS ]       |
+--------------------------------+
```

### Elementos:
*   **Formulario Estándar:** Inputs de texto para datos básicos.
*   **Acceso a PIN:** Botón separado para el flujo de cambio de PIN (Pantalla 9).
*   **Subida de Foto:** Botón para cambiar el avatar.

---

## 13. Historial de Clases (Alumno)
**Objetivo:** Consultar asistencia pasada.

```text
+--------------------------------+
| < Volver       HISTORIAL       |
+--------------------------------+
| ESTE MES (Octubre)             |
| Asistidas: 5  |  Canceladas: 1 |
+--------------------------------+
| Jueves 13 Oct - 18:00          |
| CrossFit WOD            [ OK ] |
| ------------------------------ |
| Martes 11 Oct - 19:30          |
| Powerlifting            [ OK ] |
| ------------------------------ |
| Lunes 10 Oct - 09:00           |
| Yoga              [ NO FUI ❌ ] |
| ------------------------------ |
| Viernes 7 Oct - 18:00          |
| CrossFit WOD      [ CANCELADA ]|
+--------------------------------+
```

### Elementos:
*   **Resumen Mensual:** Contador rápido de actividad.
*   **Lista Cronológica Inversa:** Clases pasadas.
*   **Estado:** Indicador visual de si asistió `[ OK ]`, faltó `[ NO FUI ]` o canceló `[ CANCELADA ]`.


