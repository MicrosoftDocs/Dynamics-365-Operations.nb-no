---
title: Trekkprinsipp
description: Dette emnet beskriver de fire trekkprinsippene som brukes for råvareforbruk.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 360172b8029faf128e9ab7e4eb34dfbed3cb3e21
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354042"
---
# <a name="flushing-principles"></a>Trekkprinsipp

[!include [banner](../includes/banner.md)]

Trekkprinsippene gjenspeiler ulike forbruksstrategier for råvarer som skal brukes i produksjonsprosessen. Forbruket er prosessen som trekker materialer fra lageret og setter verdien for de forbrukte materialene til **Varer i arbeid** (VIA) for produksjonsordrer og partiordrer. Råvarene forbrukes vanligvis fra en plassering som er konfigurert for prosessen som bruker materialet. Denne plasseringen er kjent som produksjonsinnleveringsstedet.

Før materialforbruk flyttes materialene til innleveringsstedet. Illustrasjonen nedenfor viser prosessen.

[![scenario4a.](./media/scenario4a.png)](./media/scenario4a.png)

1. Materiallager
2. Råvareplukking
3. Produksjonsinnleveringssted
4. Råvareforbruk
5. Produksjonsprosess

Materialforbruk kontrolleres via følgende fire trekkprinsipper:

- Manuell
- Start
- Ferdig
- Tilgjengelig på lokasjon

Trekkprinsippene er konfigurert i et hierarki av standardverdier. Hierarkiet begynner på frigitt produkt, der trekkprinsippet har verdien **Start**. På en stykklistelinje (BOM) eller formellinje kan trekkprinsippet fra produktet overstyres. Standard trekkprinsippet på stykklistelinjer for produksjon eller satsvise formellinjer for ordren, hentes fra produktet eller den overstyrte verdien i stykklisten eller formler.

## <a name="description-of-the-flushing-principles"></a>Beskrivelse av trekkprinsippene

### <a name="manual"></a>Manuell
Det manuelle trekkprinsippet angir at registrering av materialforbruk er en manuell operasjon. Dette prinsippet gjelder hvis du for eksempel skal kunne spore, og antall brukte partinumre eller serienumre må kunne dokumenteres, for sporingsformål. Manuelt forbruket registreres i en plukklistejournal for produksjon. For varer som er aktivert for avanserte lagerprosesser, kan en håndholdt flyt brukes.

### <a name="start"></a>Start
Start-trekkprinsippet angir at materiale automatisk brukes når produksjonsordren startes. Hvor mye materiale som forbrukes er proporsjonalt med mengden som er startet. Når Start-trekkprinsippet brukes sammen med produksjonsutførelsessystemet, kan det også brukes til å trekke materialer når en operasjon eller en produksjonsjobb er startet. Dette prinsippet gjelder hvis for eksempel avviket i forbruket er lavt, materialene er lavverdimaterialer, det er ingen krav for oppfølging eller det er en kort operasjonstid på operasjoner. 

### <a name="finish"></a>Ferdig
Ferdig-trekkprinsippet angir at materiale automatisk brukes når produksjonsordren er rapportert som fullført, eller når en operasjon som er satt opp til å bruke materialene er registrert som fullført. Hvor mye materiale som forbrukes er proporsjonalt med mengden som er rapportert som ferdig. Når Ferdig-trekkprinsippet brukes sammen med produksjonsutførelsessystemet, kan det også brukes til å trekke materialer når en operasjon eller en produksjonsjobb er fullført. Dette prinsippet er relevant i samme situasjoner som Start-prinsippet. Ferdig-prinsippet er imidlertid for operasjoner som har en lenger operasjonstid, der materialer bør ikke angis til VIA før operasjonen er fullført. 

### <a name="available-at-location"></a>Tilgjengelig på lokasjon
Tilgjengelig på lokasjon-trekkprinsippet angir at materialene automatisk brukes når de er registrert som plukket for produksjon. Materialet er registrert som plukket fra plassering når arbeidet for råvareplukking er fullført, eller når materialet er tilgjengelig på produksjonsinnleveringsstedet og materiallinjen er frigitt til lageret. Plukklisten som genereres under prosessen blir postert i en satsvis jobb. Dette prinsippet er relevant hvis du for eksempel har mange plukkaktivitetene mot én produksjonsordre. I dette tilfellet trenger du ikke å oppdatere plukklisten manuelt, og du kan få et oppdatert bilde av VIA-balansen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]