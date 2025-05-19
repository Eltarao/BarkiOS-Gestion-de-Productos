# BarkiOS-Gestion-de-Productos
Modulo funcional crud para la asignacion de programación

![Docker](https://img.shields.io/badge/Docker-✓-blue?logo=docker)  
![PHP](https://img.shields.io/badge/PHP-8.2-777BB4?logo=php)  
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql)  

## 📌 Tabla de Contenidos  
- [Descripción](#-descripción)  
- [Tecnologías](#-tecnologías)  
- [Instalación](#-instalación)  
- [Estructura](#-estructura-del-proyecto)  
- [Uso](#-uso)  
- [Despliegue](#-despliegue)   
- [Licencia](#-licencia)  

## 🌟 Descripción  
**BarkiOS** es un sistema completo para la gestión de tiendas de ropa que incluye:  

- 🛒 Plataforma de e-commerce  
- 📦 Gestión de productos


## 🛠️ Tecnologías  
```plaintext
Backend: PHP 8.2 + Composer  
Frontend: Bootstrap 5 + Vanilla JS  
Base de datos: MySQL 8.0  
Infraestructura: Docker + Apache  
Herramientas: phpMyAdmin, Beekeeper Studio  
```  

## 💻 Instalación  

### Requisitos  
```powershell
# Verificar instalación de Docker
docker --version
docker-compose --version
```

### Pasos  
1. Clonar repositorio  
2. Configurar entorno:  
   ```powershell
   cp .env.example .env
   ```  
3. Iniciar contenedores:  
   ```powershell
   docker-compose up -d --build
   ```  

## 📂 Estructura del Proyecto  
```bash
BarkiOS/  
├── app/  
│   ├── Controllers/  # Lógica de negocio  
│   ├── Models/       # Entidades de DB  
│   └── Views/        # Plantillas Twig  
├── config/           # Archivos de configuración  
├── public/           # Punto de entrada  
└── docker/           # Configuración de contenedores  
```  

## 🖥️ Uso  
**Accesos después de instalación:**  
```plaintext
URL: http://localhost:8080  
phpMyAdmin: http://localhost:8000 (root/root)  
```  

**Comandos útiles:**  
```powershell
# Ejecutar migraciones
docker-compose exec app php migrations.php

# Ver logs
docker-compose logs -f app
```  

## 🚢 Despliegue  
1. Configurar dominio en `.env`  
2. Optimizar autoload:  
   ```powershell
   composer dump-autoload -o
   ```  

## 📜 Licencia  
MIT License - Ver [LICENSE](LICENSE) para detalles.  

---  
*Documentación generada para el equipo de desarrollo BarkiOS*
