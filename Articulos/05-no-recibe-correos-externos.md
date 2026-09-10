# El usuario no recibe correos externos, pero sí internos

## Síntomas
- El usuario recibe correos de compañeros de la misma empresa sin problema.
- No le llegan correos de remitentes externos (clientes, proveedores).
- El remitente externo confirma haber enviado el correo y no recibió ningún rebote (bounce).
- El problema puede afectar a un solo usuario o a un dominio/área completa.

## Causa probable
El correo externo está siendo bloqueado o marcado como spam/cuarentena por el filtro anti-spam, reglas de bandeja de entrada mal configuradas que mueven o eliminan correos automáticamente, el dominio remitente está en una lista negra (blacklist), o hay un problema de reputación/SPF-DKIM-DMARC en la configuración de correo entrante.

## Pasos de diagnóstico
1. Pedir al usuario que revise las carpetas de Spam/Correo no deseado y Elementos eliminados.
2. Revisar si el usuario tiene reglas de bandeja de entrada configuradas que podrían estar moviendo o eliminando correos automáticamente.
3. Verificar en el panel de administración de correo (ej. Microsoft 365 Defender / Exchange Admin Center) si el mensaje quedó en cuarentena.
4. Solicitar al remitente externo el mensaje de error o rebote, si lo tuvo, para identificar el motivo del rechazo.
5. Verificar si el dominio o la IP del remitente figura en alguna lista negra pública (blacklist) usando herramientas de consulta de reputación.
6. Confirmar si el problema es exclusivo de ese usuario o si afecta a otros usuarios del mismo dominio.

## Solución
1. Si el correo estaba en cuarentena, liberarlo desde el panel de administración y, si corresponde, agregar el remitente a la lista de confianza (allow list).
2. Si había una regla de bandeja mal configurada, corregirla o eliminarla junto con el usuario.
3. Si el dominio remitente está en una blacklist, coordinar con el equipo de seguridad/mensajería para gestionar el delisting o ajustar las políticas de filtrado.
4. Si el problema es puntual de un usuario, revisar y ajustar su configuración de filtrado de spam individual.
5. Confirmar con el remitente externo que reenvíe el correo y validar que llegue correctamente a la bandeja de entrada.

## Cuándo escalar
- Escalar a: Equipo de Seguridad de Correo / Administradores de Exchange (N2)
- Si: el problema afecta a todo un dominio o área, se requiere modificar políticas de filtrado anti-spam a nivel organización, o se sospecha de un problema de reputación (SPF/DKIM/DMARC) que requiere cambios en la configuración DNS.

## Tags / Categoría
`Correo` `Spam` `Seguridad` `Exchange` `N1`
