---
title: Definere vurderingsstandarder
description: Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47fa7edeba81d826a00668a2da74113f552437f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974266"
---
# <a name="set-up-rate-masters"></a>Definere vurderingsstandarder

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du setter opp en vurderingsstandard. Logistikklederen setter vanligvis opp vurderingsstandardene, avhengig av kontraktene som er signert med transportørene. I dette scenarioet definerer du en vurderingsstandard for en flytransportør. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

## <a name="set-up-break-master"></a>Definere pausestandard

1. Gå til **Transportstyring > Oppsett > Vurdering > Pausestandard**. Pausestandarder brukes til å definere prissettingsstrukturen og dens bruddpunkter. Prissettingsstrukturen bruker fordelte priser som er basert på fysiske dimensjoner.  
1. Velg **Ny**.
1. Angi en verdi i feltet **Pausestandard**.
1. Angi en verdi i feltet **Navn**.
1. I **Datatype**-feltet velger du datatypen.
1. I **Sammenligning**-feltet angir du den typen sammenligning som er forespurt (ved hjelp av operatorer).
1. I **Pauseenhet**-feltet angir du pauseenheten.
1. I **Detaljer**-delen oppretter du så mange pauser som nødvendig for prissettingsstrukturen.
1. Velg **Lagre**.

## <a name="set-up-rate-master"></a>Definer vurderingsstandard

1. Gå til **Transportstyring > Oppsett > Vurdering > Vurderingsstandard**.
1. Velg **Ny**.
1. Skriv inn en verdi i **Vurderingsstandard**-feltet.
1. Skriv inn en verdi i **Navn**-feltet.
1. Velg rullegardinknappen i feltet **ID for metadata for vurdering** for å åpne oppslaget. ID-en for metadata for vurdering bestemmer dataene som kreves for vurderingsstandarden fordi den definerer metadataene forventet av transportstyringsmotoren som bruker denne vurderingsstandarden.  
1. I dette eksemplet velger du alternativet P2P. Dette er allerede definert i demodataene.
1. Velg koblingen i den valgte raden i listen.
1. Velg **Lagre**.

## <a name="set-up-rate-base"></a>Konfigurer satsgrunnlag

1. Velg **Satsgrunnlag**.
    * Satsgrunnlaget bestemmer satsen for transportøren, og kan brukes til å definere en tariffstruktur ettersom den strukturerer satsene i bruddpunktene definert i pausestandarden.  
2. Velg **Ny**.
3. Skriv inn en verdi i **Satsgrunnlag**-feltet.
4. Skriv inn en verdi i **Navn**-feltet.
5. Velg rullegardinknappen i feltet **Pausestandard** for å åpne oppslaget.
    * Pausestandarder brukes til å definere prissettingsstrukturen og dens bruddpunkter. Prissettingsstrukturen bruker fordelte priser som er basert på fysiske dimensjoner.  
6. I dette eksemplet bruker du vekt. Dette er allerede definert i demodataene.
7. Velg koblingen i den uthevede raden i listen.
8. Vis delen **Detaljer**.
9. Velg **Ny**.
10. Skriv inn 30301 i feltet **Fra-postnummer for levering**.
11. Skriv inn 30318 i feltet **Til-postnummer for levering**.
12. Skriv inn USA i feltet **Land/område for levering**.
13. I feltet **<1,00 kg** skriver du inn 100.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1 pund.  
14. I feltet **<5,00 kg** skriver du inn 300.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 5 pund.  
15. I feltet **<20,00 kg** skriver du inn 500.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 20 pund.  
16. I feltet **<100,00 kg** skriver du inn 1000.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 100 pund.  
17. I feltet **<1.000,00 kg** skriver du inn 3000.
    * Sett inn satsen per pund hvis den samlede vekten for lasten er mindre enn 1000 pund.  
18. Velg **Lagre**.
19. Lukk siden.

## <a name="assign-rate-base"></a>Tilordne satsgrunnlag

1. Vis delen **Tilordninger av satsgrunnlag**.
2. Velg **Ny**.
    * Du kan ha flere tilordninger av satsgrunnlag for hver vurderingsstandard. Dette gjør det mulig å opprette flere forskjellige prispunkter for hver transportør avhengig av mål, tjenester eller andre satsgrunnlag. I denne fremgangsmåten vil du bare opprette én tilordning av satsgrunnlag.  
3. Skriv inn en verdi i **Navn**-feltet.
4. Velg rullegardinknappen i feltet **Satsgrunnlag** for å åpne oppslaget.
5. Velg koblingen i den uthevede raden i listen.
6. Velg rullegardinknappen i feltet **Tjeneste** for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Velg koblingen i den uthevede raden i listen.
9. I feltet **Postnummer for henting** skriver du inn 98052.
    * Angi hvilket postnummer denne tilordningen av satsgrunnlag skal være gyldig fra.
10. I feltet **Land/område for henting** skriver du inn USA.
11. Velg **Lagre**.
