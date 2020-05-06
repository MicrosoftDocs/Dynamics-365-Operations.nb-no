---
title: Integrere aktivabehandling med anleggsmidler
description: Dette emnet beskriver hvordan du integrerer Aktivastyring- og Anleggsmiddel-modulene, slik at du kan knytte anleggsmidler til vedlikeholdsgjenstander.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276949"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Integrere aktivabehandling med anleggsmidler

[!include [banner](../../includes/banner.md)]

Ved å integrere moduelene **Aktivastyring** og **Anleggsmiddel** kan du knytte anleggsmidler til vedlikeholdsgjenstander. Anleggsmidler-brukere kan deretter opprette en vedlikeholdsgjenstand fra et nytt eller eksisterende anleggsmiddel, og brukere av Aktivastyring kan knytte en vedlikeholdsgjenstand til et eksisterende anleggsmiddel. Denne funksjonen gjør det også enkelt for anleggsmiddel-brukere å vise kostnadene som ble bokført fra arbeidsordrer for relaterte vedlikeholdsgjenstander.

> [!NOTE]
> I dette emnet refererer *vedlikeholdsgjenstander* til anleggsmidler fra **Aktivastyring**-modulen, og *anleggsmidler* refererer til anleggsmidler fra **Anleggsmidler**-modulen.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Angi en standardlokasjon for nye vedlikeholdsgjenstander som opprettes fra anleggsmidler (valgfritt)

Denne valgfrie konfiguasjonen gjør det mulig å angi et arbeidssted for nye vedlikeholdsgjenstander som opprettes fra anleggsmidler. Du fullfører vanligvis denne konfigurasjonen bare én gang, hvis du fullfører den i det hele tatt.

Følg fremgangsmåten nedenfor for å fullføre konfigurasjonen.

1. Gå til **Aktivastyring \> Oppsett \> Aktivabehandlingsparametere**.
1. Velg standardstedet i kategorien **Anleggsmidler**, i **Arbeidssted**-feltet.
1. Velg **Lagre** i handlingsruten.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Arbeide med integrerte vedlikeholdseiendeler og anleggsmidler

Denne delen inneholder en samling prosedyrer som viser ulike måter du kan arbeide med funksjonene for integrert aktivakontroll og anleggsmidler på.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Knytte en eksisterende vedlikeholdsgjenstand til et anleggsmiddel

Gjør følgende for å knytte en eksisterende vedlikeholdsgjenstand til et anleggsmiddel.

1. Gå til **Aktivastyring \> Aktiva \> Alle aktiva** (eller **Aktive aktiva**).
1. Velg et aktivum.
1. Velg et eksisterende anleggsmiddel i hurtigfanen **Anleggsmiddel** i feltet **Anleggsmiddelnummer**.
1. Velg **Lagre** i handlingsruten.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Vis anleggsmidlet som er knyttet til en valgt vedlikeholdsgjenstand

Gjør følgende for å vise anleggsmidlet som er knyttet til en valgt vedlikeholdsgjenstand.

1. Gå til **Aktivastyring \> Aktiva \> Alle aktiva** (eller **Aktive aktiva**).
1. Velg et aktivum.
1. Velg koblingen i hurtigfanen **Anleggsmiddel** i feltet **Anleggsmiddelnummer**.

    **Anleggsmidler**-siden for valgt aktiva åpnes. (Denne siden blir vanligvis funnet under **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Vise vedlikeholdsgjenstanden som er knyttet til et valgt anleggsmiddel

Gjør følgende for å vise vedlikeholdsgjenstanden som er knyttet til et valgt anleggsmiddel.

1. Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
1. Velg et aktivum.
1. På handlingsruten, i kategorien **Aktivastyring** i **Vis**-gruppen, velger du **Vedlikeholdsgjenstand**.

    **Vedlikeholdsgjenstand**-siden for aktivaet som er knyttet til det valgte anleggsmidlet, åpnes. (Denne siden finnes vanligvis under **Aktivastyring \> Anleggsmidler \> Alle anleggsmidler**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Vise vedlikeholdskostnader som er knyttet til et anleggsmiddel

Arbeidsordrer for aktivakontroll kan posteres for vedlikeholdsgjenstander, og hver arbeidsordre har vanligvis en pris. Når et anleggsmiddel er knyttet til en vedlikeholdsgjenstand, kan du gå direkte fra anleggsmiddelet for å vise de tilknyttede kostnadene.

Gjør følgende for å vise vedlikeholdskostnadene som er knyttet til et valgt anleggsmiddel.

1. Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
1. Velg et aktivum.
1. På handlingsruten, i kategorien **Aktivastyring** i **Vis**-gruppen, velger du **Vedlikeholdskostnad**.

    Siden **Vedlikeholdskostnad** åpnes, og viser de tilknyttede kostnadene.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Opprette en ny vedlikeholdsgjenstand for et eksisterende anleggsmiddel

Gjør følgende for å opprette en ny vedlikeholdsgjenstand for et eksisterende anleggsmiddel.

1. Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
1. Velg et aktivum.
1. På handlingsruten, i kategorien **Aktivastyring** i **Ny**-gruppen, velger du **Opprett vedlikeholdsgjenstand**. (Hvis dette alternativet ikke er tilgjengelig, kan det hende at et vedlikeholdsgjenstanden allerede er knyttet til det valgte anleggsmidlet.)
1. Fullfør opprettelsen av aktivumet som beskrevet i [Opprette et aktiva](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Opprette et nytt anleggsmiddel og legge til en ny vedlikeholdsgjenstand for det

Gjør følgende for å opprette et nytt anleggsmiddel og legge til en ny vedlikeholdsgjenstand for det.

1. Gå til **Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
1. Velg **Ny** i handlingsruten.
1. Fullfør opprettelsen av anleggsmidlet som beskrevet i [Opprette et anleggsmiddel](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. På handlingsruten, i kategorien **Aktivastyring** i **Ny**-gruppen, velger du **Opprett vedlikeholdsgjenstand**.
1. Fullfør opprettelsen av aktivumet som beskrevet i [Opprette et aktiva](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Fjerne tilknytningen mellom to anleggsmidler

I noen tilfeller kan det hende at du må fjerne tilknytningen for en vedlikeholdsgjenstand til anleggsmidlet. Hvis du for eksempel vil [opprette en ny vedlikeholdsgjenstand](#new-maintenance-from-fixed) fra et anleggsmiddel, må du først fjerne en eventuell eksisterende tilknytning.

Gjør følgende for å fjerne en tilknytning mellom en vedlikeholdsgjenstand og et anleggsmiddel.

1. Gå til **Aktivastyring \> Aktiva \> Alle aktiva** (eller **Aktive aktiva**).
1. Finn og åpne anleggsmidlet.
1. I hurtigfanen **Anleggsmiddel** fjerner du verdien fra **Arbeidssted**-feltet.
1. Velg **Lagre** i handlingsruten.
