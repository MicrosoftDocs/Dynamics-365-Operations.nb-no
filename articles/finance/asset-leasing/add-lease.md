---
title: Legge til eller kopiere leieavtaler (forhåndsversjon)
description: Denne artikkelen beskriver hvordan du oppretter en ny leieavtale ved å angi informasjon for den i Aktivaleie, eller kopierer informasjon fra en eksisterende leieavtale.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880939"
---
# <a name="add-or-copy-leases-preview"></a>Legge til eller kopiere leieavtaler (forhåndsversjon)

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du oppretter en leieavtale fra grunnen av i Aktivaleie, og hvordan du oppretter en leieavtale ved å kopiere en eksisterende leieavtale. Fremgangsmåten for å opprette en leieavtale fra grunnen av, omfatter å registrere informasjon for den nye leieavtalen og deretter opprette en leieplan. Etter at minst én leieavtale er opprettet, kan det være enklere å kopiere informasjonen fra en eksisterende leieavtale og deretter redigere denne informasjonen etter behov for å opprette en ny leieavtale.

## <a name="create-a-lease"></a>Opprette en leieavtale

Følg disse trinnene for å opprette en leieavtale i Aktivaleie.

1. I handlingsruten på siden **Leiesammendrag** i velger du **Ny**.
2. Angi leieavtaleinformasjonen. Obligatoriske felt har røde kantlinjer.

Startdatoen for leiebetalingen kan ikke være tidligere enn startdatoen for leien. Hvis du angir en startdato for leiebetalingen som er tidligere enn startdatoen for leien, får du en feilmelding.

Som standard er alternativet **Oppdeling av betalingsbeløp** på hurtigfanen **Generelt** på siden **Leiedetaljer** angitt til **Nei** hvis alternativet **Tillat oppdeling av betaling** på siden **Parametere for aktivaleie** er satt til **Ja**. 

Hvis alternativet **Oppdeling av betalingsbeløp** er satt til **Ja**, er **Betalingsbeløp**-feltet på hurtigfanen **Linjer i betalingsplan** låst. Dette blir angitt til totalen for betalingsbeløpene som angis senere i katalogen **Oppdeling av betalingsbeløp**.

Velg **Oppdelin av betalingsbeløp** for å åpne en side der du kan legge til de spesifiserte betalingstypene. Knappen **Legg til totaler i betalingsbeløp** flytter totalene til **Betalingsbeløp**-feltet.

> [!NOTE]
> Hvis du legger til et spesisert betalingsbeløp og deretter velger **Esc**-tasten, blir ikke de angitte beløpene lagt til i **Betalingsbeløp**-feltet på hurtigfanen **Linjer i betalingsplan**. I stedet lagres de i dialogboksen **Oppdeling av betalingsbeløp**. Hvis du vil at dialogboksen skal vise totalbeløpet, velger du **Beløp**-kolonnen, velger og holder (eller høyreklikker) og velger deretter **Summer denne kolonnen**. 

Knappen **Kopier linje** kopierer den spesifiserte betalingsoppdelingen.

## <a name="create-a-lease-schedule"></a>Opprette en leieplan

Når du er ferdig å registrere informasjon for leieavtalen, kan du følge disse trinnene for å opprette en leieplan.

> [!NOTE]
> Finansdimensjonene kan endres, avhengig av eventuelle egendefinerte finansdimensjoner.

1. Velg **Opprett tidsplaner** for å generere leietablåene. Leietablåene inneholder tidsplaner for betaling, nedbetaling, avskrivning og utgift.
2. Hvis du vil ha tilgang til leietablåene og vise nyopprettede tidsplaner, velger du **Tablåer**-fanen.

    Siden **Tablådetaljer** viser hvordan leieavtalen gjøres rede for av tablåene som er tilordnet den. Herfra kan du vise leieplanene.

    Betalingsplanen inneholder inndataene fra fanen **Linjer i betalingsplan** på siden **Legg til leieavtale**. Du kan fortsatt endre hvert betalingsbeløp og hver variable betaling. Leieforpliktelsen beregnes på grunnlag av den endrede betalingsplanen.

    > [!NOTE]
    > Startdatoen for leiebetalingen må være den samme eller en senere dato enn startdatoen for leien. Du får en feilmelding hvis startdato for leiebetalingen er tidligere enn startdatoen for leien. 

4. Når du er ferdig å se gjennom betalingsplanen, velger du **Bekreft tidsplan**. Etter at tidsplanen er bekreftet, er ikke leieavtalen lenger tilgjengelig for redigering.

    > [!NOTE]
    > Systemet beregner automatisk leieperioden fra linjene i betalingsplanen på siden **Legg til leieavtale**.
    >
    > For å beregne leieperioden i måneder finner systemet differansen mellom startdatoen og sluttdatoen for en bestemt linje i betalingsplanen. Den går deretter videre til neste linje i betalingsplanen og finner differansen på nytt. Til slutt summerer systemet alle beløpene for å fastsette leieperioden i måneder.

5. Hvis du vil vise de beregnede renteutgiftene for perioden, åpner du siden **Nedbetalingsplan for gjeld**. Hvis du vil vise beregnet lineær avskrivning, åpner du siden **Avskrivningsplan for aktiva**.
6. Når du er ferdig å se gjennom det beregnede beløpet, kan du opprette journaloppføringen for opprinnelig føring på siden **Opprinnelig føring**. Du får en melding om at journalen er opprettet.

    > [!NOTE]
    > Journaloppføringen posteres ikke i Økonomimodul før du posterer oppføringen manuelt.

7. Hvis du vil se gjennom den foreslåtte oppføringen for opprinnelig føring før du posterer den, velger du **Journal for aktivaleie**.

    > [!NOTE]
    > Du kan ikke opprette journalen for aktivaleie manuelt. Den blir automatisk opprettet når leieplaner opprettes.

8. Når du er ferdig å se gjennom journaloppføringen for opprinnelig føring og er klar til å postere den, velger du **Poster** for å føre bruksrettseiendelen og leieforpliktelsen i Økonomimodul.

## <a name="copy-a-lease"></a>Kopiere en leieavtale

Aktivaleie lar deg kopiere detaljene for en leieavtale for å opprette en ny leieavtale med samme informasjon. Du kan deretter endre leieavtalefeltene før du oppretter tidsplanene for den kopierte leieavtalen.

1. På siden **Leiesammendrag** velger du leieavtalen du vil kopiere, og deretter velger du **Kopier leieavtale** i handlingsruten.

    > [!NOTE]
    > Hvis parameteren **Manuell** er deaktivert for nummerserien for leie-ID-er, genereres neste nummer i serien automatisk som leie-ID-en til den kopierte leieavtalen. Hvis parameteren **Manuell** er aktivert, får du en melding der du blir bedt om å angi leie-ID-en før du kopierer leieavtalen.

2. Velg **Kopier**. Leieavtaledetaljene fra den valgte leieavtalen kopieres til en ny leieavtale. Du kan deretter redigere detaljene i den nye leieavtalen før du lagrer den og oppretter leieplanene.

## <a name="asset-leasing-journal"></a>Journal for aktivaleie

Alle journaloppføringer som opprettes i Aktivaleie, befinner seg i journalen for aktivaleie. På siden **Journal for aktivaleie** (**Aktivaleie \> Journaloppføringer \> Journal for aktivaleie**) kan du filtrere etter posteringsstatus, vise bestemte journaloppføringer og bilagene og postere uposterte journaloppføringer.

> [!NOTE]
> Du kan ikke opprette journalen for aktivaleie manuelt. Den blir automatisk opprettet når leieplaner opprettes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
