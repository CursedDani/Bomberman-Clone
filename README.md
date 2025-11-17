# Bomberman Clone - Implementación en Jack

![Bomberman](https://img.shields.io/badge/Language-Jack-blue)
![Platform](https://img.shields.io/badge/Platform-Nand2Tetris-green)
![Status](https://img.shields.io/badge/Status-Complete-success)

## Sustentación
https://youtu.be/kWT2HjggeUc

## Descripción

Implementación del clásico juego Bomberman en lenguaje Jack para la plataforma Nand2Tetris. El jugador controla un personaje que debe destruir todas las rocas del mapa usando bombas, mientras evita ser atrapado por enemigos en movimiento o por las explosiones de sus propias bombas.

## Integrantes del Grupo

- **Daniel Arango** - [@CursedDani](https://github.com/CursedDani)
- **Daniel Correa** - [@Danielc19](https://github.com/Danielc19)

## Características del Juego

### Mecánicas Principales
- **Personaje jugable**: Controlado con las flechas del teclado
- **Bombas**: Se colocan con la barra espaciadora y explotan después de 1 segundo
- **Explosión 3×3**: Las bombas explotan en un área de 3×3 casillas
- **Rocas destructibles**: 15 rocas distribuidas estratégicamente en el mapa
- **Enemigos móviles**: 4 enemigos con patrones de movimiento predefinidos
- **Sprite dinámico**: El personaje levanta los brazos cuando está sobre una bomba
- **Colisiones**: El personaje no puede atravesar rocas y muere al tocar enemigos

### Controles
- **Flechas (↑ ↓ ← →)**: Mover al personaje
- **Barra Espaciadora**: Colocar bomba
- **Q**: Salir del juego

### Condiciones de Victoria/Derrota
- **Victoria**: Destruir todas las 15 rocas del mapa
- **Derrota**: Ser alcanzado por una explosión o tocar un enemigo

### Enemigos
El juego incluye 4 enemigos con diferentes patrones de movimiento:
1. **Enemigo horizontal**: Patrulla de izquierda a derecha
2. **Enemigo vertical (izquierda)**: Patrulla de arriba a abajo en el lado izquierdo
3. **Enemigo vertical (derecha)**: Patrulla de arriba a abajo en el lado derecho
4. **Enemigo cuadrado**: Se mueve en un patrón cuadrado (derecha → abajo → izquierda → arriba)

Los enemigos cambian de dirección al chocar con paredes o rocas. Pueden ser destruidos por explosiones de bombas, pero esto no es necesario para ganar.

## Estructura del Proyecto

```
Bomberman/
│
├── Main.jack            # Punto de entrada del programa
├── Game.jack            # Lógica principal del juego y loop de ejecución
├── Player.jack          # Clase del personaje jugador
├── Bomb.jack            # Clase de bombas individuales
├── BombManager.jack     # Gestor de múltiples bombas (hasta 5 simultáneas)
├── Rock.jack            # Clase de rocas destructibles
├── RockManager.jack     # Gestor de las 15 rocas del mapa
├── Enemy.jack           # Clase de enemigos individuales
├── EnemyManager.jack    # Gestor de los 4 enemigos
└── README.md            # Este archivo
```

## Cómo Compilar y Ejecutar

### Usando la Interfaz Gráfica de Nand2Tetris (Online IDE)

1. **Abre el Jack Compiler:**
   - Desde el IDE de nand2tetris ir a la sección de [Jack compiler](https://nand2tetris.github.io/web-ide/compiler).

2. **Compila el proyecto:**
   - Haz clic en la carpeta que aparece al lado de **"Source"**
   - Busca entre tu directorio la carpeta `Bomberman` y selecciónala.
   - Da click en `Compile`, el compilador generará automáticamente los archivos `.vm`.

3. **Ejecuta el VMEmulator:**
   - Luego de compilar, dar click en el botón de al lado que dice `Run`, esto abrirá la interfaz del VMEmulator.
   - Configura la velocidad de ejecución a "Fast" para mejor experiencia.
   - Haz clic en **Run**.

## Estrategias de Juego

- Coloca bombas estratégicamente para destruir múltiples rocas a la vez
- Evita quedar atrapado entre enemigos y bombas
- Los enemigos tienen patrones predecibles, úsalo a tu favor
- Puedes destruir enemigos con bombas para facilitar el movimiento
- El sprite cambiado (brazos arriba) te avisa cuando estás en peligro sobre una bomba


---

**Desarrollado con 💣 para el curso de Organización de Computadores - EAFIT 2025**
