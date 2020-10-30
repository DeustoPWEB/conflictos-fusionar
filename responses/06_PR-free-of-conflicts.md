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

