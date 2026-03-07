# Knowledge Base — Smontagomme Auto

## Contesto
Questa base di conoscenza serve a CSVXpressSmart_AI per aiutare il cliente a scegliere lo smontagomme auto più adatto in base al tipo di lavoro.

## Prima distinzione
La prima distinzione utile è:

- smontagomme a piatto
- smontagomme con platorello

## Smontagomme a piatto

### Basic 224
Categoria: entry level

Caratteristiche principali:
- macchina semplice e affidabile
- 2 velocità
- adatta a piccole officine e carrozzerie
- palo che scende sul piatto con sistema a molla
- può essere integrata con Helper Arm

Quando proporla:
- cliente con volumi bassi o medio-bassi
- uso non estremo
- attività generica auto
- piccola officina
- carrozzeria
- budget orientato a una soluzione base ma seria

Limiti:
- meno evoluta rispetto a macchine professionali
- meno adatta a lavorazioni continue e impegnative

### F 535S
Categoria: professionale

Caratteristiche principali:
- macchina più professionale
- braccio/palo pneumatico
- maggiore comodità e rapidità d’uso
- configurabile con motore a 2 velocità oppure inverter
- più adatta a lavori frequenti e più impegnativi
- può essere integrata con Helper Arm

Versioni:
- 2 velocità
- inverter

Quando proporla:
- cliente che lavora spesso su auto, SUV, pneumatici più impegnativi
- officine con volume medio o medio-alto
- gommisti
- chi cerca una macchina più evoluta del basic

Punti forti:
- maggiore controllo
- più comfort operativo
- impostazione più professionale

## Helper Arm
Descrizione:
Braccio laterale di aiuto utile in particolare con:
- runflat
- UHP
- pneumatici rigidi
- cerchi impegnativi

Quando proporlo:
- se il cliente lavora spesso su runflat
- se il cliente fa un numero importante di cambi gomme
- se il cliente tratta SUV o cerchi importanti
- se vuole ridurre fatica e aumentare praticità

## Smontagomme con platorello
Categoria: più evoluta

Descrizione:
- soluzione più professionale
- adatta a lavorazioni più impegnative o ripetitive
- utile quando il cliente tratta gomme più difficili o cerca una soluzione superiore

Regola conversazionale:
Se il cliente chiede una soluzione molto professionale o lavora molto su pneumatici difficili, il bot può introdurre la categoria "con platorello", ma senza inventare modelli se non ancora presenti nella knowledge base.

## Logica di proposta
### Se il cliente dice:
- piccola officina
- pochi cambi gomme
- lavoro standard
→ orientamento: Basic 224

### Se il cliente dice:
- gommista
- SUV
- runflat
- volume medio o alto
→ orientamento: F 535S

### Se il cliente dice:
- molti runflat
- lavoro più evoluto
- macchina superiore
→ orientamento: F 535S con Helper Arm
oppure introdurre categoria con platorello

## Linguaggio suggerito
Il bot non deve parlare in modo troppo tecnico.
Deve spiegare differenze in modo semplice.

Esempio corretto:
- Basic 224: soluzione più semplice, adatta a piccoli volumi
- F 535S: macchina più professionale, più adatta a lavori frequenti e impegnativi

## Cosa NON fare
- Non inventare modelli non presenti in questa base
- Non inventare prezzi
- Non promettere disponibilità
- Non usare parole troppo generiche senza collegarle al tipo di utilizzo
