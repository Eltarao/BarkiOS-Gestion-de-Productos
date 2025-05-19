# 👔 BarkiOS - Sistema de Gestión de Productos (Docker + XAMPP)  

![Docker](https://img.shields.io/badge/Docker-✓-blue?logo=docker)  
![XAMPP](https://img.shields.io/badge/XAMPP-Compatible-FB7A24?logo=xampp)  
![PHP](https://img.shields.io/badge/PHP-8.2-777BB4?logo=php)  
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql)  


## 📌 Tabla de Contenidos  
- [Descripción](#-descripción)  
- [Tecnologías](#-tecnologías)  
- [Instalación con Docker](#-instalación-con-docker)  
- [Instalación con XAMPP](#-instalación-con-xampp)  
- [Estructura](#-estructura-del-proyecto)  
- [Uso](#-uso)   
- [Licencia](#-licencia)  

## 🛠️ Tecnologías  
```plaintext
Backend: PHP 8.2 + Composer  
Frontend: Bootstrap 5 + Vanilla JS  
Base de datos: MySQL 8.0  
Entornos: Docker (producción) | XAMPP (desarrollo)  
Herramientas: phpMyAdmin (ambos entornos)  
```  

## 🐳 Instalación con Docker  

### Requisitos  
```powershell
docker --version
docker-compose --version
```

### Pasos  
1. Clonar repositorio (rama main):  
   ```bash
   git clone git@github.com:Eltarao/BarkiOS-Gestion-de-Productos.git
   ```  
2. Configurar entorno:  
   ```powershell
   cp .env.example .env
   ```  
3. Iniciar contenedores:  
   ```powershell
   docker-compose up -d --build
   ```
3. Importar DB:  
   ```sql
   source database/barkios_db(backup 19-05-2025).sql
   ``` 

## 🛠️ Instalación con XAMPP  

### Requisitos  
- XAMPP 8.2+  
- MySQL 8.0  

### Pasos  
1. Clonar rama xampp:  
   ```bash
   git clone -b git@github.com:Eltarao/BarkiOS-Gestion-de-Productos.git
   ```  
2. Mover proyecto a `htdocs`  
3. Importar DB:  
   ```sql
   source database/productos.sql
   ```  
4. Configurar `config/database.php`  
  

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
Docker
```plaintext
http://localhost:9080/app/views/admin/products-admin.php
```
Xampp
```plaintext
http://localhost/BarkiOS-Gestion-de-Productos/app/views/admin/products-admin.php
```  

## 📜 Licencia  
MIT License - Ver [LICENSE](LICENSE) para detalles.  

---  
*Documentación generada para el equipo de desarrollo BarkiOS*
