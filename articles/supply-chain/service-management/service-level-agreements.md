---
title: Oversikt over servicenivåavtaler
description: I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1db12600aa47f537da6918c82ef3164c2123a8ac
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670811"
---
# <a name="service-level-agreements-overview"></a>Oversikt over servicenivåavtaler       

[!include [banner](../includes/banner.md)]


En servicenivåavtale er en avtale mellom et servicefirma og en servicekunde. I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.

En servicenivåavtale sørger for et standard servicenivå som tilbys kundene, og gjør det åpenbart for servicefirmaet når en servicejobb bør være ferdig.

Du kan opprette en rekke serviceavtalenivåer for å tilby ulike servicenivå til servicekunder.

## <a name="create-a-service-level-agreement"></a>Opprett en servicenivåavtale.

1.  Klikk på **Servicestyring** \> **Oppsett** \> **Serviceavtaler** \> **Servicenivåavtaler**.

2.  Skriv inn navnet på servicenivåavtalen i feltet **Servicenivåavtale**.

3.  Skriv inn klokkeslettet du ønsker å kunne fullføre servicebesøk som er knyttet til servicenivåavtalen. Velg deretter en kalender hvis du vil basere servicenivåavtalen på en bestemt kalender.

## <a name="apply-a-service-level-agreement"></a>Bruk en servicenivåavtale.

Servicenivåavtalen brukes direkte på en serviceavtale.

Serviceordrer som du oppretter manuelt og knytter til en serivceavtale som har en servicenivåavtale, måles mot denne servicenivåavtalen.

Serviceordrer som du oppretter automatisk, er ikke knyttet til en servicenivåavtale.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Bruk servicenivåavtalen for serviceavtalen

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**. Velg serviceavtalen du vil bruke servicenivåavtalen for, og klikk deretter **Rediger** i **handlingsruten**.

2.  I feltet **Servicenivåavtale** velger servicenivåavtalen du vil tilordne.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Bruk servicenivåavtalen for serviceavtalegruppen

1.  Klikk på **Servicestyring** \> **Oppsett** \> **Serviceavtaler** \> **Serviceavtalegrupper**.

2.  I feltet **Servicenivåavtale** velger servicenivåavtalen du vil tilordne.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Spor tid på en serviceordre mot en servicenivåavtale

Når du oppretter en ny serviceordre for en serviceavtale som en servicenivåavtale er tilordnet til, startes tidsintervallet for levering av tjenesten, og systemet starter å spore leveringstiden. I tillegg har du følgende alternativer:

  - Du kan starte og stanse tidsregistrering for serviceordren for å registrere den totale tiden som er brukt på serviceordrer.

  - Du kan overvåke overholdelse av tidsintervallet som er angitt i servicenicåavtalen.

  - Du kan definere årsakskoder som må angis hvis tidsintervallet til servicenivåavtalen overskrides.

## <a name="see-also"></a>Se også

[Vise samsvar med servicenivåavtaler](view-compliance-with-service-level-agreements.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]