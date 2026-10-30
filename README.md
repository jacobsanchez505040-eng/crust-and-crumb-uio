# Crust & Crumb UIO 🥐

**Sistema Independiente de Auditoría y Ranking de Bollería Artesanal en Quito.**

Crust & Crumb UIO es una Aplicación Web Progresiva (PWA) de página única, diseñada bajo un enfoque *Mobile-First*, dedicada a la evaluación técnica, catalogación y ranking de croissants y bollería de alta gama en la ciudad de Quito y sus valles. Construida con una arquitectura **Zero-Backend**, la aplicación funciona de manera 100% local en el dispositivo del auditor, garantizando velocidad, privacidad absoluta y portabilidad de datos sin necesidad de servidores externos ni conexión constante a internet.

---

## 🚀 Características Principales

*   **Arquitectura Zero-Backend (IndexedDB):** Toda la información (calificaciones de 0 a 10, textos, estados y fotografías codificadas en Base64) se almacena de forma persistente directamente en el navegador del usuario.
*   **Interfaz Táctil a Una Mano (Tap-Grid):** Diseñada para trabajo de campo. Cuenta con selectores numéricos de toque rápido del 0 al 10 (con incrementos de 0.5) para ingresar puntajes sin necesidad de abrir el teclado del teléfono.
*   **Filtro Geográfico ("📍 Cerca de mí"):** Utiliza la API de Geolocalización (HTML5) y la fórmula de Haversine para ordenar instantáneamente el catálogo de panaderías según la proximidad del usuario en kilómetros.
*   **La Ruleta del Auditor:** Un sistema de gamificación que elige aleatoriamente un local en estado "Pendiente" para resolver la fatiga de decisión sobre qué panadería visitar en el día.
*   **Modo Oscuro "Editorial Night":** Un tema visual alternativo de alta gama (Ink-black y dorado) que relaja la vista y resalta las fotografías de los productos. Guarda la preferencia en el almacenamiento local.
*   **Comparador "Modo Versus":** Enfrenta a dos panaderías asalto por asalto, generando un gráfico de polígono (Radar SVG) mediante trigonometría en JavaScript y emitiendo un veredicto técnico automático.
*   **El "Wrapped" del Auditor:** Motor gráfico integrado (`Canvas API`) que compila las puntuaciones, inversión total acumulada, alertas de margarina y fotografías del líder absoluto en un póster `.png` (1080x1920) listo para exportar y publicar en Instagram Stories.
*   **Sistema de Mención Honorífica (Bonus Track):** Categoría aislada matemáticamente del ranking oficial para documentar joyas gastronómicas fuera de concurso (postres, café de especialidad, galletería), con su propio Podio de clasificaciones.
*   **Portabilidad de Datos:** Funciones integradas para descargar la base de datos completa en un archivo `.json` y restaurarla en cualquier otro dispositivo.

---

## 🛠️ Stack Tecnológico

La aplicación está construida utilizando tecnologías web nativas, sin depender de *frameworks* pesados (como React o Angular), garantizando un rendimiento óptimo y carga instantánea.

*   **Frontend:** HTML5 Semántico, CSS3 (Custom Properties, Flexbox, CSS Grid) y utilidades de Tailwind CSS inyectadas vía CDN.
*   **Lógica y Estado:** Vanilla JavaScript (ES6+).
*   **Almacenamiento Local:** API de `IndexedDB` nativa del navegador.
*   **Gráficos & Exportación:** Manipulación dinámica del DOM para SVG y renderizado offline mediante `HTML5 Canvas`.
*   **Distribución:** Web App Manifest (PWA) compatible con iOS (Safari) y Android (Chrome) para instalación directa en la pantalla de inicio.
*   **Alojamiento:** GitHub Pages (Static Hosting).

---

## 📋 Metodología y Protocolo de Evaluación

El ranking se compone de un catálogo cerrado de **40 establecimientos**, evaluados rigurosamente sobre un máximo de **40 puntos** bajo tres categorías oficiales:

1.  **Classic Croissant (Puro):** Evaluación de la autenticidad tradicional (Crujiente, Alveolado, Sabor a Mantequilla, Aspecto).
2.  **Croissant Relleno:** Evaluación del equilibrio técnico entre la masa hojaldrada y el relleno (humedad, distribución, balance). *Los croissants salados incurren en descalificación inmediata.*
3.  **Novelty Item (De Autor):** Innovación vienesa (NY Rolls, Pain Suisse, Pain au Chocolat). Restringido a ítems de un valor máximo sugerido de $4.00.

---

## 📱 Instalación (Como PWA en iOS/Android)

Al ser una aplicación web progresiva, no requiere descargas desde la App Store ni Google Play.

1.  Abre el navegador web de tu dispositivo móvil (Safari en iOS, Chrome en Android).
2.  Visita la URL de despliegue oficial: `https://[tu-usuario].github.io/crust-and-crumb-uio/`
3.  **En iOS (Safari):** Toca el ícono de "Compartir" en la barra inferior y selecciona **"Agregar a la pantalla de inicio"**.
4.  **En Android (Chrome):** Toca el menú de tres puntos en la esquina superior derecha y selecciona **"Instalar aplicación"** o **"Agregar a la pantalla de inicio"**.
5.  Inicia la aplicación desde el ícono de tu escritorio; a partir de este momento, funciona offline.

---

## 💻 Desarrollo Local

Para correr o modificar el proyecto en tu máquina local:

1.  Clona el repositorio:
    
```bash
    git clone [https://github.com/jacobsanchez505040-eng/crust-and-crumb-uio.git](https://github.com/jacobsanchez505040-eng/crust-and-crumb-uio.git)

🖋️ Créditos

Diseño, Desarrollo y Auditoría: Jacob Sánchez.An Independent Ranking.
