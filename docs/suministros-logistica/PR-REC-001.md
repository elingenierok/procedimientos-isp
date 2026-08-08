# Procedimiento de Retiro y Recupero de Equipos (PR-REC-001)

**Norma ISO 9001:2015 - Cláusula 8.4** | **Estado:** Borrador de Trabajo | **Versión:** 0.1[cite: 1]

---

## 1. Objetivo y Alcance

**Objetivo:** Estandarizar y controlar la recepción, diagnóstico técnico, acondicionamiento y actualización sistémica de los equipos de telecomunicaciones recuperados (ONUs, routers), garantizando la exactitud entre el inventario físico y los sistemas de gestión[cite: 1].

* **Qué HACE:** Recepción física de equipos devueltos por técnicos, inspección/limpieza/desinfección, actualización de firmware (flasheo) y reseteo, verificación en sistemas (SGR / Smart OLT) y reingreso al stock operativo o descarte[cite: 1].
* **Qué NO HACE:** Contacto ni coordinación comercial con el cliente (Call Center), retiro físico en domicilio (Técnicos de Campo), ni cierres contables de cuentas (Administración)[cite: 1].

---

## 2. Matriz RACI

| Paso | Descripción | Responsable (R) | Aprueba (A) | Consultado (C) | Informado (I) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Recepción física** | Recepción en depósito de los equipos devueltos por técnicos o ventanilla[cite: 1]. | TEC / CAT | MNT | - | - |
| **2. Desvinculación en sistema** | Desvinculación en Smart OLT y SGR. Pase a "Almacén Devoluciones"[cite: 1]. | MNT | MNT | - | - |
| **3. Triaje y diagnóstico** | Clasificación visual y prueba funcional (encendido/puertos)[cite: 1]. | MNT | MNT | TEC | - |
| **4. Reacondicionamiento** | Limpieza, desinfección y reseteo a valores de fábrica[cite: 1]. | MNT | MNT | - | - |
| **5. Ingreso a Almacén Principal** | Transferencia física y sistémica de equipos viables para reuso[cite: 1]. | MNT | MNT | - | - |
| **6. Traspaso a Descarte** | Registro y traslado físico de unidades defectuosas u obsoletas[cite: 1]. | MNT | MNT | - | - |

---

## 3. Gestión de Excepciones

!!! warning "Inconsistencia de Serial / MAC en Sistema"
    El serial no coincide con la orden o figura asignado a cliente. MNT notifica a CAT para regularizar el traspaso sistémico. Si el equipo no existe en base de datos, se da de alta manualmente en SGR[cite: 1].

!!! failure "Etiqueta o Serial Ilegible"
    MNT conecta el equipo por interfaz lógica (Ethernet/consola) para obtener la MAC/serial interna. Si no responde, se deriva directamente a Descarte[cite: 1].

!!! note "Faltante de Fuente de Alimentación"
    MNT aprueba la viabilidad del equipo principal y solicita la asignación de un transformador compatible desde el stock de repuestos en SGR[cite: 1].

!!! danger "Daño Físico Severo o Deterioro Irrecuperable"
    Unidades con componentes quemados, señales de humedad o roturas irrecuperables se rechazan para reacondicionamiento y se transfieren a "Almacén Descarte"[cite: 1].

---

## 4. Indicadores de Gestión (KPIs)

* **Cantidad de Equipos Recuperados (CER):** Volumen total ingresado en el período[cite: 1].
* **Cantidad de Equipos Fuera de Circulación (CEFC):** Unidades transferidas a Descarte (Meta: $< 15\%$)[cite: 1].
* **Porcentaje de Recupero Viable (PRV):** (Equipos puestos en circulación / Equipos viables recibidos) $\times 100$ (Meta: $\ge 90\%$)[cite: 1].
* **Valor Efectivo Recuperado (VER):** Impacto económico ahorrado por reuso de equipos[cite: 1].
