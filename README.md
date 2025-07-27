# 24h-projects

**Autor:** César Perales (causa_code)

## Qué es esto

5 proyectos web simples hechos en HTML/CSS/JS vanilla. Cada uno se puede hacer en menos de 24 horas. Código limpio para aprender.

## Los Proyectos

### 1. Calculadora BMO
Una calculadora que hace sonidos cuando clickeas los botones.

**Cómo implementarlo:**
```
1. Crear botones en grid 4x4
2. Pantalla que muestre números
3. Variables: numeroActual, numeroAnterior, operador
4. Función para cada botón que actualice las variables
5. Audio API: crear oscillator + gainNode, tocar por 0.1 segundos
6. Al hacer =, evaluar la operación y mostrar resultado
```

### 2. Todo List que se Autodestruye
Lista de tareas que se borra sola después de X horas.

**Cómo implementarlo:**
```
1. Input + botón para agregar tareas
2. Array de objetos {id, texto, completado}
3. Timer: guardar Date.now() al inicio
4. setInterval cada segundo calculando tiempo restante
5. Mostrar countdown en formato HH:MM:SS
6. Cuando llegue a 0, borrar todo y mostrar pantalla negra
7. Shake CSS al eliminar: transform translateX(-5px, 5px)
```

### 3. Flappy Bird con tu Cara
Flappy Bird normal pero tu cara es el pájaro.

**Cómo implementarlo:**
```
1. Canvas + video element oculto
2. getUserMedia para obtener stream de cámara
3. Objeto pájaro: {x, y, velocidad}
4. Array de tubos: {x, alturaArriba, abajoY}
5. Game loop: actualizar posición, dibujar, detectar colisiones
6. drawImage(video, x, y) para dibujar la cara
7. Gravedad: velocidad += 0.5 cada frame
8. Salto: velocidad = -8
```

### 4. Detector de Emociones
Escribes texto y te dice qué emoción tienes.

**Cómo implementarlo:**
```
1. Textarea que escuche onChange
2. Función limpiarTexto: quitar stopwords y puntuación
3. Objeto emociones con keywords:
   feliz: ['alegre', 'genial', 'bien']
   triste: ['mal', 'horrible', 'feo']
4. Para cada palabra, buscar en qué emoción aparece
5. Contar puntos por emoción
6. Mostrar la emoción con más puntos
7. Bonus: cambiar colores de fondo según emoción dominante
```

### 5. Simulador de Entrevistas IA
Chatbot que te hace preguntas técnicas usando Gemini API.

**Cómo implementarlo:**
```
1. Input para API key de Google AI Studio
2. Array con 15 preguntas técnicas predefinidas
3. Variable contador de preguntas (máximo 10)
4. 50% probabilidad: usar pregunta random del array
5. 50% probabilidad: mandar historial a Gemini para generar nueva pregunta
6. Fetch a: generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent
7. Mostrar mensajes en formato chat (izquierda IA, derecha usuario)
8. Al llegar a 10 preguntas, mostrar resumen final
```

## Configuración Rápida

**Todo List Timer:**
Cambiar `const TIMER_HOURS = 24` por lo que quieras

**Emociones:**
Agregar palabras al objeto `EMOTIONS`

**Entrevista:**
Necesitas API key de [Google AI Studio](https://aistudio.google.com/)

## Instalación

Clona el repo, abre cualquier HTML en el navegador. Ya.

## Notas

- El de la cámara necesita HTTPS en producción
- Todos funcionan offline excepto el simulador de entrevistas
- Código simple sin frameworks para que sea fácil de entender
