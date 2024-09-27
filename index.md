# Kluss i systemet

Noen har prøvd å rote til regnskapet til tussene.  
En sleip vette har lagt inn falske tall i lefsetabellen som ligger i tusseladder-databasen.  
Heldigvis har de smarte tussene forberedt seg på knep.   
Tallene i tabellen har nemlig en innebygget sjekk, et kontrollsiffer, for å se om et tall er gyldig.


Prosedyre for å sjekke om tallet er gyldig:

Start med sifferet helt til høyre i tallet.  
Dette er kontrollsifferet som foreløpig ignoreres og brukes helt til slutt.  
Arbeid deretter mot venstre, siffer for siffer.  
Man sjekker annenhvert siffer (f.o.m. tallet til venstre for kontrollsifferet) på følgende måte:  
Gang tallet med 2. Dersom resultatet er over 10 legges sifrene i dette tallet sammen, og hvis ikke beholdes resultatet.  
Tall som ikke sjekkes beholdes som de er.  
Alle disse resultatene legges sammen, og man tar så dette resultatet modulus 10.  
Man sitter så igjen med ett enkelt tall mellom 0 og 10, og dersom 10 minus dette tallet er det samme som kontrollsifferet, er det opprinnelige tallet gyldig.
 
Eksempelnummer:   
746776  
560631  
523704  
581801  
677880  

Gjennomgang av 746776
| | 7 | 4 | 6 | 7 | 7 | 6 |
|--- | :---: | :---:  | :---:   | :---:   | :---:   | :---:   |
| ganges med  | 2 | 1 | 2 | 1 | 2 | - |
| resultat  | 14 | 4 | 12 | 7 | 14 | - |
| resultat over 10 | 1 + 4 | 4 | 1 + 2 | 7 | 1 + 4 | - |
| endelig resultat  | 5 | 4 | 3 | 7 | 5 | - |

Sum av endelige resultat: 5+4+3+7+5 = 24  
Rest modulo 10: 24 % 10 = 4  
10 minus rest: 10 - 4 = 6  

Prosedyren fører til det samme som kontrollsifferet, og tallet er derfor gyldig.

Ved å følge denne formelen kommer vi frem til at 

560631 - gyldig

523704 - gyldig

581801 - gyldig

677880 - ugylding


Summen av de ovennevnte gyldige tallene (der man inkluderer sjekksifferet) er
**2412912**

## Oppgave
Kan du finne summen av lefsetabellen etter å ha fjernet de ugyldige tallene som har blitt lagt inn?  


[Utrekk av lefsetabellen fra tusseladder-databasen](./input.txt) 

<details>
<summary>Fasit</summary>
364007655532726
</details>
