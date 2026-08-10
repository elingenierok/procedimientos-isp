# Procedimiento de Preparado de Pedidos (PR-PEDT-001)

**Norma ISO 9001:2015 - Cláusula 8.5** | **Estado:** Borrador de Trabajo | **Versión:** 0.1

---

## 1. Objetivo y Alcance

**Objetivo:** Estandarizar la recepción, auditoría de stock, armado y asignación diferida de equipos y materiales solicitados por los técnicos de calle, garantizando la trazabilidad de seriales y la transferencia sistémica entre el Almacén Principal y los Almacenes Móviles.

* **Qué HACE:**
    * Evaluación de solicitudes en Oberstock contra el stock real del técnico en SGR.
    * Acopio físico y escaneo unitario obligatorio de MAC/SN de los equipos.
    * Generación de transferencia en SGR e inserción de la ID de Transferencia en Oberstock.
    * Acopio diferido en lockers rotulados, registro final y notificación al técnico.
* **Qué NO HACE:**
    * Entrega presencial mano a mano fuera del sistema de lockers (salvo contingencia técnica declarada).
    * Despacho de solicitudes fuera del régimen estricto sin autorización explícita de supervisión.
    * Asignación de órdenes de trabajo de campo o ruteo.

---

## 2. Matriz RACI y Descripción de Pasos

| Paso | Actividad / Descripción | Responsable (R) | Aprueba (A) | Consultado (C) | Informado (I) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Emisión del Pedido** | Ingreso de la Orden de Pedido en Oberstock respetando la ventana horaria según el turno del técnico. | TEC | SIS/SUP | - | ALM |
| **2. Evaluación de Stock** | Revisión de lo solicitado en Oberstock y consulta del stock actual del TEC en SGR para validar topes e inventario. | ALM | ALM | SGR | TEC |
| **3. Acopio y Escaneo** | Picking físico de materiales y escaneo unitario obligatorio de MAC/SN de equipos. | ALM | ALM | - | - |
| **4. Transferencia SGR** | Generación de la transferencia en SGR (Almacén Principal -> Almacén Móvil TEC) y registro de ID en Oberstock. | ALM | ALM | - | - |
| **5. Staging y Cierre** | Depósito en locker rotulado, registro del N° de Locker en Oberstock, cierre de la orden y notificación. | ALM | ALM | - | TEC |

*Referencias de Roles:* **TEC:** Técnico de Calle | **ALM:** Personal de Almacén / Logística | **SUP:** Supervisor de Operaciones | **SIS:** Sistema Oberstock/SGR

---

## 3. Reglas Operativas del Proceso

* **Régimen Estricto de Pedido por Horario:** 
  * *Turno 7:30 AM:* Generan su pedido en Oberstock al finalizar la jornada del día hábil anterior. 
  * *Turno 10:00 AM:* Generan su pedido al finalizar la jornada previa. ALM procesa y arma sus pedidos en la franja de 7:30 AM a 10:00 AM.
* **Criterio de Evaluación de Stock:** ALM rechazará o ajustará cantidades si el SGR indica que el TEC ya posee stock suficiente en su móvil para la jornada, o si hay desabastecimiento general.
* **Trazabilidad Unitaria (MAC/SN):** La lectura por scanner de cada MAC/SN es un requisito excluyente. Permite que el equipo quede imputado al móvil del técnico para su posterior descuento automático al instalarlo.
* **Seguridad de Lockers:** El depósito de los materiales se hace en el locker individual asignado, cuyo acceso (candado con llave o código) es responsabilidad exclusiva del TEC asignado.

---

## 4. Diagrama de Flujo

![Diagrama de Flujo - Preparado de Pedidos](../img/FLUJO-PEDT.png)

```mermaid
graph TD;
    A[TEC emite pedido en Oberstock] --> B{¿Dentro de horario?};
    B -- No --> C[Requiere Aprobación SUP];
    C -- Rechazado --> Z[Fin - Pedido Cancelado];
    B -- Sí --> D[ALM evalúa Stock SGR];
    C -- Aprobado --> D;
    D --> E{¿Stock en Móvil OK?};
    E -- Excede Tope --> F[Ajuste de Cantidad parcial];
    E -- OK --> G[Acopio y Escaneo MAC/SN];
    F --> G;
    G --> H[Transferencia SGR a Móvil TEC];
    H --> I[Depósito en Locker y Cierre Oberstock];
    I --> J[Notificación al TEC];
