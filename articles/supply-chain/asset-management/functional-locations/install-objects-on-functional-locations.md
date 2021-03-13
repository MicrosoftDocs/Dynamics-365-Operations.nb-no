---
title: Installere aktiva på arbeidssteder
description: Dette emnet forklarer hvordan du installerer aktiva på arbeidssteder i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea67e2392d8e25a2a5f3cb7e1ff5032322f2c48
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022036"
---
# <a name="install-assets-on-functional-locations"></a>Installere aktiva på arbeidssteder

[!include [banner](../../includes/banner.md)]

 

Når du har opprettet arbeidsstedsstrukturer, er neste trinn å installere aktiva på de relevante arbeidsstedene. Dette emnet forklarer hvordan du installerer aktiva på disse arbeidsstedene i Aktivastyring. Se [Introduksjon til aktiva](../objects/introduction-to-objects.md) hvis du vil ha mer informasjon om hvordan du oppretter aktiva.

Hvis du har opprettet en aktivastruktur, må hele aktivastrukturen være installert på et arbeidssted. Derfor kan bare overordnede objekter (aktiva på øverste nivå som har ingen overordnede objekter) velges på et arbeidssted. Alle tilknyttede underordnede aktiva (underaktiva) vil også bli installert på arbeidsstedet. Når du installerer aktiva på et arbeidssted, kan finansdimensjonene for arbeidsstedet automatisk overføres til dem, avhengig av oppsettet for arbeidsstedstypen som er valgt for arbeidsstedet. Hvis du vil ha mer informasjon om hvordan du oppretter arbeidsstedstyper, se [Arbeidsstedstyper](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Du kan definere aktivatyper på arbeidsstedstypen som brukes for et arbeidssted. I dette tilfellet, når du installerer aktiva på arbeidsstedet, vises bare overordnede objekter som har samme aktivatype i listen over aktiva som kan installeres på arbeidsstedet.

Når du har installert aktiva på et arbeidssted, kan du erstatte et overordnet objekt eller en aktivastruktur etter behov. Når du installerer aktiva, velger du et overordnet objekt som skal erstattes. Alle relaterte underordnede aktiva vil også bli erstattet. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Installere en aktivastruktur på et arbeidssted

1. Velg **Aktivastyring** \> **Felles** \> **Arbeidssteder** \> **Alle arbeidssteder** eller **Aktive arbeidssteder**.
2. Velg arbeidsstedet der det skal installeres et aktivum.
3. Velg **Installer aktivum**.

    **Attributter**-delen viser en liste over kravene til aktivaattributtet som er definert på arbeidsstedstypen som er valgt for arbeidsstedet. Attributtene er bare beregnet til informasjon. Systemet validerer ikke attributtene mot aktivaattributtene som er definert på aktivumet som du installerer. Du må gjøre denne valideringen når du velger et aktivum i **Aktiva**-feltet.

4. I **Aktiva**-feltet velger du det overordnede aktivumet som skal installeres. Alle relaterte underordnede aktiva inkluderes automatisk i installasjonen.

    Delen **Aktivaattributter** til høyre for listen over aktiva viser aktivaattributtene som er knyttet til det valgte aktivumet.

5. I **Gyldighet**-feltet velger du datoen og klokkeslettet da aktivainstallasjonen er gyldig fra. Etter dette tidspunktet vil kostnader for aktivumet og relaterte underaktiva være knyttet til arbeidsstedet.

    > [!NOTE]
    > Aktivaattributtene som er definert på aktivumet, legges til i **Attributter**-delen. Kravet til **Vekt**-attributtet er for eksempel lagt til som et krav på både aktivumet og arbeidsstedet. Hvis aktivumet har attributtkrav av samme type som arbeidsstedet, angis verdiene for aktivumets attributtkrav i **Verdi**-feltene. Derfor kan du validere aktivaverdiene mot attributtkravene som er definert på arbeidsstedet. Attributtkravene som er definert på arbeidsstedet, er merket med en hake.

6. Velg **OK**.

    > [!NOTE]
    > Hvis du vil endre installasjonen av et aktivum ved å installere det på et nytt arbeidssted, følger du trinn 1 til 6 i denne fremgangsmåten. Når du installerer et aktivum på et nytt arbeidssted, avinstalleres aktivumet automatisk fra det forrige arbeidsstedet. Alle aktive vedlikeholdsforespørsler eller arbeidsordrer som ble opprettet på aktivumet før du installerte det på et nytt arbeidssted, overføres **ikke** automatisk til det nye arbeidsstedet. Hvis disse vedlikeholdsforespørslene og arbeidsordrene fortsatt er nødvendige for aktivumet, må du opprette dem på nytt manuelt etter at aktivumet er installert på den nye lokasjonen.

7. Hvis du vil vise en liste over alle aktivaene, inkludert underaktiva, som er installert på arbeidsstedet, velger du arbeidsstedet på siden **Alle arbeidssteder** og velger deretter **Aktiva**.
8. Hvis du vil vise en liste over aktive vedlikeholdsforespørsler, aktive arbeidsordrer eller feilregistreringer som er knyttet til aktivaene som er installert på et arbeidssted, velger du arbeidsstedet på siden **Alle arbeidssteder**, og deretter velger du **Forespørsler**, **Arbeidsordrer** eller **Feil**.

> [!NOTE]
> Når aktivarelaterte data endres, oppdateres de automatisk på arbeidsstedet som aktivumet er installert på. Denne automatiske oppdateringen gjelder endringer i vedlikeholdsforespørsler, arbeidsordrer, registreringer av feil på aktiva, registreringer av vedlikeholdsavbrudd og aktivamålregistreringer.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Opprette ett aktivum automatisk på et arbeidssted

Du kan definere arbeidsstedsfaser og arbeidsstedstyper for å håndtere automatisk opprettelse av *ett* aktivum på et arbeidssted. Aktivumet får samme ID og navn som arbeidsstedet. Denne funksjonaliteten kan være nyttig når du håndterer vedlikehold på et stort statisk aktivum, for eksempel en bygning.

Før du kan opprette et aktivum automatisk på et arbeidssted, må følgende oppsettsdata være tilgjengelige:

- Opprett en arbeidsstedstype for å håndtere automatisk opprettelse av et aktivum. I **Aktivatype**-feltet velger du en aktivatype. Hvis du vil har mer informasjon, kan du se [Arbeidsstedstyper](../setup-for-functional-locations/functional-location-types.md).
- Opprett en livssyklustilstand for arbeidssted for å håndtere automatisk opprettelse av et aktivum. Sett alternativet **Opprett aktivum** til **Ja**. Hvis du vil har mer informasjon, kan du se [Livssyklustilstander for arbeidssteder](../setup-for-functional-locations/functional-location-stages.md).

Når oppsettsdataene er tilgjengelige, er du klar til å opprette et aktivum.

1. På siden **Alle arbeidssteder** må du kontrollere at arbeidsstedet der du vil at aktivumet skal opprettes automatisk, bruker arbeidsstedstypen du opprettet for dette formålet.
2. Velg arbeidsstedet i listen.
3. Velg **Oppdater tilstand for arbeidssted**, og velg deretter livssyklustilstanden du opprettet for dette formålet. Ett aktivum installeres nå automatisk på arbeidsstedet. Dette aktivumet har samme navn som arbeidsstedet.
