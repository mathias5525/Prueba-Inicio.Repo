# Cargar la llave SSH pública en GitHub

## Generar y copiar la llave SSH pública

Para copiar la llave pública, debes ir a la carpeta `.ssh` en tu computadora.  
Allí encontrarás un archivo con extensión `.pub` (por ejemplo, `id_rsa.pub`).

Puedes abrir este archivo con un editor de texto (como el Bloc de notas o VS Code) y copiar todo el contenido que contiene.

---

## Agregar la llave SSH a GitHub

1. Inicia sesión en tu cuenta de **GitHub**.  
2. Ve a **Settings → SSH and GPG keys**.  
3. Crea una nueva clave haciendo clic en **New SSH Key**.  
4. Asigna un nombre descriptivo (por ejemplo, el nombre del ordenador donde estás trabajando).  
5. Pega el contenido de la llave pública en el campo correspondiente.  
6. Guarda los cambios.  

> 💡 **Consejo:** Es recomendable que cada computadora o dispositivo tenga su propia llave SSH para acceder a tu cuenta de GitHub.

---

## Comandos básicos de Git

```bash
git branch
