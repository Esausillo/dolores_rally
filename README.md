# Rally de la Independencia AR

Juego de realidad aumentada para recorrer Dolores Hidalgo, desarrollado con **Flutter** siguiendo **TDD** (Test-Driven Development).

- **Materia:** Desarrollo Móvil Integral · UTNG
- **Profesor:** Anastacio Rodríguez García
- **Alumno(s):** Esaú Rafael Guzmán Almaguer

## ¿De qué trata?

El jugador camina por el Jardín Principal buscando 6 personajes de la Independencia escondidos al azar. Un radar y un indicador de "frío o caliente" lo guían. Al estar a 15 m o menos, toca al personaje y responde una pregunta de historia para atraparlo y guardarlo en su álbum.

| Regla | Valor |
|---|---|
| Personajes | 6 |
| Distancia de aparición | 60 a 500 m del Jardín Principal |
| Radio de captura | 15 m |
| Intentos | 2 (con 2 fallos el personaje huye y reaparece en otro lugar) |
| Puntos | 100 al primer intento, 50 al segundo |

## Estructura del proyecto

```
lib/
  dominio/        reglas del juego (Dart puro)
  datos/          GPS, brújula, simuladores y almacenamiento
  presentacion/   ViewModel y pantallas
  main.dart
test/             6 archivos de prueba, 43 pruebas
capturas/         evidencias del README
```

## Cómo ejecutarlo

```bash
flutter pub get
flutter test      # corre las 43 pruebas
flutter run       # modo demo disponible sin salir del salón
```

---

## Evidencias del ciclo TDD (🔴 rojo → 🟢 verde)

En cada ronda se quitó temporalmente el código para ver la prueba **fallar** (rojo) y se restauró para verla **pasar** (verde).

### Ronda 2 · Geometría (`geo_test.dart`, 7 pruebas)

| 🔴 Rojo | 🟢 Verde |
|---|---|
| ![Ronda 2 rojo](capturas/ronda1r.png) | ![Ronda 2 verde](capturas/ronda1v.png) |

### Ronda 4 · Azar con semilla (`aparicion_test.dart`, 5 pruebas)

| 🔴 Rojo | 🟢 Verde |
|---|---|
| ![Ronda 4 rojo](capturas/ronda4r.png) | ![Ronda 4 verde](capturas/ronda4v.png) |

### Ronda 5 · Radar y frío o caliente (`radar_test.dart`, 7 pruebas)

| 🔴 Rojo | 🟢 Verde |
|---|---|
| ![Ronda 5 rojo](capturas/ronda5r.png) | ![Ronda 5 verde](capturas/ronda5v.png) |

### Ronda 6 · Motor de realidad aumentada (`motor_ar_test.dart`, 5 pruebas)

| 🔴 Rojo | 🟢 Verde |
|---|---|
| ![Ronda 6 rojo](capturas/ronda6r.png) | ![Ronda 6 verde](capturas/ronda6v.png) |

### Ronda 7 · Reglas del juego (`partida_test.dart`, 10 pruebas)

| 🔴 Rojo | 🟢 Verde |
|---|---|
| ![Ronda 7 rojo](capturas/ronda7r.png) | ![Ronda 7 verde](capturas/ronda7v.png) |

### Ronda 10 · ViewModel (`rally_viewmodel_test.dart`, 9 pruebas)

| 🔴 Rojo | 🟢 Verde |
|---|---|
| ![Ronda 10 rojo](capturas/ronda10r.png) | ![Ronda 10 verde](capturas/ronda10v.png) |

### Suite completa

43 pruebas en verde:

![flutter test](capturas/01_flutter_test.png)

---

## Capturas del juego (modo demo)

### 1. Pantalla de inicio
![Pantalla de inicio](capturas/02_pantalla_inicio.png)

### 2. Radar con el letrero "🥶 Helado"
![Radar helado](capturas/03_radar_helado.jpg)

### 3. Personaje en realidad aumentada
![Personaje AR](capturas/04_personaje_ar.jpg)

### 4. Acercándose: "🔥 Caliente"
![Caliente](capturas/05_caliente.jpg)

### 5. A 15 m o menos: "¡Tócame!"
![Tócame](capturas/06_tocame.jpg)

### 6. Pregunta de historia
![Pregunta](capturas/07_pregunta.jpg)

### 7. Dos fallos: el personaje huye
![Huida](capturas/08_huida.jpg)

### 8. Álbum de personajes
![Álbum](capturas/09_album.jpg)

---

## Datos históricos

Los datos del catálogo y las coordenadas son de práctica. Deben verificarse con fuentes históricas locales antes de usar el juego con alumnos.