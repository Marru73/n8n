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


