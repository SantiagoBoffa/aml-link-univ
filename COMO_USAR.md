# 🚀 PUSH Y USAR - 3 Pasos

## 1️⃣ Push a GitHub:

```bash
cd /Users/santiagoboffa/Documents/work/Mutual/universal-links-config/vercel-reset-password

git push
```

**Si pide password:** Usá tu token de GitHub (no tu contraseña)

---

## 2️⃣ Vercel hace Auto-Deploy

Ve a: https://vercel.com/dashboard

Verás que está deployando automáticamente. Esperá 30 segundos.

**Copiá tu URL**, ejemplo: `https://aml-link-univ.vercel.app`

---

## 3️⃣ Actualizar Backend:

**Archivo:** `aml-be/src/extensions/users-permissions/controllers/auth.ts`

**Línea 40:**
```typescript
const baseUrl = process.env.RESET_PASSWORD_URL || 'https://TU-URL-VERCEL.vercel.app';
```

**Reiniciar:**
```bash
cd /Users/santiagoboffa/Documents/work/Mutual/aml-be
docker compose restart
```

---

## ✅ PROBAR:

1. Solicitar reset password desde la app
2. Revisar email → Debería tener: `https://tu-url.vercel.app/reset-password?token=XXX`
3. Abrir desde el celular → Debería intentar abrir la app automáticamente

---

## 📱 ¿Qué hace la página?

```
Email: https://tu-url.vercel.app/reset-password?token=ABC123
       ↓
Página se abre
       ↓
JavaScript hace: window.location.href = "amlmovil://reset-password?token=ABC123"
       ↓
Se abre la app AML con el token
```

¡Eso es todo! 🎉

