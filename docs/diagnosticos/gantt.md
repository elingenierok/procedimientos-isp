```mermaid
gantt
    title Comparativo de Tiempos: Antes vs Después (ONU CATV)
    dateFormat HH:mm:ss
    axisFormat %M:%S

    section ANTES (16m 42s Total)
    Bloque A - Recepción y Conexión (0:51)      :done, a1, 00:00:00, 00:00:51
    Bloque B - SmartOLT / SGR (Fricción) (8:19) :crit, active, a2, after a1, 00:08:19
    Bloque C - Test WiFi y Etiquetado (0:44)   :done, a3, after a2, 00:00:44
    Bloque D - Acondicionamiento y GR (8:23)   :a4, after a3, 00:08:23

    section DESPUÉS (11m 43s Total)
    Bloque A - Recepción y Conexión (0:51)      :done, b1, 00:00:00, 00:00:51
    Bloque B - SmartOLT / NOC (Optimizado) (3:20):active, b2, after b1, 00:03:20
    Bloque C - Test WiFi y Etiquetado (0:44)   :done, b3, after b2, 00:00:44
    Bloque D - Acondicionamiento y GR (8:23)   :b4, after b3, 00:08:23
