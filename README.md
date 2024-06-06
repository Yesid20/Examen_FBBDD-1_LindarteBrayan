
# Filtro introducción a las bases de datos


# Examen_FBBDD-1_LindarteBrayan

		
Filtro introducción bases de datos












Brayan Yesid Lindarte Anaya 









Pedro felipe gomez bonilla

Campuslands – floridablanca, santander 
P1 




Caso estudio – modelo conceptual

* Complejo deportivo =*deporte.
			   *localización específica.
			   * jefe de organización.
			   * número de complejos.	
			   * área total ocupada.
			   * presupuesto aproximado.
	
* Complejo polideportivos= * deportes. 
			   *localización específica.
			   * jefe de organización.
                                      * área total ocupada.
* Eventos = *tipo_scenari.
	        *fecha.
	        *duración.
	        *número de participantes.
	        *número de comisarios.
* Comisarios = * nombre del comisario.
		  * tipo_of_rol.
		  * número de identificación.
* Equipamiento necesario = *número_arcos.
			           *número_pértigas.
				*barras_paralelas.
* Inventary = *tipo_of_escenario
	           *fecha_ultimo_mantenimiento.
		*available_arcos.
		*available_pértigas.
		*available_paralelas.


![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/36188386-19f3-4127-80bd-c141436a7e30)


Conversión conceptual – modelo lógico.

1). Entidades con sus atributos =

 Complejo deportivo =
			  *Identificador_complejo_deportivo = int (10)pk, serial del complejo.
			  *nombre = varchar(30), nombre alusivo a figura representativa. 
			   *deporte = varchar (30), que deporte se maneja en el complejo.
			   *localización específica = varchar (50), ubicación con valores latitudinales.
			   * jefe de organización = varchar (30), nombre del organizador. 
			   * número de complejos = int (99), cuantos complejos en ese deporte estan en existencia.
			   * área total ocupada = int (9999), capacidad de aforo en el complejo.
* presupuesto aproximado. Int(9999), valores logisticos para la realización del evento.

Complejo polideportivos=
			  *identificador_complejo_polideportivo = int(10)pk, serial del polideportivo.
			  *nombre = varchar (30), nombre del polideportivo.
		              *deporte = varchar (30), deportes que se manejaran en el polideportivo.
			   *localización específica = varchar (50), ubicación con valores latitudinales.
			   * jefe de organización = varchar (50), nombre del organizador.
* área total ocupada = int (9999), aforo para evaluar si sobrepasa el limite.



* Eventos =
	       *identificador_evento = int(100)pk, identificador del evento.
	        *tipo_escenario = varchar (30), si es deportivo o polideportivo.
	        *fecha = date (dd-mm-yy), horario establecido para la realización y finalización del evento
	        *duración = time (hh:mm), ocupación del complejo.
	        *número de participantes = int (99999), aforo que asistira.
	        *número de comisarios = int(99), personas responsables de logistica.


* Comisarios =
		*identificador_comisario = int(999)pk, identificador del comisario;
	  	*nombre del comisario = varchar (50). nombre del comisario;
		  * tipo_of_rol = varchar (30), cargo dentro de la organización.
* número de identificación = int (999999), UID nacional.



* Equipamiento necesario =
				*identificador_articulos = int (999)pk, identificador de articulo
				*numero_arcos= int (999), cantidad de accesorios solicitados.
			           *número_pértiga = int (999), cantidad de accesorios solicitados.
				*barras_paralelas = int (999), cantidad de barras paralelas solicitadas.

* Inventary =
		*identificador_inventary = int(999), identificación de inventario, pk.
		*tipo_of_escenario = varchar (99), que complejo se utilizara.
	           *fecha_ultimo_mantenimiento = date(dd-mm-yy), ultimo mantenimiento realizado.
		*available_arcos = int(99), disponibilidad de articulo.
		*available_pértigas = int (99), disponibilidad de pértigas.
		*available_paralela = int (99), disponibilidad de paralela.

  ![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/50233ddc-0aaf-48bb-ad96-6de4e4e97ccd)


Normalización de modelo lógico

1) Elimina redundancias referente a los atributos

La tabla que se unifico para no repetir datos fue complejos deportivos y complejos polideportivos y nace la tabla COMPLEJOS con el fin de no repetir datos.

![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/1c7eacd4-eacf-45ec-a791-fddece793851)


Tambien se unifico inventario y equipamiento 
![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/c123cdbb-d385-446f-b227-0cc8c1715034)


2) Atributos atómicos
Para realizar el siguiente paso debemos ya tener las tablas con el 1FN check. 

![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/314d0b49-0e5f-487f-9815-7a99aa80af14)

![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/c05eac7b-c348-42ee-b997-e10be765513c)

![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/f7dabea5-bd32-4c8f-bb16-585265d2621d)

3)Eliminación de dependencias transitivas
![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/bc6dcab3-32f0-4be4-8c04-fb25d17bca4c)
![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/da36282a-2e26-421d-a998-a361d57d4e08)
![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/d2a9023e-8f73-4b1f-a1ce-de2c1a3578cc)

Construcción formal modelo físico 


* 3 consultas solicitadas:


![image](https://github.com/Yesid20/Examen_FBBDD-1_LindarteBrayan/assets/129091134/aa6cbe3a-e364-4705-9469-dde780bafff1)


Consulta de Todos los Eventos en un Complejo Deportivo Específico.
Consulta de Eventos Celebrados en Complejos Deportivos con Jefe de Organización Específico.
Consulta de Eventos con Número de Participantes Mayor que la Media.
