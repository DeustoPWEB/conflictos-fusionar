## Paso 7: Fusiona la solicitud de extracción

Buen trabajo, @{{ user.username }}, tu solicitud de extracción está libre de conflictos. :tada: Adelante, puedes fusionar esta solicitud de extracción ahora. 
 
### :keyboard: Actividad: Fusiona esta solicitud de extracción

1. Haz clic en **Merge pull request** abajo.
1. Haz clic en **Confirm merge**.
1. Haz clic en **Delete branch** y prepárate para tu siguiente actividad.

{% if preferences.gitTool == 'cli' %}
You can also merge locally:
1. Checkout to the master branch:
    ```shell
    git checkout master
    ```
2. Ensure the master branch is up to date:
    ```shell
    git pull
    ```
3. Merge the `{{ branch }}` branch:
    ```shell
    git merge {{ branch }}
    ```
4. Enter a commit message, if asked.
5. Push your merged branches up to GitHub:
    ```shell
    git push
    ```
{% elsif preferences.gitTool == 'vscode' %}
1. Cámbiate a la rama `add-experience` haciendo clic en el nombre de la rama activa en la barra azul de la parte inferior en VS Code, y asegúrate de que está actualizada desde la pestaña **Source Control**, haciendo clic en los puntos suspensivos y seleccionando **Pull**.
2. Fusiona `master` a la rama `add-experience`. Teclea <kbd>Ctrl+Mayús+P</kbd> o <kbd>⌘+Mayús+P</kbd>, empieza a escribir "git merge" y selecciona "Git: Merge Branch..." [Go on...]
3. Verás que hay dos archivos con conflictos: `_data/experience.yml` y `_data/interests.yml`.
4. Abre `_data/experience.yml`, elimina los marcadores de conflicto y deja el contenido que quieras conservar. Guarda los cambios.
5. Con los conflictos de fusión resueltos y los marcadores eliminados del archivo `_data/experience.yml` añade el archivo a la confirmación de cambios haciendo clic en `+` al lado del nombre del archivo en la pestaña **Source Control**.
6. Abre `_data/interests.yml`, elimina los marcadores de conflicto y deja el contenido que quieras conservar. Guarda los cambios.
7. Desde la pestaña **Source Control**, añade el archivo `_data/interests.yml` (haciendo clic en `+`), escribe un mensaje descriptivo y presiona <kbd>Ctrl+Enter</kbd> o <kbd>Cmd+Enter</kbd> para realizar una confirmación de cambios.
8. Haz clic en los puntos suspensivos y presiona **Push**.
{% elsif preferences.gitTool == 'desktop' %}
You can also merge locally:
1. Checkout to the `master` branch.
2. Ensure the branch is up to date by clicking **Fetch origin**. 
3. Merge `{{ branch}} ` into the `master` branch by clicking **Current branch**, and selecting **Choose a branch to merge into master**. 
4. Select the `{{ branch }}` branch, and click **Merge {{ branch }} into master**.
5. Push your changes back to the remote by clicking **Push origin**.
{% endif %}

<hr>
<h3 align="center">Mira mi respuesta más abajo.</h3>

