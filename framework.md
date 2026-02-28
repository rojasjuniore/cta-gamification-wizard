# CTA+ Gamification Wizard Framework

## Estructura General

```
[Selección de Categoría]
         ↓
[Preguntas de Diagnóstico]
         ↓
[Generación de Plan Gamificado]
```

---

## CATEGORÍAS

### 1. 🏢 Gamificación Empresarial
**Enfoque:** Cultura, clima laboral, productividad, engagement

### 2. 💰 Gamificación de Ventas
**Enfoque:** Conversión, metas, incentivos, competencia

### 3. 👥 Gamificación de Equipos
**Enfoque:** Team building, actividades, cohesión, integración

---

## PREGUNTAS POR CATEGORÍA

### 🏢 GAMIFICACIÓN EMPRESARIAL

#### Preguntas Fijas (5)

| ID | Pregunta | Tipo | Opciones |
|----|----------|------|----------|
| E1 | ¿Cuántos empleados participarán en el programa? | Número | Input numérico |
| E2 | ¿Cuál es el problema principal que quieren resolver? | Selección única | Rotación alta / Baja productividad / Mal clima laboral / Falta de compromiso / Comunicación deficiente |
| E3 | ¿Qué comportamientos específicos quieren incentivar? | Selección múltiple | Puntualidad / Colaboración / Iniciativa / Cumplimiento de metas / Innovación / Capacitación continua |
| E4 | ¿Tienen presupuesto asignado para recompensas? | Selección única | Sin presupuesto / $1-500K COP / $500K-2M COP / +$2M COP |
| E5 | ¿En cuánto tiempo esperan ver resultados medibles? | Selección única | 1 mes / 3 meses / 6 meses / 1 año |

#### Preguntas Condicionales (3)

| ID | Condición | Pregunta | Tipo |
|----|-----------|----------|------|
| E6 | Si E2 = "Rotación alta" | ¿Cuál es su tasa de rotación anual actual? | Selección: <10% / 10-25% / 25-50% / >50% |
| E7 | Si E2 = "Baja productividad" | ¿Tienen métricas de productividad definidas? | Sí/No + texto si Sí |
| E8 | Si E4 = "Sin presupuesto" | ¿Están abiertos a recompensas no monetarias? (reconocimiento, tiempo libre, etc.) | Sí / No / Tal vez |

---

### 💰 GAMIFICACIÓN DE VENTAS

#### Preguntas Fijas (6)

| ID | Pregunta | Tipo | Opciones |
|----|----------|------|----------|
| V1 | ¿Cuántos vendedores/agentes comerciales tienen? | Número | Input numérico |
| V2 | ¿Cuál es su ticket promedio de venta? | Número | Input con moneda |
| V3 | ¿Qué porcentaje de la meta mensual están cumpliendo actualmente? | Selección | <25% / 25-50% / 50-75% / 75-100% / >100% |
| V4 | ¿Cómo compensan actualmente a los vendedores? | Selección múltiple | Salario fijo / Comisión por venta / Bonos por meta / Premios en especie |
| V5 | ¿Qué métrica quieren mejorar principalmente? | Selección única | Volumen de ventas / Ticket promedio / Retención de clientes / Nuevos clientes / Upselling/Cross-selling |
| V6 | ¿Sus vendedores prefieren competir o colaborar? | Selección | Competencia individual / Competencia por equipos / Colaboración / No sé |

#### Preguntas Condicionales (3)

| ID | Condición | Pregunta | Tipo |
|----|-----------|----------|------|
| V7 | Si V3 = "<50%" | ¿Cuál crees que es la causa principal del bajo cumplimiento? | Selección: Falta de capacitación / Metas irreales / Desmotivación / Proceso de venta deficiente / Producto/precio |
| V8 | Si V6 = "Competencia individual" | ¿Han tenido problemas de clima laboral por competencia entre vendedores? | Sí / No / A veces |
| V9 | Si V4 no incluye "Bonos por meta" | ¿Estarían dispuestos a implementar bonos por cumplimiento de meta? | Sí / No / Depende del presupuesto |

---

### 👥 GAMIFICACIÓN DE EQUIPOS

#### Preguntas Fijas (5)

| ID | Pregunta | Tipo | Opciones |
|----|----------|------|----------|
| Q1 | ¿Cuántas personas participarán? | Número | Input numérico |
| Q2 | ¿Es un evento único o un programa continuo? | Selección | Evento único / Programa mensual / Programa trimestral / Programa anual |
| Q3 | ¿La actividad será presencial, virtual o híbrida? | Selección | Presencial / Virtual / Híbrida |
| Q4 | ¿Cuál es el objetivo principal? | Selección única | Integrar nuevos miembros / Mejorar comunicación / Resolver conflictos / Celebrar logros / Diversión y desconexión |
| Q5 | ¿Cuánto tiempo tienen disponible? | Selección | 2 horas / Medio día (4h) / Día completo (8h) / Múltiples días |

#### Preguntas Condicionales (2)

| ID | Condición | Pregunta | Tipo |
|----|-----------|----------|------|
| Q6 | Si Q4 = "Resolver conflictos" | ¿Hay equipos o áreas específicas con tensiones? | Sí + descripción / No, es general |
| Q7 | Si Q3 = "Virtual" o "Híbrida" | ¿Qué plataforma usan para reuniones virtuales? | Zoom / Teams / Meet / Otra |

---

## MECÁNICAS DE GAMIFICACIÓN DISPONIBLES

### Mecánicas Core

| Mecánica | Descripción | Mejor para |
|----------|-------------|------------|
| **Puntos** | Sistema de acumulación por acciones | Todas las categorías |
| **Niveles** | Progresión por acumulación de puntos/logros | Empresarial, Ventas |
| **Badges/Insignias** | Reconocimiento por logros específicos | Todas las categorías |
| **Leaderboards** | Ranking visible de participantes | Ventas, Equipos competitivos |
| **Misiones/Retos** | Objetivos específicos con recompensa | Todas las categorías |
| **Equipos** | Agrupación para competencia/colaboración | Equipos, Empresarial |
| **Streaks** | Bonificación por consistencia | Empresarial (hábitos) |
| **Recompensas** | Premios tangibles o intangibles | Todas |

### Mecánicas Avanzadas

| Mecánica | Descripción | Mejor para |
|----------|-------------|------------|
| **Narrativa/Historia** | Contexto temático que da sentido | Equipos (eventos) |
| **Personalización** | Avatares, títulos personalizados | Empresarial largo plazo |
| **Economía virtual** | Moneda interna canjeable | Empresarial, Ventas |
| **Desbloqueos** | Contenido/beneficios que se liberan | Empresarial |
| **Feedback instantáneo** | Notificaciones en tiempo real | Ventas |

---

## LÓGICA DE GENERACIÓN DEL PLAN

### Inputs → Mecánicas Recomendadas

```javascript
// Ejemplo de lógica
if (categoria === "ventas" && competencia === "individual") {
  incluir: ["leaderboard", "badges", "recompensas"]
}

if (categoria === "empresarial" && problema === "rotacion") {
  incluir: ["niveles", "reconocimiento", "streaks", "desbloqueos"]
}

if (categoria === "equipos" && objetivo === "integracion") {
  incluir: ["equipos", "misiones_colaborativas", "narrativa"]
}
```

### Estructura del Output (Plan Gamificado)

```
1. RESUMEN EJECUTIVO
   - Objetivo del programa
   - Participantes
   - Duración estimada
   - Inversión sugerida

2. DIAGNÓSTICO
   - Problema identificado
   - Oportunidades detectadas

3. MECÁNICAS SELECCIONADAS
   - Lista de mecánicas con justificación
   - Cómo se implementa cada una

4. SISTEMA DE PUNTOS/NIVELES
   - Tabla de acciones y puntos
   - Niveles y beneficios por nivel

5. RECOMPENSAS SUGERIDAS
   - Según presupuesto indicado
   - Mix monetario/no monetario

6. CRONOGRAMA DE IMPLEMENTACIÓN
   - Fases
   - Milestones

7. MÉTRICAS DE ÉXITO
   - KPIs a medir
   - Frecuencia de medición

8. PRÓXIMOS PASOS
   - CTA para contratar implementación
```

---

## DISEÑO UI (CTA+ Style)

### Colores
- Fondo: #000000
- Acento primario: #F45325 (naranja CTA+)
- Acento secundario: #1A1A2E
- Texto: #FFFFFF
- Bordes: #ffffff20

### Tipografía
- Títulos: Archivo Black
- Cuerpo: Inter

### Componentes
- Botones con borde 1px, sin border-radius
- Cards con borde 1px solid #ffffff20
- Inputs con fondo #1A1A2E, borde 1px
- Progress bar para mostrar avance del wizard

### Animaciones
- Fade-up en entrada de secciones
- Scale-in en selección de categoría
- Slide en transición entre pasos
