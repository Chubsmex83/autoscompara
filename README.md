# AutoCompara MX 🇲🇽

Herramienta de comparación de vehículos disponibles en México. Aplicación web de una sola página, sin dependencias externas ni servidor requerido.

## Archivo

```
autocompara-mx.html
```

Abre el archivo directamente en cualquier navegador moderno (Chrome, Edge, Firefox, Safari) — incluyendo navegadores móviles en iOS y Android.

**Repositorio:** https://github.com/Chubsmex83/autoscompara

---

## Funcionalidades

### Filtros (menú superior)
- **Categoría:** Todos / Sedán / SUV / Pickup / Hatchback / Minivan / 🔋 Híbrido / ⚡ Eléctrico
  - El filtro **🔋 Híbrido** detecta automáticamente todos los vehículos con motor híbrido, PHEV, e-Power, E-Tech, DHT o mild hybrid, sin importar su categoría de carrocería
  - El filtro **⚡ Eléctrico** muestra únicamente vehículos de batería pura (BEV)
- **Precio:** Todos / -$300k / $300k–$600k / $600k–$900k / +$900k
- Los filtros de categoría y precio se combinan y actúan en tiempo real
- En móvil los filtros se deslizan horizontalmente en una sola fila

### Selección de vehículos
- Hasta **4 vehículos** simultáneos para comparar
- Búsqueda en tiempo real por marca o modelo, ordenada alfabéticamente
- Al seleccionar un auto se carga automáticamente su **fotografía real** desde Wikipedia
- Tarjeta con foto, categoría, versión, precio en MXN y nivel de confiabilidad
- El dropdown detecta el espacio disponible y abre hacia arriba si es necesario

### Tabla comparativa
Agrupa las especificaciones en 8 secciones con foto del vehículo en cada columna:
1. Precio y Categoría
2. Motor y Rendimiento
3. Capacidad y Practicidad
4. Seguridad y Garantía
5. Confiabilidad y Mantenimiento
6. Equipamiento Destacado
7. Ventajas y Desventajas
8. Red de Distribuidores

- El mejor valor de cada fila se resalta en **verde** y el peor en **rojo**
- En móvil muestra indicador "← Desliza para ver todos los autos →"

### Modo compacto al comparar
Al presionar "Comparar", el selector se colapsa en una barra delgada con chips de los vehículos seleccionados, liberando espacio para la tabla. Botón "✏️ Cambiar selección" para regresar al selector completo.

### Fotografías de vehículos
- Se cargan automáticamente desde la API de Wikipedia al seleccionar cada auto
- Aparecen con animación fade-in en las tarjetas de slot y en los encabezados de la tabla comparativa
- Si Wikipedia no tiene foto del modelo, se muestra un emoji representativo como respaldo
- Las imágenes se cachean: no se vuelven a descargar si seleccionas el mismo auto de nuevo
- Requiere conexión a internet solo para las fotos; el resto funciona offline

### Sistema de recomendación
Algoritmo de scoring con 5 criterios ponderados:

| Criterio | Peso |
|---|---|
| Relación precio-valor | 25% |
| Seguridad | 20% |
| Eficiencia de combustible | 20% |
| Desempeño (HP + Torque) | 20% |
| Practicidad (cajuela + pasajeros) | 15% |

Muestra tarjeta ganadora, barras de puntuación por criterio y etiquetas de uso ideal.

---

## Dataset

**204 vehículos** con precios MSRP oficiales México 2025–2026.

### Tipos de propulsión incluidos

| Tipo | Descripción |
|---|---|
| **Gasolina** | Motor de combustión interna tradicional |
| **Híbrido (HEV)** | Híbrido sin enchufe, self-charging |
| **Híbrido enchufable (PHEV)** | Batería recargable + motor gasolina |
| **Eléctrico puro (BEV)** | Solo batería, cero emisiones |
| **e-Power / DHT / DM-i** | Variantes de sistemas híbridos de serie |

### Marcas incluidas

| Marca | Modelos representativos |
|---|---|
| **Acura** | RDX, MDX, MDX Type S PHEV |
| **Alfa Romeo** | Tonale, Stelvio |
| **Audi** | A3, Q3, Q5, Q5 PHEV, Q7 PHEV, Q4 e-tron |
| **BAIC** | X55 Pro |
| **BMW** | Serie 3, X1, X3, 330e PHEV, X3 PHEV, X5 PHEV, iX1, i4 |
| **BYD** | Seal, Atto 3, Dolphin, Han, Tang EV, Tang DM-i PHEV, Shark PHEV |
| **Changan** | CS55 Plus, Uni-T |
| **Chirey** | Tiggo 7 Pro, Tiggo 8 Pro |
| **Chevrolet** | Onix, Trax, Equinox, Colorado, Silverado, Tahoe, Equinox EV, Blazer EV |
| **CUPRA** | Formentor VZ |
| **Fiat** | Pulse, Strada |
| **Ford** | Ranger, Territory, Bronco Sport, Bronco, Maverick, Maverick Híbrido, F-150, F-150 PowerBoost Híbrido, F-150 Raptor, Explorer, Explorer PHEV, Escape Híbrido, Mustang, Mustang Mach-E |
| **Haval** | Jolion, H6, H6 HEV |
| **Honda** | CR-V, CR-V Híbrido, Civic, HR-V, ZR-V Híbrido, Pilot, Accord Híbrido |
| **Hyundai** | Accent, Elantra, Creta, Kona Híbrido, Tucson, Tucson Híbrido, Tucson PHEV, Santa Fe, Santa Fe Híbrido, Ioniq 5, Ioniq 6 |
| **Infiniti** | QX50, QX60 Híbrido |
| **Isuzu** | D-Max |
| **JAC** | JS4, E-JS4 |
| **Jaguar** | F-Pace |
| **Jeep** | Compass, Compass 4xe PHEV, Wrangler 4xe, Renegade, Grand Cherokee, Grand Cherokee 4xe PHEV, Grand Cherokee L, Grand Cherokee L 4xe PHEV, Gladiator, Avenger |
| **JMC** | Vigus Pro |
| **Kia** | Rio, Niro Híbrido, Niro PHEV, Niro EV, Sportage, Sportage Híbrido, Sorento Híbrido, Sorento PHEV, EV6, Carnival |
| **Land Rover** | Discovery Sport PHEV, Range Rover Evoque, Defender, Defender PHEV, Range Rover PHEV |
| **Lexus** | UX 250h, NX, NX 350h, NX 450h+ PHEV, RX, RX 350h, ES 300h |
| **Lincoln** | Corsair, Navigator, Aviator PHEV |
| **Mazda** | Mazda3, CX-5, CX-30, CX-50, CX-90, CX-90 PHEV |
| **Mercedes-Benz** | GLA, Clase C, C300e PHEV, GLC, GLC300e PHEV, GLE PHEV, EQA, EQB |
| **MG** | ZS, ZS EV, HS, MG4 Electric |
| **MINI** | Cooper S, Cooper SE, Countryman PHEV |
| **Mitsubishi** | Outlander, Outlander PHEV, Eclipse Cross PHEV, L200 |
| **Nissan** | Versa, Sentra, Kicks, Kicks e-Power, NP300, X-Trail e-Power, Frontier, Ariya |
| **Omoda** | 5 |
| **Peugeot** | 2008, 3008, 3008 E-Tech Híbrido, e-2008 |
| **Porsche** | Macan, Taycan, Cayenne E-Hybrid |
| **RAM** | 700, 1500, 2500 |
| **Renault** | Duster, Koleos, Austral E-Tech, Captur PHEV, Megane E-Tech |
| **SEAT** | Ibiza, Arona, Ateca |
| **Subaru** | Forester, Outback, Crosstrek PHEV |
| **Suzuki** | Jimny, Vitara |
| **Toyota** | Corolla, Corolla Cross Híbrido, Camry Híbrido, Prius PHEV, Crown Híbrido, RAV4 Híbrido, RAV4 Prime PHEV, Venza Híbrido, Highlander Híbrido, Sienna Híbrido, Hilux, Tacoma, Tundra, bZ4X |
| **Volkswagen** | Polo, Jetta, T-Cross, Taos, Tiguan, Tiguan eHybrid PHEV, ID.4 |
| **Volvo** | XC40, C40 Recharge, EX30, XC60, XC60 T8 PHEV, XC90 T8 PHEV |

Cada vehículo incluye: motor, potencia, torque, transmisión, tracción, consumo ciudad/carretera, cajuela, capacidad de arrastre, pasajeros, calificación LATINNCAP, garantía, costo de mantenimiento anual estimado, nivel de confiabilidad (1–5), fallas conocidas frecuentes, equipamiento destacado, pros, contras y cobertura de red de distribuidores.

---

## Diseño móvil

- **Responsive completo:** 4 columnas en desktop → 2×2 en tablet y móvil
- Filtros en **scroll horizontal táctil** — una sola fila compacta, sin wrap
- Inputs con font-size 16px para evitar zoom automático en iOS
- Botones con área de toque mínima de 40px
- Dropdown inteligente: detecta espacio disponible y abre hacia arriba si es necesario
- Indicador visual "← Desliza →" en la tabla comparativa en pantallas pequeñas
- Zoom con dedos habilitado (sin restricciones de accesibilidad)
- Verificado en: Chrome, Safari iOS, Samsung Internet, Firefox Mobile

---

## Tecnología

- **HTML5 + CSS3 + JavaScript vanilla** — sin frameworks, sin build tools, sin backend
- **Google Fonts** (Inter) vía CDN
- **Wikipedia REST API** para fotografías de vehículos (gratuita, Creative Commons)
- Funciona **offline** — solo las fotos y fuentes requieren internet
- Hoja de estilos de impresión incluida (`@media print`)

## Requisitos

Ninguno. Solo un navegador moderno — en computadora o celular.
