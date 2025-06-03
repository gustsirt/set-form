# Set-Form

**Set-Form** es una página web básica que permite visualizar y responder encuestas cargadas en una hoja de cálculo de Google Sheets.

## Objetivo

El proyecto busca facilitar la creación de formularios dinámicos a partir de un documento de Google Sheets, manteniendo una estructura simple y sin necesidad de un backend complejo.

## Características

- Se conecta con Google Sheets a través de las Google APIs.
- Recibe por variable de entorno (`ENV`) el ID del documento base (`SPREADSHEET_ID`).
- Dentro del documento, se espera una hoja con las preguntas de cada encuesta.
- Genera automáticamente una visualización por cada encuesta.
- Al completar una encuesta, las respuestas se envían directamente al formulario asociado.

## Tecnologías

- Google Sheets API
- Google Drive API
- JavaScript / HTML / TAILWIND
- Variables de entorno para configuración

## Instalación

1. Clonar este repositorio.
2. Crear un archivo `.env` basado en el archivo `.env.example`.
3. Activar las APIs de Google Sheets y Drive.
4. Compartir el documento de Google Sheets con el servicio autorizado.
5. Ejecutar el proyecto.

## Variables de entorno

Ver `.env.example` para más detalles.

## Ejemplo de estructura de hoja

| encuesta_id | pregunta          | tipo   |
|-------------|-------------------|--------|
| encuesta_1  | ¿Cómo te llamás?  | texto  |
| encuesta_1  | ¿Edad?            | número |
| encuesta_2  | ¿Te gustó el curso? | opción múltiple |

## Licencia

MIT
