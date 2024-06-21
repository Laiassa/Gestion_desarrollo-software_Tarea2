# Gestion de Calidad y desarrollo de software, Tarea2
Desarrollar un flujo de trabajo basado en troncales

En este README haremos un breve resumen de la clase de gestion de codigo y tipos de flujo de trabajo.

Fede hara resumen de git Flow  
Igna hara resumen de GitLab Flow  
Ludmi hara resumen de GitHub Flow   
... hara el resumen de  desarrollo Troncal  


Federico: gitflow es un workflow propuesto por Git el cual provee estabilidad y una estructura solida para la organizacion de las
ramas en un entorno de controlador de versiones. Al tener ramas bien definidas con sus tareas especificas nos aseguramos de que
los problemas se presenten de manera temprana, pudiendo resolverlos antes de que entren a produccion. 
las desventajas son: la cantidad de conflictos que surgen al manejar tanta cantidad de ramas, y el tiempo que demoran los cambios
en llegar a produccion. La gran cantidad de ramas existentes tambien se vuelven dificiles de manejar, requiriendo un equipo 
dedicado a su mantenimiento.

## GitHub Flow

GitHub Flow es un proceso de trabajo (workflow) simple y efectivo para manejar el desarrollo de software con Git y GitHub. Es particularmente útil para proyectos con *despliegue continuo*. 

### Principios Básicos de GitHub Flow

1. **Branching**:
    - **Crear una rama**: Cada nueva característica o corrección de errores se desarrolla en su propia rama separada del `main`. La convención es nombrar la rama según la característica o el problema que estás resolviendo.
    ```sh
    git checkout -b nombre-de-la-rama
    ```

2. **Commits**:
    - **Realizar commits frecuentemente**: A medida que trabajas en tu rama, realiza commits de tus cambios frecuentemente con mensajes claros y descriptivos.

    ```sh
    git add .
    git commit -m "Descripción clara del cambio"
    ```

3. **Push**:
    - **Push de la rama**: Sube (push) tu rama a GitHub regularmente. Esto permite tener un respaldo de tu trabajo y facilita la colaboración con otros.

    ```sh
    git push origin nombre-de-la-rama
    ```
4. **Pull Request**:
    - **Abrir un Pull Request**: Una vez que hayas terminado de trabajar en tu rama, abre un Pull Request (PR) en GitHub. Esto inicia una conversación sobre los cambios y permite la revisión del código por parte de tus compañeros de equipo. Un PR puede abrirse incluso antes de que los cambios estén completos, lo que permite la revisión continua.

5. **Revisión y Discusión**:
    - **Revisión de código**: Los compañeros de equipo revisan el PR, comentan sobre el código y sugieren cambios. Se pueden realizar más commits en la misma rama para abordar los comentarios y sugerencias.

6. **Integración y Merge**:
    - **Merge a `main`**: Una vez que el PR ha sido aprobado y todas las pruebas han pasado, se puede hacer merge de la rama a `main`. Es una buena práctica usar la opción de "Squash and merge" para combinar todos los commits en uno solo antes de integrarlos en `main`.

    ```sh
    git checkout main
    git pull origin main
    git merge --squash nombre-de-la-rama
    git push origin main
    ```

7. **Despliegue**:
    - **Despliegue continuo**: Si tu proyecto está configurado para despliegue continuo, los cambios en `main` se desplegarán automáticamente a producción. De lo contrario, se puede desplegar manualmente según las políticas de tu equipo.

### Beneficios de GitHub Flow

- **Simplicidad**: Es fácil de entender y seguir.
- **Colaboración**: Facilita la colaboración entre desarrolladores mediante la revisión de código y los comentarios en PRs.
- **Integración continua**: Se integra bien con prácticas de integración y despliegue continuo.
- **Trazabilidad**: Cada cambio en `main` es revisado y discutido, lo que mejora la calidad del código.

Siguiendo estos pasos y principios, GitHub Flow ayuda a mantener un desarrollo de software organizado, colaborativo y eficiente.
