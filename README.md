# Aloxter Assistant - Cloud Functions

Este repositorio contiene las Cloud Functions que potencian el asistente virtual Aloxter. Las funciones están implementadas utilizando Firebase Cloud Functions y proporcionan la lógica del servidor para el procesamiento de lenguaje natural y la integración con OpenAI.

## Características

- Integración con OpenAI para procesamiento de lenguaje natural
- Manejo de solicitudes HTTP para comunicación con el frontend
- Sistema de autenticación y autorización
- Procesamiento de mensajes y generación de respuestas
- Gestión de contexto de conversación

## Requisitos Previos

- Node.js (v16 o superior)
- Firebase CLI
- Cuenta de Firebase
- Cuenta de OpenAI y API Key

## Configuración Local

1. Clona el repositorio:
```bash
git clone https://github.com/alexanderruiz46/asistenteia-cloudfunctions.git
cd asistenteia-cloudfunctions
```

2. Instala las dependencias:
```bash
npm install
```

3. Configura las variables de entorno:
   - Crea un archivo `.env` en la raíz del proyecto
   - Añade las siguientes variables:
   ```
   OPENAI_API_KEY=tu_api_key_de_openai
   ```

4. Inicia el emulador de Firebase:
```bash
firebase emulators:start
```

## Despliegue

1. Asegúrate de tener Firebase CLI instalado y estar autenticado:
```bash
npm install -g firebase-tools
firebase login
```

2. Selecciona tu proyecto:
```bash
firebase use tu-proyecto-id
```

3. Despliega las funciones:
```bash
firebase deploy --only functions
```

## Estructura del Proyecto

```
functions/
├── src/
│   ├── index.js        # Punto de entrada principal
│   ├── config/         # Configuraciones
│   ├── controllers/    # Controladores de funciones
│   └── utils/         # Utilidades y helpers
├── package.json
└── firebase.json
```

## Endpoints

### POST /processMessage
Procesa un mensaje del usuario y genera una respuesta utilizando OpenAI.

**Request Body:**
```json
{
  "message": "string",
  "context": "string"
}
```

**Response:**
```json
{
  "response": "string",
  "context": "string"
}
```

## Contribución

1. Fork el proyecto
2. Crea tu rama de características (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m "Add some AmazingFeature"`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## Contacto

Alexander Ruiz - [@alexanderruiz46](https://github.com/alexanderruiz46)

Link del Proyecto: [https://github.com/alexanderruiz46/asistenteia-cloudfunctions](https://github.com/alexanderruiz46/asistenteia-cloudfunctions)
