
# Práctica del curso de git, gitHub y Sourcetree

---
## Ejercicio 1

1. ¿Qué comando utilizaste en el paso 11? ¿Por qué? 
    - El comando utilizado para deshacer el ultimo *commit* perdiendo los cambios en el *working copy* son:

       <code>git reset –hard HEAD~1 </code>
       
       El comando *git reset* permite deshacer cambios y junto con la opción --hard permite deshacer los cambios en el *working copy*.

2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
    - Los comandos utilizados para rehacer un *commit* son:

        <code>git reflog
        git reset --hard **473353f**</code>


      Con el comando *git reflog* se obtiene el histórico en donde han estado las referencias a *HEAD*, con esto se puede buscar el identificador del ultimo *commit*, el cual en este caso es **473353f** y finalmente ejecutar el comando <code>git reset –hard 473353f</code> para rehacer los cambios y recuperar el *commit* anteriormente eliminado.


     
3. El *merge* del paso 13, ¿Causó algún conflicto? ¿Por qué?
      - Al ejecutar el comando  <code>git merge master</code> de la rama **styled** a **master**, no se generan conflictos, pero tampoco se realiza un cambio, ya que la rama **styled** se encuentra 1 *commit* adelantada a la rama **master**, por lo tanto, la consola muestra la siguiente respuesta:

     <code>Already up to date.</code>

4. El *merge* del paso 19, ¿Causó algún conflicto? ¿Por qué?
     - En el momento que se realiza un *merge* de **htmlify** en la rama **styled** se genero el siguiente conflicto:
     
         <code>Auto-merging git-nuestro.md
              CONFLICT (content): Merge conflict in git-nuestro.md
              Automatic merge failed; fix conflicts and then commit the result.</code>
         
         La razón de este conflicto es porque tanto en  **htmlify** y **styled** modificaron la mismas parte del archivo git-nuestro.md y *git* no puede decidir con cuál es la versión correcta del archivo.
       


5. El *merge* del paso 21, ¿Causó algún conflicto? ¿Por qué?
    - En el momento de realizar un *commit* a la rama **styled** desde la rama **máster** no se generó ningún conflicto, ya que la rama **styled** estaba adelantada en *commits* y por lo tanto **master** pudo absorber a la rama **styled**
    
6. ¿Qué comando o comandos utilizaste en el paso 25?
     - El comando para obtener el diagrama por consola es: 
       
        <code>git log –graph</code> 

7. El *merge* del paso 26, ¿Podría ser *fast forward*? ¿Por qué?
    - Si podría ser *fast-forward*, porque no se ha añadido ningún *commit* luego de crear la rama **title**, entonces la posición del *HEAD* del **master** es una posición pasada al *HEAD* de la rama **title** por lo tanto el *HEAD* de la rama **master** se puede actualizar al *HEAD* de la rama **title** sin necesidad de crear un nuevo *commit*.

8. ¿Qué comando o comandos utilizaste en el paso 27?
    - El comando utilizado para deshacer el *merge* sin perder cambios del *working copy* es: 
      <code>git reset  HEAD~1</code>


9. ¿Qué comando o comandos utilizaste en el paso 28?
    -  El comando utilizado para descartar los cambios es:
        <code>git checkout -- git-nuestro.md</code>
10. ¿Qué comando o comandos utilizaste en el paso 29?
     -  Los comando utilizados para eliminar la rama **title** es:
     <code>git branch -D title</code>
11. ¿Qué comando o comandos utilizaste en el paso 30? 
     - El comando utilizado para rehacer el *merge* deshecho es:
      <code>git reflog
       git reset --hard 2be27c8</code>

12.  ¿Qué comando o comandos usaste en el paso 32? 
     - El comando utilizado para volver al *commit *inicial es:   
     <code>git reset –hard head~3</code>
13. ¿Qué comando o comandos usaste en el punto 33? 
     - El comando utilizado para volver al estado final es:  
      <code>git reset --hard 0f0c3b6</code>