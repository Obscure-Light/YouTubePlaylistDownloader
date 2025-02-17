# YouTube Playlist Downloader

Questo progetto consente di scaricare l'intera playlist di YouTube presente in uno o più URL, grazie alla libreria [pytube](https://pypi.org/project/pytube/).

## Requisiti
- Python 3.7 o successivo
- pip per installare le dipendenze

## Installazione

1. Clona questo repository o scarica lo ZIP.
2. Installa le dipendenze con:
   ```bash
   pip install -r requirements.txt

Utilizzo

Crea un file di testo con uno o più URL di playlist di YouTube, ognuno su una riga. Ad esempio:

https://www.youtube.com/playlist?list=PLxxxxxx
https://www.youtube.com/playlist?list=PLyyyyyy

Aggiorna main.py: imposta la variabile urls_file_path con il percorso del tuo file di testo (ad esempio: "percorsi_playlist.txt").

Esegui il programma:

python main.py

Controlla i risultati: i video verranno scaricati in una cartella avente il nome della playlist oppure nella cartella specificata come parametro di download_youtube_playlist.

Utilizzo avanzato

Destinazione personalizzata: Se vuoi salvare tutti i video di una playlist in una cartella specifica, puoi passare un secondo parametro a download_youtube_playlist(url). Esempio:

download_youtube_playlist(url, output_folder="CartellaPersonalizzata")

Se non imposti output_folder, verrà usato il titolo della playlist come nome della cartella.

Supporto file multipli: Se disponi di più file di testo con diverse liste di URL, puoi gestirli uno dopo l'altro semplicemente richiamando read_urls_from_file e download_youtube_playlist per ciascun file.

Argomenti da riga di comando: Per maggiore flessibilità, puoi utilizzare argparse in main.py per leggere i percorsi di input e la cartella di destinazione come parametri passati all'esecuzione del programma.