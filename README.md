# simulacionMedicoSoftware
## Adrian Andres Ramirez Andrade
---

En el caso de uso, el actor estudiante tiene acceso a ver historial de otra persona, cosa que por reglas de negocio no debería ser posible, este solo deberia tener acceso a su propio historial de reservas, este apartado deberia pertenecer al actor de administrador.

Notificar el cambio por correo deberia estar conectado al actor estudiante para que tenga manera de comprobar que su solicitud fue recibida, aprobada o rechazada dentro del sistema, ademas de notificarle de algun cambio efectuado por el administrador.

A lo largo del diagrama de caso de uso hay ausencia de los include y extend los cuales para estudiante debe haber unos 4 include en: Cancelar reserva, ver estado de solicitudes, reservar sala y ver historial de reservas. De ver historial de reserva un extend a eliminar historial de reservas sin el estudiante asi lo desea.

El reservar sala deberia estar a posterior de consultar disponibilidad, es decir: primero se consulta a sistema si hay disponibilidad de reserva de sala y a partir de ahí hacer la reserva, posterior a esto una conexión include hacia generar una notificación por correo, esto da pie a otra falla encontrada, el aprobar reserva, rechazar reserva y cancelar reserva deberia dar a un include a notificar por correo hacia el estudiante y así el estudiante tendria un feedback con respecto a los estados de sus solicitudes.

Agregar motivo de cancelación deberia ser un extend para el estudiante si desea o no el dar un motivo.

---

En el diagrama de clase 
No se indica si Usuario tiene una relación de agregación o composición con Reserva.
No hay relación explícita entre Administrador y SistemaReservas



