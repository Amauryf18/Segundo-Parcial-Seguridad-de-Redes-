# Análisis CIS Benchmark – Router Cisco R1

## 1. Descripción del proyecto

Este proyecto tiene como objetivo realizar una evaluación de seguridad sobre un router Cisco mediante una herramienta de auditoría automatizada basada en las recomendaciones del **Center for Internet Security (CIS)**.

La evaluación permite identificar configuraciones inseguras, debilidades en los mecanismos de administración y posibles incumplimientos de las buenas prácticas de seguridad recomendadas para dispositivos de infraestructura de red.

Se utilizará la herramienta **ONYX – Cisco Automated Assessment and Auditing Tool** para realizar la evaluación inicial del router y generar un informe con los hallazgos identificados.

## 2. Objetivos

- Evaluar la configuración de seguridad del router Cisco.
- Identificar incumplimientos de las recomendaciones CIS.
- Analizar los mecanismos de administración y acceso remoto.
- Identificar configuraciones inseguras en los servicios de red.
- Generar un informe inicial de auditoría.
- Documentar los hallazgos que posteriormente servirán como referencia para aplicar medidas de hardening.

## 3. Entorno de laboratorio

| Componente | Descripción |
|---|---|
| Dispositivo auditado | Router Cisco R1 |
| Dirección IP | 10.23.13.1 |
| Sistema operativo | Cisco IOS 15.2(4)S6 |
| Herramienta de auditoría | ONYX |
| Sistema de auditoría | Ubuntu Server |
| Protocolo de administración | SSH |
| Estándar de referencia | CIS Benchmark |
| Identificador académico | Matrícula terminada en 1323 |

## 4. Herramienta utilizada

### ONYX – Cisco Automated Assessment and Auditing Tool

ONYX es una herramienta orientada a la evaluación automatizada de configuraciones de dispositivos Cisco.

Permite revisar parámetros de seguridad del dispositivo, identificar configuraciones que no cumplen con las recomendaciones de seguridad y generar resultados de auditoría.

Repositorio de la herramienta:

https://github.com/UncleSocks/Onyx

### Funciones utilizadas

- Conexión remota al dispositivo Cisco mediante SSH.
- Evaluación de configuraciones de seguridad.
- Comparación con controles de referencia CIS compatibles.
- Identificación de controles aprobados y fallidos.
- Generación de informes de auditoría.

## 5. Metodología de evaluación

La auditoría se desarrollará en las siguientes etapas:

**Fase 1 – Preparación**

Se prepara el entorno Ubuntu Server y se instala la herramienta de auditoría. Se verifica la conectividad con el router y la disponibilidad del acceso administrativo SSH.

**Fase 2 – Auditoría inicial**

Se ejecuta el análisis del router Cisco sin modificar su configuración. El propósito es obtener una referencia del estado de seguridad original del dispositivo.

**Fase 3 – Identificación de hallazgos**

Se revisan los controles evaluados y se clasifican según los resultados obtenidos:

- PASS: configuración que cumple el control evaluado.
- FAIL: configuración que no cumple el control evaluado.
- NA / Unchecked: control no aplicable o que no pudo evaluarse.

**Fase 4 – Documentación**

Se recopilan los resultados, capturas de pantalla e informe generado por la herramienta para documentar el estado inicial de seguridad del router.

## 6. Controles de seguridad evaluados

La auditoría estará orientada a revisar aspectos como:

| Área | Aspecto evaluado |
|---|---|
| Administración | Acceso administrativo seguro |
| Autenticación | Usuarios y contraseñas |
| SSH | Administración remota cifrada |
| AAA | Autenticación y autorización |
| SNMP | Configuración del protocolo de monitoreo |
| Servicios | Servicios innecesarios |
| Contraseñas | Protección de credenciales |
| Logging | Registro de eventos |
| Control de acceso | Listas de control de acceso |
| Plano de control | Protección de los servicios de administración |

Los controles definitivos dependerán de los controles incluidos en la versión del benchmark compatible con el dispositivo.

## 7. Resultados de la auditoría inicial

En esta sección se documentarán los resultados obtenidos durante el primer análisis del router Cisco R1.

**Estado inicial:** Pendiente de incorporar el informe real generado por ONYX.

| Indicador | Resultado |
|---|---|
| Total de controles evaluados | Pendiente |
| Controles PASS | Pendiente |
| Controles FAIL | Pendiente |
| Controles NA / Unchecked | Pendiente |
| Estado general | Pendiente |

### Hallazgos identificados

Se documentarán los controles que presenten incumplimientos, incluyendo:

- Identificador del control.
- Descripción del incumplimiento.
- Configuración actual del router.
- Recomendación de seguridad.
- Justificación de la recomendación.

**Nota:** Los resultados no se completarán hasta disponer del informe real de auditoría.

## 8. Evidencias

Se incluirán las siguientes evidencias:

1. Instalación de la herramienta ONYX.
2. Conectividad SSH entre Ubuntu Server y R1.
3. Ejecución de la auditoría inicial.
4. Resultados de los controles evaluados.
5. Informe HTML generado por la herramienta.
6. Capturas de los hallazgos identificados.

## 9. Estructura del repositorio

```text
Analisis-CIS-Router/
│
├── README.md
│
├── informes/
│   └── auditoria_inicial/
│       └── informe_CIS_R1.html
│
├── evidencias/
│   ├── 01_instalacion_onyx.png
│   ├── 02_conexion_ssh_R1.png
│   ├── 03_ejecucion_auditoria.png
│   ├── 04_resultados_auditoria.png
│   └── 05_hallazgos_CIS.png
│
├── configuraciones/
│   └── running-config_R1.txt
│
└── documentacion/
    └── hallazgos_y_recomendaciones.md
```

## 10. Conclusión

La evaluación mediante CIS Benchmark permite conocer el estado inicial de seguridad del router Cisco e identificar configuraciones que pueden representar riesgos para la infraestructura de red.

El informe inicial constituye la referencia para futuras actividades de hardening, permitiendo establecer qué controles requieren atención y justificar las medidas de seguridad que se implementen posteriormente.

La finalidad es mejorar la seguridad del dispositivo, fortalecer su administración y reducir la superficie de exposición de la infraestructura de red.

---

**Proyecto académico – ITLA**

Laboratorio de Seguridad de Infraestructura de Redes.

**Dispositivo auditado:** Cisco R1 – 10.23.13.1.
