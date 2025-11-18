Código para detectar vocalizaciones de cangrejos:

1. Filtro Promediador 1: promedia una ventana anti-
pulso deslizante de 15 puntos de muestra. Este filtro
atenúa pulsos unitarios que, al pasar por el filtro
pasa-banda, generarían respuestas al impulso no de-
seadas. El tamaño de ventana se elige de modo de no
afectar la banda de interés (300 kHz/20 kHz = 15).
2. Filtro Pasa Banda: filtro de muy alto orden con
banda de paso [3 kHz, 20 kHz], que selecciona la
región espectral donde se concentran las vocaliza-
ciones de interés.
3. Cálculo de potencia: se calcula la potencia instan-
tánea de la señal filtrada.
4. Filtro Promediador 2: promedia la potencia ins-
tantánea sobre una ventana de 20.000 muestras para
estabilizar el piso de ruido y suavizar las variaciones
rápidas, facilitando la aplicación de un umbral.
5. Discriminador: la potencia promediada se compara
con un umbral adaptativo, generando una señal
binaria que marca la presencia de eventos acústicos
relevantes.
