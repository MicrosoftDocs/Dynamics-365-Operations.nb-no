--- 
title: Opprette en ny forretningsavtale
description: "Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a>Opprette en ny forretningsavtale

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du vil bruke dine egne data, må du før du starter denne veiledningen passe på at et navn på journal for forretningsavtale finnes der standardrelasjonen er satt til Pris (salg).


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Opprette og postere en ny forretningsavtalejournal
1. Gå til Salg og markedsføring > Priser og rabatter > Forretningsavtalejournaler.
2. Klikk Ny.
3. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk Linjer.
7. Velg Tabell i feltet Kontokode.
    * I dette eksemplet oppdaterer du prisen for en bestemt kunde, som betyr at du må velge Tabell. Hvis du oppdaterer produktets listepris, velger du Alle, slik at den nye prisen gjelder for alle kunder. Hvis du skal skille priser mellom ulike kundesegmenter, velger du deretter Gruppe. For å merke Gruppe må du ha definert kundeprisgrupper.  
8. Klikk rullegardinknappen i feltet Kontovalg for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Velg Tabell i Varekode-feltet.
    * Når du registrerer en forretningsavtale av typen Pris (salg), må du bare velge Tabell i Varekode-feltet. Dette skyldes at en pris er en absolutt verdi og kan ikke være lik for alle produkter eller en gruppe produkter.  
11. Klikk rullegardinknappen i feltet Varerelasjon for å åpne oppslaget.
12. I listen velger du produktet du vil ha med i avtalen.
    * Noter hvilket produkt du har valgt.  
13. Klikk koblingen i den valgte raden i listen.
14. Velg et minimumsantall i Fra-feltet.
    * Hvis kunden må bestille et minimumsantall av varen før de kan få tilgang til den nye prisen, må du angi antallet her.  
    * Angi en verdi i feltet Til for å angi maksimalt antall som prisen for den avtalen ikke vil være gyldig over. Hvis du tilbyr priser og rabatter som er basert på flere avbruddspunkt for antall, angir du hver antallsintervall som et par av minste og største antall i henholdsvis Fra- og Til-feltene.  
15. Angi en pris i feltet Beløp i valuta.
16. I Fra dato-feltet angir du en dato som denne avtalen skal være gyldig fra.
17. Klikk Lagre.
18. Klikk Valider.
19. Klikk Valider valgte linjer.
20. Klikk OK.
21. Klikk Poster.
22. Klikk OK.

## <a name="view-trade-agreements-for-a-product"></a>Vise forretningsavtaler for et produkt
1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. I listen finner og velger du produktet som du akkurat har oppdatert prisen for.
3. Klikk Selg i handlingsruten.
4. Klikk Vis forretningsavtaler.
    * Se gjennom detaljene i forretningsavtalen for priser som du nettopp opprettet.    
5. Lukk siden.


