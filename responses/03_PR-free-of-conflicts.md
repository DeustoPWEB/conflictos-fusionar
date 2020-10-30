## Paso 4: Fusiona la solicitud de extracción

Buen trabajo @{{ user.username }}, tu solicitud de extracción está libre de conflictos. :tada:

> Ya he aprobado esta solicitud de extracción, así que si todavía ves "Review required" en la vista de fusión, prueba a recargar la página.

### :keyboard: Actividad: Fusiona esta solicitud de extracción

Adelante, fusiona esta solicitud de extracción ahora.

1. Haz clic en **Merge pull request** abajo.
1. Haz clic en **Confirm merge**.
1. Haz clic en **Delete branch** y prepárate para tu siguiente actividad.

{% if preferences.gitTool == 'cli' %}
You can also merge locally:
1. Checkout to the master branch:
    ```shell
    git checkout master
    ```
1. Ensure the master branch is up to date:
    ```shell
    git pull
    ```
1. Merge the `{{ branch }}` branch:
    ```shell
    git merge {{ branch }}
    ```
1. Enter a commit message, if asked.
1. Push your merged branches up to GitHub:
    ```shell
    git push
{% endif %}

<hr>
<h3 align="center">Mira mi respuesta más abajo.</h3>
