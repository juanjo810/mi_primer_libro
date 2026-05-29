# Sesion 2. Operaciones con bits

Esta sesion se centra en el manejo de bits mediante mascaras. La idea central es cambiar solo algunas posiciones de un registro mientras el resto permanece igual.

```{admonition} Objetivos de aprendizaje
:class: tip

- El complemento a uno se obtiene con `~` y cambia cada 0 por 1 y cada 1 por 0.
- Para activar bits se usa una mascara con unos en las posiciones objetivo y una operacion OR bit a bit.
- Para desactivar bits se combina una mascara inversa con una operacion AND bit a bit.
```

## Conceptos clave

- El complemento a uno se obtiene con `~` y cambia cada 0 por 1 y cada 1 por 0.
- Para activar bits se usa una mascara con unos en las posiciones objetivo y una operacion OR bit a bit.
- Para desactivar bits se combina una mascara inversa con una operacion AND bit a bit.
- Para voltear bits se usa XOR bit a bit con una mascara que marca las posiciones que cambian.
- Las reducciones permiten condensar muchos bits en un unico resultado, por ejemplo para paridad.

## Practica guiada

1. Declara un registro de 16 bits y asignale un valor inicial facil de reconocer en binario.
2. Activa un bit, desactiva tres bits y voltea otro bit usando mascaras.
3. Calcula el bit de paridad par de un registro de 8 bits.
4. Resuelve primero a mano y despues compara con la simulacion; en esta sesion la referencia principal es la tabla de bits que construyas durante el calculo.

## Indice teoria-practica-figuras

Usa esta tabla como mapa rapido: cuando un ejercicio mencione una figura, esa figura forma parte del enunciado y debe consultarse antes de escribir el codigo.

| Bloque de teoria | Ejercicios relacionados | Figuras que se deben consultar |
|---|---|---|
| Mascaras, paridad y reduccion de bits | Ejercicios 1 a 4 | Tabla manual de bits del enunciado; no hay figura externa asociada |

## Trabajo sin figura asociada
Esta sesion se apoya sobre todo en operaciones sobre registros y mascaras. Usa una tabla escrita a mano para seguir cada bit antes de ejecutar el codigo.

## Cierre

Antes de pasar a la sesion siguiente, guarda el fichero Verilog de cada ejercicio y anota dos cosas: que esperabas obtener y que imprimio realmente la simulacion. Esa comparacion es la forma mas rapida de localizar errores.

## Fuente original

Contenido redactado y ampliado a partir de la presentacion de clase y de la pagina de referencia: <http://avellano.fis.usal.es/~compi/sesion2.htm>.
