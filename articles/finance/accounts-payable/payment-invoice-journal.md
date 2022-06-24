---
title: Utlign en betalingsplan i fakturajournalen
description: Denne artikkelen beskriver hvordan du legger til en betaling i leverandørfakturajournalen.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f3ae08ea46be66dd8bf26f7f91bd73f6c5b9192f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863137"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Utlign en betalingsplan i fakturajournalen

[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 Finance versjon 10.0.25 støttes en betalingsplan nå i **Leverandørfakturajournal**.

Hvis du vil bruke denne funksjonaliteten, må du aktivere funksjonen **Bruk betalingsplan på fakturajournal** i Funksjonsbehandling.

Når funksjonen er aktivert, legges det til et nytt **Betalingsplan**-felt på **Fakturajournal**-siden. Når du oppretter en fakturajournallinje, hvis betalingsbetingelsene blir vedlikeholdt for leverandøren og betalingsbetingelsene er valgt i betalingsplanen, oppdateres **Betalingsplan**-feltet på **Fakturajournal**-siden.

Du kan endre betalingsplanen som brukes, i henhold til forretningsbehovet. Under postering av leverandørfakturajournalen blir det opprettet åpne transaksjoner for leverandøren i henhold til betalingsplanen.

 - Hvis du vil gå gjennom flere åpne leverandørtransaksjoner som ble generert fra betalingsplanen, går du til **Leverandører \> Fakturaer \> Åpne leverandørfakturaer** og angir fakturanummeret eller leverandørkontoen.
 - Hvis du vil gå gjennom eller konfigurere betalingsplanen, kan du gå til **Leverandører \> Betalingsoppsett \> Betalingsplan**.
 - Hvis du vil konfigurere betalingsbetingelsene og tilordne en betalingsplan, kan du gå til **Leverandører \> Betalingsoppsett \> Betalingsbetingelser**.
 - Hvis du vil vedlikeholde betalingsbetingelsene for en leverandør, kan du gå til **Leverandører \> Alle leverandører**, velge leverandørkontoen og deretter, på **Betaling**-fanen, angi feltet **Betalingsbetingelser**.

Betalingsplanfunksjonen er også tilgjengelig i prosessen **Register for leverandørfaktura**. Hvis det er valgt en betalingsplan i fakturaregistreringsjournalen, vil det **ikke** bli generert flere leverandørbetalingslinjer når fakturaregisteret posteres. Leverandørbetalingslinjene genereres når fakturaen godkjennes.

## <a name="limitation"></a>Begrensning

Hvis betalingsplanen er i fakturahodet for en ventende leverandørfaktura, finnes det en avansert side hvor brukere kan redigere betalingslinjene. (Brukere kan for eksempel redigere forfallsdatoen og verdien for hver betalingslinje.) Betalingslinjer som genereres fra fakturajournalen, vil ha verdien fra betalingsplanen.

Denne funksjonaliteten blir tilgjengelig for **Leverandørfakturajournal** og **Ventende fakturaer** i en fremtidig versjon.
