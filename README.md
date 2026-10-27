# C-H Studio Android — MVP funcional inicial

## Incluye
- Grabación real del micrófono del dispositivo a M4A/AAC (44.1 kHz).
- Importación de archivos de audio con el selector Android.
- Biblioteca local de grabaciones.
- Reproducción de grabaciones e instrumentales importadas.
- Control de volumen de reproducción.
- Interfaz oscura con acento rosa, estilo estudio musical.

## Requisitos gratuitos
- Android Studio (estable reciente)
- Android SDK Platform 35
- JDK 17 (normalmente incluido con Android Studio)
- Teléfono Android para probar; permite acceso al micrófono cuando se solicite.

## Abrir y ejecutar
1. Descarga y extrae `CH_Studio_Android.zip`.
2. En Android Studio selecciona **Open** y elige la carpeta `CH_Studio_Android`.
3. Espera a que Gradle sincronice. Necesita conexión a internet para descargar dependencias.
4. Si Android Studio solicita instalar Android SDK 35, acepta.
5. Conecta el teléfono por USB y activa las opciones de desarrollador + depuración USB, o usa un emulador.
6. Pulsa **Run**. Concede permiso de micrófono cuando la app lo solicite.
7. Pulsa **REC**, graba unos segundos, pulsa **DETENER** y reproduce la grabación.
8. Pulsa **Importar audio** para cargar una instrumental o una voz existente.

## Limitaciones conocidas de esta versión
Esta es la primera base funcional, no un DAW completo:
- No hay edición por regiones, recorte visual, multipista sincronizada, MIDI/piano roll ni exportación de mezcla.
- El deslizador de reverb es solamente una maqueta visual y aún no procesa el audio.
- El volumen cambia al preparar la reproducción; mover el control durante una pista ya iniciada no actualiza el reproductor en tiempo real.
- Android y los fabricantes varían en latencia, permisos y compatibilidad de códecs.
- No se incluye Auto-Tune real todavía. Para una corrección de tono de calidad hay que integrar un procesador DSP dedicado y probar latencia y calidad en dispositivos reales.

## Próximas etapas sugeridas
1. Reproductor con posición/seek y edición básica de recorte.
2. Motor de audio de baja latencia (Oboe/AAudio) y reproducción sincronizada.
3. Procesamiento DSP real: EQ, compresor, reverb, delay.
4. Grabación multipista y mezcla/exportación WAV.
5. Corrección de tono vocal y presets de trap melódico.
