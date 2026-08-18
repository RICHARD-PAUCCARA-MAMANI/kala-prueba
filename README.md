# ⛽ Grifos Kala — Panel de Operaciones

Panel de administración y control de ventas para estaciones de servicio **Grifos Kala**. Aplicación web completa con login, dashboard, gestión de trabajadores, registro de ventas y cierre de turno.

![React](https://img.shields.io/badge/React-18-61DAFB?style=flat&logo=react)
![Recharts](https://img.shields.io/badge/Recharts-2.x-4FB0A6?style=flat)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat&logo=javascript)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5)
![Responsive](https://img.shields.io/badge/Responsive-Mobile%20%26%20Desktop-4FB0A6?style=flat)

---

## 📸 Capturas de la interfaz

### 🔐 Pantalla de Login
Login seguro con selección de rol (Trabajador / Administrador), validación de campos y conexión cifrada HTTPS/TLS.

```
┌─────────────────────────────────┐
│         ⛽ GRIFOS KALA          │
│     Panel de operaciones        │
├─────────────────────────────────┤
│  [Trabajador] [Administrador]   │
│                                 │
│  Usuario:                       │
│  ┌─────────────────────────┐    │
│  │ ej. rhuaman             │    │
│  └─────────────────────────┘    │
│  Contraseña:                    │
│  ┌─────────────────────────┐    │
│  │ ••••••••           👁   │    │
│  └─────────────────────────┘    │
│                                 │
│  ┌─────────────────────────┐    │
│  │      Ingresar           │    │
│  └─────────────────────────┘    │
│                                 │
│  🔒 Conexión cifrada (HTTPS)    │
└─────────────────────────────────┘
```

### 📊 Panel de Administrador — Resumen
Dashboard con KPIs en tiempo real, gráficos de ventas semanales (Norte vs Sur), distribución de formas de pago y gestión de precios.

```
┌──────────────────────────────────────────────────┐
│  PRECIOS VIGENTES · Grifo Kala Norte             │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐       │
│  │ Diésel B5│  │Urea 32   │  │Gasolina  │       │
│  │ S/ 23.10 │  │ S/ 2.50  │  │S/ 19.90  │       │
│  └──────────┘  └──────────┘  └──────────┘       │
│                                                   │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────┐│
│  │ Ventas   │ │Galones   │ │Facturas  │ │Boletas│
│  │S/ 8,214  │ │  1,246   │ │   34     │ │  118 ││
│  └──────────┘ └──────────┘ └──────────┘ └──────┘│
│                                                   │
│  ┌─────────────────────┐ ┌──────────────────┐   │
│  │ 📊 Ventas grifo     │ │ 💳 Formas pago   │   │
│  │    (Barras 7 días)  │ │    (Pie chart)   │   │
│  │  ████  ████  ████   │ │     ◉ Efectivo   │   │
│  │  ████  ████  ████   │ │     ◉ Tarjeta    │   │
│  └─────────────────────┘ └──────────────────┘   │
└──────────────────────────────────────────────────┘
```

### 👥 Gestión de Trabajadores y Turnos
Edición de horarios semanales por trabajador con toggle libre/trabaja, horarios de entrada y salida por día.

```
┌──────────────────────────────────────────────────┐
│  4 trabajadores registrados   [+ Añadir]         │
│                                                   │
│  ┌──────────────────────────────────────────┐    │
│  │ RH Rosa Huamán · DNI 45871203           │    │
│  │ Grifo Kala Norte · usuario "rhuaman"     │    │
│  │ Lun 06:00-14:00 · Mar 06:00-14:00 · ... │    │
│  └──────────────────────────────────────────┘    │
│                                                   │
│  HORARIO SEMANAL:                                │
│  ┌─────┬─────┬─────┬─────┬─────┬─────┬─────┐   │
│  │ Lun │ Mar │ Mié │ Jue │ Vie │ Sáb │ Dom │   │
│  │06:00│06:00│06:00│06:00│06:00│Libre│Libre│   │
│  │14:00│14:00│14:00│14:00│14:00│     │     │   │
│  └─────┴─────┴─────┴─────┴─────┴─────┴─────┘   │
└──────────────────────────────────────────────────┘
```

### ⛽ Registro de Venta (Trabajador)
Formulario completo de registro de venta: selección de producto, cantidad por galones o soles, forma de pago, comprobante (boleta/factura) y resumen del turno.

```
┌──────────────────────────────────────────────────┐
│  1. SELECCIONA EL PRODUCTO                       │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐       │
│  │⛽ Diésel  │  │💧 Urea 32│  │⛽ Gasolina│       │
│  │ S/ 23.10 │  │ S/ 2.50  │  │ S/ 19.90 │       │
│  └──────────┘  └──────────┘  └──────────┘       │
│                                                   │
│  2. ¿CÓMO TE LO PIDEN?                           │
│  (●) Por galones  (○) Por soles                  │
│  ┌─────────────────────────────────────┐         │
│  │ 40                                 │         │
│  └─────────────────────────────────────┘         │
│  = S/ 924.00 en total                            │
│                                                   │
│  3. FORMA DE PAGO    4. COMPROBANTE              │
│  [💵][💳][📱][↔️]   (●) Boleta  (○) Factura     │
│                                                   │
│  Total a cobrar:        ┌───────────────────┐    │
│  S/ 924.00              │ Registrar venta ✓ │    │
│                         └───────────────────┘    │
│                                                   │
│  RESUMEN TURNO · Norte: S/ 1,585.00              │
│  3 ventas recientes                              │
└──────────────────────────────────────────────────┘
```

### 🔒 Cierre de Turno
Resumen por método de pago, validación de caja, cálculo de diferencia y reporte de turnos anteriores.

```
┌──────────────────────────────────────────────────┐
│  RESUMEN DEL TURNO · Grifo Kala Norte            │
│                                                   │
│  💵 Efectivo      S/ 462.00                      │
│  💳 Tarjeta       S/ 924.00                      │
│  📱 Yape          S/ 199.00                      │
│  ↔️  Transferencia S/   0.00                      │
│  ─────────────────────────────                   │
│  Total del turno  S/ 1,585.00                    │
│                                                   │
│  Efectivo contado en caja (S/):                  │
│  ┌─────────────────────────────────────┐         │
│  │ 462.00                             │         │
│  └─────────────────────────────────────┘         │
│  ✅ La caja cuadra exactamente.                   │
│                                                   │
│  ┌─────────────────────────────────────┐         │
│  │   Cerrar turno y enviar reporte     │         │
│  └─────────────────────────────────────┘         │
└──────────────────────────────────────────────────┘
```

---

## 🚀 Características

### 🔐 Autenticación
- Login con selección de rol (Trabajador / Administrador)
- Validación de campos obligatorios
- Mostrar/ocultar contraseña con icono toggle
- Mensajes de error con iconos descriptivos

### 📊 Dashboard de Administrador
- **KPIs**: Ventas del día, galones despachados, facturas y boletas emitidas
- **Gráfico de barras**: Ventas comparativas por grifo (Norte vs Sur) — últimos 7 días
- **Gráfico circular**: Distribución de formas de pago (Efectivo, Tarjeta, Yape, Transferencia)
- **Actualización de precios**: Editor inline para modificar precios de Diésel, Urea y Gasolina

### 👥 Gestión de Trabajadores
- Lista de trabajadores con iniciales, DNI, estación y usuario
- **Editor de horario semanal**: Toggle libre/trabaja por día con horarios de entrada/salida
- Agregar nuevos trabajadores con formulario completo
- Eliminar trabajadores con un clic

### ⛽ Registro de Ventas (Trabajador)
- Selección de producto (Diésel B5, Urea 32, Gasolina Regular)
- Entrada por galones/kilogramos o por soles
- Conversión automática entre unidades
- 4 métodos de pago: Efectivo, Tarjeta, Yape, Transferencia
- Comprobante: Boleta o Factura (con campos RUC y Razón Social)
- Historial de ventas recientes del turno

### 🔒 Cierre de Turno
- Resumen por método de pago
- Campo para contar efectivo en caja
- Cálculo automático de diferencia (sobrante/faltante)
- Confirmación de cierre con avance automático de fecha operativa
- Historial de turnos cerrados anteriores

### 📱 Diseño Responsive
- Adaptado para móvil (≤640px), tablet y escritorio
- Grids que se apilan automáticamente en pantallas pequeñas
- Horario semanal con scroll horizontal en móvil
- Header simplificado en dispositivos móviles
- Tabs con scroll horizontal

---

## 🛠️ Tecnologías

| Tecnología | Versión | Uso |
|---|---|---|
| **React** | 18 | Framework UI |
| **Recharts** | 2.12 | Gráficos de barras y circular |
| **Google Fonts** | — | Oswald, Inter, JetBrains Mono |
| **SVG Icons** | — | Iconos inline (estilo Lucide) |
| **CSS** | — | Media queries + estilos inline |

> **Nota**: No requiere build ni dependencias locales. Todo se carga desde CDN.

---

## 📁 Estructura del Proyecto

```
kala-prueba/
├── index.html          # Página completa (HTML + React + Recharts)
└── README.md           # Esta documentación
```

---

## ▶️ Ejecución

### Opción 1: Abrir directamente
```bash
# Simplemente abre index.html en tu navegador
open kala-prueba/index.html        # macOS
xdg-open kala-prueba/index.html    # Linux
start kala-prueba/index.html       # Windows
```

### Opción 2: Servidor local (recomendado para CORS)
```bash
cd kala-prueba
npx serve .
# → http://localhost:3000
```

### Opción 3: GitHub Pages
1. Ir a **Settings → Pages** en el repositorio
2. Seleccionar rama `main` y carpeta `/ (root)`
3. Guardar
4. Acceder a: `https://RICHARD-PAUCCARA-MAMANI.github.io/kala-prueba/`

---

## 👤 Usuarios de prueba

| Rol | Usuario | Contraseña |
|---|---|---|
| Trabajador | `rhuaman` | cualquiera |
| Trabajador | `jquispe` | cualquiera |
| Trabajador | `mcondori` | cualquiera |
| Trabajador | `emamani` | cualquiera |
| Administrador | `admin` | cualquiera |

> **Nota**: El login es una demo. En producción, las credenciales se validarían contra un backend con hash bcrypt/Argon2.

---

## 🎨 Paleta de Colores

| Color | Hex | Uso |
|---|---|---|
| Background | `#12161A` | Fondo principal |
| Panel | `#212930` | Tarjetas y paneles |
| Amber | `#E8A33D` | Acento principal, acciones |
| Teal | `#4FB0A6` | Gráfico Sur, estado activo |
| Green | `#8CAE5E` | Urea, estados positivos |
| Red | `#DD6259` | Errores, diferencias |
| Text | `#F3EFE6` | Texto principal |

---

## 📋 Funcionalidades pendientes (Roadmap)

- [ ] Backend con autenticación real (JWT / Sessions)
- [ ] Base de datos para persistencia de ventas y trabajadores
- [ ] Exportar reportes a PDF
- [ ] Modo oscuro / claro
- [ ] Notificaciones push para alertas de stock
- [ ] Historial de ventas por rango de fechas
- [ ] Control de inventario de combustible
- [ ] Generación automática de boletas/facturas SUNAT

---

## 📄 Licencia

MIT License — Uso libre para fines educativos y comerciales.

---

**Desarrollado con ⛽ para Grifos Kala**
