---
title: Opprette en prosessmal i Attract
description: Dette emnet gir informasjon om hvordan du oppretter en prosessmal i Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 533b9abd3d57c5bf8f3d9da85020c86012436f2f
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622724"
---
# <a name="create-a-process-template-in-attract"></a>Opprette en prosessmal i Attract

[!include [banner](includes/banner.md)]

En *mal for ansettelsesprosess* inneholder alle aktivitetene som bør tas med som en del av ansettelsesprosessen for en jobb. Dette emnet beskriver elementene i en prosessmal i Microsoft Dynamics 365 Talent: Attract. Det forklarer også hvordan du oppretter en mal.

> [!NOTE]
> Maloppretting av er en del av tillegget for omfattende ansettelse for Attract.

## <a name="template-management"></a>Malbehandling

Organisasjoner kan bestemme om gruppemedlemmer eller bare administratorer kan opprette prosessmaler i Attract. Hvis du vil konfigurere malbehandling, kan du gå til **Administrasjonssenter** \> **Malbehandling**. Hvis du vil at gruppemedlemmer skal opprette sine egne maler, kan du aktivere malbehandling. Hvis du ikke aktiverer malbehandling, kan bare administratorer opprette maler.

## <a name="default-template"></a>Standardmal

Bare administratorer kan angi standardmalen. Standardmalen blir brukt hvis det ikke er valgt en mal når det opprettes en jobb. For å angi standardmalen kan du gå til **Administrasjonssenter** \> **Malbehandling**. På kortet for malen som skal være standardmalen, velg ellipseknappen (**...**), og velg deretter **Bruk som standard**.

## <a name="create-a-process-template"></a>Opprette en prosessmal

Administratorer, rekrutterere og ansettelsesansvarlige kan opprette prosessmaler. En prosessmal består av *stadier* og *aktiviteter*. Stadier gruppere sammen én eller flere aktiviteter. Som standard har hver prosessmal kundeemne-, søknads- og tilbudsaktiviteter. Stadiene som inneholder disse aktivitetene, kan gis nytt navn. Du kan legge til flere faser ved å velge **+ Nytt stadium**. Aktiviteter kan legges til et stadium ved å dra dem til det aktuelle stadiet, eller ved å dobbeltklikke dem i aktivitetslisten.

> [!NOTE]
> Navn på stadium er synlig for kandidater på siden **Søknadsstatus**. Dette bør du tenke over når du velger navn for stadier.

Hvis du vil ha mer informasjon om aktiviteter, kan du se [Aktiviteter i ansettelsesprosess i Attract](./activities-attract.md).

Følg denne fremgangsmåten for å opprette en mal for ansettelsesprosess.

1. Gå til **Maler**.
2. Velg **Ny**.
3. I feltet **Malnavn** angir du et navn for malen, og deretter velger du **Opprett**.
4. I listen **Velg godkjenningsprosessen** velger du **Standard** for å kreve godkjenning for en jobb.
5. Velg for å aktivere eller deaktivere kundeemner.
6. Valgfritt: Legge til eller fjerne stadier.

    - Hvis du vil legge til et stadium, kan du velge **+ Nytt stadium**.
    - Hvis du vil fjerne et stadium, hold pekeren over det stadiet, og velg deretter papirkurv-knappen som vises.

        > [!NOTE]
        > Stadiene kundemne, søknad og tilbud kan ikke fjernes, men kan gis nytt navn.

7. Valgfritt: Legge til eller fjerne aktiviteter.

    - Hvis du vil legge til en aktivitet, drar du den fra aktivitetslisten til høyre til det aktuelle stadiet. Du kan også dobbeltklikke aktiviteten, og deretter velge stadiet du vil legge den til.
    - Hvis du vil fjerne en aktivitet, utvider du den og velger deretter papirkurv-knappen på overskriften for aktiviteten.

8. Velg **Lagre**.
