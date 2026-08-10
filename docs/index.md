# Portal de Procedimientos Operativos - Obercom

Bienvenido al centro de documentación oficial. Utiliza la red interactiva de procesos o el menú lateral para acceder a la documentación estandarizada.

**Mapa Interactivo de Procesos**

<div id="network-map" style="height: 480px; width: 100%; border: 1px solid #41B6E6; border-radius: 8px; background-color: #0f172a; margin-top: 15px; margin-bottom: 20px;"></div>

<script src="https://unpkg.com/vis-network/standalone/umd/vis-network.min.js"></script>
<script>
  // Definición de las burbujas (Nodos)
  const nodes = new vis.DataSet([
    { id: 1, label: 'PR-COM-001\nCompras', shape: 'dot', size: 30, color: { background: '#00205B', border: '#41B6E6' }, font: { color: '#ffffff', face: 'Raleway', size: 14 }, url: 'suministros-logistica/PR-COM-001/' },
    { id: 2, label: 'PR-PEDT-001\nPedidos Técnicos', shape: 'dot', size: 30, color: { background: '#00205B', border: '#41B6E6' }, font: { color: '#ffffff', face: 'Raleway', size: 14 }, url: 'suministros-logistica/PR-PEDT-001/' },
    { id: 3, label: 'PR-REC-001\nRecupero de Equipos', shape: 'dot', size: 30, color: { background: '#00205B', border: '#41B6E6' }, font: { color: '#ffffff', face: 'Raleway', size: 14 }, url: 'suministros-logistica/PR-REC-001/' },
    { id: 4, label: 'PR-AIS-001\nProceso Aislado', shape: 'dot', size: 22, color: { background: '#334155', border: '#94a3b8' }, font: { color: '#ffffff', face: 'Raleway', size: 12 }, url: '#' }
  ]);

  // Definición de conexiones entre procesos
  const edges = new vis.DataSet([
    { from: 2, to: 1, label: 'Insumos faltantes', color: { color: '#41B6E6' }, font: { color: '#94a3b8', size: 11, align: 'middle' }, arrows: 'to' },
    { from: 2, to: 3, label: 'Equipos devueltos', color: { color: '#41B6E6' }, font: { color: '#94a3b8', size: 11, align: 'middle' }, arrows: 'to' }
  ]);

  // Parámetros de física y comportamiento visual
  const container = document.getElementById('network-map');
  const data = { nodes: nodes, edges: edges };
  const options = {
    physics: {
      enabled: true,
      barnesHut: { gravConstant: -2500, springLength: 120, centralGravity: 0.3 }
    },
    nodes: { borderWidth: 2 },
    interaction: { hover: true, zoomView: true, dragView: true }
  };

  // Inicialización de la red
  const network = new vis.Network(container, data, options);

  // Redirección al hacer clic en cualquier burbuja
  network.on("click", function (params) {
    if (params.nodes.length > 0) {
      const nodeId = params.nodes[0];
      const nodeData = nodes.get(nodeId);
      if (nodeData.url && nodeData.url !== '#') {
        window.location.href = nodeData.url;
      }
    }
  });
</script>

---

**Áreas Operativas**
* **Suministros y Logística:** Gestión de compras, inventario de móviles y recupero de hardware.
