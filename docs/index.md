# Portal de Procedimientos Operativos - Obercom

Bienvenido al centro de documentación oficial. Navega a través de la red de procesos para acceder a cada documento estandarizado.

<div class="mermaid">
graph TD
    %% Estilos Neón / Fondo Oscuro
    classDef area fill:#0d1117,stroke:#00f3ff,stroke-width:3px,color:#00f3ff,font-weight:bold;
    classDef activo fill:#0d1117,stroke:#39ff14,stroke-width:2px,color:#39ff14,font-weight:bold;
    classDef desarrollo fill:#0d1117,stroke:#ff007f,stroke-width:2px,color:#ff007f;

    %% Nivel 1: Área Principal
    SL[<b>SUMINISTROS Y LOGÍSTICA</b>]:::area

    %% Nivel 2: Procedimientos VIGENTES (Alineación Horizontal)
    subgraph VIGENTES ["Procedimientos Activos"]
        direction LR
        PEDS[PR-PEDS-001<br>Pedidos Sucursales]:::activo
        PEDT[PR-PEDT-001<br>Pedidos Técnicos]:::activo
        REC[PR-REC-001<br>Recupero Equipos]:::activo
        COM[PR-COM-001<br>Compras]:::activo
    end

    %% Nivel 3: Procedimientos EN DESARROLLO
    subgraph FUTUROS ["En Desarrollo / Próximos"]
        direction LR
        HER[PR-HER-001<br>Herramientas]:::desarrollo
        AUDS[PR-AUDS-001<br>Auditoría Móviles]:::desarrollo
        SCR[PR-SCR-001<br>Disposición Final]:::desarrollo
    end

    %% Jerarquía Principal (Conexiones de Cabecera)
    SL ==> PEDS
    SL ==> PEDT
    SL ==> REC
    SL ==> COM
    SL -.- FUTUROS

    %% Interconexiones Operativas entre Procesos
    PEDT -.->|Falta Stock| COM
    PEDT -.->|Equipo Fallado| REC
    REC -.->|Baja Definitiva| COM

    %% Hipervínculos a Archivos
    click PEDS "suministros-logistica/PR-PEDS-001/"
    click PEDT "suministros-logistica/PR-PEDT-001/"
    click REC "suministros-logistica/PR-REC-001/"
    click COM "suministros-logistica/PR-COM-001/"
    click HER "suministros-logistica/PR-HER-001/"
    click AUDS "suministros-logistica/PR-AUDS-001/"
    click SCR "suministros-logistica/PR-SCR-001/"
</div>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({
    startOnLoad: true,
    theme: 'dark',
    flowchart: {
      curve: 'linear',
      nodeSpacing: 25,
      rankSpacing: 45
    }
  });
</script>

---

**Áreas Operativas**
* **Suministros y Logística:** Gestión de compras, inventario de móviles, abastecimiento a sucursales y recupero de hardware.
