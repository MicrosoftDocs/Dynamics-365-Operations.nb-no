---
title: Legg til en ny områdeside
description: Dette emnet beskriver hvordan du legger til en ny områdeside i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797557"
---
# <a name="add-a-new-site-page"></a>Legg til en ny områdeside

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en ny områdeside i Microsoft Dynamics 365 Commerce.

Når du har opprettet maler og fragmenter for området, er neste trinn å begynne å opprette sider som bruker dem. For å komme i gang må du velge en mal eller et oppsett, et sidenavn og en side-URL-adresse.

## <a name="template-or-layout"></a>Mal eller oppsett

Du kan enten bruke en mal eller et oppsett for den nye siden. For mer informasjon, se [Oversikt over maler og oppsett](templates-layouts-overview.md).

## <a name="page-name"></a>Sidenavn

Sidenavnet må være unikt for siden. Det bør være beskrivende, slik at du enkelt kan finne det, og andre personer vet hva siden er ment for. Velg sidenavnet nøye, fordi det ikke kan endres senere.

## <a name="page-url"></a>URL-adresse for side

Du kan velge å angi en URL-adresse til den nye siden. Når du oppretter en side, kan du angi en streng som skal brukes til å opprette en fullstendig URL-adresse. Denne strengen kalles en relativ URL-adresse eller en URL-plassholder. En fullstendig URL-adresse genereres deretter på grunnlag av URL-plassholderen, og den nye siden tilordnes. Du kan endre URL-plassholderen senere, før du publiserer siden. Hvis du vil ha mer informasjon, kan du se [Opprette en URL-adresse for side](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce kobler fra URL-adresser og innhold. Du kan med andre ord opprette en side som ikke er tilknyttet en URL-adresse, og det kan opprettes en URL-adresse som ikke er tilknyttet en side. Innholdsbytting kan derfor utføres for en URL-adresse og krever ikke nedetid, og omadresseringer er enklere å administrere.

## <a name="add-a-new-page"></a>Legge til en ny side

Følg denne fremgangsmåten for å legge til en ny områdeside på området.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Ny side**.
1. I dialogboksen **Ny side** velger du malen og deretter **OK**.
1. I feltet **Sidenavn** angir du et sidenavn (for eksempel **Min nye side**).
1. I feltet **URL** angir du en streng (URL-plassholder) for å fullføre URL-adressen (for eksempel **minnyeside**).
1. Velg **OK**. Redigeringsprogrammet for side vises. Legg merke til at det automatisk blir lagt til et topptekst og en bunntekst på siden basert på malen du har valgt.
1. På sideoppsettet velger du sporet for **Hoved**, velger ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. Velg **Container**, og velg deretter **OK**.
1. Velg **Flytende container**, velg ellipseknappen, og velg deretter **Legg til modul**.
1. Velg **Innholdsrik blokk**, og velg dereter **OK**.
1. Velg **Innholdsrik blokk**, velg ellipseknappen, og velg deretter **Legg til modul**.
1. Velg **Innholdsrikt blokkelement**, og velg dereter **OK**.
1. I avsnittsruten til høyre velger du **Avsnitt**, og deretter, i feltet, angir du **Min testtekst**.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. I feltet **Kommentarer** angr du **La til nye side**, og deretter velger du **OK**.
1. Velg **Forhåndsvisning** for å forhåndsvise siden. Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.
1. Velg **Publiser**.
1. I navigasjonsbanen (søkebaner) velger du **Fabrikam** (eller navnet på området).
1. Velg **URL-adresser** i navigasjonsruten til venstre.
1. Finn og velg URL-adresse (**minnyeside**) i listen.
1. Velg **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en produktside](enrich-product-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

[Kontrollere tilgjengelighet for sideinnhold](verify-accessibility.md)

[Opprette dynamiske e-handelssider basert på URL-parametere](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
