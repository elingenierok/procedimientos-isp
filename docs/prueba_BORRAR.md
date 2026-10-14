<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ficha Operativa - Área de Suministros y Logística (S&L) | Obercom</title>
<style>
  @page {
    size: A4 portrait;
    margin: 8mm;
  }
  @media print {
    body { background: white !important; -webkit-print-color-adjust: exact; print-color-adjust: exact; }
    .no-print { display: none !important; }
    .page-container { box-shadow: none !important; padding: 0 !important; width: 100% !important; margin: 0 !important; }
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }
  
  body {
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    background-color: #f1f5f9;
    color: #0f172a;
    font-size: 8.3pt;
    line-height: 1.3;
    display: flex;
    justify-content: center;
    padding: 15px;
  }

  .page-container {
    background: #ffffff;
    width: 210mm;
    max-width: 100%;
    min-height: 285mm;
    padding: 10mm;
    border-radius: 8px;
    box-shadow: 0 8px 24px rgba(0,0,0,0.08);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .btn-print {
    background: #0284c7;
    color: #ffffff;
    border: none;
    padding: 7px 14px;
    font-size: 8.5pt;
    font-weight: 700;
    border-radius: 5px;
    cursor: pointer;
    margin-bottom: 10px;
    align-self: flex-end;
    box-shadow: 0 2px 4px rgba(2, 132, 199, 0.25);
  }
  .btn-print:hover { background: #0369a1; }

  /* HEADER BANNER */
  .header-banner {
    background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
    color: #ffffff;
    padding: 12px 16px;
    border-radius: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-left: 6px solid #00f3ff;
    margin-bottom: 9px;
  }
  .header-title h1 { font-size: 13.5pt; font-weight: 900; letter-spacing: -0.2px; color: #f8fafc; }
  .header-title p { font-size: 8pt; color: #38bdf8; font-weight: 600; text-transform: uppercase; margin-top: 1px; }
  
  .badges-group { display: flex; gap: 5px; flex-direction: column; align-items: flex-end; }
  .badge {
    padding: 2.5px 7px;
    border-radius: 4px;
    font-size: 7.2pt;
    font-weight: 700;
    text-transform: uppercase;
  }
  .badge-cyan { background: #00f3ff; color: #0f172a; }
  .badge-dark { background: #334155; color: #cbd5e1; }

  /* MISION CARD */
  .mission-card {
    background: #f0fdf4;
    border: 1px solid #bbf7d0;
    border-left: 4px solid #16a34a;
    border-radius: 6px;
    padding: 8px 12px;
    margin-bottom: 9px;
  }
  .mission-title {
    font-size: 8pt;
    font-weight: 800;
    color: #15803d;
    text-transform: uppercase;
    margin-bottom: 2px;
  }
  .mission-text { font-size: 7.7pt; color: #166534; line-height: 1.25; }

  /* LIDERAZGO CARD */
  .leadership-card {
    background: #f8fafc;
    border: 1px solid #cbd5e1;
    border-left: 5px solid #f59e0b;
    border-radius: 6px;
    padding: 8px 12px;
    margin-bottom: 9px;
  }
  .leadership-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 4px;
  }
  .leadership-title { font-size: 8.8pt; font-weight: 800; color: #92400e; text-transform: uppercase; }
  .role-badge { background: #fef3c7; color: #b45309; padding: 2px 6px; border-radius: 4px; font-size: 7pt; font-weight: 700; }
  
  .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
  .bullet-list { list-style: none; }
  .bullet-list li {
    position: relative;
    padding-left: 13px;
    margin-bottom: 2.5px;
    font-size: 7.5pt;
    color: #334155;
  }
  .bullet-list li::before {
    content: "•";
    position: absolute;
    left: 2px;
    color: #0284c7;
    font-weight: bold;
    font-size: 9pt;
  }

  /* SUB-VERTICALES OPERATIVAS: 3 COLUMNAS */
  .verticals-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 8px;
    margin-bottom: 9px;
  }
  .card-vertical {
    background: #ffffff;
    border-radius: 6px;
    border: 1px solid #cbd5e1;
    padding: 9px 10px;
    display: flex;
    flex-direction: column;
  }
  .v-compras { border-top: 4px solid #0284c7; }
  .v-deposito { border-top: 4px solid #10b981; }
  .v-sucursal { border-top: 4px solid #8b5cf6; }

  .v-title {
    font-size: 8.5pt;
    font-weight: 800;
    text-transform: uppercase;
    margin-bottom: 3px;
  }
  .v-compras .v-title { color: #0369a1; }
  .v-deposito .v-title { color: #047857; }
  .v-sucursal .v-title { color: #6d28d9; }

  .v-roles {
    font-size: 7pt;
    font-weight: 700;
    color: #64748b;
    margin-bottom: 6px;
    padding-bottom: 4px;
    border-bottom: 1px dashed #e2e8f0;
  }

  /* WIDGETS DE IMPACTO OPERATIVO */
  .metrics-section {
    background: #f8fafc;
    border: 1px solid #e2e8f0;
    border-radius: 6px;
    padding: 8px 10px;
    margin-bottom: 9px;
  }
  .section-label {
    font-size: 7.8pt;
    font-weight: 800;
    color: #334155;
    text-transform: uppercase;
    margin-bottom: 6px;
    display: flex;
    justify-content: space-between;
  }
  .kpi-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 6px; }
  .metric-card {
    background: #ffffff;
    border: 1px solid #cbd5e1;
    border-radius: 5px;
    padding: 6px;
    text-align: center;
  }
  .metric-val { font-size: 9.5pt; font-weight: 900; color: #0284c7; }
  .metric-desc { font-size: 6.8pt; font-weight: 700; color: #475569; text-transform: uppercase; margin-top: 2px; }

  /* FOOTER */
  .footer-bar {
    margin-top: auto;
    border-top: 2px solid #0f172a;
    padding-top: 6px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 7pt;
    color: #64748b;
  }
</style>
</head>
<body>

<div style="display: flex; flex-direction: column; width: 210mm;">
  <button onclick="window.print()" class="btn-print no-print">🖨️ Imprimir / Guardar en PDF</button>

  <div class="page-container">
    <div>
      <!-- HEADER BANNER -->
      <div class="header-banner">
        <div class="header-title">
          <h1>ÁREA DE SUMINISTROS Y LOGÍSTICA (S&L)</h1>
          <p>Obercom Telecomunicaciones | Mapa Operativo y Estructura de Roles</p>
        </div>
        <div class="badges-group">
          <span class="badge badge-cyan">Motor Logístico</span>
          <span class="badge badge-dark">Sede Central: Oberá, Misiones</span>
        </div>
      </div>

      <!-- MISIÓN Y RAZÓN DE SER -->
      <div class="mission-card">
        <div class="mission-title">Nuestra Razón de Ser</div>
        <div class="mission-text">
          Garantizar la <b>continuidad operativa</b> y sostener la <b>expansión de la red GPON</b> al menor <b>Costo Total de Propiedad (TCO)</b>. Aseguramos que las cuadrillas de campo y la red de sucursales dispongan de los insumos en tiempo y forma, optimizando recursos y protegiendo el capital corporativo.
        </div>
      </div>

      <!-- LIDERAZGO Y ESTRATEGIA -->
      <div class="leadership-card">
        <div class="leadership-header">
          <span class="leadership-title">Liderazgo & Dirección General del Área</span>
          <span class="role-badge">Rol: Gerente de Suministros y Logística</span>
        </div>
        <div class="grid-2">
          <ul class="bullet-list">
            <li><b>Estrategia & Alineación:</b> Planificación integral y sinergia directa con Dirección General.</li>
            <li><b>Control Presupuestario:</b> Optimización y reducción continua del TCO en la cadena.</li>
          </ul>
          <ul class="bullet-list">
            <li><b>Tablero de Mando:</b> Monitoreo y reporte periódico de KPIs operativos y comerciales.</li>
            <li><b>Gestión del Riesgo:</b> Blindaje preventivo contra quiebres de stock y demoras críticas.</li>
          </ul>
        </div>
      </div>

      <!-- 3 SUB-VERTICALES OPERATIVAS -->
      <div class="verticals-grid">
        
        <!-- VERTICAL 1 -->
        <div class="card-vertical v-compras">
          <div class="v-title">1. Compras & Suministros</div>
          <div class="v-roles">Encargado de Compras | Asistente de Suministros</div>
          <ul class="bullet-list">
            <li><b>Negociación Comercial:</b> Compulsa, cuadro comparativo de presupuestos y precios.</li>
            <li><b>Padrón Homologado:</b> Auditoría y calificación continua de proveedores estratégicos.</li>
            <li><b>Insumos Críticos:</b> Adquisición de fibra óptica, ONUs y equipamiento GPON.</li>
            <li><b>Compras Operativas:</b> Ferretería, insumos menores, compras web y soporte a Finanzas.</li>
            <li><b>Gestión Local:</b> Retiros comerciales y logística de insumos en plaza local.</li>
          </ul>
        </div>

        <!-- VERTICAL 2 -->
        <div class="card-vertical v-deposito">
          <div class="v-title">2. Depósito & Equipamiento</div>
          <div class="v-roles">Mantenimiento de Equipamiento | Asist. Suministros</div>
          <ul class="bullet-list">
            <li><b>Laboratorio Técnico:</b> Diagnóstico, limpieza, reparación y flasheo de firmware en ONUs y routers.</li>
            <li><b>Control de Inventario:</b> Conciliación física diaria vs. sistemas (SGR / SmartOLT).</li>
            <li><b>Auditorías Cruzadas:</b> Fiscalización de stock en depósitos de las sucursales.</li>
            <li><b>Kits Diarios:</b> Preparación y despacho de materiales para cuadrillas de calle.</li>
            <li><b>Flota Móvil:</b> Control periódico de herramientas e insumos a bordo de camionetas.</li>
          </ul>
        </div>

        <!-- VERTICAL 3 -->
        <div class="card-vertical v-sucursal">
          <div class="v-title">3. Red de Sucursales</div>
          <div class="v-roles">Asistente de Sucursal (Nexo Intersucursal)</div>
          <ul class="bullet-list">
            <li><b>Nexo Operativo:</b> Puente logístico directo entre Casa Central (Oberá) e interior.</li>
            <li><b>Gestión de Stock Local:</b> Control analítico de existencias e insumos en cada sede.</li>
            <li><b>Recepción & Remesas:</b> Despacho y recepción física de encomiendas de insumos.</li>
            <li><b>Soporte a Técnicos:</b> Armado diario de kits de trabajo para instaladores locales.</li>
            <li><b>Alerta Preventiva:</b> Reporte temprano de faltantes y supervisión de móviles locales.</li>
          </ul>
        </div>

      </div>

      <!-- PILARES OPERATIVOS / KPIS -->
      <div class="metrics-section">
        <div class="section-label">
          <span>Capacidades de Gestión y Control Logístico</span>
          <span style="color: #0284c7;">Trazabilidad Extremo a Extremo</span>
        </div>
        <div class="kpi-row">
          <div class="metric-card">
            <div class="metric-val">TCO</div>
            <div class="metric-desc">Costo Total Propiedad</div>
          </div>
          <div class="metric-card">
            <div class="metric-val">SGR / OLT</div>
            <div class="metric-desc">Gestión de Stock Activo</div>
          </div>
          <div class="metric-card">
            <div class="metric-val">100%</div>
            <div class="metric-desc">Kits Diarios a Campo</div>
          </div>
          <div class="metric-card">
            <div class="metric-val">Auditoría</div>
            <div class="metric-desc">Depósitos e Intersucursal</div>
          </div>
        </div>
      </div>
    </div>

    <!-- FOOTER -->
    <div class="footer-bar">
      <div><b>Obercom Telecomunicaciones</b> — Dirección de Operaciones y Cadena de Suministro</div>
      <div>Casa Central: Oberá, Misiones | Gestión Logística Integrada</div>
    </div>

  </div>
</div>

</body>
</html>
