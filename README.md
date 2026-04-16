# 🍬 Control Empresarial Alfajores

Sistema web de gestión de stock, ventas y pagos para el negocio de alfajores.
Desarrollado con HTML, JavaScript y Firebase Firestore como base de datos en tiempo real.

---

## 🚀 Funcionalidades

- 📦 **Gestión de stock** — Registra pedidos por sabor, cantidad y precio
- 🛒 **Registro de ventas** — Descuenta stock automáticamente al vender
- 👤 **Cliente por venta** — Registra a quién se le vendió cada pedido
- 💵 **Método de pago** — Distingue entre pagos en efectivo y por transferencia
- ✅ **Estado de pago** — Marca ventas como "Realizado" o "No Realizado"
- 📅 **Ventas por día** — Agrupa automáticamente las ventas por fecha
- 📊 **Resumen general** — Muestra totales por vendedor y por método de pago
- 🔄 **Tiempo real** — Todos los datos se sincronizan automáticamente con Firebase

---

## 🧑‍💼 Vendedores

| Vendedor | Rol |
|----------|-----|
| Dann     | Vendedor |
| Gio      | Vendedor |

---

## 🍡 Sabores disponibles

- Cheescake de limón / maracuyá
- Lulada, Banana Pudding, Franui
- Milo Crunch, Coffe Toffee, Brownie
- Caramelo Salado, Dulce de Leche
- Snowreo, Chocolatoso, Red Velvet, Snickers

---

## 🛠️ Tecnologías usadas

| Tecnología | Uso |
|------------|-----|
| HTML5 + CSS3 | Interfaz de usuario |
| JavaScript (ES6+) | Lógica del negocio |
| Firebase Firestore | Base de datos en tiempo real |
| Firebase Hosting | Despliegue web |

---

## ⚙️ Instalación y uso local

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/alfajores-gyd.git
   ```
2. Abre el archivo `index.html` con **Live Server** desde VS Code
   - Clic derecho → *Open with Live Server*

> ⚠️ No abras el archivo directamente con doble clic en el explorador,
> ya que los módulos de Firebase requieren un servidor local (http://).

---

## 🌐 Despliegue con Firebase Hosting

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

El sitio quedará disponible en:
`https://alfajores-gyd.web.app`

---

## 📁 Estructura del proyecto
alfajores-gyd/
│
├── index.html # Aplicación completa (HTML + CSS + JS)
└── README.md # Documentación del proyecto

texto

---

## 📄 Colecciones en Firestore

| Colección | Campos principales |
|-----------|--------------------|
| `stock`   | sabor, cantidad, precio |
| `ventas`  | sabor, cantidad, vendedor, cliente, metodoPago, estadoPago, total, fecha |

---

## 📌 Notas

- Los totales del resumen **solo cuentan ventas con estado "Realizado"**
- Al eliminar una venta, el stock se **restaura automáticamente**
- La fecha de cada venta se genera con `serverTimestamp()` de Firebase

---

*Desarrollado para uso interno del negocio Alfajores G&D* 🍬
