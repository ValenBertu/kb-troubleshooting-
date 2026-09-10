# La impresora de red no responde / no imprime

## Síntomas
- Los documentos quedan encolados en la cola de impresión sin imprimirse.
- El usuario recibe un error del tipo "Impresora fuera de línea" o "No se puede conectar con la impresora".
- La impresora aparece disponible en la red pero no procesa los trabajos.
- Algunos usuarios pueden imprimir y otros no, dentro de la misma impresora compartida.

## Causa probable
Cola de impresión trabada por un trabajo corrupto, la impresora perdió conectividad de red (IP cambiada por DHCP), el spooler de impresión dejó de responder, o el driver instalado no coincide con el modelo/firmware de la impresora.

## Pasos de diagnóstico
1. Verificar el estado físico de la impresora: encendida, con papel, sin atascos ni errores en su panel.
2. Confirmar si el problema es de un solo usuario o de todos los que imprimen en esa impresora.
3. Hacer ping a la IP de la impresora desde el equipo del usuario para confirmar conectividad de red.
4. Revisar la cola de impresión de Windows (`Panel de control > Dispositivos e impresoras`) para ver si hay trabajos atascados.
5. Verificar en el servicio "Cola de impresión" (Print Spooler) si está corriendo correctamente.
6. Comparar la IP configurada en el driver de impresora del equipo contra la IP real actual de la impresora (pudo cambiar si no tiene IP fija).

## Solución
1. Si hay trabajos atascados, cancelar todos los documentos de la cola y reiniciar el servicio Print Spooler.
2. Si la IP cambió, actualizar la IP en las propiedades del puerto de la impresora o reconfigurar la IP fija en la impresora desde su panel/página web de administración.
3. Si el ping no responde, reiniciar la impresora (apagar/encender) y revisar su conexión de red física o WiFi.
4. Si el problema persiste en un solo equipo, eliminar la impresora y volver a instalarla con el driver correcto y actualizado.
5. Si afecta a todos los usuarios, verificar el estado del servidor de impresión (si existe) y reiniciar el servicio de impresión compartida.

## Cuándo escalar
- Escalar a: Soporte de Infraestructura / Proveedor de la impresora (N2)
- Si: la impresora presenta un error de hardware persistente, requiere actualización de firmware, o el problema está en el servidor de impresión central y no en los equipos cliente.

## Tags / Categoría
`Hardware` `Impresoras` `Red` `N1`
