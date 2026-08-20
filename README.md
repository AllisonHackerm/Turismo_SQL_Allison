# Accommodation Tourism Database

## Descripción

**Accommodation Tourism Database** es una base de datos desarrollada en PostgreSQL para la gestión de alojamientos turísticos. Permite administrar propietarios, huéspedes, reservas, habitaciones, pagos, reseñas, ubicaciones y servicios disponibles en cada alojamiento.

El proyecto está diseñado para simular el funcionamiento de plataformas de hospedaje similares a Airbnb, Booking o Expedia, facilitando el control de información relacionada con establecimientos turísticos y sus procesos de reservación.

---

## Tecnologías Utilizadas

- PostgreSQL 14 o superior
- SQL (DDL y DML)
- PL/pgSQL
- Sistema de secuencias (SERIAL y SEQUENCE)
- Restricciones de integridad referencial

---

## Estructura de la Base de Datos

La base de datos contiene las siguientes tablas principales:

| Tabla | Descripción |
|---------|-------------|
| accommodation_types | Tipos de alojamiento |
| accommodations | Información de los alojamientos |
| amenities | Servicios disponibles |
| accommodation_amenities | Relación entre alojamientos y servicios |
| owners | Propietarios de alojamientos |
| locations | Ubicaciones |
| rooms | Habitaciones |
| guests | Huéspedes |
| bookings | Reservaciones |
| booking_guests | Acompañantes de una reserva |
| booking_statuses | Estados de las reservas |
| payments | Pagos realizados |
| reviews | Reseñas y valoraciones |
| staff_users | Usuarios administrativos |

---

## Características Principales

- Gestión de propietarios y alojamientos.
- Registro de huéspedes.
- Administración de habitaciones.
- Control de reservas y estados de reservación.
- Registro de pagos.
- Gestión de reseñas y calificaciones.
- Asociación de múltiples servicios a cada alojamiento.
- Control de ubicaciones geográficas.
- Actualización automática de registros mediante triggers.

---

## Instalación

### 1. Crear la base de datos

```sql
CREATE DATABASE accommodations_tourism
WITH TEMPLATE=template0
ENCODING='UTF8';
```

### 2. Ejecutar el script

```bash
psql -U postgres -d accommodations_tourism -f accommodation_database_restore.sql
```

---

## Relaciones Principales

- Un propietario puede tener varios alojamientos.
- Un alojamiento pertenece a una ubicación.
- Un alojamiento puede tener múltiples habitaciones.
- Un alojamiento puede poseer múltiples servicios.
- Un huésped puede realizar múltiples reservas.
- Una reserva puede generar pagos y reseñas.
- Cada reserva posee un estado específico.

---

## Datos Incluidos

El script incorpora registros de ejemplo para:

- Tipos de alojamiento.
- Servicios.
- Propietarios.
- Ubicaciones.
- Alojamientos.
- Reservas.
- Pagos.
- Habitaciones.
- Reseñas.

Estos datos permiten realizar pruebas y consultas inmediatamente después de restaurar la base de datos.

---

## Objetivo del Proyecto

Desarrollar una solución de base de datos robusta para la administración de alojamientos turísticos, facilitando el almacenamiento, consulta y gestión de información relacionada con reservas, huéspedes, propietarios y servicios.

---

## Autor

Proyecto académico desarrollado utilizando PostgreSQL como sistema gestor de bases de datos relacional.