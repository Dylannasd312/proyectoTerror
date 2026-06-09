# FLUJO DE TRABAJO - GIT FLOW SIMPLIFICADO

## Descripción
El proyecto utiliza un flujo de trabajo basado en Git Flow simplificado, el cual permite organizar el desarrollo mediante ramas para evitar conflictos y mantener estabilidad en el código.

---

## Rama main
La rama `main` contiene la versión estable del proyecto.  
Aquí solo se sube código que ya ha sido probado y funciona correctamente.

---

## Rama develop
La rama `develop` es donde se integran todas las funcionalidades en desarrollo.  
Sirve como base para crear nuevas características y probar el sistema completo antes de pasar a producción.

---

## Ramas feature/*
Las ramas `feature/*` se utilizan para desarrollar nuevas funcionalidades del proyecto.

Ejemplos:
- feature/movimiento-personaje
- feature/linterna
- feature/enemigo

Cada funcionalidad se desarrolla de forma independiente y luego se integra en la rama `develop`.

---

## Flujo de trabajo

1. Crear rama develop a partir de main
2. Crear ramas feature desde develop
3. Desarrollar la funcionalidad en feature
4. Hacer merge de feature a develop
5. Finalmente, hacer merge de develop a main

---

## Ejemplo práctico

### 1. Crear rama develop
git checkout -b develop

### 2. Subir rama develop
git push -u origin develop

---

### 3. Crear una rama feature
git checkout -b feature/movimiento-personaje

---

### 4. Simular cambios
git add .
git commit -m "Se implementa movimiento del personaje"

---

### 5. Volver a develop y hacer merge
git checkout develop
git merge feature/movimiento-personaje

---

### 6. Subir cambios
git push origin develop

---

### 7. Merge final a main
git checkout main
git merge develop

---

## Estado actual del flujo
- Rama main creada
- Rama develop creada
- Rama feature implementada
- Merge realizado correctamente (simulado)

---

## Conclusión
El uso de Git Flow simplificado permite mantener un desarrollo ordenado, facilitando la integración de nuevas funcionalidades sin afectar la estabilidad del proyecto.
