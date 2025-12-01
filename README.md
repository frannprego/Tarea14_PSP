# Tarea14_PSP

## Apartado 1: En el primer apartodo nos manda crear las tablas correspondientes a la empresa. Para ellos las crearemos de la siguiente forma: 

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


## Apartado 2: Inserta 5 registros inventados en la tabla a través de una sentencia SQL.

```bash
INSERT INTO public."EmpresasFCT" (nombre, quiereAlumnos, numAlumnos, fechaContacto)
VALUES
('PANADERIA PACO', FALSE, 100, '2025-04-15'),
('PANADERIA RUBEN', FALSE, 170, '2025-03-03'),
('PANADERIA DIEGO', FALSE, 150, '2025-12-10'),
('PANADERIA MANUEL', TRUE, 100, '2025-01-01'),
('PANADERIA DAMIAN', TRUE, 150, '2025-04-03');
```

<img width="629" height="821" alt="3" src="https://github.com/user-attachments/assets/d3d6998f-df09-401c-8b39-c3360cc9066a" />


## Apartado 3: Realiza una consulta donde se muestren todos los datos de la tabla EmpresasFCT ordenados por fechaContacto, de modo que en la primera fila salga el que tenga la fecha más reciente.

<img width="629" height="821" alt="4" src="https://github.com/user-attachments/assets/87f1b601-72f4-42a4-af80-db7b25446e63" />

## Apartado 4: Realiza una consulta que permita obtener un listado de todos los contactos de Odoo (no empresas) con la siguiente información: - Nombre - Cuya ciudad NO sea Tracy - Nombre comercial de la empresa ordenados alfabéticamente por el nombre comercial de la empresa

```bash
SELECT rp.name AS "Nombre", rp.city AS "Ciudad", rpe.name AS "Nombre Comercial de la Empresa" 
FROM res_partner rp LEFT JOIN res_partner rpe ON rp.parent_id = rpe.id WHERE rp.parent_id 
IS NOT NULL AND rp.city <> 'Tracy' ORDER BY rpe.name ASC;
```
<img width="855" height="795" alt="5" src="https://github.com/user-attachments/assets/bdfefd21-53be-43c9-bcf6-285b00ba1569" />



