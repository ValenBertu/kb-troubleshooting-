# El usuario no puede iniciar sesión en su cuenta corporativa

## Síntomas
- Mensaje de "Usuario o contraseña incorrectos" a pesar de ingresar los datos correctos.
- La cuenta indica estar bloqueada o deshabilitada.
- El inicio de sesión se acepta pero luego cierra sesión inmediatamente o no carga el perfil.
- El problema puede ocurrir solo en un dispositivo o en todos los dispositivos del usuario.

## Causa probable
Bloqueo de cuenta por múltiples intentos fallidos, contraseña expirada, problema de sincronización con el directorio activo (AD) o proveedor de identidad, perfil de usuario corrupto en el equipo local, o problema de conectividad con el controlador de dominio.

## Pasos de diagnóstico
1. Confirmar con el usuario la hora exacta en la que empezó el problema y si cambió la contraseña recientemente.
2. Verificar en el Active Directory / proveedor de identidad si la cuenta figura bloqueada, deshabilitada o con la contraseña expirada.
3. Revisar si el usuario puede iniciar sesión desde otro dispositivo o solo falla en el equipo reportado (esto distingue problema de cuenta vs. problema local).
4. Consultar el visor de eventos de Windows (Event Viewer > Seguridad) en busca de errores de autenticación.
5. Verificar que el equipo tenga conectividad con el controlador de dominio (`ping` al DC, o `nltest /dsgetdc:dominio`).
6. Confirmar si hay un aviso de expiración de contraseña o de política de complejidad no cumplida.

## Solución
1. Si la cuenta está bloqueada, desbloquearla desde el AD / panel de administración de identidad.
2. Si la contraseña expiró, forzar un restablecimiento y comunicárselo al usuario de forma segura.
3. Si el problema es solo en un equipo, verificar el perfil de usuario local: puede requerir eliminar el perfil corrupto y dejar que Windows cree uno nuevo en el próximo inicio de sesión.
4. Si hay problemas de conectividad con el controlador de dominio, revisar la configuración de red del equipo (DNS apuntando al DC correspondiente).
5. Confirmar con el usuario que puede iniciar sesión correctamente y que su perfil, accesos y archivos se cargan con normalidad.

## Cuándo escalar
- Escalar a: Equipo de Identidad y Accesos / Administradores de Dominio (N2)
- Si: la cuenta presenta un problema de sincronización entre sistemas (AD, correo, SSO), se sospecha de un incidente de seguridad (intentos de acceso sospechosos), o el desbloqueo/restablecimiento no resuelve el inicio de sesión.

## Tags / Categoría
`Cuentas` `Accesos` `Active Directory` `Seguridad` `N1`
