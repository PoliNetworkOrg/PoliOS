# Guida all'installazione / Installation guide

> 🚧 **Schema da completare / Outline to complete.** Ogni riga `📸` indica lo screenshot da aggiungere (salvalo in `docs/images/` e inseriscilo con `![descrizione](images/nome.png)`). Le caselle `[ ]` sono i controlli da fare mentre provi i passaggi.
> Each `📸` line is a screenshot to add (save it in `docs/images/`, insert it with `![description](images/name.png)`). The `[ ]` boxes are things to verify while you try the steps.

**Indice / Contents**: [0. Prima di iniziare](#0-prima-di-iniziare--before-you-start) · [1. Scarica e verifica l'ISO](#1-scarica-e-verifica-liso--download-and-verify-the-iso) · [2A. VirtualBox](#2a-virtualbox) · [2B. VMware](#2b-vmware) · [2C. UTM (Mac Apple Silicon)](#2c-utm-mac-apple-silicon) · [2D. Computer reale](#2d-computer-reale-usb--bare-metal-usb) · [3. Installazione](#3-installazione-del-sistema--installing-the-system) · [4. Primo avvio](#4-primo-avvio-polios-welcome--first-boot-polios-welcome) · [5. Problemi frequenti](#5-problemi-frequenti--troubleshooting)

---

## 0. Prima di iniziare / Before you start

- [ ] Requisiti hardware (vedi [README](../README.md#requisiti-hardware)) / Hardware requirements
- [ ] Backup dei dati se installi su un computer reale / Back up your data if installing on a real computer
- [ ] Per il Wi-Fi del Politecnico: codice persona e password / For Polimi Wi-Fi: your codice persona and password
- 📸 _Schermata che mostra le specifiche del computer (RAM, disco) / Screenshot of the computer's specs_

## 1. Scarica e verifica l'ISO / Download and verify the ISO

1. Scarica l'ISO dal link nella release / Download the ISO from the link in the release: **TODO link**
2. Verifica SHA-256 / Verify SHA-256:
   - macOS / Linux: `shasum -a 256 polios-*.iso` (Linux anche `sha256sum`)
   - Windows (PowerShell): `Get-FileHash polios-*.iso -Algorithm SHA256`
   - [ ] Il risultato coincide con quello della release / Result matches the release
- 📸 _Terminale con il confronto del checksum / Terminal showing the checksum comparison_

---

## 2A. VirtualBox

1. Nuova VM / New VM → tipo **Linux**, versione **Ubuntu (64-bit)** (o "Other Linux 64-bit")
2. RAM ≥ **4096 MB**, CPU ≥ **2**, disco ≥ **25 GB**
3. Display → **Graphics Controller: VMSVGA**
4. Storage → collega l'ISO al lettore ottico / attach the ISO to the optical drive
5. Avvia / Start
- 📸 _Creazione VM · impostazioni display (VMSVGA) · selezione ISO_
- [ ] Appunti e ridimensionamento schermo funzionano? / Do clipboard and screen resize work?

## 2B. VMware

1. Nuova VM / New VM (Fusion / Workstation / Player) → "Installa da disco o immagine" / "Install from disc or image"
2. Sistema operativo ospite / Guest OS: **Ubuntu 64-bit** (o Linux → Other Linux 6.x 64-bit)
3. RAM ≥ **4 GB**, CPU ≥ **2**, disco ≥ **25 GB**
4. Avvia / Start
- 📸 _Scelta ISO · scelta del sistema operativo · riepilogo VM_
- [ ] Appunti e ridimensionamento schermo funzionano? / Do clipboard and screen resize work?

## 2C. UTM (Mac Apple Silicon)

> ⚠️ PoliOS è solo **amd64**: su Apple Silicon UTM lo **emula** ed è **lento**. / PoliOS is **amd64 only**: on Apple Silicon UTM **emulates** it and it is **slow**.

1. Nuova VM → **Emula** / New VM → **Emulate** → **Linux**
2. Architettura **x86_64**, RAM ≥ **4096 MB**, core ≥ **2**, disco ≥ **25 GB**
3. Display: **virtio-gpu** (o `virtio-ramfb`) · TODO: verificare / verify
4. ISO nel lettore CD/DVD / ISO in the CD/DVD drive
- 📸 _Nuova VM · architettura · display · avvio_
- [ ] Tempi di avvio e fluidità (nota per il README) / Boot time and smoothness (note for the README)

## 2D. Computer reale (USB) / Bare metal (USB)

1. Scrivi l'ISO su una chiavetta (≥ 8 GB, **si cancella tutto**) / Write the ISO to a USB stick (≥ 8 GB, **everything is erased**):
   - balenaEtcher (macOS / Windows / Linux) oppure Rufus (Windows, modalità **DD** se richiesto)
2. Riavvia ed entra nel menu di avvio / Reboot into the boot menu (TODO: tasti per marca: F12 Lenovo/Dell, F9 HP, Esc/F8 ASUS, Opzione ⌥ Mac Intel…)
3. Scegli la chiavetta / Pick the USB stick
- [ ] Secure Boot: funziona attivo? / does it work enabled?
- 📸 _Etcher · menu di avvio · schermata di avvio di PoliOS (con il logo)_

---

## 3. Installazione del sistema / Installing the system

Dalla sessione live, doppio clic su **Install PoliOS / Installa** (TODO: nome esatto dell'icona).

1. Lingua / Language — 📸
2. Layout tastiera / Keyboard layout — 📸
3. Aggiornamenti e codec multimediali / Updates and multimedia codecs — 📸 (TODO: consigliato spuntare?)
4. Tipo di installazione / Installation type — 📸
   - **Cancella disco e installa / Erase disk and install** (VM: la scelta semplice)
   - **Accanto a un altro sistema (dual boot) / Alongside another OS** — ⚠️ backup prima / back up first — 📸
   - **Altro / Something else** (partizionamento manuale / manual partitioning)
   - [ ] Crittografia del disco (LUKS): funziona con la schermata di avvio PoliOS? / does the PoliOS boot screen show the passphrase prompt?
5. Fuso orario / Time zone (Europe/Rome) — 📸
6. Nome, computer, utente, password / Name, computer name, username, password — 📸
7. Attendi la copia dei file / Wait for the copy — 📸
8. **Riavvia / Restart**, poi togli l'ISO o la chiavetta / then remove the ISO or USB stick — 📸

## 4. Primo avvio: PoliOS Welcome / First boot: PoliOS Welcome

1. Schermata di login con lo sfondo PoliOS / Login screen — 📸
2. Al primo accesso si apre **PoliOS Welcome** / opens at first login — 📸
3. **Pagina Wi-Fi** (solo se c'è un adattatore Wi-Fi) / (only with a Wi-Fi adapter):
   - Nome utente = **codice persona** (`@polimi.it` si aggiunge da solo) / adds `@polimi.it` automatically
   - Password Polimi · opzione Ethernet 802.1X solo per le prese cablate del campus / only for campus wired ports
   - Puoi **saltare** / You can **skip** — 📸
4. **Pagina corsi** / Courses page: spunta i tuoi corsi → **Installa** / tick your courses → **Install** — 📸
   - Passa il mouse su un corso per vedere i pacchetti / hover a course to see its packages
   - Pulsante **English / Italiano** in basso a sinistra / language button bottom left — 📸
   - Serve Internet / Internet is required
5. Inserisci la password dell'utente quando richiesta / enter your user password when asked — 📸
6. **Tutto pronto / All set** — 📸
- Riaprire la procedura / Reopen it: menu applicazioni → **PoliOS Welcome** — 📸

## 5. Problemi frequenti / Troubleshooting

| Problema / Problem | Cosa fare / What to do |
|---|---|
| Nessuna pagina Wi-Fi nella procedura / No Wi-Fi page | Nelle VM è normale (nessun adattatore). Su PC reale controlla che il Wi-Fi sia visibile al sistema. / Normal in VMs. On real hardware check the system sees the adapter. |
| "Nessuna connessione a Internet" nella pagina corsi / "No internet" on the courses page | Collegati e riapri PoliOS Welcome dal menu. / Connect and reopen it from the menu. |
| Il Wi-Fi smette di funzionare dopo un po' / Wi-Fi stops working later | Le password Polimi scadono: aggiorna la password con PoliOS Welcome. / Polimi passwords expire: update it with PoliOS Welcome. |
| Schermo piccolo o appunti non condivisi in VM / Small screen or no clipboard in VM | TODO: strumenti ospite per ogni hypervisor / guest tools per hypervisor |
| Avvio dalla chiavetta non riesce / Can't boot from USB | TODO: Secure Boot, modalità UEFI/Legacy, riscrittura chiavetta / rewrite the stick |
| TODO | TODO |

**Non trovi la soluzione? / Still stuck?** Apri una [segnalazione](../../../issues/new/choose) / Open an [issue](../../../issues/new/choose).
