# Amigo Secreto

Aplicación web para organizar un intercambio de regalos entre amigos. Permite agregar participantes, realizar el sorteo y compartir las asignaciones sin que nadie quede emparejado consigo mismo.

Está construida con HTML, CSS y JavaScript, sin frameworks, dependencias ni proceso de build.

## Demo

[https://jcam2327.github.io/juego-del-AmigoSecreto/](https://jcam2327.github.io/juego-del-AmigoSecreto/)

## Características

- Alta de participantes con validación de nombres vacíos y duplicados exactos.
- Sorteo aleatorio con algoritmo Fisher-Yates.
- Evitación de autoasignaciones durante el sorteo.
- Ajuste de respaldo si no se encuentra una combinación válida tras 100 intentos.
- Resultados visibles en pantalla para compartir cada asignación.
- Diseño responsive alineado al sistema visual del portfolio.
- Tema claro y oscuro automático según la preferencia del sistema (`prefers-color-scheme`).
- Accesibilidad básica: enlace para saltar al contenido, etiquetas de formulario, regiones `aria-live` y foco visible.
- Sin backend, autenticación, persistencia ni dependencias externas.

## Cómo usar

1. Escribí el nombre de un participante y presioná **Añadir**.
2. Repetí el proceso hasta agregar al menos dos personas.
3. Presioná **Sortear amigo** para generar las asignaciones.
4. Compartí cada resultado con la persona correspondiente.

Para empezar de nuevo, recargá la página. La aplicación no incluye un botón de reinicio ni permite eliminar participantes de la lista.

## Cómo funciona

- Los nombres se guardan en un array en memoria.
- Antes de agregar, se valida que el campo no esté vacío y que el nombre no exista ya en la lista.
- El sorteo baraja una copia de los participantes con Fisher-Yates.
- Se repite el barajado hasta obtener una combinación sin autoasignaciones, con un máximo de 100 intentos.
- Si se agota ese límite, se aplica un ajuste de respaldo para corregir las posiciones que hayan quedado iguales.
- Los resultados se renderizan en pantalla con el formato `Participante ➔ Asignado`.
- No se envían datos a ningún servidor ni se guardan entre sesiones.

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

## Ejecutar localmente

Podés abrir `index.html` directamente en el navegador o levantar un servidor local:

```bash
python -m http.server 8000
```

Luego abrí `http://localhost:8000`.

## Despliegue

El proyecto se publica con GitHub Pages desde la raíz de la rama `main`. No requiere build ni configuración adicional: al hacer push de los cambios, GitHub Pages sirve la última versión.

## Privacidad y limitaciones

- Todos los resultados se muestran juntos en pantalla; la privacidad depende de cómo se compartan.
- No hay backend, autenticación ni base de datos.
- Los datos viven en memoria: al recargar la página se pierde la lista.
- No se pueden eliminar participantes individualmente ni reiniciar el sorteo desde la interfaz.
- El sorteo usa `Math.random()` en el navegador; es adecuado para un intercambio informal, no para un sorteo con garantías criptográficas.
- La herramienta no reemplaza un sorteo certificado ni un proceso con requisitos de auditoría.

## Estado

Publicado como demo en GitHub Pages. Última actualización: 2026-11-06.

## Enlaces

- [Demo](https://jcam2327.github.io/juego-del-AmigoSecreto/)
- [Repositorio](https://github.com/JCAM2327/juego-del-AmigoSecreto)
