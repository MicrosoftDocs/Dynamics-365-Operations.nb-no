---
title: Tekniske firmaer og dataeierskapsregler
description: Dette emnet beskriver hvordan du kan bruke ett eller flere tekniske firmaer for å sikre at hoveddataene for produkter er sentralt opprettet og vedlikeholdt. Et teknisk firma representerer firmaet som eier de tekniske produktene og de teknisk relevante dataene.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5cab02600e13a1a539b5ae0cd3ff66960430e826
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434856"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Tekniske firmaer og dataeierskapsregler

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Tekniske firmaer og driftsfirmaer

Du kan bruke ett eller flere *tekniske firmaer* for å sikre at hoveddataene for produkter er sentralt opprettet og vedlikeholdt. Et teknisk firma eier de tekniske produktene og de teknisk relevante dataene. Det er alltid koblet til (basert på) en eksisterende *juridisk enhet*, som også er et firma. Ved hjelp av denne tilkoblingen oppretter systemet et sentralt inngangspunkt for alle teknisk relevante data for tekniske produkter i det tekniske firmaet. I dette sentrale inngangspunktet opprettes tekniske produkter, og teknisk relevante data opprettholdes. Fra den vil tekniske produkter og teknisk relevante data bli frigitt til *driftsfirmaer*, som er andre juridiske enheter. (Hvis du vil ha mer informasjon om frigivelsesbehandling, kan du se [Frigi produktstrukturer](release-product-structure.md).) Disse driftsfirmaene vil bruke de tekniske dataene slik de er utformet av det tekniske firmaet. Alle logistikkdata vedlikeholdes lokalt av hvert tekniske firma og driftsfirma.

Hvis du vil opprette et teknisk firma, går du til **Behandling av teknisk endring \> Oppsett \> Tekniske organisasjoner**. Velg **Ny**, angi et navn på det tekniske firmaet, og velg det eksisterende firmaet (juridisk enhet) det er basert på.

Hvis du skal integrere med eksterne systemer for produktlivssyklus (PLM), må du opprette en forretningsenhet (en type firma) som skal bli et eksternt firma.

## <a name="engineering-product-categories-and-engineering-companies"></a>Kateogirer for teknisk produkt kategorier og tekniske firmaer

*Kategorier for teknisk produkt* bidrar til å sikre at tekniske produkter opprettes i henhold til firmaets forretningsregler og opptrer som nødvendig. Hvis du vil ha mer informasjon om kategorier for teknisk produkt, kan du se [Utviklingsversjoner og utviklingsproduktkategorier](engineering-versions-product-category.md).

Hver kategori for teknisk produkt tilhører et bestemt teknisk firma, og kan bare opprette produkter som tilhører dette firmaet. På samme måte tilhører rettigheten til å vedlikeholde et teknisk produkt til firmaet som er knyttet til produktets kategori for teknisk produkt.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Data som eies av det tekniske firmaet

Siden det teknsike firmaet eier teknisk relevante data, kontrollerer det følgende prosesser:

- **Opprettelse av tekniske produkter:** Hvert tekniske firma kan bare opprette nye tekniske produkter som er basert på en kategori for teknisk produkt som det eier. I enkelte tilfeller beholder driftsfirmaer sine egne lokale data som er relatert til disse produktene.
- **Oppretting av tekniske versjoner:** Når et firma oppretter et nytt teknisk produkt, oppretter systemet automatisk en første teknisk versjon for det. Bare det eiende tekniske firmaet vil kunne opprette nye versjoner av dette produktet.
- **Oppretting og vedlikehold av tekniske attributter:** Når et firma oppretter et nytt teknisk produkt, legger systemet automatisk til tekniske attributter i det. Bare det eiende tekniske firmaet vil kunne opprette og vedlikeholde verdiene for disse attributtene. Hvis du vil ha mer informasjon om tekniske attributter, kan du se [Tekniske attributter og søk i tekniske attributter](engineering-attributes-and-search.md).
- **Oppretting og vedlikehold av stykklister som er koblet til tekniske versjoner:** Det eiende tekniske firmaet kan koble en stykkliste direkte til en teknisk produktversjon. Når disse stykklistene frigis til andre juridiske enheter, er endringer i de tekniske dataene på stykklistene begrenset på følgende måter:

    - Driftsfirmaet kan ikke fjerne frigitte stykklistelinjer.
    - De tekniske feltene på stykklistelinjene er skrivebeskyttet for driftsfirmaet. Alle andre felter er logistikkimplementeringsfelter, og kan redigeres av driftsfirmaet.
    - Driftsfirmaet kan legge til stykklistelinjer i den samme stykklisten. På denne måten kan du legge til lokale tillegg, for eksempel pakkematerialer eller smørevæsker.
    - Driftsfirmaet kan legge til en helt ny, lokal stykkliste. Denne endringen kan være nødvendig i tilfeller der det for eksempel ikke finnes stykkliste under frigivelsen. Driftsfirmaet eier og vedlikeholder disse lokale stykklistene. Hvis du vil ha mer informasjon om frigivelsesbehandling, kan du se [Frigi produktstrukturer](release-product-structure.md).
    - Alle lokale stykklister og stykklistelinjer beholdes når det tekniske firmaet oppdaterer stykklisten.

- **Oppretting og vedlikehold av ruter som er koblet til tekniske versjoner:** Det eiende tekniske firmaet kan koble en rute direkte til hver tekniske versjon. Når disse rutene frigis til andre juridiske enheter, er endringer i de tekniske dataene på rutene begrenset på følgende måter:

    - De andre juridiske enhetene kan ikke fjerne teknsike data på rutene.
    - De andre juridiske enhetene kan legge til operasjoner i ruten. På denne måten kan de legge til lokale rutetrinn.
    - Driftsfirmaer kan legge til helt nye, lokale ruter. Denne endringen kan være nødvendig hvis du for eksempel ikke har inkludert ruter under frigivelsen. Driftsfirmaene eier og vedlikeholder disse lokale rutene. Hvis du vil ha mer informasjon om frigivelsesbehandling, kan du se [Frigi produktstrukturer](release-product-structure.md).
    - Alle endringer som gjøres lokalt, beholdes når oppdateringer fra det tekniske firmaet frigis på nytt til rutene.

- **Oppretting og vedlikehold av tekniske dokumenter:** Det tekniske firmaet kan knytte tekniske dokumenter til hver teknisk versjon.

    - Når disse dokumentene frigis til andre juridiske enheter, blir dokumentene beskyttet fra å bli fjernet av driftsfirmaet.
    - Andre juridiske enheter kan legge til helt nye, lokale dokumenter. Driftsfirmaet eier og vedlikeholder disse lokale dokumentene.
