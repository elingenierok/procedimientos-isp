```mermaid
gantt
    title COMPARATIVO DE TIEMPOS - ANTES VS DESPUES (ONU CATV)
    dateFormat  YYYY-MM-DD HH:mm:ss
    axisFormat  %M:%S

    section ESCENARIO ANTES (16m 42s Total)
    Bloque A - Recepcion y Conexion (00:51)       :done, a1, 2026-01-01 00:00:00, 2026-01-01 00:00:51
    Bloque B - SmartOLT y SGR - Friccion (08:19)  :crit, active, a2, 2026-01-01 00:00:51, 2026-01-01 00:09:10
    Bloque C - Test WiFi y Etiquetado (00:44)     :done, a3, 2026-01-01 00:09:10, 2026-01-01 00:09:54
    Bloque D - Acondicionamiento y GR (08:23)     :a4, 2026-01-01 00:09:54, 2026-01-01 00:18:17

    section ESCENARIO DESPUES (11m 43s Total)
    Bloque A - Recepcion y Conexion (00:51)       :done, b1, 2026-01-01 00:00:00, 2026-01-01 00:00:51
    Bloque B - SmartOLT y NOC - Optimizado (03:20) :active, b2, 2026-01-01 00:00:51, 2026-01-01 00:04:11
    Bloque C - Test WiFi y Etiquetado (00:44)     :done, b3, 2026-01-01 00:04:11, 2026-01-01 00:04:55
    Bloque D - Acondicionamiento y GR (08:23)     :b4, 2026-01-01 00:04:55, 2026-01-01 00:13:18
