¡Lo has conseguido, @{{ user.username }}! Buen trabajo resolviendo ese conflicto. La mayoría de conflictos en tu día a día serán bastante sencillos, como el de esta actividad. Puede que necesites discutir la resolución con tu equipo. Si estáis trabajando juntos y revisando las solicitudes de extracción, resolver conflictos es fácil.

### ¿Qué acaba de pasar?

Resolver un conflicto no fusiona atuomáticamente una solicitud de extracción en GitHub. En ves de eso, almacena la resolucion en una confirmación de cambios de fusión y te permite a ti y a tu equipo seguir trabajando.

Para resolver un conflicto, GitHub realiza lo que se conoce como *fusión inversa*. Esto significa que los cambios de la rama `master` se han fusionado a tu rama `update-config`. 

Con una fusión inversa, solamente se actualiza la rama `update-config`. Esto te permite probar el código resuelto en tu rama antes de que lo fusiones a `master`. La rama `master` debería tratarse como lista para publicación, o código libre de errores.

## Paso 2: Fusiona la primera solicitud de extracción resuelta

Adelante, fusiona esta solicitud de extracción ahora.

> Ya he aprobado esta solicitud de extracción, así que si todavía ves "Review required" en la vista de fusión, prueba a recargar la página.
> 
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
    ```
{% elsif preferences.gitTool == 'desktop' %}
You can also merge locally:
1. Checkout to the `master` branch by clicking **Current branch**, and selecting `master`.
1. Ensure the branch is up to date by clicking **Fetch origin**. 
2. Merge `{{ branch}} ` into the `master` branch by clicking **Current branch**, and selecting **Choose a branch to merge into master**. 
3. Select the `{{ branch }}` branch, and click **Merge {{ branch }} into master**.
4. Push your changes back to the remote by clicking **Push origin**.
{% endif %}

<hr>
<h3 align="center">Mira mi respuesta más abajo.</h3>