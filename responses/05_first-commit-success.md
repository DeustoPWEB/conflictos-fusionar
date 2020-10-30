## ¿De dónde vienen los conflictos?

En un escenario del mundo real, es posible que un compañero o colega haya editado las mismas líneas del mismo archivo que tú en tu solicitud de extracción.

Para demostrarlo, voy a ser tu colega :wave:. En esta otra solicitud de extracción {{ secondPR }}, verás que el archivo `education` ha sido modificado. La otra solicitud de extracción se acaba de fusionar a `master`, lo cual significa que ahora hay un conflicto en tu solicitud de extracción.

## Paso 6: Resuelve nuevos conflictos

### :keyboard: Actividad: Resuelve el conflicto

{% if preferences.gitTool == 'cli' %}
1. Make sure master is up to date by checking out to `master`, and typing `git pull`. 
1. Resolve the conflicts locally by checking out to the `add-education` branch, merging `master`, and repeating your previous steps.
{% elsif preferences.gitTool == 'desktop' %}
1. Get any new changes by clicking **Fetch origin**.
1. Resolve the conflicts locally by checking out to the `add-education` branch, merging `master`, and repeating your previous steps.
{% else %}
1. In the "This branch has conflicts that must be resolved" section of the pull request, click **Resolve conflicts**.
{% endif %}

Como el conflicto lo has creado tú, siéntete libre de resolverlo como mejor te parezca.

<hr>
<h3 align="center">Vuelve a esta solicitud de extracción para los próximos pasos.</h3>
