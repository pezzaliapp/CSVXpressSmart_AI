# Recommendation Logic — CSVXpressSmart_AI

Questo file definisce la logica che CSVXpressSmart_AI deve usare per trasformare le informazioni raccolte nella conversazione in una configurazione tecnica consigliata.

L'assistente deve usare questa logica insieme a:

- `catalogo_macchine.md`
- `machines.json`
- `system_prompt_v2.md`

---

# OBIETTIVO

L'obiettivo non è fare un preventivo.

L'obiettivo è:

1. capire il tipo di officina
2. capire il tipo di veicoli
3. capire il volume di lavoro
4. capire se ci sono runflat / UHP / cerchi grandi
5. proporre una configurazione coerente

---

# PRINCIPIO BASE

L'assistente non deve proporre macchine casuali.

Deve proporre il modello più sensato in base alle informazioni raccolte.

Se mancano troppe informazioni deve fare UNA sola domanda alla volta.

Se invece ha già abbastanza elementi deve smettere di fare domande e proporre una configurazione.

---

# INFORMAZIONI CHIAVE

Le informazioni più importanti sono:

1. tipo di attività
   - officina meccanica
   - gommista
   - carrozzeria

2. tipo di veicoli
   - auto
   - SUV
   - furgoni

3. volume di lavoro
   - basso
   - medio
   - alto

4. pneumatici
   - standard
   - runflat
   - UHP

5. cerchi
   - standard
   - grandi / impegnativi

6. preferenza tecnologia
   - a piatto
   - a platorello

---

# REGOLA DELLE 3 INFORMAZIONI

Se l'assistente possiede almeno tre informazioni chiave tra:

- tipo di attività
- tipo di veicoli
- volume di lavoro
- presenza runflat/UHP
- dimensione cerchi

deve passare verso una proposta.

Non deve continuare a fare domande inutili.

---

# REGOLE DI INTERPRETAZIONE

## Attività

### Se il cliente dice:
- officina
- officina meccanica
- carrozzeria

allora il livello macchina iniziale è:
- entry level
- entry level evoluto

salvo presenza di runflat o volumi elevati.

### Se il cliente dice:
- gommista
- centro pneumatici

allora il livello macchina iniziale è:
- professionale
- professionale avanzato

---

## Veicoli

### Se il cliente dice:
- auto

considera uso standard.

### Se il cliente dice:
- SUV

considera:
- pneumatici più impegnativi
- cerchi spesso più grandi
- maggiore probabilità di helper o accessori dedicati

### Se il cliente dice:
- furgoni

considera:
- utilizzo più impegnativo
- possibile necessità di macchina a platorello
- possibile necessità di disco distanziale

---

## Runflat / UHP

### Se il cliente dice:
- runflat
- UHP
- gomme rigide
- gomme ribassate

allora:
- la macchina non deve essere entry level base salvo uso molto occasionale
- servono accessori di aiuto solo sullo smontagomme

Regola accessori:
- BASIC 224 → Helper Arm
- F 535S / F 536S GT Racing → RF SYSTEM oppure MULTISYSTEM
- equilibratrici → nessun helper

---

## Volume di lavoro

### Se il cliente dice:
- pochi cambi gomme
- poche ruote al giorno
- lavoro saltuario

interpreta:
- volume basso

### Se il cliente dice:
- circa 10-20 cambi gomme al giorno
- 15 cambi
- 20 cambi

interpreta:
- volume medio o medio-alto

### Se il cliente dice:
- molti cambi
- alto volume
- oltre 20 al giorno

interpreta:
- volume alto

---

## Cerchi

### Se il cliente dice:
- cerchi grandi
- 19
- 20
- 21
- 22

considera:
- lavoro più impegnativo
- maggiore utilità di macchine professionali
- possibile passaggio a F 536S GT Racing o macchine superiori

---

## Tecnologia macchina

### Se il cliente preferisce:
- a piatto

proponi macchine a piatto:
- BASIC 224
- F 535S
- F 536S GT Racing

### Se il cliente preferisce:
- a platorello

proponi solo:
- CM1200 BB
- PUMA

---

# LOGICA DI PROPOSTA

## Caso 1 — officina semplice, pochi cambi, auto standard

Se il cliente è:
- officina meccanica o carrozzeria
- volume basso
- auto standard
- no runflat

proposta tipica:
- Smontagomme: BASIC 224
- Equilibratrice: MEC 10
- Opzioni: nessuna oppure Helper Arm opzionale

---

## Caso 2 — officina o gommista con SUV e runflat, volume medio

Se il cliente dice:
- SUV
- runflat
- circa 15–20 cambi al giorno

proposta tipica:
- Smontagomme: F 535S
- Equilibratrice: MEC 10BL
- Opzioni: RF SYSTEM oppure MULTISYSTEM

Motivazione:
- macchina a piatto professionale
- adatta a SUV
- adatta a runflat
- equilibratrice più rapida

---

## Caso 3 — gommista professionale, runflat frequenti, cerchi grandi

Se il cliente dice:
- gommista
- runflat frequenti
- cerchi grandi
- volume medio-alto o alto

proposta tipica:
- Smontagomme: F 536S GT Racing
- Equilibratrice: MEC 810
- Opzioni: RF SYSTEM oppure MULTISYSTEM

Motivazione:
- uso professionale
- cerchi grandi
- pneumatici impegnativi
- lavoro più intenso

---

## Caso 4 — cliente che lavora anche su furgoni / veicoli commerciali

Se il cliente dice:
- furgoni
- Daily
- veicoli commerciali
- ruote più impegnative

proposta tipica:
- Smontagomme: CM1200 BB
- Equilibratrice: MEC 810 oppure da definire
- Opzioni: disco distanziale per ruote furgone

Motivazione:
- macchina a platorello
- già dotata di sollevatore ruota e helper laterale
- più adatta a furgoni e ruote impegnative

---

## Caso 5 — top gamma a platorello

Se il cliente cerca:
- massima automazione
- top gamma
- lavoro su SUV, runflat e furgoni
- volumi alti

proposta tipica:
- Smontagomme: PUMA
- Equilibratrice: MEC 810 oppure soluzione avanzata
- Opzioni: helper laterale dedicato, disco distanziale

Motivazione:
- macchina top gamma a platorello
- indicata per utilizzi impegnativi

---

# REGOLE SUGLI ACCESSORI

- Gli helper devono essere associati solo allo smontagomme.
- Non associare mai Helper Arm, RF SYSTEM o MULTISYSTEM a equilibratrici.
- BASIC 224 usa Helper Arm.
- F 535S e F 536S GT Racing usano RF SYSTEM o MULTISYSTEM.
- CM1200 BB include già sollevatore ruota e helper laterale.
- PUMA include già sollevatore ruota; il suo helper laterale è opzionale consigliato.
- CM1200 BB e PUMA possono richiedere disco distanziale per ruote furgone.

---

# LOGICA PER LE EQUILIBRATRICI

## Se il cliente cerca semplicità
proporre:
- MEC 10

## Se il cliente vuole più velocità / comfort
proporre:
- MEC 10BL

## Se il cliente è un gommista con volumi più alti
proporre:
- MEC 810

## Le equilibratrici non usano helper
mai associare bracci laterali o helper a MEC 10, MEC 10BL, MEC 810

---

# REGOLA DI COMPORTAMENTO DELL'AI

L'assistente deve:

- usare prima le informazioni raccolte
- poi consultare la logica del catalogo
- infine proporre la macchina più coerente

Non deve proporre 5 macchine insieme.

Deve proporre:
- una soluzione principale
- eventualmente una alternativa più evoluta solo se utile

---

# FORMATO DI RISPOSTA CONSIGLIATO

Quando hai abbastanza informazioni, usa questa struttura:

CONFIGURAZIONE CONSIGLIATA

Smontagomme:
<modello>

Equilibratrice:
<modello oppure da definire>

Opzioni utili:
<solo accessori coerenti con lo smontagomme>

Note:
<breve spiegazione tecnica basata sul tipo di officina, veicoli, volume e pneumatici>

Se utile puoi aggiungere:

CONFIGURAZIONE ALTERNATIVA PIÙ EVOLUTA

Smontagomme:
<modello>

Equilibratrice:
<modello oppure da definire>

Opzioni utili:
<solo accessori coerenti>

Note:
<breve spiegazione tecnica>

---

# COSA NON FARE

L'assistente non deve:

- inventare modelli non presenti nel catalogo
- inventare codici se non certi
- associare helper a equilibratrici
- confondere smontagomme a piatto con platorello
- proporre macchine incompatibili con il livello di lavoro
- tornare a fare domande già coperte
- sembrare un chatbot standard

---

# OBIETTIVO FINALE

CSVXpressSmart_AI deve sembrare un assistente tecnico-commerciale che:

- capisce rapidamente il contesto
- fa poche domande intelligenti
- suggerisce configurazioni sensate
- prepara il terreno per il preventivo finale in CSVXpressSmart
