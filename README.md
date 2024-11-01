# Descrizione progetto

Una libreria Python per la generazione, validazione e decodifica del codice fiscale italiano. La libreria permette di creare un codice fiscale a partire dai dati anagrafici, verificarne la correttezza e ottenere informazioni come sesso, data e luogo di nascita.

## Installazione

Per installare la libreria, utilizzare pip:

```bash
pip install codicefiscale-ita
```
## Funzionalità
- **Generazione Codice Fiscale**: Crea un codice fiscale da dati anagrafici.
- **Validazione Codice Fiscale**: Verifica la correttezza del codice fiscale.
- **Estrazione Informazioni**: Rileva sesso, data e luogo di nascita dal codice fiscale.

## Requisiti di Sistema
La libreria richiede Python 3.7 o superiore.

## Utilizzo
- ### Generazione del Codice Fiscale
Genera un codice fiscale a partire dai dati personali come cognome, nome, sesso, data di nascita e comune di nascita.

```
from codicefiscale import genera_codice_fiscale

codice_fiscale = genera_codice_fiscale(
    cognome="Rossi",
    nome="Mario",
    sesso="M",
    data_nascita="01/01/1985",
    comune="Roma"
)
print(codice_fiscale)  # Output: RSSMRA85A01H501Z
```

- ### Validazione del Codice Fiscale
Verifica se un codice fiscale è valido e conforme agli standard.

```
from codicefiscale import is_valido_codice_fiscale

try:
    is_valido_codice_fiscale("RSSMRA85A01H501Z")
    print("Codice fiscale valido")
except ValueError as e:
    print(f"Codice fiscale non valido: {e}")
```

### Estrazione di Informazioni dal Codice Fiscale
#### Sesso
Estrae il sesso dal codice fiscale.

```
from codicefiscale import get_sesso

sesso = get_sesso("RSSMRA85A01H501Z")
print(sesso)  # Output: M
```
#### Data di Nascita
Estrae la data di nascita dal codice fiscale.

```
from codicefiscale import get_data_nascita

data_nascita = get_data_nascita("RSSMRA85A01H501Z")
print(data_nascita)  # Output: 01/01/1985
```
#### Comune di Nascita
Estrae il comune di nascita dal codice fiscale.

```
from codicefiscale import get_comune

comune = get_comune("RSSMRA85A01H501Z")
print(comune)  # Output: Roma
```

## Contributi
I contributi sono benvenuti! Se hai suggerimenti, segnalazioni di bug o nuove funzionalità da proporre, sentiti libero di aprire una issue o di fare una pull request sul repository GitHub.

## Licenza
Questa libreria è rilasciata sotto la licenza MIT. Per ulteriori informazioni, consulta il file LICENSE.

## Contatti
Per ulteriori informazioni, contattaci a filippo.casadei2004@gmail.com.