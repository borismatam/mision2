# Proyecto Misión 2 — Clasificador de Flores (IA)

Este proyecto corresponde a la práctica de desarrollo, control de versiones y colaboración con Git/GitHub del Módulo 2. Contiene una implementación base de un modelo de clasificación con el dataset Iris (usando scikit-learn), organizada de forma modular para ejercitar buenas prácticas de código, pruebas unitarias y flujo de trabajo en equipo.

---

## 📁 Estructura del Proyecto

A continuación se detalla la organización de los directorios y archivos:

```text
proyecto-mision-2/
│
├── codigo/                 # Directorio para scripts y utilidades de soporte adicionales
├── datos/                  # Directorio destinado al almacenamiento de datasets y datos locales
├── notebooks/              # Cuadernos Jupyter para exploración, análisis y prototipado
├── proyecto.py             # Script principal en la raíz (punto de entrada general)
├── README.md               # Documentación general del repositorio y guía de comandos
│
└── proyecto_ia/            # Módulo principal del proyecto de Machine Learning
    ├── .gitignore          # Reglas de exclusión de archivos temporales y entornos
    ├── README.md           # Documentación específica del submódulo IA
    ├── requirements.txt    # Dependencias del proyecto (scikit-learn, etc.)
    │
    ├── src/                # Código fuente del clasificador
    │   ├── __init__.py     # Inicializador de paquete Python
    │   ├── metricas.py     # Funciones auxiliares para cálculo y evaluación de métricas
    │   └── predictor.py    # Entrenamiento del modelo base y generación de predicciones
    │
    └── tests/              # Pruebas unitarias
        └── test_metricas.py # Tests automatizados para las métricas del modelo
```

---

## ⚙️ Instalación y Configuración del Entorno

Para configurar el entorno de ejecución, sitúate en la carpeta `proyecto_ia` o en la raíz:

1. **Crear el entorno virtual de Python**:
   ```bash
   python -m venv .venv
   ```

2. **Activar el entorno virtual**:
   - En **Windows PowerShell**:
     ```powershell
     .venv\Scripts\Activate.ps1
     ```
   - En **Linux / macOS**:
     ```bash
     source .venv/bin/activate
     ```

3. **Instalar dependencias**:
   ```bash
   pip install -r proyecto_ia/requirements.txt
   ```

---

## 🚀 Comandos de Ejecución y Pruebas

Una vez activado el entorno virtual y ubicándote dentro de la carpeta `proyecto_ia`:

- **Ejecutar el modelo predictor**:
  ```bash
  python -m src.predictor
  ```

- **Lanzar la suite de pruebas unitarias**:
  ```bash
  python -m unittest discover -s tests -v
  ```

---

## 🛠️ Guía Rápida de Comandos Básicos de Git

A continuación se resumen los comandos esenciales de Git para trabajar en el proyecto de forma individual y en equipo:

### 1. Configuración Inicial (`settings / config`)
Configura tu identidad (nombre y correo electrónico) antes de realizar commits. Esta configuración quedará asociada a tus aportaciones.

```bash
# Definir tu nombre de usuario global
git config --global user.name "Tu Nombre"

# Definir tu correo electrónico global
git config --global user.email "tu_email@ejemplo.com"

# Comprobar la configuración actual
git config --list
```

### 2. Clonar un Repositorio (`clone`)
Descarga una copia exacta de un repositorio remoto en tu máquina local.

```bash
git clone https://github.com/borismatam/mision2.git
```

### 3. Consultar Estado y Preparar Cambios (`status` & `add`)
Permite ver qué archivos se han modificado y agregarlos al área de preparación (*staging area*).

```bash
# Ver el estado de la rama actual y los archivos modificados / sin seguimiento
git status

# Añadir un archivo específico al área de preparación
git add nombre_archivo.py

# Añadir todos los archivos modificados y nuevos al área de preparación
git add .
```

### 4. Confirmar Cambios (`commit`)
Registra de forma permanente los cambios preparados en el historial del repositorio con un mensaje descriptivo.

```bash
git commit -m "feat: descripción breve y clara del cambio realizado"
```

### 5. Gestión de Ramas (`branch` & `switch/checkout`)
Trabajar con ramas permite desarrollar nuevas características (`features`) o corregir errores sin afectar la rama principal.

```bash
# Listar todas las ramas locales (la activa se marcará con un asterisco *)
git branch

# Crear una nueva rama
git branch nombre-de-la-rama

# Cambiar a una rama existente
git checkout nombre-de-la-rama
# (O con el comando moderno):
git switch nombre-de-la-rama

# Crear una nueva rama y cambiarte a ella inmediatamente
git checkout -b feature/nueva-funcionalidad
# (O con el comando moderno):
git switch -c feature/nueva-funcionalidad

# Eliminar una rama local (cuando ya fue fusionada)
git branch -d nombre-de-la-rama
```

### 6. Descargar y Subir Cambios (`pull` & `push`)
Permite sincronizar tu repositorio local con el repositorio remoto (GitHub).

```bash
# Descargar y fusionar los últimos cambios del repositorio remoto a tu rama local
git pull

# Si es una rama específica del remoto:
git pull origin main

# Subir tus commits locales al repositorio remoto por primera vez (asociando seguimiento -u)
git push -u origin feature/nueva-funcionalidad

# Subir los cambios posteriores en la rama actual
git push
```

### 7. Otros Comandos
- **`git log --oneline`**: Muestra el historial reciente de commits en formato compacto de una sola línea.
- **`git diff`**: Muestra las diferencias exactas de código pendientes de preparación.
- **`git fetch`**: Descarga la información del repositorio remoto sin mezclarla automáticamente con tu código de trabajo.
- **`git merge <rama>`**: Fusiona los cambios de la rama indicada dentro de la rama activa.
