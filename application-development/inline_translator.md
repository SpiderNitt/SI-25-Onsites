# Inline Text Translator

## Objective

Create a simple API that translates text from one language to another using a public translation service such as [LibreTranslate](https://libretranslate.com/). This tool can be used in various applications to provide real-time language translation with minimal setup.

## Key Features to Implement

### 1. Text Translation API

**Functionality:**  
Accept input text along with source and target languages, and return the translated version.

**Requirements:**
- `POST /translate`
- Request body:
  ```json
  {
    "text": "Hello, how are you?",
    "source": "en",
    "target": "es"
  }
Response:

json
Copy
Edit
{
  "translatedText": "Hola, ¿cómo estás?"
}
Use a public translation API like LibreTranslate.

### 2. Input Validation
**Functionality:**
Ensure valid input parameters are provided.

**Requirements:**

- Validate that text is a non-empty string.
- Validate that source and target are valid ISO language codes.
- Return informative error messages for invalid requests.