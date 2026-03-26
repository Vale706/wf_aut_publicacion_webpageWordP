Automated AI Content Publisher (n8n + Ollama + WordPress)
Este proyecto es un sistema de automatización de ciclo completo que transforma datos estructurados de eventos en artículos de prensa profesionales, utilizando IA local para la generación de contenido y la REST API de WordPress para la distribución dinámica.

🚀 Arquitectura del Proyecto
El flujo está diseñado en n8n y sigue una lógica de pipeline de datos:

Trigger: Captura de nuevos registros en Google Sheets.

Media Manager: Descarga automatizada de flyers desde Google Drive y subida a la biblioteca de WordPress.

AI Engine: Procesamiento de lenguaje natural mediante Ollama (ejecución local de LLMs) para redactar el cuerpo de la noticia basado en prompts técnicos.

Logic Switch: Enrutamiento de datos hacia diferentes portales (Ateneo / CC Patria Grande) según el origen.

CMS Integration: Publicación automática vía API, vinculando featured_media y categorías específicas para visualización en Elementor.
<img width="1600" height="566" alt="image" src="https://github.com/user-attachments/assets/2774195d-872d-40f3-ab3a-62307650d3fc" />



Nodo Google Sheet


<img width="445" height="782" alt="image" src="https://github.com/user-attachments/assets/633cdc56-5f48-4c08-bf16-35fa5fc995ff" />


Nodo Edit Fields


<img width="568" height="756" alt="image" src="https://github.com/user-attachments/assets/71ce27fb-bd9a-44a7-b1a2-c15a19ce7f98" />


Nodo Switch


<img width="569" height="791" alt="image" src="https://github.com/user-attachments/assets/84350587-d91f-468c-800c-3e584cad8a02" />


Nodo HTTP Request para descaragr imagen


<img width="569" height="801" alt="image" src="https://github.com/user-attachments/assets/f0944449-4c51-4c35-98ac-a944cfb8cd2a" />


Nodo HTTP Request para subir imagen 


<img width="565" height="811" alt="image" src="https://github.com/user-attachments/assets/c0c2c4dd-6b33-4950-8911-7c70212909c3" />


Nodo OLlama


<img width="565" height="798" alt="image" src="https://github.com/user-attachments/assets/404d1b00-ffec-4ff7-b097-f83e9a177797" />


Nodo HTTP Request Subir Post


<img width="1310" height="813" alt="image" src="https://github.com/user-attachments/assets/956d99e4-8548-466a-8fca-a168afecb12f" />





🛠️ Stack Tecnológico
n8n: Orquestador de flujos de trabajo (Self-hosted).

Ollama: Motor de IA local para generación de texto (Privacidad de datos y 0 costo de API).

WordPress REST API: Gestión y publicación automatizada de contenidos.

Elementor & Post Grid: Visualización dinámica de los datos en el frontend.

📁 Estructura del Repositorio
/workflow: Contiene el archivo .json para importar el flujo en n8n.
README.md: Documentación técnica.

🌟 Valor Agregado
Este sistema elimina la carga manual de eventos, reduciendo el tiempo de publicación de 15 minutos a menos de 30 segundos por nota, garantizando consistencia en el diseño y privacidad absoluta al procesar la IA en un entorno local (Docker).
