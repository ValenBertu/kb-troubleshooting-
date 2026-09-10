# Word o Excel se cierra inesperadamente o deja de responder

## Síntomas
- La aplicación (Word, Excel u otra de Office) se cierra sola sin mensaje de error, o muestra "Ha dejado de funcionar".
- El programa se congela ("No responde") al abrir un archivo específico o al realizar una acción puntual (ej. usar una macro, insertar una imagen).
- El problema ocurre solo con determinados archivos y no con documentos nuevos en blanco.
- Se pierden cambios no guardados de forma recurrente por estos cierres inesperados.

## Causa probable
Complemento (add-in) de Office corrupto o incompatible, archivo específico dañado o con formato corrupto, instalación de Office con archivos dañados, falta de actualizaciones de Office, o conflicto con la plantilla normal.dotm/personal.xlsb del usuario.

## Pasos de diagnóstico
1. Confirmar si el problema ocurre con todos los archivos o solo con uno o unos pocos documentos específicos.
2. Verificar si el problema ocurre también al abrir un documento nuevo en blanco (esto distingue problema de archivo vs. problema de la aplicación).
3. Revisar si hay complementos (add-ins) de terceros instalados que coincidan con el momento en que comenzó el problema.
4. Comprobar la versión de Office instalada y si hay actualizaciones pendientes.
5. Revisar el Visor de eventos de Windows (Aplicación) para identificar el módulo específico que causa el cierre.
6. Intentar abrir el archivo problemático en modo seguro (`winword /safe` o `excel /safe`) para descartar conflictos de plantillas o add-ins.

## Solución
1. Si el problema es específico de un archivo, intentar abrirlo en modo seguro o copiar el contenido a un documento nuevo para descartar corrupción del archivo original.
2. Si se identifica un add-in problemático, deshabilitarlo desde Archivo > Opciones > Complementos y confirmar si el problema se resuelve.
3. Si el problema es general de la aplicación, actualizar Office a la última versión disponible.
4. Si persiste, ejecutar una reparación de Office desde Panel de Control > Programas > Office > Cambiar > Reparación rápida (o reparación en línea si la rápida no resuelve).
5. Si se sospecha de la plantilla normal.dotm/personal.xlsb dañada, renombrarla o eliminarla para que la aplicación genere una nueva por defecto.
6. Confirmar con el usuario que el archivo y la aplicación funcionan con normalidad después de aplicar la solución.

## Cuándo escalar
- Escalar a: Soporte de Aplicaciones / Administradores de Microsoft 365 (N2)
- Si: el problema se repite en múltiples equipos después de una actualización de Office (posible bug de una versión específica), o se requiere una reinstalación completa de la suite de Office que excede el alcance de N1.

## Tags / Categoría
`Software` `Office` `Word` `Excel` `Aplicaciones` `N1`
