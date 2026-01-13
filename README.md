# HalloWheel - Distribución y Despliegue de Aplicación JavaFX

Este repositorio contiene los archivos resultantes de la tarea práctica "Desarrollo y Distribución de una Aplicación", correspondiente al módulo de Desarrollo de Interfaces. El proyecto simula un ciclo profesional de entrega de software, partiendo de una aplicación JavaFX hasta obtener un instalador nativo para Windows.

## 📋 Descripción del Proyecto

**HalloWheel** es una aplicación de escritorio desarrollada en JavaFX. El objetivo de esta práctica ha sido empaquetar dicha aplicación para que pueda ser distribuida e instalada en cualquier equipo Windows, independientemente de si tiene Java instalado o no, garantizando una experiencia de usuario fluida y profesional.

## 🚀 Contenido del Repositorio

A continuación se detallan los archivos principales y su correspondencia con los requisitos de la tarea:

### 1. Instalador Final (Entregable Principal)
*   **Archivo:** `HalloWheel_installer.exe`
*   **Función:** Es el producto final para el usuario. Al ejecutarlo, inicia un asistente que instala la aplicación, copia los archivos necesarios (incluyendo el JRE), crea accesos directos en el Escritorio y Menú Inicio, y registra el desinstalador en el sistema.

### 2. Ejecutable Nativo
*   **Archivo:** `DI05_TunelTerror_App.exe`
*   **Herramienta:** Generado con **Launch4j**.
*   **Características:**
    *   Envuelve el archivo JAR para ejecutarse como un binario de Windows (`.exe`).
    *   Configurado para no mostrar la consola de comandos.
    *   Utiliza el JRE embebido en la carpeta `mi_jre_ligero` para asegurar la portabilidad.
    *   Icono personalizado de Halloween.

### 3. Archivo JAR
*   **Archivo:** `DI05_TunelTerror-1.0-SNAPSHOT.jar`
*   **Herramienta:** Generado con **Maven**.
*   **Estado:** Archivo base de la aplicación, verificada su ejecución mediante `java -jar`.

### 4. Documentación Técnica
*   **Archivo:** `Memoria Técnica_ Despliegue y Distribución de Aplicación JavaFX.pdf`
*   **Contenido:** Documento explicativo que detalla paso a paso el proceso seguido, las configuraciones utilizadas en Launch4j e Inno Setup, y las pruebas realizadas.

### 5. Recursos y Configuración (`/resources`)
Carpeta con los assets necesarios para la creación del instalador:
*   `hallowheel_setup_script.iss`: Script de **Inno Setup** utilizado para compilar el instalador.
*   `config.xml`: Archivo de configuración de Launch4j.
*   `license.txt`, `readme_before.txt`, `readme_final.txt`: Archivos de texto mostrados durante la instalación.
*   `*.ico`: Iconos utilizados para el ejecutable y el instalador.

## ⚙️ Proceso de Desarrollo

El flujo de trabajo seguido para completar la tarea ha sido:

1.  **Generación del JAR:** Compilación y empaquetado del proyecto JavaFX asegurando la correcta gestión de dependencias.
2.  **Creación del EXE:** Uso de Launch4j para crear un lanzador `.exe` que integra el JAR y apunta a un JRE local, eliminando la dependencia de una instalación global de Java.
3.  **Creación del Instalador:** Configuración de un script en Inno Setup para generar un instalador profesional que gestiona la copia de archivos, creación de accesos directos y desinstalación limpia.
4.  **Personalización:** Se ha cuidado la estética del instalador con iconos propios, mensajes personalizados y una estructura clara.

## 👤 Autor
**Gabriel Sánchez Heredia**
Desarrollo de Interfaces

---
*Proyecto realizado con fines educativos para el ciclo de Desarrollo de Aplicaciones Multiplataforma.*