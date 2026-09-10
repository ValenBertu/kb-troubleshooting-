# El equipo no logra conectarse a la red WiFi

## Síntomas
- El usuario ve la red WiFi en la lista pero no logra conectarse.
- Aparece el mensaje "No se pudo conectar a esta red" o similar.
- La conexión se establece pero no hay acceso a Internet ("sin Internet, protegido").
- El problema puede afectar a un solo equipo o a varios dentro de la misma oficina/área.

## Causa probable
Puede deberse a credenciales incorrectas, un adaptador de red con drivers desactualizados o corruptos, conflicto de IP, un perfil de red guardado dañado, o un problema del lado del router/AP (saturación de canal, DHCP agotado).

## Pasos de diagnóstico
1. Confirmar si el problema es puntual (un solo equipo) o generalizado (varios usuarios reportan lo mismo al mismo tiempo).
2. Verificar que el usuario esté ingresando la contraseña correcta y seleccionando la red correcta (puede haber SSIDs duplicados o de invitados).
3. Comprobar el estado del adaptador de red en el equipo (Administrador de dispositivos > Adaptadores de red) — buscar íconos de advertencia.
4. Ejecutar `ipconfig /all` (Windows) o `ifconfig` (Linux/Mac) para verificar si el equipo obtuvo una IP válida o quedó con una IP APIPA (169.254.x.x).
5. Probar conectar el mismo equipo a otra red WiFi conocida (por ejemplo, un hotspot móvil) para descartar que el problema sea del hardware del equipo.
6. Revisar en el router/AP la cantidad de dispositivos conectados y si el pool de DHCP está agotado.

## Solución
1. Si las credenciales eran incorrectas, reingresarlas y olvidar/reconectar la red desde cero (eliminar el perfil guardado).
2. Si el adaptador de red presenta errores, actualizar o reinstalar el driver del adaptador WiFi.
3. Si la IP es APIPA, liberar y renovar la IP: `ipconfig /release` seguido de `ipconfig /renew`.
4. Si el problema es generalizado, reiniciar el punto de acceso/router y verificar la configuración de DHCP (ampliar el rango si está agotado).
5. Si persiste en un solo equipo, restablecer la configuración de red del sistema operativo (network reset) y reiniciar el equipo.
6. Verificar que el firmware del router/AP esté actualizado.

## Cuándo escalar
- Escalar a: Equipo de Redes (N2)
- Si: el problema afecta a múltiples usuarios/equipos simultáneamente, se sospecha de un problema en el AP/switch/controlador WiFi, o se requiere acceso a la configuración de infraestructura de red que no está disponible en N1.

## Tags / Categoría
`Red` `WiFi` `Conectividad` `N1` `Hardware`
