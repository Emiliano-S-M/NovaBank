# Sprint 01 - Fundación del proyecto

## Objetivo del sprint

Establecer la arquitectura base del proyecto NovaBank y preparar la infraestructura necesaria para el desarrollo de los microservicios.

---

# Objetivos

* Crear el proyecto padre con Maven.
* Definir la estructura del repositorio.
* Configurar el servidor de configuración.
* Configurar el servidor Eureka Discovery.
* Configurar API Gateway.
* Documental la arquitectura inicial.
* Definir el modelo de dominio.

---

# Tareas completadas

## Configuración del proyecto

* Creación del proyecto Maven padre.
* Organización del repositorio.
* Definición de carpetas principales.

---

## Infraestructura

Se implementaron los siguientes componentes:

* Servidor de configuración
* Servidor de descubrimiento Eureka
* Puerta de enlace API

Los servicios fueron integrados correctamente y API Gateway quedó registrado en Eureka.

---

## Documentación

Se creó la documentación inicial del proyecto:

* LÉAME.md
* SISTEMA_ARQUITECTURA.md
  *DOMINIO_MODEL.md

También se preparó la estructura para los Architecture Decision Records (ADR).

---

# Tecnologías utilizadas

*Java 21
* experto
* Bota de primavera
* Nube de primavera
* Configuración de nube de primavera
* Servidor Eureka
* Puerta de enlace de la nube de primavera

---

# Entregables

* Infraestructura inicial completamente funcional.
* Arquitectura del sistema documentada.
* Modelo del dominio definido.
* Proyecto preparado para iniciar el desarrollo del Auth Service.

---

# Lecciones aprendidas

Durante este sprint se desarrolló la base arquitectónica del proyecto.

Se priorizó la planificación y documentación antes del desarrollo de la lógica de negocio con el objetivo de construir un sistema mantenible y escalable.

---

# Próximo sprint

Sprint 02 estará enfocado en el desarrollo del Servicio de Autenticación.

Las actividades principales serán:

* Implementar Spring Security.
* Registro de usuarios.
* Inicio de sesión.
  *JWT.
* Actualizar fichas.
* Roles y permisos.
* Integración con PostgreSQL.

## Métricas del sprint

| Metric                  |    Value |
|-------------------------|---------:|
| Duration                | 1 Sprint |
| Infrastructure Services |        3 |
| Business Services       |        0 |
| Documentation Files     |        4 |
| ADR Created             |        0 |
| Tests                   |        0 |