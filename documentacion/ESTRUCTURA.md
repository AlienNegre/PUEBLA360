# Estructura del código

El archivo `src/puebla-turistica-360.dc.html` tiene cuatro partes, en este orden:

1. **Estilos** (`<style>` dentro de `<helmet>`): fuentes, animaciones `pt*` y reglas globales. Etiquetas `SEC:CSS-*`.
2. **Plantilla** (entre `<x-dc>` y `</x-dc>`): el HTML de todas las pantallas. Cada pantalla se muestra solo cuando su bandera `s.<nombre>` es verdadera.
3. **Datos** (primera parte del `<script>`): agencias, tarifas, textos por idioma, preguntas del chat y listas de pantallas. Etiquetas `SEC:DATOS`, `SEC:TEXTOS`, `SEC:CHATBOT-DATOS`, `SEC:NAVEGACION`.
4. **Lógica** (clase `Component`): estado, navegación, cálculos y `renderVals()`, que entrega a la plantilla todo lo que lee. Etiquetas `SEC:LOGICA`, `SEC:ESTADO`, `SEC:RENDER-*`.

## Pantallas

Turista: T1 splash, T2 idioma, T3 acceso, T4 verificación, T5 bienvenida, T6 cotizador, T7 resultados, T8 pago, T9 confirmación, T10 mis cotizaciones.

Empresa: E1 crear cuenta, E2 ID asignado, E3 login, E4 cobros, E5 DataTur, E6 datos del perfil, E7 aviso de privacidad, E8 empresa visible, E9 panel.

Elementos que flotan sobre cualquier pantalla: menú de hamburguesa, chatbot, aviso de privacidad y mensajes breves (toast).

## Cómo fluyen los datos

`state` guarda lo que cambia. Un botón llama a una acción de `h` (definida con `act`), que usa `setState` o `go()` para navegar. `renderVals()` recalcula todo y la plantilla se actualiza.

## Cambios frecuentes

- **Agencias, precios, teléfonos:** constante `AG` (`SEC:DATOS`).
- **Tarifas por actividad y valor de monedas:** `RATE`. Tipo de cambio: `FX`.
- **Textos de la interfaz:** objeto `T` (`SEC:TEXTOS`) y las constantes `FR`, `DE`, `PT`, `IT`.
- **Preguntas del chatbot:** `FAQS` (`SEC:CHATBOT-DATOS`).
- **Perfil de empresa por defecto:** `state` (`SEC:ESTADO`): `cName`, `cPass`, `cId`, `loginId`, `loginPass`, `wallets`, `dtId`, `profile`.
- **Colores:** objeto `C` en `renderVals()` (`SEC:RENDER-TEMA`).
- **Fotos de agencias:** carpeta `src/images/` y campo `photo` de `AG`.
