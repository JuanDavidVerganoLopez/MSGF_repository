# MSGF — Clases límite y control 

La iteración 2 amplía el sistema de préstamos con aportes anuales y becas-crédito que se tramitan por semestre. Se mantienen las clases límite/control de la primera iteración y se agregan las siguientes.

## Clases límite (Boundary)

- **PantallaSolicitudPrestamo**: registra solicitudes de préstamo ordinario.
- **PantallaEstadoSolicitud**: permite consultar el estado de una solicitud.
- **PantallaPagos**: consulta saldos y registra pagos.
- **PantallaGestionPrestamos**: interfaz del gestor para evaluación, formalización y cartera.
- **PantallaRegistroAporte**: registra el aporte recibido en un año y muestra su trazabilidad.
- **PantallaPresupuestoBecas**: consulta el fondo disponible y la asignación de recursos.
- **PantallaSolicitudBecaCredito**: permite al estudiante solicitar el apoyo para un semestre y consultar su estado.
- **PantallaRegistroMatricula**: registra el costo de matrícula y la confirmación del periodo.
- **PantallaEntregaNotas**: recibe el reporte académico del semestre.
- **PantallaResultadoAcademico**: informa si el costo de matrícula se condona o se convierte en obligación de pago.

## Clases de control (Control)

- **ControlSolicitudPrestamo**: crea y valida solicitudes ordinarias.
- **ControlEvaluacionPrestamo**: aplica criterios de aprobación del préstamo.
- **ControlPrestamo**: formaliza el préstamo, coordina desembolso y saldo.
- **ControlPagos**: registra pagos y actualiza la cartera.
- **ControlAportes**: registra aportes anuales y los asocia al ejercicio correspondiente.
- **ControlFondoBecasCredito**: actualiza el presupuesto disponible y reserva recursos para apoyos aprobados.
- **ControlBecaCreditoSemestral**: gestiona solicitud, aprobación, matrícula y desembolso del semestre.
- **ControlReporteAcademico**: valida que las notas correspondan al estudiante y al periodo.
- **ControlEvaluacionAcademica**: evalúa el reporte usando la política vigente de MSGF.
- **ControlCondonacion**: aplica la condonación o genera una obligación de pago según el resultado.

## Reglas de negocio pendientes de definición
- El aporte se registra por año y alimenta el fondo destinado a becas-crédito.
- Cada beca-crédito corresponde a un periodo académico semestral y debe evaluarse de nuevo en cada semestre.
- Al terminar el semestre, el estudiante presenta sus notas. Según la política académica aprobada por MSGF, el costo de matrícula se **condona** o se convierte en una **obligación de devolución**.
- La política debe precisar la nota/promedio mínimo, créditos aprobados, excepciones, plazos y forma de devolución. No se fija un umbral arbitrario en estos diagramas.
- Deben definirse controles para evitar comprometer más dinero que el presupuesto anual disponible.
