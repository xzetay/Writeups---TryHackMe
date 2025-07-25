![Pasted image 20250709140547.png]]

### Enumeracion

![[Pasted image 20250709141829.png]]

### Pagina web:

![[Pasted image 20250709141916.png]]

### Primer fuzzeo:

![[Pasted image 20250709143132.png]]

### Pagina web encontrada:

![[Pasted image 20250709143155.png]]

En este lugar hay algo oculto, no se puede ver a simple vista pero si arrastramos todo el texto aparecera:

![[Pasted image 20250709143241.png]]

### El segundo fuzzeo muestra otro directorio:

![[Pasted image 20250709143446.png]]

Es una pagina web con un video:

![[Pasted image 20250709143507.png]]

Hay un mensaje en el codigo fuente de la pagina web:

![[Pasted image 20250709143531.png]]

Parece ser que hay un archivo .`ticket`:
El tercer fuzzeo mostro un archivo:

![[Pasted image 20250709143842.png]]

Lo que hay adentro de el:

![[Pasted image 20250709143900.png]]

Aqui dice que solo es la ficha para ingresar a Queen's Gambit:
En este caso el cifrado esta en Base 58:

![[Pasted image 20250709144102.png]]

### Procedemos a decodificar:

![[Pasted image 20250709144152.png]]

Es la contraseña del usuario oculto `vigilante`:

![[Pasted image 20250709144243.png]]

Tambien se encontro otro usuario:

![[Pasted image 20250709151754.png]]

Viendo los binarios de cada imagen se puede ver lo siguiente:

![[Pasted image 20250709144813.png]]

Se ve que el tercer archivo hay una parte del encabezado que hace ilusión a un tipo de imagen .`PNG`, pero otro que no, se deberá cambiar este valor para continuar:

Editaremos el archivo, se usara `hexedit`:

![[Pasted image 20250709151620.png]]

Los valores antes mostrados se cambiaran para que este ahora en PNG se modifican valores hexadecimales

Ahora si se puede ver la imagen:

![[Pasted image 20250709151638.png]]

Esta contraseña sirve para abrir `aa.jpg`:

![[Pasted image 20250709152054.png]]

Hay un archivo llamado `shado`:

![[Pasted image 20250709152120.png]]

Y otro llamado `password.txt`:

![[Pasted image 20250709152158.png]]

En esta maquina la contraseña del SSH es `M3tahuman`:

![[Pasted image 20250709152444.png]]

### Flag:

![[Pasted image 20250709152508.png]]

Viendo que podemos ejecutar como root encontramos lo siguiente:

![[Pasted image 20250709152558.png]]

Simplemente busque en GFTOBins como explotar el binario y listo:

### Flag:

![[Pasted image 20250709152639.png]]

---














