--- 
title: "Opprette en innkjøpsgjentakelsesordre"
description: "Denne fremgangsmåten viser hvordan du oppretter en gjentatt bestilling ved å kopiere linjer fra et tidligere bestillingsdokument til en ny eller eksisterende bestilling."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 257582d889ff55753f9bdbd234f0540503d20f27
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-repeat-purchase-order"></a>Opprette en innkjøpsgjentakelsesordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en gjentatt bestilling ved å kopiere linjer fra et tidligere bestillingsdokument til en ny eller eksisterende bestilling. Det finnes to metoder for å opprette gjentatte ordrer. Du kan bruke handlingene som er tilgjengelige på dokumentnivå i handlingsruten, eller du kan bruke linjedetaljhandlingene. handlinger på dokumentetnivå er hovedsaklig beregnet på å opprette en ny bestilling ved å legge til linjer og hodeinformasjon fra en annen ordre, mens linjedetaljerhandlingen er hovedsaklig for å legge til linjer i en eksisterende ordre. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Denne oppgaven utføres vanligvis av en innkjøpsagent.


## <a name="create-a-new-repeat-purchase-order"></a>Opprette en gjentatt innkjøpsreturordre
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
    * Først prøver vi alternativet for å kopiere informasjon til en ny ordre.  
2. Klikk Ny.
3. Angi US-101 i Leverandørkonto-feltet.
4. Klikk OK.
5. Klikk Bestilling i handlingsruten.
6. Klikk Fra alle.
    * Dette er siden der du kan kopiere fra eksisterende ordre til ordren din. Det finnes ulike alternativer for hvordan linjene kopieres og ulike typer dokumenter som du kan kopiere fra. Vi skal først se på alternativene for hvordan linjene kopieres.   
7. Utvid seksjonen Parametere.
    * Antallsfaktor-feltet er nyttig hvis du vil bruke et antall som er forskjellig fra det som er i ordren du kopierer fra. Hvis du for eksempel vil bestille to ganger antallet som er i linjene du kopierer fra, skriver du inn 2 i dette feltet, og systemet vil deretter legge til linjer der det opprinnelige antallet er doblet.  
    * Snu fortegn-feltet støtter også endring av det bestilte antallet ved å endre fortegnet for antallet for ordrelinjer som er lagt til. Dette kan være nyttig hvis du vil tilbakeføre en transaksjon, ved å opprette bestillingslinjer negerer transaksjonen. Dette alternativet velges automatisk når siden åpnes fra handlingen Opprett kreditnota.  
    * Alternativet Kopier gebyrer lar deg kopiere gebyrer til den nye ordren fra dokumentet du kopierer ordrelinjene fra.  
    * Alternativet Beregn priser bruker gjeldende priser og rabatter i stedet for å kopiere disse fra dokumentet du kopierer annen informasjon fra.  
    * Alternativet Kopier presist oppretter en nøyaktig kopi av verdiene i alle feltene i ordrehodet og linjene i dokumentet. Hvis det ikke er merket av for dette alternativet, brukes standardverdiene for mange av feltene som er relatert til leverandører og produkter, som om du oppretter den nye ordren manuelt. Hvis ordren du kopierer fra for eksempel har overstyrt standard fakturakonto for leverandøren, vil den samme fakturakontoen kopieres til bestillingen. Hvis du ikke velger alternativet Kopier presist, brukes i stedet standard fakturakonto for leverandøren på bestillingen.  
    * Alternativet Slett innkjøpslinjer sletter alle bestillingslinjene som allerede finnes på bestillingen som du kopierer til, før du bruker de nye linjene. Vær forsiktig når du bruker dette alternativet, siden dette sletter alle eksisterende linjer uten advarsel.  
    * Hvis du bruker alternativet Kopier ordrehode, trenger du ikke opprette hodeinformasjon manuelt på den nye bestillingen. Legg merke til at dette alternativet vil føre til at standardverdier brukes for feltene som er knyttet til leverandøren. Bruk alternativet Kopier presist hvis dokumentet du kopierer fra har ikke-standardverdier du vil kopiere.  
8. Skjul Parametere-delen.
    * Du kan kopiere fra forskjellige dokumentkilder, og hver har en egen del på denne siden. Delen Bestillinger lar deg for eksempel kopiere fra eksisterende bestillinger.  
9. Klikk linjen for bestillingen som har ID-en 00015. 
10. Velg linjen ved å klikke i avmerkingsboksen.
11. Fjern merket i avmerkingsboksen for linjen, slik at den ikke kopieres til bestillingen.
    * Nå er fire linjer valgt som skal kopieres til bestillingen. Det er mulig å velge flere bestillingslinjer fra andre bestillinger og kopiere dem også til bestillingen. Det er også mulig å legge til linjer fra andre typer innkjøpsdokumenter. De neste trinnene går gjennom de ulike alternativene.  
12. Skjul Bestillinger-delen.
13. Vis Bekreftelse-delen.
    * Her kan du velge bestillingsbekreftelser å kopiere fra. Bestillingsbekreftelser identifiseres med tilhørende innkjøpsjournal-ID eller bestillings-ID.  
14. Skjul Bekreftelse-delen.
15. Vis Produktkvitteringer-delen.
    * Her kan du velge produktkvitteringsjournaler å kopiere fra. Produktkvitteringsjournalene identifiseres med produktkvitteringsbilaget eller bestillings-ID-en.   
16. Skjul Produktkvitteringer-delen.
17. Vis Fakturaer-delen.
    * Her kan du velge leverandørfakturaer å kopiere fra. Fakturaene identifiseres av fakturabilaget eller bestillings-ID-en.   
18. Skjul Fakturaer-delen.
19. Vis delen Valgte linjer eller topptekst som skal kopieres.
    * Denne visningen viser et sammendrag av alle dokumenter og linjer som du har valgt å kopiere til bestillingen.   
20. Skjul delen Valgte linjer eller topptekst som skal kopieres.
21. Klikk OK.
    * De fire linjene du valgte, er nå kopiert til den nye bestillingen.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopiere linjer til en eksisterende bestilling
    * I stedet for å kopiere en hel ordre, er det mer vanlig å opprette en ny bestilling og fullstendig informasjon i bestillingshodet, og deretter kopiere enkeltlinjer fra eksisterende ordrer.  
1. Klikk Bestillingslinje.
2. Klikk Fra alle.
    * Siden som åpnes, er identisk med den som ble vist før, men forskjellige alternativer er valgt når den åpnes fra ordrelinjevisningen. La oss gå gjennom parameterne.   
3. Utvid seksjonen Parametere.
    * Alternativet Slett innkjøpslinjer er ikke valgt. Dette betyr at du kan kopiere nye linjer til ordren uten å fjerne eksisterende linjer.   
    * Alternativet Kopier ordrehode er heller ikke valgt, siden vi bare legger til flere linjer til ordren.   
4. Skjul Parametere-delen.
    * I dette eksemplet skal vi kopiere linjer fra en eksisterende bestilling.   
5. Klikk linjen for bestillingen som har ID-en 00034. 
6. Velg linjen ved å klikke i avmerkingsboksen.
    * Legg merke til at linjen med enkeltordren i denne bestillingen også er valgt.  
7. Klikk OK.
    * Den ekstra ordrelinjen er lagt til bestillingen.  


