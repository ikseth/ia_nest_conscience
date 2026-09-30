# Decision 0001: genesis de conscience

Fecha: 2026-09-30

## Decision

Se siembra `ia_nest_conscience` como semilla documental, sin codigo ni
contrato publico:

1. **Mudanza de la doctrina.** El diseno reconciliado de la capa, que vivia en
   `core docs/FRONTERAS.md` marcado `[doctrina de capa]`, muda a
   `docs/DOCTRINA.md`. En el core queda la costura y un puntero.
2. **Base conceptual de la deliberacion** en `docs/FUNDAMENTOS.md`, en estado
   propuesta: comite de miembros divergentes, discrepante obligatorio,
   resolucion como artefacto, suelo procedimental retirable y autonomia ganada
   por clase de decision.
3. **Declaracion de intenciones publica** en `publications/`, en ingles y en
   espanol (meta ADR 0012 para el texto con acentos).

## Motivo

La capa tenia diseno reconciliado desde julio (`core ADR 0034`, `core ADR 0037`)
y un consumidor esperando: `extended` ya reserva memorias de identidad y
entidades cuyo unico dueno de escritura es conscience
(`extended docs/VISION_MEMORIA.md`). Faltaba la base de COMO delibera; la aporta
la "Carta abierta sobre OCIR" (Ignacio Jose Garcia de Hoyos, 2026-09-11),
adaptada en `docs/FUNDAMENTOS.md`.

**Nombre del repo.** `core ADR 0033` nombra esta capa
`ia_nest_core_conscience`. El repo se crea como `ia_nest_conscience`, igual que
la memoria se creo como `ia_nest_extended` y no como `ia_nest_core_extended`: el
prefijo `core_` sobraba en las dos. El ADR del core conserva su texto; la
deriva se anota en `meta docs/REGISTRO_CAPAS.md`.

## Consecuencia

- `core docs/FRONTERAS.md` deja de alojar doctrina de conscience; conserva la
  costura.
- La fila de la capa en `meta docs/REGISTRO_CAPAS.md` pasa a semilla.
- Sin SemVer ni tag hasta que exista contrato publico.

## Impacto de version

Ninguno: no hay contrato publico.
