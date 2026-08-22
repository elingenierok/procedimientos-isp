<button onclick="window.print()" class="md-button md-button--primary btn-print" style="margin-bottom: 15px;">
  🖨️ Imprimir / Descargar PDF
</button>

# PROCEDIMIENTO DE COORDINACIÓN LOGÍSTICA Y TRASLADOS (PR-CLOG-001)

**Norma ISO 9001:2015 - Cláusulas 8.1 y 8.5.4** | **Estado:** Borrador | **Versión:** 0.1

---

## 1. Objetivo y Alcance

**Objetivo:** Estandarizar la planificación, consolidación y ejecución de viajes, envíos a sucursales y retiros locales de Obercom, optimizando el uso de la flota habilitada y garantizando la preservación de los materiales e insumos durante el transporte.

* **Qué HACE:**
    * Programación y consolidación de itinerarios para viajes periódicos o puntuales a sucursales.
    * Coordinación de salidas para retiros de materiales en proveedores locales a requerimiento de Compras o Administración.
    * Selección del móvil adecuado en función del volumen de carga, considerando únicamente unidades con estado "Apto para Operar".
    * Supervisión del acondicionamiento, sujeción y trazabilidad documental de los bienes trasladados hasta su recepción en destino.
* **Qué NO HACE:**
    * Mantenimiento mecánico, reparación, control de VTV, seguros o habilitación legal de los vehículos (corresponde a Mantenimiento de Flota).
    * Ejecución del checklist de estado mecánico/físico de la unidad (corresponde al Chofer/Técnico y Mantenimiento de Flota).
    * Negociación comercial o gestión de compras con proveedores locales.

---

## 2. Matriz RACI y Descripción de Pasos

| Paso | Actividad / Descripción | Responsable (R) | Aprueba (A) | Consultado (C) | Informado (I) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Requerimiento y Consolidación** | Recepción de necesidades de traslado (sucursales/compras) y agrupamiento por rutas/fechas. | CLOG | GSL | ADM / SUC | - |
| **2. Asignación de Unidad "Apta"** | Selección del vehículo adecuado verificando en matriz el estado "Apto para Operar" emitido por Flota. | CLOG | GFL | GFL | CHO |
| **3. Programación de Ruta** | Definición de horarios de salida/llegada, chofer asignado y hoja de ruta consolidada. | CLOG | GSL | CHO | SUC |
| **4. Control de Carga y Preservación** | Verificación del embalaje, estibaje correcto y cotejo físico contra remito de salida (Oberstock/SGR). | CLOG | CLOG | Depósito | SUC |
| **5. Monitoreo de Trayecto** | Seguimiento del viaje a sucursal/proveedor y gestión de novedades operativas en ruta. | CLOG | GSL | CHO | SUC |
| **6. Cierre y Recepción Conforme** | Confirmación de entrega en destino, firma de remito de recepción y liberación del móvil. | SUC | CLOG | CHO | GFL |

*Referencias de Roles:* **CLOG:** Coordinador Logístico | **GFL:** Gestor de Flota Vehicular | **GSL:** Gerente de Suministros y Logística | **CHO:** Chofer / Técnico Designado | **SUC:** Responsable de Sucursal | **ADM:** Administración / Compras

---

## 3. Reglas Operativas del Proceso

* **[Regla 1 / Ventana Horaria de Programación]:** Todas las solicitudes de envío o viajes a sucursales deben registrarse con un mínimo de 24 horas de anticipación. Solicitudes imprevistas solo se procesarán como "Emergencia Operativa" con autorización del Gerente de S&L.
* **[Regla 2 / Uso Exclusivo de Unidades Aptas]:** El Coordinador Logístico únicamente podrá programar viajes en vehículos que figuren con estatus verde ("Apto para Operar") en el tablero de Mantenimiento de Flota. Queda prohibida la asignación de móviles "En Taller" o con documentación vencida.
* **[Regla 3 / Criterio de Consolidación de Carga]:** Ningún viaje interurbano saldrá a sucursales con una capacidad de carga inferior al 60%, salvo que transporte un insumo crítico para el restablecimiento del servicio de red.
* **[Regla 4 / Trazabilidad Sistémica Obligatoria]:** Todo material, equipo o herramienta que suba a un vehículo para traslado debe contar con su correspondiente Remito de Transferencia generado en el sistema (Oberstock/SGR). Queda prohibido el traslado de materiales sin respaldo sistémico.
## 4. Diagrama de Flujo

```mermaid
graph TD;
    A[Recepción de Solicitud de Traslado / Envíos] --> B[Consolidación de Carga y Definición de Ruta];
    B --> C{¿Móvil Asignado está "APTO" en Flota?};
    C -- No --> D[Solicitar Reasignación / Habilitación a Gestor de Flota];
    D --> C;
    C -- Sí --> E[Carga de Materiales y Emisión de Remito Sistémico];
    E --> F[Ejecución del Viaje / Traslado a Destino];
    F --> G[Entrega y Firma Conforme de Remito en Sucursal];
    G --> H[Cierre de Viaje y Liberación de Unidad];
```
---

## 5. Gestión de Excepciones

!!! warning "Indisponibilidad de Móvil Apto o Indisponibilidad de Carga"
    **Escenario:** Se requiere un envío urgente a sucursal o retiro local, pero no existen vehículos en estatus "Apto para Operar" o la capacidad del móvil disponible es insuficiente.  
    **Acción Correctiva:** El Coordinador Logístico escala la prioridad al Gerente de S&L para evaluar la contratación de un flete/transporte externo contratado o la reprogramación de envíos no críticos, evitando en todo momento el uso de unidades no habilitadas por Flota.

!!! failure "Faltante o Insumo Dañado Durante el Traslado"
    **Escenario:** El material o equipo llega a destino en la sucursal con faltantes respecto al remito o con daños físicos por mala sujeción en el viaje.  
    **Acción Correctiva:** La sucursal receptora detiene la conformidad del remito en sistema, toma registro fotográfico y emite una Salida No Conforme (SNC). El Coordinador Logístico investiga la causa raíz (embalaje, estibaje o chofer) y coordina la reposición inmediata del stock afectado.

---

## 6. Indicadores de Gestión (KPIs)

* **Cumplimiento del Cronograma de Envíos (CCE):**
    * **Fórmula:** `(Viajes y Envíos Entregados en Tiempo y Forma / Total de Viajes Programados) * 100`
    * **Meta:** `≥ 95%`

* **Ocupación Eficiente de Carga (OEC):**
    * **Fórmula:** `(Promedio de Carga Útil Utilizada en Viajes Interurbanos / Capacidad Máxima Vehicular) * 100`
    * **Meta:** `≥ 75%`

* **Tasa de Preservación de Insumos en Tránsito (TPIT):**
    * **Fórmula:** `100 - [(Valor Monetario de Insumos Dañados o Extraviados en Tránsito / Valor Total Transportado) * 100]`
    * **Meta:** `100%`

---

## 7. Historial de Control de Cambios

| Versión | Fecha | Descripción de la Modificación | Autor |
| :--- | :--- | :--- | :--- |
| 0.1 | 22/08/2026 | Confección del borrador inicial para desvinculación de Logística | Consultoría ISO 9001 / S&L |
