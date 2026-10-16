# Índice de búsqueda

Cada bloque importante del código lleva una etiqueta `SEC:NOMBRE`. Búscala con Ctrl+F o Ctrl+Shift+F en VS Code. Las líneas corresponden a `src/puebla-turistica-360.dc.html`.

| Etiqueta | Línea | Qué hace |
|---|---|---|
| `CSS-BASE` | 15 | Reinicio: quita el margen por defecto del navegador. |
| `CSS-FONDO` | 18 | Animaciones del fondo de presentación. ptDrift: rombos que suben · ptBurstA/ptBurstB: onda al pulsar (dos nombres alternados para reiniciar  |
| `CSS-ANIMACIONES` | 23 | Todas las animaciones empiezan con "pt". Cada una se usa así: |
| `CSS-ENLACES` | 67 | Color de enlaces (normal y al pasar el cursor) tomado de la paleta. |
| `CSS-TRANSICION-PANTALLA` | 72 | Cada pantalla marcada con data-pt-screen entra deslizándose. |
| `CSS-ESCALONADO` | 74 | Los hijos directos del área desplazable de cada pantalla aparecen en cascada, con retraso creciente (nth-child). |
| `CSS-INTERACCION` | 83 | Transiciones suaves, sin resalte táctil en móvil, brillo al pasar el cursor, reducción al pulsar y anillo azul al enfocar campos. |
| `CSS-TARJETAS` | 89 | Las tarjetas (radio 18px) se elevan ligeramente al pasar el cursor. |
| `RAIZ` | 94 | Contenedor de toda la página. themeVars define las variables CSS de color (--pri, --bg, --ink...) según claro/oscuro. Centra el teléfono en  |
| `FONDO-ANIMADO` | 97 | Fondo de presentación alrededor del teléfono, con la marca Puebla 360°. Reacciona a cada pulsación: lanza una onda, sube la intensidad del r |
| `PANTALLA-TELEFONO` | 115 | Recorte redondeado del teléfono. Es una columna: barra de estado arriba y la pantalla activa debajo. Las pantallas se muestran con sc-if seg |
| `BARRA-ESTADO` | 117 | Barra de estado decorativa: hora, isla dinámica y señal. |
| `T1-SPLASH` | 122 | Pantalla inicial: fondo azul con logo animado, nombre y barra de carga. Pasa sola a Idioma a los 3.5 s. |
| `T2-IDIOMA` | 149 | Elegir idioma (es, en, fr, de, pt, it). Toda la app cambia al elegir. |
| `T3-ACCESO` | 168 | Crear cuenta o iniciar sesión como turista. Botón ‹ regresa a la pantalla anterior (historial). |
| `T4-VERIFICACION` | 194 | Verificación de identidad con documento y rostro (animación por pasos idStep 0 a 4). |
| `T5-BIENVENIDA` | 265 | Saludo con el nombre del usuario. Pasa sola a Cotizador a los 6 s. |
| `T6-COTIZADOR` | 296 | Pantalla principal del turista: presupuesto, actividades, fechas, ciudad, personas y notas. |
| `T7-RESULTADOS` | 391 | Opciones de agencias. Estados: cargando, error, vacío y lista. |
| `T8-PAGO` | 442 | Pago. Indicador de pasos: Cotizar, Opciones, Pago. |
| `T9-CONFIRMACION` | 482 | Confirmación de la solicitud, con confeti. |
| `T10-MIS-COTIZACIONES` | 501 | Historial de cotizaciones enviadas, guardado en el dispositivo (localStorage "pt360-quotes"). |
| `E1-CREAR-CUENTA-EMPRESA` | 525 | Registro de empresa: nombre y contraseña con reglas de seguridad. |
| `E2-ID-ASIGNADO` | 544 | Muestra el ID asignado a la empresa para guardarlo y copiarlo. |
| `E3-LOGIN-EMPRESA` | 560 | Inicio de sesión con ID y contraseña (vienen prellenados). |
| `E4-COBROS` | 575 | Registro de cobros: activar monedas y dirección de wallet con validación por red. |
| `E5-DATATUR` | 599 | Consulta DataTur con identificador y consentimiento. |
| `E6-DATOS-PERFIL` | 615 | Revisar y corregir los datos del perfil de la empresa. |
| `E7-AVISO-PRIVACIDAD` | 629 | Aviso de privacidad: aceptar o rechazar. |
| `E8-EMPRESA-VISIBLE` | 642 | Confirma que la empresa ya aparece en la app. |
| `E9-PANEL-EMPRESA` | 655 | Panel con pestañas Solicitudes y Datos de pago. Estados: cargando, error, vacío y datos. |
| `MENU-HAMBURGUESA` | 692 | Botón de tres rayas (arriba a la izquierda, oculto en el splash). |
| `CHATBOT` | 713 | Botón flotante "?" que abre el asistente. |
| `AVISO-PRIVACIDAD-HOJA` | 737 | Hoja inferior con el aviso de privacidad de datos biométricos. |
| `DATOS` | 764 | Constantes del negocio. |
| `VALIDACION` | 781 | walletOk(moneda, dirección): comprueba el formato con una expresión regular según la red. |
| `TEXTOS` | 790 | T: todos los textos de la interfaz por idioma. Español (es) e inglés (en) completos; fr, de, pt, it se completan más abajo y heredan el ingl |
| `TEXTOS-AGENCIAS` | 855 | AGTXT: descripción de cada agencia por idioma. |
| `CHATBOT-DATOS` | 860 | FAQS: preguntas frecuentes. k = palabras clave para reconocer la pregunta; es/en = pregunta (q) y respuesta (a). |
| `TRADUCCIONES` | 873 | FR, DE, PT, IT: textos de interfaz en francés, alemán, portugués e italiano. |
| `MIS-COTIZACIONES-LECTURA` | 895 | loadQ(): lee las cotizaciones guardadas en localStorage; si no hay o falla, devuelve lista vacía. |
| `NAVEGACION` | 897 | SCREENS_T: orden de pantallas del turista. SCREENS_C: pantallas de empresa (prefijo c_). |
| `LOGICA` | 906 | Clase principal. Guarda el estado, controla la navegación y calcula todos los valores que usa la plantilla (renderVals). |
| `ESTADO` | 908 | Datos que cambian durante el uso. |
| `NAVEGACION-ENTRAR` | 937 | enter(id): acciones automáticas al llegar a una pantalla. |
| `MIS-COTIZACIONES-GUARDAR` | 950 | saveQuote(): arma la cotización con los datos actuales, la agrega al inicio de la lista y la guarda en localStorage. |
| `NAVEGACION-IR` | 958 | go(id): cambia de pantalla guardando la actual en el historial (replace=true no la guarda). Cierra desplegables y avisos. |
| `CHATBOT-LOGICA` | 965 | sendChat: agrega el mensaje del usuario y responde tras una pausa. Si viene de una pregunta sugerida usa su respuesta; si es texto libre bus |
| `CALCULOS` | 984 | days(): días del viaje, mínimo 1. |
| `RENDER` | 992 | renderVals(): prepara todo lo que lee la plantilla. Se ejecuta en cada cambio de estado. |
| `RENDER-TEMA` | 998 | Paleta de colores. C cambia entre oscuro y claro; se aplica como variables CSS. |
| `RENDER-ESTILOS` | 1009 | Estilos reutilizables. |
| `RENDER-ACCIONES` | 1023 | h: acciones que los botones de la plantilla llaman. act(nombre, función) las registra. |
| `VALIDACION-COTIZAR` | 1055 | Cotizar: revisa actividades, fechas, ciudad, hora y personas. Si falta algo, muestra la lista; si no, "Datos completos". |
| `RENDER-ACCIONES-EMPRESA` | 1093 | Acciones del flujo de empresa. |
| `RENDER-DERIVADOS` | 1123 | Valores calculados a partir del estado. |
| `RENDER-RESULTADOS` | 1154 | Tarjetas de agencias: precio en la moneda elegida, selección, estilo y brillo. |
| `RENDER-PAGO` | 1175 | Agencia, moneda y monto a pagar. accepted: monedas que acepta; coinAmt: precio convertido. |
| `RENDER-PANEL-EMPRESA` | 1212 | Estados y colores de solicitudes. |
| `RENDER-VERIFICACION` | 1256 | Animación de verificación de identidad. |
| `RENDER-MIS-COTIZACIONES` | 1292 | qs: datos de la pantalla Mis cotizaciones. |
| `RENDER-CHAT` | 1325 | Preguntas ya hechas, nombre del usuario y estructura del chat (mensajes y preguntas sugeridas). |
| `RENDER-FONDO` | 1345 | bg: estilos del fondo animado. lvl (0 a 1) crece con cada pulsación hasta 15. El nombre de la animación de la onda alterna entre ptBurstA y  |
| `RENDER-SALIDA` | 1354 | Objeto con todo lo que la plantilla puede leer: s (pantalla activa), h (acciones), t (textos) y los valores anteriores. |
