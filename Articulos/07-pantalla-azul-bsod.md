# Pantalla azul (BSOD) recurrente en Windows

## Síntomas
- El equipo muestra una pantalla azul con un código de error (ej. `MEMORY_MANAGEMENT`, `DRIVER_IRQL_NOT_LESS_OR_EQUAL`) y se reinicia solo.
- El problema ocurre de forma esporádica o cada vez que se realiza una acción específica (abrir cierto programa, conectar un periférico).
- El usuario reporta pérdida de trabajo no guardado por los reinicios inesperados.
- Puede ocurrir tanto en el arranque como durante el uso normal del equipo.

## Causa probable
Drivers desactualizados, corruptos o incompatibles (especialmente de video o red), problema de memoria RAM defectuosa, sobrecalentamiento del hardware, corrupción de archivos del sistema, o conflicto causado por una actualización reciente de Windows o de algún software.

## Pasos de diagnóstico
1. Anotar el código de error exacto que muestra la pantalla azul (aparece en la parte inferior del mensaje).
2. Revisar el Visor de eventos de Windows (Event Viewer > Registros de Windows > Sistema) en busca de errores relacionados al momento del BSOD.
3. Identificar si el problema comenzó después de instalar un programa, driver o actualización específica.
4. Verificar la temperatura y el estado de ventilación del equipo (sobrecalentamiento como posible causa).
5. Ejecutar el diagnóstico de memoria de Windows (`mdsched.exe`) para descartar RAM defectuosa.
6. Ejecutar `sfc /scannow` para verificar la integridad de los archivos del sistema.
7. Revisar si hay drivers marcados con advertencia en el Administrador de dispositivos.

## Solución
1. Si se identificó un driver problemático (frecuentemente de video o red), actualizarlo o revertirlo a una versión anterior estable.
2. Si el problema surgió tras una actualización de Windows, desinstalar la actualización reciente y posponerla hasta que haya un parche estable.
3. Si `sfc /scannow` detecta y repara archivos corruptos, reiniciar el equipo y confirmar si el problema persiste.
4. Si el diagnóstico de memoria detecta errores, reemplazar el módulo de RAM defectuoso.
5. Si se confirma sobrecalentamiento, limpiar el sistema de ventilación o revisar la pasta térmica del procesador.
6. Si el problema persiste sin causa clara, considerar una reparación del sistema operativo o reinstalación limpia como última instancia.

## Cuándo escalar
- Escalar a: Soporte de Hardware / Especialista en Sistemas (N2)
- Si: el diagnóstico apunta a una falla de hardware (RAM, placa madre, disco), el BSOD persiste después de descartar drivers y software, o se requiere análisis de archivos de volcado de memoria (memory dump) para identificar la causa raíz.

## Tags / Categoría
`Software` `Sistema Operativo` `Windows` `BSOD` `Drivers` `N1`
