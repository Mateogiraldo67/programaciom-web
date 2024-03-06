// Ejemplo de uso:
console.log(numeroDeCaracteres("Hola mundo", "o"));   // Devuelve 2 (hay 2 'o' en la cadena)
console.log(numeroDeCaracteres("abcdefg", "e"));     // Devuelve 1 (hay 1 'e' en la cadena)
console.log(numeroDeCaracteres("aaaaaa", "a"));      // Devuelve 6 (hay 6 'a' en la cadena)

/*/Escribir una función llamada sumarArreglo que reciba un arreglo de números y retorne la suma de todos los elementos./*/
function sumarArreglo(arreglo) {
    let suma = 0;
    for (let i = 0; i < arreglo.length; i++) {
        suma += arreglo[i];
    }
    return suma;
}

// Ejemplo de uso:
console.log(sumarArreglo([1, 2, 3, 4, 5]));  // Devuelve 15 (1 + 2 + 3 + 4 + 5 = 15)
console.log(sumarArreglo([10, -5, 8]));      // Devuelve 13 (10 + (-5) + 8 = 13)

/*/Escribir una función llamada multiplicarArreglo que reciba un arreglo de números y retorne la multiplicación de todos los elementos./*/

function multiplicarArreglo(arreglo) {
    let multiplicacion = 1;
    for (let i = 0; i < arreglo.length; i++) {
        multiplicacion *= arreglo[i];
    }
    return multiplicacion;
}

// Ejemplo de uso:
console.log(multiplicarArreglo([1, 2, 3, 4, 5]));  // Devuelve 120 (1 * 2 * 3 * 4 * 5 = 120)
console.log(multiplicarArreglo([10, -5, 8]));      // Devuelve -400 (10 * (-5) * 8 = -400)

/*/Escribir una función llamada removerCeros que reciba un arreglo de números y retorne un nuevo arreglo excluyendo los ceros (0)./*/
function removerCeros(arreglo) {
    return arreglo.filter(numero => numero !== 0);
}

// Ejemplo de uso:
console.log(removerCeros([1, 0, 5, 0, 3]));      // Devuelve [1, 5, 3]
console.log(removerCeros([0, 0, 0, 0]));        // Devuelve []
console.log(removerCeros([-5, 0, 10, 0, -8]));  // Devuelve [-5, 10, -8]

/*/Escribir una función llamada sumarArreglo que reciba tres argumentos: un arreglo de números, la posición inicial y la posición final. La función debe retornar la suma de todos los números dentro del rango (la posición inicial y la posición final, incluyéndolas).

Nota: puedes asumir que la posición inicial va a ser menor o igual a la posición final, y que están dentro de los límites del arreglo./*/

function sumarArreglo(arreglo, inicio, final) {
    let suma = 0;
    for (let i = inicio; i <= final; i++) {
        suma += arreglo[i];
    }
    return suma;
}

// Ejemplo de uso:
console.log(sumarArreglo([1, 2, 3, 4, 5], 1, 3));  // Devuelve 9 (2 + 3 + 4 = 9)
console.log(sumarArreglo([10, -5, 8, 2, 6], 0, 2)); // Devuelve 13 (10 + (-5) + 8 = 13)


/*/Escribir una función llamada transcribir que reciba un string (una cadena de ADN) y retorne otro string (su complemento ARN).

Los complementos son los siguientes:

G -> C
C -> G
T -> A
A -> U
/*/
function transcribir(cadenaADN) {
    let cadenaARN = "";
    for (let i = 0; i < cadenaADN.length; i++) {
        switch (cadenaADN[i]) {
            case 'G':
                cadenaARN += 'C';
                break;
            case 'C':
                cadenaARN += 'G';
                break;
            case 'T':
                cadenaARN += 'A';
                break;
            case 'A':
                cadenaARN += 'U';
                break;
            default:
                // Si el carácter no es G, C, T o A, simplemente lo copiamos
                cadenaARN += cadenaADN[i];
        }
    }
    return cadenaARN;
}

// Ejemplo de uso:
console.log(transcribir("GCTA"));  // Devuelve "CGAU"
console.log(transcribir("ACGT"));  // Devuelve "UGCA"

/*/Escribir una función llamada capitalizar que reciba un string y capitalice la primera letra:/*/
function capitalizar(cadena) {
    return cadena.charAt(0).toUpperCase() + cadena.slice(1);
}

// Ejemplo de uso:
console.log(capitalizar("hola mundo"));  // Devuelve "Hola mundo"
console.log(capitalizar("javascript")); // Devuelve "Javascript"

/*/Escribir una función llamada capitalizar que reciba un string y capitalice la primera letra de cada palabra:/*/
function capitalizar(cadena) {
    return cadena.replace(/\b\w/g, function(char) {
        return char.toUpperCase();
    });
}

// Ejemplo de uso:
console.log(capitalizar("hola mundo"));          // Devuelve "Hola Mundo"
console.log(capitalizar("javascript es genial")); // Devuelve "Javascript Es Genial"

/*/Escribir una función llamada max que reciba un arreglo de números y retorne el número máximo:

Nota: Intentarlo hacer sin el método Math.max de JavaScript./*/
function max(arreglo) {
    if (arreglo.length === 0) {
        return undefined; // Si el arreglo está vacío, retornamos undefined
    }

    let maximo = arreglo[0]; // Tomamos el primer número como el máximo inicialmente
    for (let i = 1; i < arreglo.length; i++) {
        if (arreglo[i] > maximo) {
            maximo = arreglo[i]; // Si encontramos un número mayor, actualizamos el máximo
        }
    }
    return maximo;
}

// Ejemplo de uso:
console.log(max([3, 7, 2, 10, 5]));    // Devuelve 10 (el número máximo en el arreglo)
console.log(max([-5, -3, -9, -1]));     // Devuelve -1 (el número máximo en el arreglo)
console.log(max([]));                  // Devuelve undefined (el arreglo está vacío)

/*/Escribir una función llamada min que reciba un arreglo de números y retorne el número mínimo:

Nota: Intentarlo hacer sin el método Math.min de JavaScript./*/


function min(arreglo) {
    if (arreglo.length === 0) {
        return undefined; // Si el arreglo está vacío, retornamos undefined
    }

    let minimo = arreglo[0]; // Tomamos el primer número como el mínimo inicialmente
    for (let i = 1; i < arreglo.length; i++) {
        if (arreglo[i] < minimo) {
            minimo = arreglo[i]; // Si encontramos un número menor, actualizamos el mínimo
        }
    }
    return minimo;
}

// Ejemplo de uso:
console.log(min([3, 7, 2, 10, 5]));    // Devuelve 2 (el número mínimo en el arreglo)
console.log(min([-5, -3, -9, -1]));     // Devuelve -9 (el número mínimo en el arreglo)
console.log(min([]));                  // Devuelve undefined (el arreglo está vacío)


/*/Escribir una función llamada password que reciba un string y retorne un nuevo string realizando los siguientes cambios:

Las mayúsculas se reemplazan por minúsculas.
Se eliminan los espacios en blanco.
Reemplaza el caracter “a” por “4”.
Reemplaza el caracter “e” por “3”.
Reemplaza el caracter “i” por “1”.
Reemplaza el carater “o” por “0”./*/

function password(cadena) {
    // Convertir mayúsculas a minúsculas
    cadena = cadena.toLowerCase();
    
    // Eliminar espacios en blanco
    cadena = cadena.replace(/\s/g, '');
    
    // Reemplazar caracteres según las reglas dadas
    cadena = cadena.replace(/a/g, '4');
    cadena = cadena.replace(/e/g, '3');
    cadena = cadena.replace(/i/g, '1');
    cadena = cadena.replace(/o/g, '0');
    
    return cadena;
}

// Ejemplo de uso:
console.log(password("Hola Mundo"));        // Devuelve "h0l4mund0"
console.log(password("OpenAI es increíble")); // Devuelve "0p3n41esincr31bl3"
