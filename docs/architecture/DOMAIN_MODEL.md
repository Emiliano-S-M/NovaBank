# NovaBank - Domain Model
## Introducción
El Domain Model define las entidades principales del sistema bancario NovaBank, sus responsabilidades, relaciones y
reglas de negocio.

Este documento represent el lenguaje del negocio y servirá como guía para el desarrollo de todos los microservicios del
proyecto.

El objetivo es separar claramente la lógica del negocio de los detalles técnicos de implementación.

---

## Objetivos
* Identificar las entidades principales del sistema.
* Definir las responsabilidades de cada entidad.
* Establecer los límites de cada microservicio.
* Facilitar el mantenimiento y evolución del sistema

---

## Principios del Dominio

NovaBank seguirá los siguientes principio:
* Cada microservicio será propietario de sus propios datos.
* Ningún servicio acederá directamente a la base de datos de otro.
* La comunicación entre microservicios se realizará mediante APIs REST o mensajería.
* Cada entidad tendrá una única responsabilidad dentro del negocio.
* El dominio será independiente de frameworks y tecnologías.

---

## Entidades Principales

### Customer

Representa a un cliente registrado en el banco.

Responsabilidades:

* Mantener información personal.
* Almacenar datos de contacto.
* Asociarse a una o varias cuentas bancarias.
* Solicitar productos financieros.

---

### User

Representa las credenciales utilizadas para acceder al sistema.

Responsabilidades:

* Autenticación
* Gestión de contraseña.
* Asociación de Roles.
* Asociación de permisos.

---

### Role

Define el conjunto de privilegios asignados a un usuario.

Ejemplos:
* ADMIN
* CUSTOMER
* EMPLOYEE
* AUDITOR

---

### Permission

Representa una acción específica permitida dentro del sistema.

Ejemplos:

* CREATE_ACCOUNT
* TRANSFER
* APPROVE_LOAN
* VIEW_REPORTS

---

### Account

Representa una cuenta bancaria perteneciente a un cliente

Tipos previstos:

* Cuenta de ahorro
* Cuenta corriente
* Cuenta empresarial

Responsabilidades:

* Administrar saldo.
* Registrar movimientos.
* Permitir transferencias.

---

### Transaction

Representa cualquier movimiento financiero.

Tipos previstos:

* Depósito
* Retiro
* Transferencia
* Pago
* Comisión

---

### Card

Representa una tarjeta asociada a una cuenta.

Tipos previstos:

* Débito
* Crédito

---

### Loan

Representa un préstamo solicitado por un cliente.

Responsabilidades:

* Registrar monto.
* Registrar plazo.
* Registrar estado.
* Registrar pagos.

---

### Notification

Representa una notificación enviada al cliente.

Canales previstos:

* Correo electrónico
* SMS
* Push

---

### Audit

Representa un evento importante ocurrido dentro del sistema.

Ejemplos:

* Inicio de sesión
* Cambio de contraseña
* Transferencia realizada
* Creación de cuenta

---

### Relaciones del Dominio
```text
Customer

├── posee → Account

├── solicita → Loan

├── recibe → Notification

└── utiliza → User

Account

└── genera → Transaction

User

└── posee → Role

Role

└── contiene → Permission
```

---

### Reglas de Negocio
* Un cliente puede tener múltiples cuentas.
* Una cuenta pertenece únicamente a un cliente.
* Toda transacción debe quedar registrada.
* Toda operación importante debe generar un evento de auditoría.
* Los usuarios deben autenticarse mediante JWT.
* Las contraseñas nunca se almacenarán en texto plano.
* Cada servicio será propietario de su información.

---

### Eventos de Negocio

Eventos previstos:

* Cliente registrado.
* Usuario autenticado.
+ Cuenta creada.
* Depósito realizado.
* Retiro realizado.
* Transferencia realizada.
* Préstamo solicitado.
* Notificación enviada.

---

### Límites de los Microservicios

Auth Service

* User
* Role
* Permission

Customer Service

* Customer

Account Service

* Account

Transaction Service

* Transaction

Loan Service

* Loan

Notification Service

* Notification

Audit Service

* Audit

---
### Futuras Extensiones

El dominio podrá ampliarse con nuevas funcionalidades como:

* Inversiones.
* Gestión de tarjetas virtuales.
* Pagos internacionales.
* Detección de fraude.
* Open Banking.
* Integración con inteligencia artificial.
* Integración con aplicaciones móviles.