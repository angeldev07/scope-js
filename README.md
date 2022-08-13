
//Algunas notas sobre el scop

-¿Qué es el scope?
    En palabras sencillas, el scope es el alcance que tiene una variable dentro de nuestro código,es decir, que funciones, bloques de código y partes de nuestro código puede hacer uso de una varibale. Hay que tener en cuenta que las variables (let y const), las funciones y los objetos se contemplan también como variables, entonces el scope también las afecta.

Tenemos 3 tipos de scope en total:
    1. Global
    2. Function o de función
    3. Block 
   
-Tengamos previamente claro los conceptos de: declaración, asignación y redeclaración:
    - Si queremos declarar una varibale basta con poner la palabra reservada var, let o const + el nombre que va a tener nuestra Varible. Por ejemplo, queremos declarar una variable para que guarde un nombre, lo podemos hacer de la siguiente manera:
            - var nombre;
            - let nombre;
            - const nombre; (esto arroja un error. Lo explicaremos más adelante)   
    Ahora bien, cuando hablamos de asignación, nos estamos referiendo a 'darle' un valor a nuestra variable. Por ejemplo:
            - var edad = 16;
            - let nombre = "John Doe";
            - const numero = 5;
    ¿Notas algo raro? Así es, estamos declarando nuestra variable y a la vez asignando un valor. Sin embargo, no es necesario hacer esto en la misma linea de código. Podemos declarar nuestra variable y algunas lineas de código adelante asignarle un valor: 
            -let nombre; //aquí solo declaramos
             nombre = "John Doe" //aqui asignamos.

--Global Scope:
    El global scope hace referencia a toda variable, función u objeto que puede ser accedida desde cualquiera parte del código. Para declarar variables globales basta con declarar el pie de página de nuestro documento .js, es decir, sin encerrarla en un bloque de código.
    //Esto es una variable global
        let numero = 32145458

        function number() {
            //Esto es un error. 
            nombre = "angel"
            console.log(`${numero} ${nombre}`);
        }

        number()
        console.log(nombre);