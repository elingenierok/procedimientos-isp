# Portal de Procedimientos Operativos - Obercom

Bienvenido al centro de documentación oficial. Navega a través de la red jerárquica de procesos para acceder a cada documento estandarizado.

```mermaid
graph TD
    %% Estilos Neón para Fondo Oscuro
    classDef area fill:#0d1117,stroke:#00f3ff,stroke-width:3px,color:#00f3ff,font-weight:bold;
    classDef proceso fill:#0d1117,stroke:#39ff14,stroke-width:2px,color:#39ff14,font-weight:bold;
    classDef aislado fill:#0d1117,stroke:#ff007f,stroke-width:2px,color:#ff007f;

    %% Nivel 1: Área Principal
    SL[SUMINISTROS Y LOGÍSTICA]:::area

    %% Nivel 2: Procesos Descendientes
    PEDT[PR-PEDT-001<br>Pedidos Técnicos]:::proceso
    REC[PR-REC-001<br>Recupero de Equipos]:::proceso
    ALM[PR-ALM-001<br>Inventario Físico]:::aislado

    %% Nivel 3: Aprovisionamiento y Compras
    COM[PR-COM-001<br>Compras]:::proceso

    %% Jerarquía Principal (Líneas de Cascada)
    SL ==> PEDT
    SL ==> REC
    SL ==> ALM

    %% Enredaderas Cruzadas (Relaciones de Interconexión)
    PEDT -.->|Falta de Stock| COM
    PEDT -.->|Equipo Fallado| REC
    REC -.->|Baja Definitiva| COM

    %% Hipervínculos a Documentos
    click PEDT "suministros-logistica/PR-PEDT-001/"
    click COM "suministros-logistica/PR-COM-001/"
    click REC "suministros-logistica/PR-REC-001/"
```

---

**Áreas Operativas**
* **Suministros y Logística:** Gestión de compras, inventario de móviles y recupero de hardware.
