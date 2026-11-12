# Guida all'acquisto del PC per corso di studio

>  ⚠️ **NOTE**: This page is currently Italian only. English translation is Work in Progress.

**Fonte:** export della chat Telegram ["Consigli per acquisto PC"](https://t.me/joinchat/OOC4qk2QS1FM37aETHuzWQ) (17.961 messaggi con testo, 2020-08 → 2026-10).
Requisiti e programmi cambiano con i docenti e gli anni: per i corsi con affidabilità bassa conviene chiedere conferma nel gruppo Telegram del corso.

## Le tre fasce

| Fascia | Per cosa | CPU | RAM | SSD | GPU | Budget indicativo |
|---|---|---|---|---|---|---|
| **Leggero** | Programmazione, MATLAB, Office. Va bene quasi qualsiasi portatile recente, anche usato. | i5 / Ryzen 5 recente (va bene la serie U) | 16 GB | 512 GB | Integrata | 400-900 € |
| **CAD** | CAD 3D al primo anno, poi MATLAB; in magistrale FEM e CFD. | Serie H (i5/i7, Ryzen 5/7) | 16 GB (32 in magistrale) | 512 GB - 1 TB | Per MRT basta spesso una buona integrata; dedicata con almeno 4 GB di VRAM per margine o per FEM/CFD | 800-1.300 € |
| **Rendering** | BIM, modellazione 3D e rendering di fine progetto. | Serie H (i7 / Ryzen 7) | 32 GB (16 minimo) | 1 TB (+ disco esterno) | Dedicata NVIDIA RTX x060 o superiore, necessaria | 1.100-1.800 € |

I budget sono indicativi, ricavati dalle richieste in chat 2024-2026.

## Per corso

### Ingegneria dell'informazione

#### Ing. Informatica  
*Fascia Leggero · 496 messaggi in chat (affidabilità alta)*

- **Programmi**: Compilatore C (Fondamenti); Cisco Packet Tracer + VM VirtualBox (Reti); Linux per il progetto di API; Java + IntelliJ (Ing. del Software); Vivado (Reti Logiche, 3° anno)
- **CPU**: Qualsiasi x86 recente, anche serie U · **RAM**: 16 GB (32 utili in magistrale) · **SSD**: 512 GB (1 TB se dual boot) · **GPU dedicata**: Non serve
- **Mac**: Sconsigliato: Vivado non esiste per Mac e su Apple Silicon va solo emulato; si ripiega su Citrix, VM o il PC del compagno di progetto.
- **Linux**: Consigliato. L'unico ostacolo citato sono gli esami al PC con SEB.
- **Note**: 'Per inginf un potato PC funzionerà' fino a Vivado al 3° anno. L'usato va benissimo.
- Messaggi di esempio: #20189 #22004 #29008 #28863 #29998 #6708 #26593 #27147

#### Data Science / AI (magistrale)  
*Fascia Leggero · 24 messaggi in chat (affidabilità bassa)*

- **Programmi**: Python + Jupyter; Google Colab / Kaggle per l'addestramento; Docker; CUDA/PyTorch (opzionale)
- **CPU**: 8 core · **RAM**: 16-32 GB · **SSD**: 512 GB - 1 TB · **GPU dedicata**: Non serve
- **Mac**: Possibile, ma alcune librerie e la GPU per il training sono limitate.
- **Linux**: Ideale: Docker vede la GPU NVIDIA solo su Linux (o WSL2).
- **Note**: Le challenge di Deep Learning si fanno con i piani gratuiti di Colab/Kaggle. Una GPU NVIDIA in locale accorcia i tempi ma non è necessaria.
- **Pareri discordanti**: GPU dedicata: per qualcuno serve in magistrale se fai ML/IA (#9533), per altri non serve nemmeno lì (#9539).
- Messaggi di esempio: #8873 #8881 #8862 #18677 #9533 #9539

#### Ing. Elettronica  
*Fascia Leggero · 69 messaggi in chat (affidabilità media)*

- **Programmi**: Compilatore C; MATLAB (segnali); Vivado 2018 (Sistemi Elettronici Digitali); PSpice / LTspice; Microcontrollori
- **CPU**: i5/Ryzen 5 recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: Sconsigliato per Vivado (usabile via virtual desktop del Poli).
- **Linux**: Buono: Vivado e MATLAB sono nativi; PSpice no (LTspice va con Wine).
- **Note**: 'Non ci sono requisiti particolari, se hai già un portatile è molto probabile che vada più che bene'.
- Messaggi di esempio: #29392 #25656 #13215 #21989 #22273

#### Ing. Automazione  
*Fascia Leggero · 95 messaggi in chat (affidabilità media)*

- **Programmi**: MATLAB + Simulink; Excel; C; VS Code; ROS / ROS 2 (Robotics); CoppeliaSim
- **CPU**: 8 core per Simulink nei progetti · **RAM**: 8 GB al 1° anno, 16 GB in magistrale · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: Sconsigliato: ROS su Apple Silicon è 'difficile se non impossibile'.
- **Linux**: Ottimo: ROS è nativo su Ubuntu.
- **Note**: Triennale leggera ('il primo anno useremo solo matlab, excel e C'); in magistrale 16 GB e 8 core per Simulink e robotica.
- Messaggi di esempio: #7075 #9554 #27180 #26633 #26759 #24525

#### Ing. Biomedica  
*Fascia CAD · 73 messaggi in chat (affidabilità media)*

- **Programmi**: MATLAB; SolidWorks; Compilatore C; LabVIEW; Python; Magistrale: Abaqus, Ansys Fluent, ROS, Unity
- **CPU**: Serie H per la magistrale · **RAM**: 16 GB (32 in magistrale con FEM/CFD) · **SSD**: 512 GB · **GPU dedicata**: Consigliata
- **Mac**: Possibile in triennale tranne SolidWorks (Windows).
- **Linux**: Dual boot per SolidWorks; il resto è nativo.
- **Note**: Triennale: 'Matlab, solidworks, un compilatore qualsiasi'. In magistrale, con Abaqus e Fluent, si consiglia serie H, 16 GB e GPU dedicata.
- Messaggi di esempio: #6875 #19934 #16391 #9281 #19936

#### Ing. Matematica  
*Fascia Leggero · 84 messaggi in chat (affidabilità media)*

- **Programmi**: C (Code::Blocks); MATLAB (Analisi Numerica); R; Python; AMPL
- **CPU**: Qualsiasi recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: Va bene: 'usiate solo MatLab, Python, R e altra roba molto portabile'.
- **Linux**: Va bene, tutto nativo.
- **Note**: La GPU dedicata non serve in triennale; in magistrale può servire a seconda del percorso.
- Messaggi di esempio: #5269 #13225 #23565 #9047 #27042 #28240

#### Ing. Fisica  
*Fascia Leggero · 35 messaggi in chat (affidabilità bassa)*

- **Programmi**: MATLAB; Python; C; ROOT / Geant4 (fisica delle particelle)
- **CPU**: Qualsiasi recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: Va bene per MATLAB e Python; ROOT e Geant4 sono più comodi su Linux.
- **Linux**: Ottimo: ROOT e Geant4 nascono su Linux.
- **Note**: Pochi messaggi in chat: confermare sul gruppo del corso. Le simulazioni Monte Carlo usano la CPU, non la GPU.
- Messaggi di esempio: #10887 #28671 #22633 #22636

### Ingegneria industriale

#### Ing. Gestionale  
*Fascia Leggero · 123 messaggi in chat (affidabilità media)*

- **Programmi**: C; Excel; MATLAB base (magistrale)
- **CPU**: Qualsiasi recente · **RAM**: 8-16 GB · **SSD**: 256-512 GB · **GPU dedicata**: Non serve
- **Mac**: Va bene se i programmi del piano di studi ci sono.
- **Linux**: Va bene; Excel via web o LibreOffice.
- **Note**: 'A parte programmare in C ed usare excel non molto altro'. Alcune attività extracurricolari molto diffuse (es. il JEMP) usano software solo Windows.
- Messaggi di esempio: #10580 #13362 #17286 #25860 #10594

#### Ing. Meccanica  
*Fascia CAD · 293 messaggi in chat (affidabilità alta)*

- **Programmi**: Inventor, SolidWorks, Solid Edge (MRT, 1° anno); C + MATLAB (Informatica B); Inventor + CATIA (3° anno); Magistrale: Abaqus, Ansys, HyperMesh, Rhino, CFD
- **CPU**: i5/R5 recente in triennale; serie H in magistrale · **RAM**: 16 GB (32 in magistrale) · **SSD**: 512 GB - 1 TB · **GPU dedicata**: Consigliata
- **Mac**: Sconsigliato: i CAD del primo anno sono solo Windows.
- **Linux**: Solo in dual boot: 'per ingegneria meccanica sei obbligato ad avere Windows'.
- **Note**: Il PC serve soprattutto al primo semestre (MRT) e al terzo anno. Serve un portatile per i laboratori; in aula il Poli può prestarne uno durante le esercitazioni di CAD.
- **Pareri discordanti**: GPU dedicata per MRT: molti dicono che basta una buona grafica integrata; altri consigliano almeno 4 GB di VRAM. Diventa indispensabile con FEM/CFD in magistrale.
- Messaggi di esempio: #21843 #9384 #16518 #19468 #28496 #29859 #11072 #24178 #27956

#### Ing. Aerospaziale  
*Fascia CAD · 313 messaggi in chat (affidabilità alta)*

- **Programmi**: SolidWorks, Solid Edge, Inventor (MRT); MATLAB (dal 2° anno, molto); C; Magistrale CFD: Ansys Fluent, OpenFOAM, SU2, Gmsh, ParaView, XFLR5
- **CPU**: Serie H, 8+ core per la CFD · **RAM**: 16 GB (32 per CFD) · **SSD**: 1 TB · **GPU dedicata**: Consigliata
- **Mac**: Sconsigliato: 'Solo Matlab esiste per macOs'.
- **Linux**: Dual boot per i CAD; per la CFD in magistrale Linux è la scelta migliore (OpenFOAM, SU2).
- **Note**: 16 GB in triennale, 32 GB e 1 TB se farai CFD. Per le associazioni studentesche tecniche serve una GPU dedicata.
- **Pareri discordanti**: GPU dedicata in triennale: 'per Metodi di rappresentazione tecnica basta un'APU decente' contro chi consiglia almeno 4 GB di VRAM. Tutti concordano che serve solo con la CFD (magistrale o associazioni).
- Messaggi di esempio: #17432 #22531 #21844 #13190 #21771 #3685 #27956 #26189 #24178 #28630 #19132 #27460

#### Ing. Energetica  
*Fascia CAD · 106 messaggi in chat (affidabilità media)*

- **Programmi**: Inventor, SolidWorks, Solid Edge (MRT); MATLAB; C; AutoCAD
- **CPU**: i5/i7 recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Consigliata
- **Mac**: Sconsigliato (CAD solo Windows).
- **Linux**: Solo in dual boot.
- **Note**: Dopo MRT 'non dovrò usarlo in futuro': il carico pesante è concentrato al primo anno.
- **Pareri discordanti**: GPU dedicata per MRT: consigliata da molti (4 GB di VRAM), ma per i corsi del primo anno basta anche un'integrata recente.
- Messaggi di esempio: #1059 #14217 #16667 #16730 #12571 #28040

#### Ing. Elettrica  
*Fascia CAD · 33 messaggi in chat (affidabilità bassa)*

- **Programmi**: MATLAB + Simulink (Modellistica); Mathcad; PSpice; AutoCAD; Solid Edge (3° anno); DIALux; PowerWorld (magistrale)
- **CPU**: i5 recente o superiore · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: 'Un Mac è da escludersi praticamente a priori'.
- **Linux**: Solo in dual boot (Mathcad, DIALux, Solid Edge sono Windows).
- **Note**: Simulink con molti dati riempie la RAM: meglio RAM espandibile.
- Messaggi di esempio: #23342 #22630 #1838

#### Ing. Chimica  
*Fascia Leggero · 27 messaggi in chat (affidabilità bassa)*

- **Programmi**: MATLAB; Excel; Mathcad; Visual Studio; Fluent / COMSOL / OpenFOAM; Aspen HYSYS e Granta (dal virtual desktop)
- **CPU**: i5/R5 recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: Possibile con limiti (Mathcad, Aspen).
- **Linux**: Possibile con Citrix per Aspen/Granta.
- **Note**: 'A chimica una 3050 è già tanto'.
- Messaggi di esempio: #17532 #18775 #16197

#### Ing. Materiali e Nanotecnologie  
*Fascia Leggero · 18 messaggi in chat (affidabilità bassa)*

- **Programmi**: MATLAB; Excel; AutoCAD / SolidWorks; Granta EduPack
- **CPU**: i5/R5 recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Consigliata
- **Mac**: Possibile con limiti.
- **Linux**: Dual boot per il CAD.
- **Note**: Pochi messaggi in chat: confermare sul gruppo del corso. Sconsigliati i Surface (batteria e prestazioni).
- **Pareri discordanti**: GPU: nel 2023 si consigliava una dedicata (#18229), nel 2026 '32GB di Ram e scheda video integrata' (#29597).
- Messaggi di esempio: #18226 #18452 #4241 #29597 #18227

### Ingegneria civile e ambientale

#### Ing. Civile  
*Fascia CAD · 32 messaggi in chat (affidabilità bassa)*

- **Programmi**: AutoCAD; Software strutturali (magistrale strutture); MATLAB; Excel
- **CPU**: Ryzen 7 / i7 recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Consigliata
- **Mac**: Sconsigliato.
- **Linux**: Dual boot.
- **Note**: Pochi messaggi in chat: confermare sul gruppo del corso. Un esame di Geometria si svolge al PC.
- Messaggi di esempio: #4541 #9620 #15738

#### Ing. Edile / Edile-Architettura  
*Fascia Rendering · 57 messaggi in chat (affidabilità media)*

- **Programmi**: AutoCAD; Revit; Rhinoceros; Adobe (Photoshop); Excel
- **CPU**: Serie H · **RAM**: 16 GB minimo · **SSD**: 512 GB - 1 TB · **GPU dedicata**: Necessaria
- **Mac**: Sconsigliato (Revit solo Windows).
- **Linux**: Dual boot.
- **Note**: Il prof di Disegno Edile ha indicato almeno 16 GB di RAM, una buona scheda video e almeno 500 GB di disco. Schermo: circa 100% sRGB e 300 nit.
- Messaggi di esempio: #20790 #21456 #19160 #27330 #12160

#### Ing. Ambientale  
*Fascia Leggero · 20 messaggi in chat (affidabilità bassa)*

- **Programmi**: C, SQL, Excel (1° anno); MATLAB; R; QGIS / ArcGIS (magistrale); CAD
- **CPU**: i5/R5 recente · **RAM**: 16 GB · **SSD**: 512 GB · **GPU dedicata**: Non serve
- **Mac**: Possibile con limiti (ArcGIS).
- **Linux**: Buono: QGIS, R e MATLAB sono nativi.
- Messaggi di esempio: #16318 #17253 #25595

### Architettura e urbanistica

#### Architettura  
*Fascia Rendering · 434 messaggi in chat (affidabilità alta)*

- **Programmi**: AutoCAD; Revit (BIM); Rhinoceros + Grasshopper; SketchUp, ArchiCAD; Adobe Photoshop, Illustrator, InDesign; 3ds Max, V-Ray, Lumion, Enscape
- **CPU**: Serie H (i7 / Ryzen 7) · **RAM**: 32 GB (16 minimo) · **SSD**: 1 TB + disco esterno · **GPU dedicata**: Necessaria
- **Mac**: Regge i primi 1-2 anni (AutoCAD, Adobe, SketchUp, Rhino), poi Revit e i motori di render richiedono Windows (Parallels, a pagamento).
- **Linux**: Non praticabile come unico sistema: quasi nessuno dei programmi del corso gira su Linux.
- **Note**: 'Ad architettura vi servono delle macchine potenti con scheda grafica dedicata, che altrimenti a fine progetto il rendering non lo fate'. I programmi da soli occupano 100+ GB.
- Messaggi di esempio: #24886 #24857 #25429 #15077 #12417 #23721

#### Urbanistica  
*Fascia Rendering · 12 messaggi in chat (affidabilità bassa)*

- **Programmi**: QGIS; ArcGIS; AutoCAD; Adobe; Rendering 3D
- **CPU**: Serie H · **RAM**: 16-32 GB · **SSD**: 1 TB · **GPU dedicata**: Necessaria
- **Mac**: Possibile con limiti (ArcGIS).
- **Linux**: Parziale: QGIS è nativo, il resto no.
- **Note**: Gli shapefile pesano: molta RAM e SSD capiente. Conta la fedeltà cromatica dello schermo.
- Messaggi di esempio: #26271 #29798 #26699 #25957 #9365

### Design

#### Design del Prodotto  
*Fascia Rendering · 120 messaggi in chat (affidabilità media)*

- **Programmi**: Rhinoceros 7/8; SolidWorks; Autodesk Alias; KeyShot; Blender, Cinema 4D; AutoCAD; Adobe
- **CPU**: Serie H · **RAM**: 16-32 GB · **SSD**: 1 TB · **GPU dedicata**: Necessaria
- **Mac**: Sconsigliato: SolidWorks e Alias sono solo Windows, KeyShot e i render beneficiano di GPU NVIDIA.
- **Linux**: Non praticabile come unico sistema.
- **Note**: Conta anche lo schermo (copertura colore).
- Messaggi di esempio: #21774 #27997 #16442 #21497 #22700

#### Design degli Interni  
*Fascia Rendering · 93 messaggi in chat (affidabilità media)*

- **Programmi**: AutoCAD; Revit; 3ds Max + motore di render; Adobe Photoshop, Illustrator, InDesign
- **CPU**: Serie H · **RAM**: 32 GB (16 minimo) · **SSD**: 1 TB · **GPU dedicata**: Necessaria
- **Mac**: Sconsigliato (Revit, 3ds Max solo Windows).
- **Linux**: Non praticabile come unico sistema.
- **Note**: Schermo con buona qualità del pannello (es. serie ProArt); sotto i 1000 € il Full HD va bene. Recentemente consigliate RTX 5060 e 32 GB.
- Messaggi di esempio: #23001 #23696 #28371 #24074 #25429 #29418 #27095 #25629

#### Design della Comunicazione  
*Fascia Leggero · 65 messaggi in chat (affidabilità media)*

- **Programmi**: Adobe InDesign, Illustrator, Photoshop, After Effects, Premiere; Blender; Figma; AutoCAD / 3ds Max (occasionale)
- **CPU**: Recente · **RAM**: 16 GB minimo, 32 consigliati · **SSD**: 512 GB - 1 TB · **GPU dedicata**: Consigliata
- **Mac**: Va bene: è l'unico Design dove il Mac è una scelta sensata (con abbastanza RAM).
- **Linux**: Non praticabile come unico sistema (Adobe).
- **Note**: 'Per UI design su Figma ti basta un Air'; per video e 3D serve più potenza.
- Messaggi di esempio: #20256 #22408 #22848 #29372 #21497 #22410

#### Design della Moda  
*Fascia Rendering · 32 messaggi in chat (affidabilità bassa)*

- **Programmi**: Adobe CC (Illustrator, Photoshop); SolidWorks; KeyShot; Lectra Kaledo; CLO 3D
- **CPU**: Serie H · **RAM**: 16 GB · **SSD**: 512 GB - 1 TB · **GPU dedicata**: Necessaria
- **Mac**: Sconsigliato (SolidWorks, Kaledo solo Windows).
- **Linux**: Non praticabile come unico sistema.
- **Note**: Una RTX 3060 basta. Il portatile è necessario, un tablet grafico è comodo ma non indispensabile.
- Messaggi di esempio: #21953 #24238 #25406 #12641 #25427 #19225

## Consigli generali (dai messaggi fissati e dalle risposte ricorrenti)

- **Prima i programmi, poi il PC.** Guarda il piano di studi o chiedi nel gruppo del corso quali software userai; i CAD e il rendering sono ciò che decide GPU e sistema operativo.
- **Non serve comprare subito.** Per le ingegnerie il primo semestre è leggero: se hai già un portatile, provalo e cambialo quando capisci cosa ti serve.
- **RAM**: 8 GB iniziano a essere pochi, punta a 16 GB. Controlla che la RAM non sia saldata, così puoi espanderla.
- **CPU**: le sigle U e T privilegiano la batteria, la H le prestazioni. Per CAD e rendering serve la serie H.
- **SSD**: 512 GB come minimo; 1 TB per Architettura, Design o per il dual boot. Per l'archivio c'è 1 TB di OneDrive con l'account del Poli.
- **Mac**: nella maggior parte dei corsi è sconsigliato. Molti programmi sono solo Windows/Linux x86 e su Apple Silicon serve Parallels a pagamento con Windows ARM in emulazione. Fa eccezione Design della Comunicazione.
- **Schermo** (Architettura, Edile, Design, Urbanistica): punta a circa 100% sRGB e 300 nit; sotto i 1000 € il Full HD va bene.
- **Dimensioni**: in chat si sconsigliano i 17,3 pollici, troppo ingombranti da portare ogni giorno. Serve comunque un portatile, non solo un fisso: laboratori e lavori di gruppo si fanno in aula.
- **Niente processori ARM** (Snapdragon / Windows on ARM): in chat sono sconsigliati perché molti programmi universitari sono solo x86. Vale anche per chi vuole metterci Linux.
- **Tablet**: non sostituisce il portatile; è utile per gli appunti (OneNote, GoodNotes, Notability) e 64 GB bastano. Spesso conviene portatile + tablet rispetto a un 2-in-1.
- **Licenze**: i programmi richiesti dai corsi si ottengono gratis con l'account del Poli (software.polimi.it); di solito le istruzioni arrivano alla prima lezione. Adobe è riservato a Design e ai corsi che lo usano.
- **Senza Windows**: il Poli offre il Virtual Desktop (Citrix) e presta portatili durante le esercitazioni di CAD.
- **Risparmiare**: sconti studenti sui siti di Dell, HP, Lenovo e Apple; Black Friday; usato recente (il mercatino PoliNetwork è @mercatinopolimi).
- **Quando chiedi in chat**, specifica: corso e anno, budget, per quanti anni vuoi tenerlo, altri usi (gaming, editing), e manda i link dei modelli.

## Se vuoi usare Linux

- **Marche**: in chat i più consigliati per Linux sono ThinkPad e Dell (Latitude/XPS); c'è la lista dei portatili certificati Ubuntu (ubuntu.com/certified).
- **NVIDIA**: con Secure Boot attivo i driver proprietari danno problemi; preferisci una distro che li gestisca o firma i moduli.
- **Dual boot**: salva la chiave di ripristino BitLocker prima di ridimensionare la partizione Windows, e prendi almeno 1 TB di SSD (o due slot M.2).
- **Prima volta su Linux**: in chat si consigliano Ubuntu LTS o Mint, partendo con dual boot o VM invece di passare tutto in un colpo.
- **Esami al PC**: Safe Exam Browser non gira su Linux. Tieni Windows in dual boot o avvisa il docente con largo anticipo.

## Autori

<table>
<tr>
<td align="center"><a href="https://github.com/leox1024"><img src="https://github.com/leox1024.png?size=100" width="100" alt="Leox1024"><br><sub><b>Leox1024</b></sub></a></td>
</tr>
</table>
