---
title: Rapporter for utsalgspris
description: Denne artikkelen gir en oversikt over prisrapportfunksjonen, som kan brukes til å vise kommende prisendringer for assorterte produkter.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269034"
---
# <a name="retail-price-reports"></a>Rapporter for utsalgspris

[!include [banner](includes/banner.md)]


Hvis du vil gi konkurransedyktige priser til kundene, endrer forhandlerne ofte priser på varer. Butikksjefer ønsker muligheten til å få enkel tilgang til nylige eller kommende priser, slik at de kan planlegge de nødvendige ressursene for å oppdatere prisetikettene som vises på butikkhyllene. Med frigivelse 10.0 av Retail kan en butikksjef åpne **Pris**-rapporten ved å gå til **Alle butikker \> Butikk \> Prisrapport** og vise de oppdaterte prisene for produktene som er knyttet til butikken. 

For å aktivere rapporten må parameteren **Aktiver prisrapport for butikk** være aktivert. Denne parameteren ligger i fanen **Handelsparametere \> Rabatter \> Diverse**. Ved å åpne siden **Prisrapport** vises en dialogboks med forskjellige konfigurasjoner. De tilgjengelige konfigurasjonene vises nedenfor.

| Konfigurasjon | beskrivelse |
|---|---|
| Fra dato / Til dato| Datointervallet som prisrapporten skal genereres for. Varigheten er for øyeblikket begrenset til 7 dager. |
| Kanal| Butikken som prisrapporten skal genereres for. |
| Vis produkter med tilgjengelig beholdning| Hvis du setter dette til **Ja**, vises priser for bare produktene som for øyeblikket har fysisk beholdning tilgjengelig i lageret. |
| Vis priser for varianter | Hvis du setter dette til **Ja**, vises priser for variantene sammen med produktstandarder. Dette bør bare settes til **På** hvis du har variantspesifikke priser, ettersom antall rader blir svært stor. I fremtidige versjoner vil vi aktivere de dimensjonsbaserte prisene, slik at butikksjefen kan velge dimensjonene som prisene skal vises for. |
| Vis produkter med prisendringer | Hvis du setter dette til **Ja**, vises prisene bare for datoene da prisen ble endret. Prisen for *én dag før* den valgte **Fra dato** vises alltid, slik at butikksjefen enkelt kan identifisere produktene som ikke har endret pris for den valgte varigheten, og også kan vise den gjeldende prisen. |

Når rapporten er generert, kan Excel-filen lastes ned for eventuelle ekstra filtreringsbehov. Prisrapporten kan også brukes til å kontrollere de historiske prisene for produkter for tidligere datoer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
