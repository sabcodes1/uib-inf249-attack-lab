# INF249 – Attack Lab (MA2, “ma3”)

Dette prosjektet er fra **INF249 – Nettverkssikkerhet (UiB)** og er en praktisk 
penetrasjonstest-lab i et lukket virtuelt miljø.

## Scenario
Målet var å finne en skjult flagg (`FLAG{...}`) på en målmaskin i samme nettverk som en 
inngangsmaskin (“entrypoint”). Arbeidet fulgte en realistisk angrepskjede:

## Hva jeg gjorde
- **Nettverksrekognosering**
  - Fant IP-adressen til målmaskinen.
  - Skannet tjenester med nmap for å kartlegge åpne porter og tjenester.

- **Initial tilgang**
  - Identifiserte en feilkonfigurert tjeneste som ga fotfeste på systemet.
  - Oppnådde første shell på målmaskinen.

- **Post-exploitation**
  - Enumererte brukerkontoer på systemet.
  - Hentet ut passord-hasher fra maskinen.
  - Knekket svake passord med passende verktøy.

- **Privilege escalation**
  - Fikk tilgang til konto med sudo-rettigheter.
  - Navigerte til riktig hjemmekatalog og hentet flagget.

## Verktøy
- Linux CLI
- nmap  
- SSH  
- Passordknekking (f.eks. John the Ripper / hashcat)  
- Standard enumeration-teknikker

## Dokumentasjon
Full rapport: `report/INF249_MA2_attack_lab.pdf`
