# 🔐 AML Reset Password - Vercel

Página simple para manejar los links de recuperación de contraseña de la app AML.

---

## 🎯 ¿Qué hace?

Recibe links del email tipo:
```
https://tu-vercel.vercel.app/reset-password?token=ABC123
```

Y automáticamente intenta abrir la app:
```
amlmovil://reset-password?token=ABC123
```

---

## 🚀 Deploy en Vercel

**Ya está conectado con GitHub** - Auto-deploy cada push.

```bash
git add .
git commit -m "Update"
git push
```

---

## 📁 Estructura:

```
vercel-reset-password/
├── public/
│   ├── index.html              ← Página principal
│   └── .well-known/            ← Universal Links (para después)
│       ├── apple-app-site-association
│       └── assetlinks.json
├── vercel.json                 ← Config Vercel
└── package.json
```

---

## 📖 Documentación:

- **`COMO_USAR.md`** → Pasos para usar después del deploy
- **`DESPUES_DEL_DEPLOY.md`** → Checklist post-deploy

---

## ✅ Próximos pasos:

1. Push a GitHub
2. Vercel auto-deploya
3. Actualizar backend con tu URL de Vercel
4. ¡Probar!

**Lee `COMO_USAR.md` para instrucciones detalladas** 📄
