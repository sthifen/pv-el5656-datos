# Datos en vivo — arreglos FV 1 y 6 (EL-5656, Grupo 4, TEC San Carlos)

**Página:** https://sthifen.github.io/pv-el5656-datos/

Compara el rendimiento de dos arreglos fotovoltaicos (1 y 6). Una Raspberry Pi 4 registra un dato
por minuto y la página muestra las gráficas en vivo (irradiancia, temperaturas, humedad, potencia,
voltaje y corriente DC, rendimiento y energía).

**Sensores:** Spektron 210 (irradiancia, por ADS1115), 2 DS18B20 (temperatura de celda),
2 DHT22 (temperatura y humedad ambiente) e inversores SMA Sunny Boy (lado DC por Modbus TCP o web).

**Datos:** `datos/AAAA-MM-DD.csv`, una fila por minuto (NaN = sin lectura):
`fecha, G_Wm2, Tc1_C, Tc6_C, Tamb1_C, Tamb6_C, HR1_pct, HR6_pct, Pdc1_W, Pdc6_W, Vdc1_V, Vdc6_V, Idc1_A, Idc6_A`

Se publican solos desde la Pi cada 6 min (`publicar.py`).
Nota: desde el 30/10/2026 19:04 la irradiancia tiene corregido el desfase de noche (antes marcaba ~138 W/m² sin sol).
