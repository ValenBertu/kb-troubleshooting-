# El equipo funciona muy lento / rendimiento degradado

## Síntomas
- El equipo tarda mucho en iniciar sesión o en abrir programas comunes.
- El cursor o las aplicaciones se congelan momentáneamente durante el uso normal.
- El ventilador funciona a máxima velocidad de forma constante, incluso sin uso intensivo.
- El problema empeora con el tiempo de uso continuo (arranca bien pero se vuelve lento después de un rato).

## Causa probable
Uso excesivo de CPU/RAM/disco por parte de procesos en segundo plano (incluyendo malware), disco con poco espacio libre o cercano a su capacidad máxima, demasiados programas configurados para iniciar con el sistema, fragmentación o desgaste del disco (en discos mecánicos HDD), o hardware insuficiente para la carga de trabajo actual.

## Pasos de diagnóstico
1. Abrir el Administrador de tareas y revisar el uso de CPU, memoria RAM y disco para identificar procesos que consuman recursos de forma anormal.
2. Verificar el espacio libre en el disco del sistema (un disco casi lleno, especialmente SSD, degrada notablemente el rendimiento).
3. Revisar la lista de programas de inicio (Administrador de tareas > Inicio) para identificar aplicaciones innecesarias que ralentizan el arranque.
4. Ejecutar un análisis completo de antivirus/antimalware para descartar procesos maliciosos consumiendo recursos.
5. Verificar si el equipo cumple con los requisitos mínimos de hardware para el software que utiliza el usuario a diario.
6. Revisar el estado de salud del disco (usando herramientas como `chkdsk` o el estado S.M.A.R.T.) para descartar un disco en proceso de falla.

## Solución
1. Finalizar o desinstalar procesos/programas identificados como responsables del consumo excesivo de recursos.
2. Liberar espacio en disco eliminando archivos temporales, vaciando la papelera y desinstalando programas no utilizados.
3. Deshabilitar programas innecesarios del inicio del sistema para acelerar el arranque y liberar recursos en segundo plano.
4. Si se detecta malware, eliminarlo con las herramientas correspondientes y verificar que el equipo quede limpio.
5. Si el disco es un HDD tradicional y presenta fragmentación alta, ejecutar una desfragmentación (no aplica a discos SSD).
6. Si el hardware es insuficiente para la carga de trabajo actual (poca RAM, disco mecánico lento), evaluar una mejora de hardware como solución a mediano plazo (ej. ampliar RAM, migrar a SSD).

## Cuándo escalar
- Escalar a: Soporte de Hardware / Equipo de Infraestructura (N2)
- Si: el diagnóstico indica que el disco está fallando y requiere reemplazo, el equipo necesita una actualización de hardware que excede el alcance de N1, o el problema persiste en múltiples equipos de forma simultánea (posible causa de red o política de grupo).

## Tags / Categoría
`Rendimiento` `Hardware` `Software` `Malware` `N1`
