
Semana #6 (Capa de datos)

## Laboratorio 3.02: SQL (202302)

LABORATORIO

* Obligatorio
  

Envió este laboratorio el 1 de mayo de 2024 .

**Normalización y script DDL para la base de datos del blog.**

Excelente trabajo en la normalización y creación de los scripts DDL para la base de datos del blog. Has entendido correctamente la estructura necesaria para las tablas y sus relaciones. Tu código SQL para crear las tablas `Authors`y `Posts`es correcto y refleja adecuadamente la normalización de los datos proporcionados en el enunciado. También ha insertado los datos con éxito en las tablas. Buen uso de la clave primaria y la clave foránea para vincular las tablas. ¡Sigue así!

¿Fue útil esta retroalimentación?

**Normalización y script DDL para la base de datos de aerolíneas**

Ha realizado un buen trabajo normalizando la base de datos de aerolíneas y creando los scripts DDL. Tu solución muestra una clara comprensión de la creación de las tablas `Customers`, `Aircrafts`y `Flights`, siguiendo una buena normalización. Los datos se han insertado correctamente y ha establecido las claves primarias y foráneas donde era necesario. Sin embargo, asegúrese de revisar los nombres de las columnas y las claves extranjeras para que reflejen con precisión los datos relacionados. El nombre de la columna `CustomerMilleage`en la tabla `Customers`parece contener un error tipográfico y podría ajustarse a `CustomerMileage`. Además, cuando revise las claves foráneas, verifique que las referencias sean consistentes y correctas en términos de las relaciones entre las tablas. Estos pequeños detalles son importantes para mantener la integridad de la base de datos.

¿Fue útil esta retroalimentación?

**Script SQL para el número total de vuelos**

Perfecto, tu consulta SQL para obtener el número total de vuelos es correcto. `SELECT COUNT(*) as Total_Vuelos FROM Flights;`devuelve la cantidad exacta de registros de vuelo en la tabla `Flights`, lo cual cumple con lo requerido en las instrucciones. Continúa trabajando con esta precisión y atención al detalle.

¿Fue útil esta retroalimentación?

**Script SQL para la distancia promedio de vuelo**

Muy bien, tu consulta SQL calcula con éxito la distancia promedio de vuelo utilizando la función `AVG`. Tu sintaxis tiene buen formato y facilita la lectura del código: `SELECT ROUND(AVG(Flights.FlightMilleage), 2) AS Distancia_Media_De_Vuelo FROM Flights;`. Es un excelente uso de las funciones de agregación y redondeo para proporcionar un resultado claro y comprensible.

¿Fue útil esta retroalimentación?

**Script SQL para el número promedio de asientos por vuelo**

Tu script SQL para calcular el número promedio de asientos por vuelo está ejecutado correctamente. La consulta `SELECT ROUND(AVG(AirCrafts.AircraftSeats), 2) AS Media_Asientos_Vuelo FROM Aircrafts INNER JOIN Flights ON Aircrafts.AircraftId = Flights.AircraftId;`utiliza correctamente la unión `INNER JOIN`para combinar las tablas y la función `AVG`para calcular el promedio. Buen trabajo.

¿Fue útil esta retroalimentación?

**Script SQL para el promedio de millas voladas por los clientes agrupados por estatus**

Excelente uso del `INNER JOIN`y `GROUP BY`en tu consulta para calcular el promedio de millas voladas por los clientes, agrupadas por estatus de cliente con la consulta `SELECT Status, ROUND(AVG(CustomerMilleage), 2) AS Promedio_Millas_Por_Cliente FROM Customers INNER JOIN Flights ON Customers.CustomerId = Flights.CustomerId GROUP BY Status;`. Ha aplicado correctamente las funciones de agregación para proporcionar una visión clara de los datos aglomerados por una categoría común. Sigue así.

¿Fue útil esta retroalimentación?

**Script SQL para el número máximo de millas voladas por los clientes agrupados por estatus**

Tu consulta para obtener el número máximo de millas voladas por los clientes agrupados por estatus es exactamente lo que se requería: `SELECT Status, MAX(CustomerMilleage) AS Maximo_Millas_Por_Cliente FROM Customers INNER JOIN Flights ON Customers.CustomerId = Flights.CustomerId GROUP BY Status;`has utilizado de forma correcta la función `MAX`junto con `GROUP BY`. Gran manejo de consultas SQL.

¿Fue útil esta retroalimentación?

**Script SQL para el número total de aeronaves con nombre que contiene Boeing**

Ha demostrado una sólida comprensión del operador `LIKE`en SQL. Tu consulta `SELECT COUNT(*) AS Numero_Aeronaves_Boeing FROM Aircrafts WHERE AircraftName LIKE 'Boeing%';`filtra efectivamente y cuenta todas las aeronaves que contienen la palabra 'Boeing' en su nombre. Esta es una habilidad útil para la manipulación y consulta de cadenas de texto.

¿Fue útil esta retroalimentación?

**Script SQL para encontrar vuelos con distancia entre 300 y 2000 millas**

Tu consulta SQL para encontrar vuelos dentro de un rango específico de millas está bien formulada: `SELECT Customers.Name, FlightNumber AS Numero_Vuelo, FlightMilleage as Millas_Vuelo FROM Flights inner join Customers on Flights.CustomerId = Customers.CustomerId WHERE FlightMilleage BETWEEN 200 AND 2000;`. Asegúrese de que el rango de millas coincida exactamente con las instrucciones del laboratorio, en este caso, entre 300 y 2000 millas. Aun así, esta consulta captura la idea principal y utiliza correctamente la cláusula `BETWEEN`.

¿Fue útil esta retroalimentación?

**Script SQL para la distancia promedio de vuelo reservada agrupada por estatus de cliente**

No completado.

**Script SQL para averiguar la aeronave más reservada por los miembros de estatus de oro**

No completado.

