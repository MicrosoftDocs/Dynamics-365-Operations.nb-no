--- 
title: Opprette og redigere salgstilbud
description: "Denne fremgangsmåten beskriver hvordan du oppretter og oppdaterer et salgstilbud."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 7ffa4fe8d87db5b3f8293ec9dbc042496d09d6e3
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---
# <a name="create-and-edit-sales-quotations"></a>Opprette og redigere salgstilbud

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du oppretter og oppdaterer et salgstilbud. Du kan kjøre denne fremgangsmåten med dine egne data eller i demonstrasjonsdataselskapet USMF.


## <a name="create-a-sales-quotation"></a>Opprett et salgstilbud
1. Gå til Salg og markedsføring > Salgstilbud > Alle tilbud.
2. Klikk Ny.
3. Velg Kundeemne i feltet Kontotype.
4. Angi eller velg en verdi i feltet Kundeemne.
5. Utvid seksjonen Generelt.
    * Fordi du valgte å opprette et tilbud fra området Salg og markedsføring settes typen automatisk til Salgstilbud. Hvis du vil opprette et tilbud for et prosjekt, må du åpne det fra prosjektstyrings- og regnskapsmodulen.   
6. Klikk OK.
    * Feltene og handlinger i tilbudslinjene er veldig lik de i salgsordrelinjene.   Som salgsordrer kan du kan opprette tilbud for en bestemt vare, eller når varenummeret er ukjent eller ikke finnes på tidspunktet for oppretting av tilbud, kan tilbud opprettes for en salgskategori.  
7. Angi eller velg en verdi i feltet Vare.
8. Skriv inn en verdi i feltet Vare.
9. Lukk siden.
10. Angi et tall i feltet Antall.
    * Hvis det finnes gyldige forretningsavtaler for varen som er valgt på linjen, kopieres den aktuelle prisen og rabattene automatisk til tilbudslinjen. Kontroller at Enhetspris-feltet inneholder en verdi, og du kan også angi rabattverdier hvis du vil.  
11. Klikk Lagre.
12. Klikk Salgstilbud i handlingsruten.
13. Klikk Totaler.
14. Klikk OK.
15. Klikk Salgstilbudslinje.
16. Klikk Priser.
    * På siden Kjør prissimulering kan du eksperimentere med å justere forventet omsetning eller lønnsomhet for tilbudet basert på ønsket enhetspris, rabattbeløp, rabattprosent, totalbeløp, margin eller dekningsgrad.   Når du er fornøyd med måltallene, du bruker forslaget på tilbudslinjen, og de prisrelaterte feltene oppdateres tilsvarende.  
    * Du kan opprette så mange prissimuleringer som du ønsker. Når du klikker Ny, kopieres prisbetingelsene fra gjeldende tilbudslinje til siden. Du kan deretter endre verdiene i de prisrelaterte feltene til målene. En endring i ett av feltene vil utløse omberegning i alle de andre feltene. For at systemet skal beregne salgsmargin og dekningsgrad, må produktets enhetskostnad være kjent. Bruk kategorien Simulerte priser for en detaljert visning av de opprinnelige prisene, foreslåtte endringer og deres virkning på tilbudstotalene.   Som regel når en simulering som angir et nytt beløp brukes for tilbudslinjen, beregner systemet på nytt og angir en ny verdi i feltet Enhetspris. Hvis simuleringen er basert på en ny margin eller et nytt dekningsbidrag, oppdateres bare feltet Nettobeløp og enhetsprisen er tom. I begge tilfeller slettes eventuelle rabatter som var på tilbudslinjen før simuleringen.  
17. Lukk siden.
18. Klikk Tilbud i handlingsruten.
19. Velg Send tilbud.
20. Velg Ja i feltet Skriv ut tilbud.
21. Klikk OK.
    * Rapporten kan ta litt tid å generere. Ikke lukk siden før dette gjøres.  
22. Lukk siden.

## <a name="update-a-sales-quotation"></a>Oppdater et salgstilbud
1. Klikk Følg opp i handlingsruten.
2. Klikk Konverter til kunde.
3. Angi en verdi i Kundekonto-feltet.
4. Klikk Kontroller.
    * Kontroller at det vises en melding om at kontonummeret som du skrev inn, er ledig for bruk.  
5. Klikk OK.
    * Systemet har nå opprettet en ny kundekonto for kundeemnet på tilbudet.  
6. Lukk siden.
7. Klikk Følg opp i handlingsruten.
8. Klikk Bekreft.
9. Angi eller velg en verdi i feltet Årsak.
10. Klikk OK.
11. Klikk Generelt i handlingsruten.
12. Klikk Salgsordrer.
13. Lukk siden.


