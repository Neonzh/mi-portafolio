# Guía del proyecto tienda-tecsup

Esta guía explica el trabajo realizado en el proyecto **tienda-tecsup**, desarrollado durante el Laboratorio 03. El objetivo principal fue trabajar con un repositorio remoto mediante Git y GitHub, realizar una corrección en el código y proponerla mediante un Pull Request.

## Descripción del proyecto

El proyecto corresponde a una pequeña tienda web que muestra productos y calcula el total de un carrito de compras.

Durante el desarrollo se trabajó con un repositorio remoto y una copia personal mediante un fork. Luego se clonó el proyecto en la computadora para poder modificarlo y probar los cambios.

Los principales elementos utilizados fueron:

- Git para controlar las versiones del proyecto.
- GitHub para almacenar el repositorio remoto.
- Un fork para tener una copia propia del repositorio.
- Una rama independiente para realizar la corrección.
- Issues para reportar problemas.
- Pull Requests para proponer los cambios realizados.

### Archivos principales

| Archivo       | Función                                                          |
| ------------- | ---------------------------------------------------------------- |
| `index.html`  | Contiene la estructura y los elementos principales de la página. |
| `estilos.css` | Contiene los estilos, colores y tipografía de la página.         |
| `script.js`   | Contiene la lógica utilizada para calcular el total del carrito. |
| `README.md`   | Contiene información y resultados esperados del proyecto.        |

## Instalación y uso

Para trabajar con el proyecto desde una computadora es necesario tener Git instalado, una cuenta de GitHub y un editor de código como Visual Studio Code.

### Pasos de instalación

1. Crear un fork del repositorio `tienda-tecsup` desde GitHub.
2. Clonar el fork en la computadora utilizando Git.
3. Entrar a la carpeta del proyecto.
4. Abrir el proyecto con Visual Studio Code.
5. Ejecutar `index.html` en el navegador para comprobar el funcionamiento.
6. Realizar los cambios necesarios y comprobar el resultado antes de subirlos.

Un comando utilizado para comprobar el repositorio remoto fue `git remote -v`, ya que permite verificar que `origin` apunta al fork personal.

### Corrección realizada

Uno de los errores encontrados estaba relacionado con el cálculo del total del carrito. La función `calcularTotal` sumaba solamente el precio de cada producto y no tomaba en cuenta su cantidad. Por ese motivo, el total mostrado inicialmente era **S/ 43.00**, cuando el resultado esperado era **S/ 68.00**.

La corrección consistió en multiplicar el precio por la cantidad del producto:

```javascript
function calcularTotal(lista) {
  let total = 0;

  for (const producto of lista) {
    total = total + producto.precio * producto.cantidad;
  }

  return total;
}
```

Después de realizar el cambio, se comprobó el resultado en el navegador y el total pasó a mostrar **S/ 68.00**.

## Trabajo con Git

Para organizar la corrección se utilizó una rama independiente llamada `fix-total-carrito`. Después de modificar el código, se revisaron los cambios con `git diff`, se creó un commit y finalmente se subió la rama al repositorio remoto.

Algunos comandos importantes utilizados durante el trabajo fueron:

| Comando      | Uso                                                     |
| ------------ | ------------------------------------------------------- |
| `git clone`  | Descarga el repositorio remoto a la computadora.        |
| `git status` | Permite revisar el estado actual del repositorio.       |
| `git diff`   | Muestra los cambios realizados en los archivos.         |
| `git commit` | Guarda los cambios en el historial local.               |
| `git push`   | Envía los commits al repositorio remoto.                |
| `git pull`   | Descarga cambios recientes desde el repositorio remoto. |

### Estado del trabajo

- [x] Crear el fork del repositorio.
- [x] Clonar el proyecto en la computadora.
- [x] Identificar y corregir el error del cálculo del carrito.
- [x] Crear una rama para la corrección.
- [x] Realizar un commit con los cambios.
- [x] Subir la rama mediante `git push`.
- [x] Crear un Pull Request.

## Resultado

El trabajo permitió practicar el flujo de colaboración mediante **fork → clone → branch → commit → push → Pull Request**. También se comprobó la importancia de revisar los cambios antes de crear un Pull Request, verificando que solamente se modificara el archivo necesario.

### Evidencia del proyecto

Aquí colocaré posteriormente una captura de pantalla del proyecto funcionando:

> **[Insertar aquí la imagen del proyecto]**

La imagen debe guardarse dentro del repositorio y agregarse mediante una ruta relativa, por ejemplo:

insertar imagen....

## Enlace externo

Repositorio original utilizado durante el laboratorio:

https://github.com/jeisson-tecsup/tienda-tecsup

También se puede consultar el repositorio personal del proyecto en GitHub.
