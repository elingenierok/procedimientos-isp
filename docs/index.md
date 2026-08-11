# Portal de Procedimientos Operativos - Obercom

Bienvenido al centro de documentación oficial. Navega a través de la red de procesos para acceder a cada documento estandarizado.

<div class="mermaid">
graph LR
    %% Estilos Neón / Fondo Oscuro
    classDef area fill:#0d1117,stroke:#00f3ff,stroke-width:3px,color:#00f3ff,font-weight:bold;
    classDef activo fill:#0d1117,stroke:#39ff14,stroke-width:2px,color:#39ff14,font-weight:bold;
    classDef desarrollo fill:#0d1117,stroke:#ff007f,stroke-width:2px,color:#ff007f;

    %% Nodo Raíz (Izquierda)
    SL[<b>SUMINISTROS Y LOGÍSTICA</b>]:::area

    %% Columna 1: Procedimientos Activos
    subgraph ACT ["🟢 PROCEDIMIENTOS ACTIVOS"]
        direction TB
        COM[PR-COM-001 Compras]:::activo
        PEDS[PR-PEDS-001 Pedidos Sucursales]:::activo
        PEDT[PR-PEDT-001 Pedidos Técnicos]:::activo
        REC[PR-REC-001 Recupero de Equipos]:::activo

        COM ~~~ PEDS ~~~ PEDT ~~~ REC
    end

    %% Columna 2: Procedimientos En Desarrollo
    subgraph DES ["🔴 EN DESARROLLO"]
        direction TB
        AUDS[PR-AUDS-001 Auditoría de Móviles]:::desarrollo
        HER[PR-HER-001 Reposición de Herramientas]:::desarrollo
        SCR[PR-SCR-001 Disposición Final / Scrap]:::desarrollo

        AUDS ~~~ HER ~~~ SCR
    end

    %% Conexiones Principales (Distribución Horizontal)
    SL ==> ACT
    SL -.-> DES

    %% Links de Navegación
    click COM "suministros-logistica/PR-COM-001/"
    click PEDS "suministros-logistica/PR-PEDS-001/"
    click PEDT "suministros-logistica/PR-PEDT-001/"
    click REC "suministros-logistica/PR-REC-001/"
    click AUDS "suministros-logistica/PR-AUDS-001/"
    click HER "suministros-logistica/PR-HER-001/"
    click SCR "suministros-logistica/PR-SCR-001/"
</div>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({
    startOnLoad: true,
    theme: 'dark',
    flowchart: {
      curve: 'linear',
      nodeSpacing: 15,
      rankSpacing: 50
    }
  });
</script>

---

**Áreas Operativas**
* **Suministros y Logística:** Gestión de compras, inventario de móviles, abastecimiento a sucursales y recupero de hardware.
