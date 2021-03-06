---
title: Oversikt over servicenivåavtaler
description: I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55d65de5c041bd100bf8267bdbe3c5c5eb061a61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835924"
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