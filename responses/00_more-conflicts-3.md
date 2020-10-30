## Paso 3: Resuelve conflictos más complejos

Exactamente ingual que tu primer conflicto, esta solicitud de extracción ya es _conflictiva_ (porque tiene un conflicto).

Esta vez, sin embargo, lo he hecho un poquito más complicado.

- En lugar de un conflicto, ¡tienes tres!
- En vez de un solo archivo con conflictos, ¡tienes dos!  
- De hecho uno de tus archivos tiene algunos marcadores de conflicto antiguos. Esto puede ocurrir si alguien se olvida de eliminar los marcadores al resolver un conflicto.

### :keyboard: Actividad: Resuelve estos conflictos

{% if preferences.gitTool == 'cli' %}
1. Checkout to the `add-experience` branch and ensure it is up to date:
    ```shell
    git checkout add-experience
    git pull
    ```
1. Merge the `master` branch into the `add-experience` branch. To ensure that you're working with an up to date copy of `master`, we'll use its remote tracking branch:
    ```shell
    git merge origin/master
    ```
1. In Git's response, you'll see two files with conflicts: `_data/experience.yml` and `_data/interests.yml`.
1. Open `_data/experience.yml` in your text editor.
1. Remove the conflict markers and pick your desired content. 
1. With the merge conflicts resolved and the markers removed in the `_data/experience.yml` file, stage the file:
    ```shell
    git add _data/experience.yml
    ```
1. Open the next file in your text editor: `_data/interests.yml`.
1. Remove the conflict markers and pick your desired content. 
1.  Close the file. Stage it and commit your changes:
    ```shell
    git add _data/interests.yml
    git commit -m "merge master into add-experience"
    ```
11. Push your merged branches to GitHub:
    ```shell
    git push
    ```
{% elsif preferences.gitTool == 'vscode' %}
1. Cámbiate a la rama `add-experience` haciendo clic en el nombre de la rama activa en la barra azul de la parte inferior en VS Code, y asegúrate de que está actualizada desde la pestaña **Source Control**, haciendo clic en los puntos suspensivos y seleccionando **Pull**.
2. Fusiona `master` a la rama `add-experience`. Teclea <kbd>Ctrl+Mayús+P</kbd> o <kbd>⌘+Mayús+P</kbd>, empieza a escribir "git merge" y selecciona "Git: Merge Branch...", y selecciona la rama `master`. Se abrirá una ventana en la parte inferior derecha informando de que existen conflictos, que puedes cerrar. 
3. En la pestaña **Source Control**, los archivos con conflictos se muestran bajo el desplegable "Merge Changes" y con una `C` a su derecha. Verás que hay dos archivos con conflictos: `_data/experience.yml` y `_data/interests.yml`.
4. Abre `_data/experience.yml`, elimina los marcadores de conflicto y deja el contenido que quieras conservar. Guarda los cambios.
5. Con los conflictos de fusión resueltos y los marcadores eliminados del archivo `_data/experience.yml`, añade el archivo a la confirmación de cambios haciendo clic en `+` al lado del nombre del archivo en la pestaña **Source Control**.
6. Abre `_data/interests.yml`, elimina los marcadores de conflicto y deja el contenido que quieras conservar. Guarda los cambios.
7. Desde la pestaña **Source Control**, añade el archivo `_data/interests.yml` (haciendo clic en `+`), escribe un mensaje descriptivo y presiona <kbd>Ctrl+Enter</kbd> o <kbd>Cmd+Enter</kbd> para realizar una confirmación de cambios.
8. Haz clic en los puntos suspensivos y presiona **Push**.
{% elsif preferences.gitTool == 'desktop' %}
1. Checkout to the `add-experience` branch by clicking **Current branch**, and selecting `add-experience`. 
2. Merge `master` into the `add-experience` branch by clicking **Current branch**, and selecting **Choose a branch to merge into update-config**. 
3. Select the `master` branch, and click **Merge master into update-config**.
4. You'll be prompted about the merge conflict, and asked if you'd like to resolve it in your default editor. Click the button to open each file in your default editor. 
5. Remove the conflict markers and pick your desired content for each file. 
6. Save and close the files.
7. Back in GitHub Desktop, click **Commit merge**.
8. Push your changes back to the remote by clicking **Push origin**.
{% else %}
1. Click **Resolve conflicts**.
1. On the left, you will notice two files listed: `_data/experience.yml` and `_data/interests.yml`. Let's start with `_data/experience.yml`.
1. Remove the conflict markers and pick your desired content. 
1. With the merge conflicts resolved and the markers removed in the `_data/experience.yml` file, click **Mark as resolved**.
1. GitHub will present the next file with conflicts, `_data/interests.yml`.
1. Remove the conflict markers and pick your desired content. 
1. When you are finished, click **Mark as resolved**.
1. Click **Commit merge**.
{% endif %}
<hr>
<h3 align="center">Mira mi respuesta más abajo.</h3>

