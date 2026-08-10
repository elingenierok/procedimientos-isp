# Portal de Procedimientos Operativos - Obercom

Bienvenido al centro de documentación oficial. Navega a través de la red jerárquica de procesos para acceder a cada documento estandarizado.

<div class="mermaid">
graph TD
    classDef area fill:#0d1117,stroke:#00f3ff,stroke-width:3px,color:#00f3ff,font-weight:bold;
    classDef proceso fill:#0d1117,stroke:#39ff14,stroke-width:2px,color:#39ff14,font-weight:bold;
    classDef aislado fill:#0d1117,stroke:#ff007f,stroke-width:2px,color:#ff007f;

    SL[SUMINISTROS Y LOGÍSTICA]:::area

    PEDT[PR-PEDT-001<br>Pedidos Técnicos]:::proceso
    REC[PR-REC-001<br>Recupero de Equipos]:::proceso
    PEDT[PR-PEDT-001<br>Pedidos Técnicos]:::proceso

    COM[PR-COM-001<br>Compras]:::proceso

    SL ==> PEDT
    SL ==> REC
    SL ==> PETS

    PEDT -.->|Falta de Stock| COM
    PEDT -.->|Equipo Fallado| REC
    REC -.->|Baja Definitiva| COM
    

    click PEDT "suministros-logistica/PR-PEDT-001/"
    click COM "suministros-logistica/PR-COM-001/"
    click REC "suministros-logistica/PR-REC-001/"
    click REC "suministros-logistica/PR-PETS-001/"
</div>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
  mermaid.initialize({ startOnLoad: true, theme: 'dark' });
</script>

---

**Áreas Operativas**
* **Suministros y Logística:** Gestión de compras, inventario de móviles y recupero de hardware.
