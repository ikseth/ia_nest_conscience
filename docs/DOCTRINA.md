# Doctrina de conscience

Estado: activo
Version: 1.1 - 2026-09-30

Diseno ya reconciliado de esta capa: QUE es conscience y como se relaciona con
el resto del ente. La base conceptual de COMO delibera esta en
`docs/FUNDAMENTOS.md` (propuesta).

Origen: vivia en `core docs/FRONTERAS.md`, marcado `[doctrina de capa]`, como
deuda declarada hasta que se sembrara este repo (conscience ADR 0001). Las
decisiones de origen siguen en el core y no se mueven: son historia.

## Que es

- Supervisor etico/de personalidad del ente (`core ADR 0034`), dual:
  - **Modo live**: supervisa los checkpoints del flujo del orquestador; puede
    bloquear o replantear lo que le genere duda, contrastando con su memoria
    etica.
  - **Modo sueno**: con el core en reposo (quiesce, capacidad administrativa
    futura del core con su propio ADR), revisa en batch la telemetria del dia
    para contextualizar, aprender y generar nuevas tramas de memoria.

    **Disparador pendiente (quiesce).** El modo sueno necesita que el core pueda
    ponerse en reposo, y esa capacidad (`core docs/PLAN.md`, fase v0.2-4) esta
    DIFERIDA hasta que exista su consumidor. Sembrar este repo no la activa: el
    consumidor es la IMPLEMENTACION del modo sueno. Antes de empezar a
    implementarlo, primer paso: abrir un CR al core para reactivar esa fase.
- Sistema nervioso VOLUNTARIO del ente, frente a pulse, el involuntario
  (`core ADR 0037`). Lo voluntario puede vetar lo involuntario.
- No ejecuta el pensar que supervisa: la orquestacion es del core
  (`core ADR 0034`).

## Sedimentacion

- Sus resoluciones se persisten como memoria de comportamiento e identidad, un
  tier de la memoria de `ia_nest_extended`, y vuelven al core por
  enriquecimiento (`core ADR 0025`, `core ADR 0031`). La personalidad del ente
  se sedimenta; el motor no se toca.
- En extended esas memorias son DELEGADAS: extended es su sustrato y su
  mecanismo, conscience su unico dueno de escritura
  (`extended docs/VISION_MEMORIA.md`, `extended ADR 0002`).

## Lo que absorbe esta capa

- El modelo de control/verificacion de respuesta, alternativa descartada para
  el core (`core ADR 0025`), y la "doble conciencia" viven aqui.

## Frontera

La costura la fija el core y vive alli (`core docs/FRONTERAS.md`): contratos
publicos + checkpoints de supervision del orquestador (`core ADR 0034`) +
telemetria CSV/JSONL (`core ADR 0010`, `core ADR 0015`).
