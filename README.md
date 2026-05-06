# 🎵 Jarvis for Spotify

Controla Spotify con aplausos. Sin tocar el teclado, sin abrir el celular — solo aplaude.

Desarrollado por **Pandiah**.

---

## ✨ ¿Qué hace?

| Acción | Resultado |
|--------|-----------|
| 👏 Un aplauso | Play / Pause |
| 👏👏 Doble aplauso | Siguiente canción (o abre Spotify si está cerrado) |

---

## 🚀 Descarga y uso

> 🎙️ **Importante — antes de abrir el programa:** asegúrate de que tu micrófono esté activo y desbloqueado. Si usas software para silenciar o bloquear el micrófono (como privacidad del sistema, aplicaciones de control de audio, etc.), desactívalo antes de ejecutar Jarvis. Al iniciarse, el programa realiza una **calibración automática de 2 segundos** para medir el ruido ambiente — si el micrófono está bloqueado en ese momento, la calibración fallará y la detección de aplausos no funcionará correctamente.


1. Asegúrate de que tu micrófono esté listo y sin bloquear
2. Ejecútalo — no necesitas instalar Python ni nada más

> ⚠️ Windows puede mostrar una advertencia de SmartScreen la primera vez. Haz clic en **"Más información" → "Ejecutar de todas formas"**.

---

## 🛠️ Ejecutar desde el código fuente

### Requisitos

```bash
pip install PyQt6 pyaudio numpy pyautogui
```

> Si `pyaudio` falla en Windows:
> ```bash
> pip install pipwin
> pipwin install pyaudio
> ```

### Uso

```bash
python jarvis_spotify.py
```

### Opciones

```bash
python jarvis_spotify.py --sensitivity 4       # Ajusta la sensibilidad (default: 5)
python jarvis_spotify.py --no-shape            # Más permisivo con la detección
python jarvis_spotify.py --playlist spotify:playlist:XXXXXX  # Abre una playlist específica
```


## 🔬 ¿Cómo detecta los aplausos?

El detector usa una **huella espectral** de 5 criterios para distinguir aplausos de música:

1. **Transiente** — el sonido debe ser impulsivo, no sostenido
2. **Alta frecuencia** — los aplausos concentran energía por encima de 2 kHz
3. **Planitud espectral** — los aplausos son ruido broadband, no tonos musicales
4. **Tasa de cruces por cero** — los aplausos tienen oscilaciones muy rápidas
5. **Decaimiento rápido** — la segunda mitad del sonido debe ser más silenciosa que la primera

Se necesitan al menos **4 de 5 puntos** para confirmar un aplauso. Esto evita que la música o la voz disparen acciones accidentalmente.

---

## 📋 Requisitos del sistema

- Windows 10 / 11
- Micrófono (integrado o externo)
- Spotify instalado

---

## 📄 Licencia

MIT — úsalo, modifícalo y compártelo libremente.
