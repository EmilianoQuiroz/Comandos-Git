# Comandos-Git

![image](https://user-images.githubusercontent.com/78452543/226786216-e9aff967-dc1e-4308-b629-c4875babf707.png)

## Git:
Es un software de "Control de Versiones" que fue diseñada por Linus Torvalds, es Open Source y muy potente, permite registrar el historial de cambios de un proyecto y facilita a los usuarios a llevar el seguimiento de los cambios de un archivo.

## Comandos importantes de Git:

### Establecemos los valores de configuración.

Ahora debemos establecer las variables de configuración global, que son muy importantes, especialmente si estás trabajando con otros desarrolladores. La principal ventaja de esto es que es más fácil averiguar quién ha hecho un commit de determinado bloque de código.

- git config puede ser usado para establecer una configuración específica de usuario, como el nombre de usuario ,y el email, etc.
        
        git config --global user.name "nombre"
        git config --global user.email "correo@correo.com2
   
- Habilitar la útil colorización del producto de la línea de comando.

        git config --global color.ui auto

- Ver la configuracion.

        git config --list
       
- Puedes establecer fácilmente un alias para cada comando mediante git config.

        git config --global alias.ci 'commit'

- Con este comando haremos que git detecte automaticamente lo que queremos escribir

        git config --global help.autocorrect 1
        
### Crear repositorios

- Iniciar un nuevo repositorio

        git init
