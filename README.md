# PrintContainer.js

A lightweight JavaScript utility for printing specific HTML containers while **preserving existing page CSS** and adding **print-only control** such as scaling and element visibility.

Designed for:
- Invoices
- Bills
- ERP systems
- Admin panels
- Reports & dashboards

---

## ✨ Features

- ✔ Print a specific container  
- ✔ Preserve original page styles  
- ✔ Print scale control (10%–100%)  
- ✔ Hide elements only during print  
- ✔ Show print-only elements  
- ✔ Chrome / Edge / Firefox compatible  
- ✔ No DOM mutation  
- ✔ No dependencies  

---

## 📦 Installation

Copy `printContainer.js` into your project and include it:

```html
<script src="printContainer.js"></script>
````

---

## 🚀 Basic Usage

```js
PrintContainer('printArea');
```

---

## 🔍 Advanced Usage

### Scale Content

```js
PrintContainer('invoice', 80);
```

---

### Hide Elements During Print

```js
PrintContainer(
  'invoice',
  100,
  ['.btn', '.pagination', '[data-hide-print]']
);
```

---

### Show Print-Only Elements

```html
<div class="print-only d-none">Authorized Signature</div>
```

```js
PrintContainer(
  'invoice',
  100,
  [],
  ['.print-only']
);
```

---

### Full Control Example

```js
PrintContainer(
  'invoice',
  85,
  ['.btn', '.no-print'],
  ['.print-only', '#signature']
);
```

---

## 🧩 API Reference

### `PrintContainer(id, scale, hideSelectors, showSelectors)`

| Parameter       | Type       | Description                      |
| --------------- | ---------- | -------------------------------- |
| `id`            | `string`   | Container ID to print            |
| `scale`         | `number`   | Print scale (10–100)             |
| `hideSelectors` | `string[]` | Elements hidden only in print    |
| `showSelectors` | `string[]` | Elements forced visible in print |

---

## 🎨 CSS Preservation Strategy

This utility:

* Copies all `<style>` tags
* Copies all linked stylesheets
* Adds only minimal print-safe CSS
* Does **not** override fonts, layout, or colors

This ensures the printed output looks identical to the screen version unless explicitly changed.

---

## 🖨 Browser Support

| Browser | Support           |
| ------- | ----------------- |
| Chrome  | ✅                 |
| Edge    | ✅                 |
| Firefox | ✅ (fallback used) |
| Safari  | ⚠ Limited         |

---

## 📄 License

MIT License

---

## 👨‍💻 Author

**Anmol Singh**
GitHub: [https://github.com/anmolscripts](https://github.com/anmolscripts)

---

## ⭐ Support

If this utility helps you, please ⭐ star the repository.