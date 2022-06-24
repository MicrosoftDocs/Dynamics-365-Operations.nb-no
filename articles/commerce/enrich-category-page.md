---
title: Supplere en kategorimålside
description: Denne artikkelen dekker supplering av kategorisider i Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bfee3b09768fa19ab95c880d7f7cbf330a8c58d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856970"
---
# <a name="enrich-a-category-landing-page"></a>Supplere en kategorimålside

[!include [banner](includes/banner.md)]

Denne artikkelen dekker supplering av kategorisider i Dynamics 365 Commerce.

Commerce leverer en standard kategorimålside som brukes når kategoridata vises. En standard kategoriside inneholder nødvendige elementer, for eksempel presiseringer, kategoriserte produktplasseringer, sorteringsalternativer, et valgsammendrag og sidenummereringskontroller. 

I stedet for å bruke standard kategoriside kan det imidlertid være lurt å bruke en "supplert" kategorimålside med mer innhold og mer spesifikke elementer. Et typisk supplement kan involvere å legge til kategorispesifikt markedsføringsinnhold på kategorisiden. Dette innholdet kan inkludere produktplassering på tvers av kategorier for kryssalgsformål, redigeringslister, bilder, videoer og annen tekst. Du kan enten endre standard kategoriside eller definere en annen kategoriside for en bestemt kategori.

![Supplere kategorimålside.](./media/CategoryLandingPages.png)

I Commerce-områdebyggeren inneholder siden **Produkter** en liste over kategorier fra kanalen som er tilordnet området. Hvis statusen **Supplert** er valgt for en kategoriside, er denne kategorisiden supplert. Hvis ikke brukes standard kategoriside og -innhold for kategorien. Du kan forhåndsvise både de supplerte og de ikke-supplerte produktsidene for en kategori ved å velge kategorinavnet.

Gjør følgende for å gjøre en kategoriside rikere:

1. På **Produkter**-siden velger du navnet på kategorien som du vil supplere kategorisiden for. Standard kategoriside for den valgte kategorien åpnes i redigeringsprogrammet for sider.
2. Velg **Suppler kategoriside**.
3. Velg en mal for den berikede kategorisiden. Hvis du bare gjør små endringer, kan du velge standard kategoriside. Du kan også velge en bestemt kategorisidemal. Når du velger en mal, åpnes redigeringsprogrammet for side, og den valgte malen brukes til å opprette en ny kategoriside for den valgte kategorien. Siden sjekkes ut til deg, og du kan nå utføre endringene.

> [!NOTE]
> Moduler som bruker kategorispesifikasjonsdata, bruker dataene fra den valgte kategorien. Innstillingene for malen du velger, avgjør hvilke endringer du kan utføre.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en produktside](enrich-product-page.md)

[Kontrollere tilgjengelighet for sideinnhold](verify-accessibility.md)

[Opprette dynamiske e-handelssider basert på URL-parametere](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
