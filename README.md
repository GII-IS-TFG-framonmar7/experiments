# Manual de Despliegue

Este manual de despliegue proporciona instrucciones paso a paso para reproducir los experimentos.

## Prerrequisitos

Antes de comenzar con el despliegue, se deben tener instalados los siguientes componentes en el sistema:

- **Python 3.11.9**: Para verificar la versión de Python hay que ejecutar `python --version` en la terminal.
- **Git**: Para verificar la instalación de Git hay que ejecutar `git --version` en la terminal.
- **Virtualenv (opcional)**: Se recomienda usar un entorno virtual para gestionar las dependencias de Python. Para instalar virtualenv puede ejecutar `pip install virtualenv`.

## Pasos para el Despliegue

### Paso 1: Clonar el Repositorio

1. Abra una terminal y ejecute el siguiente comando para clonar el repositorio de la aplicación:
    ```sh
    git clone https://github.com/GII-IS-TFG-framonmar7/experiments.git
    ```

2. Cambie al directorio del repositorio clonado:
    ```sh
    cd experiments
    ```

### Paso 2: Crear y Activar un Entorno Virtual (Opcional)

Se recomienda crear un entorno virtual para aislar las dependencias de la aplicación. Para crear y activar un entorno virtual, ejecute los siguientes comandos:

- En sistemas Windows:
    ```sh
    python -m venv ..\env
    ..\env\Scripts\activate
    ```
    
- En sistemas Unix o MacOS:
    ```sh
    python3 -m venv ../env
    source ../env/bin/activate
    ```

### Paso 3: Instalar las Dependencias

- Con el entorno virtual activado (si se utiliza), instale las dependencias requeridas por la aplicación ejecutando:
    ```sh
    pip install -r requirements.txt
    ```

### Paso 4: Descargar Pesos del Modelo YOLO

- Descargue los pesos del modelo YOLO ejecutando el siguiente comando:
    ```sh
    python .\commands\get_weights.py
    ```

Una vez completados los pasos, el siguiente sería correr los experimentos, que son los ficheros ipynb.