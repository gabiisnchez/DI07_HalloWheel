# HalloWheel - Distribución y Despliegue de Aplicación JavaFX

Este repositorio contiene los archivos resultantes de la tarea práctica "Desarrollo y Distribución de una Aplicación", correspondiente al módulo de Desarrollo de Interfaces. El proyecto simula un ciclo profesional de entrega de software, partiendo de una aplicación JavaFX hasta obtener un instalador nativo para Windows.

## 📋 Descripción del Proyecto

**HalloWheel** es una aplicación de escritorio desarrollada en JavaFX. El objetivo de esta práctica ha sido empaquetar dicha aplicación para que pueda ser distribuida e instalada en cualquier equipo Windows, independientemente de si tiene Java instalado o no, garantizando una experiencia de usuario fluida y profesional.

## 📂 Estructura del Proyecto

A continuación se muestra la organización de los archivos en el directorio principal:

```text
DI07_HalloWheel/
├── mi_jre_ligero/                     # Entorno de ejecución Java (JRE) portable
├── resources/                         # Recursos gráficos y textos para el instalador
│   ├── config.xml                     # Configuración de Launch4j
│   ├── license.txt                    # Licencia mostrada en el instalador
│   ├── readme_before.txt              # Información previa a la instalación
│   ├── readme_final.txt               # Información post-instalación
│   └── *.ico                          # Iconos de la aplicación e instalador
├── DI05_TunelTerror-1.0-SNAPSHOT.jar  # Archivo Java original (Maven)
├── DI05_TunelTerror_App.exe           # Ejecutable nativo (Launch4j)
├── hallowheel_installer.exe           # Instalador final (Inno Setup)
├── hallowheel_script.iss              # Script de configuración del instalador
├── Memoria Técnica...pdf              # Documentación detallada del proceso
└── README.md                          # Este archivo
```

## 🚀 Contenido del Repositorio

Detalle de los archivos principales y su función en el ciclo de distribución:

### 1. Instalador Final (Entregable Principal)
*   **Archivo:** `hallowheel_installer.exe`
*   **Función:** Es el producto final para el usuario. Al ejecutarlo, inicia un asistente que instala la aplicación, copia los archivos necesarios (incluyendo el JRE), crea accesos directos en el Escritorio y Menú Inicio, y registra el desinstalador en el sistema.

### 2. Ejecutable Nativo
*   **Archivo:** `DI05_TunelTerror_App.exe`
*   **Herramienta:** Generado con **Launch4j**.
*   **Características:**
    *   Envuelve el archivo JAR para ejecutarse como un binario de Windows (`.exe`).
    *   Configurado para no mostrar la consola de comandos.
    *   Utiliza el JRE embebido en la carpeta `mi_jre_ligero` para asegurar la portabilidad.
    *   Icono personalizado de Halloween.

### 3. Script de Inno Setup
*   **Archivo:** `hallowheel_script.iss`
*   **Herramienta:** **Inno Setup Compiler**.
*   **Función:** Contiene todas las directivas necesarias para compilar el instalador. Define qué archivos copiar, dónde crear los accesos directos, los textos de licencia y la configuración del registro de Windows.

### 4. Archivo JAR
*   **Archivo:** `DI05_TunelTerror-1.0-SNAPSHOT.jar`
*   **Herramienta:** Generado con **Maven**.
*   **Estado:** Archivo base de la aplicación, verificada su ejecución mediante `java -jar`.

### 5. Documentación Técnica
*   **Archivo:** `Memoria Técnica_ Despliegue y Distribución de Aplicación JavaFX.pdf`
*   **Contenido:** Documento explicativo que detalla paso a paso el proceso seguido, las configuraciones utilizadas en Launch4j e Inno Setup, y las pruebas realizadas.

### 6. Recursos y Configuración (`/resources`)
Carpeta con los assets necesarios para la creación del instalador:
*   `config.xml`: Archivo de configuración de Launch4j.
*   `license.txt`, `readme_before.txt`, `readme_final.txt`: Archivos de texto mostrados durante la instalación.
*   `*.ico`: Iconos utilizados para el ejecutable y el instalador.

## ⚙️ Proceso de Desarrollo

El flujo de trabajo seguido para completar la tarea ha sido:

1.  **Generación del JAR:** Compilación y empaquetado del proyecto JavaFX asegurando la correcta gestión de dependencias.
2.  **Creación del EXE:** Uso de Launch4j para crear un lanzador `.exe` que integra el JAR y apunta a un JRE local, eliminando la dependencia de una instalación global de Java.
3.  **Creación del Instalador:** Configuración del script `.iss` en Inno Setup para generar un instalador profesional que gestiona la copia de archivos, creación de accesos directos y desinstalación limpia.
4.  **Personalización:** Se ha cuidado la estética del instalador con iconos propios, mensajes personalizados y una estructura clara.

## 👤 Autor
**Gabriel Sánchez Heredia**
---
*Proyecto realizado con fines educativos para el ciclo de Desarrollo de Aplicaciones Multiplataforma.*