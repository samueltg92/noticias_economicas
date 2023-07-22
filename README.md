# Noticias Económicas

Este script de Python utiliza la biblioteca "requests" para hacer llamadas a la API de Alpha Vantage y obtener noticias sobre diversos temas relacionados con blockchain, mercados financieros, economía macro, finanzas y tecnología. Luego, utiliza la biblioteca "pandas" para manipular los datos y mostrarlos en un DataFrame. El objetivo es mostrar las noticias más recientes en esos temas durante la última hora.

Aquí está una descripción paso a paso del script:

Importar las bibliotecas necesarias:

requests: para realizar solicitudes HTTP a la API de Alpha Vantage y obtener los datos de las noticias.
pandas: para manipular los datos en forma de DataFrame, lo que facilita su análisis y presentación.
datetime y timedelta de datetime: para trabajar con fechas y calcular el intervalo de tiempo de una hora.
pytz: para manejar zonas horarias.
os y load_dotenv de dotenv: para cargar la clave de API desde un archivo .env.
Cargar la clave de API desde un archivo .env utilizando load_dotenv().

Definir el tema de interés en una lista llamada topics. El script busca noticias sobre cada tema en esta lista.

Crear una lista vacía llamada news_data para almacenar la información de las noticias.

Definir una función convert_datetime(x) que convierte una cadena de fecha y hora en un objeto de fecha y hora de Python utilizando el formato especificado.

Recorrer la lista de temas (topics) y para cada tema:
a. Construir la URL de la API de Alpha Vantage con el tema, la hora actual y la hora hace una hora.
b. Realizar una solicitud HTTP GET a la URL utilizando la biblioteca requests.
c. Analizar la respuesta JSON para obtener los datos de las noticias.
d. Para cada noticia en la respuesta, extraer la información relevante (título, hora de publicación, fuente y resumen) y agregarla a la lista news_data.

Después de recopilar todas las noticias para todos los temas, convertir la lista news_data en un DataFrame de pandas llamado df.

Finalmente, mostrar el DataFrame df con las noticias recopiladas utilizando print(df).
