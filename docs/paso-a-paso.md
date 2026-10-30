# Práctica guiada: un issue, GitHub Projects y Toggl Track

**Objetivo:** iniciar y verificar un registro de tiempo de Toggl asociado con un issue que también está en un GitHub Project v2.

**Duración:** 10–15 minutos.

**No se requiere:** API, token, sincronización automática ni configuración de automatizaciones.

## Los tres objetos

| Servicio | Objeto de esta práctica | Qué hace |
|---|---|---|
| GitHub, repositorio | Issue `#1` (o el número que tenga en la URL) | Describe el trabajo y conserva discusión y criterios de aceptación. |
| GitHub Projects | Tarjeta que apunta al issue | Permite ordenar y actualizar el estado del trabajo. |
| Toggl Track | Proyecto de Toggl y entrada de tiempo | Registra cuánto tiempo dedica una persona a la tarea. |

Aunque el repositorio y el Project estén vinculados, el **proyecto de Toggl es otro objeto**. Nombrar igual el Project y el proyecto de Toggl no sincroniza sus campos.

## Antes de empezar

- Tener iniciada sesión en GitHub y poder abrir el repositorio y su Project.
- Tener instalada y abierta la extensión oficial de Toggl Track en Chrome, Firefox o Edge, con sesión iniciada.
- Tener acceso a un Workspace de Toggl. Seleccionar un proyecto de Toggl si ya existe; si no, para la demostración se puede registrar la entrada sin proyecto.
- Mantener la misma cuenta/perfil de navegador durante el recorrido; una ventana privada o un perfil distinto puede no tener iniciada la sesión de la extensión.

## Paso 1. Comprueba que la tarjeta es un issue real

1. Abre el [Project de demostración](https://github.com/orgs/IES-Rafael-Alberti/projects/REEMPLAZAR).
2. Abre la tarjeta **Preparar una ficha de ayuda para conectar Toggl con un issue**.
3. Comprueba que muestra un enlace a un issue del repositorio. La dirección debe terminar en `/issues/NÚMERO`.
4. Abre ese enlace para llegar a la página del issue.

**Si la tarjeta es un borrador:** un borrador pertenece únicamente al Project; todavía no es un issue del repositorio y no tiene URL `/issues/NÚMERO`. Usa el menú de la tarjeta para convertirlo en issue y selecciona este repositorio. Después abre el issue creado.

> Para esta demostración, no empieces desde la vista del tablero: abre el issue del repositorio. Es ahí donde la integración del navegador puede reconocer el contexto de GitHub.

## Paso 2. Comprueba la integración de Toggl

1. Abre la extensión de Toggl Track.
2. Entra en su configuración y busca **Integrations**.
3. Comprueba que **GitHub** está habilitado. Los nombres exactos pueden variar ligeramente con la versión o el idioma.
4. Vuelve a la página del issue y recárgala si la tenías abierta.

## Paso 3. Inicia el temporizador desde GitHub

1. En la página del issue, busca el botón o enlace de Toggl para iniciar el temporizador.
2. Antes de empezar, comprueba la descripción y el proyecto de Toggl sugeridos.
3. Selecciona el proyecto de Toggl adecuado, si corresponde.
4. Inicia el temporizador y comprueba en la extensión que está corriendo.

Si la descripción automática no identifica bien la tarea, usa este formato:

```text
IES-Rafael-Alberti/demo-toggl-github-projects#N | revisar criterios del issue | URL_DEL_ISSUE
```

El `#N` se sustituye por el número real que aparece en la URL del issue.

## Paso 4. Plan B: iniciar el registro manualmente

Si el botón de Toggl **no aparece** en GitHub:

1. Copia la URL del issue del repositorio.
2. Abre la extensión de Toggl y crea una entrada nueva.
3. Escribe en la descripción el identificador `repositorio#N`, una acción concreta y la URL.
4. Selecciona el proyecto de Toggl si existe y comienza el temporizador.
5. Comprueba en la extensión que el tiempo está corriendo.

Este método registra el tiempo igual de válido; la extensión solo evita escribir algunos datos a mano.

## Paso 5. Detén y comprueba el registro

1. Detén el temporizador tras una breve acción de demostración.
2. Abre los registros de Toggl y comprueba que la entrada quedó guardada, con la duración, descripción y proyecto que esperabas.
3. Vuelve al Project de GitHub y actualiza el estado de la tarjeta según el trabajo real.

El estado del Project **no cambia** al detener el temporizador. La entrada de Toggl tampoco demuestra por sí sola que el criterio de aceptación del issue se haya cumplido.

## Si falla la integración

| Síntoma | Comprobación / solución |
|---|---|
| No aparece el botón de Toggl | Verifica sesión y GitHub habilitado en Integrations, recarga el issue y prueba en un navegador/perfil compatible. Usa el plan B manual si sigue sin aparecer. |
| La tarjeta no tiene número ni URL `/issues/N` | Probablemente es un borrador. Conviértelo en issue y vuelve a abrirlo desde el repositorio. |
| El botón inicia con otro proyecto o descripción | Corrige esos campos antes de guardar y verifica la entrada al terminar. |
| Toggl registra tiempo pero la tarjeta no cambia | Es el comportamiento esperado: actualiza el estado del Project por separado. |
| La extensión funciona en la página del issue pero no en el tablero | Sigue usando el issue del repositorio como punto de inicio. No es necesario iniciar el temporizador desde la tarjeta. |

## Resultado esperado

- La tarjeta del Project enlaza a un issue real del repositorio.
- El issue puede abrirse en una URL `/issues/N`.
- Toggl Track contiene una entrada guardada con identificador del issue y duración.
- El estado del Project se revisa y actualiza de forma independiente.

## Documentación consultada

- [Toggl Track: integración con GitHub](https://toggl.com/integrations/github).
- [Toggl Track: extensión del navegador](https://support.toggl.com/en-us/article/toggl-track-browser-extension-132qk56/).
- [GitHub Docs: añadir issues y borradores a un Project](https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-items-in-your-project/adding-items-to-your-project).
- Documentación consultada el 30/10/2026. La ubicación y los rótulos de los controles pueden cambiar.
