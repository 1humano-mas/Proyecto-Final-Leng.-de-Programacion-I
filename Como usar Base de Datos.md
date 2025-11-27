# Recuerden que el formato SIEMPRE será:
Fecha: "2023-12-31" (Año-Mes-Día) -> Importante para ordenar correctamente.
Hora: "14:30" (Hora:Minutos, formato 24h).

## Para obtener datos (Select)
from database.db_manager import DBManager
db = DBManager()  
##### Ejemplo: Traer todos los doctores
lista_doctores = db.obtener_datos("SELECT * FROM doctores")
##### Devuelve: [{'id': 1, 'nombre': 'Juan', ...}, {'id': 2, ...}]

## Para guardar datos (Insert/Update/Delete)
from database.db_manager import DBManager

db = DBManager()
##### Ejemplo: Guardar un paciente
sql = "INSERT INTO pacientes (nombre, apellido, dni) VALUES (?, ?, ?)"
parametros = ("Ana", "Gomez", "12345678")
db.ejecutar_consulta(sql, parametros)
