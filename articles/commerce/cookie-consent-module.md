---
title: Samtykkemodul for informasjonskapsel
description: Dette emnet dekker samtykkemoduler for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a277ef0634c4ddd5769d278ce6186aac5e84ebfa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352524"
---
# <a name="cookie-consent-module"></a>Samtykkemodul for informasjonskapsler

[!include [banner](includes/banner.md)]

Dette emnet dekker samtykkemoduler for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Samtykkemodulen for informasjonskapsel ber områdebrukere uttrykkelig om å gi samtykke for å tillate informasjonskapsler for alle funksjoner eller moduler som sporer informasjonskapsler for nettlesere. Samtykke er nødvendig første gang en områdebruker blar seg frem til et område i en ny nettleserøkt. Når samtykke er mottatt, spores det, og områdebrukeren blir ikke spurt om samtykke på nytt. Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).

Hvis godkjenning av informasjonskapsler for område ikke er mottatt, vil ingen av funksjonene eller modulene som krever samtykke for informasjonskapsel, vises på siden. Betalingsmodulen, modulen for sosial deling og foretrukkede butikkfunksjon vil for eksempel kreve samtykke for informasjonskapsel, og vil ikke bli gjengitt hvis samtykke for områdebruker ikke er mottatt. 

En samtykkemodul for informasjonskapsel kan konfigureres i en sides topptekstfragment, slik at den kan håndheves når siden lastes. Samtykkemodulen for informasjonskapsel bør ha en tydelig melding som informerer områdebrukeren om bruk av informasjonskapsler på området, og som skal gi en kobling til områdets personvernside.

Illustrasjonen nedenfor fremhever et eksempel på en melding fra informasjonskapselen med en kobling til områdets side for personvernpolicy som vises i toppteksten på en områdeside.
![Eksempel på en samtykkemodul for informasjonskapsel.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Egenskaper for samtykkemodul for informasjonskapsel

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Rik tekst                  | Rik tekst | Angir en varsling i rik tekst til områdebrukere om at området bruker informasjonskapsler for nettleser, og at brukere bør godta bruk av informasjonskapsler for at området skal fungere optimalt. |
| Koblinger | URL | Én eller flere koblinger kan legges til på områdets personvernside som beskriver typene informasjonskapsler som spores på området. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Legg til en tillatelsesmodul for informasjonskapsler på områdesider

Hvis du vil legge til en samtykkemodul for informasjonskapsel på flere områdesider, kan den legges til i et delt topptekstfragment. Når topptekstfragmentet blir lagt til på alle områdesider, vil det automatisk vises en varsling om samtykke for informasjonskapsel første gang en områdebruker går til en områdeside.

Hvis du vil ha mer informasjon om topptekstfragmenter og moduler, kan du se [Topptekstmodul](author-header-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Topptekstmodul](author-header-module.md) 

[Informasjonskapselsamsvar](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]