# El usuario no puede conectarse a la VPN corporativa

## Síntomas
- El cliente VPN muestra un error al intentar conectar (ej. "No se pudo establecer la conexión VPN", timeout de conexión).
- La conexión VPN se establece pero el usuario no puede acceder a recursos internos (servidores, carpetas compartidas, sistemas internos).
- La VPN se conecta y se desconecta de forma intermitente.
- El problema puede ocurrir solo desde ciertas redes (ej. WiFi doméstico) y no desde otras.

## Causa probable
Credenciales incorrectas o vencidas, cliente VPN desactualizado o mal configurado, bloqueo del firewall/router del lado del usuario (puertos VPN bloqueados), certificado de VPN expirado, o caída/saturación del servidor/concentrador VPN del lado de la empresa.

## Pasos de diagnóstico
1. Confirmar que el usuario está ingresando las credenciales correctas y que su cuenta no está bloqueada o con la contraseña vencida.
2. Verificar la versión del cliente VPN instalado y si coincide con la versión soportada por la empresa.
3. Comprobar la conectividad general a Internet del usuario antes de intentar la conexión VPN.
4. Revisar si el problema ocurre en múltiples redes o es específico de una red particular (posible bloqueo de puertos VPN en un router doméstico o de un tercero).
5. Consultar los logs del cliente VPN para identificar el punto exacto donde falla la conexión (autenticación, negociación de túnel, etc.).
6. Verificar del lado del servidor si el concentrador VPN está operativo y si hay otros usuarios reportando el mismo problema.

## Solución
1. Si las credenciales están vencidas o la cuenta bloqueada, restablecer la contraseña o desbloquear la cuenta según corresponda.
2. Si el cliente VPN está desactualizado, actualizarlo a la versión soportada y reintentar la conexión.
3. Si el bloqueo es de un router/firewall del lado del usuario, verificar que los puertos y protocolos necesarios (según el tipo de VPN: IPsec, SSL VPN, etc.) no estén bloqueados, o probar con una red distinta como diagnóstico.
4. Si el certificado de VPN expiró, coordinar con el equipo de seguridad la renovación del certificado del usuario.
5. Si la conexión se cae de forma intermitente, revisar la estabilidad de la conexión a Internet del usuario y, si es estable, reportar el patrón de caídas para análisis del lado del servidor.
6. Confirmar con el usuario que, una vez conectado, puede acceder correctamente a los recursos internos esperados.

## Cuándo escalar
- Escalar a: Equipo de Redes y Seguridad (N2)
- Si: el problema afecta a múltiples usuarios simultáneamente, se sospecha de una caída o saturación del concentrador VPN, o se requiere revisión de reglas de firewall/certificados a nivel de infraestructura.

## Tags / Categoría
`VPN` `Acceso Remoto` `Red` `Seguridad` `Conectividad` `N1`
