---
title: markmap
markmap:
  colorFreezeLevel: 2
---
# Flujo de Datos en SAP BW

## 1. Fuente de Datos (DataSource)
- **Definición**: Origen de datos a extraer para cargar en BW.
- **Tipos**:
  - Sistema SAP ERP
  - Archivos planos (CSV, Excel)
  - Sistemas externos
- **Creación**:
  - Definir la DataSource en el sistema fuente.
  - Especificar las características a extraer.
  - Replicar la DataSource en el sistema BW.

## 2. InfoObjects (Características y Métricas)
- **Definición**: Elementos básicos de almacenamiento y definición de datos.
- **Tipos**:
  - Características (e.g., Cliente, Producto)
  - Métricas (e.g., Cantidad Vendida, Ingreso)
- **Creación**:
  - Definir InfoObjects necesarios en BW.
  - Reutilizar en ADSO y otros objetos.

## 3. Advanced DataStore Object (ADSO)
- **Definición**: Contenedor de datos para almacenar y procesar información.
- **Tipos**:
  - Staging
  - Almacenamiento histórico
  - Reporting
- **Creación**:
  - Definir la estructura con InfoObjects.
  - Configurar tipo de ADSO (Inbound, Active, Change Log).

## 4. Transformación
- **Definición**: Mapea campos de DataSource a ADSO, realiza conversiones.
- **Creación**:
  - Crear transformación entre DataSource y ADSO.
  - Definir reglas de asignación.
  - Agregar reglas para cálculos y mapeos.

## 5. Data Transfer Process (DTP)
- **Definición**: Carga datos desde la DataSource al ADSO.
- **Tipos**:
  - Full Load (Carga completa)
  - Delta Load (Carga incremental)
- **Creación**:
  - Crear DTP entre DataSource y ADSO.
  - Configurar tipo de carga y filtros.

## 6. Carga de Datos (Data Load)
- **Definición**: Ejecutar DTP para transferir datos.
- **Proceso**:
  - Ejecutar el DTP.
  - Validar la transferencia al ADSO.
  - Verificar tablas internas del ADSO (Inbound, Active, Change Log).

## 7. CompositeProvider (Opcional)
- **Definición**: Combina ADSOs y otros objetos para vistas virtuales.
- **Creación**:
  - Definir ADSOs y objetos del CompositeProvider.
  - Configurar uniones (joins) y uniones lógicas (unions).
  - Utilizar como fuente en la capa de reporting.

## 8. Capa de Reporting (Queries)
- **Definición**: Crea queries para visualizar datos en herramientas de análisis.
- **Creación**:
  - Utilizar queries en BW para definir datos y métricas.
  - Diseñar consultas para usuarios finales.
  - Consumir datos con SAP Analysis for Office o SAP Analytics Cloud.
