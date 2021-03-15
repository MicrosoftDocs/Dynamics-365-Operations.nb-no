---
title: Kontobehandlingssider og -moduler
description: Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c465b8883438eee886b177274bf89ddb86aa00b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980562"
---
# <a name="account-management-pages-and-modules"></a>Kontobehandlingssider og -moduler

[!include [banner](includes/banner.md)]

Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

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

### <a name="user-profile-page"></a>Brukerprofilside

Siden brukerprofil viser brukerkontodetaljer, for eksempel brukerens navn og e-postadresse. Den bruker brukerprofildetaljene og brukerprofilredigeringsmodulene. Selv om epostadresse ikke kan fjernes, kan den redigeres. Brukerprofilsiden viser også brukerpreferansene som gjør en bruker i stand til å velge/velge bort bestemte funksjoner, for eksempel tilpassing av anbefalingslister. 

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