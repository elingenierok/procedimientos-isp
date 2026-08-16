```mermaid
gantt
    title COMPARATIVO DE TIEMPOS - ANTES VS DESPUES (ONU CATV)
    dateFormat  YYYY-MM-DD HH:mm:ss
    axisFormat  %M:%S

    section ESCENARIO ANTES (16m 42s Total)
    Bloque A - Recepcion y Conexion (00:51)       :done, a1, 2026-01-01 00:00:00, 2026-01-01 00:00:51
    Bloque B - SmartOLT y SGR - Friccion (08:19)  :crit, active, a2, after a1, 8m 19s
    Bloque C - Test WiFi y Etiquetado (00:44)     :done, a3, after a2, 44s
    Bloque D - Acondicionamiento y GR (08:23)     :a4, after a3, 8m 23s

    section ESCENARIO DESPUES (11m 43s Total)
    Bloque A - Recepcion y Conexion (00:51)       :done, b1, 2026-01-01 00:00:00, 2026-01-01 00:00:51
    Bloque B - SmartOLT y NOC - Optimizado (03:20):active, b2, after b1, 3m 20s
    Bloque C - Test WiFi y Etiquetado (00:44)     :done, b3, after b2, 44s
    Bloque D - Acondicionamiento y GR (08:23)     :b4, after b3, 8m 23s
