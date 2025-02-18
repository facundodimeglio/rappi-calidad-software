# 📘 README.md – Repositorio de Simulación para Rappi

## 📝 Descripción
Este repositorio documenta la simulación de control de cambios de la aplicación **Rappi**, empleando **Git** y la estrategia **Git Flow**, con evidencias de ramas, commits y actualizaciones alineadas con la matriz de trazabilidad.

---
## 📂 Estructura del Proyecto
```plaintext
📂 rappi-calidad-software/
├── src/
│   ├── backend/
│   ├── frontend/
│   └── mobile/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── system/
├── docs/
│   ├── requirements/
│   └── test-cases/
└── CHANGELOG.md
```

---
## 🌿 Estrategia de Branching (Git Flow)
- 🚀 **main:** Versión estable en producción.
- 🔧 **develop:** Integración de nuevas funcionalidades.
- 🛠️ **feature/:** Desarrollo de nuevas características.
- 📦 **release/:** Preparación de versiones.
- 🚑 **hotfix/:** Corrección de errores críticos.

---
## 🗝️ Cambios Realizados Según la Matriz de Trazabilidad
- 🟢 `feature/update-test-status:` Actualiza el estado de **CP-003** y **CP-012** ('Pendiente' ➔ 'Aprobado').
- 🛑 `hotfix/fix-cp006:` Corrige error en **CP-006** ('Fallido' ➔ 'Aprobado').

---
## 💻 Comandos Ejecutados
```bash
# Clonar el repositorio
git clone https://github.com/facundodimeglio/rappi-calidad-software.git
cd rappi-calidad-software

# Crear estructura y primer commit
git init
mkdir -p src/backend src/frontend src/mobile tests/unit docs/test-cases
git add .
git commit -m "Estructura inicial"
git push origin main

# Crear ramas feature y hotfix
git checkout -b feature/update-test-status
echo "Actualización CP-003 y CP-012" > docs/test-cases/update-status.md
git commit -am "Feature: Actualización CP-003 y CP-012"
git push origin feature/update-test-status

git checkout -b hotfix/fix-cp006
echo "Corrección CP-006" > docs/test-cases/hotfix.md
git commit -am "Hotfix: Corrección CP-006"
git push origin hotfix/fix-cp006

# Fusionar ramas
git checkout develop
git merge feature/update-test-status
git merge hotfix/fix-cp006
git checkout main
git merge develop
git push origin main
```

---
## 📊 Historial de Cambios (`git log --graph`):
```plaintext
* 7f3e2d5 (main) Merge: Hotfix CP-006
|\  
| * 5c2a1f3 (hotfix/fix-cp006) Hotfix: Corrección CP-006
| * 4b7c2e1 (feature/update-test-status) Feature: Actualización CP-003 y CP-012
* | 3a2d9e0 (develop) Merge: Actualización de test status
```

---
## ✅ Conclusión
- ✔️ Se demuestra el uso completo de **Git Flow**.
- ✔️ Se evidencia la relación entre cambios y matriz de trazabilidad.
- ✔️ Se documenta el historial de cambios para futuras auditorías.
