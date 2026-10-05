# Taller: Git Profesional, GitHub Flow y Code Review

Repositorio del taller práctico de la asignatura **Electiva**.

**Estudiante:** Ermes Raúl Barragán Elles
**Docente:** Ing. Ricardo Vanegas Alarcón
**Universidad Tecnológica de Bolívar**

---

## Objetivo

Aplicar la estrategia **GitHub Flow** mediante ramas y Pull Requests, configurar
reglas de protección y estandarización en el repositorio remoto, y realizar una
auditoría manual de código identificando violaciones a las métricas de calidad.

## Estructura del taller

| Parte | Contenido | Peso |
|---|---|---|
| 1 | Configuración de la infraestructura en GitHub | 30 % |
| 2 | Simulación de desarrollo y apertura del Pull Request | 35 % |
| 3 | Auditoría y Code Review manual | 35 % |

## Flujo de trabajo

La rama `main` está protegida: no admite *pushes* directos. Todo cambio entra
por Pull Request con al menos una aprobación.

```
main  ──────────────────────────────────▶
        \                          /
         feature/modulo-pagos ────▶  (Pull Request)
```

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `pagos.py` | Módulo de procesamiento de pagos sometido a auditoría |
| `.github/pull_request_template.md` | Plantilla de Pull Request con el checklist de calidad |

## Criterios de calidad aplicados en la revisión

- Complejidad ciclomática **V(G) ≤ 5**
- Uso de **Guard Clauses** para evitar anidamiento excesivo
- **0 valores mágicos** en el código
- Pruebas unitarias que cubran los caminos nuevos
