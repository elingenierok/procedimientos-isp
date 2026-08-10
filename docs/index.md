# Portal de Procedimientos Operativos - Obercom

Bienvenido al centro de documentación oficial. Utiliza el mapa interactivo o el menú lateral para acceder a los procedimientos estandarizados.

**Mapa de Interconexión de Procesos**

```mermaid
graph TD
    %% Estilos de la marca Obercom
    classDef obercom fill:#00205B,stroke:#41B6E6,stroke-width:2px,color:#ffffff;

    %% Definición de Nodos
    COM[PR-COM-001<br>Compras]:::obercom
    PEDT[PR-PEDT-001<br>Pedidos Técnicos]:::obercom
    REC[PR-REC-001<br>Recupero de Equipos]:::obercom

    %% Relaciones entre Procesos
    PEDT -->|Insumos faltantes| COM
    PEDT -->|Equipos devueltos| REC

    %% Hipervínculos a los archivos del portal
    click COM "suministros-logistica/PR-COM-001/" "Ver Procedimiento de Compras"
    click PEDT "suministros-logistica/PR-PEDT-001/" "Ver Pedidos Técnicos"
    click REC "suministros-logistica/PR-REC-001/" "Ver Recupero de Equipos"
```

---

**Áreas Operativas**
* **Suministros y Logística:** Gestión de compras, inventario de móviles y recupero de hardware.
