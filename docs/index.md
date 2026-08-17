# 🏢 Área de Suministros y Logística (S&L)

!!! abstract "Nuestra Razón de Ser"
    El área de **Suministros y Logística (S&L)** de Obercom tiene como misión principal garantizar la continuidad operativa y sostener la expansión de nuestra red de telecomunicaciones al menor **Costo Total de Propiedad (TCO)**. 
    
    Somos el motor logístico de la empresa: aseguramos que nuestros equipos de campo y sucursales siempre tengan los materiales que necesitan, en el momento y lugar correctos, optimizando los recursos y protegiendo el capital de la organización.

---

## 🗺️ Mapa Operativo y Estructura de Roles

A continuación, se detalla la estructura organizativa del área, liderada por la Gerencia y dividida en tres grandes verticales operativas.

```mermaid
graph TD
    classDef gerencia fill:#0d1117,stroke:#ffbf00,stroke-width:2px,color:#ffbf00,font-weight:bold;
    classDef area fill:#161b22,stroke:#00f3ff,stroke-width:2px,color:#00f3ff,font-weight:bold;
    classDef rol fill:#1f2428,stroke:#39ff14,stroke-width:1px,color:#c9d1d9,border-radius:5px;

    %% Liderazgo
    GER["<b>👑 Gerente de Suministros y Logística</b><br>Estrategia, Presupuesto (TCO) y KPIs"]:::gerencia

    %% Sub-Vertical 1
    subgraph SV1 ["🛒 1. Compras y Suministros"]
        direction TB
        R_COMP["<b>👔 Encargado de Compras</b><br>Compras Estratégicas y Proveedores"]:::rol
        R_ASIS["<b>🗂️ Asistente de Suministros</b><br>Compras Operativas y Soporte"]:::rol
    end

    %% Sub-Vertical 2
    subgraph SV2 ["📦 2. Depósito y Equipamiento"]
        direction TB
        R_MANT["<b>💻 Mantenimiento de Equipamiento</b><br>Flasheo ONUs y Control Stock"]:::rol
        R_SUC["<b>👶 Asistente de Sucursal</b><br>Nexo Operativo y Stock Local"]:::rol
        R_PAS["<b>🤓 Pasante (Trainee)</b><br>Apoyo QA y Logística Inversa"]:::rol
    end

    %% Sub-Vertical 3
    subgraph SV3 ["🚚 3. Flota Vehicular"]
        direction TB
        R_FLOTA["<b>🚛 Encargado de Flota</b><br>Mantenimiento, VTV, Combustible"]:::rol
    end

    %% Conexiones Jerárquicas
    GER ==> SV1
    GER ==> SV2
    GER ==> SV3

    %% Conexiones Operativas Internas
    R_COMP -.->|Delega tareas| R_ASIS
    R_MANT -.->|Abastece / Audita| R_SUC
