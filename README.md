---
# Ubicar en la ruta

git init

####### Configuracion de la cuenta ######

git config --global user.name <name>
git config --global user.email <email>
git config --global user.password <key>
git remote add origin <https>

### Comandos para ver, registrar commits ###

git clone <http>
git status

git add .
git add -u
git add -A

git commit -m <"mi primer commit">
git log

##### Branchs #####

git branch <rama>
git branch -m <name>  <newName>
git switch <rama>
git switch -c <rama>
git checkout <branch>
git checkout <hashCommit>
git branch -d <branch>
git branch -D <branch>

###### GitHub ######

git diff <branch1>  <branch2>
git merge <branchOrigen> <branchDestino>
git push -u origin <main>
git pull origin <branch>

#para traer cambios si hay modificaciones desde github
git pull --rebase origin main

###### para guardar contraseña ######
git config --global credential.helper store

####------>>>>>cat ~/.git-credentials
### para que git ya no guarde passwords ###
git config --global --unset credential.helper



###### Para crear un repositorio desde git ######



pkg install gh

gh auth login

gh repo create <mi-proyecto> --public

## --private o --public ##



git remote add origin https://github.com/usuario/<mi-proyecto.git>

git branch -M main
git push -u origin main