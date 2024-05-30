
### Ejercicio 1: Crear y cambiar entre ramas

1. Clona el repositorio de ejemplo:
   ```bash
   git clone https://github.com/desarrolladoresTH/BootCamp-FullStack.git
   cd BootCamp-FullStack
   
   Si quieres que se muestren todos los archivos del repo
   ls -a 
   ```

2. Crea una nueva rama llamada `feature/nueva-caracteristica`:
   ```bash
   git branch feature/nueva-caracteristica
   ```

3. Cambia a la nueva rama creada:
   ```bash
   git checkout feature/nueva-caracteristica
   ```

4. Realiza algunos cambios en cualquier archivo y luego haz commit de esos cambios en la nueva rama.

### Ejercicio 2: Fusionar una rama con la principal

1. Asegúrate de estar en la rama principal:
   ```bash
   git checkout main
   ```

2. Actualiza la rama principal con los cambios de la rama `feature/nueva-caracteristica`:
   ```bash
   git merge feature/nueva-caracteristica
   ```

3. Resuelve cualquier conflicto que pueda surgir durante la fusión, si es necesario.

### Ejercicio 3: Eliminar una rama después de fusionar

1. Una vez que hayas fusionado la rama `feature/nueva-caracteristica` con éxito, puedes eliminarla:
   ```bash
   git branch -d feature/nueva-caracteristica
   ```

2. Verifica que la rama haya sido eliminada correctamente:
   ```bash
   git branch
   ```

### Ejercicio 4: Crear una nueva rama a partir de un commit anterior

1. Utiliza `git log` para encontrar el hash de un commit anterior al que te encuentras actualmente.

2. Crea una nueva rama llamada `hotfix/reparacion-bug` a partir del commit seleccionado:
   ```bash
   git checkout -b hotfix/reparacion-bug <HASH_DEL_COMMIT>
   ```

3. Realiza los cambios necesarios para corregir el error en la nueva rama y haz commit de esos cambios.


### Ejercicio 5: Revertir cambios en una rama

1. Cambia a la rama principal:
   ```bash
   git checkout main
   ```

2. Realiza algunos cambios en cualquier archivo y haz commit de esos cambios en la rama principal.

3. Ahora, descubre que esos cambios no eran necesarios y que necesitas revertirlos. Crea una nueva rama llamada `revertir-cambios` y cámbiate a ella:
   ```bash
   git checkout -b revertir-cambios
   ```

4. Utiliza `git log` para encontrar el hash del commit que deseas deshacer.

5. Revierte los cambios del commit seleccionado:
   ```bash
   git revert <HASH_DEL_COMMIT>
   ```

6. Resuelve cualquier conflicto que pueda surgir y haz commit del mensaje de revertido.

### Ejercicio 6: Resolver conflictos durante la fusión

1. Imagina que has estado trabajando en una nueva característica en la rama `feature/nueva-caracteristica` y alguien más ha realizado cambios en la rama principal (`main`).

2. Cambia a la rama principal y realiza algunos cambios diferentes en el mismo archivo que has modificado en la rama de la nueva característica.

3. Intenta fusionar la rama `feature/nueva-caracteristica` con la rama principal:
   ```bash
   git checkout main
   git merge feature/nueva-caracteristica
   ```

4. Resuelve los conflictos que surjan durante la fusión, utilizando un editor de texto para decidir qué cambios mantener y qué cambios descartar.

### Ejercicio 7: Restaurar una rama eliminada

1. Supongamos que por error eliminaste la rama `feature/nueva-caracteristica`.

2. Utiliza `git reflog` para encontrar el hash del commit más reciente en la rama `feature/nueva-caracteristica`.

3. Crea una nueva rama con ese commit:
   ```bash
   git checkout -b feature/nueva-caracteristica <HASH_DEL_COMMIT>
   ```

4. Verifica que la rama se haya restaurado correctamente y que todos los cambios estén presentes.

