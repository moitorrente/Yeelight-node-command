### NOMBRE
    consoling 

### SINTAXIS
```shell
Yeelight>consoling [{on | off}]
```

### DESCRIPCION
Alterna entre mostrar o no la información enviada y recibida a la bombilla.
Por defecto desactivado.

### PARAMETROS
1. `on`: activar consoling
2. `off`: desactivar consoling

En caso de que no se especifique el parámetro, se alternará entre activado/desactivado.

### EJEMPLO
Cambio de color con `consoling` desactivado:
```shell
Yeelight>blue
Yeelight>Bombilla => ok
```

Cambio de color con `consoling` activado:
```shell
Yeelight>blue
Yeelight>Cliente  => {"id":0,"method":"set_rgb","params":[255]}
Yeelight>Bombilla => {"id":0,"result":["ok"]}
```