# Juego de piedra, papel o tijera

```python
import numpy as np
import time

def piedra_tijera_papel():
    
    # las opciones asignadas a lo que vencen
    opciones = {'piedra':'tijera', 'tijera' : 'papel', 'papel' : 'piedra'}
    
    # Entrada del jugador
    jugador = input("Elige entre piedra, papel o tijera: ")
    while jugador not in {'piedra','tijera','papel'}:
        print("Cometiste un error...")
        jugador = input("Elige entre piedra, papel o tijera: ")
        
        
    # Selección aleatoria para el computador
    computadora = np.random.choice(['piedra','tijera','papel'])
    
    # Mostrar selecciones en la pantalla
    time.sleep(.5)
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


