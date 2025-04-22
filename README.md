# Inventario_Nube_AWS
Es mi proyecto final de kubernetes donde haré un pequeño proyecto sobre la implementación de kubernetes.


Gestión de Inventario en la Nube con DevOps
Este proyecto tiene como objetivo desarrollar una solución escalable para la gestión de inventario en la nube, utilizando una arquitectura basada en microservicios y tecnologías modernas de DevOps. La infraestructura inicial se implementó con Terraform para la provisión de recursos en AWS, Ansible para la automatización de configuraciones y Vault para la gestión segura de secretos. Posteriormente, se evoluciona el proyecto incorporando contenedorización (Docker), orquestación con Kubernetes (Amazon EKS) y monitoreo a través de Prometheus y Grafana.

Tabla de Contenidos
Descripción del Proyecto

Tecnologías Utilizadas

Arquitectura y Estructura del Proyecto

Requisitos e Instrucciones de Instalación

Despliegue y Automatización (CI/CD)

Monitoreo y Observabilidad

Control de Versiones y Flujo de Trabajo

Contribuciones

Licencia

Descripción del Proyecto
El proyecto ofrece una solución para la gestión de inventarios en tiempo real, adaptándose a las necesidades de empresas que requieren escalabilidad, confiabilidad y monitoreo constante. La solución se compone de múltiples servicios que se ejecutan en contenedores, gestionados y orquestados con Kubernetes, permitiendo:

Empaquetado de servicios en contenedores: Utilizando Docker para contenerizar cada módulo (backend, frontend, API, base de datos, etc.).

Orquestación y despliegue: Mediante Amazon Elastic Kubernetes Service (EKS) para gestionar el ciclo de vida de los contenedores.

Monitoreo: A través de Prometheus y Grafana para recolectar métricas y visualizar el estado de la infraestructura y los servicios.

Tecnologías Utilizadas
Infraestructura y Automatización:

Terraform

Ansible

Vault

Contenedores y Orquestación:

Docker

Kubernetes (Amazon EKS)

Monitoreo:

Prometheus

Grafana

CI/CD y Control de Versiones:

GitHub (repositorio privado)

GitHub Actions

Servicios en la Nube:

AWS EC2, RDS, S3, Cognito, CloudWatch, SNS, ElastiCache, QuickSight, Lambda

Arquitectura y Estructura del Proyecto
La solución está diseñada de manera modular, con cada componente desplegado en contenedores de Docker. La estructura del proyecto se organiza de la siguiente manera:

rust
Copiar
Editar
/backend         
->
 Código del servicio 
backend
 (API, lógica de negocio).
/frontend        
->
 Código del servicio 
frontend
 (interfaz de usuario).
/deploy          
->
 Archivos de despliegue para 
Kubernetes
 (manifiestos YAML).
/terraform       
->
 Código para aprovisionamiento de la infraestructura en AWS.
/ansible         
->
 Playbooks para la configuración de 
entornos
 (opcional en esta versión).
.github/workflows
->
 Archivos de configuración para GitHub 
Actions
 (CI/CD).
README.md        
->
 Documentación general del proyecto.
Requisitos e Instrucciones de Instalación
Requisitos Previos
Cuenta en GitHub y AWS.

Docker instalado.

Kubectl instalado y configurado.

AWS CLI configurado.

Acceso a un clúster de Amazon EKS (puedes crearlo usando Terraform).

Pasos para Clonar y Configurar el Proyecto
Clonar el Repositorio:

bash
Copiar
Editar
git 
clone
 https://github.com/tuusuario/inventario-devops.git
cd
 inventario-devops
