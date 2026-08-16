# Biblioteca de Documentación Operativa - Obercom

<div class="mermaid">
graph LR
    classDef area fill:#0d1117,stroke:#00f3ff,stroke-width:3px,color:#00f3ff,font-weight:bold;
    classDef activo fill:#0d1117,stroke:#39ff14,stroke-width:2px,color:#39ff14,font-weight:bold;

    %% Bloques Raíz (Áreas)
    SL[<b>SUMINISTROS Y LOGÍSTICA</b>]:::area
    DG[<b>DIAGNÓSTICOS TÉCNICOS</b>]:::area

    %% Subgráfico S&L
    subgraph S_L ["🟢 Suministros y Logística"]
        direction TB
        COM[PR-COM-001 Compras]:::activo
        PEDS[PR-PEDS-001 Pedidos Sucursales]:::activo
        PEDT[PR-PEDT-001 Pedidos Técnicos]:::activo
        REC[PR-REC-001 Recupero de Equipos]:::activo
    end

    %% Subgráfico Diagnósticos
    subgraph DIAG ["🔍 Diagnósticos"]
        direction TB
        DGEQU[DG-EQU-001 Diagnóstico de Equipos]:::activo
    end

    %% Conexiones
    SL ==> S_L
    DG ==> DIAG

    %% Enlace cruzado (Ejemplo: Recupero deriva a Diagnóstico)
    REC -.->|Evaluar Fallas| DGEQU

    %% Links
    click COM "suministros-logistica/PR-COM-001/"
    click PEDS "suministros-logistica/PR-PEDS-001/"
    click PEDT "suministros-logistica/PR-PEDT-001/"
    click REC "suministros-logistica/PR-REC-001/"
    click DGEQU "diagnosticos/DG-EQU-001/"
</div>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({ startOnLoad: true, theme: 'dark', flowchart: { curve: 'linear' } });
</script>
