# Backlog inicial

## Epicas
1. Autenticacion y perfiles
2. Reservas y calendario semanal
3. Bonos y consumo de sesiones
4. Administracion y operativa
5. Monitor y ejercicios

## Historias de usuario (seleccion)

### Epica 1: Autenticacion y perfiles
- HU1: Como alumno quiero acceder con email/telefono y PIN para gestionar mis reservas.
  - Criterios: valida credenciales; redirige segun rol; bloquea intentos invalidos.
- HU2: Como alumno quiero restablecer mi PIN para recuperar acceso.
  - Criterios: flujo controlado; PIN de 6 digitos; confirmacion visible.
- HU3: Como alumno quiero editar mis datos personales.
  - Criterios: nombre, apellidos, foto, telefono; cambios persistentes.

### Epica 2: Reservas y calendario
- HU4: Como alumno quiero ver la semana actual y sesiones por dia.
  - Criterios: muestra dia actual por defecto; orden cronologico; cupos visibles.
- HU5: Como alumno quiero reservar una sesion disponible.
  - Criterios: respeta aforo y bono; confirma reserva; descuenta sesion segun reglas.
- HU6: Como alumno quiero entrar en lista de espera si no hay cupo.
  - Criterios: se agrega en orden; notificacion placeholder.
- HU7: Como alumno quiero cancelar o cambiar una reserva.
  - Criterios: libre si faltan mas de 45 minutos; penaliza si no.

### Epica 3: Bonos
- HU8: Como alumno quiero ver mis bonos y sesiones restantes.
  - Criterios: muestra tipo de bono, sesiones usadas, sesiones disponibles.
- HU9: Como admin quiero registrar el pago y asignar bono.
  - Criterios: selecciona bono; marca estado de pago; fechas de vigencia.

### Epica 4: Administracion
- HU10: Como admin quiero crear y gestionar sesiones.
  - Criterios: alta, edicion y baja; asignar monitor; ajustar aforo.
- HU11: Como admin quiero confirmar asistencia al inicio de clase.
  - Criterios: lista de alumnos por sesion; marcar presentes; actualizar consumo.
- HU12: Como admin quiero mover o eliminar alumnos de sesiones.
  - Criterios: actualiza aforo; ajusta lista de espera si aplica.

### Epica 5: Monitor
- HU13: Como monitor quiero ver mis sesiones asignadas.
  - Criterios: listado por fecha; acceso rapido.
- HU14: Como monitor quiero registrar ejercicios de la sesion.
  - Criterios: campo de texto o lista; guarda por sesion.
