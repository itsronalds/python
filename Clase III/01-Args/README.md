# Uso de `*args` en Funciones en Python

La palabra clave **`*args`** permite a las funciones recibir un número indefinido de argumentos posicionales. Es particularmente útil cuando no se sabe cuántos valores se pasarán a una función al momento de su definición.

> Los valores pasados mediante `*args` se almacenan en forma de una **tupla**, lo que facilita su iteración y manipulación.

---

## ¿Cómo Usar `*args` en Funciones?

Cuando se utiliza `*args` en la definición de una función, se pueden pasar múltiples valores como parámetros sin necesidad de especificar cada uno explícitamente.

### Ejemplo Básico:

```python
# Definimos una función que acepte un número indefinido de parámetros
def print_numbers(*args):
    for num in args:
        print(num)

# Llamamos a la función con múltiples valores
print_numbers(1, 10, 20, 40, 0, 10)
```

**Salida:**

```
1
10
20
40
0
10
```

---

## Combinar `*args` con Otros Parámetros

Las funciones pueden utilizar `*args` junto con parámetros definidos explícitamente. Los argumentos posicionales regulares se deben declarar primero.

### Ejemplo:

```python
# Definimos una función que utiliza un parámetro regular y *args
def add_to_all(plus_number, *args):
    new_numbers = []

    for number in args:
        new_numbers.append(number + plus_number)

    return new_numbers

# Llamamos a la función pasando un número base y una serie de valores
result = add_to_all(5, 10, 15, 20, 25, 30)

# Imprimimos el resultado
print(result)
```

**Salida:**

```
[15, 20, 25, 30, 35]
```

---

## Ventajas de Usar `*args`

1. **Flexibilidad:** Permite que una función acepte múltiples argumentos sin necesidad de conocer la cantidad exacta de antemano.
2. **Compatibilidad:** Facilita el trabajo con datos dinámicos o listas de valores como entrada.
3. **Simplicidad:** Reduce la necesidad de escribir múltiples parámetros en la definición de la función.

---

## Consideraciones

- Los valores pasados a `*args` se almacenan en una **tupla**, por lo que son **inmutables**.
- `*args` debe colocarse después de los parámetros posicionales regulares en la definición de la función.

---

Utilizar `*args` es una práctica fundamental en Python para escribir funciones dinámicas y versátiles. ¡Experimenta con ellas para aprovechar al máximo su flexibilidad! 🚀
