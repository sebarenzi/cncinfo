
 
 1. No muevas la pieza del lugar, la recuperación solo será precisa si la pieza no se ha movido respecto al origen (cero) que usaste al empezar.

 2. Reinicia UGS y el CNC, enciende el CNC y conecta de nuevo UGS.
  Re-haz el homing si tu máquina tiene sensores. Si no, deberás reestablecer el punto cero manualmente.

 3. Reestablece el “Zero” manualmente
  Lleva la herramienta exactamente al mismo punto de inicio (X, Y, Z).
  Usa Reset Zero en UGS para fijar ese punto como origen otra vez.

 4. Identifica la última línea de G-code ejecutada, UGS generalmente no guarda la línea exacta, pero puedes ver el punto donde el corte quedó interrumpido.
  Abre tu archivo .gcode o .nc en un editor de texto.
  Busca la coordenada más cercana donde se detuvo el corte.
  Puedes usar un visualizador de G-code como ncviewer.com para ayudarte.

 5. Crea un archivo nuevo desde esa línea
  Corta el G-code desde donde se detuvo (o un poco antes por seguridad).
  Guarda ese fragmento como un nuevo archivo .gcode.
  Carga ese nuevo archivo en UGS y lánzalo desde el nuevo cero.
