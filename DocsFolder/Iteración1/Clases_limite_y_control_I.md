# MSGF — Clases límite y control 

## Clases límite 
Representan los puntos de interacción entre los actores y el sistema.

- PantallaSolicitudPrestamo: captura datos del solicitante, monto y plazo; muestra validaciones.
- PantallaEstadoSolicitud: permite consultar el estado de una solicitud.
- PantallaPagos: presenta saldo y permite registrar/consultar pagos.
- PantallaGestionPrestamos: interfaz del gestor para revisar solicitudes y administrar préstamos.

## Clases de control 
Organiza las reglas y el flujo del caso de uso, sin ser la interfaz ni los datos persistentes.

- ControlSolicitudPrestamo: crea y valida solicitudes, y coordina su evaluación.
- ControlEvaluacion: aplica los criterios definidos por MSGF y registra el resultado.
- ControlPrestamo: formaliza préstamos aprobados, coordina el desembolso y calcula el saldo.
- ControlPagos: valida y registra pagos, actualiza el saldo pendiente.

## Criterios y supuestos
- Los criterios de aprobación, tasa, plazos y documentación deben ser configurables por MSGF; no se inventan valores de negocio.
- El diagrama de clases representa las entidades principales y sus asociaciones; las clases límite/control se detallan aquí para separar interfaz, lógica y datos.
