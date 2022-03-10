---
title: Livssyklustilstander for arbeidssted
description: Dette emnet beskriver hvordan du konfigurerer tilstander for arbeidssteder og livssyklusmodeller i Aktivastyring.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a9893ad497bbe442d74f5212153fa466d2c85eb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360976"
---
# <a name="functional-location-lifecycle-states"></a>Livssyklustilstander for arbeidssted

[!include [banner](../../includes/banner.md)]

 

Dette emnet beskriver hvordan du konfigurerer livssyklustilstander for arbeidssteder og livssyklusmodeller i Aktivastyring. Livssyklustilstander for arbeidssteder definerer tilstandene som et arbeidssted kan gå gjennom, for eksempel opprettet, aktivt og avsluttet. Du kan vise alle arbeidssteder, uavhengig av livssyklustilstanden, på listesiden **Alle arbeidssteder**. Du kan endre statusen for et arbeidssted ved å velge det på listesiden **Alle arbeidssteder** og velge **Oppdater arbeidsstedstilstand**.

## <a name="set-up-functional-location-lifecycle-states"></a>Definer livssyklustilstander for arbeidssted

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Livssyklustilstander**.
2. Velg **Ny** for å opprette en ny arbeidsstedstilstand.
3. Sett inn tilstands-ID-en i feltet **Livssyklustilstand** og et navn på arbeidsstedstilstanden i **Navn**-feltet. I feltet **Livssyklusmodeller** kan du se antallet livssyklusmodeller for arbeidssted som bruker arbeidsstedstilstanden.
4. I hurtigfanen **Generelt** velger du "Ja" på veksleknappen **Aktiv** hvis arbeidsstedet skal være aktivt i denne fasen.
5. Velg "Ja" på veksleknappen **Opprett aktiva** hvis det skal være mulig å opprette et aktivum automatisk med samme navn som den arbeidsstedet og installere det på arbeidsstedet i denne tilstanden.  
>[!NOTE]
>Denne veksleknappen er relatert til **Aktivatype**-feltet på hurtigfanen **Generelt** i skjemaet **Arbeidsstedstyper** (**Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Arbeidsstedstyper**).
6. Velg "Ja" på veksleknappen **Endre navn på sted** hvis det skal være mulig å endre navnet på arbeidsstedet i denne tilstanden.
7. Velg "Ja" på veksleknappen **Nye underordnede steder** hvis det skal være mulig å legge til nye underordnede steder på arbeidsstedet i denne tilstanden.
8. Velg "Ja" på veksleknappen **Installer aktiva** hvis det skal være mulig å installere aktiva på arbeidsstedet i denne tilstanden.
9. Velg "Ja" på veksleknappen **Slett arbeidssted** hvis det skal være mulig å slette arbeidsstedet i denne tilstanden.
10. Velg en aktivatilstand i feltet **Livssyklustilstand** hvis du vil at livssyklustilstanden for alle aktiva som er installert på arbeidsstedet, skal oppdateres automatisk i denne tilstanden. Eksempel: Hvis du lukker et arbeidssted og setter livssyklustilstanden for arbeidsstedet til "Avsluttet", vil du kanskje automatisk endre livssyklustilstanden for aktivaene som er installert på arbeidsstedet, til "Ikke i bruk".


>[!NOTE]
>Livssyklustilstander for arbeidssted, livssyklusmodeller og typer er relatert og brukt på samme måte som livssyklustilstander og livssyklusmodeller for arbeidsordrer og arbeidsordretyper. 

## <a name="set-up-functional-location-lifecycle-models"></a>Definer livssyklusmodeller for arbeidssted

Når du har opprettet livssyklustilstandene som kreves for arbeidsstedene, kan de deles inn i grupper. Dette gjøres for å opprette livssyklusmodellflyten som kan brukes for ulike typer arbeidssteder. Som et minimum bør en standard livssyklusmodell for arbeidssteder opprettes.

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Livssyklusmodeller**.
2. Velg **Ny** for å opprette en ny livssyklusmodell.
3. Sett inn livssyklusmodell-ID-en i feltet **Livssyklusmodell** og et navn på livssyklusmodellen i **Navn**-feltet. I feltene **Arbeidsstedstyper** og **Livssyklustilstander** kan du se antallet arbeidsstedstyper som bruker livssyklusmodellen og antallet tilstander som er valgt i livssyklusmodellen.
4. I hurtigfanen **Livssyklustilstander** velger du tilstandene som skal inkluderes i modellen. Denne gjøres ved å klikke på en tilstand i delen **Gjenværende livssyklustilstander** og klikke på ![fremoverpilen](media/02-setup-for-functional-locations.png) knapp.
5. Hvis du vil velge alle tilgjengelige tilstander for en modell, klikker du knappen for å ![velge alle tilgjengelige tilstander](media/03-setup-for-functional-locations.png) . Alle tilstdnder overføres til delen **Valgte livssyklustilstander**.
6. Hvis du vil fjerne en valgt tilstand fra modellen, velger du tilstanden i delen **Valgte livssyklustilstander**, og deretter velger du ![tilbakepilen.](media/04-setup-for-functional-locations.png) knapp.
7. Velg **Oppdateringer av livssyklustilstander** for å definere hvilke livssyklustilstander som kan følge en valgt tilstand.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]