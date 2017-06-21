# Tracking
Questo è il sito da cui potete scaricare il software presentato sulla rivista ElettronicaIn riguardo ad una applicazione che usa Arduino come regolatore PID che comanda un pan-tilt su cui montare una webcam collegata al PC.
Il progetto è quindi composto da uno sketch per Arduino ed un software Java che utilizza OpenCV per identificare la posizione di un qualsiasi volto umano.
In particolare l'archivio zip contiene:
* lo scketch TrackPID da caricare su Arduino
* il file di lancio su windows Tracking.bat
* l'applicazione completa ed eseguibile Tracking.jar
* le due librerie native (per win64) da porre nella directory di lancio: libcv64\opencv_java320.dll e libser64/rxtxSerial.dll
* il file di configurazione Tracking.properties da porre anch'esso nella directory di lancio
* il file per i pattern di riconoscimento del volto umano haarcascade_frontalface_alt.xml (da porre nella directory di lancio)

Infine per documentazione:
* i sorgenti delle due classi Java che compongono la parte su PC che identifica la posizione del volto
* un piccolo ReadMe.txt per illustrare l'utilizzo

Nel sito trovate anche, per comodità, un archivio di modelli di riconiscimento di oggetti tratto da OpenCV:
haarcascades.zip

Contenuto del file ReadMe.txt:

Estrarre:
- Tracking.bat
- Tracking.jar
- Tracking.properties
- haarcascade_frontalface_alt.xml
- libcv64
- libser64
nella directory creata per l'applicazione.

Estrarre TrackPID e caricarlo su Arduino

Eventualmente modificare Tracking.properties in particolare nella voce 
   Port=...  (togliere il commento)
in base alla porta su cui è collegato Arduino.

A questo punto potete lanciare Tracking.bat

Volendo potete cambiare l'oggetto da tracciare scaricando un nuovo modello xml
da questo sito : file haarcascades.zip

Potete cambiare modello tramite Tracking.properties o direttamente come 
parametro di lancio.

Per avere l'help fare: Tracking.bat ?  

Per maggiori informazione sui parametri guardare lo sketch TracPID o il file 
sorgente Java: TrackArduPID.java

NB. La libreria seriale SerialLib.jar è stata completata con una classe per
una gestione semplificata della seriale simile alla gestione su Arduino. In ogni
caso contiene la documentazione e il sorgente.
