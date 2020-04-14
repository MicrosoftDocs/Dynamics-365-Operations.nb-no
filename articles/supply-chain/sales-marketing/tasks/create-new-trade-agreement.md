---
title: Opprette en ny forretningsavtale
description: Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a964b357ac9abb65cd097b084630a53f1553ad04
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146554"
---
# <a name="create-a-new-trade-agreement"></a>Opprette en ny forretningsavtale

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en forretningsavtale der du registrerer en ny salgspris for produkt som du har avtalt med en bestemt kunde. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du vil bruke dine egne data, må du før du starter denne veiledningen passe på at et navn på journal for forretningsavtale finnes der standardrelasjonen er satt til Pris (salg).


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Opprette og postere en ny forretningsavtalejournal
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salg og markedsføring > Forretningsavtalejournaler**.
2. Klikk på **Ny**.
3. Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. I **Handlingsrute** klikker du på **Linjer**.
6. Velg Tabell i **Kontokode**-feltet.
    
    I dette eksemplet oppdaterer du prisen for en bestemt kunde, som betyr at du må velge Tabell. Hvis du oppdaterer produktets listepris, velger du Alle, slik at den nye prisen gjelder for alle kunder. Hvis du skal skille priser mellom ulike kundesegmenter, velger du deretter Gruppe. For å merke Gruppe må du ha definert kundeprisgrupper.  

7. Klikk på rullegardinknappen i **Kontovalg**-feltet for å åpne oppslaget.
8. Finn og velg ønsket post i listen.
9. Velg Tabell i **Varekode**-feltet.
    
    Når du registrerer en forretningsavtale av typen Pris (salg), må du bare velge Tabell i **Varekode**-feltet. Dette skyldes at en pris er en absolutt verdi og kan ikke være lik for alle produkter eller en gruppe produkter.
    
10. Klikk på rullegardinknappen i **Varerelasjon**-feltet for å åpne oppslaget.
11. I listen velger du produktet du vil ha med i avtalen. Noter hvilket produkt du har valgt.  
12. Velg et minimumsantall i **Fra**-feltet.
    - Hvis kunden må bestille et minimumsantall av varen før de kan få tilgang til den nye prisen, må du angi antallet her.  
    - Angi en verdi i feltet **Til** for å angi maksimalt antall som prisen for den avtalen ikke vil være gyldig over. Hvis du tilbyr priser og rabatter som er basert på flere avbruddspunkt for antall, angir du hver antallsintervall som et par av minste og største antall i henholdsvis **Fra**- og **Til**-feltene.
13. Angi en pris i feltet **Beløp i valuta**.
14. Angi en dato som denne avtalen er gyldig fra, i **Fra dato**-feltet i **Detaljer**-delen.
15. Klikk **Lagre**.
16. Klikk på **Valider**.
17. Klikk på **Valider valgte linjer**.
18. Klikk **OK**.
19. Klikk **Poster**.
20. Klikk **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Vise forretningsavtaler for et produkt
1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.
2. I listen finner og velger du produktet som du akkurat har oppdatert prisen for.
3. I **Handlingsrute** klikker du på **Selg**.
4. Klikk på **Vis forretningsavtaler**.
    
    Se gjennom detaljene i forretningsavtalen for priser som du nettopp opprettet.    

5. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser
### <a name="community-blogs"></a>Fellesskapsblogger
- [Salgspriser i Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
