# Regex

Referencias sobre expresiones regulares.

## Caracteres de búsqueda

| Operación | Descripción |
| ----- | ---- |
| `.` | Encuentra cualquier carácter, excepto saltos de líneas. |
| `\d` | Encuentra cualquier dígito entre 0-9. |
| `\D` | Encuentra todo lo que no sea un digito. |
| `[0-9]` | Realiza la misma función que `\d`. |
| `\w` | Encuentra cualquier letra, mayúscula o minúscula, incluyendo números. |
| `\W` | Encuentra todo lo contrario a `\w`. |
| `[a-zA-Z0-9]` | Realiza la misma búsqueda si combinamos `[\w\d]`. |
| `\s` | Encuentra donde hay espacios, ya sea que fueron hechos con tab o barra espaciadora. |
| `\S` | Encuentra todo lo que no sea espacio o todo lo contrario a `\s`. |
| `[a-zA-Z]` | Encontrar todos los caracteres del abecedario. |
| `*` | Es un delimitador y significa cero o muchas coincidencias. |
| `+` | Es un delimitador y significa una o muchas coincidencias. |
| `?` | Es un delimitador y significa cero o una sola coincidencia. También ayuda a reducir los matches |
| `^`| Encuentra todo lo contrario a la expresión que esté después de dicho carácter. Es la forma de negar una expresión definida. |
| `[^0-9]` | Encontrará todo carácter que no sea número (ejemplo de negación). |
| `\t` | Encuentra espacio realizado con tabulador. |
| `\r` | Encuentra retorno de carro o inicio. |
| `\n` | Encuentra las líneas nuevas. |
| `{X,Y}` | X y Y se reemplaza con números, el cual sirve para definir entre un rango válido para encuntrar una expresión definida. Por ejemplo: `\d{1,3}`, encuentra entre uno a tres dígitos que estén seguidos uno del otro. |
| `{X,}` | X se reemplaza con un número, el cual indica que encuentra una expresión definida que cumpla al menos X ocurrencias. |
| `^` | Indica el inicio de una línea. |
| `$` | Indica el final de una línea. |
| `^$` | La combinación de los caracteres inicio y fin el cual abarquen una expresión regular, ayuda a filtrar las líneas completas que no cumplan con la expresión definida. |
| `(XYZ)` | Los paréntesis agrupan expresiones regulares y son útiles para definir un patrón de repetición, ejemplo: `^(\d{2,2}\s?){3}$`. La regex anterior, encuentra 3 pares de números separados por un espacio entre ellos: `23 34 56`. Sin paréntesis, la regex quedaría: `^\d{2,2}\s\d{2,2}\s\d{2,2}$`. Adicionalmente, sirve para realizar reemplazos, obteniendo el match que hay dentro del paréntesis y colocándolo en una nueva cadena de información, haciendo uso de variables como $1, $2, etc... |