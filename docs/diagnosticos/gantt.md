```mermaid
graph LR
    subgraph ANTES ["ESCENARIO ANTES (Tiempo Total: 16:42 min)"]
        direction LR
        A1["A. Recepción<br>00:51 min"] --> A2["B. SmartOLT / SGR<br>08:19 min (CUELLO BOTELLA)"]
        A2 --> A3["C. Test WiFi<br>00:44 min"]
        A3 --> A4["D. Acondicionamiento<br>08:23 min"]
    end

    subgraph DESPUES ["ESCENARIO DESPUÉS (Tiempo Total: 11:43 min - 30% AHORRO)"]
        direction LR
        B1["A. Recepción<br>00:51 min"] --> B2["B. SmartOLT / NOC<br>03:20 min (OPTIMIZADO)"]
        B2 --> B3["C. Test WiFi<br>00:44 min"]
        B3 --> B4["D. Acondicionamiento<br>08:23 min"]
    end

    style A2 fill:#e74c3c,stroke:#922b21,color:#ffffff,stroke-width:2px
    style B2 fill:#27ae60,stroke:#1e8449,color:#ffffff,stroke-width:2px
