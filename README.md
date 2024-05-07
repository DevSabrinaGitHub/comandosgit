# comandosgit

#editar nombres, emails en forma global:  
git config --global user.email "nuestro email"
git confif --global user.name "nuestro nombre"

#acceder a las listas o cambios:
git config --global list 


#crear repositorio en git desde cualquier disco 
cd c: 

//nombre carpeta que crearemos:
mkdir nombrecarpeta

//eliminar una carpeta: 
rmdir nombrecarpeta


//acceder a la carpeta para crear un archivo: 
cd nombrecarpeta

//una vez que entramos a la carpeta, creamos el archivo: 
mkdir nombrearchivo

//comenzamos a usar git
//iniciamos git: 
git init

//entramos al cd con el nombre de la carpeya y luego archivo: 
cd nombrecarpeta
cd nombrearchivo

//mostrar archivos:
ls


//añadir archivos (si o si para ver lo que se realiza en el archivo sea cambios del codigo , elimaciones etc) :
git add nombrearchivo.extension 


//ver o mostrar el codigo que se ha eliminado: 
//ejemplo si en ese archivo en visual ponemos hola, mundo y eliminamos ( , mundo) lo que hace ckeckout es mostrar nuevamente el codigo que se elimino:
git checkout nombrearchivo.extension

//cuando realizamos un cambio en git y queremos que el codigo que borramos o modificamos ya no aparezca:
//tenemos el archivo nuevo con los datos nuevos.
//por ultimo: 
git add nombrearchivo.extension y guarda los cambios, ya no muestra el codigo anterior
//presionamos:
git checkout nombrearchivo.extension 
//nos muestra el codigo tal y como dejamos.


//volver al codigo que se ha eliminado
git commit -m "volviendo al codigo" -a
// llamamos a la funcion para mostrar nuevamente lo borrado en vsc
git reset --hard  volviendo al codigo 




//ejemplo a realizar: 

//entramos a visual
//escribimos un codigo en el archivo: hola, mundo
//borramos una porcion de un codigo: .mundo
// git ckeckout nombrearchivo.extension : muestra el codigo borrado en vsc, vuelve a aparecer hola, mundo


//evitamos eso:
//escribimos de nuevo el codigo que queremos guardar : hola
//guardamos: git add nombrearchivo.extension
// ver cambios: git checkout nombrearchivo.txt
// muestra solamente hola ahora

//queremos que nos vuelva  a aparecer : ,mundo
// git reset --hard 
// en vsc vuelve el codigo : hola, mundo


//cambiar el nombre de un archivo: 
git mv nombrearchivo.extension  nombrearchivoNUEVO.extension
//guardamos 
git add nombrearchivoNUEVO.txt

//ver el estado de git (mostar cualquier cambio de codigo o archivo) 
git status 


//CUALQUIER CAMBIO QUE SE REALIZA EN UN ARCHIVO SIEMPRE LO DEBEMOS GUARDAR CON EL COMANDO : git add nombrearchivo.extension

//ver codigos que se agrego con:
git show archivo.txt

(acordar guardar con add) 

//comando que nos muestra quien hizo un cambio en el codigo/ obtener identificacion del commit: 
git log

//comando para ver el id en abreviatura chiquita
git log --oneline

//cambiar numero del commit id: 
git config --global core.abbrev 5
//nos imprime el id en 5 digitos


//ver que cambios realizamos o que codigos agregamos/eliminamos: 
git diff 
git add archivo.extension
git diff
git diff --stage
git status 

//subir a github los cambios: 
//vamos a github, copiamos el codigo que nos muestra en nuestra repo
git remote add origin linkdelperfilyrepo
//pegamos en la terminal de git
//copiamos del github y pegamos en la terminal
git push -u origin main 
//enter y nos indica que debemos poner el nombre de usuario de github y contraseña
