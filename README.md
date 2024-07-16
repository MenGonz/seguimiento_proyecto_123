

# Introducción
Esta idea de implementación es simple, moderna, y minimiza muchísimo los costos mediante el uso mayoritario de herramientas open source. El despliegue del proyecto es lo único que requeriría dinero. Y aún así se logra minimizar el costo mediante el uso de herramientas de AWS, que son herramientas por excelencia de tipo "cobro por uso". Es una idea escalable, fácilmente trabajable y las herramientas usadas tienen todas una curva de aprendizaje pronunciada.


# Plan de Implementación
## 1. Idea de la Arquitectura
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

## 2. Selección de Tecnologías o Librerías
### Frontend

- **React.js** o **Vue.js**: Componentes reutilizables y estado centralizado.
- **Chart.js** o **D3.js**: Gráficos y visualizaciones interactivas.
- **Axios**: Para realizar solicitudes HTTP a las APIs del backend.
- **Tailwind CSS** o **Material-UI**: Estilos consistentes y responsivos.

### Backend

- **Node.js**: Plataforma ligera y eficiente.
- **Express.js**

# Presupuesto Mensual Estimado

| Servicio        | Descripción                                        | Coste Mensual |
|-----------------|----------------------------------------------------|---------------|
| **AWS EC2**     | Instancia t3a.small (2 vCPUs, 2 GB RAM)            | $17.00        |
|                 | Almacenamiento EBS (20 GB)                         | $2.00         |
|                 | Transferencia de Datos Saliente (50 GB)            | $4.50         |
| **AWS S3**      | Almacenamiento (10 GB)                             | $0.23         |
|                 | Transferencia de Datos Saliente (10 GB)            | $0.90         |
| **AWS RDS**     | Instancia db.t3.small (2 vCPUs, 2 GB RAM)          | $21.00        |
|                 | Almacenamiento (20 GB)                             | $2.30         |
|                 | Transferencia de Datos Saliente (50 GB)            | $4.50         |
| **AWS Lambda**  | Solicitudes (1 millón de solicitudes)              | $0.20         |
|                 | Duración (100,000 GB-segundos)                     | $1.67         |
| **Otros Costos**| AWS Route 53                                       | $0.50         |
|                 | Certificados SSL (Let's Encrypt)                   | $0.00         |
| **Total**       |                                                    | **$54.80**    |
