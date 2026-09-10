# El usuario no puede enviar ni recibir correos en Outlook

## Síntomas
- Los correos enviados quedan en la bandeja de salida sin enviarse.
- Aparece un error de conexión al servidor ("No se puede conectar al servidor" o similar).
- No llegan correos nuevos aunque otros usuarios sí reciben con normalidad.
- Outlook muestra el estado "Desconectado" o "Intentando conectar" en la barra inferior.

## Causa probable
Problemas de conectividad a Internet, perfil de Outlook corrupto, archivo de datos (.ost/.pst) dañado, credenciales de la cuenta desactualizadas, buzón lleno o caído del lado del servidor de correo, o un add-in de Outlook causando conflictos.

## Pasos de diagnóstico
1. Confirmar si el problema es solo en Outlook o también afecta el acceso al correo vía navegador (webmail), para distinguir si es un problema local o del servidor.
2. Verificar la conectividad general a Internet del equipo.
3. Revisar el estado de la conexión en la esquina inferior de Outlook (Conectado / Desconectado / Modo sin conexión).
4. Comprobar si el usuario tiene activado por error el "Modo sin conexión" (pestaña Enviar y recibir).
5. Verificar el tamaño del buzón y si se superó la cuota asignada.
6. Revisar si el problema comenzó después de instalar un add-in o actualización reciente de Outlook.
7. Consultar si hay un aviso general de caída del servicio de correo (mail server / Microsoft 365 status).

## Solución
1. Si estaba activado el modo sin conexión, desactivarlo desde la pestaña "Enviar y recibir".
2. Si el problema es de conectividad general, resolver primero el acceso a Internet del equipo.
3. Si el buzón está lleno, liberar espacio archivando correos antiguos o solicitando ampliación de cuota.
4. Si se sospecha de un add-in problemático, iniciar Outlook en modo seguro (`outlook.exe /safe`) y deshabilitar add-ins desde Archivo > Opciones > Complementos.
5. Si el archivo de datos está dañado, ejecutar la herramienta de reparación de bandeja de entrada (`scanpst.exe`) sobre el archivo .ost/.pst correspondiente.
6. Si nada de lo anterior funciona, eliminar y volver a configurar el perfil de Outlook desde cero (Panel de control > Cuentas de correo).
7. Confirmar con el usuario que puede enviar y recibir correos de prueba correctamente.

## Cuándo escalar
- Escalar a: Equipo de Mensajería / Administradores de Microsoft 365 o Exchange (N2)
- Si: el problema afecta a múltiples usuarios simultáneamente, se sospecha una caída del servidor de correo, o se requiere intervención sobre permisos/configuración del buzón a nivel servidor.

## Tags / Categoría
`Correo` `Outlook` `Microsoft 365` `Conectividad` `N1`
