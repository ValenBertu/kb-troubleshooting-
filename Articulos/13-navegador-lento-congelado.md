# El navegador carga páginas muy lento o se congela

## Síntomas
- Las páginas web tardan mucho en cargar o quedan "en blanco" varios segundos.
- El navegador se congela ("No responde") al abrir varias pestañas o un sitio en particular.
- El uso de memoria RAM del navegador es anormalmente alto en el Administrador de tareas.
- El problema no ocurre en otros equipos con el mismo sitio web, apuntando a una causa local.

## Causa probable
Demasiadas pestañas o extensiones abiertas consumiendo memoria, caché y cookies acumuladas y corruptas, una extensión específica causando conflictos, versión desactualizada del navegador, o un problema de conectividad/DNS que hace lenta la resolución de sitios.

## Pasos de diagnóstico
1. Verificar cuántas pestañas y extensiones tiene abiertas el usuario y el consumo de RAM del navegador en el Administrador de tareas.
2. Confirmar si el problema ocurre en un sitio específico o en todos los sitios web por igual.
3. Probar el mismo sitio en modo incógnito/privado (que desactiva la mayoría de las extensiones) para aislar si el problema es una extensión.
4. Verificar si el navegador está actualizado a la última versión estable.
5. Probar la velocidad de conexión a Internet y la resolución DNS (por ejemplo, comparando la carga de un sitio vía IP directa vs. nombre de dominio).
6. Revisar el tamaño de la caché y las cookies almacenadas del navegador.

## Solución
1. Si el problema se resuelve en modo incógnito, identificar y deshabilitar la extensión conflictiva desde la configuración de extensiones del navegador.
2. Limpiar caché, cookies y datos de navegación acumulados desde la configuración del navegador.
3. Actualizar el navegador a la última versión disponible.
4. Reducir la cantidad de pestañas/extensiones activas simultáneamente si el consumo de RAM es el causante principal.
5. Si se sospecha de un problema de DNS, cambiar temporalmente a un servidor DNS público confiable y verificar si mejora la velocidad de carga.
6. Como última instancia, reinstalar el navegador o crear un perfil de usuario nuevo dentro del mismo navegador para descartar un perfil corrupto.

## Cuándo escalar
- Escalar a: Equipo de Redes / Seguridad (N2)
- Si: el problema de lentitud ocurre en todos los navegadores y equipos de una misma red (indicando un problema de proxy, DNS o ancho de banda a nivel de infraestructura), o se sospecha de una extensión maliciosa que requiera análisis de seguridad.

## Tags / Categoría
`Software` `Navegador` `Rendimiento` `Conectividad` `N1`
