# Amigo Secreto

Aplicación web para organizar un intercambio de regalos entre amigos. Permite agregar participantes, realizar el sorteo y compartir los resultados sin que nadie quede asignado a sí mismo.

## Demo

[https://jcam2327.github.io/juego-del-AmigoSecreto/](https://jcam2327.github.io/juego-del-AmigoSecreto/)

## Características

- Agregar participantes a la lista.
- Validación de nombres vacíos y duplicados.
- Sorteo con algoritmo que evita autoasignaciones.
- Resultados visibles en pantalla para compartirlos.
- Diseño responsive alineado al sistema visual del portfolio.
- Modo claro y oscuro según la preferencia del sistema.

## Tecnologías

- HTML5
- CSS3
- JavaScript (ES6)

No utiliza frameworks, dependencias ni proceso de build.

## Estructura

```text
juego-del-AmigoSecreto/
├── index.html
├── style.css
├── app.js
├── assets/
│   ├── amigo-secreto.png
│   └── play_circle_outline.png
└── README.md
```

## Cómo usar

1. Escribí el nombre de un participante y presioná **Añadir**.
2. Repetí el proceso hasta agregar al menos dos personas.
3. Presioná **Sortear amigo** para generar las parejas.
4. Compartí cada resultado con la persona correspondiente.

## Estado

Proyecto de formación publicado como demo en GitHub Pages.

El sorteo se ejecuta del lado del cliente y los resultados se muestran en pantalla. No hay backend, autenticación ni persistencia de datos. La privacidad de cada asignación depende de cómo se compartan los resultados.

## Enlaces

- [Demo](https://jcam2327.github.io/juego-del-AmigoSecreto/)
- [Repositorio](https://github.com/JCAM2327/juego-del-AmigoSecreto)
