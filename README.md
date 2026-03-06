# Visor para bancos de preguntas

## El programa visor

El programa visor se ejecuta en un navegador web, y sirve para mostrar, de forma consecutiva o aleatoriamente, un conjunto de preguntas y respuestas para estudiarlas. Para ello:

- Usa `←` / `→` para navegar por las preguntas.
- Pulsa `S` para mostrar/ocultar la solución.
- Pulsa `R` para barajar las preguntas.
- Recarga la página para ordenarlas.

Mediante este programa es posible repasar las respuestas a las preguntas de los exámenes si mantienes activada la función de mostrar solución, reteniendo de esta forma la respuesta correcta, o bien recorrer las preguntas para intentar acertar las respuestas y ver inmediatamente el resultado mostrando/ocultando la solución a la pregunta.

## Estructura de los datos

El programa requiere que esté habilitado el soporte JavaScript en el navegador.

Al ser abierto, importa un fichero llamado `bancoDePreguntas.js` que contiene:

- Cada una de las preguntas del banco de preguntas
- Las respuestas posibles asociadas a cada pregunta
. El número de respuesta correcta de entre las respuestas
- El número de examen al que corresponde la pregunta (opcional)

La estructura de los datos es la siguiente:

```javascript
window.bancoDePreguntas = [
  {
    "pregunta": "Texto de la pregunta",
    "opciones": [
      "Respuesta 1.",
      "Respuesta 2.",
      "Respuesta 3.",
      "Respuesta 4."
    ],
    "correcta": 0,
    "examen": 1
  },

  ...otras preguntas aquí...

]
```

El valor "correcta" indica la opción correcta de ente las opciones posibles. En el ejemplo, la primera opción es la 0 y la cuarta es la 3 (índice 0).

Cada pregunta debe tener, al menos, dos respuestas posibles.

## Bancos de preguntas

Se pueden incorporar nuevas preguntas al banco de preguntas o también intercambiar el fichero `bancoDePreguntas.js` con otras temáticas de estudio, en ese caso:

- El fichero `bancoDePreguntas.js` debe estar en la carpeta donde se encuentre el programa `visor.html`.
- El nuevo banco de preguntas debe tener el nombre `bancoDePreguntas.js`, por lo que se deberá renombar el fichero del banco de preguntas actual.
- El banco de preguntas debe tener al menos una pregunta con sus correspondientes opciones, e indicar la respuesta correcta.

## Sobre el autor

Este programa fue realizado por: Javier Guerra, el 27 de febrero de 2026.

Para su desarrollo se ha empleado la IA Copilot.

El código se distribuye bajo licencia GPL v.3.
