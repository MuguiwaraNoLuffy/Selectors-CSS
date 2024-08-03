# Felix Josue Lopez 2021-0116
Clase
# Definiciones de Selectores CSS

## Selectores de ID
- **`#fancy`**: Selecciona el elemento con el id "fancy". En HTML, los ids son únicos, por lo que este selector seleccionará un solo elemento.
- **`#fancy pickle`**: Selecciona todos los elementos `<pickle>` que están contenidos dentro del elemento con id "fancy". Esto aplica solo si `<pickle>` es un descendiente de un elemento con id "fancy".

## Selectores de Clase
- **`.small`**: Selecciona todos los elementos que tienen asignada la clase "small". Los selectores de clase son útiles para aplicar estilos a grupos de elementos.
- **`orange.small`**: Selecciona todos los elementos `<orange>` que también tienen la clase "small". Combina un selector de tipo (elemento) con un selector de clase.

## Selectores de Descendientes
- **`bento orange.small`**: Selecciona todos los elementos `<orange>` con la clase "small" que están dentro de un elemento `<bento>`. Este selector busca elementos `<orange>` que son descendientes de `<bento>`, no necesariamente hijos directos.

## Selectores de Grupo
- **`bento, plate`**: Selecciona todos los elementos `<bento>` y todos los elementos `<plate>`. Este selector de grupo aplica los mismos estilos a múltiples tipos de elementos.

## Selector Universal
- **`*`**: Selecciona todos los elementos de la página. Este selector es muy potente y debe usarse con cuidado para no afectar a todos los elementos de manera no intencionada.

## Selectores de Hijos
- **`plate *`**: Selecciona todos los elementos que son descendientes (hijos, nietos, etc.) de un elemento `<plate>`. Es similar al selector universal pero limitado a los descendientes de `<plate>`.
- **`plate > apple`**: Selecciona todos los elementos `<apple>` que son hijos directos de un elemento `<plate>`. No selecciona nietos u otros descendientes.

## Selector de Hermano Adyacente
- **`plate + apple`**: Selecciona el primer elemento `<apple>` que es inmediatamente siguiente (hermano adyacente) a un elemento `<plate>`. Ambos elementos deben ser hijos del mismo elemento padre.

## Selector de Hermanos Generales
- **`bento ~ pickle`**: Selecciona todos los elementos `<pickle>` que son hermanos (no necesariamente adyacentes) de un elemento `<bento>`. Todos deben compartir el mismo elemento padre.

## Pseudo-clases
- **`orange:first-child`**: Selecciona el primer hijo `<orange>` de su elemento padre. Útil para aplicar estilos especiales al primer elemento de un grupo.
- **`plate > :only-child`**: Selecciona el único hijo de un elemento `<plate>`. Aplica estilos cuando un `<plate>` tiene un solo hijo.
- **`.small:last-child`**: Selecciona el último hijo de un elemento padre, pero solo si este hijo tiene la clase "small".
- **`:nth-child(3)`**: Selecciona el tercer hijo de su elemento padre, sin importar el tipo de elemento.
- **`bento:nth-last-child(3)`**: Selecciona el tercer hijo desde el final dentro de un elemento `<bento>`. Cuenta los hijos desde el último hasta el primero.
- **`apple:first-of-type`**: Selecciona el primer elemento `<apple>` de su tipo dentro de su elemento padre.
- **`:nth-of-type(even)`**: Selecciona todos los elementos de un tipo específico que están en posiciones pares dentro de su elemento padre.
- **`:nth-of-type(2n+3)`**: Selecciona todos los elementos de un tipo específico que están en posiciones que cumplen con la fórmula 2n+3 (por ejemplo, 3, 5, 7, etc.).
- **`apple:only-of-type`**: Selecciona el único elemento `<apple>` de su tipo dentro de su elemento padre.
- **`.small:last-of-type`**: Selecciona el último elemento de su tipo que también tiene la clase "small" dentro de su elemento padre.
- **`bento:empty`**: Selecciona todos los elementos `<bento>` que no tienen hijos ni contenido alguno.
- **`apple:not(.small)`**: Selecciona todos los elementos `<apple>` que no tienen la clase "small". Útil para aplicar estilos a todos los `<apple>` excepto a los que tienen una clase específica.

## Selectores de Atributo
- **`[for]`**: Selecciona todos los elementos que tienen el atributo `for`, sin importar su valor. Comúnmente usado en etiquetas `<label>`.
- **`plate[for]`**: Selecciona todos los elementos `<plate>` que tienen el atributo `for`. Combina el selector de tipo y el de atributo.
- **`[for="Vitaly"]`**: Selecciona todos los elementos que tienen el atributo `for` con el valor exacto "Vitaly".
- **`[for^="Sa"]`**: Selecciona todos los elementos que tienen el atributo `for` cuyo valor comienza con "Sa".
- **`[for$="ato"]`**: Selecciona todos los elementos que tienen el atributo `for` cuyo valor termina en "ato".
- **`[for*="obb"]`**: Selecciona todos los elementos que tienen el atributo `for` cuyo valor contiene la cadena "obb".
