---
title: Supplere en produktside
description: Denne artikkelen beskriver hvordan du supplerer en produktside i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f01dcc2518fe861339b4984522582ed3de7aa6ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282141"
---
# <a name="enrich-a-product-page"></a>Supplere en produktside

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du supplerer en produktside i Microsoft Dynamics 365 Commerce.

Som standard bruker webområdet en generell side til å vise produktdata. Denne siden inneholder grunnleggende informasjon om produktet og kontrollene som kreves for å selge den. Du kan imidlertid supplere informasjonen som kommer fra Commerce Scale Unit, med tilleggsbilder eller -tekst for et bestemt produkt. Denne prosessen kalles å supplere produktsiden.

I mange tilfeller vil du ha bruk for et bestemt tilleggsinnhold for produktene. Når du går til **Detaljhandel og handel** i redigeringsverktøyet, vil du se en liste over produkter fra kanalen som er tilordnet området. I denne listen viser kolonnen for **Supplert** om produktsiden for et produkt er supplert. Hvis det vises et merke i kolonnen, finnes det en supplert produktside for produktet. Hvis det ikke vises noen avmerking, brukes standard produktside og -innhold for produktet. Du kan forhåndsvise både supplerte og ikke-supplerte produktsider ved å velge et produktnavn fra listen.

## <a name="enrich-a-product-page"></a>Supplere en produktside

Følg denne fremgangsmåten for å supplere en produktside.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Produkter** i navigasjonsruten til venstre.
1. Velg et hvilket som helst produkt som ikke har en supplert produktside.
1. Klikk på **Suppler produktside** i handlingsruten.
1. Velg **PDP-mal**, og velg deretter **OK**.
1. Utvid **Hoved**-sporet i sidedisposisjonstreet til venstre.
1. Velg ellipseknappen (**...**) for **Hoved**-sporet, og velg deretter **Legg til modul**.
1. Velg **Container 2**, og velg deretter **OK**.
1. Velg ellipseknappen for **Container 2**, og velg deretter **Legg til modul**.
1. Velg **Funksjon**, og velg deretter **OK**.
1. I egenskapsruten til høyre, i feltet **Rik tekst**, angir du oppdatert beskrivelse for produktet.
1. I feltet **Overskrift** angir du overskriftstekst, og deretter velger du **OK**.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. I feltet **Kommentarer** angir du **Supplerte et produkt**, og deretter velger du **OK**.
1. Velg **Forhåndsvisning** for å forhåndsvise den supplerte produktsiden. Når du er ferdig, lukker du forhåndsvisningskategorien for å gå tilbake til redigeringsverktøyet.
1. Velg **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

[Kontrollere tilgjengelighet for sideinnhold](verify-accessibility.md)

[Opprette dynamiske e-handelssider basert på URL-parametere](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
