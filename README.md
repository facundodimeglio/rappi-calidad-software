# rappi-calidad-software
Rappi Calidad de Software
📌 Descripción

Este repositorio simula el control de cambios de la aplicación Rappi utilizando Git y la estrategia Git Flow, mostrando el uso de ramas, commits y actualizaciones según la matriz de trazabilidad.

🗃️ Estructura del Proyecto

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


🚀 Estrategia de Branching (Git Flow)

main: Código estable en producción.

develop: Rama de integración de nuevas funcionalidades.

feature/: Nuevas funcionalidades.

release/: Preparación de versiones.

hotfix/: Correcciones urgentes.

🔑 Cambios Realizados Según la Matriz de Trazabilidad

feature/update-test-status: Actualiza el estado de CP-003 y CP-012 ('Pendiente' a 'Aprobado').

hotfix/fix-cp006: Corrige el error de CP-006 ('Fallido' a 'Aprobado').

💻 Comandos Ejecutados

# Clonar y configurar
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
git commit -am "Feature: Actualización de CP-003 y CP-012"
git push origin feature/update-test-status

git checkout -b hotfix/fix-cp006
echo "Corrección CP-006" > docs/test-cases/hotfix.md
git commit -am "Hotfix: Corrección CP-006"
git push origin hotfix/fix-cp006

# Fusionar ramas a develop y main
git checkout develop
git merge feature/update-test-status
git merge hotfix/fix-cp006
git checkout main
git merge develop
git push origin main

Este README refleja el control de cambios, el uso adecuado de ramas y la coherencia con la matriz de trazabilidad, evidenciando la gestión organizada mediante Git Flow.

