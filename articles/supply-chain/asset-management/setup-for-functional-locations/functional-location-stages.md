---
title: Livsløpstilstander for arbeidssted
description: Dette emnet beskriver hvordan du konfigurerer tilstander for arbeidssteder og livsløpsmodeller i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eedc21dde32671b4f5539ac4e798a8e1329c191
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434707"
---
# <a name="functional-location-lifecycle-states"></a>Livsløpstilstander for arbeidssted

[!include [banner](../../includes/banner.md)]

 

Dette emnet beskriver hvordan du konfigurerer livsløpstilstander for arbeidssteder og livsløpsmodeller i Aktivastyring. Livsløpstilstander for arbeidssteder definerer tilstandene som et arbeidssted kan gå gjennom, for eksempel opprettet, aktivt og avsluttet. Du kan vise alle arbeidssteder, uavhengig av livsløpstilstanden, på listesiden **Alle arbeidssteder**. Du kan endre statusen for et arbeidssted ved å velge det på listesiden **Alle arbeidssteder** og velge **Oppdater arbeidsstedstilstand**.

## <a name="set-up-functional-location-lifecycle-states"></a>Definer livsløpstilstander for arbeidssted

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Livsløpstilstander**.
2. Velg **Ny** for å opprette en ny arbeidsstedstilstand.
3. Sett inn tilstands-ID-en i feltet **Livsløpstilstand** og et navn på arbeidsstedstilstanden i **Navn**-feltet. I feltet **Livsløpsmodeller** kan du se antallet livsløpsmodeller for arbeidssted som bruker arbeidsstedstilstanden.
4. I hurtigfanen **Generelt** velger du "Ja" på veksleknappen **Aktiv** hvis arbeidsstedet skal være aktivt i denne fasen.
5. Velg "Ja" på veksleknappen **Opprett aktiva** hvis det skal være mulig å opprette et aktivum automatisk med samme navn som den arbeidsstedet og installere det på arbeidsstedet i denne tilstanden.  
>[!NOTE]
>Denne veksleknappen er relatert til **Aktivatype**-feltet på hurtigfanen **Generelt** i skjemaet **Arbeidsstedstyper** (**Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Arbeidsstedstyper**).
6. Velg "Ja" på veksleknappen **Endre navn på sted** hvis det skal være mulig å endre navnet på arbeidsstedet i denne tilstanden.
7. Velg "Ja" på veksleknappen **Nye underordnede steder** hvis det skal være mulig å legge til nye underordnede steder på arbeidsstedet i denne tilstanden.
8. Velg "Ja" på veksleknappen **Installer aktiva** hvis det skal være mulig å installere aktiva på arbeidsstedet i denne tilstanden.
9. Velg "Ja" på veksleknappen **Slett arbeidssted** hvis det skal være mulig å slette arbeidsstedet i denne tilstanden.
10. Velg en aktivatilstand i feltet **Livsløpstilstand** hvis du vil at livsløpstilstanden for alle aktiva som er installert på arbeidsstedet, skal oppdateres automatisk i denne tilstanden. Eksempel: Hvis du lukker et arbeidssted og setter livsløpstilstanden for arbeidsstedet til "Avsluttet", vil du kanskje automatisk endre livsløpstilstanden for aktivaene som er installert på arbeidsstedet, til "Ikke i bruk".


>[!NOTE]
>Livsløpstilstander for arbeidssted, livsløpsmodeller og typer er relatert og brukt på samme måte som livsløpstilstander og livsløpsmodeller for arbeidsordrer og arbeidsordretyper. 

## <a name="set-up-functional-location-lifecycle-models"></a>Definer livsløpsmodeller for arbeidssted

Når du har opprettet livsløpstilstandene som kreves for arbeidsstedene, kan de deles inn i grupper. Dette gjøres for å opprette livsløpsmodellflyten som kan brukes for ulike typer arbeidssteder. Som et minimum bør en standard livsløpsmodell for arbeidssteder opprettes.

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Livsløpsmodeller**.
2. Velg **Ny** for å opprette en ny livsløpsmodell.
3. Sett inn livsløpsmodell-ID-en i feltet **Livsløpsmodell** og et navn på livsløpsmodellen i **Navn**-feltet. I feltene **Arbeidsstedstyper** og **Livsløpstilstander** kan du se antallet arbeidsstedstyper som bruker livsløpsmodellen og antallet tilstander som er valgt i livsløpsmodellen.
4. I hurtigfanen **Livsløpstilstander** velger du tilstandene som skal inkluderes i modellen. Denne gjøres ved å klikke på en tilstand i delen **Gjenværende livsløpstilstander** og klikke på ![fremoverpilen](media/02-setup-for-functional-locations.png).
5. Hvis du vil velge alle tilgjengelige tilstander for en modell, klikker du knappen for å ![velge alle tilgjengelige tilstander](media/03-setup-for-functional-locations.png). Alle tilstdnder overføres til delen **Valgte livsløpstilstander**.
6. Hvis du vil fjerne en valgt tilstand fra modellen, velger du tilstanden i delen **Valgte livsløpstilstander**, og deretter velger du ![tilbakepilen](media/04-setup-for-functional-locations.png).
7. Velg **Oppdateringer av livsløpstilstander** for å definere hvilke livsløpstilstander som kan følge en valgt tilstand.
