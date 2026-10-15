# 🌴 Jungle Hits

Organizador de archivos de música con inteligencia artificial.

Jungle Hits escanea una biblioteca de música desordenada, identifica cada pista, completa sus metadatos y la ordena en una estructura de carpetas limpia y consistente.

## ¿Qué hace?

- **Escanea** carpetas con archivos de audio (MP3, FLAC, WAV, M4A, OGG…).
- **Identifica** las canciones mediante huellas acústicas y los metadatos existentes (tags ID3, nombre de archivo).
- **Enriquece** los metadatos con IA: artista, título, álbum, año, género, etc.
- **Clasifica** por género, estado de ánimo, energía o BPM.
- **Detecta duplicados** y versiones de baja calidad.
- **Renombra y mueve** los archivos a una estructura ordenada, con modo de simulación previo.

## Estructura de destino (ejemplo)

```
Musica/
├── Artista/
│   └── Año - Álbum/
│       ├── 01 - Título.mp3
│       └── 02 - Título.mp3
└── _Revisar/        # pistas que la IA no pudo identificar con confianza
```

## Cómo funciona

1. **Escaneo**: se recorre la carpeta de origen y se lee la información básica de cada archivo.
2. **Análisis**: se generan huellas acústicas y se consultan servicios de identificación musical.
3. **IA**: un modelo de lenguaje resuelve ambigüedades, normaliza nombres y propone clasificaciones.
4. **Plan**: se genera un plan de cambios (renombrados, movimientos, tags) que se puede revisar.
5. **Aplicación**: tras confirmar, se ejecutan los cambios. Nunca se borra nada sin confirmación.

## Estado del proyecto

🚧 En fase inicial. Este repositorio todavía no contiene código; el README describe la visión y el alcance previstos.

## Hoja de ruta

- [ ] Escáner de biblioteca y lectura de metadatos
- [ ] Identificación por huella acústica
- [ ] Normalización y enriquecimiento de tags con IA
- [ ] Clasificación por género / mood / BPM
- [ ] Detección de duplicados
- [ ] Modo simulación (`--dry-run`) y plan de cambios revisable
- [ ] Interfaz de línea de comandos (CLI)
- [ ] Informe final de la organización

## Uso previsto

```bash
# Simular sin tocar nada
jungle-hits organize ~/Descargas/Musica --dest ~/Musica --dry-run

# Aplicar los cambios
jungle-hits organize ~/Descargas/Musica --dest ~/Musica
```

> Los comandos son orientativos y pueden cambiar durante el desarrollo.

## Principios

- **Seguro**: operaciones reversibles y siempre con vista previa.
- **Transparente**: cada decisión de la IA queda registrada y se puede revisar.
- **Local primero**: los archivos de audio no salen de tu equipo; solo se envían metadatos cuando es necesario.

## Contribuir

Las ideas y contribuciones son bienvenidas. Abre un issue para proponer cambios antes de enviar un pull request.

## Licencia

Por definir.
