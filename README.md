# Set-Form

**Set-Form** es una página web construida con Astro y TailwindCSS que permite visualizar y responder encuestas cargadas desde un documento de Google Sheets.

## Objetivo

El proyecto busca facilitar la generación de formularios dinámicos basados en hojas de cálculo de Google Sheets, manteniendo una estructura simple y sin backend adicional.

## Características

* Framework moderno: **Astro** + **TailwindCSS** para una experiencia rápida y responsiva.
* Integración directa con **Google Sheets API**.
* Configuración simple por variables de entorno.
* Generación automática de páginas de encuestas.
* Envío de respuestas al formulario asociado.

## Tecnologías

* [Astro](https://astro.build/)
* [TailwindCSS](https://tailwindcss.com/)
* Google Sheets API
* Google Drive API

## Instalación

1. Clonar el repositorio.
2. Crear un archivo `.env` basado en `.env.example`.
3. Activar las APIs necesarias en Google Cloud Console.
4. Compartir el documento de Google Sheets con el email del servicio autorizado.
5. Ejecutar el servidor local con:

   ```bash
   npm install
   npm run dev
   ```

## Variables de entorno

Estas variables son necesarias para conectarse correctamente a la hoja de Google Sheets:

* `SPREADSHEET_ID`: ID del documento de Google Sheets que contiene las encuestas.
* `GOOGLE_CLIENT_EMAIL`: Email del cliente de servicio autorizado.
* `GOOGLE_PRIVATE_KEY`: Clave privada del cliente de servicio (respetar los saltos de línea, usar `\n` si es necesario).

Guarda estas variables en un archivo `.env` en la raíz del proyecto.

---

### `.env.example`

```env
# ID del documento de Google Sheets
SPREADSHEET_ID=tu_id_de_spreadsheet_aqui

# Email del cliente de servicio autorizado
GOOGLE_CLIENT_EMAIL=servicio@proyecto.iam.gserviceaccount.com

# Clave privada del cliente de servicio (respetar saltos de línea)
GOOGLE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\nABC123...\n-----END PRIVATE KEY-----\n"
```

---

## Ejemplo de estructura de hoja

La hoja dentro del documento debe tener una estructura similar a:

| encuesta\_id | pregunta               | tipo             |
| ------------ | ---------------------- | ---------------- |
| encuesta\_1  | ¿Cómo te llamás?       | texto            |
| encuesta\_1  | ¿Cuántos años tenés?   | número           |
| encuesta\_2  | ¿Te gustó el servicio? | opción\_múltiple |

## Licencia

MIT
