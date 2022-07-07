---
title: Installere aktiva på funksjonslokasjoner
description: Denne artikkelen forklarer hvordan du installerer aktiva på funksjonslokasjoner i Aktivastyring.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ae571f4ad7210b31d212b0472610b36dc5c488b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016079"
---
# <a name="install-assets-on-functional-locations"></a>Installere aktiva på funksjonslokasjoner

[!include [banner](../../includes/banner.md)]

 

Når du har opprettet funksjonslokasjonsstrukturer, er neste trinn å installere aktiva på de relevante funksjonslokasjonene. Denne artikkelen forklarer hvordan du installerer aktiva på disse funksjonslokasjonene i Aktivastyring. Se [Introduksjon til aktiva](../objects/introduction-to-objects.md) hvis du vil ha mer informasjon om hvordan du oppretter aktiva.

Hvis du har opprettet en aktivastruktur, må hele aktivastrukturen være installert på en funksjonslokasjon. Derfor kan bare overordnede objekter (aktiva på øverste nivå som har ingen overordnede objekter) velges på en funksjonslokasjon. Alle tilknyttede underordnede aktiva (underaktiva) vil også bli installert på funksjonslokasjonen. Når du installerer aktiva på en funksjonslokasjon, kan finansdimensjonene for funksjonslokasjonen automatisk overføres til dem, avhengig av oppsettet for funksjonslokasjonstypen som er valgt for funksjonslokasjonen. Hvis du vil ha mer informasjon om hvordan du oppretter funksjonslokasjonstyper, se [Funksjonslokasjonstyper](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Du kan definere aktivatyper på funksjonslokasjonstypen som brukes for en funksjonslokasjon. I dette tilfellet, når du installerer aktiva på funksjonslokasjonen, vises bare overordnede objekter som har samme aktivatype i listen over aktiva som kan installeres på funksjonslokasjonen.

Når du har installert aktiva på en funksjonslokasjon, kan du erstatte et overordnet objekt eller en aktivastruktur etter behov. Når du installerer aktiva, velger du et overordnet objekt som skal erstattes. Alle relaterte underordnede aktiva vil også bli erstattet. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Installere en aktivastruktur på en funksjonslokasjon

1. Velg **Aktivastyring** \> **Funksjonslokasjoner** \> **Alle funksjonslokasjoner** eller **Aktive funksjonslokasjoner**.
2. Velg funksjonslokasjonen der det skal installeres et aktivum.
3. Velg **Installer aktivum**.

    **Attributter**-delen viser en liste over kravene til aktivaattributtet som er definert på funksjonslokasjonstypen som er valgt for funksjonslokasjonen. Attributtene er bare beregnet til informasjon. Systemet validerer ikke attributtene mot aktivaattributtene som er definert på aktivumet som du installerer. Du må gjøre denne valideringen når du velger et aktivum i **Aktiva**-feltet.

4. I **Aktiva**-feltet velger du det overordnede aktivumet som skal installeres. Alle relaterte underordnede aktiva inkluderes automatisk i installasjonen.

    Delen **Aktivaattributter** til høyre for listen over aktiva viser aktivaattributtene som er knyttet til det valgte aktivumet.

5. I **Gyldighet**-feltet velger du datoen og klokkeslettet da aktivainstallasjonen er gyldig fra. Etter dette tidspunktet vil kostnader for aktivumet og relaterte underaktiva være knyttet til funksjonslokasjonen.

    > [!NOTE]
    > Aktivaattributtene som er definert på aktivumet, legges til i **Attributter**-delen. Kravet til **Vekt**-attributtet er for eksempel lagt til som et krav på både aktivumet og funksjonslokasjonen. Hvis aktivumet har attributtkrav av samme type som funksjonslokasjonen, angis verdiene for aktivumets attributtkrav i **Verdi**-feltene. Derfor kan du validere aktivaverdiene mot attributtkravene som er definert på funksjonslokasjonen. Attributtkravene som er definert på funksjonslokasjonen, er merket med en hake.

6. Velg **OK**.

    > [!NOTE]
    > Hvis du vil endre installasjonen av et aktivum ved å installere det på en ny funksjonslokasjon, følger du trinn 1 til 6 i denne fremgangsmåten. Når du installerer et aktivum på en ny funksjonslokasjon, avinstalleres aktivumet automatisk fra den forrige funksjonslokasjonen. Alle aktive meldinger eller arbeidsordrer som ble opprettet på aktivumet før du installerte det på en ny funksjonslokasjon, overføres **ikke** automatisk til den nye funksjonslokasjonen. Hvis disse meldingene og arbeidsordrene fortsatt er nødvendige for aktivumet, må du opprette dem på nytt manuelt etter at aktivumet er installert på den nye lokasjonen.

7. Hvis du vil vise en liste over alle aktivaene, inkludert underaktiva, som er installert på funksjonslokasjonen, velger du funksjonslokasjonen på siden **Alle funksjonslokasjoner** og velger deretter **Aktiva**.
8. Hvis du vil vise en liste over aktive meldinger, aktive arbeidsordrer eller feilregistreringer som er knyttet til aktivaene som er installert på en funksjonslokasjon, velger du funksjonslokasjonen på siden **Alle funksjonslokasjoner**, og deretter velger du **Forespørsler**, **Arbeidsordrer** eller **Feil**.

> [!NOTE]
> Når aktivarelaterte data endres, oppdateres de automatisk på funksjonslokasjonen som aktivumet er installert på. Denne automatiske oppdateringen gjelder endringer i meldinger, arbeidsordrer, registreringer av feil på aktiva, registreringer av vedlikeholdsavbrudd og aktivamålregistreringer.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Opprette ett aktivum automatisk på en funksjonslokasjon

Du kan definere funksjonslokasjonsfaser og funksjonslokasjonstyper for å håndtere automatisk opprettelse av *ett* aktivum på en funksjonslokasjon. Aktivumet får samme ID og navn som funksjonslokasjonen. Denne funksjonaliteten kan være nyttig når du håndterer vedlikehold på et stort statisk aktivum, for eksempel en bygning.

Før du kan opprette et aktivum automatisk på en funksjonslokasjon, må følgende oppsettsdata være tilgjengelige:

- Opprett en funksjonslokasjonstype for å håndtere automatisk opprettelse av et aktivum. I **Aktivatype**-feltet velger du en aktivatype. Hvis du vil har mer informasjon, kan du se [Funksjonslokasjonstyper](../setup-for-functional-locations/functional-location-types.md).
- Opprett en livssyklustilstand for funksjonslokasjon for å håndtere automatisk opprettelse av et aktivum. Sett alternativet **Opprett aktivum** til **Ja**. Hvis du vil har mer informasjon, kan du se [Livssyklustilstander for funksjonslokasjoner](../setup-for-functional-locations/functional-location-stages.md).

Når oppsettsdataene er tilgjengelige, er du klar til å opprette et aktivum.

1. På siden **Alle funksjonslokasjoner** må du kontrollere at funksjonslokasjonen der du vil at aktivumet skal opprettes automatisk, bruker funksjonslokasjonstypen du opprettet for dette formålet.
2. Velg funksjonslokasjonen i listen.
3. Velg **Oppdater tilstand for funksjonslokasjon**, og velg deretter livssyklustilstanden du opprettet for dette formålet. Ett aktivum installeres nå automatisk på funksjonslokasjonen. Dette aktivumet har samme navn som funksjonslokasjonen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]