# Crear y actualizar repositorio en Git y GitHub en Linux

1. Crear un repositorio en **GitHub**.

   ![01](/home/alanr/Documentos/Markdown/Git y GitHub/images/01.png)

2. Al crear el repositorio de dará un enlace, que nos será útil más adelante.

   ![02](/home/alanr/Documentos/Markdown/Git y GitHub/images/02.png)

3. Abrir la Terminal dentro de la **carpeta** que contiene **todos** los archivos y carpetas del proyecto.

   ```bas
   alanr@alanr-HP-Compaq-6000-Pro-SFF-PC: ~Escritorio/Ejemplo-Git-GitHub$ 
   ```

4. Ingresar el comando <**git init**> para inicializar el repositorio.

   ```bash
   git init
   Inicializando repositorio Git vacío en /home/alanr/Escritorio/Ejemplo-Git-GitHub/.git/
   ```

5. Ahora hay que agregar los archivos y para esto tenemos dos formas:

   1. Agregar los archivos de uno por uno con el comando <**add**>

      ```bash
      git add index.html
      git add images/beautiful_sunset_18-wallpaper-1280x1024.jpg
      ```

   2. Agregar **todos** los archivos dentro de la carpeta con el comando <**add .**>

      ```bash
      git add .
      ```

6. Agregaremos una descripción de la actualización en el repositorio. Haremos esto con el comando <**git commit -m "<Descripcion de la actualizacion>"**>

   ```bash
   git commit -m "Primer commit"
   [master (commit-raíz) 815643f] Primer commit
    2 files changed, 10 insertions(+)
    create mode 100644 images/beautiful_sunset_18-wallpaper-1280x1024.jpg
    create mode 100644 index.html
   ```

7. Después, agregamos la rama principal con el comando <**git branch -M <u>Rama</u>**>

   ```bash
   git branch -M main
   ```

8. En este punto ya tenemos el seguimiento del repositorio de manera local en nuestro equipo, pero todavía no está en el repositorio de GitHub, para esto haremos lo siguiente:

   1. Copiar el enlace que GitHub nos proporcionó al crear el repositorio.

      https://github.com/aldanaalaan/Ejemplo-Git-GitHub.git

   2. Ejercitar el comando  <**git remote add origin <u>Enlace al repositorio</u>**>

      ```bash
      git remote add origin https://github.com/aldanaalaan/Ejemplo-Git-GitHub.git
      ```

   3. Comando <**git push origin main**> e ingresamos nuestro usuario y contraseña de GitHub.

      ```bash
      git push origin main
      Username for 'https://github.com': aldanaalaan
      Password for 'https://aldanaalaan@github.com': 
      Enumerando objetos: 5, listo.
      Contando objetos: 100% (5/5), listo.
      Compresión delta usando hasta 2 hilos
      Comprimiendo objetos: 100% (5/5), listo.
      Escribiendo objetos: 100% (5/5), 425.88 KiB | 19.36 MiB/s, listo.
      Total 5 (delta 0), reusado 0 (delta 0)
      To https://github.com/aldanaalaan/Ejemplo-Git-GitHub.git
       * [new branch]      main -> main
      ```

Para realizar actualizaciones del repositorio y subirlas a GitHub, necesitamos repetir los pasos **5** y  **6**, después ejecutar el comando <**git push origin main**> y volver a ingresar nuestro usuario y contraseña de GitHub.

```bash
git add .
git commit -m "Segundo commit"
[main cb5bda2] Segundo commit
 1 file changed, 2 insertions(+), 2 deletions(-)
git push origin main
Username for 'https://github.com': aldanaalaan
Password for 'https://aldanaalaan@github.com': 
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 2 hilos
Comprimiendo objetos: 100% (3/3), listo.
Escribiendo objetos: 100% (3/3), 340 bytes | 340.00 KiB/s, listo.
Total 3 (delta 1), reusado 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/aldanaalaan/Ejemplo-Git-GitHub.git
   815643f..cb5bda2  main -> main
```

Y ahora al entrar a GitHub tenemos un repositorio con dos commits con todos los archivos y modificaciones realizadas.

![03](/home/alanr/Documentos/Markdown/Git y GitHub/images/03.png)
