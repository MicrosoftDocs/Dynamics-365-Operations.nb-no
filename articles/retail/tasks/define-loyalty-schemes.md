---
title: " Definere fordelsskjemaer"
description: Denne prosedyren hjelper med å definere en fordelsplan.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 362d6cf877c484c438641980d109b3bed4464b68
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564676"
---
# <a name="define-loyalty-schemes"></a> Definere fordelsskjemaer

[!include [task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren hjelper med å definere en fordelsplan. Fordelsplaner er fordelsopptjenings- og innløsingsregler for et fordelsprogram. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. Gå til Detaljhandel og handel > Kunder > Fordel > Fordelsplaner.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Plan-ID.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
    * Du kan ha flere fordelsplaner for et fordelsprogram. Fordelsplaner kan være for alle kanalene eller bare et delsett av kanalene.  
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk Lagre.
9. Klikk Legg til linje.
10. Velg et alternativ i feltet Aktivitetstype.
    * Velg Kjøp av produkter basert på beløp hvis du vil at kundene skal oppnå fordeler basert på hvor mye de bruker. Velg Kjøp av produkter basert på antall hvis du vil at kundene skal oppnå fordeler basert på hvor mange produkter de kjøper.  Velg Antall salgstransaksjoner hvis du vil at kundene skal opptjene fordeler for alle salgstransaksjoner uansett hva eller hvor mye som kjøpes.  
    * Velg en kategori. Kategorien begrenser hvilke produkter opptjeningsregelen gjelder for.  
    * Hvis du vil at opptjeningsregelen skal gjelde for alle produkter, lar du feltet stå tomt.  
11. Angi et tall i feltet Beløp/antall for aktivitet.
    *  For aktivitetstypen Antall salgstransaksjoner bør du alltid bruke verdien 1,0. For aktivitetstypene Kjøp av produkter basert på beløp eller Kjøp av produkter basert på antall utløses ikke opptjeningsregelen hvis transaksjonen er lavere enn den angitte verdien. Hvis for eksempel aktivitetstypen er Kjøp av produkter basert på beløp og du angir 10,00, vil ikke salgstransaksjonen på 9,00 opptjene fordeler for denne opptjeningsregelen.  
12. Skriv inn en verdi i Aktivitetsvaluta-feltet.
13. Klikk rullegardinknappen i feltet ID for fordelspoeng for å åpne oppslaget.
14. Klikk koblingen i den valgte raden i listen.
15. Angi et tall i Fordelspoeng-feltet.
    * Fordelspoeng av typen beløp registrerer opptjente beløp i desimaler. Hvis for eksempel opptjeningsregelen tilsier at du får 1 poeng for hver krone som brukes, og kunden bruker 1,25 kroner, får kunden 1,25 fordelspoeng. Fordelspoeng av typen antall registrerer opptjente beløp i heltall. Hvis for eksempel opptjeningsregelen tilsier at du får 1 poeng for hver krone som brukes, og kunden bruker 1,25 kroner, får kunden 1,0 fordelspoeng.  
16. Klikk Lagre.
17. Klikk Legg til linje.
    * Innløsingsregler brukes når fordelsbetalingsmåten brukes.  
18. Klikk rullegardinknappen i feltet ID for fordelspoeng for å åpne oppslaget.
    * Det vises bare fordelspoeng som kan innløses.  
19. Klikk koblingen i den valgte raden i listen.
20. Angi et tall i Fordelspoeng-feltet.
21. Velg et alternativ i feltet Innløsingstype.
    * Når du velger Betaling etter beløp, behandles feltet Beløp eller antall som en valutaverdi. I dette tilfellet er beløpet for fordelspoeng som brukes per valutaenhet med betaling, et fast forholdstall. Når du velger Betaling etter antall, behandles feltet Beløp eller antall som en antallsverdi. I dette tilfellet er beløpet for fordelspoeng som brukes per vareantall, et fast forholdstall, men beløpet i valuta kan variere hvis prisen på varene som betales med fordelspoeng, varierer for samme antall. Innløsningstypen Rabatt for fordelspoeng er bare gyldig når konfigurasjonsnøkkelen for Russland under Land-/områdespesifikke funksjoner er aktivert, og ISO-koden er satt til RU under Funksjonalitetsprofiler for salgssted.  
    * Velg en kategori. Kategorien begrenser hvilke produkter innløsingsregelen gjelder for.  
    * Hvis du vil at innløsingsregelen skal gjelde for alle produkter, lar du feltet stå tomt.  
22. Angi et tall i Beløp eller antall-feltet.
23. Skriv inn en verdi i Valuta-feltet.
24. Klikk Lagre.
25. Klikk Legg til linje.
    * Velg en eller flere noder fra listen Tilgjengelige organisasjonsnoder og flytt dem til listen Valgte organisasjonsnoder ved å klikke pilen mellom de to listene.  
26. Klikk OK.
27. Klikk Lagre.
    * Hver gang du endrer kanaler for en fordelsplan, må du kjøre Behandle fordelsplaner. På denne måten får kanalene oppdaterte fordelsplaner.  

