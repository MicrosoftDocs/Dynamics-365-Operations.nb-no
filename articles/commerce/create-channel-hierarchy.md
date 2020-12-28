---
title: Opprette et kanalnavigasjonshierarki
description: Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414540"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Opprette et kanalnavigasjonshierarki


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Et kanalnavigeringshierarki brukes til å gruppere og organisere produkter i kategorier, slik at produktene kan blas gjennom på nettet eller på salgsstedet (POS).

## <a name="create-a-channel-navigation-hierarchy"></a>Opprette et kanalnavigasjonshierarki

Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Produkter og kategorier \> Kanalnavigasjonskategorier**.
1. I handlingsruten velger du **Ny**.
1. I **Navn**-boksen angir du et navn.
1. I **Beskrivelse**-boksen angir du en beskrivelse.
1. Velg **Opprett**.
1. I handlingsruten velger du **Ny kategorinode** for å opprette en rotnode.
1. I **Navn**-boksen angir du et navn.
1. I **Beskrivelse**-boksen angir du en beskrivelse.
1. I **Brukervennlig navn**-boksen angir du et brukervennlig navn.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en rotnode.

![Eksempel på rotnode](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Opprette navigasjonskategorinoder

Hvis du vil opprette eventuelle ekstra navigasjonskategorinoder for å representere produktkategoriene på kanalen, følger du disse trinnene.

1. I navigasjonsruten velger du den overordnede noden du vil legge til en kategori i.
1. I handlingsruten velger du **Ny kategorinode**.
1. I **Navn**-boksen angir du et navn.
1. I **Beskrivelse**-boksen angir du en beskrivelse.
1. I **Brukervennlig navn**-boksen angir du et brukervennlig navn.
1. I **Visningsrekkefølge**-boksen angir du en visningsrekkefølge (valgfritt).
1. Velg **Lagre** i handlingsruten.

Følgende bilde viser et eksempel på et fullført kanalnavigasjonshierarki.

![Eksempel på kanalhierarki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Legge til produkter i kategorinoder

Hvis du vil legge til produkter i kategorinoder, følger du disse trinnene.

1. Velg en kategorinode.
1. Under **Produkter** velger du **Legg til**.
1. Finn det nye produktet / de nye produktene du vil legge til, ved hjelp av produktnummer eller produktnavn, og velg deretter **OK**.
1. Velg **Lagre** i handlingsruten.

> [!NOTE]
> Tilføying av produkter i en node i kanalnavigasjonshierarkiet er ikke tilstrekkelig for produktene som vises på en valgt kanal. Produktene må også være sortert til et produkt.

Det følgende bildet viser en eksempelnode med produkter lagt til.

![Produkter lagt til i en kategorinode](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Legge til produktattributtgrupper i kategorinoder

> [!NOTE]
> Attributtgrupper må opprettes før du kan legge dem til i en node i kanalnavigasjonshierarkiet.

Hvis du vil legge til en attributtgruppe i en kategorinode, følger du disse trinnene.

1. Velg en kategorinode.
1. Under **Produktattributtgruppe** velger du **Legg til**.
1. Finn attributtgruppen(e) du vil legge til, og velg deretter **OK**.
1. Velg **Lagre** i handlingsruten.

Det følgende bildet viser en eksempelnode med produktattributtgrupper lagt til.

![Produktattributtgrupper i en node](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Definere sortimenter](set-up-assortments.md)

[Administrere attributter og attributtgrupper](attribute-attributegroups-lifecycle.md)
