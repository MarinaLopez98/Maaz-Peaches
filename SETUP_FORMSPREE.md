# 📧 Configuración de Comentarios con Formspree para GitHub Pages

Esta guía te muestra cómo activar los comentarios para que lleguen a **marinalo.lm644@gmail.com**.

## ✅ Compatible con GitHub Pages

Formspree funciona perfectamente con sitios estáticos como GitHub Pages, sin necesidad de servidor backend.

---

## 🚀 Pasos de Configuración (5 minutos)

### **Paso 1: Crear Cuenta en Formspree**

1. Ve a **[https://formspree.io/register](https://formspree.io/register)**
2. Regístrate con tu email **marinalo.lm644@gmail.com** (o con GitHub)
3. Confirma tu email

### **Paso 2: Crear un Formulario**

1. Una vez dentro, haz clic en **"+ New Form"**
2. Dale un nombre: `Comentarios Blog`
3. Copia el **Form ID** (se ve algo así: `xpwzyabc`)

### **Paso 3: Configurar el Email de Destino**

1. En la página de tu formulario, ve a **Settings** → **Email**
2. Asegúrate que el email de destino sea: **marinalo.lm644@gmail.com**
3. Activa **"Send me an email when a new submission arrives"**

### **Paso 4: Actualizar el Código**

Abre el archivo: `src/components/blog/CommentsSection.astro`

Busca la línea 12 que dice:

```html
<form class="comment-form" id="commentForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

Reemplaza `YOUR_FORM_ID` con tu Form ID de Formspree. Ejemplo:

```html
<form class="comment-form" id="commentForm" action="https://formspree.io/f/xpwzyabc" method="POST">
```

### **Paso 5: Desplegar**

1. Guarda el archivo
2. Haz commit y push a GitHub:

```bash
git add .
git commit -m "Configurar Formspree para comentarios"
git push
```

3. Espera 1-2 minutos a que GitHub Pages se actualice

### **Paso 6: Probar**

1. Ve a tu blog: **https://marinalopez98.github.io/Maaz-Peaches/blog/blogpost-1**
2. Baja hasta la sección de comentarios
3. Escribe un comentario de prueba
4. Haz clic en **"Enviar comentario"**
5. Verifica que te llegue el email a **marinalo.lm644@gmail.com**

---

## 📧 Qué Recibirás por Email

Cada comentario llegará con:
- **Nombre** del autor (o "Anónimo")
- **Comentario** completo
- **URL de la página** donde se dejó el comentario
- **Fecha y hora** del envío

---

## 🎨 Funcionalidad

✅ **Los comentarios se ven en la página** inmediatamente después de enviarlos
✅ **Te llega un email** con cada comentario
✅ **Funciona en GitHub Pages** sin problemas
✅ **Gratis** hasta 50 envíos/mes (más que suficiente para un blog personal)

---

## 🔒 Privacidad

- Los comentarios se guardan **localmente en el navegador** de cada visitante
- Solo tú recibes los emails
- Formspree almacena los envíos en tu dashboard (puedes exportarlos o borrarlos)

---

## 💰 Plan Gratuito de Formspree

- **50 envíos/mes** gratis
- Si necesitas más, puedes upgradear o crear múltiples formularios

---

## ❓ Problemas Comunes

### El comentario no aparece en la página
- Verifica que JavaScript esté habilitado en el navegador
- Revisa la consola del navegador (F12) por errores

### No me llega el email
- Verifica tu spam/correo no deseado
- Confirma que configuraste el email correcto en Formspree
- Verifica que el Form ID sea correcto en el código

### Error al enviar
- Asegúrate de estar conectado a internet
- Verifica que el Form ID en el código coincida con el de Formspree

---

## 🎉 ¡Listo!

Una vez configurado, los comentarios:
1. Se mostrarán en la página inmediatamente
2. Te llegarán por email a **marinalo.lm644@gmail.com**
3. Funcionarán sin problemas en GitHub Pages

---

🍑 **Maaz-Peaches Blog** - Sistema de Comentarios Simple y Funcional
