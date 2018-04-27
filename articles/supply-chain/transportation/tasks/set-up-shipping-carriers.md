--- 
title: "Definere transportører"
description: "Denne prosedyren viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-shipping-carriers"></a>Definere transportører

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du konfigurerer en transportør og definere operasjoner, for eksempel service, forsendelsesmåte, transportbetalingsmiddel, transportbegrensninger og forsendelsessats. En transportkoordinator kan deretter tilordne en transportør til en innkommende eller utgående last.


## <a name="create-a-new-shipping-carrier"></a>Opprett en ny transportør
1. Gå til Transportstyring > Oppsett > Transportører > Transportører.
2. Klikk Ny.
3. Skriv inn en verdi i Transportør-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk rullegardinknappen i Modus-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Fyll ut generell informasjon om transportøren
1. Aktiver/deaktiver utvidelsen av delen Oversikt.
2. Merk eller fjern merket for Aktiver transportør.
3. Klikk rullegardinknappen i feltet Leverandør for å åpne oppslaget.
    * Velg leverandørkontoen som transportøren skal tilordnes til.  
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Velg et alternativ i feltet Transportbetalingsmiddel.
    * Velg Manuell for å bruke siden Transportbetalingsmiddel, eller velg EDI for å oppdatere betalingsmiddelet ved hjelp av utveksling av elektroniske data (EDI – Electronic Data Interchange).  
7. Merk eller fjern merket for Aktiver transportørrangering.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Opprett de nødvendige tjenestene for transportøren
1. Aktiver/deaktiver utvidelsen av delen Tjenester.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i Transportørtjeneste-feltet.
5. Skriv inn en verdi i Navn-feltet.
6. Klikk rullegardinknappen i feltet Transportmetode for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Definer adressen for transportør (valgfritt)
1. Aktiver/deaktiver utvidelsen av delen Adresser.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Navn eller beskrivelse.
4. Klikk rullegardinknappen i feltet Land/område for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk rullegardinknappen i feltet Postnummer for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Skriv inn en verdi i Gate-feltet.
10. Klikk OK.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Definer vurderingsprofilen for transportøren
1. Aktiver/deaktiver utvidelsen av delen Vurderingsprofiler.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i feltet Vurderingsprofil.
5. Skriv inn en verdi i Navn-feltet.
6. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.
10. Finn og velg ønsket post i listen.
11. Klikk koblingen i den valgte raden i listen.
12. Klikk rullegardinknappen i feltet Ratemotor for å åpne oppslaget.
    * Velg ratemotoren som er i samsvar med kontrakten du har med transportøren.  
13. Finn og velg ønsket post i listen.
14. Klikk koblingen i den valgte raden i listen.
15. Klikk rullegardinknappen i feltet Vurderingsstandard for å åpne oppslaget.
16. Finn og velg ønsket post i listen.
17. Klikk koblingen i den valgte raden i listen.
18. Klikk rullegardinknappen i feltet Transittidmotor for å åpne oppslaget.
19. Klikk koblingen i den valgte raden i listen.
20. Klikk Lagre.


