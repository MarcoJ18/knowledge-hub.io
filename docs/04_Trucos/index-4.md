---
title: Eliminar Banner MonsterInsights
---

## Paso 1.Acceder al Divi
- Para eliminar la marca de agua del footer de MonsterInsights de la version premiun con css
- Accedemos a Divi -> Opciones del Tema -> CSS Personalizado (abajo del todo).
![1](https://github.com/user-attachments/assets/f0d6a918-0b99-469f-ada9-2834ae8d7cce)

## Paso 2.Añadimos el codigo
- Añadimos el siguiente código personalizado de texto que aparece en la imagen

```
  div[style*="text-align: center"] a[href*="monsterinsights.com"] {
    display: none !important;
}
```

## Paso 3.Guardar
- Guardar cambios
![image](https://github.com/user-attachments/assets/ee9d794c-3658-438f-901d-cec0656e6550)
