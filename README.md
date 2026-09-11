# Base de Conocimiento (KB) de Troubleshooting

Repositorio con una base de conocimiento de troubleshooting de IT, pensada para simular cómo se documentan y resuelven incidentes técnicos en un entorno corporativo real (estilo Zendesk, Confluence o ServiceNow).

## 🎯 Objetivo

Este proyecto no busca ser una colección de notas sueltas, sino demostrar el formato y el criterio con el que se documenta un problema técnico en un equipo de soporte profesional: identificación clara del síntoma, diagnóstico estructurado, solución reproducible y criterio de escalación.

Lo armé como parte de mi portfolio para roles de **IT Support / Helpdesk / Service Desk**, mostrando cómo pienso y documento la resolución de incidentes.

## 🗂️ Estructura de cada artículo

Todos los artículos siguen la misma plantilla, para que la base de conocimiento sea consistente y fácil de navegar:

- **Título del problema** — claro y buscable
- **Síntomas** — qué observa el usuario
- **Causa probable** — hipótesis más comunes
- **Pasos de diagnóstico** — numerados, de lo más simple a lo más complejo
- **Solución** — paso a paso
- **Cuándo escalar** — a qué nivel/equipo si no se resuelve
- **Tags / Categoría**

Podés ver la plantilla en blanco en [`plantilla/template-articulo.md`](./Plantilla/template-articulo.md).

## 📚 Índice de artículos

### Red y Conectividad
- [No conecta a la red WiFi](./Articulos/01-no-conecta-wifi.md)
- [Impresora de red no responde](./Articulos/02-impresora-no-responde-red.md)

### Cuentas y Accesos
- [Usuario no puede iniciar sesión en su cuenta corporativa](./Articulos/03-usuario-no-puede-iniciar-sesion.md)

### Correo y Comunicaciones
- [No se puede enviar ni recibir correos en Outlook](./Articulos/04-outlook-no-envia-recibe-correo.md)
- [No recibe correos externos, pero sí internos](./Articulos/05-no-recibe-correos-externos.md)

### Hardware / Equipos
- [El equipo no enciende / no bootea](./Articulos/06-equipo-no-enciende.md)

### Software y Sistema Operativo
- [Pantalla azul (BSOD) recurrente en Windows](./Articulos/07-pantalla-azul-bsod.md)
- [La actualización de Windows falla o queda trabada](./Articulos/08-windows-update-falla.md)

### VPN y Acceso Remoto
- [El usuario no puede conectarse a la VPN corporativa](./Articulos/09-no-conecta-vpn.md)

### Backups y Almacenamiento
- [El backup automático falla o no se completa](./Articulos/10-backup-automatico-falla.md)

### Rendimiento
- [El equipo funciona muy lento / rendimiento degradado](./Articulos/11-equipo-lento-rendimiento.md)

### Aplicaciones de Oficina
- [Word o Excel se cierra inesperadamente o deja de responder](./Articulos/12-office-se-cierra-no-responde.md)
- [El navegador carga páginas muy lento o se congela](./Articulos/13-navegador-lento-congelado.md)

### Seguridad
- [Se sospecha de malware o infección en el equipo](./Articulos/14-sospecha-malware.md)

### Dispositivos Móviles
- [El correo corporativo no sincroniza en el celular](./Articulos/15-correo-no-sincroniza-celular.md)

> El índice se irá actualizando a medida que se agreguen los 15 artículos planificados.

## 🏢 Cómo se usaría en un entorno real

En una empresa, este tipo de artículos vive normalmente en herramientas como **Zendesk Guide, Confluence o ServiceNow Knowledge Base**, integradas con el sistema de tickets: cuando un agente de N1 resuelve un caso, lo documenta acá para que:

- Otros agentes puedan resolver el mismo problema más rápido sin reinventar el diagnóstico.
- Se reduzca el tiempo de resolución (MTTR) en incidentes recurrentes.
- Haya un criterio claro y objetivo de cuándo escalar un caso a otro nivel o equipo.

## 🏷️ Tags utilizados

`Red` · `WiFi` · `Hardware` · `Impresoras` · `Cuentas` · `Accesos` · `Active Directory` · `Seguridad` · `Conectividad` · `Correo` · `Outlook` · `Microsoft 365` · `Spam` · `Exchange` · `Encendido` · `Notebook` · `PC de escritorio` · `Software` · `Sistema Operativo` · `Windows` · `BSOD` · `Drivers` · `Windows Update` · `Actualizaciones` · `VPN` · `Acceso Remoto` · `Backups` · `Almacenamiento` · `Continuidad de Datos` · `Rendimiento` · `Malware` · `Ransomware` · `Antivirus` · `Office` · `Word` · `Excel` · `Aplicaciones` · `Navegador` · `Móviles` · `MDM` · `N1` · `N2`

---

✅ Base de conocimiento completa: 15 artículos cubriendo Red, Hardware, Cuentas y Accesos, Correo, Software y Sistema Operativo, VPN, Backups, Rendimiento, Aplicaciones de Oficina, Seguridad y Dispositivos Móviles.
