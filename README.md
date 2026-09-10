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
- _Próximamente_

### Hardware / Equipos
- _Próximamente_

### Software y Sistema Operativo
- _Próximamente_

### VPN y Acceso Remoto
- _Próximamente_

### Backups y Almacenamiento
- _Próximamente_

> El índice se irá actualizando a medida que se agreguen los 15 artículos planificados.

## 🏢 Cómo se usaría en un entorno real

En una empresa, este tipo de artículos vive normalmente en herramientas como **Zendesk Guide, Confluence o ServiceNow Knowledge Base**, integradas con el sistema de tickets: cuando un agente de N1 resuelve un caso, lo documenta acá para que:

- Otros agentes puedan resolver el mismo problema más rápido sin reinventar el diagnóstico.
- Se reduzca el tiempo de resolución (MTTR) en incidentes recurrentes.
- Haya un criterio claro y objetivo de cuándo escalar un caso a otro nivel o equipo.

## 🏷️ Tags utilizados

`Red` · `WiFi` · `Hardware` · `Impresoras` · `Cuentas` · `Accesos` · `Active Directory` · `Seguridad` · `Conectividad` · `N1` · `N2`

---

📌 Proyecto en construcción — se irán sumando artículos hasta completar 15 casos de troubleshooting.
