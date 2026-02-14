# Requerimientos del Sistema — Alcance (scope.md)

Ruta: DOSW-Laboratorio4/docs/requirements/scope.md

## 1. Sistema

- **Nombre del sistema:** Bankify
- **Objetivo:** Proveer un sistema básico para la gestión de cuentas bancarias que permita a clientes finales consultar saldos, realizar depósitos y generar reportes tributarios; además centralizar evidencias y documentación del laboratorio.

## 2. Problema a resolver

Actualmente Bankify no cuenta con un sistema centralizado que permita:

- Registrar cuentas bancarias de manera validada.
- Consultar el saldo de una cuenta.
- Realizar depósitos de dinero de forma controlada.
- Generar reportes tributarios en PDF para clientes.
- Enviar reportes a la DIAN en formato JSON.

El objetivo es crear una versión inicial que cumpla las reglas de negocio básicas y permita validar el modelo antes de escalar a funcionalidades más complejas.

## Reglas de negocio generales

- Los números de cuenta deben tener exactamente 10 dígitos; solo números, sin caracteres especiales.
- Los dos primeros dígitos del número de cuenta representan el banco (ej.: `01` -> Bancolombia, `02` -> Davivienda).
- Una cuenta solo es válida si pertenece a un banco registrado en el sistema.

## 3. Diagrama de contexto

### 3.1 Diagrama

Adjunte la imagen del diagrama de contexto en `docs/uml/Diagrama de Contexto.png` y actualice esta sección para referenciarla.

### 3.2 Actores

| Actor / Rol | Descripción |
|-------------|-------------|
| Usuario final | Cliente del sistema Bankify que consulta saldos y realiza depósitos. |
| Operador / Supervisor | Personal autorizado para gestionar clientes y cuentas. |
| Gerente financiero | Genera y envía reportes tributarios para la DIAN. |

### 3.3 Sistemas externos

| Sistema | Descripción |
|--------:|-------------|
| Repositorio GitHub | Aloja el código fuente y artefactos del proyecto. |
| Servicio de CI (opcional) | Ejecuta compilaciones y pruebas automatizadas. |
| Servicio de generación de PDFs | Produce reportes tributarios en PDF para clientes. |
| Servicio DIAN (export) | Endpoint al que se envían reportes en formato JSON. |

## 4. Alcance del sistema

### 4.1 Dentro del sistema (Funciones que el sistema SÍ realiza)

1. Autenticación con usuario y contraseña para operadores y clientes.
2. Gestión de clientes: crear, activar, inactivar y actualizar información por roles autorizados.
3. Gestión de cuentas: crear, activar, inactivar y actualizar cuentas bancarias; validar número de cuenta y banco asociado.
4. Consultar saldo de cuentas por parte del cliente.
5. Realizar depósitos a una cuenta por parte del cliente u otros usuarios.
6. Generar reportes tributarios en PDF para clientes.
7. Exportar reportes en formato JSON para integración con DIAN.
8. Eliminar un cliente y las cuentas asociadas cuando aplique.

### 4.2 Fuera del sistema (Funciones que NO realiza)

1. No gestiona infraestructura de despliegue en producción (p. ej. provisioning en la nube).
2. No procesa pasarelas de pago externas ni conciliaciones avanzadas.
3. No gestiona notificaciones masivas (solo soporte para exportar datos a servicios externos).

## 5. Notas y evidencias

- Para el Diagrama de Contexto copie la imagen a `docs/uml/Diagrama de Contexto.png` y referencia aquí.

**Autor:** Juan Silva, Laura Castillo, Kevin Cuitiva
**Fecha:** 2026-02-14

