# DIAGNÓSTICO OPERATIVO: OPTIMIZACIÓN Y AUDITORÍA EN BANCO DE PRUEBAS (DIAG-ONU-001)

**Área:** Suministros y Logística - Mantenimiento de Equipos | **Familia de Equipos:** ONUs GPON CATV (ZTE F6600R) | **Estado:** Aprobado / Diagnóstico Final | **Versión:** 1.0

---

## 1. Marco Introductorio y Requisitos Previos

**Objetivo:** Diagnosticar formalmente la operación de prueba técnica, verificación física y clasificación en laboratorio de las ONUs CATV. El propósito es identificar cuellos de botella sistémicos versus ineficiencias del factor humano, estableciendo una línea base real de tiempos para la construcción del Procedimiento Operativo Estandarizado (POE).

* **Resumen Ejecutivo del Trabajo Realizado:**
    * **Metodología:** Relevamiento integral de 2.5 días bajo la modalidad de trabajo auditado en pareja (*Benchmarking Inter-sucursales*).
    * **Desglose de Variables:** Discriminación entre la eficiencia del técnico y la latencia propia de las plataformas informáticas de gestión.
    * **Resultados Obtenidos:** Resolución de falla de parametrización en SmartOLT junto al área de NOC, reduciendo el aprovisionamiento lógico de **08:19 min** a **03:20 min**.
    * **Impacto Operativo:** Reducción del ciclo total de **16:42 min** a **11:43 min** (-30%), incrementando la capacidad diaria por técnico en **+46.4%** (de 28 a 41 equipos/día).

* **Insumos y Herramientas Obligatorias:**
    * **Banco de Pruebas:** Fuente de alimentación 12V / 1.5A, lápiz óptico de limpieza SC/APC, cable coaxial RG6, patch cords de fibra.
    * **Sistemas / Software:** Plataforma SmartOLT, Sistema de Gestión Real (SGR), Sistema ISP, gestión TR069.
    * **EPP y Seguridad:** Protecciones ESD (manta/pulsera antiestática) y lentes de seguridad para manipulación de fibra óptica.

---

## 2. Desarrollo Técnico del Flujo Operativo

### 2.1. Escenario Inicial ("Antes" - Con Fricción Sistémica)
En esta fase, la producción se encontraba condicionada por bloqueos en las plataformas informáticas, generando esperas pasivas en el operario.

* **Bloque A - Recepción y Conexión Física (`00:51 min`):** Conexión eléctrica (12V/1.5A), limpieza de conector SC/APC, enrosque de coaxial RG6 y escaneo en SGR para ubicación en almacén temporal.
* **Bloque B - Carga y Aprovisionamiento Lógico (`08:19 min` - CUELLO DE BOTELLA):** Carga de datos en ISP, reemplazo de ONU en SmartOLT, desregistración simultánea en SGR y depuración de interfaz PPP 1.1. **Causa de la falla:** Comandos bloqueados en SmartOLT y SGR (plataformas "girando" en espera de respuesta de la OLT física).
* **Bloque C - Pruebas Operativas y Etiquetado (`00:44 min`):** Lectura de potencia óptica, configuración de SSID/Password local (2.4/5GHz), test de velocidad inalámbrico, impresión de etiqueta térmica y transferencia simplificada en sistema.
* **Bloque D - Acondicionamiento y Cierre Administrativo (`08:23 min`):** Registro de cambio de condición (Artículo Usado/Nuevo) en SGR, limpieza profunda del chasis, inspección física y empaquetado en bolsa transparente con transformador.
* **Tiempo Total Inicial:** **16:42 minutos por unidad** (~28 equipos/día).

### 2.2. Escenario Optimizado ("Después" - Con Intervención NOC)
Se articuló una solución técnica con el área de NOC para eliminar las colas de espera en TR069 y corregir la ejecución de comandos en SmartOLT, eliminando la latencia en el banco de pruebas.

* **Explicación de la Mejora:** Se sustituyó el procedimiento manual de espera pasiva por un protocolo de alta directa y depuración de la interfaz PPP 1.1.
* **Nuevo Bloque B Reemplazante (`03:20 min`):** Carga fluida de datos en ISP, ejecución inmediata de reemplazo en SmartOLT, resincronización lógica directa y desvinculación limpia en SGR sin bucles de red.
* **Tiempo Total Optimizado:** **11:43 minutos por unidad** (~41 equipos/día). *(Los Bloques A, C y D se mantuvieron estables en sus tiempos base)*.

### 2.3. Diagramas de Flujo Comparativos

```mermaid
graph TD
    subgraph ANTES ["Escenario Inicial (16:42 min)"]
        A1[Bloque A: Conexión <br/> 00:51 min] --> A2[Bloque B: SmartOLT/SGR <br/> 08:19 min - CUELLO BOTELLA]
        A2 --> A3[Bloque C: Test WiFi <br/> 00:44 min]
        A3 --> A4[Bloque D: Acondicionado <br/> 08:23 min]
    end

    subgraph DESPUES ["Escenario Optimizado (11:43 min)"]
        B1[Bloque A: Conexión <br/> 00:51 min] --> B2[Bloque B: SmartOLT/NOC <br/> 03:20 min - OPTIMIZADO]
        B2 --> B3[Bloque C: Test WiFi <br/> 00:44 min]
        B3 --> B4[Bloque D: Acondicionado <br/> 08:23 min]
    end
```

## 3. Matriz Comparativa de Tiempos y Capacidad

| Etapa / Bloque del Proceso | Escenario Inicial ("Antes") | Escenario Optimizado ("Después") | Variación Absoluta | Variación Porcentual |
| :--- | :---: | :---: | :---: | :---: |
| **Bloque A:** Recepción y Conexión Física | 00:51 min | 00:51 min | 00:00 min | 0.0% |
| **Bloque B:** Carga y Aprovisionamiento Lógico | **08:19 min** | **03:20 min** | **-04:59 min** | **-60.0%** |
| **Bloque C:** Pruebas Operativas y Etiquetado | 00:44 min | 00:44 min | 00:00 min | 0.0% |
| **Bloque D:** Acondicionamiento Físico y GR | 08:23 min | 08:23 min | 00:00 min | 0.0% |
| **TIEMPO TOTAL POR UNIDAD** | **16:42 min** | **11:43 min** | **-04:59 min** | **-29.8%** |
| **CAPACIDAD DIARIA TEÓRICA (Jornada 8h)** | **28 equipos / día** | **41 equipos / día** | **+13 equipos** | **+46.4%** |

### Comparativo Visual de Tiempos por Etapa

| Escenario | Bloque A (Conexión) | Bloque B (SmartOLT / SGR) | Bloque C (WiFi) | Bloque D (Acondicionado) | Tiempo Total |
| :--- | :---: | :--- | :---: | :--- | :---: |
| **ANTES** | 🟦 0:51 | 🟥🟥🟥🟥🟥🟥🟥🟥 **8:19** *(Fricción)* | 🟨 0:44 | 🟩🟩🟩🟩🟩🟩🟩🟩 **8:23** | **16:42 min** |
| **DESPUÉS** | 🟦 0:51 | 🟩🟩🟩 **3:20** *(Optimizado NOC)* | 🟨 0:44 | 🟩🟩🟩🟩🟩🟩🟩🟩 **8:23** | **11:43 min** |

> **Leyenda Visual:**  
> 🟦 *Conexión física* | 🟥 *Cuello de botella sistémico* | 🟩 *Proceso optimizado / Acondicionamiento* | 🟨 *Prueba inalámbrica*

## 4. Diagnóstico de Fricciones: Sistema vs. Factor Humano

!!! failure "Fricción Sistémica (Resuelta)"
    **Diagnóstico:** Se confirmó que la baja producción histórica no respondía únicamente a la actitud del trabajador. Las demoras en la respuesta de las plataformas SmartOLT y SGR llegaban a inflar el tiempo de prueba en hasta un **85% adicional**. Sin la intervención con NOC, el técnico quedaba atado a un bucle de espera sin posibilidad de acelerar el trabajo.

!!! warning "Factor Humano y Fricción Operativa (Bajo Control)"
    **Diagnóstico:** El acompañamiento auditado reveló que realizar cargas administrativas en el sistema SGR en medio de las pruebas ópticas dispersaba la atención del operario. Se ordenó trasladar todo el empaque y registro en SGR al final del ciclo (Bloque D), fijando un estándar de **08:23 min**. Con la plataforma optimizada, cualquier demora superior a los 11:43 min totales pasa a ser atribuible a micro-pausas, desorden en la mesa o uso del celular.

## 5. Conclusiones y Decisiones Estratégicas

* **1. Imposición del SLA Objetivo:** Se fija formalmente como norma de laboratorio un tiempo límite de **11:43 minutos por equipo CATV**. Esta métrica servirá de base para auditar la productividad diaria del personal.
* **2. Protocolo de Escalamiento a NOC:** Queda prohibido que el técnico permanezca esperando la respuesta pasiva del sistema. Si un comando en SmartOLT supera los **45 segundos en bucle**, se debe abrir un ticket inmediato a NOC.
* **3. Respaldo Técnico para RRHH:** El informe proporciona evidencia cuantitativa y objetiva para desestimar excusas operativas sobre las planillas diarias, permitiendo exigir un rendimiento acorde a la nueva capacidad instalada (**41 equipos/día**).
* **4. Transferibilidad a Sucursales y Stock:** Este diagnóstico constituye el insumo principal para redactar el POE definitivo que se extrapolará a las sucursales sin personal exclusivo de prueba, asegurando que los dos almacenes auditados (Principal y Devoluciones) mantengan un registro de stock 100% certero.

## 6. Historial de Control de Cambios

| Versión | Fecha | Descripción de la Modificación | Autor |
| :--- | :--- | :--- | :--- |
| 0.1 | 16/08/2026 | Medición inicial con fricción de sistema (16:42 min total). | Auditoría de Laboratorio |
| 1.0 | 16/08/2026 | Optimización de SmartOLT c/NOC y fijación de SLA (11:43 min total). | Jefatura de Depósito / S&L |
