---
title: Kontobehandlingssider og -moduler
description: Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885815"
---
# <a name="account-management-pages-and-modules"></a>Kontobehandlingssider og -moduler

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Kontobehandling refererer til en gruppe med sider som brukes til å behandle informasjon som er relatert til brukerkontoer i Dynamics 365 Commerce. Kontobehandlingssidene inkluderer målsiden for kontostyring, brukerprofilside, brukeradresseside, ordreloggside, ordredetaljerside, loyalitetsside og ønskelisteside.

### <a name="account-management-landing-page"></a>Målside for kontobehandling

Målsiden for kontoadministrasjons bruker følgende moduler:

- **Innholdsplassering** – Denne modulen er en containermodul som inneholder alle modulene på målsiden for kontostyring.
- **Velkomstelement for konto** – Denne modulen brukes til å gi en velkomstmelding på kontobehandlingssiden. Den inneholder egenskaper for overskriften og flisstørrelsen. Egenskapen **Flisstørrelse** angir bredden på modulen i innholdsplasseringsmodulen. Verdiområdet fra **1** til **12**, der **12** representerer den fullstendige bredden på innholdsplasseringscontaineren.
- **Plasseringselement for kontoordre** – Denne modulen brukes til å gi et sammendrag av antall ordrer som er lagt inn av brukerkontoen. Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer". Vis detaljer-koblingen bør konfigureres til å omdirigere til ordreloggsiden.
- **Plasseringselement for kontoprofil** – Denne modulen brukes til å gi et sammendrag av brukerprofilen. Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer". Vis detaljer-koblingen bør konfigureres til å omdirigere til brukerprofilsiden.
- **Ønskelisteelement for konto** – Denne modulen brukes til å gi et sammendrag av varene i kundens ønskeliste. Det kan for eksempel stå "Du har 10 elementer i ønskelisten". Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer". Vis detaljer-koblingen bør konfigureres til å omdirigere til ønskelistesiden.
- **Kontoadresseelement** – Denne modulen brukes til å gi et sammendrag av brukerens adresse. Det kan for eksempel stå "Du har lagt til 2 adresser i kontoen din". Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer". Vis detaljer-koblingen bør konfigureres til å omdirigere til brukeradressesiden.
- **Kontofordelselement** – Denne modulen brukes til å vise og koble til informasjon om fordelsprogrammer. Den inneholder egenskaper for overskriften, flisstørrelsen, koblingen "vis detaljer" og koblingen "bli medlem". "Vis detaljer"-koblingen bør konfigureres til å omdirigere til fordelssiden. Koblingen "bli medlem" kan konfigureres til å omadressere til en side der brukere kan bli med i fordelsprogrammet.

### <a name="order-history-page"></a>Siden Ordrehistorikk

Siden for ordrehistorikk bruker ordreloggmodulen til å vise alle de siste ordrene som brukeren har lagt inn.

### <a name="order-details-page"></a>Side for ordredetaljer

Ordredetaljer-siden inneholder detaljert informasjon for hver ordre og er tilgjengelig fra ordrehistorikksiden. Den bruker ordredetaljermodulen, som krever salgs-IDen eller transaksjons-IDen for å hente ordredetaljene.

### <a name="user-profile-page"></a>Brukerprofilside

Siden brukerprofil viser brukerkontodetaljer, for eksempel brukerens navn og e-postadresse. Den bruker brukerprofilmodulen. Selv om epostadresse ikke kan fjernes, kan den redigeres. Brukerprofilsiden viser også brukerpreferansene som gjør en bruker i stand til å velge/velge bort bestemte funksjoner, for eksempel tilpassing av anbefalingslister. 

### <a name="user-address-page"></a>Brukeradresseside

Siden for brukeradresse viser listen over adresser som er knyttet til brukerkontoen. Brukeren har enten oppgitt disse adressene under utsjekking eller lagt dem til direkte på denne siden. Brukeradressemodulen brukes til å legge til og redigere adresser, angi primæradresse og gjengi eksisterende adresser på siden.

### <a name="wish-list-page"></a>Ønskelisteside

Ønskelistesiden viser varene som er lagt til på kundens ønskeliste. Den bruker ønskelistemodulen til å vise ønskelisteelementer.

### <a name="loyalty-page"></a>Fordelsside

Fordelssiden lar kunder bli med i et fordelsprogram eller, hvis de allerede er medlemmer at fordelsprogrammet, vise programdetaljer. De kan også vise poengene de har tjent opp og løst inn i nylige transaksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
