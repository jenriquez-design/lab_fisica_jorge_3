# Laboratorio Virtual: Caída Libre de una Piedra

Un entorno educativo interactivo, moderno y visualmente atractivo para explorar en profundidad el fenómeno físico de la caída libre según la mecánica clásica newtoniana.

---

## 🚀 Cómo Ejecutar

Simplemente abre el archivo [index.html](file:///C:/Users/Dell/.gemini/antigravity/scratch/caida_libre_lab/index.html) en cualquier navegador web moderno (Google Chrome, Microsoft Edge, Firefox, Safari). No requiere ningún servidor local ni instalación previa de dependencias.

---

## 🔬 Características Principales

1. **Simulación Cinemática en Tiempo Real**:
   - Piedra con textura realista, sombra dinámica y estela de trayectoria.
   - Torre métrica de referencia graduada de $0\text{ m}$ hasta la altura configurada.
   - Línea de referencia del suelo con detección de colisión exacta y sistema de partículas al impactar.

2. **Vectores Cinemáticos Integrados**:
   - **Vector Velocidad ($\vec{v}$)** en color cian/esmeralda: flecha cuya longitud y dirección varían en tiempo real según la rapidez instantánea.
   - **Vector Aceleración ($\vec{a}$)** en color carmesí/rosa: flecha de magnitud constante apuntando siempre hacia el centro gravitatorio ($a = -g$).
   - Etiquetas numéricas en tiempo real acopladas a los vectores.
   - Separación horizontal para evitar solapamientos visuales.

3. **Tres Gráficas Cinemáticas Sincronizadas**:
   - **Posición vs. Tiempo $h(t)$**: Rama de parábola cóncava hacia abajo con marcador de instante actual.
   - **Velocidad vs. Tiempo $v(t)$**: Línea recta de pendiente negativa $-g$ con marcador dinámico.
   - **Aceleración vs. Tiempo $a(t)$**: Línea recta horizontal constante en el valor $-g$.
   - Interactividad bidireccional: mover el deslizador de tiempo actualiza de inmediato las tres gráficas y la piedra.

4. **Comparativa Gravitatoria Planetaria**:
   - **Tierra**: $9.81\text{ m/s}^2$
   - **Luna**: $1.62\text{ m/s}^2$
   - **Marte**: $3.71\text{ m/s}^2$
   - **Venus**: $8.87\text{ m/s}^2$
   - **Júpiter**: $24.79\text{ m/s}^2$
   - **Mercurio**: $3.70\text{ m/s}^2$
   - Atmósferas y superficies visualmente personalizadas para cada mundo.
   - Tabla comparativa que calcula en vivo el tiempo de impacto y la velocidad final en los 6 cuerpos celestes.

5. **Experimentos Interactivos "¿Qué pasaría si...?"**:
   - *¿Qué ocurre si duplicas la altura?* Demuestra por qué el tiempo crece con factor $\sqrt{2} \approx 1.414$ y no al doble.
   - *¿Qué ocurre si cambias de la Tierra a la Luna?* Muestra la caída lenta en gravedad reducida.
   - *¿Qué ocurre si la velocidad inicial es hacia abajo ($v_0 < 0$)?* Comprueba que la aceleración no cambia.
   - *¿En qué planeta llega al suelo con mayor velocidad?* Demuestra la colosal aceleración en Júpiter.

6. **Medidor de Transformación de Energía**:
   - Visualización dinámica de la conservación de la energía mecánica:
     $$E_m = E_p + E_k = mgh + \frac{1}{2}mv^2 = \text{constante}$$
   - Transición progresiva de energía potencial gravitatoria a energía cinética conforme la piedra desciende.

7. **Control de Reproducción y Modos Especiales**:
   - Reproducir, Pausar, Reiniciar y Avance Fotograma a Fotograma (*Step*).
   - Modo Cámara Lenta ($0.2\times$, $0.5\times$ y $1.0\times$).
   - Efectos sonoros sintetizados mediante Web Audio API (opcionales con botón de audio).

---

## 📐 Modelo Físico Matemático

El simulador utiliza las ecuaciones diferenciales ideales de Newton sin resistencia del aire:

$$\frac{d^2 h}{dt^2} = -g \implies a(t) = -g$$
$$\frac{dh}{dt} = v(t) = v_0 - gt$$
$$h(t) = h_0 + v_0 t - \frac{1}{2}gt^2$$

Tiempo hasta el impacto con el suelo ($h = 0$):
$$t_{\text{impacto}} = \frac{v_0 + \sqrt{v_0^2 + 2gh_0}}{g}$$

Velocidad al tocar el suelo:
$$v_{\text{impacto}} = -\sqrt{v_0^2 + 2gh_0}$$
