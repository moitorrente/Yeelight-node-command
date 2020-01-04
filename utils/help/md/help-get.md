### NOMBRE
    get


### SINTAXIS
```shell
npm run yeelight get [propiedad]
```


### DESCRIPCION
Solicita las propiedades a la bombilla. 

Se puede solicitar propiedades concretas, en caso de que no se escriba ninguna propiedad se solcitarán todas.


###  PARAMETROS
1. **Propiedad**:
    - `power`: Estado de la bombilla. 
        - `on`: encendida 
        - `off`: apagada
    - `bright`: Porcentaje de brillo. Rango `[1 - 100]`
    - `ct`: Temperatura de color. Rango `[1700 - 6500]` (k)
    - `rgb`: Color. Rango `[1 - 16777215]`
    - `hue`: Hue. Rango `[0 - 359]`
    - `sat`: Saturación. Rango `[0 - 100]`
    - `color_mode`: 
        - `1`: modo rgb 
        - `2`: modo temperatura 
        - `3`: modo hsv
    - `flowing`: 
        - `0`: flow no está ejecutándose 
        - `1`: flow ejecutándose
    - `delayoff`: Tiempo restante del timer. Rangp `[1 - 60]` (minutos)
    - `flow_params`: Parámetros de flujo actuales (solo con datos cuando 'flowing' es 1)
    - `music_on`: 
        - `0`: Modo música está desactivado 
        - `1`: Modo música está activado
    - `name`: Nombre de la bombilla. Se puede asignar con el comando "name"


### EJEMPLO
Solicitud de todos los parametros:
```shell
npm run yeelight get
```


Solicitud de nombre y estado de la bombilla:
```shell
npm run yeelight get name power
```


### EJEMPLO PETICION ENVIADA
```javascript
{ 
    id: 0, 
    method: 'get_prop', 
    params: [ 'name' ] 
}
```


### EJEMPLO RESPUESTA
```javascript
{
    id: 0, 
    result: [ 'bombilla-escritorio' ] 
}
```