# Juego de piedra, papel o tijera

```python
import numpy as np
import time

#Def funciona para almacenar todo lo programado y llamarlo después
def piedra_tijera_papel():


    # las opciones asignadas a lo que vencen
    # Diccionario es con {} y puede relacionarse un término y llamar otro

    # Opciones de qué le gana a qué
    opciones = {'piedra':'tijera',
                'tijera' : 'papel',
                'papel' : 'piedra'}
    
    # Entrada del jugador
    # input significa permitir incluir valores al usuario por consola
    # Ejecuta 
    jugador = input("Elige entre piedra, papel o tijera: ")

    #Bucle While ejecuta la lógica mientras que se cumpla una condición
    #For ejecuta una lógica una cantidad n de veces 
    while jugador not in {'piedra','tijera','papel'}:
        print("Cometiste un error...")
        jugador = input("Elige entre piedra, papel o tijera: ")
        
        
    # Selección aleatoria para el computador
    computadora = np.random.choice(['piedra','tijera','papel'])
    
    # Mostrar selecciones en la pantalla
    time.sleep(.5)

#\n genera una nueva linea
    print("\nHas seleccionado:", jugador)
    print("La computadora ha seleccionado:", computadora, '\n')
    time.sleep(2)
    
    # Determinar el ganador
    if opciones[jugador] == computadora: 
        print("Has ganado!")
    elif opciones[computadora] == jugador:
        print("Has perdido!")
    else: 
        print("Empate!")

#############################

def cuadrado(num):
    print(num*num)


