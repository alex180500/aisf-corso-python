![logo](images/logo_corso.png)

# Introduzione

Questa repository serve come base al corso _"Python: Un Approccio Da Fisico"_ ma anche per qualsiasi curioso che vuole inziare a usare Python per il calcolo scientifico.

Per visualizzare i notebook potete o visualizzarli direttamente su GitHub andando a cliccare su [**intro_python_1**](intro_python_1.ipynb) e su [**intro_python_2**](intro_python_2.ipynb) oppure scaricarli per farli girare in locale `guardando nelle release (qua andare ad inserire link)`.

## Struttura del Corso

Il corso è diviso in due notebook corrispondenti alle due giornate del 21/04/23 e del 22/04/23. Gli argomenti trattati sono:

- **Giornata 1:** introduzione, sintassi di base, pacchetti e programmazione ad oggetti, vettori e rng su numpy.

- **Giornata 2:** grafici e stili con matplotlib, funzioni avanzate di numpy, funzioni utili di scipy, fit ai minimi quadrati, esempi di analisi di laboratorio e di simulazioni numeriche.

# Per Iniziare

Per prima cosa dobbiamo installare Python! Per farlo useremo **Miniconda** che ci installerà `conda`, un gestore di ambienti di Python (per sapere cosa è un ambiente [guarda sotto](#python-ed-ambienti)).

Perciò scaricate l'[ultima versione di Miniconda per il vostro OS](https://docs.conda.io/en/latest/miniconda.html), seguite le istruzioni e lasciate tutte le impostazioni come da default. Per maggiori informazioni sull'installazione [consultate qui](https://conda.io/projects/conda/en/stable/user-guide/install/index.html).

Ora possiamo usare l'**Anaconda Prompt** per gestire i nostri pacchetti e gli ambienti.

## Conda e Ambienti

Come primissima cosa settiamo come canale di default (da cui verranno scaricati tutti i pacchetti) **Conda Forge**. Forge è un canale community-driven che tiene i cosiddetti _feedstock_, [per più informazioni, consultate il loro sito.](https://conda-forge.org/) 

Eseguiamo quindi questi due comandi (basta farli una volta all'istallazione e fine)
```
conda config --add channels conda-forge
conda config --set channel_priority strict
```
Perfetto, ora possiamo iniziare! Per prima cosa aggiorniamo conda e l'ambiente **base** eseguendo `conda update conda` e poi `conda update --all` (quando eseguiamo _conda update_ verrà chiesto se proseguire e possiamo premere invio per continuare).

Ora creiamo il nostro nuovo ambiente dove andare a lavorare e installare tutti i pacchetti. Diamo un nome al nostro ambiente e quindi creiamolo tramite il comando
```
conda create -n nome_ambiente python=3.11
```
Questo creerà un ambiente con il nome dato e l'ultima versione di **Python 3.11** (al 16/04/23 è _Python 3.11.3_).

Dopo che avrà finito attiviamolo con `conda activate nome_ambiente` (se dovessimo tornare nell'ambiente base basta fare `conda deactivate`). Ora possiamo installare tutti i pacchetti che ci serviranno per questo corso. Quindi possiamo eseguire
```
conda install numpy matplotlib scipy notebook
```
Che installerà le ultime versione dei pacchetti [NumPy](https://numpy.org/doc/stable/index.html), [Matplotlib](https://matplotlib.org/stable/index.html), [SciPy](https://docs.scipy.org/doc/scipy/index.html) e [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/latest/?badge=latest).

## Il Jupyter Notebook

Ora che abbiamo installato _Jupyter Notebook_ possiamo iniziare a usare Python. Per iniziare navighiamo nella cartella dove abbiamo scaricato il materiale con `cd percorso_cartella`.

Una volta entrati eseguiamo `jupyter notebook`, questo aprirà l'interfaccia del notebook nel browser e clicchiamo sul notebook che ci interessa.

Possiamo ora creare dei **blocchi** (premendo il +) che possono essre _codice_ o _markdown_. I blocchi **Markdown** sono dei blocchi di testo, [per la sintassi di base leggi qui.](https://www.markdownguide.org/basic-syntax/).

Concentriamoci sui blocchi di codice ora. Per eseguire un blocco possiamo cliccare sulla freccia **Run** oppure usare **Shift + Enter**.

Il codice viene eseguito in sequenza (blocco dopo blocco) e potete eseguire i blocchi nell'ordine che preferite. Nel caso aveste dei problemi potete riavviare l'esecuzione andando su _Kernel -> Restart_.

Per altre informazioni consultate la [guida ufficiale di Jupyter Notebook.](https://jupyter-notebook.readthedocs.io/en/latest/notebook.html)

# Informazioni Utili Varie

## Informazioni Utili su Conda

Per installare un pacchetto su conda basta usare `conda install nome_pacchetto`, quando volete aggiornare il vostro ambiente, prima attivatelo (se non lo è già) e poi eseguite `conda update --all` che aggiornerà tutti i pacchetti.

Nella rara eventualità che il pacchetto che vi serve non sia presente su _conda-forge_ potete usare **pip**, il gestore di pacchetti di base di Python basato sul **Python Package Index** o **PyPi**. Per installare un pacchetto con _pip_ basta eseguire `pip install nome_pacchetto`, _però..._

Vi consiglio caldamente di creare un nuovo ambiente quando dovete farlo, installare prima tutti i pacchetti da conda-forge e poi quelli rimanenti da pip solo alla fine. Vi consiglio di leggere bene [l'articolo nella wiki ufficiale su questo argomento.](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#pip-in-env)

Se avete bisogno di ricordarvi i comandi [qui trovate la **cheat sheet di Conda**.](https://docs.conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf)

In generale per qualsiasi dubbio su Conda [visualizzate la sua ottima documentazione.](https://docs.conda.io/projects/conda/en/latest/user-guide/index.html)

## Consigli per Windows

Se avete Windows vi do qualche consiglio. Installate l'ultima versione di [Powershell](https://www.microsoft.com/store/productId/9MZ1SNWT0N5D) e poi installate anche [Windows Terminal](https://www.microsoft.com/store/productId/9N0DX20HK701).

**Windows Terminal** è un emulatore di terminale moderno e modificabile ampiamente, inoltre gira molto bene su Windows 11. Fate un profilo con il nuovo Powershell di default, se volete cambiate pure la cartella di base.

Per **settare conda** su questo terminale potete o aggiungere manualmente l'executable di conda alle _variabili d'ambiente_ oppure (quello che vi consiglio) aprire l'_Anaconda Prompt_ e scrivere `conda init powershell`. Lui si preoccuperà di inizializzare powershell per voi, ora potete usare **Powershell** da dentro Windows Terminal come se fosse l'_Anaconda Prompt_.

Inoltre, potreste volere far girare degli script all'avvio di Powershell. Per far ciò basta eseguire il comando `notepad $PROFILE` e accettare (solo la prima volta). Questo creerà un file **PROFILE** dove ogni riga verrà passata a _Powershell_ all'avvio. Una cosa che metto io spesso è `conda activate ambiente_che_uso_per_ora` per evitare di dover attivare l'ambiente di conda ogni volta.

**P.S.** se volete avere una linea di comando _spaziale_ allora date uno sguardo a [Oh My Posh](https://ohmyposh.dev/). E se volete usate pure il [mio tema custom](https://github.com/alex180500/simple-monokai).

## Lista di Pacchetti Utili

- [**tqdm:**](https://tqdm.github.io/) libreria per creare delle barre di caricamento durante i loop
- [**uncertainties:**](https://pythonhosted.org/uncertainties/) libreria fantastica per effettuare operazioni tra numeri con errori associati (funziona anche con array di numeri)
- [**pandas:**](https://pandas.pydata.org/docs/) libreria per data analysis
- [**streamlit:**](https://docs.streamlit.io/) una libreria che permette di creare interfacce grafiche semplicemente e caricare le app sul cloud
- [**black:**](https://black.readthedocs.io/en/stable/) un formattatore di codice che segue lo [stile PEP 8](https://peps.python.org/pep-0008/)
- [**lmfit:**](https://lmfit.github.io/lmfit-py/intro.html) pacchetto per effettuare fit più complessi
- [**plotly**](https://plotly.com/python/), [**seaborn**](https://seaborn.pydata.org/) e [**bokeh:**](https://docs.bokeh.org/en/latest/) altre librerie per la visualizzazione
- [**sympy:**](https://docs.sympy.org/latest/index.html) libreria per calcolo letterale (tipo Mathematica)
- [**python-igraph**](https://python.igraph.org/en/stable/) e [**networkx:**](https://networkx.org/documentation/stable/index.html) librerie per studiare reti complesse
- [**tenpy:**](https://tenpy.readthedocs.io/en/latest/index.html) libreria per tensor network

# Licenza

Tutto il materiale è stato creato da **Alessandro Romancino** per il suddetto corso tenuto dal comitato locale _AISF Palermo_. Il materiale del corso è distribuito con _licenza MIT_, perciò siete liberi di **fare quello che volete** con il materiale.

Se volete, potete citarmi linkando il mio profilo [`https://github.com/alex180500`](https://github.com/alex180500). **Grazie!**