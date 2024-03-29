---
title: Manuell oppdatering av anleggsmiddeltellere
description: Denne artikkelen beskriver manuell oppdatering av aktivatellere i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30c672286c16a4353556a507019960edb93f8b1b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016601"
---
# <a name="manual-update-of-asset-counters"></a>Manuell oppdatering av anleggsmiddeltellere

[!include [banner](../../includes/banner.md)]



Tellere brukes til å opprette registreringer for aktiva, for eksempel registreringer om antall timer som aktivumet har vært i operasjon, eller antallet som er produsert.

Tellertypen som er valgt for en teller, kan være satt til å arve tellerverdier. Med andre ord er alternativet **Arv aktivatellerverdier** satt til **Ja** i hurtigfanen **Generelt** på siden **Tellere** (**Aktivabehandling** > **Oppsett** > **Aktivatyper** > **Tellere**). I dette tilfellet oppdateres alle underordnede aktiva som bruker den samme tellertypen, automatisk når du oppretter en ny tellerlinje av denne typen.

På siden **Alle aktiva** oppretter du tellerregistreringer for timer eller antall for et aktivum basert på avlesningene for aktivumet.

1. Velg **Aktivastyring** > **Aktiva** > **Alle aktiva**.

2. Velg aktivumet, og deretter velger du **Tellere**, i handlingsruten, fanen **Aktiva** i gruppen **Forebyggende**. Siden **Aktivatellere** viser en liste over alle tidligere tellerregistreringer som er gjort for det valgte aktivumet.

3. Velg **Ny** for å opprette en registrering. Aktiva-ID angis automatisk i **Aktiva**-feltet.

4. Velg den aktuelle telleren i **Teller**-feltet. Bare tellere som er relatert til aktivatypen som er valgt i aktivumet, er tilgjengelige for valg. Den aktuelle enheten settes inn automatisk i **Enhet**-feltet.

5. I feltet **Registrert** velger du dato og klokkeslett for tellerregistreringen.

6. I feltet **Verdi** angir du tallet siden den forrige tellerregistreringen. Du kan også angi samlet tellerantall i feltet **Aggregert verdi**.

Merk følgende punkt:

- Hvis du fysisk installerer en ny teller på et aktivum, må du registrere endringen i aktivumet på siden **Aktivatellere**. Deretter må du opprette to registreringslinjer som har identiske tidsstempler. Den første linjen må være for telleren du erstatter. I linjen som er knyttet til den nye telleren, merker du av for **Tilbakestill teller**. I **Total**-feltet er totalt antall summen av tellertotalene for alle registrerte verdier på denne tellertypen.

- Hvis det er merket av for **Tilbakestill teller** for et aktivum ved hjelp av en vedlikeholdsplan med intervalltypen Én gang fra... eller Når nådd..., er telleren fremdeles aktiv på den nye tellerlinjen fordi du oppretter en egen tellerlinje og begynner på nytt med en ny teller.

Illustrasjonen nedenfor viser et eksempel på siden **Aktivatellere**.

![Figur 1.](media/11-work-orders.png)

På siden **Aktivatellere** (**Aktivabehandling** > **Forespørsler** > **Aktiva** > **Aktivatellere**) kan du utføre tellerregistreringer for flere aktivumer samtidig etter behov.

>[!NOTE]
>Du kan definere et område for å definere avvik i manuelle tellerregistreringer. Du kan også angi hvilken type melding som skal vises hvis registreringer er utenfor det definerte området. Hvis du vil ha informasjon om hvordan du definerer tellere, se [Tellere](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]