# El backup automático falla o no se completa

## Síntomas
- El software de backup muestra un estado de "Fallido" o "Incompleto" en el último trabajo programado.
- El usuario recibe (o no recibe) una notificación de error del sistema de backup.
- El backup se detiene siempre en el mismo punto o porcentaje.
- Al intentar restaurar un archivo, se descubre que el backup más reciente disponible es más viejo de lo esperado.

## Causa probable
Espacio insuficiente en el destino de backup (disco local, NAS o almacenamiento en la nube), credenciales o permisos vencidos hacia el destino, archivos en uso o bloqueados durante el proceso de backup, conexión de red interrumpida hacia el repositorio, o un trabajo programado mal configurado.

## Pasos de diagnóstico
1. Revisar el log/historial del software de backup para identificar el mensaje de error específico del último intento fallido.
2. Verificar el espacio disponible en el destino de backup (disco, NAS, almacenamiento en la nube).
3. Confirmar que las credenciales de la cuenta o servicio usado para el backup no hayan expirado o cambiado.
4. Revisar la conectividad de red hacia el destino de backup al momento programado del trabajo.
5. Verificar si hay archivos grandes o en uso constante que puedan estar causando bloqueos durante el proceso.
6. Confirmar que el trabajo programado (schedule) esté correctamente configurado y no se haya desactivado por error.

## Solución
1. Si el destino está sin espacio, liberar espacio eliminando backups antiguos según la política de retención, o ampliar el almacenamiento disponible.
2. Si las credenciales expiraron, actualizarlas en la configuración del software de backup.
3. Si hay problemas de conectividad, verificar la red hacia el destino y, si es posible, reprogramar el trabajo fuera de horarios de alta carga de red.
4. Si ciertos archivos bloquean el proceso, excluirlos temporalmente o usar una solución de backup con soporte para copias de volumen en sombra (VSS) que permita respaldar archivos en uso.
5. Corregir la configuración del trabajo programado si se detectó un error (horario, selección de carpetas, cuenta de servicio).
6. Ejecutar un backup manual de prueba después de aplicar la corrección para confirmar que el proceso se completa correctamente.

## Cuándo escalar
- Escalar a: Equipo de Infraestructura / Administración de Backups (N2)
- Si: el problema afecta al backup de servidores críticos, se sospecha de una falla en el sistema de almacenamiento (NAS/SAN), o han pasado múltiples ciclos sin un backup exitoso y se requiere garantizar la continuidad de la protección de datos.

## Tags / Categoría
`Backups` `Almacenamiento` `Continuidad de Datos` `N1`
