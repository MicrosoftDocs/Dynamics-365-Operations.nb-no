--- 
title: Definere vurderingsstandarder
description: "Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a>Definere vurderingsstandarder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard. Logistikklederen setter vanligvis opp vurderingsstandardene, avhengig av kontraktene som er signert med transportørene. I dette scenarioet definerer du en vurderingsstandard for en flytransportør. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="set-up-rate-master"></a>Definer vurderingsstandard
1. Gå til Transportstyring > Oppsett > Vurdering > Vurderingsstandard.
2. Klikk Ny.
3. Skriv inn en verdi i Vurderingsstandard-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk rullegardinknappen i feltet ID for metadata for vurdering for å åpne oppslaget.
    * ID-en for metadata for vurdering bestemmer dataene som kreves for vurderingsstandarden fordi den definerer metadataene forventet av TMS-motoren som bruker denne vurderingsstandarden.  
6. I dette eksemplet velger du alternativet P2P
7. Klikk koblingen i den valgte raden i listen.
8. Klikk Lagre.

## <a name="set-up-rate-base"></a>Konfigurer satsgrunnlag
1. Klikk Satsgrunnlag.
    * Satsgrunnlaget bestemmer satsen for transportøren, og kan brukes til å definere en tariffstruktur ettersom den strukturerer satsene i bruddpunktene definert i pausestandarden.  
2. Klikk Ny.
3. Skriv inn en verdi i Satsgrunnlag-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk rullegardinknappen i feltet Pausestandard for å åpne oppslaget.
    * Pausestandarder brukes til å definere prissettingsstrukturen og dens bruddpunkter. Prissettingsstrukturen bruker fordelte priser som er basert på fysiske dimensjoner.  
6. I dette eksemplet bruker du vekt
7. Klikk koblingen i den valgte raden i listen.
8. Aktiver/deaktiver utvidelsen av delen Detaljer.
9. Klikk Ny.
10. Skriv inn 30301 i feltet Fra-postnummer for levering.
11. Skriv inn 30318 i feltet Til-postnummer for levering.
12. Skriv inn USA i feltet Land/område for levering.
13. I feltet <1,00 kg skriver du inn 100.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1 pund.  
14. I feltet <5,00 kg skriver du inn 300.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 5 pund.  
15. I feltet <20,00 kg skriver du inn 500.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 20 pund.  
16. I feltet <100,00 kg skriver du inn 1000.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 100 pund.  
17. I feltet <1.000,00 kg skriver du inn 3000.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1000 pund.  
18. Klikk Lagre.
19. Lukk siden.

## <a name="assign-rate-base"></a>Tilordne satsgrunnlag
1. Aktiver/deaktiver utvidelsen av delen Tilordninger av satsgrunnlag.
2. Klikk Ny.
    * Du kan ha flere tilordninger av satsgrunnlag for hver vurderingsstandard. Dette gjør det mulig å opprette flere forskjellige prispunkter for hver transportør avhengig av mål, tjenester eller andre satsgrunnlag. I denne fremgangsmåten vil du bare opprette én tilordning av satsgrunnlag.  
3. Skriv inn en verdi i Navn-feltet.
4. Klikk rullegardinknappen i feltet Satsgrunnlag for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk rullegardinknappen i feltet Service for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. I feltet Postnummer for henting skriver du inn 98052.
    * Angi hvilket postnummer denne tilordningen av satsgrunnlag skal være gyldig fra.    
10. I feltet Land/område for henting skriver du inn USA.
11. Klikk Lagre.


