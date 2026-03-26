Automated AI Content Publisher (n8n + Ollama + WordPress)
Este proyecto es un sistema de automatización de ciclo completo que transforma datos estructurados de eventos en artículos de prensa profesionales, utilizando IA local para la generación de contenido y la REST API de WordPress para la distribución dinámica.

🚀 Arquitectura del Proyecto
El flujo está diseñado en n8n y sigue una lógica de pipeline de datos:

Trigger: Captura de nuevos registros en Google Sheets.

Media Manager: Descarga automatizada de flyers desde Google Drive y subida a la biblioteca de WordPress.

AI Engine: Procesamiento de lenguaje natural mediante Ollama (ejecución local de LLMs) para redactar el cuerpo de la noticia basado en prompts técnicos.

Logic Switch: Enrutamiento de datos hacia diferentes portales (Ateneo / CC Patria Grande) según el origen.

CMS Integration: Publicación automática vía API, vinculando featured_media y categorías específicas para visualización en Elementor.

🛠️ Stack Tecnológico
n8n: Orquestador de flujos de trabajo (Self-hosted).

Ollama: Motor de IA local para generación de texto (Privacidad de datos y 0 costo de API).

WordPress REST API: Gestión y publicación automatizada de contenidos.

Elementor & Post Grid: Visualización dinámica de los datos en el frontend.

📁 Estructura del Repositorio
/workflow: Contiene el archivo .json para importar el flujo en n8n.

/prompts: Configuración de los prompts enviados a Ollama.

README.md: Documentación técnica.

🌟 Valor Agregado
Este sistema elimina la carga manual de eventos, reduciendo el tiempo de publicación de 15 minutos a menos de 30 segundos por nota, garantizando consistencia en el diseño y privacidad absoluta al procesar la IA en un entorno local (Docker).
