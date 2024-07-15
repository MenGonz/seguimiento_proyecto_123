# Plan de Implementación para la Web App Interactiva

## 1. Definición de la Arquitectura

### Frontend

- **Framework**: React.js o Vue.js para una interfaz de usuario dinámica e interactiva.
- **Bibliotecas**: Chart.js o D3.js para visualización de datos; Axios para llamadas a APIs.
- **Estilo**: Tailwind CSS o Material-UI para una apariencia moderna y responsiva.

### Backend

- **Servidor**: Node.js con Express.js para manejar solicitudes HTTP y APIs RESTful.
- **Autenticación y Autorización**: Auth0 para la gestión de usuarios y roles.
- **Seguridad**: HTTPS con certificados SSL para encriptar datos en tránsito.

### Base de Datos

- **Sistema de Gestión de Bases de Datos (DBMS)**: PostgreSQL para almacenamiento y consultas eficientes.
- **Modelo de Datos**: Esquema relacional con tablas optimizadas para análisis de productividad.

### ETL (Extract, Transform, Load)

- **Lenguaje**: Python con pandas para la manipulación de datos.
- **Orquestación**: Apache Airflow para gestionar y automatizar procesos ETL.
- **Fuentes de Datos**: APIs de Salesforce, archivos Excel y otras fuentes.

### Despliegue

- **Proveedor de Nube**: AWS para servicios escalables y gestionados.
- **Componentes**:
    - **EC2**: Para alojar el servidor backend.
    - **S3**: Para almacenamiento de archivos y backups.
    - **RDS**: Para la base de datos PostgreSQL.
    - **Lambda**: Para funciones serverless y procesamiento de datos.
    - **Route 53**: Para gestión de DNS y dominio.

## 2. Selección de Tecnologías

### Frontend

- **React.js** o **Vue.js**: Componentes reutilizables y estado centralizado.
- **Chart.js** o **D3.js**: Gráficos y visualizaciones interactivas.
- **Axios**: Para realizar solicitudes HTTP a las APIs del backend.
- **Tailwind CSS** o **Material-UI**: Estilos consistentes y responsivos.

### Backend

- **Node.js**: Plataforma ligera y eficiente.
- **Express.js**

<!-- Bugdet -->

# Optimistic Monthly Budget Estimate for the Interactive Web App

## AWS EC2 (Elastic Compute Cloud)

- **Instance t3a.small (2 vCPUs, 2 GB RAM)**: $17/month.
    - **Description**: Adequate for handling backend and frontend operations for a small number of users.
- **EBS (Elastic Block Store) Storage**: 20 GB at $0.10 per GB/month = $2/month.
- **Data Transfer Out**: 50 GB at $0.09 per GB = $4.50/month.

### Subtotal for EC2: $23.50/month

## AWS S3 (Simple Storage Service)

- **Storage**: 10 GB at $0.023 per GB/month = $0.23/month.
- **Data Transfer Out**: 10 GB at $0.09 per GB = $0.90/month.

### Subtotal for S3: $1.13/month

## AWS RDS (Relational Database Service)

- **Instance db.t3.small (2 vCPUs, 2 GB RAM)**: $21/month.
    - **Description**: Suitable for a small-scale production PostgreSQL database.
- **Storage**: 20 GB at $0.115 per GB/month = $2.30/month.
- **Data Transfer Out**: 50 GB at $0.09 per GB = $4.50/month.

### Subtotal for RDS: $27.80/month

## AWS Lambda (Serverless Functions)

- **Requests**: Assuming 1 million requests at $0.20 per million requests = $0.20/month.
- **Duration**: Assuming 100,000 GB-seconds at $0.00001667 per GB-second = $1.67/month.

### Subtotal for Lambda: $1.87/month

## Other Costs

- **AWS Route 53**: $0.50 per domain/month.
- **SSL Certificates**: Free with Let's Encrypt.

### Subtotal for Other Costs: $0.50/month

## Total Estimated Monthly Cost

- **EC2**: $23.50/month
- **S3**: $1.13/month
- **RDS**: $27.80/month
- **Lambda**: $1.87/month
- **Other Costs**: $0.50/month

### **Total: $54.80/month**