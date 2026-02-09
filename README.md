# terrorgym

Documentacion base del proyecto terrorgym. Esta es la referencia principal para guiar el desarrollo y las decisiones de producto.

## Resumen ejecutivo
terror gym es una webapp para gestionar clases de un gimnasio con reservas semanales, bonos mensuales y control de asistencia. El objetivo es sustituir la gestion manual por un sistema simple, rapido y orientado a movil.

## Objetivos
- Automatizar reservas semanales con control de aforo y lista de espera.
- Reducir tareas manuales del administrador.
- Dar al alumno visibilidad de su bono, sesiones restantes y estadisticas.
- Registrar asistencia y penalizaciones por cancelacion tardia.

## Alcance inicial
- Autenticacion por email o telefono + PIN de 6 digitos.
- Roles: Alumno, Monitor y Administrador (posible rol combinado Admin+Monitor).
- Calendario semanal con horarios fijos y reservas por clase.
- Bonos mensuales: 2 clases/semana (20 EUR) y 3 clases/semana (30 EUR).
- Lista de espera cuando el aforo (15) esta completo.
- Cancelacion libre hasta 45 minutos antes, despues consume sesion.
- Panel admin para gestionar usuarios, clases, aforos y asistencia.

## Fuera de alcance inicial
- Pasarela de pagos dentro de la app (el pago es externo y se registra manualmente).
- Notificaciones avanzadas (solo mensajes basicos en el flujo de alta, si aplica).
- App nativa.

## Documentos
- Vision del producto: [docs/vision.md](docs/vision.md)
- Roles y flujos: [docs/roles-y-flujos.md](docs/roles-y-flujos.md)
- Reglas de negocio: [docs/reglas-de-negocio.md](docs/reglas-de-negocio.md)
- Diseno tecnico: [docs/diseno-tecnico.md](docs/diseno-tecnico.md)
- Backlog inicial: [docs/backlog.md](docs/backlog.md)
- Privacidad y seguridad: [docs/privacidad-y-seguridad.md](docs/privacidad-y-seguridad.md)

## Glosario
- Bono: paquete mensual que define el numero de clases semanales disponibles.
- Sesion: clase concreta en una fecha y hora.
- Reserva: inscripcion de un alumno a una sesion.
- Lista de espera: cola cuando el aforo esta lleno.
- Asistencia: confirmacion de presencia en la sesion.

## Restricciones y supuestos
- Webapp responsive, foco movil vertical para alumno/monitor y tablet horizontal para admin.
- Tecnologias: HTML, CSS y JavaScript vanilla. Hosting en Vercel. Base de datos Postgres via Supabase.
- Idioma principal: espanol.

## Estado
Este documento es base viva; cualquier cambio de alcance o reglas debe reflejarse aqui y en docs.
