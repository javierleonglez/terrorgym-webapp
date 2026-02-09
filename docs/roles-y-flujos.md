# Roles y flujos

## Roles
### Alumno
- Gestionar reservas semanales.
- Consultar bono, sesiones restantes, historial y estadisticas.
- Editar perfil personal.

### Monitor
- Aparecer asignado a sesiones.
- Registrar ejercicios de la sesion.
- Consultar listados de alumnos por sesion.

### Administrador
- Crear, modificar y eliminar sesiones.
- Gestionar aforos y horarios.
- Alta de usuarios y asignacion de roles.
- Confirmar asistencia al inicio de las clases.
- Gestionar el estado de pago (manual).
- Mover o eliminar alumnos de sesiones.
- Puede tener rol de Monitor.

## Flujos clave
### Login
1. Usuario introduce email o telefono.
2. Introduce PIN de 6 digitos.
3. Sistema valida y redirige segun rol.

### Restablecer PIN
1. Usuario solicita restablecer PIN.
2. Admin o flujo asistido valida identidad.
3. Usuario define nuevo PIN.

### Reserva de clase (Alumno)
1. Usuario entra a pantalla principal.
2. Ve semana actual y selecciona dia.
3. Ve sesiones del dia con cupos y lista de espera.
4. Reserva una sesion si tiene cupo de bono disponible.
5. Si no hay cupo, se une a lista de espera.

### Cambio o cancelacion
1. Usuario selecciona su reserva.
2. Puede cambiar o cancelar si faltan mas de 45 minutos.
3. Si cancela dentro de 45 minutos, se consume sesion.

### Confirmacion de asistencia (Admin)
1. Admin abre sesion al inicio.
2. Marca asistencia por alumno.
3. Actualiza consumo de sesiones.

### Gestion de sesiones (Admin)
1. Crear nuevas sesiones o modificar horario.
2. Asignar monitor.
3. Ajustar aforo.
