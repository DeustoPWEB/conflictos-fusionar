## Paso 5: Crea tu propio conflicto

Hasta ahora, esta solicitud de extracción no tiene ningún conflicto. He añadido algunas protecciones adicionales a las ramas para evitar que combines nada antes de que esté listo.

En la última actividad, has resuelto un conflicto creado por otra persona. Esta vez vas a crear el conflicto de fusión tú misma/o.

### :keyboard: Actividad: Haz cambios en esta rama

{% if preferences.gitTool == 'cli' %}
1. Check out to this branch:
    ```shell
    git checkout add-education
    ```
1. Open `_data/education.yml` in your text editor.
1. Modify the content in the `degree:`, `uni:`, `year:`, and `summary:` lines.
1. Stage and commit the changes:
    ```shell
    git add _data/education.yml
    git commit -m "<YOUR-MESSAGE>"
    ```
1. Push your changes to GitHub:
    ```shell
    git push
    ```
{% elsif preferences.gitTool == 'vscode' %}
1. Cámbiate a la rama `add-education` haciendo clic en el nombre de la rama activa en la barra azul de la parte inferior en VS Code.
2. Abre el archivo `_data/education.yml`.
3. Modifica el contenido de las líneas `degree:`, `uni:`, `year:`, y `summary:`.
4. Guarda los cambios al archivo.
5. En la pestaña **Source Control**, añade el archivo `_data/education.yml` a la confirmación de cambios, escribe un mensaje descriptivo y presiona <kbd>Ctrl+Enter</kbd> o <kbd>Cmd+Enter</kbd>
6. Haz clic en los puntos suspensivos y presiona **Push**
{% elsif preferences.gitTool == 'desktop' %}
1. Checkout to the `add-education` branch.
1. Merge `master` into the `add-education` branch.
1. Open the `_data/education.yml` file in your default editor. 
1. Modify the content in the `degree:`, `uni:`, `year:`, and `summary:` lines.
1. Save and close the file.
2. Back in GitHub Desktop, see that your changes are staged for commit because the box next to the title is checked on the left side. 
1. Enter a short and descriptive commit message, and click **Commit to add-education**. 
3. Push your changes back to the remote by clicking **Push origin**.
{% else %}
1. Click on the **Files changed** tab in this pull request.
1. Click ![octicon-kebab-horizontal] in the top right-hand corner of the `_data/education.yml` file that had been previously modified.
1. Click **Edit file** to open the file editor.
1. Modify the content in the `degree:`, `uni:`, `year:`, and `summary:` lines.
1. Scroll to the bottom of the page and enter a commit message for your change.
1. Click the **Commit changes** button, making sure the "Commit directly to the **add-education** branch" option is selected.
{% endif %}
<hr>
<h3 align="center">Mira mi respuesta más abajo.</h3>

[octicon-kebab-horizontal]: https://unpkg.com/octicons/build/svg/kebab-horizontal.svg
