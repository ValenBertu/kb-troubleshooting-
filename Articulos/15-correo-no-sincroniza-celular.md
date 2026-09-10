# El correo corporativo no sincroniza en el celular

## Síntomas
- La app de correo (Outlook, Gmail u otra) en el celular no muestra correos nuevos que ya llegaron a la bandeja en la PC.
- Aparece un error de autenticación o "No se puede sincronizar la cuenta" en el dispositivo móvil.
- El usuario recibe notificaciones con retraso significativo (varias horas) respecto a la llegada real del correo.
- El problema ocurre solo en el celular, mientras que en la PC/webmail el correo funciona con normalidad.

## Causa probable
Política de acceso condicional o MDM (gestión de dispositivos móviles) que bloquea el dispositivo por no cumplir requisitos, credenciales o token de autenticación vencido en la app móvil, configuración incorrecta de sincronización, conexión de datos/WiFi inestable en el dispositivo, o límite de dispositivos vinculados alcanzado en la cuenta.

## Pasos de diagnóstico
1. Confirmar que el correo funciona con normalidad en la PC/webmail, para aislar el problema al dispositivo móvil.
2. Verificar el estado de la conexión a Internet del celular (WiFi y datos móviles).
3. Revisar si la app de correo solicita reingresar credenciales o muestra algún mensaje de error específico.
4. Si la empresa usa una solución de gestión de dispositivos móviles (MDM/Intune), verificar el estado de cumplimiento (compliance) del dispositivo.
5. Confirmar si el dispositivo está dentro del límite de dispositivos permitidos por la política de la organización.
6. Revisar la configuración de sincronización dentro de la app (frecuencia de sincronización, carpetas seleccionadas).

## Solución
1. Si las credenciales o el token vencieron, cerrar sesión y volver a iniciar sesión en la app de correo del celular.
2. Si el dispositivo no cumple con las políticas de seguridad del MDM (ej. falta PIN, cifrado desactivado), guiar al usuario para ajustar la configuración requerida y volver a registrar el dispositivo.
3. Si hay un problema de conectividad, probar alternando entre WiFi y datos móviles para descartar una red específica como causa.
4. Si se alcanzó el límite de dispositivos vinculados, dar de baja un dispositivo antiguo o no utilizado desde el panel de administración de la cuenta.
5. Ajustar la configuración de sincronización dentro de la app si estaba mal configurada (frecuencia, carpetas).
6. Como última instancia, eliminar la cuenta de la app de correo del celular y volver a configurarla desde cero.

## Cuándo escalar
- Escalar a: Equipo de Identidad y Dispositivos Móviles / MDM (N2)
- Si: el problema está relacionado con políticas de acceso condicional o cumplimiento que el usuario no puede resolver por sí mismo, se requiere acceso al panel de administración de MDM, o el problema afecta a varios dispositivos móviles de la organización simultáneamente.

## Tags / Categoría
`Móviles` `Correo` `MDM` `Accesos` `Seguridad` `N1`
