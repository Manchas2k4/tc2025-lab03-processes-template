# Actividad colaborativa - Manejo de procesos
Escribe un programa llamado descending que recibe de línea de comando un número entero positivo.

```
$ .\descending number
```

El programa generará el siguiente árbol de procesos: el proceso inicial creará un hijo de **NIVEL_1**, el proceso de **NIVEL_1** creará dos procesos de **NIVEL_2**, cada proceso de **NIVEL_2** creará tres procesos de nivel **NIVEL_3**; y así sucesivamente **NIVEL_N-1** creará **N** procesos de **NIV EL_N**. Cada proceso deberá desplegar información sobre el id de su padre y su propio id. Los procesos de nivel **N** dormirán 1 segundo antes de terminar. Cada proceso deberá esperar hasta que todos sus hijos hayan terminado.

Ejemplos de uso:
```
$ .\descending
usage: descending number
--------------------------------------------------------------------------
$ .\descending texto
descending: the parameter must be a positive integer number
--------------------------------------------------------------------------
$ .\descending texto
descending: the parameter must be a positive integer number
--------------------------------------------------------------------------
$ .\descending 12.14
descending: the parameter must be a positive integer number
--------------------------------------------------------------------------
$ .\descending -10
descending: the parameter must be a positive integer number
--------------------------------------------------------------------------
$ .\descending -10
descending: the parameter must be a positive integer number
--------------------------------------------------------------------------
$ .\descending 0
descending: the parameter must be a positive integer number
--------------------------------------------------------------------------
$ .\descending 3
PPID = 1234 PID = 1235 NIVEL = 0
	PPID = 1235 PID = 1236 NIVEL = 1
		PPID = 1236 PID = 1237 NIVEL = 2
			PPID = 1237 PID = 1238 NIVEL = 3
			PPID = 1237 PID = 1239 NIVEL = 3
			PPID = 1237 PID = 1240 NIVEL = 3
		PPID = 1236 PID = 1241 NIVEL = 2
			PPID = 1241 PID = 1242 NIVEL = 3
			PPID = 1241 PID = 1243 NIVEL = 3
			PPID = 1241 PID = 1244 NIVEL = 3
```

|     | Ponderación                                                                                                                                                                                                |
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +10 | Verifica que el programa reciba la cantidad correcta de<br>parámetros. En caso de que no sea así, el programa<br>despliega un mensaje adecuado y termina, regresando<br>-2 como resultado de su ejecución. |
| +10 | Verifica que number sea un número entero válido (mayor<br>a cero). En caso de que no sea así, el programa<br>despliega un mensaje adecuado y termina, regresando<br>-3 como resultado de su ejecución.     |
| +70 | El programa implementa una solución correcta. Regresa<br>0 como resultado de su ejecución.                                                                                                                 |