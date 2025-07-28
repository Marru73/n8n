# n8n‑projects

Este repositorio centraliza mis flujos de trabajo de n8n.

### AI PUBLISHER:

    ## Workflows

    ### `AI Social Publisher RSS

    - **Archivo**: `AI Social Publisher RSS.json`  
    - **Descripción**: Envía noticias a Telegram, registra la elección y gestiona timeouts.  
    - **Version**: v1.0  
    - **Última actualización**: 24/07/2025  

    ### AI Publisher – Publicar RRSS
    - **Archivo**: `AI Publisher – Publicar RRSS.json`  
    - **Descripción**: Sub‑workflow que procesa la pulsación de “elegir” y lanza publicación en RRSS.  
    - **Version**: v1.0  

    ### AI Publisher – Ai Publisher No pulsado elegir.json

    - **Archivo**: `Ai Publisher No pulsado elegir.json`  
    - **Descripción**: Sub‑workflow que gestiona expiración de 10 min y notifica timeouts.  
    - **Version**: v1.0  

    ## Uso

    1. Importa cualquiera de los JSON en tu instancia de n8n (Workflows → Import).  
    2. Configura tus **Credentials** (Telegram, Google Sheets, APIs externas).  
    3. Activa los workflows y deja que corran según su trigger (Schedule o Webhook).


### SECRETARIO:

    ## Workflows:

    **Nota IMPORTANTE:** En esta carpeta tienes el "Flujo Principal Telegram" básico con sus Subworkflows y también tienes "Flujo Principal Telegram Compacto" que está actualizado con nodos Agent IA Tool, para prescindir de subworkflows, aunque aún contienen un par de ellos.

- **Flujo Principal Telegram**  
  Orquestador principal que recibe mensajes de Telegram, detecta texto/voz/foto y llama al agente adecuado (Gmail, Calendario, Contactos, Documentos, Contabilidad, Writer, Calculadora o Búsqueda web). 
- 
- **Actualizar base de conocimiento**  
  Sube documentos, los divide en fragmentos con un _text splitter_ y los indexa en un vector store de Supabase usando embeddings de OpenAI.  

- **Agente especialista en contactos**  
  Agente conversacional que consulta, crea o actualiza contactos en Google Contacts mediante un prompt en español, orquestado por OpenAI GPT.  

- **Agente especialista en crear contenido**  
  Agente que genera textos profesionales (artículos, guiones, resúmenes, posts) en español siguiendo un sistema de roles e instrucciones claras.  

- **Agente especialista en Gmail**  
  Agente para gestionar correos: enviar, responder, marcar como no leído, etiquetar o borrar mensajes y crear borradores en Gmail.  
 
- **Agente especializado de calendario**  
  Agente para crear, consultar, editar y eliminar eventos en Google Calendar, con validación de fechas y horarios en zona Europe/Madrid.  

- **Agente especializado en documentos**  
  Agente que interactúa con Google Docs: crear documentos, obtenerlos o actualizarlos según instrucciones del usuario (sin redactar contenido).  
 
- **Control de gastos e ingresos**  
  Procesa texto libre con OpenAI para extraer concepto, descripción, valor y fecha, y registra automáticamente la fila en la hoja de Google Sheets correspondiente (Gastos o Ingresos). 
>>>>>>> 85a7b435bfb85f69613d5047d69033d9a97e1fd5
