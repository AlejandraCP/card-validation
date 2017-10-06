# Función Tarjeta de crédito válida

**Esta función confirma la validez del número de una tarjeta por medio del algoritmo de Luhn.  
El usuario ingresará su número de tarjeta y se mostrará una ventana emergente informando si el número es válido o no.**

## Contenido  

* Archivos adjuntos.  
* Pseudocódigo de la función.  
* Diagrama de flujo.  

### Archivos adjuntos en repositorio
1. **Carpeta app** contiene archivo app.js en el cuál se ecuentra el código de la función con el lenguaje Javascript.  
2. **archivo index.html** está vinculado con app.js, el usuario podrá acceder a la función mediante este archivo.
3. **README.md** contiene pseudocódigo de la función y diagrama de flujo.  


### Pseudocódigo de la función Cifrado César  

* Inicio función Cifrado  
  * sum = 0
  * numberCard = mostrar('Escribe el número de tu tarjeta').separar caracteres().invertir orden(): solicita número.  
  * Mientras(numberCard.longitud < 16 || numberCard.longitud > 16) {
    numberCard = mostrar('El número de tu tarjeta debe contener solo 16 dígitos, vuelve a escribir el número de tu tarjeta.').split('').reverse(): solicita número.  
  }  
  * para ( i = 0; si i < numberCard.longitud; i+1){  
    * si(numberCard[i] === string vacío || numberCard[i] es NaN){
      numberCard = mostrar('No coloque espacios vacios o letras, vuelve a escribir el número de tu tarjeta. ').separar caracteres('').invertir orden(): solicita número.  
       }  

    }  
  * para ( j = 0; si j < numberCard.longitud; j+1){  
    var valueChar = ocnvertir(numberCard[j])  

    if(j % 2 === 0){
     sum += valueChar;
    }
    // Si el índice del elemento es impar, el elemento se multiplica por 2.
    if(j % 2 !== 0){
      // Si el producto es menor a 9, se adiciona a sum.
      if((valueChar * 2) <= 9 ){
       sum += (valueChar * 2);
       // Si el producto es mayor a 9, se separan los dígitos del producto y se suman.
      }
      if ((valueChar * 2) > 9){
        // El producto se convierte a string para separar los dígitos.
       var twoDigitis = (valueChar * 2).toString();
       var sumDigitis = parseInt(twoDigitis[0]) + parseInt(twoDigitis[1]);
       sum += sumDigitis;
      }
    }
  }
