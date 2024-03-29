---
title: Leveringsplaner
description: Med leveringsplaner kan du spore ordrelinjeantallet når du bruker flere leveringer for en enkelt salgsordre, et salgstilbud eller en bestilling.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b50558c5da71351082d36276a3185e1f91543f2b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573471"
---
# <a name="delivery-schedules"></a>Leveringsplaner

[!include [banner](../includes/banner.md)]

Med leveringsplaner kan du spore ordrelinjeantallet når du bruker flere leveringer for en enkelt salgsordre, et salgstilbud eller en bestilling.

Bruk en leveringsplan når det totale antallet i en ordre eller en tilbudslinje må leveres i flere leveranser. Individuelle forsendelser representeres av leveringslinjer. To eller flere leveringslinjer utgjør én leveringsplan. Leveringslinjene kan ha andre leveringsdatoer, antall, leveringsmåter og lagerdimensjoner, for eksempel område og lager.  

**Eksempel på en leveringsplan**

| Element                              | Verdi                                    |
|-----------------------------------|------------------------------------------|
| Totalbestilling (opprinnelig ordrelinje) | 600 stoler                               |
| Ønsket leveringsplan       | 100 stoler per måned                     |
| Forespurt tidsramme for levering | 6 måneder, den første dagen i hver måned |

I dette scenariet ber kunden ber om levering av 600 stoler i partier på 100 stoler over en periode på seks måneder. For å holde oversikt over kravene til levering oppretter du en leveringsplan. På siden for leveringstidsplan oppretter du seks separate leveringslinjer. Hver leveringslinje inneholder 100 stoler og angir leveringsdatoen for disse 100 stolene. I dette tilfellet motposteres hver linje den første dagen i måneden i seks måneder etter hverandre.  

Når du oppretter en leveringsplan, endres automatisk den opprinnelige ordrelinjen til **Bestillingslinje med flere leveringer**. En linje av denne typen kalles en kommersielle linje og merkes med et ikon. Leveringslinjen er merket med et annet ikon. Hvis du endrer et antall på en leveringslinje, oppdateres den kommersielle linjen til det totale antallet i leveringsplanen. Hvis en forretningsavtale har definert en sluttrabatt for ordren, sikrer leveringsplanen at bestillingen er kvalifisert for sluttrabatten, selv om ordren er delt inn i separate leveranser.  

Ordrer som har en leveringsplan, behandles mot leveringslinjene. Behandling inkluderer postering av følgesedler, produktkvitteringer og fakturering.  

Dokumentutskrifter av ordrer og tilbud som har en leveringsplan, viser bare leveringslinjene. De vises ikke de opprinnelige linjene (kommersielle linjer). **Merk:** I tillegg vises bare leveringslinjene når du utfører følgende handlinger:

-   Poster
-   Kopier side
-   Bla gjennom listesider og rapporter

Når du bekrefter salgstilbud, viser de resulterende salgsordrene hele leveringsplanen, også ordrelinjene som har flere leveringer. I tillegg vises hele leveringsplanen på alle de viktige sidene, for eksempel salgsordrer, salgstilbud og bestillinger.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]