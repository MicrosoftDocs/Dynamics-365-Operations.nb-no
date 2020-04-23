---
title: Type kritisk aktivitet for aktiva
description: Emnet forklarer typer kritsk aktivitet for aktiva i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c6d3742425a3b92282a62c142b9c325e2d7042f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216603"
---
# <a name="asset-criticality-types"></a>Type kritisk aktivitet for aktiva

[!include [banner](../../includes/banner.md)]

 

Emnet forklarer typer kritsk aktivitet for aktiva i Aktivastyring. Kritiske forhold omkring aktiva er knyttet til aktiva og overføres til arbeidsordrer. Dette kan ikke endres på en arbeidsordre. Kritiske forhold omkring aktiva brukes til å beregne arbeidsordrekritikalitet under planlegging av arbeidsordrer. Det brukes med andre ord til å beregne i hvilken grad en vedlikeholdsjobb på et aktivum påvirker produksjonsplanen og produktiviteten i selskapet. Hvis du vil ha mer informasjon om oppsettet som er knyttet til beregning av poengsummer for arbeidsordreplanlegging, kan du se [Parametere i Aktivastyring](../setup-for-objects/enterprise-asset-management-parameters.md).

Hvis du vil definere kritikalitet, må du først opprette kritikalitetstypene som skal brukes i aktivaoppsettet. Deretter konfigurerer du aktivakritikalitetene.

## <a name="set-up-criticality-types"></a>Definere kritikalitetstyper

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Type kritisk aktivitet**.
2. Velg **Ny** for å opprette en oppføring.
3. I **Kritikalitet**-feltet angir du et tall som angir kritikalitet.
4. I **Navn**-feltet angir du et navn på kritikalitetstypen.
5. Angi en faktor i feltet **Faktor**. Denne faktoren brukes under beregning av arbeidsordreplanlegging for å bestemme kritikalitetsposten som skal brukes. (Posten som har den høyeste faktoren er alltid brukt.) Denne innstillingen er relevant hvis, som vist i illustrasjonen nedenfor, det opprettes kritikalitetslinjer som har samme kritikalitetsverdi.

    ![Siden Type kritisk aktivitet](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Definer kritiske forhold omkring aktiva

1. Velg **Aktivastyring** \> **Oppset** \> **Kritiske forhold omkring aktiva**.
2. Velg **Ny** for å opprette en oppføring.
3. Avhengig av det påkrevde nivået for aktivakritikalitet kan du foreta relevante valg i feltene **Arbeidssted**, **Aktivatype**, **Produsent**, **Modell**, **Aktivum**, **Jobbtypekategori**, **Jobbtype**, **Jobbtypevariant** og **Jobbehov**.

    > [!NOTE]
    > Når en aktivumkritikalitet er valgt, gjennomgår Aktivastyring alle aktivakritikalitetsposter for å kontrollere om det finnes et mulig samsvar. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord kontrollerer Aktivastyring først **jobbehovet**. Hvis det ikke blir funnet noen treff, kontrolleres **jobbtypevarianten**. Hvis det ikke blir funnet noen treff, kontrolleres **jobbtypen** og så videre. Som du kan se i oppsettet av siden, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff. Hvis det ikke blir funnet noen treff, brukes "standard"-oppføringen som ikke har noen valg.

4. I **Kritikalitet**-feltet velger du en av de kritikalitetsverdiene du opprettet i forrige fremgangsmåte.

### <a name="notes-about-criticality-setup"></a>Merknader om kritikalitetsoppsett

- Hvis du endrer en aktivumkritikalitet i dette oppsettet etter at du allerede har brukt den på en arbeidsordre, oppdateres ikke kritikaliteten i arbeidsordren i henhold til dette.
- Kritikaliteten i en arbeidsordre beregnes på nytt hver gang en arbeidsordrelinje legges til eller slettes fra arbeidsordren.
- Hvis en arbeidsordre inneholder flere arbeidsordrejobber, brukes alltid den høyeste kritikaliteten i henhold til **Faktor**-feltet på siden **Kritikalitetstyper** i arbeidsordren.
- Vanligvis kan aktivakritikalitet endres over en periode. Kritikalitet kan påvirkes ved kjøp av nytt utstyr, saneringer, og så videre. Vurder å reevaluere aktivakritikalitetene med jevne mellomrom (for eksempel én gang per år eller hvert annet år) for å sikre at kritikalitetsdefinisjonene samsvarer med det gjeldende produksjonsoppsettet.
