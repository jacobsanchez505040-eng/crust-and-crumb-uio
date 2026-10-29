# Crust & Crumb UIO 🥐

**Sistema Independiente de Auditoría y Ranking de Bollería Artesanal en Quito**

Crust & Crumb UIO es una aplicación web de página única (SPA) diseñada bajo un enfoque *Mobile-First* para la evaluación técnica, catalogación y ranking de croissants y bollería de alta gama en Quito y sus valles. Construida con una arquitectura **Zero-Backend**, la aplicación funciona de manera 100% local en el dispositivo del auditor, garantizando velocidad, privacidad y portabilidad de datos sin necesidad de servidores, bases de datos externas o conexión constante a internet.

## 🚀 Características Principales

* **Arquitectura Zero-Backend (IndexedDB):** Toda la información (calificaciones, textos y fotografías codificadas en Base64) se almacena de forma persistente en el navegador del usuario utilizando `IndexedDB`.
* **Interfaz Táctil a Una Mano:** Diseñada para trabajo de campo en cafeterías. Cuenta con selectores numéricos de toque rápido (Tap-Grid) para ingresar puntajes del 1 al 10 (con incrementos de 0.5) sin necesidad de abrir el teclado del teléfono.
* **Motor de Reglas Gastronómicas:** El código aplica reglas de negocio estrictas en tiempo real:
* Penalizaciones automáticas en el puntaje si se detecta uso de margarina.
* Descalificación automática de croissants salados.
* Requisito de justificación técnica obligatoria si un ítem de autor supera la barrera de los $4.00.


* **Procesamiento de Imágenes Cliente-Lado:** Captura o sube fotos directamente desde la interfaz. El sistema utiliza la `Canvas API` para redimensionar y comprimir las imágenes automáticamente antes de guardarlas en la base de datos local.
* **Generador de Instagram Stories:** Motor gráfico integrado que compila las puntuaciones, el veredicto final y las fotografías del croissant en un canvas oculto, exportando un archivo `.png` (1080x1920) con diseño editorial listo para publicar en redes sociales.
* **Comparador de Radar Biométrico:** Generación dinámica de gráficos de radar en formato `<svg>` puro (usando trigonometría en JavaScript) para comparar visualmente el rendimiento de dos panaderías frente a frente.
* **Portabilidad Total de Datos:** Funciones integradas para exportar la base de datos completa (incluyendo imágenes) a un archivo `.json` plano, y restaurarlo en cualquier otro dispositivo.

## 🛠️ Stack Tecnológico

La aplicación está construida sin *frameworks* ni librerías de terceros para garantizar un rendimiento óptimo, carga instantánea y longevidad del código.

* **Frontend:** HTML5 Semántico, CSS3 (Custom Properties, Grid, Flexbox, UI Responsivo).
* **Lógica y Estado:** Vanilla JavaScript (ES6+).
* **Almacenamiento:** Native `IndexedDB` API (vía API asíncrona transaccional).
* **Gráficos & Exportación:** HTML5 `<canvas>` API, `<svg>` en línea.
* **Alojamiento:** Preparado para GitHub Pages (Static Hosting).

## 📋 Protocolo de Evaluación (Categorías)

El sistema soporta una base de datos de 38 establecimientos pre-cargados y los evalúa bajo tres métricas sobre 40 puntos cada una:

1. **Classic Croissant:** Evalúa *Crujiente (10)*, *Alveolado (10)*, *Sabor (10)* y *Aspecto (10)*. Búsqueda de la técnica tradicional francesa.
2. **Croissant Relleno:** Evalúa *Textura Interna (10)*, *Distribución (10)*, *Balance de Sabor (10)* y *Presentación (10)*. El relleno no debe colapsar la masa base.
3. **Novelty Item (Ítem de Autor):** Evalúa *Textura Perfecta (10)*, *Cobertura/Topping (10)*, *Diseño/Estructura (10)* y *Sabor Principal (10)*. Ejemplos: New York Rolls, Pain au Chocolat, Pain Suisse. (Sustituible por un segundo croissant relleno si el local no califica).

## 💻 Instalación y Uso

Dado que es una aplicación estática, no se requiere configuración de entorno, compilación (build steps) ni instalación de dependencias (`npm`).

1. Clona este repositorio:
```bash
git clone https://github.com/TU_USUARIO/crust-and-crumb-uio.git

```


2. Abre la carpeta del proyecto.
3. Asegúrate de tener la carpeta `/assets` en la raíz con las 5 imágenes editoriales de muestra (`puro-exterior.png`, `puro-interior.png`, `relleno-exterior.png`, `relleno-interior.png`, `nyrolls.png`, `painauchocolat.png`, `noveltyej1.png`).
4. Abre el archivo `index.html` en cualquier navegador web moderno (Safari, Chrome, Firefox, Edge).
5. Para uso óptimo, abre la URL alojada desde tu iPhone y selecciona **"Agregar a la pantalla de inicio"** (Add to Home Screen) para utilizarla como una App Nativa (Web App Capable).

## 📂 Respaldo de Datos (Backup)

Para mover tus evaluaciones de un dispositivo a otro (ej. del iPhone a tu PC de escritorio):

1. Ve a la pestaña **Data** en la aplicación.
2. Haz clic en **"Descargar Respaldo JSON"**. Esto generará y descargará un archivo `crust-crumb-backup-YYYY-MM-DD.json`.
3. Envía ese archivo a tu otro dispositivo.
4. En el nuevo dispositivo, ve a la pestaña **Data**, haz clic en **"Restaurar"** y selecciona el archivo `.json`. La aplicación se sincronizará automáticamente.

## 📄 Licencia

Este proyecto es de uso personal y editorial para la catalogación gastronómica. El código fuente está abierto para inspección y uso académico/portafolio.
