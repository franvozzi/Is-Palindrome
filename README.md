# Is Palindrome?
Leetcode problem number 9.

```text
Given an integer x, return true if x is a palindrome, and false otherwise.


Example 1:

Input: x = 121
Output: true
Explanation: 121 reads as 121 from left to right and from right to left.
Example 2:

Input: x = -121
Output: false
Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.
Example 3:

Input: x = 10
Output: false
Explanation: Reads 01 from right to left. Therefore it is not a palindrome.
```

## Mi primer solución: Two Pointers (Dos punteros)
¿Qué es un palíndromo? Es una palabra o frase cuyas letras están dispuestas de tal manera que resulta la misma leída de izquierda a derecha que de derecha a izquierda.
La lógica de este problema es verificar si una palabra es palíndromo o no.

En este challenge se nos proporciona un ```integer```, mi idea fue convertirlo a String y luego hacer un split de caracteres.
Luego, comparar ambas "puntas" de la palabra si es igual a la otra. Si es palíndromo = true, sino return false.

```javascript
function isPalindrome(x: number): boolean {
    if (x < 0) {return false }
    const str = String(x)
    for (let i = 0;i < Math.floor(str.length / 2); i++) {
        if (str[i] !== str[str.length - i - 1]){
            return false;
        }    
    }
    return true;   
};
```

## Segunda solución: Enfoque Numérico
Primero, verificamos si el número es positivo o negativo. Si es true seguimos, sino el algoritmo se acaba (false).
Luego, guardamos una variable ```original``` y otra ```reversed``` en otra.
