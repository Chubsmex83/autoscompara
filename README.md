# AutoCompara MX 🇲🇽

Herramienta de comparación de vehículos disponibles en México. Aplicación web de una sola página, sin dependencias externas ni servidor requerido.

## Archivo

```
autocompara-mx.html
```

Abre el archivo directamente en cualquier navegador moderno (Chrome, Edge, Firefox, Safari) — incluyendo navegadores móviles en iOS y Android.

---

## Funcionalidades

### Filtros (menú superior)
- **Categoría:** Todos / Sedán / SUV / Pickup / Hatchback / Minivan / 🔋 Híbrido / ⚡ Eléctrico
  - El filtro **Híbrido** detecta automáticamente todos los vehículos con motor híbrido, PHEV, e-Power, E-Tech, DHT o mild hybrid
  - El filtro **Eléctrico** muestra únicamente vehículos de batería pura (BEV)
- **Precio:** Todos / Menos de $300,000 / $300k–$600k / $600k–$900k / Más de $900,000
- Los filtros funcionan en combinación y actualizan el listado en tiempo real

### Selección de vehículos
- Hasta **4 vehículos** simultáneos para comparar
- Búsqueda en tiempo real por marca o modelo
- Ordenados alfabéticamente en el dropdown
- Tarjeta con emoji del tipo de vehículo, categoría, versión, precio en MXN y nivel de confiabilidad
- El dropdown se abre hacia arriba automáticamente si no hay espacio hacia abajo

### Tabla comparativa
Agrupa las especificaciones en 7 secciones:
1. Precio y Categoría
2. Motor y Rendimiento
3. Capacidad y Practicidad
4. Seguridad y Garantía
5. Confiabilidad y Mantenimiento
6. Equipamiento Destacado
7. Ventajas y Desventajas
8. Red de Distribuidores

- El mejor valor de cada fila se resalta en **verde** y el peor en **rojo**
- Desplazamiento horizontal en móvil con indicador visual

### Modo compacto al comparar
Al presionar "Comparar", el selector se colapsa en una barra delgada con chips de los vehículos seleccionados, liberando espacio para ver la tabla. Botón "✏️ Cambiar selección" para regresar.

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

**204 vehículos** con precios MSRP oficiales México 2025–2026, incluyendo:

### Tipos de propulsión
| Tipo | Descripción |
|---|---|
| Gasolina | Motor de combustión interna tradicional |
| Híbrido (HEV) | Híbrido sin enchufe (self-charging) |
| Híbrido enchufable (PHEV) | Carga eléctrica + motor gasolina |
| Eléctrico puro (BEV) | Solo batería, sin motor de combustión |
| e-Power / DHT / DM-i | Variantes de sistemas híbridos de serie |

### Marcas incluidas

| Marca | Modelos destacados |
|---|---|
| Acura | RDX, MDX, MDX Type S PHEV |
| Alfa Romeo | Tonale, Stelvio |
| Audi | A3, Q3, Q5, Q5 PHEV, Q7 PHEV, Q4 e-tron |
| BAIC | X55 Pro |
| BMW | Serie 3, X1, X3, 330e PHEV, X3 PHEV, X5 PHEV, iX1, i4 |
| BYD | Seal, Atto 3, Dolphin, Han, Tang EV, Tang DM-i PHEV, Shark PHEV |
| Changan | CS55 Plus, Uni-T |
| Chirey | Tiggo 7 Pro, Tiggo 8 Pro |
| Chevrolet | Onix, Trax, Equinox, Colorado, Silverado, Tahoe, Equinox EV, Blazer EV |
| CUPRA | Formentor |
| Fiat | Pulse, Strada |
| Ford | Ranger, Territory, Bronco Sport, Bronco, Maverick, Maverick Híbrido, F-150, F-150 PowerBoost, F-150 Raptor, Explorer, Explorer PHEV, Escape Híbrido, Mustang, Mustang Mach-E |
| Haval | Jolion, H6, H6 HEV |
| Honda | CR-V, CR-V Híbrido, Civic, HR-V, Pilot, ZR-V Híbrido, Accord Híbrido |
| Hyundai | Accent, Elantra, Creta, Kona Híbrido, Tucson, Tucson Híbrido, Tucson PHEV, Santa Fe, Santa Fe Híbrido, Ioniq 5, Ioniq 6 |
| Infiniti | QX50, QX60 Híbrido |
| Isuzu | D-Max |
| JAC | JS4, E-JS4 |
| Jaguar | F-Pace |
| Jeep | Compass, Compass 4xe PHEV, Wrangler 4xe, Renegade, Grand Cherokee, Grand Cherokee 4xe PHEV, Grand Cherokee L, Grand Cherokee L 4xe PHEV, Gladiator, Avenger |
| JMC | Vigus Pro |
| Kia | Rio, Niro Híbrido, Niro PHEV, Niro EV, Sportage, Sportage Híbrido, Sorento Híbrido, Sorento PHEV, EV6, Carnival |
| Land Rover | Discovery Sport PHEV, Range Rover Evoque, Defender, Defender PHEV, Range Rover PHEV |
| Lexus | UX 250h, NX, NX 350h, NX 450h+ PHEV, RX, RX 350h, ES 300h |
| Lincoln | Corsair, Navigator, Aviator PHEV |
| Mazda | Mazda3, CX-5, CX-30, CX-50, CX-90, CX-90 PHEV |
| Mercedes-Benz | GLA, Clase C, C300e PHEV, GLC, GLC300e PHEV, GLE PHEV, EQA, EQB |
| MG | ZS, ZS EV, HS, MG4 Electric |
| MINI | Cooper S, Cooper SE, Countryman PHEV |
| Mitsubishi | Outlander, Outlander PHEV, Eclipse Cross PHEV, L200 |
| Nissan | Versa, Sentra, Kicks, Kicks e-Power, NP300, X-Trail e-Power, Frontier, Ariya |
| Omoda | 5 |
| Peugeot | 2008, 3008, 3008 E-Tech Híbrido, e-2008 |
| Porsche | Macan, Taycan, Cayenne E-Hybrid |
| RAM | 700, 1500, 2500 |
| Renault | Duster, Koleos, Austral E-Tech, Captur PHEV, Megane E-Tech |
| SEAT | Ibiza, Arona, Ateca |
| Subaru | Forester, Outback, Crosstrek PHEV |
| Suzuki | Jimny, Vitara |
| Toyota | Corolla, Corolla Cross Híbrido, Camry Híbrido, Prius PHEV, Crown Híbrido, RAV4 Híbrido, RAV4 Prime PHEV, Venza Híbrido, Highlander Híbrido, Sienna Híbrido, Hilux, Tacoma, Tundra, bZ4X |
| Volkswagen | Polo, Jetta, T-Cross, Taos, Tiguan, Tiguan eHybrid PHEV, ID.4 |
| Volvo | XC40, XC40 C40 Recharge, EX30, XC60, XC60 T8 PHEV, XC90 T8 PHEV |

Cada vehículo incluye: motor, potencia, torque, transmisión, tracción, consumo ciudad/carretera, cajuela, capacidad de arrastre, pasajeros, calificación LATINNCAP, garantía, costo mantenimiento anual, nivel de confiabilidad, fallas conocidas, equipamiento, pros, contras y red de distribuidores.

---

## Diseño móvil

- **Responsive completo:** grilla 4 columnas en desktop → 2×2 en tablet/móvil
- Filtros de categoría y precio con **scroll horizontal táctil** en una sola fila
- Inputs con fuente 16px para evitar zoom automático en iOS
- Botones con área de toque mínima de 40px
- Dropdown que detecta espacio disponible y abre hacia arriba si es necesario
- Indicador "← Desliza →" en tabla comparativa en móvil
- Zoom con dedos habilitado (sin restricciones de accesibilidad)
- Compatible con Chrome, Safari, Samsung Internet, Firefox Mobile

---

## Tecnología

- HTML5 + CSS3 + JavaScript vanilla
- Sin frameworks, sin build tools, sin backend
- Google Fonts (Inter) vía CDN
- Funciona **offline** (solo Google Fonts requiere internet)
- Hoja de estilos de impresión incluida

## Requisitos

Ninguno. Solo un navegador moderno — en computadora o celular.
