# LEGO Loop: la segunda vida del ladrillo LEGO gracias a la visión artificial

**Trabajo de digitalización. Empresa analizada: The LEGO Group**

> **La idea en una frase:** LEGO fabrica el juguete más duradero del mundo, pero no sabe recuperarlo. Sus piezas usadas se clasifican **a mano** y solo en tres países. Proponemos una red de plantas con **visión artificial y robots** que identifican cada pieza usada (entre más de 25.000 tipos distintos), la limpian, la revisan y la devuelven al mercado a través de **BrickLink**, la web de segunda mano que LEGO ya posee, con un **pasaporte digital de producto**.

**Cómo leer este documento:**
- **(dato)** es una cifra real con fuente, listada en el Anexo D.
- **(supuesto)** es una estimación nuestra, razonada, que usamos para los cálculos.
- "LEGO Loop" es el nombre que damos a la propuesta; no es un programa real de LEGO.
- Antes de entregar, conviene comprobar las cifras principales en el *Informe Anual 2025* de LEGO (enlace en el Anexo D).

---

## 0. ¿Por qué LEGO? (y por qué encaja con lo que pide el profesor)

| Lo que pide el profesor | Cómo lo cumple este proyecto |
|---|---|
| **Empresa grande** | ≈11.200 M€ de ventas y 33.801 empleados en 2025 (dato) |
| **Realista** | La tecnología ya existe. Una startup lituana (Sort A Brick) ya clasifica LEGO usado con IA con un 99 % de precisión (dato), y LEGO tiene patentes propias de reconocimiento de piezas con redes neuronales (dato) |
| **Que la empresa lo pueda pagar** | La inversión (25 M€) equivale al **0,8 % del beneficio operativo de un solo año** |
| **Original** | La mayoría de trabajos eligen Zara, Mercadona o Amazon. Casi nadie se pregunta qué pasa con el LEGO que hay en los trasteros |
| **Cuanto más friki, mejor** | IA entrenada con los modelos 3D oficiales de cada pieza, detección automática de clones (Lepin, Mould King…), minifiguras, BrickLink, AFOLs… (ver glosario, Anexo B) |

---

## 1. Objetivos estratégicos de la empresa

### 1.1 Presentación de la empresa

| | |
|---|---|
| **Qué hace** | Diseña, fabrica y vende juguetes de construcción (LEGO System, DUPLO, Technic…) y experiencias digitales asociadas |
| **Sede y origen** | Billund (Dinamarca), fundada en 1932 por Ole Kirk Kristiansen |
| **Propiedad** | Empresa familiar no cotizada: 75 % KIRKBI (familia Kirk Kristiansen) y 25 % Fundación LEGO |
| **Ventas 2025** | 83.500 M de coronas danesas ≈ **11.200 M€** (+12 %) (dato) |
| **Beneficio operativo 2025** | 22.000 M DKK ≈ **2.950 M€** (+18 %) (dato) |
| **Beneficio neto 2025** | 16.700 M DKK ≈ **2.240 M€** (+21 %), el mejor año de su historia (dato) |
| **Empleados** | **33.801** (+8 %) (dato) |
| **Crecimiento frente al mercado** | Ventas al consumidor +16 %, frente al +7 % del mercado del juguete (dato) |
| **Fábricas** | Billund (Dinamarca), Nyíregyháza (Hungría), Kladno (Chequia), Monterrey (México), Jiaxing (China) y Binh Duong (Vietnam, abierta en 2025). En construcción: Virginia (EE. UU.), más de 1.500 M$ de inversión, apertura en 2027 (dato) |
| **Tiendas** | Más de 1.100 tiendas de marca en el mundo (dato) |
| **Dónde opera** | Vende en más de 130 países |
| **Dato clave para el proyecto** | Desde 2019 es dueña de **BrickLink**, el mayor mercado online de piezas LEGO nuevas y usadas: más de 1 millón de miembros y más de 10.000 tiendas de 70 países (dato) |

*Conversión usada: 1 € = 7,46 DKK (la corona danesa está anclada al euro).*

### 1.2 Qué quiere conseguir LEGO en los próximos años

Estos objetivos salen de sus informes anuales y de sus compromisos públicos. Cada uno tiene un **indicador (KPI)**, y en el punto 6 comprobamos si el proyecto lo cumple.

| # | Objetivo estratégico | Evidencia (fuente) | KPI con el que lo mediremos en el punto 6 |
|---|---|---|---|
| **O1** | **Crecer de forma rentable** y llegar a más niños | Inversión en fábricas nuevas (Vietnam, Virginia) y ampliaciones en Hungría, México y China. Su CEO destaca que llegan "a más niños que nunca" (dato) | Nuevos ingresos, EBITDA y plazo de recuperación de la inversión |
| **O2** | **Sostenibilidad**: −37 % de emisiones en 2032 respecto a 2019, cero plástico fósil en 2032 (la mitad en 2026) y cero emisiones netas en 2050 | Compromisos públicos. En 2025, el 52 % del material comprado ya era renovable o reciclado (dato) | Toneladas de plástico que no hay que fabricar y toneladas de CO₂ evitadas |
| **O3** | **Fans y experiencia del cliente**, incluidos los adultos (AFOL) | Compró BrickLink "para reforzar los lazos con los fans adultos" (dato). Programa de fidelización LEGO Insiders | Hogares participantes, satisfacción (NPS) y nuevos servicios para fans |
| **O4** | **Tecnología digital y cadena de suministro** | En sus resultados de 2025 cita como prioridades estratégicas "sostenibilidad, red de cadena de suministro y tecnología digital" (dato) | Procesos automatizados con IA y datos pieza a pieza integrados en sus sistemas |
| **O5** | **Anticiparse a la regulación europea** | El Reglamento (UE) 2025/2509 de seguridad de los juguetes obliga a tener un **Pasaporte Digital de Producto desde el 1-8-2030** (dato). En Francia, los fabricantes de juguetes ya tienen responsabilidad ampliada del productor desde 2022 (dato) | Pasaporte digital funcionando antes de 2030 |

### 1.3 El problema: la paradoja del ladrillo eterno

1. **El ladrillo LEGO no se rompe.** Una pieza de 1958 sigue encajando con una de hoy. Es su mayor virtud… y un problema ambiental, porque es plástico que dura décadas.
2. **Cuanto más vende LEGO, más plástico nuevo necesita.** Su intento de fabricar ladrillos con botellas recicladas (rPET) fracasó en 2023, porque habría **aumentado** las emisiones (dato). En 2025 sus emisiones totales fueron de **2,19 millones de toneladas de CO₂e, un +0,2 %** respecto a 2024: no bajan, porque el crecimiento se come las mejoras (dato). El 99 % de esas emisiones vienen de la cadena de suministro, sobre todo de materiales (dato).
3. **Mientras tanto, miles de millones de piezas duermen en los trasteros.** La respuesta de LEGO es **LEGO Replay**, un programa de donación que:
   - solo existe en **EE. UU., Canadá y Reino Unido** (este último, en piloto desde 2024) (dato);
   - **clasifica e inspecciona cada pieza a mano** (dato);
   - no genera ingresos (todo se dona) y no da nada a cambio al que dona;
   - en 5 años ha movido **≈557 toneladas (300 millones de piezas)** (dato). Parece mucho, pero LEGO fabrica **decenas de miles de millones de piezas cada año**.
4. **¿Por qué no escala? Porque clasificar LEGO a mano es imposible.** Hay más de **25.000 combinaciones de forma y color** (dato). Una persona puede separar "ladrillos rojos" de "placas azules", pero no identificar cada pieza exacta. Por eso las piezas solo se pueden donar en cajas mezcladas, nunca revender una a una.
5. **Se pierde mucho valor.** Un kilo de LEGO usado sin clasificar se vende a ≈4–10 €. Un kilo clasificado vale ≈15–30 € (dato: 2–5 $/lb frente a 8–15 $/lb). Y LEGO es dueña del mayor mercado de segunda mano (BrickLink), pero no participa en él como vendedora de usado.
6. **La regulación aprieta**: pasaporte digital obligatorio en 2030 y responsabilidad del productor en Francia.

> **Conclusión del diagnóstico:** el problema de fondo no es el plástico, es la **información**. Nadie sabe qué pieza es cada pieza. Y eso es justo lo que resuelve la digitalización.

---

## 2. Áreas a digitalizar

Cada área conecta con al menos un objetivo del punto 1.

| # | Área / departamento | Cómo se hace hoy (problema) | Tecnología propuesta | Objetivo |
|---|---|---|---|---|
| **A** | **Recogida y relación con el cliente** (Consumer Experience, tiendas) | En Replay metes piezas en una caja, pegas una etiqueta y no recibes nada. En España no existe | **App "LEGO Loop"** (módulo de la app de LEGO): la cámara del móvil escanea el montón y una IA estima kilos, valor y minifiguras (como la app Brickit, pero con tecnología propia de LEGO). A cambio, crédito en LEGO Insiders. Entrega en tienda LEGO o en oficina de Correos | O1, O3 |
| **B** | **Operaciones: clasificación y control de calidad** (Supply Chain) | A mano, por grupos grandes. Inviable para 25.000 tipos | **Planta "Brick Hub"**: lavado industrial, cintas, cámaras desde varios ángulos y una **red neuronal** que identifica cada pieza en milisegundos; chorros de aire la envían a su cajón. Visión artificial para detectar defectos y clones. Una persona solo revisa los casos dudosos | O2, O4 |
| **C** | **Inventario, precios y venta** (BrickLink, Pick a Brick, e-commerce) | La pieza usada no tiene inventario ni precio. LEGO no vende usado | **Inventario digital pieza a pieza** conectado por API a BrickLink y Pick a Brick. **Precio dinámico con IA** a partir del histórico de precios de BrickLink. **Algoritmo que "recompone" sets completos** con el stock disponible | O1, O3 |
| **D** | **Trazabilidad y cumplimiento** (Legal, Calidad, Sostenibilidad) | No hay trazabilidad del usado. El pasaporte digital será obligatorio en 2030 | **Pasaporte Digital de Producto**: un QR en cada caja de segunda vida con el origen, el % reutilizado, el lavado y el CO₂ evitado (estándar GS1 Digital Link) | O5, O2 |
| **E** | **Datos para diseño y producción** (Diseño, Planificación) | LEGO no sabe qué piezas se rompen, cuáles sobran en los hogares ni cuáles faltan | **Plataforma de datos con cuadros de mando (BI)**: tasa de rotura por pieza, color y antigüedad; piezas que ya no hace falta volver a fabricar para Pick a Brick; datos de desgaste para los equipos que prueban los nuevos plásticos renovables | O2, O4 |

### 2.1 Cómo funciona la máquina (la parte friki)

1. **Tolva y vibrador**: el montón de piezas lavadas entra en una tolva y una bandeja vibratoria las separa para que pasen **de una en una**.
2. **Túnel de cámaras**: cada pieza pasa por varias cámaras que la fotografían desde distintos ángulos.
3. **Red neuronal convolucional (CNN)**: identifica la pieza (su código de elemento), el color y el estado.
   - **Truco friki:** la IA se entrena con **imágenes sintéticas** generadas a partir de los **modelos 3D oficiales de cada pieza que LEGO ha fabricado**. Es lo que hizo el ingeniero Daniel West con su *Universal LEGO Sorting Machine* usando Blender (dato), pero LEGO tiene los planos oficiales de todo su catálogo.
   - LEGO ya tiene **patentes de reconocimiento de piezas con redes neuronales** (patente US10213692B2) (dato).
4. **Control de calidad por visión**: detecta grietas, decoloración, mordiscos, restos de pegamento y **clones** (marcas que imitan a LEGO), por ejemplo mirando si aparece el logo "LEGO" en los tetones.
5. **Chorros de aire**: empujan la pieza al cajón que le toca.
6. **Humano en el bucle**: si la IA no está segura (confianza baja), la pieza va a un inspector. Cada corrección del inspector reentrena la IA.

**Referencia real de rendimiento:** la máquina industrial de Sort A Brick procesa ≈1.000 piezas por hora, reconoce más de 25.000 elementos (4.000 formas y 40 colores) y acierta más del 99 % (dato). Nuestro diseño agrupa **3 máquinas en un "módulo"** (3.000 piezas por hora) (supuesto).

### 2.2 Los destinos de cada kilo recogido (supuesto)

| Destino | % del kilo | Qué es |
|---|---|---|
| **Sets "LEGO Segunda Vida"** y **piezas sueltas** | 75 % | Sets completos recompuestos (si falta alguna pieza, se añade nueva) y piezas sueltas vendidas en la tienda oficial de LEGO en BrickLink y en Pick a Brick |
| **Donación Replay** | 10 % | Cajas para ONG y colegios: se mantiene el compromiso social del programa actual |
| **Reciclaje de material** | 15 % | Piezas dañadas o clones. Se trituran para productos que no son juguetes (como las cajas de almacenaje del piloto británico) |

**Servicio extra para fans adultos: "Clasifica mi colección".** El fan manda sus 20 kg de piezas mezcladas y se las devuelven clasificadas e inventariadas en su cuenta de BrickLink, por **10 €/kg** (es lo que ya cobra Sort A Brick) (dato).

---

## 3. Plan de integración

### 3.1 Fases y plazos

| Fase | Cuándo | Qué se hace |
|---|---|---|
| **0 · Preparación** | Oct 2026 – Mar 2027 | Plan de negocio. Acuerdo con un socio tecnológico (tipo Sort A Brick), por licencia o por inversión (LEGO ya invierte en startups a través de LEGO Ventures). Diseño de la app. Alquiler de una nave para el piloto en el Corredor del Henares (Madrid). Primer entrenamiento de la IA con los modelos 3D oficiales |
| **1 · Piloto en España** | Abr 2027 – Dic 2027 | **4 módulos** en Madrid. Recogida en las tiendas LEGO de España y en oficinas de Correos. Venta solo por BrickLink. Objetivo: 60 t |
| **Decisión (go/no-go)** | Dic 2027 | Se miden los KPIs del piloto (ver 3.2). Si se cumplen, se escala; si no, se corrige o se para |
| **2 · Escalado europeo** | 2028 – 2029 | **Brick Hub junto a la fábrica de Kladno** (Chequia), en el centro de Europa y cerca de Alemania, el mayor mercado de juguetes europeo: 22 módulos en 2028 y 14 más en 2029. Se amplía a Alemania, Francia, Italia, Portugal, Benelux, Dinamarca, Polonia… Se integran Pick a Brick y los sets recompuestos. Primeros pasaportes digitales |
| **3 · Consolidación** | 2030 – 2032 | Plena capacidad (≈1.340 t/año entre Madrid y Kladno). Pasaporte digital adaptado a la obligación del 1-8-2030. Migración de Replay Reino Unido al nuevo modelo. Estudio de un segundo hub junto a la fábrica de Virginia (fuera de los cálculos) |

**Calendario visual:**

```
                     2026  2027              2028              2029      2030-2032
                      T4   T1  T2  T3  T4    T1  T2  T3  T4    T1 … T4
Fase 0 Preparación   ████  ██
Fase 1 Piloto España           ██  ██  ██
Decisión go/no-go                        ◆
Fase 2 Hub Kladno                            ██  ██  ██  ██    ██ … ██
Fase 3 Consolidación                                                     ██████████
```

### 3.2 La prueba piloto y sus criterios de decisión

Se hace primero en **España** porque es un mercado mediano y representativo del sur de Europa, tiene buena red de paquetería y tiendas LEGO en las grandes ciudades, y **un fallo aquí sale barato**.

| KPI del piloto | Umbral para escalar |
|---|---|
| Precisión de identificación (verificada por muestreo) | ≥ 98 % |
| Toneladas recogidas / hogares participantes | ≥ 60 t / ≥ 10.000 hogares |
| Precio medio de venta | ≥ 26 €/kg vendido |
| Margen de contribución | ≥ 10 €/kg recogido |
| Satisfacción del cliente (NPS) | ≥ 50 |
| Reclamaciones por calidad o higiene | < 1 % de pedidos, y 0 incidentes de seguridad |

**Qué pasa si sale mal:** si el piloto da cifras del escenario pesimista, **no se construye el hub**. La pérdida máxima sería de ≈6,4 M€, el **0,2 % del beneficio operativo anual** de LEGO. El piloto funciona como un seguro.

### 3.3 Cómo se conectan los sistemas

```
 CLIENTE                         PLANTA (Brick Hub)                    VENTA Y DATOS
 ───────                         ──────────────────                    ─────────────
 App LEGO (módulo Loop)
   │ foto del montón
   ▼
 IA de tasación (nube) ──► LEGO Insiders (CRM)
   │  kg y valor estimados     crédito provisional
   ▼
 Entrega: tienda / Correos ──► Recepción y pesaje ──► crédito definitivo (CRM)
                                  │
                                  ▼
                           MES (control de líneas):
                           cada pieza = código + color + estado
                                  │
                                  ▼
                           WMS (inventario pieza a pieza) ◄──► ERP de LEGO (SAP)
                                  │                             stock y contabilidad
                                  ▼
                           Motor de destino y precios (IA)
                           ├─► API BrickLink (tienda oficial)
                           ├─► Pick a Brick (lego.com)
                           ├─► Sets recompuestos ──► Pasaporte digital (QR)
                           ├─► Cajas de donación Replay (ONG)
                           └─► Reciclaje de material
                                  │
                                  ▼
                           Plataforma de datos (BI) ──► Diseño · Planificación · Sostenibilidad
```

**Integraciones clave:**
- **App ↔ LEGO Insiders**, para dar el crédito.
- **Planta ↔ ERP (SAP)**, para el stock y la contabilidad.
- **Inventario ↔ BrickLink y Pick a Brick**, para vender.
- **Todo ↔ plataforma de datos.**
- **Privacidad (RGPD):** las fotos de los usuarios se procesan y se borran; nunca se guardan imágenes de sus casas.

### 3.4 Quién se encarga

| Responsable | Qué hace |
|---|---|
| **Dirección de Operaciones** (patrocinador) y **Dirección de Sostenibilidad** (copatrocinador) | Aprueban el presupuesto, deciden el go/no-go y rinden cuentas al comité de dirección |
| **Director/a del programa LEGO Loop** (oficina de proyecto) | Coordina plazos, costes y riesgos |
| **Digital Technology** | App, IA, integraciones con SAP, BrickLink e Insiders, plataforma de datos |
| **Operaciones / Supply Chain** | Construir y operar las plantas de Madrid y Kladno |
| **Equipo BrickLink + e-commerce** | Tienda oficial de usado, Pick a Brick y precios |
| **Legal, Calidad y Cumplimiento** | Seguridad de los juguetes usados, pasaporte digital, RGPD |
| **RRHH** | Selección, formación y gestión del cambio (punto 5) |
| **Tiendas LEGO de España** | Puntos de recogida durante el piloto |
| **Socios externos** | Tecnología de clasificación (tipo Sort A Brick), logística (Correos) y ONG (donación) |

---

## 4. Costes y beneficios

### 4.1 Supuestos principales

| Supuesto | Valor | En qué se basa |
|---|---|---|
| Piezas por kilo | 538 | Dato de Replay: 300 M de piezas en 1,23 M de libras |
| Capacidad de un módulo (3 máquinas) | 3.000 piezas/h | Sort A Brick: 1.000 piezas/h por máquina (dato) |
| Coste de un módulo | 360.000 € (120.000 € por máquina) | Supuesto |
| Horas al año | 3.840 h (2 turnos) · 6.000 h (3 turnos) | Supuesto |
| Toneladas recogidas | 60 → 350 → 800 → 1.050 → 1.150 → 1.200 (2027–2032) | Supuesto. Replay EE. UU. recoge ≈110 t/año sin dar nada a cambio; aquí hay crédito y toda Europa |
| Kilos por envío | 6 kg | Supuesto |
| Precio medio de venta | 30 €/kg vendido | Mezcla de piezas sueltas, sets y minifiguras. Un kilo nuevo cuesta ≈54 € (0,10 €/pieza), y los lotes clasificados se venden a 15–30 €/kg (dato) |
| Crédito al usuario | 5 €/kg en puntos LEGO Insiders | Parecido a lo que se saca en Wallapop por LEGO a granel, pero sin esfuerzo |
| Logística de entrada | 2 €/kg | Supuesto |
| Lavado, energía y consumibles | 0,60 €/kg procesado | Supuesto |
| Envío y comisiones de venta | 2 €/kg vendido | Supuesto |
| Canibalización | 10 % de las ventas de usado | Clientes que habrían comprado nuevo. Se cuenta como coste (supuesto) |
| Ventas extra gracias al crédito | 2 €/kg recogido de margen | El que canjea su crédito suele comprar algo más (supuesto) |
| Servicio "Clasifica mi colección" | 10 €/kg | Precio de Sort A Brick (dato) |

### 4.2 Inversión (compra, instalación y software)

| Concepto | 2027 Piloto Madrid | 2028 Hub Kladno (A) | 2029 Hub Kladno (B) | Total |
|---|---:|---:|---:|---:|
| Módulos de clasificación (IA + cámaras + cintas) | 1,44 (4 mód.) | 7,92 (22 mód.) | 5,04 (14 mód.) | 14,40 |
| Lavado industrial, preclasificación y robots de empaquetado | 0,40 | 1,80 | 0,60 | 2,80 |
| Adecuación de naves (instalación) | 0,30 | 2,50 | – | 2,80 |
| Software: app de tasación, inventario, integraciones, plataforma de datos y pasaporte digital | 1,50 | 1,80 | 0,40 | 3,70 |
| Acuerdo con el socio tecnológico (licencia o participación) | 0,80 | – | – | 0,80 |
| Formación inicial | 0,20 | 0,30 | 0,10 | 0,60 |
| **Total (M€)** | **4,6** | **14,3** | **6,1** | **25,0** |

A partir de 2031 se añade **1 M€ al año para renovar la tecnología** (cámaras, ordenadores con GPU).

### 4.3 Costes de funcionamiento y lo que se pierde mientras se instala

- **Costes fijos anuales** (personal, alquiler, mantenimiento, licencias y marketing): 2,1 M€ en 2027, que suben a **7,2–7,3 M€** con el hub a pleno rendimiento. En 2030 se reparten así: 100 personas × 42.000 € = 4,2 M€; alquiler, mantenimiento y energía, 1,4 M€; licencias y nube, 0,6 M€; marketing, 1,0 M€.
- **Lo que se pierde mientras se instala: 1,6 M€ en total (2027–2029).** Incluye:
  - la curva de aprendizaje (al principio, más piezas van a revisión manual);
  - horas del personal en formación;
  - pruebas y calibración de las máquinas;
  - el espacio que se deja de usar en Kladno para otras cosas.
- **No hay que parar ninguna fábrica**, porque es un proceso nuevo que corre en paralelo.

### 4.4 Cuánto se gana o se ahorra

**Economía de un kilo recogido (escenario base):**

| Concepto | €/kg |
|---|---:|
| Venta de piezas y sets (75 % del kilo × 30 €) | +22,50 |
| Margen de las ventas extra gracias al crédito | +2,00 |
| Crédito al usuario | −5,00 |
| Logística de entrada | −2,00 |
| Lavado y energía | −0,60 |
| Envío y comisiones de venta | −1,50 |
| Gestión del material rechazado | −0,20 |
| Canibalización (10 % de las ventas) | −2,25 |
| **Margen de contribución** | **≈ +13 €/kg** |

Contamos el crédito a su valor nominal (5 €), aunque a LEGO le cuesta menos porque el cliente lo canjea por productos LEGO. **El cálculo es conservador.**

**Otros beneficios difíciles de pasar a euros:**
- datos de uso real para diseño;
- pasaporte digital listo antes de que sea obligatorio;
- imagen de marca;
- un canal de entrada más barato para familias que hoy no pueden pagar LEGO nuevo.

### 4.5 Cuenta de resultados del proyecto, ROI y plazo de recuperación (escenario base, M€)

| Año | Toneladas (recogidas + servicio) | Ingresos | Costes variables + canibalización | Fijos + transición | **EBITDA** | Inversión | Flujo del año | **Acumulado** |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| 2027 | 60 + 0 | 1,5 | 0,7 | 2,6 | **−1,8** | 4,6 | −6,4 | −6,4 |
| 2028 | 350 + 20 | 8,8 | 4,1 | 5,6 | **−0,9** | 14,3 | −15,2 | −21,6 |
| 2029 | 800 + 80 | 20,4 | 9,3 | 6,9 | **+4,2** | 6,1 | −1,9 | −23,5 |
| 2030 | 1.050 + 120 | 26,9 | 12,2 | 7,2 | **+7,5** | 0,0 | +7,5 | −16,0 |
| 2031 | 1.150 + 150 | 29,7 | 13,4 | 7,3 | **+9,0** | 1,0 | +8,0 | −8,0 |
| 2032 | 1.200 + 150 | 30,9 | 14,0 | 7,3 | **+9,6** | 1,0 | +8,6 | **+0,7** |
| **Total** | | **118,1** | | | **27,7** | **27,0** | | |

**Indicadores:**
- **Plazo de recuperación (payback): ≈ 6 años.** La inversión se recupera a finales de 2032.
- **ROI a 6 años** = (27,7 − 27,0) / 27,0 ≈ **+3 %**, es decir, a los 6 años se queda en tablas.
- **ROI a 10 años (vida útil de la planta)** = (66,3 − 31,0) / 31,0 ≈ **+114 %**.
- **VAN a 10 años** (tasa de descuento del 8 %) ≈ **+14 M€**.

*Fórmula usada: ROI = (beneficio acumulado − inversión) / inversión. Tomamos el EBITDA como beneficio, antes de impuestos y amortizaciones, para simplificar.*

### 4.6 Escenarios

| Escenario | Hipótesis | Payback | ROI a 10 años | VAN a 10 años (8 %) |
|---|---|---|---|---|
| **Pesimista** | −30 % de volumen y 24 €/kg | No se recupera | Negativo | −25 M€, **pero el piloto lo detecta y se para con una pérdida de ≈6,4 M€** |
| **Base** | Tabla anterior | ≈ 6 años | +114 % | +14 M€ |
| **Optimista** | +20 % de volumen y 34 €/kg | ≈ 4 años | +291 % | +48 M€ |

> **Lectura:** el proyecto no es una mina de oro, pero es **rentable, de riesgo controlado gracias al piloto** y estratégico. Las dos variables que más pesan son **cuánta gente dona** y **a qué precio se vende**. Por eso el piloto mide justo esas dos.

### 4.7 ¿Puede pagarlo LEGO?

**Sí, sin problema.**
- Los 25 M€ de inversión son el **0,8 % de su beneficio operativo de 2025** (≈2.950 M€).
- El piloto (4,6 M€) es el **0,16 %**.
- LEGO está invirtiendo más de 1.500 M$ solo en la fábrica de Virginia y aumentó un 20 % su gasto en iniciativas de sostenibilidad en 2025 (dato).

---

## 5. Cambios en la empresa

### 5.1 Procesos: antes y después

| Proceso | ANTES (Replay / hoy) | DESPUÉS (LEGO Loop) |
|---|---|---|
| **Donar piezas** | Caja + etiqueta. No sabes qué mandas ni recibes nada. En España no se puede | Escaneas con la app, ves la estimación de valor, recibes crédito y entregas en tienda o en Correos |
| **Clasificar** | A mano, por grandes grupos | Visión artificial pieza a pieza, 25.000+ tipos, más del 99 % de acierto. Una persona solo revisa las dudas |
| **Control de calidad** | Inspección visual humana, sin registro | Visión artificial para grietas, decoloración y clones, con cada decisión registrada |
| **Destino de la pieza** | Todo a donación en cajas mezcladas | Un algoritmo decide el mejor destino: set recompuesto, pieza suelta, donación o reciclaje |
| **Inventario y venta** | No existe | Inventario en tiempo real conectado a BrickLink y Pick a Brick, con precio dinámico |
| **Información al comprador** | Ninguna | Pasaporte digital con QR: origen, % reutilizado y CO₂ evitado |
| **Planificación y diseño** | Sin datos de lo que pasa con las piezas después de venderlas | Datos de roturas, sobrantes y faltantes para decidir qué fabricar |

**El viaje de una pieza (para contarlo en la presentación):**
1. Un loro de un set de Piratas de 1989 lleva 30 años en un trastero de Valladolid.
2. Su dueña lo escanea con la app junto a 6 kg de piezas y recibe 30 € de crédito.
3. Lo deja en la tienda LEGO de Madrid.
4. En el Brick Hub, la IA lo reconoce en 0,3 segundos ("pieza 2546, verde").
5. Pasa el control de calidad y se lava.
6. Un fan alemán lo compra en BrickLink para completar su galeón.
7. La caja lleva un QR que cuenta toda su historia.

### 5.2 Recursos humanos

**Plantilla del programa en 2030: ≈100 personas (Madrid 25, Kladno 70, equipo digital 5)**

| Puesto | Tipo | Nº (2030) | Formación |
|---|---|---:|---|
| Operador/a de línea de clasificación | **Nuevo** | 33 | 4 semanas + certificación interna |
| Técnico/a de lavado y preclasificación | **Nuevo** | 12 | 1 semana + higiene de juguetes |
| Inspector/a de calidad ("humano en el bucle") | **Nuevo** | 15 | 3 semanas: catálogo de piezas, defectos, clones |
| Técnico/a de mantenimiento mecatrónico | **Nuevo** | 8 | 6 semanas con el socio tecnológico |
| Montaje de sets y logística | **Nuevo** | 18 | 2 semanas |
| Ingeniero/a de visión artificial y datos | **Nuevo** | 5 | Especialización en IA (entrenamiento continuo del modelo) |
| Jefes de planta y de turno | **Nuevo** | 9 | Liderazgo y gestión del cambio |

**Puestos que cambian (no se crean ni se destruyen):**

| Puesto | Cómo cambia |
|---|---|
| **Dependientes de las tiendas LEGO** | Recogen y pesan donaciones y ayudan con la app (formación de 1 día) |
| **Atención al cliente** | Resuelve dudas y reclamaciones sobre créditos |
| **Equipos de BrickLink y Pick a Brick** | Gestionan stock nuevo y usado a la vez |
| **Planificadores de producción y diseñadores de materiales** | Usan los datos de retorno para decidir |

**Puestos que desaparecen:**
- En Europa no se pierde ningún puesto de LEGO, porque este proceso no existía.
- Donde sí se sustituye trabajo manual es en la **clasificación manual de Replay** (EE. UU., Canadá, Reino Unido), que hoy hacen socios externos. Cuando se migre (fase 3), a esas personas se les ofrecerá **recolocación** como inspectores de calidad o en el futuro hub de Virginia, con formación pagada.
- También desaparecen tareas (no personas), como la tasación y el inventario manuales.

**Despidos y reubicaciones:**
- **Compromiso de cero despidos.**
- El 50 % de las plazas del hub de Kladno se ofrecen **primero a la plantilla actual** de la fábrica (movilidad interna voluntaria).
- Los turnos de noche se pactan con los representantes de los trabajadores.

**Cómo conseguir que la plantilla acepte el cambio (plan en 5 pasos):**
1. **Explicar el porqué.** Reuniones abiertas con la historia y los datos: *"el ladrillo más sostenible es el que ya existe"*.
2. **Diseñar el proceso con la plantilla usando LEGO® SERIOUS PLAY®,** el método de talleres que inventó la propia LEGO. Los operarios y dependientes construyen con ladrillos cómo sería su puesto ideal. Usar LEGO para digitalizar LEGO: nivel friki máximo.
3. **Formación por niveles:**
   - e-learning de 2 h para toda la plantilla afectada;
   - 1 día para tiendas;
   - 4–6 semanas y certificación "Brick Hub Operator" para operarios y técnicos.
4. **"Brick Champions".** Un embajador en cada tienda y cada turno, un canal de sugerencias y un incentivo ligado a los KPIs de calidad.
5. **Medir y celebrar.** Encuestas de clima, rotación y tasa de errores. Se celebran hitos (la pieza 100 millones clasificada…).

**Gestión del cambio externa:**
- Los **vendedores de BrickLink** pueden temer que LEGO les haga la competencia.
- **Solución:** la tienda de LEGO es un vendedor más, sin ventaja en el buscador, y el plan se consulta antes con la comunidad a través del **LEGO Ambassador Network**.

---

## 6. Impacto en la empresa

### 6.1 Balance final

| Dimensión | Impacto previsto (2032) |
|---|---|
| **Económico** | Nueva línea de negocio de **≈31 M€/año de ingresos** y **≈9,6 M€/año de EBITDA**. Inversión recuperada en ≈6 años. ROI a 10 años ≈ +114 %. Es pequeño comparado con LEGO (0,3 % de sus ventas), pero rentable y ampliable a EE. UU. y Asia |
| **Clientes** | ≈**200.000 hogares al año** donan (1.200 t ÷ 6 kg). Sets de segunda vida **40–50 % más baratos**, así que llegan familias que hoy no pueden pagar LEGO nuevo. Los fans adultos consiguen piezas descatalogadas y un servicio de clasificación |
| **Trabajadores** | ≈**100 empleos directos nuevos**, cero despidos, nuevas competencias digitales (IA, mecatrónica, datos) |
| **Imagen de marca** | LEGO pasa de "juguete de plástico" a "juguete circular". Buena historia para prensa y redes. **Riesgo:** acusaciones de *greenwashing* si se exagera, así que se publican datos auditados |
| **Medio ambiente** | **1.200 t/año de piezas siguen en uso** (≈650 millones de piezas). Se evitan **≈1.900–3.700 t de CO₂e al año** (3,1 kg CO₂e por kg de ABS virgen no fabricado (dato), según si cada pieza reutilizada sustituye a una nueva al 50 % o al 100 %). Siendo honestos, es **solo el 0,1–0,2 % de la huella de LEGO**. Además, el 15 % dañado se recicla en vez de acabar en el vertedero |

### 6.2 Riesgos y cómo se controlan

| Riesgo | Prob. | Impacto | Cómo se controla |
|---|---|---|---|
| **Poca gente dona** | Media | Alto | Piloto con go/no-go, crédito atractivo, recogida en tiendas y en Correos |
| **Canibalización** (se venden menos productos nuevos) | Media | Medio | Ya se descuenta en los cálculos. Se prioriza lo descatalogado y los sets antiguos, y se mide en el piloto |
| **La tecnología no alcanza la precisión o la velocidad** | Baja-media | Alto | Tecnología ya probada (99 %), humano en el bucle y entrenamiento con modelos 3D oficiales |
| **Higiene y seguridad** (juguete usado para niños) | Media | Muy alto | Lavado industrial, inspección, cumplimiento del Reglamento (UE) 2025/2509. Para menores de 3 años (DUPLO), controles reforzados |
| **Fraude:** envío de clones o de otros objetos para cobrar crédito | Media | Medio | La IA detecta clones y el crédito definitivo se da después del pesaje y la verificación |
| **Enfado de los vendedores de BrickLink** | Media | Medio | LEGO es un vendedor más, sin trato preferente, y se consulta antes a la comunidad |
| **Acusación de *greenwashing*** | Baja | Alto | Informar solo de datos medidos y auditados |
| **Privacidad** (fotos de los usuarios) | Baja | Medio | Procesamiento en el propio móvil y borrado inmediato (RGPD) |
| **Depender de una startup pequeña** | Media | Medio | Participación en el socio o licencia con acceso al código, y equipo propio de IA |

### 6.3 ¿Cumple los objetivos del punto 1? (cierre del círculo)

| Objetivo (punto 1) | Qué consigue LEGO Loop en 2032 | ¿Cumple? |
|---|---|---|
| **O1 · Crecer de forma rentable** | +31 M€/año de ingresos, EBITDA positivo desde 2029, inversión recuperada en ≈6 años | ✅ **Sí** (modesto en tamaño, pero rentable) |
| **O2 · Sostenibilidad** | 1.200 t/año de plástico que no hay que fabricar y ≈1.900–3.700 t CO₂e/año evitadas (0,1–0,2 % de su huella) | 🟡 **Parcialmente**: ayuda y demuestra un modelo circular que se puede replicar, pero **por sí solo no consigue el −37 %** |
| **O3 · Fans y experiencia del cliente** | ≈200.000 hogares al año, sets más baratos, piezas descatalogadas y servicio para fans adultos | ✅ **Sí** |
| **O4 · Tecnología digital y cadena de suministro** | IA propia, datos pieza a pieza integrados con SAP, BrickLink y Pick a Brick | ✅ **Sí** |
| **O5 · Anticiparse a la regulación** | Pasaporte digital funcionando en 2029, antes de la obligación de agosto de 2030 | ✅ **Sí** |

### 6.4 Conclusión

- LEGO quiere **crecer y a la vez contaminar menos**, y hoy esas dos cosas chocan: cuanto más vende, más plástico nuevo necesita.
- LEGO Loop no resuelve la paradoja entera, pero sí ataca una parte que nadie está atacando: **las piezas que ya existen**.
- El problema era de **información** (saber qué pieza es cada pieza entre 25.000 tipos) y por eso la solución es **digital**: visión artificial, datos y pasaporte digital.
- Es **realista**: la tecnología ya funciona en una startup europea y LEGO tiene patentes propias.
- Es **asequible**: menos del 1 % del beneficio de un año.
- Tiene el **riesgo controlado**: un piloto de 4,6 M€ decide si se escala.
- Cumple 4 de los 5 objetivos estratégicos y contribuye honestamente al quinto.

---

## Anexo A. Alternativas que se valoraron y se descartaron

| Empresa | Idea | Por qué se descartó |
|---|---|---|
| **PortAventura World** | Gemelo digital del parque, IA para colas y sensores para el mantenimiento predictivo de las atracciones | Menos datos públicos, y las colas virtuales ya existen (Disney) |
| **Games Workshop (Warhammer)** | Fábrica inteligente y preventas antibots | Friki máximo, pero muy nicho, con pocos datos en español y difícil de explicar en clase |
| **Renfe** | Mantenimiento predictivo con gemelo digital | Tema muy visto y muy político (reparto Renfe/Adif) |

## Anexo B. Glosario friki

| Término | Significado |
|---|---|
| **AFOL** | *Adult Fan of LEGO*: fan adulto de LEGO |
| **BrickLink** | Mercado online de piezas LEGO, propiedad de LEGO desde 2019 |
| **Pick a Brick** | Servicio de LEGO para comprar piezas sueltas |
| **Elemento / Design ID** | Código único de cada pieza (forma + color) |
| **Minifigura** | El muñequito LEGO; es lo que más vale en los lotes usados |
| **Clon** | Pieza de otra marca compatible con LEGO (Lepin, Mould King, Cobi…) |
| **CNN** | Red neuronal convolucional, el tipo de IA que reconoce imágenes |
| **Humano en el bucle** | Sistema en el que la IA decide lo fácil y una persona revisa lo dudoso |
| **Balance de masas** (*mass balance*) | Método para contabilizar el material renovable que se mezcla con el fósil en la fábrica del proveedor |
| **DPP** | *Digital Product Passport*, el pasaporte digital de producto de la UE |

## Anexo C. Ideas para la presentación

1. **Demostrar el problema en directo.** Traed una bolsa de LEGO mezclado y pedid a un compañero que encuentre una pieza concreta en 30 segundos. Así se entiende por qué clasificar a mano no escala.
2. **Enseñar la app Brickit** escaneando un montón de piezas (es gratis). Es la "versión casera" del área A.
3. **Poner 30 segundos del vídeo de la *Universal LEGO Sorting Machine*** de Daniel West.
4. **Contar el viaje de la pieza** (el loro pirata de 1989) para explicar el antes y el después.
5. **Cerrar con la tabla 6.3**, la que conecta con el punto 1.

## Anexo D. Fuentes

**Datos de la empresa (resultados y fábricas):**
- LEGO. Resultados 2025: https://www.lego.com/en-us/aboutus/news/2026/march/the-lego-group-delivers-record-results-in-2025-driven-by-strong-brand-and-innovative-portfolio
- LEGO. Informe Anual 2025 (PDF): https://www.lego.com/cdn/cs/aboutus/assets/blte543dd46714c9226/The_LEGO_Group_2025_Annual_Report.pdf
- Toy World Magazine. Resultados 2025: https://toyworldmag.co.uk/lego-reveals-2025-full-year-results/
- Fortune. Fábrica de Vietnam: https://www.fortune.com/europe/2025/04/09/lego-1-billion-factory-vietnam-demand-brick-toys
- Supply Chain Digital. Virginia y ampliaciones: https://supplychaindigital.com/news/lego-group-supply-chain-expansion
- Brick Fanatics. Más de 1.100 tiendas: https://www.brickfanatics.com/lego-stores-reached-four-digits-beyond-in-1hy-2026

**Sostenibilidad y emisiones:**
- LEGO. Materiales sostenibles: https://www.lego.com/en-us/sustainability/sustainable-materials
- ESG Today. 52 % renovable/reciclado: https://www.esgtoday.com/lego-surpasses-50-renewable-and-recycled-content-in-bricks/
- LEGO. Acción climática: https://www.lego.com/en-us/sustainability/climate-action
- DitchCarbon. Emisiones de LEGO: https://ditchcarbon.com/organizations/lego
- CNN. LEGO abandona el rPET (2023): https://edition.cnn.com/2023/09/25/business/lego-abandons-recycled-plastic-bottle-bricks

**LEGO Replay:**
- LEGO. Página de Replay: https://www.lego.com/en-us/sustainability/replay
- Good News Network. Cinco años de Replay: https://www.goodnewsnetwork.org/400000-kids-now-have-legos-to-play-with-thanks-to-parents-donating-1-2-mil-pounds-of-used-bricks-so-far/
- Brick Fanatics. Replay en Reino Unido: https://www.brickfanatics.com/lego-replay-trial-launches-in-the-uk

**BrickLink:**
- LEGO Ambassador Network. Compra de BrickLink: https://lan.lego.com/news/overview/the-lego-group-acquires-bricklink/

**Tecnología de clasificación y reconocimiento:**
- heise. Sort A Brick: https://www.heise.de/en/news/Sort-A-Brick-automatically-assembles-used-building-blocks-into-sets-10792840.html
- Robotics & Automation News. Sort A Brick: https://roboticsandautomationnews.com/2025/10/20/startup-sort-a-brick-looking-to-raise-e3-million-to-scale-up-worlds-first-automated-lego-sorting-conveyor/95652/
- Daniel West. Universal LEGO Sorting Machine: https://medium.com/data-science/a-high-speed-computer-vision-pipeline-for-the-universal-lego-sorting-machine-253f5a690ef4
- Patente de LEGO de reconocimiento con CNN: https://patents.google.com/patent/US10213692B2/en
- App Brickit: https://brickit.app/

**Regulación:**
- SGS. Reglamento (UE) 2025/2509: https://www.sgs.com/en-us/news/2025/12/safeguards-18725-eu-toy-safety-regulation-2025-2509-published
- InfoDPP. Pasaporte digital de juguetes (agosto de 2030): https://infodpp.eu/en/industries/toys/
- Ecomaison. Responsabilidad del productor de juguetes en Francia: https://ecomaison.com/en/filiere-jouets/

**Precios y huella del material:**
- brick'em. Precio del LEGO usado a granel: https://brickem.io/blog/lego-bulk-price-per-pound
- BAGE Plastics. Huella de carbono del ABS virgen: https://bage-plastics.com/sustainable-recycled-granules-by-bage-plastics-with-excellent-carbon-footprint/
