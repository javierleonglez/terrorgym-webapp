# Diseno tecnico (alto nivel)

## Stack
- Frontend: HTML, CSS, JavaScript vanilla.
- Hosting: Vercel.
- Backend: Supabase (Postgres + Auth si aplica).

## Arquitectura
- SPA ligera con rutas por rol.
- API via Supabase para datos y autenticacion.
- Acceso movil primero, admin optimizado para tablet en horizontal.

## Autenticacion
- Login por email o telefono + PIN de 6 digitos.
- PIN almacenado de forma segura (hash en backend).
- Restablecimiento de PIN via flujo administrado.

## Entidades principales
- Usuario: datos personales y roles.
- Bono: tipo, precio, sesiones por semana, estado.
- Sesion: fecha, hora, aforo, monitor asignado.
- Reserva: usuario, sesion, estado, timestamps.
- Lista de espera: orden de solicitud por sesion.
- Asistencia: confirmacion por sesion.

## Relaciones (resumen)
- Usuario 1..n Reservas.
- Sesion 1..n Reservas.
- Sesion 1..n Lista de espera.
- Usuario 1..n Asistencias.
- Monitor es un rol de Usuario.

## Reglas de acceso
- Alumno: solo ve sus reservas y datos personales.
- Monitor: ve sesiones asignadas y asistentes.
- Admin: acceso total.

## Consideraciones
- Registrar eventos clave (reserva, cancelacion, penalizacion).
- Validar limites de bono por semana.
- Controlar race conditions en aforo y lista de espera.
