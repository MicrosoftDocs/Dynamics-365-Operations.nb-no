---
title: Opprette et nytt lageroppsett
description: "Denne fremgangsmåten viser hvordan du definerer informasjon om lokasjonene i lageret."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-warehouse-layout"></a>Opprette et nytt lageroppsett

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du definerer informasjon om lokasjonene i lageret. Dette gjelder bare for lagrene som er opprettet ved hjelp av "grunnleggende lageraktiviteter" i lagermodulen, ikke for lagre som er opprettet i lagerstyringsmodulen. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-the-default-location-capacity"></a>Angi standard lokasjonskapasitet
1. Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.
2. Klikk kategorien Lokasjoner.
3. Angi et nummer i Standardbredde-feltet.
4. Angi et nummer i Standarddybde-feltet.
5. Angi et tall i Standardhøyde-feltet.
6. Klikk Lagre.
7. Lukk siden.

## <a name="define-the-location-name-format"></a>Definer formatet for plasseringsnavn
1. Gå til Lagerstyring > Oppsett > Lageroppdeling > Lagre.
2. Klikk Ny.
3. Skriv inn en verdi i Lager-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Aktiver/deaktiver utvidelsen av delen Lokasjonsnavn.
    * Alternativene i denne delen definerer standardformatet for lokasjonsnavn. I vårt eksempel skal vi ta med gangnummer, reolnummer og hyllenummer.  
8. Sett alternativet Inkluder gang til Ja.
9. Sett alternativet Ta med reol til Ja.
10. I Format-feltet velger du en verdi for reolen.
    * For eksempel: -##  
11. Sett alternativet Ta med hylle til Ja.
12. I Format-feltet velger du en verdi for hyllen.
    * For eksempel: -##  

## <a name="define-warehouse-locations"></a>Definer lagerlokasjoner
1. Klikk Lager i handlingsruten.
2. Klikk Lokasjonsveiviser.
3. Klikk Neste.
4. Fjern merkingen av alternativet Utleveringsporter
5. Fjern merkingen av alternativet Bulklokasjoner
6. Klikk Neste.
7. Klikk Neste.
8. Klikk Neste.
9. Klikk Neste.
10. Klikk Neste.
11. Klikk Neste.
12. Klikk Neste.
    * Legg merke til at de fysiske dimensjonene som vises på denne siden er de du angir i begynnelsen av denne fremgangsmåten.  
13. Klikk Neste.
14. Klikk Finish.
15. Lukk siden.
16. Oppdater siden.

