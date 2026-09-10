# La actualización de Windows falla o queda trabada

## Síntomas
- Windows Update muestra un error al intentar instalar una actualización (ej. código `0x80070002`, `0x8024402F`).
- La barra de progreso de instalación queda trabada en un porcentaje durante mucho tiempo (ej. "Trabajando en actualizaciones 35%").
- El equipo queda en un ciclo de reinicio intentando aplicar la actualización sin completarla.
- El usuario no puede usar el equipo con normalidad mientras la actualización está en curso o falla repetidamente.

## Causa probable
Archivos de actualización corruptos o incompletos, espacio en disco insuficiente, servicios de Windows Update detenidos o mal configurados, conflicto con software de seguridad de terceros, o problema de conectividad con los servidores de actualización.

## Pasos de diagnóstico
1. Anotar el código de error exacto que muestra Windows Update, si lo hay.
2. Verificar el espacio disponible en el disco del sistema (una actualización puede fallar si no hay suficiente espacio libre).
3. Confirmar el estado de los servicios relacionados: Windows Update, Servicio de Transferencia Inteligente en Segundo Plano (BITS) y Criptográfico.
4. Revisar si hay un antivirus/software de seguridad de terceros que pudiera estar bloqueando el proceso de actualización.
5. Verificar la conectividad a Internet y el acceso a los servidores de Microsoft Update.
6. Ejecutar el "Solucionador de problemas de Windows Update" integrado en el sistema para un diagnóstico automático inicial.

## Solución
1. Si falta espacio en disco, liberar espacio (eliminar archivos temporales, usar Liberador de espacio en disco) y reintentar la actualización.
2. Si los servicios de Windows Update están detenidos, reiniciarlos desde `services.msc` (Windows Update, BITS, Criptográfico).
3. Limpiar la carpeta de caché de actualizaciones (`C:\Windows\SoftwareDistribution`) con los servicios detenidos, y volver a intentar la actualización.
4. Si se sospecha de un conflicto con el antivirus de terceros, desactivarlo temporalmente y reintentar la instalación.
5. Ejecutar `sfc /scannow` y `DISM /Online /Cleanup-Image /RestoreHealth` para reparar posibles archivos de sistema corruptos que afecten la actualización.
6. Si el equipo queda en ciclo de reinicio, forzar un apagado completo, esperar unos minutos y reintentar; si no se resuelve, iniciar en Modo seguro para deshacer la actualización pendiente.

## Cuándo escalar
- Escalar a: Equipo de Infraestructura / Administración de Parches (N2)
- Si: el problema se repite en múltiples equipos de la organización (indicando un problema con el paquete de actualización o el servidor WSUS interno), o la reparación de archivos de sistema no resuelve el ciclo de fallos.

## Tags / Categoría
`Software` `Sistema Operativo` `Windows Update` `Actualizaciones` `N1`
