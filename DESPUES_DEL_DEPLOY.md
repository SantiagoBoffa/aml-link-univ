# ✅ Después del Deploy - Checklist

## 📝 Tu URL de Vercel:

```
https://TU-PROYECTO.vercel.app
```

👆 **Anota tu URL aquí cuando la tengas**

---

## 🔧 PASO 1: Actualizar Backend

**Archivo:** `aml-be/src/extensions/users-permissions/controllers/auth.ts`

**Línea 40, cambiar:**

```typescript
const baseUrl = process.env.RESET_PASSWORD_URL || 'TU_URL_DE_VERCEL_AQUI';
```

**Reiniciar backend:**
```bash
cd aml-be
docker compose restart
```

---

## 📱 PASO 2: Actualizar App

**Archivo:** `aml-fe/app.json`

**Cambiar estas líneas:**

```json
"ios": {
  "associatedDomains": [
    "applinks:TU-PROYECTO.vercel.app"
  ]
},

"android": {
  "intentFilters": [
    {
      "data": [
        {
          "host": "TU-PROYECTO.vercel.app"
        }
      ]
    }
  ]
}
```

---

## 🧪 PASO 3: Probar

1. **Verificar archivos:**
   - `https://TU-PROYECTO.vercel.app/.well-known/apple-app-site-association`
   - `https://TU-PROYECTO.vercel.app/reset-password?token=test`

2. **Solicitar reset password**

3. **Verificar email tiene la URL correcta**

---

## ✅ Checklist Final:

- [ ] Deploy a Vercel completado
- [ ] URL de Vercel anotada
- [ ] Backend actualizado y reiniciado
- [ ] app.json actualizado
- [ ] Archivos .well-known accesibles
- [ ] Email enviado con URL correcta
- [ ] Deep link probado y funcionando

---

¡Listo para producción! 🚀

