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
  * Mientras(numberCard.longitud < 16 ó numberCard.longitud > 16) {  
    numberCard = mostrar('El número de tu tarjeta debe contener solo 16 dígitos, vuelve a escribir el número de tu tarjeta.').separar caracteres('').invertir orden(): solicita número.  
  }  
  * para ( i = 0; si i < numberCard.longitud; i+1){  
    * si( numberCard[i] === string vacío ó numberCard[i] es NaN){  
      numberCard = mostrar('No coloque espacios vacios o letras, vuelve a escribir el número de tu tarjeta. ').separar caracteres('').invertir orden(): solicita número.  
       }  

    }  
  * para ( j = 0; si j < numberCard.longitud; j+1){  
    valueChar = convertir a numéro(numberCard[j])  
      * si ( j / 2 resto es 0 ){  
        sum = sum + valueChar  
      }  
      * si ( j / 2 resto !== 0 ){  
          * si ((valueChar x 2) <= 9 ){  
            sum = sum + (valueChar x 2)  
          }  
          *  si ((valueChar x 2) > 9){  
            twoDigitis = (valueChar x 2).convertir a string()  
            sumDigitis = convertir a número(twoDigitis[primer dígito]) + convertir a número(twoDigitis[segundo dígito])  
            sum = sum + sumDigitis  
          }  

        }  

    }
  * si(sum / 10 resto es 0){  
    mostrar('El número de su tarjeta es valido')  
  }  
  sino  
   mostrar('El número de su tarjeta es invalido')  

  }
