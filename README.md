# Tarea14_PSP

## Apartado 1

En el primer apartodo nos manda crear las tablas correspondientes a la empresa. Para ellos las crearemos de la siguiente forma: 
```bash
CREATE TABLE public. "EmpresasFCT" (
	idEmpresa SERIAL PRIMARY KEY,
	nombre VARCHAR(40),
	quiereAlumnos BOOLEAN,
	numAlumnos INTEGER,
	fechaContacto DATE
);
```

<img width="771" height="611" alt="1" src="https://github.com/user-attachments/assets/1245114a-7d69-4c33-b488-c46b7eb27d24" />
<img width="285" height="261" alt="2" src="https://github.com/user-attachments/assets/672e0574-ed09-4052-8a55-3ab7f52fb126" />


## Apartado 2
Ahora tenemos que inserta 5 registros inventados en la tabla a través de una sentencia SQ. o haremos de la siguiente forma:

```bash
select * from public."EmpresasFCT"
```

<img width="629" height="821" alt="3" src="https://github.com/user-attachments/assets/d3d6998f-df09-401c-8b39-c3360cc9066a" />
