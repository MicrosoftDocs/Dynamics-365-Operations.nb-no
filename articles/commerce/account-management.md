---
title: Kontobehandlingssider og -moduler
description: Denne artikkelen dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 2db9a1218802234297e9d027691e5887d6a5c808
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274462"
---
# <a name="account-management-pages-and-modules"></a>Kontobehandlingssider og -moduler

[!include [banner](includes/banner.md)]

Denne artikkelen dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.

Kontobehandling refererer til en gruppe med sider som brukes til å behandle informasjon som er relatert til brukerkontoer i Dynamics 365 Commerce. Kontobehandlingssidene inkluderer målsiden for kontostyring, brukerprofilside, brukeradresseside, ordreloggside, ordredetaljerside, loyalitetsside og ønskelisteside.

### <a name="account-management-landing-page"></a>Målside for kontobehandling

Målsiden for kontoadministrasjons bruker følgende moduler:

- **Container** - Alle modulene for målside for kontobehandlings må plasseres i en container. 
- **Velkomstflis for konto** – Denne modulen brukes til å gi en velkomstmelding på kontobehandlingssiden. Den inneholder egenskaper for overskriften.
- **Generell flis for konto** – Denne modulen kan brukes til å angi overskrifter og koblinger til kontobehandlingssider, for eksempel sidene Ordrehistorikk og Min profil. Generell flis-modulen kan brukes til å konfigurere en flis for en side. I Fabrikam brukes denne modulen for koblinger for Ordrehistorikk- og Min profil-siden på målsiden for kontobehandling.
- **Ønskelisteflis for konto** – Denne modulen brukes til å gi et sammendrag av varene i kundens ønskeliste. Det kan for eksempel stå "Du har 10 elementer i ønskelisten". Den inneholder egenskaper for overskriften og koblingen "Vis detaljer". Vis detaljer-koblingen bør konfigureres til å omdirigere til ønskelistesiden. 
- **Kontoadresseflis** – Denne modulen brukes til å gi et sammendrag av brukerens adresse. Det kan for eksempel stå "Du har lagt til 2 adresser i kontoen din". Den inneholder egenskaper for overskriften og koblingen "Vis detaljer". Vis detaljer-koblingen bør konfigureres til å omdirigere til brukeradressesiden.
- **Kontofordelsflis** – Denne modulen brukes til å vise og koble til informasjon om fordelsprogrammer. Denne flisen har to tilstander: en tilstand viser koblinger til et fordelsprogram hvis brukeren ikke allerede er medlem. Den andre tilstanden viser koblinger for å vise siden med fordelsdetaljer når brukeren allerede er medlem. Egenskaper inkluderer overskriften, Registrering-koblingen og Vis fordel-koblingen. Vis fordel-koblingen bør konfigureres til å omdirigere til fordelssiden. Registrering-koblingen kan konfigureres til å omadressere til en side der brukere kan bli med i fordelsprogrammet. 

### <a name="order-history-page"></a>Siden Ordrehistorikk

Siden for ordrehistorikk bruker ordreloggmodulen til å vise alle de siste ordrene som brukeren har lagt inn.

### <a name="order-details-page"></a>Side for ordredetaljer

Ordredetaljer-siden inneholder detaljert informasjon for hver ordre og er tilgjengelig fra ordrehistorikksiden. Den bruker ordredetaljermodulen, som krever salgs-IDen eller transaksjons-IDen for å hente ordredetaljene.

### <a name="my-profile-page"></a>Min profilside

Min profil-siden viser brukerens kontoprofildetaljer ved hjelp av kontoprofilmodulen. Siden viser e-postadressen som er knyttet til brukerens konto, i tillegg til innstillinger som er angitt for kontoen. Hvis du definerer egendefinerte kundeattributter, viser også delen Tilleggsinformasjon disse attributtene. Brukere kan redigere navn, innstillinger eller tilleggsinformasjon (hvis tilgjengelig).

### <a name="user-address-page"></a>Brukeradresseside

Siden for brukeradresse viser listen over adresser som er knyttet til brukerkontoen. Brukeren har enten oppgitt disse adressene under utsjekking eller lagt dem til direkte på denne siden. Brukeradressemodulen brukes til å legge til og redigere adresser, angi primæradresse og gjengi eksisterende adresser på siden.

### <a name="wish-list-page"></a>Ønskelisteside

Ønskelistesiden viser varene som er lagt til på kundens ønskeliste. Den bruker ønskelistemodulen til å vise ønskelisteelementer.

### <a name="loyalty-page"></a>Fordelsside

Fordelssiden lar kunder vise sine fordelsdetaljer hvis de allerede er medlemmer av fordelsprogrammet. De kan også vise poengene de har tjent opp og løst inn i nylige transaksjoner. Siden bruker modulen for fordelsdetaljer til å vise fordelsdetaljene. 

For å bli med i et fordelsprogram kan det opprettes en markedsføringsside med moduler for fordelsregistrering og fordelsvilkår. Hvis brukeren ikke er medlem av et fordelsprogram, vil disse modulene gjøre det mulig for brukeren å registrere seg.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Beholdermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
