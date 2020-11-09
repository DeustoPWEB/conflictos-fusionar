# Bienvenida a Gestionar conflictos al fusionar :tada:

Hola, y ¡bienvenida! Si estás aquí para aprender acerca de los conflictos al fusionar, y practicar, estás en el lugar correcto.

En este curso aprenderás por qué ocurren los conflictos al fusionar y resolverás unos pocos. Los conflictos de fusión de este curso son lo suficientemente sencillos como para que puedas resolverlo desde la interfaz web de GitHub.com. Aunque, si lo prefieres, puedes resolverlos usando la línea de comandos o alguna otra herramienta local.

Como extra, ¡el proyecto que usaremos para este curso es un CV alojado en [GitHub Pages](https://help.github.com/en/categories/github-pages-basics)! Así que, si quieres seguir trabajando en él después de completar este curso, por supuesto puedes seguir haciéndolo.

Antes de que empieces este curso recomendamos que completes la [Introduction a GitHub]({{ host }}/{{ course.Owner.login }}/introduction-to-github). 

> Nota: Puede que te des cuenta de que ya existen algunas ramas y solicitudes de extracción. Las iremos usando más tarde en las actividades de este curso.

### Cómo ocurren los conflictos de fusión

Un **conflicto de fusión** ocurre cuando se han realizado cambios al mismo fragmento del mismo archivo en dos ramas diferentes. Generalmente te darás cuenta de que hay un conflicto durante una solicitud de extracción.

Esto puede resultar intimidatorio, pero no te asustes, Git sabe cómo gestionarlo. Solamente necesita un ser humano que decida cómo resolver el conflicto.

## Paso 1: Resuelve un conflicto sencillo

Puede que fusiones muchas solicitudes de extracción antes de siquiera encontrarte con tu primer conflicto de fusión. Esto es porque Git es inteligente en lo que respecta a las fusiones. A no ser que estés siguiendo muy de cerca las demás ramas, no sabrás que hay un conflicto hasta que crees una solicitud de extracción.

Esta rama es un gran ejemplo. En este escenario, dos de nuestros amigos han estado trabajando en este repositorio. Ambos han creado ramas, han hecho cambios al archivo `_config.yml`, y han abierto solicitudes de extracción. Una solicitud de extracción se ha fusionado con `master` sin ningún problema, pero la otra tiene un conflicto.

El histórico de `master` y esta rama tiene un aspecto parecido a esto:

![deviated branches](https://user-images.githubusercontent.com/13326548/36703493-b8f4d5ee-1b10-11e8-9f95-4ec9993fe704.png)

Como esta solicitud de extracción cambia las mismas líneas del archivo `_config.yml`, hay un conflicto de fusión. 

Ayudemos a nuestros amigos a resolver este conflicto.

### :keyboard: Actividad: Resuelve tu primer conflicto de fusión

{% if preferences.gitTool == 'cli' %}

1. Open your preferred command line interface, which we'll call your shell from now on.
1. Clone this repository:
      ```shell
     git clone {{ thePayload.repository.clone_url }}
      ```
1. Navigate to the repository in your shell:
      ```shell
      cd {{ thePayload.repository.name }}
      ```
1. Checkout to the `update-config` branch and ensure it is up to date:
    ```shell
    git checkout update-config
    git pull
    ```
1. Merge the `master` branch into the `update-config` branch. To ensure that you're working with an up to date copy of `master`, we'll use its remote tracking branch:
    ```shell
    git merge origin/master
    ```
1. In Git's response, you'll see the file with the conflict. Open it in your text editor.
1. Look for the marked hunks that begin with  `<<<<<<<  update-config` and ends with `>>>>>>> master`. These markers are added by Git to show you the content that is in conflict.
1. Remove the changes made on the master branch by deleting all of the content below the `=======` and above `>>>>>>> master`.
1. Next, remove the merge conflict markers by deleting the following lines:

       <<<<<<< update-config
       =======
        >>>>>>> master

1. Save and close the file. Stage and commit your changes:
    ```shell
    git add .
    git commit -m "merge master into update-config"
    ```
1. Push your merged branches to GitHub:
    ```shell
    git push
    ```

{% elsif preferences.gitTool == 'vscode' %}
1. En VS Code, abre la Paleta de Comandos (o _Command Palette_) usando <kbd>Ctrl+Mayús+P</kbd> en Windows, o <kbd>⌘+Mayús+P</kbd> en macOS. También puedes seguir [la documentación oficial de VS Code](https://code.visualstudio.com/docs/editor/versioncontrol#_cloning-a-repository) sobre clonar repositorios.
1. Escribe `git clone`y presiona <kbd>Enter</kbd>
2. Pega la URL del repositorio en la nueva ventana y presiona <kbd>Enter</kbd>:
      ```shell
      {{ thePayload.repository.clone_url }}
      ```
3. Selecciona la ubicación en el que quieres guardar el repositorio y haz clic en **Choose folder**. Después, abre la ubicación que seleccionaste (haciendo clic en **Open**).  
4.  En la pestaña **Source Control**, haz clic en los puntos suspensivos y selecciona **Pull** para asegurarte de que está actualizada.
5. Haz clic en `master` en la parte inferior de la ventana de VS Code. Esto abrirá la Paleta de Comandos con todos los comandos relacionados a ramas de Git; selecciona la rama `origin/update-config` 
6. Fusiona `master` a la rama `update-config`. Para esto, teclea <kbd>Ctrl+Mayús+P</kbd> o <kbd>⌘+Mayús+P</kbd>, empieza a escribir "git merge" y selecciona "Git: Merge Branch...". Selecciona la rama que quieres fusionar: en este caso, `master`
7. Se abrirá una ventana en la parte inferior derecha informando de que existen conflictos, que puedes cerrar. En la barra lateral, los archivos con conflictos se muestran bajo el desplegable "Merge Changes" y con una `C` a su derecha. Abre el archivo `_config.yml` para editarlo
8. Busca el fragmento marcado que empieza con `<<<<<<<  HEAD` y termina con `>>>>>>> master`. Estos marcadores los añade Git para señalarte el contenido que está generando el conflicto. 
9.  Elimina los cambios realizados sobre la rama `master` borrando todo el contenido debajo de `=======` y por encima de `>>>>>>> master`.
10. Después, elimina los marcadores de conflicto suprimiendo las siguientes líneas:
       ```
       <<<<<<< update-config
       =======
        >>>>>>> master
        
11. Guarda el archivo. Desde la pestaña **Source Control**, añade el archivo recién modificado (debajo de "Merge changes") a la confirmación de cambios, escribe un mensaje descriptivo y presiona <kbd>Ctrl+Enter</kbd> o <kbd>Cmd+Enter</kbd> para realizar una confirmación de cambios.
12. Haz clic en los puntos suspensivos y presiona **Push**.

{% elsif preferences.gitTool == 'desktop' %}

1. First, make sure you have [GitHub Desktop](https://desktop.github.com/) installed and [configured](https://help.github.com/en/desktop/getting-started-with-github-desktop/authenticating-to-github). 
2. On the `code` tab of this repository, click the green **Clone or download** button. Click **Open in Desktop**. 
3. In GitHub Desktop, confirm the blue **Clone** button in the pop up window. 
4. Checkout to the `update-config` branch by clicking **Current branch**, and selecting `update-config`. 
5. Merge `master` into the `update-config` branch by clicking **Current branch**, and selecting **Choose a branch to merge into update-config**. 
6. Select the `master` branch, and click **Merge master into update-config**.
7. You'll be prompted about the merge conflict, and asked if you'd like to resolve it in your default editor. Click the button to open the file in your default editor. 
8. Look for the marked hunks that begin with  `<<<<<<<  update-config` and ends with `>>>>>>> master`. These markers are added by Git to show you the content that is in conflict.
9. Remove the changes made on the master branch by deleting all of the content below the `=======` and above `>>>>>>> master`.
10. Next, remove the merge conflict markers by deleting the following lines:

       <<<<<<< update-config
       =======
        >>>>>> master

11. Save and close the file.
12. Back in GitHub Desktop, click **Commit merge**.
13. Push your changes back to the remote by clicking **Push origin**.

{% else %}

1. At the bottom of the page in the "This branch has conflicts that must be resolved" section of the Pull Request, click the **Resolve conflicts** button.
2. Look for the highlighted sections that begins with  `<<<<<<<  update-config` and ends with `>>>>>>> master`. These markers are added by Git to show you the content that is in conflict.
3. Remove the changes made on the master branch by deleting all of the content below the `=======` and above `>>>>>>> master`.
4. Next, remove the merge conflict markers by deleting the following lines:

       <<<<<<< update-config
       =======
        >>>>>>> master

5. With the merge conflict markers removed, click **Mark as resolved**.
6. Finally, click **Commit merge**.

{% endif %}

> A veces, la mejor manera de resolver un conflicto de fusión es añadir contenido de las dos ramas, ¡o incluso algo que no está en ninguna! Esta es la razón por la que Git necesita un ser humano que mire el código y haga los cambios apropiados.

<hr>
<h3 align="center">Mira mi respuesta más abajo.</h3>

