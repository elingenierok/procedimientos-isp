# Mapa Operativo - Suministros y Logística

<div class="mermaid">
graph LR
    classDef area fill:#0d1117,stroke:#00f3ff,stroke-width:3px,color:#00f3ff,font-weight:bold;
    classDef subvertical fill:#161b22,stroke:#39ff14,stroke-width:2px,color:#39ff14,font-weight:bold;
    classDef tarea fill:#161b22,stroke:#8b949e,stroke-width:1px,color:#c9d1d9,border-radius:5px;

    %% Bloque Raíz
    SL[<b>SUMINISTROS Y LOGÍSTICA</b>]:::area

    %% Sub-Vertical 1
    subgraph SV1 ["🛒 Compras y Suministros"]
        direction TB
        C1[Gestión de Proveedores]:::tarea
        C2[Compras Estratégicas]:::tarea
        C3[Compras Operativas]:::tarea
    end

    %% Sub-Vertical 2
    subgraph SV2 ["📦 Depósito y Equipamiento"]
        direction TB
        D1[Control SGR / SmartOLT]:::tarea
        D2[Reacondicionamiento ONUs]:::tarea
        D3[Despacho a Técnicos]:::tarea
        D4[Auditoría a Sucursales]:::tarea
    end

    %% Sub-Vertical 3
    subgraph SV3 ["🚚 Flota Vehicular"]
        direction TB
        F1[Mantenimiento Preventivo]:::tarea
        F2[Control Legal VTV/Seguros]:::tarea
        F3[Checklist Diario y Consumo]:::tarea
    end

    %% Conexiones
    SL ==> SV1
    SL ==> SV2
    SL ==> SV3
    
    %% Relaciones operativas (Ejemplo: Compras nutre al depósito)
    SV1 -.->|Ingreso de Mercadería| SV2
</div>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({ startOnLoad: true, theme: 'dark', flowchart: { curve: 'basis' } });
</script>
