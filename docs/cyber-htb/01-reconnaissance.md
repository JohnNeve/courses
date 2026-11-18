---
title: "Cheatsheet MkDocs Material"
description: "Riferimento completo a tutte le formattazioni disponibili"
tags:
  - template
  - sintassi
  - markdown
---

# Titolo Principale della Pagina (H1)

Questo è un file di riferimento rapido. Puoi copiare e incollare i blocchi che ti servono. 
Puoi usare il testo in **grassetto**, in *corsivo*, o anche ==evidenziato in giallo==.

## 1. Riquadri Colorati (Admonitions)

Usa i riquadri per far risaltare concetti importanti.

!!! note "Nota standard"
    Questo è il riquadro base, utile per definizioni o commenti.

!!! tip "Suggerimento"
    Ottimo per le "best practice" o scorciatoie.

!!! warning "Attenzione"
    Per avvisare di possibili errori non critici.

!!! danger "Pericolo / Errore Critico"
    Da usare per concetti che possono distruggere sistemi (es. `rm -rf`).

!!! example "Esempio Pratico"
    Mostra un esempio di implementazione.

### Riquadri a scomparsa (Collapsible)

??? abstract "Soluzione dell'esercizio (Clicca per espandere)"
    Puoi nascondere il testo usando `???` invece di `!!!`. Ottimo per non spoilerare le soluzioni degli esercizi di programmazione!

???+ success "Riquadro aperto di default"
    Usando `???+` il riquadro è comprimibile ma parte già aperto.

---

## 2. Blocchi di Codice e Terminale

Puoi evidenziare la sintassi di quasi tutti i linguaggi di programmazione e avere il tasto "Copia" in automatico.

```python
# Esempio di codice Python
def saluta(nome):
    print(f"Ciao, {nome}!")
    return True
```

```bash
# Esempio di terminale
sudo apt update && sudo apt upgrade
```

### Schede per confrontare il codice (Tabs)

Le schede sono perfette per mostrare come fare la stessa cosa in linguaggi o sistemi operativi diversi:

=== "Windows (PowerShell)"
    ```powershell
    ipconfig /all
    ```

=== "Linux (Bash)"
    ```bash
    ip a
    ```

=== "Cisco IOS"
    ```text
    show ip interface brief
    ```

---

## 3. Liste e Liste di Controllo (Task)

Le liste classiche:

* Elemento 1
* Elemento 2
    * Sotto-elemento 2.1
    * Sotto-elemento 2.2
* Elemento 3

Le liste di controllo (utili per le metodologie di Penetration Testing):

- [x] Eseguire ping sweep
- [x] Scansione Nmap delle porte aperte
- [ ] Ricerca vulnerabilità sui servizi (da fare)
- [ ] Exploitation (da fare)

---

## 4. Tabelle Dati

Le tabelle sono perfette per riassumere caratteristiche o parametri.

| Protocollo | Porta Predefinita | Trasporto | Uso Principale |
| :--- | :---: | :---: | ---: |
| **HTTP** | 80 | TCP | Navigazione web in chiaro |
| **HTTPS** | 443 | TCP | Navigazione web cifrata |
| **DNS** | 53 | UDP/TCP | Risoluzione nomi a dominio |
| **SSH** | 22 | TCP | Accesso remoto sicuro |

*(I due punti ` : ` nella seconda riga definiscono l'allineamento: sinistra, centro, centro, destra).*

---

## 5. Immagini

Immagine standard con testo alternativo (per accessibilità):
![Schema della Topologia di Rete](img/topologia.png)

Se vuoi aggiungere una didascalia sotto l'immagine, puoi usare l'HTML di base:
<figure>
  <img src="img/topologia.png" alt="Schema della Topologia di Rete" />
  <figcaption>Fig 1. - Architettura di rete aziendale standard</figcaption>
</figure>

---

## 6. Matematica e Formule (LaTeX)

*Nota: Richiede configurazione Javascript aggiuntiva in mkdocs.yml*

Formule all'interno del testo (inline): L'equazione della relatività è $E = mc^2$.

Formula come blocco isolato:
$$
f(x) = \int_{-\infty}^\infty \hat f(\xi)\,e^{2 \pi i \xi x} \,d\xi
$$

---

## 7. Citazioni e Scorciatoie da Tastiera

> Questa è una citazione a blocco (Blockquote).
> Utile per citare manuali, RFC o documentazioni ufficiali.

Se devi indicare scorciatoie da tastiera, usa i tag HTML standard:
Premi <kbd>Ctrl</kbd> + <kbd>C</kbd> per interrompere il processo nel terminale, oppure <kbd>F12</kbd> per aprire gli strumenti di sviluppo.

<iframe 
    src="https://drive.google.com/file/d/1urCOPKL99EHb3hI3S6v6we2ewmU0H7FY/view?usp=drive_link" 
    width="100%" 
    height="600" 
    style="border: none; border-radius: 8px;" 
    allow="autoplay">
</iframe>



<iframe 
    width="100%" 
    style="aspect-ratio: 16/9; border-radius: 8px;" 
    src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
    title="YouTube video player" 
    frameborder="0" 
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
    allowfullscreen>
</iframe>