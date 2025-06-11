# Actividad 1: Configuración de Entorno de Desarrollo Web

## Datos del Estudiante
* **Nombre:** Jorge Arcibar Gonzalez
* **Matrícula:** Al03003955
* **Carrera:** Ingeniería en Desarrollo de Software
* **Semestre:** Séptimo Semestre

## Datos de la Materia
* **Nombre:** Diseño de Aplicaciones Web
* **Profesor:** Carlos Ignacio Hernández Nolasco

---

## ¿Qué es Markdown y para qué se usa?

**Markdown** es un **lenguaje de marcado ligero** que nos permite dar formato a texto plano de una manera sencilla y legible. Fue creado con la idea de que el documento fuente sea fácil de leer y escribir por humanos, sin necesidad de un software especial.

Se utiliza principalmente para:

* **Documentación de proyectos:** Es muy común en plataformas como GitHub para archivos `README.md` que describen el proyecto.
* **Creación de contenido web:** Blogs, artículos, y páginas web.
* **Notas y listas:** Para organizar ideas rápidamente.
* **Mensajes:** En foros y chats donde se requiere un formato simple.

La sintaxis de Markdown es intuitiva. Por ejemplo:
* Los encabezados se crean con `#` (uno para Título 1, dos para Título 2, etc.).
* El texto en **negritas** se logra con `**doble asterisco**`.
* El texto en *cursiva* con `*un solo asterisco*`.
* Las listas con guiones (`-`) o asteriscos (`*`).
* Los enlaces con `[Texto](URL)`.

Markdown facilita la conversión a otros formatos como HTML, lo que lo hace muy versátil para la web y la documentación.

---

## Opciones de Marcado en Markdown

Markdown ofrece una variedad de opciones sencillas para formatear texto. Aquí algunas de las más comunes y útiles:

* **Encabezados:** Se definen con el símbolo `#`. Un `#` es para el título más grande (H1), `##` para H2, y así sucesivamente hasta `######` (H6).
    * Ejemplo: `# Título Principal`, `## Subtítulo`

* **Párrafos y Saltos de Línea:** Un párrafo se crea simplemente escribiendo texto. Para un salto de línea, se necesitan dos espacios al final de la línea o una línea en blanco entre párrafos.

* **Énfasis (Negritas e Itálicas):**
    * **Negritas:** Se usan dos asteriscos (`**texto**`) o dos guiones bajos (`__texto__`).
    * Itálicas: Se usa un asterisco (`*texto*`) o un guion bajo (`_texto_`).
    * Combinación: `**_texto_**`

* **Listas:**
    * **Listas desordenadas (sin orden):** Se usan guiones (`-`), asteriscos (`*`) o signos de más (`+`).
        * Ejemplo:
            ```markdown
            - Primer elemento
            - Segundo elemento
            * Tercer elemento
            ```
    * **Listas ordenadas:** Se usan números seguidos de un punto.
        * Ejemplo:
            ```markdown
            1. Primer elemento
            2. Segundo elemento
            ```

* **Bloques de Código:**
    * Para código en línea: Se encierra el texto entre comillas invertidas simples (backticks ` ``código`` `).
    * Para bloques de código: Se encierran con tres comillas invertidas (triple backtick ` ``` `) al inicio y al final, y opcionalmente se puede especificar el lenguaje para resaltado de sintaxis.
        * Ejemplo:
            ```
            ```python
            print("Hola Mundo")
            ```
            ```

* **Enlaces:** Se crean con `[Texto del Enlace](URL)`.
    * Ejemplo: `[Mi GitHub](https://github.com/jorgearcibargon)`

* **Imágenes:** Similar a los enlaces, pero con un signo de exclamación `!` al principio: `![Texto Alternativo](URL_de_la_imagen)`.

* **Citas en Bloque:** Se usa el símbolo `>` al principio de la línea.
    * Ejemplo: `> Esta es una cita de un texto.`

* **Líneas Horizontales:** Se crean con tres o más guiones (`---`), asteriscos (`***`) o guiones bajos (`___`).

---

## Comandos Esenciales de Git

Aquí se listan comandos fundamentales de Git, cruciales para el control de versiones de proyectos:

### 1. Verificar el estado de un repositorio local

* **`git status`**: Muestra el estado de tu directorio de trabajo y el área de preparación. Te indica qué archivos han sido modificados, cuáles están listos para ser "commiteados", y cuáles no están siendo rastreados por Git.
    * Ejemplo de uso:
        ```bash
        git status
        ```

### 2. Añadir archivos individualmente o globalmente al área de preparación (staging area)

* **`git add <nombre_del_archivo>`**: Prepara archivos específicos para el próximo commit.
    * Ejemplo de uso:
        ```bash
        git add mi_archivo.html
        ```
* **`git add .`**: Prepara todos los archivos nuevos y modificados en el directorio actual y subdirectorios para el próximo commit.
    * Ejemplo de uso:
        ```bash
        git add .
        ```

### 3. Añadir comentarios a un commit

* **`git commit -m "Tu mensaje descriptivo"`**: Guarda los cambios preparados en el historial del repositorio con un mensaje que describe los cambios. El mensaje debe ser conciso y claro.
    * Ejemplo de uso:
        ```bash
        git commit -m "Sección de navegación añadida en el footer."
        ```
* **`git commit -am "Tu mensaje"`**: Una combinación de `git add .` y `git commit -m "..."`. Solo funciona para archivos ya rastreados por Git. No añade archivos nuevos.
    * Ejemplo de uso:
        ```bash
        git commit -am "Cambios menores en el CSS."
        ```

### 4. Subir tus cambios al repositorio remoto

* **`git push <nombre_del_remoto> <nombre_de_la_rama>`**: Sube los commits de tu repositorio local a un repositorio remoto.
    * El remoto suele ser `origin` (el nombre por defecto de GitHub).
    * La rama suele ser `main` o `master`.
    * Ejemplo de uso:
        ```bash
        git push origin main
        ```
* **`git push -u origin main`**: La primera vez que haces un `push` a una rama nueva, usas `-u` para establecer el "upstream", lo que te permite usar `git push` (sin `origin main`) en el envío de comandos en el futuro para esa rama.
    * Ejemplo de uso:
        ```bash
        git push -u origin main
        ```

### 5. Crear, navegar y eliminar ramas

* **`git branch`**: Lista todas las ramas en tu repositorio local. La rama actual se marca con un asterisco.
    * Ejemplo de uso:
        ```bash
        git branch
        ```
* **`git branch <nombre_de_la_rama>`**: Crea una nueva rama, pero no te cambia a ella.
    * Ejemplo de uso:
        ```bash
        git branch nueva-funcionalidad
        ```
* **`git checkout <nombre_de_la_rama>`**: Cambia a la rama especificada.
    * Ejemplo de uso:
        ```bash
        git checkout nueva-funcionalidad
        ```
* **`git checkout -b <nombre_de_la_rama>`**: Una abreviatura para crear una nueva rama Y cambiarte a ella inmediatamente.
    * Ejemplo de uso:
        ```bash
        git checkout -b desarrollo-rapido
        ```
* **`git branch -d <nombre_de_la_rama>`**: Elimina la rama localmente. Solo puedes eliminar ramas que ya se han fusionado o que no estés usando.
    * Ejemplo de uso:
        ```bash
        git branch -d rama-terminada
        ```
* **`git push origin --delete <nombre_de_la_rama>`**: Elimina una rama en el repositorio remoto.
    * Ejemplo de uso:
        ```bash
        git push origin --delete rama-vieja
        ```

### 6. Revertir un repositorio a un commit específico

* **`git log`**: Muestra el historial de commits. Necesitarás el *hash* (ID único) del commit al que quieres regresar.
    * Ejemplo de uso:
        ```bash
        git log
        ```
* **`git reset --hard <hash_del_commit>`**: **ADVERTENCIA: Este comando es destructivo.** Mueve la rama actual al commit especificado y descarta todos los cambios posteriores en tu directorio de trabajo. Úsalo con extrema precaución.
    * Ejemplo de uso:
        ```bash
        git reset --hard a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9t0
        ```
* **`git revert <hash_del_commit>`**: Crea un nuevo commit que deshace los cambios de un commit anterior. Es una forma más segura de "deshacer" cambios porque mantiene el historial intacto.
    * Ejemplo de uso:
        ```bash
        git revert f0e9d8c7b6a5e4d3c2b1a0f9e8d7c6b5a4s3d2f1
        ```