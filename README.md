Este proyecto implementa un sistema completo de Generación Aumentada por Recuperación (RAG). Utiliza dos flujos de n8n interconectados para crear un chatbot inteligente capaz de responder preguntas basándose exclusivamente en tus propios documentos.

El sistema funciona en dos partes:

1. Flujo de Ingesta de Archivos: Monitorea una carpeta de Google Drive. Cuando se añade un archivo nuevo (PDF, DOCX, XLSX, etc.) , el flujo lo procesa, lo divide en partes , genera "embeddings" (vectores semánticos con IA) y los almacena en una base de datos vectorial Supabase.
2. Flujo de Chat Interactivo (RAG): Proporciona una interfaz de chat para que un usuario pueda hacer preguntas. El flujo busca en Supabase los fragmentos de texto más relevantes para la pregunta , los entrega a un modelo de IA (OpenAI) como "contexto" y genera una respuesta precisa basada solo en esa información.

🎯 Problema que Resuelve
Elimina la necesidad de buscar manualmente información en grandes cantidades de documentos internos (como políticas de empresa, reportes financieros o manuales técnicos).

Este flujo permite a cualquier equipo obtener respuestas instantáneas y precisas de su propia base de conocimiento usando lenguaje natural.

👥 Audiencia Objetivo

Equipos de RRHH: Para consultar políticas de vacaciones, beneficios, etc..

Equipos de Finanzas: Para extraer datos rápidos de reportes o presupuestos.

Equipos de Soporte: Para encontrar soluciones en la documentación técnica.

Desarrolladores: Como una base para integrar IA y gestión de conocimiento en aplicaciones.
