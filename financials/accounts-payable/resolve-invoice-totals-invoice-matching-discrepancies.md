---
title: "Løse avvik under kontroll for fakturatotaler"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c947f84e6510073d49045f93af703c16d0ebc1ba
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Løse avvik under kontroll for fakturatotaler

[!include[banner](../includes/banner.md)]




Én type fakturakontrollvalidering er kontroll av fakturatotaler. For å angi at systemet skal utføre kontroll av fakturatotaler går du til siden **Leverandørparametere**, kategorien **Fakturavalidering** og setter alternativet **Samsvar fakturatotaler** til **Ja**. 

Du kan bruke kontroll av fakturatotaler som hjelp for å garantere at totale fakturabeløp ikke avviker fra forventede beløp med mer enn et godkjent avvik. Seks totaler sammenlignes på siden **Samsvarende detaljer for fakturatotaler**. Hvis noen av totalene avviker fra den forventede tilsvarende bestillingstotalen, flagges et samsvarsavvik. 

For å se gjennom fakturaen med totalsamsvarsavvik går du til arbeidsområdet **Leverandørfakturaregistrering** og klikker flisen **Ventende fakturaer**. Gå deretter til handlingsruten, velg kategorien **Gjennomgang**, og klikk **Samsvarende detaljer**. Hvis samsvarsavvik er oppdaget, vises advarselsikoner ved siden av fakturabeløpet. Du kan vise mer detaljert informasjon om totalene ved å vise samsvarende detaljer for fakturatotaler. 

Når du identifiserer et avvik, kan du det hende du må kontakte leverandøren hvis mener at informasjon i fakturaen er feil. Avhengig av den resulterende avtalen med leverandøren kan du deretter gjøre ett av følgende:

-   Godta prisavviket og postere fakturaen som har samsvarende avvik. Systemet kan være konfigurert til å kreve godkjenning før det kan postere hvis det finnes samsvarende avvik. I så fall må du godkjenne det samsvarende avviket og du kan eventuelt skrive inn en merknad om godkjenning. Du kan deretter velge å postere fakturaen.
-   Korriger fakturabeløpet til det forventede beløpet og poster fakturaen.
-   Be om at leverandøren krediterer hele beløpet og gir deg en ny, korrigert faktura.





