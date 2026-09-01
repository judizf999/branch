# branch
branch (rama)
# 1. Edita o crea un archivo
echo "Nueva funcionalidad" >> archivo.txt

# 2. Verifica el estado
git status

# 3. Agrega los cambios al área de preparación
git add archivo.txt

# 4. Confirma los cambios (commit)
git commit -m "Agrega nueva funcionalidad de login"

# 5. Sube la rama al repositorio remoto
git push origin feature-login
# 1. Cámbiate a la rama que va a RECIBIR los cambios (normalmente main)
git checkout main

# 2. Asegúrate de tener la última versión de main
git pull origin main

# 3. Fusiona la otra rama dentro de main
git merge feature-login
git push origin main
git branch -d feature-login          # elimina localmente
git push origin --delete feature-login   # elimina en el remoto
Auto-merging archivo.txt
CONFLICT (content): Merge conflict in archivo.txt
Automatic merge failed; fix conflicts and then commit the result.
<<<<<<< HEAD
Este es el texto de la rama main
=======
Este es el texto de la rama feature-login
>>>>>>> feature-login
>>>>>>> git add archivo.txt
>>>>>>>    git commit -m "Resuelve conflicto entre main y feature-login"
>>>>>>>    git push origin main
>>>>>>>    git commit -m "Resuelve conflicto entre main y feature-login"
