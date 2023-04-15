![aisf_python_logo](images/logo_corso.png)

# Introduzione

Questa repository serve come base al corso _"Python: Un Approccio Da Fisico"_ ma anche per qualsiasi curioso che vuole inziare a usare Python per il calcolo scientifico.

Per visualizzare i notebook potete o visualizzarli direttamente su GitHub andando a cliccare su [**intro_python_1**](intro_python_1.ipynb) e su [**intro_python_2**](intro_python_2.ipynb) oppure scaricarli in locale `guardando nelle release` (qua andare ad inserire link).

# Per Iniziare

Per prima cosa dobbiamo installare Python! Per farlo useremo **Miniconda** che ci installerà `conda`, un gestore di ambienti di Python (per sapere cosa è un ambiente [guarda sotto](#python-ed-ambienti)).

Perciò scaricate l'[ultima versione di Miniconda per il vostro OS](https://docs.conda.io/en/latest/miniconda.html), seguite le istruzioni e lasciate tutte le impostazioni come da default. Per maggiori informazioni sull'installazione [consultate qui](https://conda.io/projects/conda/en/stable/user-guide/install/index.html).

Ora possiamo usare l'**Anaconda Prompt** per gestire i nostri pacchetti e gli ambienti.

## Python ed Ambienti

Per iniziare




## Consigli per Windows

Se avete Windows vi do qualche consiglio. Installate l'ultima versione di [Powershell](https://www.microsoft.com/store/productId/9MZ1SNWT0N5D) e poi installate anche [Windows Terminal](https://www.microsoft.com/store/productId/9N0DX20HK701).

**Windows Terminal** è un emulatore di terminale moderno e modificabile ampiamente, inoltre gira molto bene su Windows 11. Fate un profilo con il nuovo Powershell di default, se volete cambiate pure la cartella di base.

Per **settare conda** su questo terminale potete o aggiungere manualmente l'executable di conda alle _variabili d'ambiente_ oppure (quello che vi consiglio) aprire l'_Anaconda Prompt_ e scrivere `conda init powershell`. Lui si preoccuperà di inizializzare powershell per voi, ora potete usare **Powershell** da dentro Windows Terminal come se fosse l'_Anaconda Prompt_.

Inoltre, potreste volere far girare degli script all'avvio di Powershell. Per far ciò basta eseguire il comando `notepad $PROFILE` e accettare (solo la prima volta). Questo creerà un file **PROFILE** dove ogni riga verrà passata a _Powershell_ all'avvio. Una cosa che metto io spesso è `conda activate ambiente_che_uso_per_ora` per evitare di dover attivare l'ambiente di conda ogni volta.

**P.S.** se volete avere una linea di comando _spaziale_ allora date uno sguardo a [Oh My Posh](https://ohmyposh.dev/). E se volete usate pure il [mio tema custom](https://github.com/alex180500/simple-monokai).

## Licenza

Tutto il materiale è stato creato da **Alessandro Romancino** per il suddetto corso tenuto dal comitato locale _AISF Palermo_. Il materiale del corso è distribuito con _licenza MIT_, perciò siete liberi di **fare quello che volete** con il materiale.

Se volete, potete citarmi linkando il mio profilo [`https://github.com/alex180500`](https://github.com/alex180500). **Grazie!**