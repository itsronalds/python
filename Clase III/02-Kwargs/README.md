# Uso de `**kwargs` en Funciones en Python

La palabra clave **`**kwargs`\*\* permite a las funciones recibir una cantidad indefinida de argumentos nombrados en forma de pares clave-valor. Estos argumentos son almacenados automáticamente en un diccionario, lo que los hace flexibles y fáciles de manejar.

> **Nota:** El término "kwargs" es un estándar de convención, pero puedes usar cualquier nombre precedido por `**`.

---

## ¿Cómo Usar `**kwargs` en Funciones?

Cuando definimos una función con `**kwargs`, podemos pasarle argumentos nombrados, y estos se almacenarán como un diccionario.

### Ejemplo Básico:

```python
# Definimos una función que recibe un diccionario mediante **kwargs
def print_values(**kwargs):
    for key, value in kwargs.items():
        print(f"{key} => {value}")

# Llamamos a la función pasando argumentos nombrados
print_values(name='Ronald', lastname='Abu Saleh', age=30)
```

**Salida:**

```
name => Ronald
lastname => Abu Saleh
age => 30
```

---

## Combinar `**kwargs` con Otros Parámetros

Puedes usar `**kwargs` junto con parámetros regulares. Los argumentos nombrados adicionales serán capturados por `**kwargs`.

### Ejemplo:

```python
# Definimos una función que combina un parámetro regular y **kwargs
def greetings(welcome, **kwargs):
    quote = f"{welcome} {kwargs['name']} {kwargs['lastname']} de {kwargs['age']} años"
    print(quote)

# Llamamos a la función con un mensaje de bienvenida y argumentos nombrados
greetings('Hola', name='Ronald', lastname='Abu Saleh', age=30)
```

**Salida:**

```
Hola Ronald Abu Saleh de 30 años
```

---

## Ventajas de Usar `**kwargs`

1. **Flexibilidad:** Permite manejar una cantidad variable de argumentos nombrados.
2. **Organización:** Almacena los argumentos en un diccionario, lo que facilita su manipulación.
3. **Compatibilidad:** Ideal para funciones genéricas que necesitan aceptar argumentos adicionales sin romper su estructura.

---

## Consideraciones

- Los argumentos pasados a `**kwargs` son almacenados como un diccionario, por lo que las claves deben ser únicas.
- `**kwargs` debe colocarse después de los parámetros posicionales y de `*args` en la definición de la función.

---

`**kwargs` es una herramienta poderosa para crear funciones versátiles y dinámicas. ¡Aprovecha su flexibilidad para mejorar tus proyectos en Python! 🚀
