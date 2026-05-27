# Tablero de Control de Cobranzas — Seguros Confianza

Vista operativa para la Jefatura de Cobranzas y stakeholders autorizados.

## Acceso

El tablero está cifrado con **AES-256-GCM** y la clave se deriva con **PBKDF2-SHA-256
de 200,000 iteraciones**. Para acceder se requiere usuario y contraseña.

El descifrado ocurre íntegramente en el navegador (Web Crypto API). El servidor
nunca recibe la contraseña.

## Despliegue

Este repo está pensado para servirse vía GitHub Pages:

1. Settings → Pages → Source: `main` branch / root.
2. Una vez activado, el tablero queda disponible en `https://<usuario>.github.io/<repo>/`.

## Regeneración

El archivo `index.html` se genera ejecutando `scripts/encrypt_tablero.py` desde el
repo privado del proyecto. No se versionan datos sensibles ni credenciales aquí.
