# proskjekt

## Av Arman

*idag så skal jeg skrive oppgave*

*min oppgave skal handle om og lage ett nettverk mellom rasberry pi og en pc med windows opperativt system. jeg skal bruke en ruter og switch til og lage WAN og hoste nettsider fra begge pc-er og hoste de på den andre.*

## Ting jeg trenger 

- rasberry Pi
- thinkpad
- Router 
- switch 
- 2 x ethernett kabel
- 1 x HDMI kabell

## Hva jeg skal prøve og få fram.

*jeg skal vise til lærerene at jeg kan sette opp nettverk, hoste nettside, og gjøre det immelomm to forksjelige pc-er med to forkjelige opperativt systemer.*


*det som er viktigst er og lage en python fil som jeg kan hoste på rasberry pi-en* 

# Mål for prosjektet #

Jeg vil demonstrere følgende ferdigheter:

Sette opp et fungerende LAN (Local Area Network) ved hjelp av router og switch.

Konfigurere nettverksinnstillinger på både Windows-PC og Raspberry Pi.

Hoste en enkel nettside:

En nettside hostet fra Raspberry Pi

En nettside hostet fra Windows-PC

Krysstilgang – nettsiden fra Pi skal kunne åpnes på Windows-PC og motsatt.

Lage en enkel Python-fil som fungerer som en webserver på Raspberry Pi-en.

# hvordan proskjektet går # 

Til nå går det ganske fint, 


# Debugging #

Gått gjennom mye problemer, men har klart og komme meg forbi disse feilene.

- sliter med å åpne server på rasberry pi
- bruk av feil ip adresser. (statisk og dynamisk)
- brannmuren har ikke lagt til gang til portnummeret
- Netmasken på rasperry pi-en var satt til 255.255.255.0 som gjør at pc-en med windows operativt ikke kan hoste servern på nettlesern dems.
- 

# rette op feilene #

🔵 BLÅ (LAVT NIVÅ) – hvordan løfte disse
🔵 Programmering

Status nå:
Du lager én Python-fil som hoster en nettside (bra start).

Hvordan forbedre:

Bruk http.server i Python, men:

Legg til egne funksjoner

Kommenter koden

Bruk if __name__ == "__main__":

Eksempel (bedre enn minimum):

from http.server import HTTPServer, SimpleHTTPRequestHandler

def start_server(port=8000):
    server = HTTPServer(("", port), SimpleHTTPRequestHandler)
    print(f"Server kjører på port {port}")
    server.serve_forever()

if __name__ == "__main__":
    start_server()


👉 Hvorfor dette er bedre:

Viser forståelse for Python-struktur

Ikke bare kopiert kode

Enkelt å forklare muntlig

🔵 Debugging

Status nå:
Lite eller ingen feilsøking dokumentert.

Hvordan forbedre:

Vis at du har møtt feil og løst dem

Eksempler på ting du kan teste og skrive om:

ping mellom PC og Pi

Feil IP-adresse

Brannmur blokkerer port 8000

Eksempel du kan skrive i oppgaven:

"Da jeg prøvde å åpne nettsiden fra Windows-PC-en fikk jeg ingen respons. Jeg brukte ping for å sjekke tilkoblingen og oppdaget at Raspberry Pi-en hadde en annen IP-adresse enn forventet."

👉 Dette viser problemløsing og debugging, ikke bare at “det funket”.

🟢 GRØNN (MIDDELS) – hvordan løfte disse til HØY
🟢 Dokumentasjon

Status nå:
Kort README / lite forklaring (GitHub-teksten du viste).

Hvordan forbedre:
Lag en ordentlig README med disse delene:

Mål

Utstyr

Nettverksoppsett (tekst + evt. bilde)

IP-adresser

Hvordan starte webserver

Feil og løsninger

Eksempel:

## Hvordan starte webserver på Raspberry Pi
1. Start Raspberry Pi
2. Åpne terminal
3. Kjør:
   python3 server.py
4. Åpne nettleser på Windows-PC:
   http://192.168.1.10:X


👉 Dette alene kan løfte karakteren merkbart.

🟢 Sikkerhet

Status nå:
Sikkerhet nevnes lite eller ikke konkret.

Hvordan forbedre (enkelt, men smart):

Forklar at:

Nettverket er lokalt (LAN)

Ingen port forwarding til internett

Endre standardpassord på Raspberry Pi (si at du har gjort det)

Forklar brannmur kort

Eksempeltekst:

"For sikkerhet ble nettsiden kun tilgjengelig på det lokale nettverket. Raspberry Pi-en ble ikke eksponert mot internett, og standardpassord ble endret."

🟢 Infrastruktur (nettverk)

Status nå:
Du bruker router + switch, men forklarer lite.

Hvordan forbedre:

Forklar forskjellen på:

Router (DHCP, WAN/LAN)

Switch (kobler enheter)

Vis hvordan kablene er koblet

Eksempel:

"Routeren delte ut IP-adresser via DHCP. Switchen ble brukt for å koble Raspberry Pi og Windows-PC til samme lokale nettverk."

