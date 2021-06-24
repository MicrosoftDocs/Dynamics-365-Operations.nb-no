---
title: Oversikt over øyeblikksbilder (forhåndsversjon)
description: Dette emnet beskriver øyeblikksbildefunksjonen, som gjør at du kan lagre en kontantflytprognose for analyse eller sammenligning med faktiske data senere. Når du genererer en kontantstrømprognose, kan du lagre denne prognosen som et øyeblikksbilde. Du kan deretter bruke disse øyeblikksbildene til å redigere kontoene som var inkludert i prognosen, eller sammenligne prognosen i øyeblikksbildet med faktiske data.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 593d6fa8efdecf1b64ef802e6861783d6f85489c
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186596"
---
# <a name="snapshots-overview-preview"></a>Oversikt over øyeblikksbilder (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ved hjelp av øyeblikksbilder kan organisasjoner redigere og lagre informasjon om likviditetsbeholdningen og kontantstrømprognoser på et tidspunkt. Du kan sammenligne øyeblikksbildet med faktisk finans, undersøke avviket og bruke denne informasjonen til å forbedre kontantstrømprognoser over tid. Mer spesifikt kan øyeblikksbilder brukes på følgende måter:

- Spor likviditetsbeholdning og kontantstrømprognoser over tid.
- Filtrer dataene for å vise et delsett av juridiske enheter som øyeblikksbildet ble opprettet for.
- Rediger likviditetsbeholdning og kontantstrømprognosen som ble generert av systemet.
- Utfør hva-skjer-hvis-analyse for å vurdere visninger for optimistisk, pessimistisk og mest sannsynlig for kontantstrømmen.
- Sammenlign den faktiske økonomiske ytelsen med prognosen som er lagret i øyeblikksbildet.

Du kan opprette et øyeblikksbilde ved å velge **Nytt øyeblikksbilde** enten i kategorien **Likviditetsbeholdning** eller i kategorien **Kontantstrømprognose** i arbeidsområdet for **Kontantstrømprognose**. Når et øyeblikksbilde opprettes, kan innflyten og utflyten i det redigeres og lagres. Alle lagrede øyeblikksbilder er tilgjengelige i kategorien **Øyeblikksbilder**. Hvis du vil åpne et øyeblikksbilde, velger du navnet.

Kontantinnflytene og -utflytene i øyeblikksbilder kan redigeres når som helst. Når et innflytbeløp eller et utflytbeløp redigeres, blir det oppdaterte beløpet fordelt til likviditetskontoene som opprettet den opprinnelige saldoen. Når du er ferdig med å redigere et øyeblikksbilde, velger du **Lagre** for å lagre endringene.

Hvis du vil sammenligne flere øyeblikksbilder, velger du **Sammenlign øyeblikksbilder**. Du kan sammenligne to øyeblikksbilder om gangen. Velg de to øyeblikksbildene som skal sammenlignes, og velg deretter **OK**. Siden **Sammenlign øyeblikksbilde** vil vise en sammenligning av de valgte øyeblikksbildene. Diagrammet på den øvre delen av siden viser en sammenligning av kontantinnflytene, kontantutflytene og banksaldoer i de overlappende periodene mellom de to øyeblikksbildene. Rutenettet i den nedre delen viser en detaljert sammenligning av de to prognosene for hvert likviditetsbeløp. **Avvik**-kolonnen i rutenettet viser differansen mellom saldoene i en periode.

Hvis du vil sammenligne faktiske økonomiske resultater med en prognose som ble lagret som et øyeblikksbilde, velger du **Sammenlign med faktiske data**. Siden **Sammenlign øyeblikksbilde** vil vise en sammenligning av de faktiske beløpene og prognosen. Diagrammet på den øvre delen av siden viser en sammenligning av kontantinnflytene, kontantutflytene og banksaldoer i de overlappende periodene mellom de to øyeblikksbildene. Rutenettet i den nedre delen viser en detaljert sammenligning av faktiske saldoer per periode og prognosesaldoen for hver likviditetsbeløp. **Avvik**-kolonnen i rutenettet viser differansen mellom den faktiske balansen i en periode og prognosesaldoen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
