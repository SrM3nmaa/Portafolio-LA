# Programa creado por Leyva Gonzalez Irving Antonio
# Programa de un conjunto de saludos

import random
# Conjunto de Saludos
print("") 
nombre = "Menma"
saludos = [
    " Bienvenido " + nombre + " , Un Cordial Saludo ",
    " Hola " + nombre + " , ¿ En Que Te Podemos Servir ?",
    " Es Un Placer Tenerte Nuevamete " + nombre,
    " Hola " + nombre + " , ¿ Cómo Estás ?",
    " Hola " + nombre + " , ¿Cómo Te Va ? "
]

# Impresion de Saludos de forma aleatoria
indice=random.randint(0,len(saludos)-1)
print(saludos[indice])