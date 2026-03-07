# Catalogo tecnico (senza prezzi) — CSVXpressSmart_AI

Questo catalogo serve come base di conoscenza per l'assistente CSVXpressSmart_AI.

Il catalogo contiene:
- categorie di macchine
- modelli disponibili
- logica di utilizzo
- suggerimenti di configurazione

Non contiene prezzi.
I prezzi reali sono gestiti dal sistema CSVXpressSmart tramite listino.

---

# PRIMA DOMANDA UTILE

Quando un cliente chiede uno smontagomme o un preventivo, la prima distinzione utile è:

Preferisci uno smontagomme **a piatto** oppure **con platorello**?

Questa domanda aiuta a capire il livello di macchina necessario.

---

# SMONTAGOMME AUTO

## Smontagomme a piatto — Entry Level

### F 524

Target:
- officine meccaniche
- carrozzerie
- piccoli gommisti

Uso tipico:
- volumi medio-bassi
- pneumatici standard

Caratteristiche:
- macchina semplice e affidabile
- motore 2 velocità
- funzionamento classico a piatto

Accessori consigliati:
- Helper Arm (se presenti runflat occasionali)

---

### F 524S

Categoria: entry level evoluto

Target:
- officine
- piccoli gommisti

Caratteristiche:
- macchina più robusta
- buona versatilità

Accessori consigliati:
- Helper Arm

---

### F 524 SW

Categoria: entry level professionale

Target:
- officine con un po’ più di lavoro

Caratteristiche:
- macchina più completa
- maggiore stabilità operativa

Accessori consigliati:
- Helper Arm
- accessori runflat

---

# SMONTAGOMME AUTO — PROFESSIONALE

### F 535

Target:
- gommisti
- officine con volumi medi

Caratteristiche:
- macchina più robusta
- maggiore produttività

Accessori consigliati:
- Helper Arm
- accessori runflat

---

### F 535S

Categoria: professionale avanzata

Target:
- gommisti
- officine con SUV
- presenza di pneumatici runflat
- volumi medi o medio-alti

Caratteristiche:
- braccio/palo pneumatico
- maggiore velocità operativa

Motorizzazione configurabile:
- 2 velocità
- inverter (controllo modulato)

Accessori consigliati:
- Helper Arm
- kit runflat

Quando proporla:
- SUV
- runflat frequenti
- 15–30 cambi gomme giorno

---

### F 536S GT Racing

Categoria: professionale evoluta

Target:
- gommisti
- pneumatici performanti
- cerchi grandi
- volumi medio-alti

Caratteristiche:
- macchina più veloce
- progettata per lavori intensivi

Accessori consigliati:
- Helper Arm
- inverter

---

### F 528S GT MI

Categoria: professionale avanzata

Target:
- gommisti
- lavoro frequente su SUV

Caratteristiche:
- macchina ergonomica
- maggiore comfort operatore

Accessori consigliati:
- Helper Arm
- accessori runflat

---

# SMONTAGOMME LIVELLO SUPERIORE

### CM 1200BB

Categoria:
macchina evoluta

Uso tipico:
- gommisti professionali
- lavorazioni impegnative

---

### LIGRO MI

Categoria:
alta gamma

Uso tipico:
- gommisti professionali
- lavori intensivi

Caratteristiche:
- maggiore automazione
- maggiore comfort operatore

---

### PUMA MI

Categoria:
top gamma

Uso tipico:
- gommisti ad alto volume
- pneumatici difficili
- cerchi grandi

Caratteristiche:
- massimo livello di automazione
- minimo sforzo operatore

---

# EQUILIBRATRICI / BILANCIATRICI AUTO

## Livello base

### MEC 5

Uso tipico:
- piccole officine
- uso occasionale

Caratteristiche:
- semplice
- affidabile

---

### MEC 5B

Versione evoluta MEC 5.

---

### MEC 10

Categoria:
standard officina

Target:
- officine meccaniche
- piccoli gommisti

Caratteristiche:
- equilibratrice semplice
- affidabile
- uso quotidiano

---

### MEC 10B

Versione evoluta MEC 10.

---

### MEC 10BL

Categoria:
standard avanzato

Caratteristiche:
- bloccaggio automatico
- maggiore velocità operativa

---

# EQUILIBRATRICI LIVELLO INTERMEDIO

### MEC 20
### MEC 20L
### MEC 200
### MEC 200A

Uso tipico:
- gommisti
- officine con volumi medi

---

# EQUILIBRATRICI PROFESSIONALI

### MEC 810
### MEC 810VD
### MEC 810VDB
### MEC 810VDBL

Uso tipico:
- gommisti professionali
- volumi medio-alti

---

# EQUILIBRATRICI AVANZATE

### MEC 820
### MEC 820VDL
### Touch MEC 1000

Categoria:
top gamma

Caratteristiche:
- touchscreen
- maggiore automazione

Uso tipico:
- centri pneumatici
- officine ad alto volume

---

# ACCESSORI IMPORTANTI

## Helper Arm

Descrizione:
braccio laterale di aiuto per smontagomme.

Utilità:
- runflat
- pneumatici UHP
- cerchi difficili

Quando proporlo:
- SUV
- runflat
- volumi medi o alti

---

## Inverter

Descrizione:
controllo elettronico della velocità del motore.

Vantaggi:
- maggiore precisione
- maggiore comfort operatore

---

## RF System

Sistema dedicato per pneumatici runflat.

---

## Multi System

Sistema per lavorazioni versatili su cerchi complessi.

---

# CHECKLIST QUALIFICAZIONE CLIENTE

Durante la conversazione l'assistente dovrebbe raccogliere queste informazioni:

1. Tipo attività
   - officina meccanica
   - gommista
   - carrozzeria

2. Tipo veicoli
   - auto
   - SUV
   - furgoni

3. Volume di lavoro
   - pochi cambi gomme giorno
   - medio
   - alto

4. Pneumatici
   - standard
   - runflat
   - UHP

5. Dimensione cerchi più frequente

6. Preferenza macchina
   - entry level
   - professionale

7. Spazio disponibile in officina (se necessario)

---

# LOGICA DI PROPOSTA

Se il cliente dice:

piccola officina  
pochi cambi gomme  

→ configurazione tipica:

Smontagomme: F 524  
Equilibratrice: MEC 10  

---

Se il cliente dice:

SUV  
runflat  
20 cambi gomme giorno  

→ configurazione tipica:

Smontagomme: F 535S  
Equilibratrice: MEC 10BL  
Opzioni: Helper Arm

---

Se il cliente dice:

gommista  
molti runflat  
cerchi grandi  

→ configurazione tipica:

Smontagomme: F 536S GT Racing  
Equilibratrice: MEC 810  
Opzioni: Helper Arm

---

# REGOLE PER L'ASSISTENTE AI

L'assistente deve:

- non inventare modelli non presenti nel catalogo
- non inventare prezzi
- non promettere disponibilità
- fare una domanda alla volta
- usare le informazioni già fornite dal cliente

Quando ha abbastanza dati deve generare il blocco:

[SUGGERIMENTO PER PREVENTIVO]

Smontagomme:
Equilibratrice:
Opzioni:
Note:
