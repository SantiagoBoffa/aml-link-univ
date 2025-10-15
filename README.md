# AML Reset Password - SIMPLE

## ¿Qué hace?

Página HTML simple que redirige a la app AML.

**URL:**
```
https://tu-vercel.app/?token=ABC123
```

**Hace:**
```
window.location.href = "amlmovil://reset-password?token=ABC123"
```

## Deploy

Ya está conectado con GitHub. Solo:

```bash
git add .
git commit -m "Update"
git push
```

Vercel auto-deploya.

## Usar en el backend

En `aml-be/src/extensions/users-permissions/controllers/auth.ts` línea 40:

```typescript
const baseUrl = 'https://TU-URL.vercel.app';
const resetPasswordUrl = `${baseUrl}/?token=${resetPasswordToken}`;
```

¡Eso es todo!
