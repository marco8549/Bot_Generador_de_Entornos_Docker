# 📦 Proyecto Final — Bot Generador de Entornos Docker  
**DAM · Sistemas Informáticos · Proyecto Integrador — Tercera Evaluación**

Este proyecto consiste en un **bot de Telegram con IA** capaz de generar y desplegar automáticamente entornos Docker a partir de descripciones en lenguaje natural.  
El usuario escribe lo que necesita, y el sistema construye y levanta el entorno completo.

Ejemplo:

> **“Necesito un entorno para una app Python con PostgreSQL y Redis”**  
>  
> ✔ Entorno generado  
> ✔ URL: http://localhost:8080  
> ✔ PostgreSQL: 5432  
> ✔ Redis: 6379  
> ✔ Credenciales: usuario / 1234  

Tecnologías utilizadas:

- Docker · Docker Compose  
- n8n  
- OpenHands  
- Ollama / Groq / Hugging Face  
- Telegram Bot  
- Git · GitHub  

---

## 🧠 Arquitectura del Sistema

```mermaid
flowchart LR
    A[Mensaje del usuario en Telegram] --> B[n8n recibe Webhook]
    B --> C[IA genera docker-compose.yml]
    C --> D[OpenHands despliega el entorno]
    D --> E[Bot responde con la URL y estado]

📦 proyecto-final-bot-docker
 ├── docker-compose.yml
 ├── README.md
 ├── /capturas
 │    ├── portada.png
 │    ├── flujo-n8n.png
 │    ├── despliegue.png
 │    └── bot-telegram.png
 ├── /n8n-flow
 │    └── flow.json
 └── video-demostracion.mp4

