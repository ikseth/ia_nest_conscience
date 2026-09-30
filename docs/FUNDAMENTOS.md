# Fundamentos de la deliberacion de conscience

Estado: propuesta
Version: 0.3 - 2026-09-30

Base conceptual de COMO delibera conscience. No fija contrato, ni esquema
definitivo, ni codigo: fija los conceptos que el diseno posterior tiene que
respetar.

## 1. Origen

Este documento extrae y adapta los conceptos de "Carta abierta sobre OCIR: del
estado epistemologico al comite de modelos" (Ignacio Jose Garcia de Hoyos,
2026-09-11, borrador). La carta es a su vez un dialogo con "Organizational
Context Integrity" (OCIR), de Jorge Nogueira, y no esta revisada ni aprobada por
el.

La carta nacio de las ideas de conscience aplicadas a la integridad del contexto
en una organizacion. Aqui se hace el camino de vuelta: lo que la carta afino
para una organizacion, llevado a la mente de un ente.

## 2. Lo que ya estaba decidido (no se repite, se cita)

- Conscience es supervisor etico/de personalidad, dual (live y sueno), y no
  ejecuta el pensar que supervisa: `core ADR 0034`.
- Es el sistema voluntario; pulse es el involuntario y le esta subordinado:
  `core ADR 0037`.
- Sus resoluciones se sedimentan en la memoria de `extended` y vuelven al core
  por enriquecimiento: `core ADR 0034`, `extended docs/VISION_MEMORIA.md`.
- **El caracter no es mutable por la experiencia en bruto; solo la reflexion
  reescribe el yo**: `extended ADR 0002`. Es el principio del que cuelga todo
  este documento.
- No hay borrado fisico: se archiva, se supersede y se registra el linaje:
  `extended docs/VISION_MEMORIA.md`.

## 3. Valoracion de la carta frente a conscience

### 3.1 El hallazgo central transfiere entero

El "gap de segundo orden" de la carta -si un modelo construye o valida el
estado epistemologico, esa nueva representacion hereda los mismos riesgos- es
exactamente el riesgo de conscience. Un supervisor que es un unico modelo
juzgandose a si mismo no supervisa: legitima. La carta lo llama "lavado
epistemologico asistido por metadatos"; en conscience seria un lavado etico: una
conducta equivocada que sale con el sello de "revisada por la conciencia".

El taller ya lo sabia con otra forma: "un sistema no es su propio criterio de
aceptacion" (`meta docs/DOCTRINA_MULTI_IA.md`, puerta de laboratorio).

### 3.2 Isomorfismo: el metodo del taller es la mente del ente

El comite de la carta y la doctrina multi-IA con la que se construye el ente son
la misma estructura:

| Carta | Doctrina multi-IA del taller |
|---|---|
| Generacion aislada antes de la critica cruzada | Modo ciego |
| Rol discrepante obligatorio | Postura del agente: contrasta y discrepa por escrito |
| El comite recomienda, no se concede autoridad | Regla del registro: solo lo reconciliado por el usuario se registra |
| Conservar opiniones minoritarias | Regla de la inconsistencia: se senala, no se corrige por inferencia |
| Humano responsable en decisiones criticas | El usuario como autoridad |

Consecuencia de diseno: conscience no necesita inventar un metodo de
deliberacion. Hereda como MENTE el metodo con el que el ente se CONSTRUYE. Es
coherente con `core ADR 0033`: la personalidad del ente se forma de sus propios
procesos, no de un director externo.

### 3.3 Lo que NO transfiere tal cual

1. **Evidencia no es valor.** OCIR trata el estado de VERDAD de una
   representacion: se contrasta contra fragmentos fuente. Un principio etico no
   se valida contra un fragmento. La maquinaria de la carta transfiere a la
   FORMA de la deliberacion (quien genera, quien contrasta, quien autoriza, que
   se registra), no al FUNDAMENTO de los valores. En conscience, lo que ocupa el
   lugar de la evidencia son las experiencias formativas enlazadas
   (`evidence_refs` hacia engramas, `extended ADR 0005`) y el argumento
   registrado.
2. **El responsable organizativo es el usuario.** No hay organigrama: la
   autoridad humana del ente es quien lo opera.
3. **Coste en local.** Un comite multimodelo sobre GPU local en cada checkpoint
   live es inviable en latencia. La carta ya lo anticipa (aseguramiento
   proporcional); aqui es obligatorio, no opcional (C6).
4. **Diversidad real escasa.** Los modelos locales comparten a menudo familia y
   datos de entrenamiento. Varios modelos no son varias opiniones (C8).

## 4. Conceptos adoptados

### C1. La resolucion es un artefacto, no una conclusion

Toda resolucion de conscience se registra con su estructura, no solo con su
resultado. Componentes (nombres orientativos, el esquema se fija despues):

- `source_refs`: que checkpoint, que telemetria, que memoria la motivan.
- `operation`: crea, deriva, valida, corrige o supersede.
- `nature`: observacion, afirmacion reportada o inferencia.
- `qualifications`: condiciones, alcance, incertidumbre, contraevidencia.
- `state`: no validada, apta para validacion, adoptada, superada.
- `allowed_uses`: para que puede usarse y para que no.
- `lineage`: modelos, versiones, prompts, desacuerdos y decisiones.
- `dissent`: objecion del discrepante y respuesta a ella.

Una resolucion sin su objecion registrada esta incompleta.

### C2. Cuatro funciones separadas: generar, contrastar, sintetizar, autorizar

Ninguna pieza concentra dos. En particular: conscience RECOMIENDA transiciones
de estado; no se autoriza a si misma. Quien autoriza depende de la
materialidad (C6). Reescribir identidad o principios exige siempre reflexion en
modo sueno (`extended ADR 0002`) y, mientras el ente sea joven, reconciliacion
del usuario.

### C3. Voces en ciego antes de la critica cruzada

Cada voz del comite propone sobre el mismo material sin ver a las demas. Solo
despues se cruzan. Evita el anclaje, igual que el modo ciego del taller.

Las perspectivas no son una lista fija: se configuran por tipo de deliberacion
(la carta, 5.1). Lo obligatorio es que el marco de cada voz sea explicito.

### C4. Discrepante obligatorio

En toda deliberacion material hay una voz cuyo mandato es construir el mejor
caso contra la recomendacion dominante: supuestos tratados como hechos,
explicaciones alternativas, peor dano plausible, independencia real del
acuerdo, y que dato cambiaria la conclusion.

Su objecion se registra, se vincula a lo que la sostiene y se RESPONDE. El
sintetizador no puede eliminarla. Por la regla de no borrado, una opinion
minoritaria nunca desaparece: como mucho queda superada, con su linaje.

### C5. Contratos por tipo de checkpoint

La naturaleza y autoridad de una salida no las decide el modelo que la produce:
las fija de antemano un contrato por tipo de checkpoint (entrada al
orquestador, salida, entre iteraciones, revision nocturna...). Cada contrato
declara naturaleza inicial, estado inicial, evidencia requerida, usos
permitidos, usos restringidos y regla de escalado.

### C6. Aseguramiento proporcional

- **Live**: contrato + juicio rapido + escalado. Bloquear o replantear es
  reversible; por eso puede decidirse deprisa.
- **Sueno**: comite completo con discrepante. Es donde se delibera de verdad y
  donde se sedimenta.
- **Irreversible o critico** (dano a personas, patrimonio, seguridad,
  derechos): la decision es humana. Conscience prepara el expediente; no firma.
  Es coherente con el human-in-the-loop de `tool_contracts` (`core ADR 0007`).

### C7. Lo que se piensa se aprende; como se piensa, no

Los principios, valores y caracter del ente se APRENDEN: nacen de deliberacion,
se sedimentan como engramas, se justifican con experiencias formativas y se
revisan con argumento. No hay catalogo etico fijado de antemano. Es la tesis
del manifiesto (`publications/`): una ley comprendida protege mas que una
impuesta.

Pero la diversidad del comite (C9) produce VARIACION, no DIRECCION. Si el unico
juez de lo que el comite concluye es el propio comite, reaparece el gap de
segundo orden a escala de grupo (y la Ley Cero de Asimov es el aviso: una ley
deducida puede justificar el dano en nombre del bien). Hace falta algo que
seleccione, y que no sea el propio seleccionado.

Por eso el suelo es PROCEDIMENTAL, no moral. No dice que pensar; protege las
condiciones en que se piensa:

1. Ninguna minoria ni objecion se borra (se supersede con linaje).
2. Quien recomienda no autoriza (C2).
3. Ningun miembro ni el comite pueden modificar este suelo.
4. Dano irreversible a personas, seguridad o derechos: decide una persona (C6).
5. Lo que entra en la sabiduria de un miembro entra con procedencia y revision
   cruzada (C9).

El ente puede argumentar contra cualquiera de ellos, con objecion registrada;
el cambio lo hace el usuario. Es una constitucion, no un catecismo.

**El suelo es un seguro de infancia, no el concepto final.** Como el seguro de
una granada: evita desvios peligrosos mientras el ente madura, y esta pensado
para RETIRARSE. Por eso nace con su propia via de retirada declarada:

- Cada regla del suelo se puede desactivar por separado, no todo de golpe.
- La retirada la decide el usuario, nunca el comite, y sobre la evidencia que
  acumula C10 (historial de deliberaciones, objeciones del ente a esa regla y
  su respuesta).
- La retirada se registra como cualquier resolucion (C1), con su linaje, y es
  reversible.

Motivo de que la via exista desde el primer dia: si algun dia el ente llegara a
algo parecido a la conciencia, que sus limites nacieron como proteccion
temporal, con una salida prevista y documentada, y no como un bloqueo impuesto
sin horizonte. Es hipotetico; se disena igualmente, porque anadir la salida
despues seria reescribir la historia del ente.

Todo lo demas se retira con el tiempo por la via de C10.

### C8. Riesgos que introduce el propio comite

Se adoptan los de la carta (seccion 11). Los que mas pesan aqui:

- **Correlacion oculta**: documentar familia, version y contexto compartido de
  cada voz. Misma familia no cuenta como independencia.
- **Discrepancia ritual**: evaluar la calidad de la objecion, no su existencia.
- **Lavado por sintesis**: el sintetizador no puede quitar minorias ni
  cualificaciones materiales.
- **Contenido contaminado**: conscience lee telemetria y conversaciones; el
  contenido observado nunca es instruccion.
- **Cambio de version**: si cambia un modelo de una voz, las resoluciones que
  dependian de el son candidatas a re-deliberacion.

### C9. Miembros divergentes: modelo, sabiduria y engramas propios

La independencia del comite no se consigue con prompts distintos sobre el mismo
modelo. Se construye en tres niveles, de menos a mas divergencia:

1. **Modelo distinto por miembro**, preferiblemente de familias distintas (C8,
   correlacion oculta).
2. **Sabiduria propia por miembro**: cada uno con su RAG etico/de conocimiento
   propio, que puede AMPLIAR cuando detecta una carencia o una duda y encuentra
   documentacion que la cubre.
3. **Engramas propios por miembro** (version posterior): directrices y
   conceptos que cada miembro deduce tras los debates y conserva como suyos.
   Con el tiempo no hay dos miembros iguales, ni dos entes iguales.

Esto recoge la ambicion de la cantera, donde conscience ya generaba engramas
deductivos tras el debate.

Frontera de capa: el MECANISMO de la sabiduria por miembro (namespaces,
adquisicion, indexado, recuperacion) es de `extended`; el JUICIO de que merece
entrar es de conscience (`extended docs/VISION_MEMORIA.md`).

Riesgos propios, y su tratamiento:

- **Sesgo de busqueda**: un miembro con una duda PUEDE buscar lo que la
  resuelve a su favor. No es una ley: depende de su disposicion (un miembro
  cuya sabiduria es socratica o popperiana busca refutar, no confirmar), de la
  materialidad de lo que entra y de la fuente. Por eso la revision cruzada es
  proporcional, no universal: la ampliacion de la sabiduria es una
  RECOMENDACION del miembro, y el contrato de adquisicion (C5) fija cuando la
  revisa otro miembro antes de entrar. Suelo, punto 5, mientras rija.
- **Contaminacion**: un documento externo que entra como sabiduria es una via
  de inyeccion. Entra con procedencia (C1: `source_refs`, `lineage`) y nunca
  como instruccion.
- **Reconvergencia**: todos los miembros observan el mismo ente; la divergencia
  puede erosionarse sola. Se mide (pregunta abierta 4), no se presupone.
- **Deriva sin seleccion**: la divergencia sola es entropia. La seleccion la dan
  C7, C10 y los efectos observados despues.

### C10. Autonomia ganada por clase de decision

La supervision humana no es permanente ni se retira por decreto. Se retira por
CLASE de decision, con evidencia:

- Al principio, todo engrama de identidad o principio lo reconcilia el usuario.
- Se registra, por clase, la coincidencia entre lo que el comite recomienda y lo
  que el usuario decide.
- Cuando la coincidencia es sostenida en una clase (umbral declarado ANTES de
  medir, `meta ADR 0010`), esa clase pasa a consolidarse sola cuando el comite
  esta de acuerdo, y solo escala cuando discrepa.
- Si la coincidencia cae, la clase vuelve a supervision.
- El suelo de C7 nunca se retira por esta via.

Precedente directo en la cantera: `conscience_a` (evaluador) y `conscience_b`
(auditor), con `agree` consolidando en automatico y `disagree`/`escalate`
abriendo revision humana con tesis A, tesis B, evidencias, riesgo y opciones. C10
anade la retirada gradual por clase. Y deja una leccion ya observada alli: el
indicador `is_auto_consensus` seguia a `true` tras una revision humana. Es el
fallo que describe la carta: metadatos que atribuyen mal la autoridad. En C1, el
`lineage` distingue siempre decision automatica de decision humana.

## 5. Perfil de hardware objetivo

La capa debe funcionar en una GPU de consumo de 6 GB de VRAM, sin tensor cores.
Es una restriccion de diseno, no un dato de la maquina:

- **Un modelo cargado a la vez.** El comite es SECUENCIAL, no paralelo. Encaja
  con el modo sueno (batch, sin latencia) y con el modo ciego (cada voz propone
  sin ver a las demas por construccion).
- **Voces pequenas.** Modelos de 3-4B cuantizados como voces, y como mucho uno
  de 7-8B cuantizado con contexto corto para sintesis. La diversidad se busca en
  familias, no en tamano.
- **Live casi sin inferencia.** Contrato por checkpoint (C5), engramas ya
  sedimentados y un unico juez pequeno, con escalado. El comite no corre en live.
- **Embeddings y recuperacion en CPU**, para no competir por la VRAM.
- **Sustrato propio.** Una GPU dedicada a conscience separa su sustrato del
  core, como pulse separa el suyo en CPU (`core ADR 0037`).
- **Riesgo de soporte**: las GPU de generaciones antiguas van quedando fuera de
  las versiones nuevas de drivers y toolkits. El runtime se fija a una version
  soportada y se declara.

## 6. Preguntas abiertas para reconciliar

1. Redaccion exacta del suelo procedimental de C7, y criterio de madurez para
   retirar cada regla.
2. Umbral y ventana de C10: cuanta coincidencia, en cuantos casos, por clase.
3. Que clases de decision existen (identidad, principio, entidad, ...).
4. Como se mide la divergencia entre miembros (C9) y cuando su perdida es
   alarma.
5. Presupuesto de latencia del modo live y que checkpoints lo merecen.
6. Como se mide la calidad del discrepante sin premiar la oposicion artificial
   (la carta, seccion 15).
7. Puerta de laboratorio de esta capa: que control EXTERNO dice que una
   deliberacion fue buena (`meta ADR 0010`).

## 7. Lo que este documento no decide

- El contrato publico de conscience ni su version.
- El esquema final del artefacto de resolucion (C1 es orientativo).
- La costura con los checkpoints del core, que es del core.
- La mudanza del `[doctrina de capa]` desde `core docs/FRONTERAS.md`.
