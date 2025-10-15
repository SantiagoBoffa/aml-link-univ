# AML Reset Password - Página Simple

## 🎯 Qué hace:

Esta página recibe un link tipo:
```
https://tu-url.vercel.app/reset-password?token=XXX
```

Y automáticamente intenta abrir la app con:
```
amlmovil://reset-password?token=XXX
```

---

## 🚀 Deploy en Vercel:

Ya está conectado con GitHub. Solo hacé:

```bash
git add .
git commit -m "Update"
git push
```

Vercel hace auto-deploy 🎉

---

## ✅ Cómo probar:

1. Deployar en Vercel
2. Obtener tu URL (ej: `https://aml-link-univ.vercel.app`)
3. Actualizar backend con esa URL
4. Solicitar reset password
5. Abrir el email en el celular
6. Tocar el link → Debería abrir la app

---

## 📝 Próximos pasos (cuando funcione):

- Agregar archivos `.well-known` para Universal Links
- Mejorar la página fallback
- Agregar links a App Store / Play Store
