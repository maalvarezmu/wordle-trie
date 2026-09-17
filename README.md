# Wordle — con motor de validación propio (Trie)

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat)

Recreación del clásico juego de palabras [Wordle](https://lapalabradeldia.com/), construida con HTML, CSS y JavaScript sobre [Vite](https://vitejs.dev/).

La particularidad de esta implementación es que la validación de palabras **no depende de ninguna librería externa ni de una búsqueda lineal**: el diccionario está indexado en un **Trie** construido desde cero, lo que permite verificar en tiempo eficiente si una palabra existe y buscar coincidencias por prefijo — la misma técnica usada en sistemas de autocompletado y correctores ortográficos.

## Vista previa

<img src="./public/preview.png">

## Detalles técnicos: ¿por qué un Trie?

Para validar si una palabra ingresada por el usuario existe en el diccionario, en vez de recorrer un arreglo con miles de palabras (`O(n · L)` por búsqueda), el diccionario se indexa una sola vez en un Trie al iniciar la aplicación. Esto permite:

- **Validación en O(L)**, donde `L` es la longitud de la palabra, sin importar el tamaño del diccionario.
- Una base reutilizable para features futuras como sugerencias por prefijo o autocompletado.

## Comenzando

### Prerrequisitos

Tener `npm` instalado. Si no lo tienes, descárgalo desde el [sitio oficial de Node.js](https://nodejs.org/).

### Instalación

1. Clona este repositorio:

   ```bash
   git clone https://github.com/maalvarezmu/wordle-trie.git
   ```

2. Instala las dependencias y ejecútalo en modo desarrollo:

   ```bash
   npm install
   npm run dev
   ```

3. Alternativamente, abre la carpeta `entrega/index` en tu navegador, o usa la extensión [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) desde tu editor.

## Construido con

- [Vite](https://vitejs.dev/) — Bundler
- [CSS](https://developer.mozilla.org/es/docs/Web/CSS) — Lenguaje de estilos
- [JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript) — Lenguaje de programación, incluyendo la implementación propia del Trie

## Contribuyendo

Aprecio cualquier sugerencia para mejorar el contenido de este proyecto. Si deseas contribuir, por favor crea un "issue" en el repositorio o contáctame directamente. Valoraré tus aportes para mejorar este repositorio.

## Autores

- **Mateo Álvarez Murillo** [drifterDev](https://github.com/drifterDev)
- **Efraín Gómez Ramírez** [EfraGR](https://github.com/EfraGR)
- **Libardo Jose Navarro Pedrozo** [LibardoNavarro](https://github.com/LibardoNavarro)

## Licencia

Los códigos incluidos en este proyecto están bajo la Licencia MIT. Para obtener más información, consulta el archivo [LICENSE](LICENSE) en la raíz del repositorio.
