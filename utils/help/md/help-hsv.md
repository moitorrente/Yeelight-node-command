### NOMBRE
    hsv

### SINTAXIS
```shell
Yeelight>hsv [hue] [saturacion] <{sudden | smooth}> <duración>
```

### DESCRIPCION
Cambia el color de la luz en función del valor de hue y saturación introducidos.


### PARAMETROS
1. **HUE**: rango de valores permitidos `[0 - 359]`

2. **Saturación**: rango de valores permitidos `[0 - 100]`
    
3. **Efecto**: Tipo de cambio de brillo.
    - `sudden`: Cambia el color de la luz de inmediato
    - `smooth`: Cambia el color de la luz con un intervalo definido con el parametro de duración

4. **Duración**: El parámetro de duración solo se tendrá en cuenta con el efecto `smooth` y el valor introducido estará en segundos.


### EJEMPLO
Cambio inmediato de color a azul:
```shell
Yeelight>hsv 250 100
Yeelight>hsv 250 100 sudden
```

Cambio de color a azul con un intervalo de 3 segundos:
```shell
Yeelight>hsv 250 100 smooth 3
```


### EJEMPLO PETICION ENVIADA
```javascript
{ 
    id: 0, 
    method: 'set_hsv', 
    params: [ 250, 100 ] }
```


### EJEMPLO RESPUESTA
```javascript    
{ 
    id: 0, 
    result: [ 'ok' ] 
}
```
