# Kluss i systemet

Noen har prøvd a rote til regnskapet til tussene.  
Heldigvis har systemet et innebygget sjekk nummer for å se om hvert tall er gyldig.


Hvordan sjekke om tallet er ekte:

Fra høyre i tallet ta ett ig ett suffer (eksludert første som er sjekk tallet) og gang sifferet med 2 annenhver gang.  
Hvis et av tallene blir høyere en 10 så pluss sammen tier plassen og ener plassen.  
Summere disse tallene.
Resulterende tall skal så modulus 10 for å finne rest  
Sjekk siffer skal være 10 - tallet som er funnet
 
Eksempel nummer:   
746776  
560631  
523704  
581801  
677880  

Gjennomgang av 746776
| | 7 | 4 | 6 | 7 | 7 | 6 |
|--- | :---: | :---:  | :---:   | :---:   | :---:   | :---:   |
| multiplikator  | 2 | 1 | 2 | 1 | 2 | - |
| resultat  | 14 | 4 | 12 | 7 | 14 | - |
| reduser tall over 10 | 1 + 4 | 4 | 1 + 2 | 7 | 1 + 4 | - |
| produkt  | 5 | 4 | 3 | 7 | 5 | - |

sum av produkter: 5+4+3+7+5 = 24  
rest etter modulus: 24 % 10 = 4  
trekk resultat fra 10: 10 - 4 = 6  

funnet sjekk nummer er 6

Nummeret passer med oppgitt nummer så dette taller er gyldig

ved å følge denne formelen kommer vi frem til at 

560631 - gyldig

523704 - gyldig

581801 - gyldig

677880 - ugylding


summen av de gyldige tallene (inkludert sjekk nummer) er
**2412912**

"Ekte" data ligger i [Dataset](./output.txt) 

<details>
<summary>Fasit</summary>
364007655532726
</details>
