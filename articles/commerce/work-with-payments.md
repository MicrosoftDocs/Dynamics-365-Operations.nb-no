---
title: Betalingsmåter i telefonsentre
description: Denne artikkelen beskriver de ulike betalingsmåtene som du kan bruke i et telefonsenter i Dynamics 365 Commerce.
author: josaw1
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7f47b6865f408a1dc833dcf15fc254ef8b802bcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902717"
---
# <a name="payment-methods-in-call-centers"></a>Betalingsmåter i telefonsentre

[!include [banner](includes/banner.md)]

I Dynamics 365 Commerce inneholder konfigurasjonen av telefonsenterkanalen en innstilling som heter **Aktiver ordrefullføring**. Denne innstillingen kan garantere at alle ordrer som opprettes av brukere av kanalen, bare frigis til ordrebehandling hvis de har en forhåndsbetalt eller forhåndsautorisert betaling som er innenfor de godkjente avvikene. Hvis innstillingen **Aktiver ordrefullføring** er slått på, kan telefonsenterbrukere angi betalinger mot salgsordrer for kunder ved hjelp av funksjonene for betalingsbehandling for telefonsenter. Hvis innstillingen er deaktivert, kan ikke telefonsenterbrukere bruke funksjoner for betalingsbehandling, men de kan fremdeles bruke forskuddsbetalinger for salgsordrer ved å bruke standardfunksjon for kunder.

Som en del av kanalkonfigurasjonen kan et firma definere betalingsmåter som er tillatt for en telefonsenterkanal. Telefonsenterkanalen bruker samme de betalingsmåtene som er definert for butikkanalene.

Hvis du vil konfigurere betalingsmåter for en telefonsenterkanal, kan du gå til **Retail og Commerce** \> **Kanaler** \> **Telefonsentre** \> **Alle telefonsentre**, og deretter, på **Oppsett**-menyen, velger du alternativet **Betalingsmåter**.

Når du oppretter en betalingsmåte, finnes det fem funksjoner for betalingsmåte som du kan tilordne.

| Funksjon            | beskrivelse |
|---------------------|-------------|
| Normal              | Bruk **Normal**-funksjonen for betalingsmåten når du definerer betalingsmåter som kontant eller bilag. Når disse typene betalinger brukes på en salgsordre i telefonsenteret, settes **Forskuddsbetaling**-flagget som standard til **Ja**. Dette bokfører umiddelbart et forskuddbetalingsbilag til kundekontoen når denne ordren sendes. Brukere kan endre **Forskuddbetaling**-flagget til **Ingen** hvis ønsket, slik at betalingsbilaget ikke opprettes før postering av faktura. Forskuddsbetalingsbilaget posteres i transaksjonshistorikken til en kunde, der det systematisk utlignes mot fakturaen for salgsordren. |
| Kontroll               | Bruk **Sjekk**-funksjonen når du definerer et banksjekkinstrument som en form for betaling. Når denne typen betaling brukes for en salgsordre, må brukeren angi kundens sjekknummer som en del av betalingsplasseringen. Sjekkbetalinger behandles alltid som forskuddsbetalinger når de brukes, og betalingsbilag opprettes umiddelbart ved ordreoverføring. Disse forskuddsbetalingsbilagene utlignes systematisk mot fakturaene som opprettes for ordren. |
| Kort               | Kortbetalingstyper representerer alle typer betaling som krever registrering av et kortnummer som er angitt på kundens betalingskort. Eksempler er kredittkort og gavekort. Når du konfigurerer disse betalingstypene, må du bruke **Kortoppsett**-menyen for å definere kort-IDer som er knyttet til denne betalingsmetoden. Ved ordreregistrering kan brukere angi om kortbetalingen skal forskuddsbetales, ved hjelp av alternativet **Forskuddsbetaling** som vises på siden for betalingsregistrering. Med mindre virksomheten krever forskuddsbetaling, er den vanlige flyten til en vanlig kredittkortbetaling en totrinnsprosess, der godkjenning innhentes ved ordreregistrering, og deretter utlignes og hentes betalingen fra kundekortet ved fakturering. Forskuddsbetaling anbefales for gavekortbetalinger, fordi gavekortsaldoen skal reduseres umiddelbart slik at kunden ikke kan bruke den samme verdien et annet sted. |
| Kunde            | **Kunde**-funksjonen på en betalingsmåte betyr at betalingen blir brukt på kundens kredittgrense eller satt "på kontoen." I Commerce kan en kunde være tilordnet en kredittgrense som kan valideres på tidspunktet for ordreregistrering. Betalinger som gjøres ved å bruke en betalingsmåte som er knyttet til **Kunde**-funksjonen, oppretter en gjeld mot kundens konto. Når salgsordren deretter faktureres, vises en forfalt saldo. I slike tilfeller må sender kundene vanligvis en betaling, i henhold til vilkårene som er tildelt. Et tidligere åpent kredittbilag på kundekontoen kan eventuelt brukes til å utligne saldoen som forfaller. Legg merke til at selv om du definerer denne betalingsmåten, vises den ikke blant betalingsalternativene i ordreregistrering i telefonsenteret med mindre **Tillat a konto**-flagget er angitt på i kundeposten for kunden som du arbeider med. Dette flagget finnes i kategorien **Betalingsstandarder** i kundeposten. |
| Betalingsmiddel fjern/flyt | Funksjonen **Betalingsmiddel fjern/flyt** brukes ikke av telefonsenteret. Den er bare tilgjengelig når du definerer betalingsmåtene som POS-programmet bruker i en butikkanal. |

Når betalingsmåter defineres, bør de kobles til en finans- eller bankkonto. Hvis du utelater dette trinnet, får brukerne feil når de prøver å lagre betalingstypen.

## <a name="refund-payment-methods"></a>Betalingsmåte for refundering

For behandling av refundering bruker telefonsenteren også noen av betalingsmåtene som er definert i kunder. Hvis du vil konfigurere disse betalingsmåtene, kan du gå til **Retail og Commerce** \> **Kanaloppsett** \> **Telefonsenteroppsett** \> **Refunderingsmetoder for telefonsenter**. Du må fullføre denne konfigurasjonen for å behandle refunderingssjekker til kunder. Hvis en kunde for eksempel opprinnelig har betalt for en ordre ved bruk av kontanter eller sjekk, kan brukeren sende kunden refunderingssjekk via kunder. I dette tilfellet må betalingstypene kontanter og sjekkbetaling i telefonsenteret tilordnes til den riktige betalingsmåten i kunder for å garantere at refunderingen behandles på riktig måte.

I tillegg, hvis en bruker behandler en returordre som en telefonsenterbruker i Commerce, men brukeren ikke kan koble returen til et opprinnelig salg, må betalingsmåten **Retur** defineres i parameterne for telefonsenter. Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Telefonsenteroppsett** \> **Parametere for telefonsenter**, og kontroller deretter at en betalingsmåte er definert i kategorien **RMA/retur** under **Betalingsmåte**. Betalingsmåten blir betalingsmåten som brukes til refunderinger. Den vil vanligvis defineres som en sjekkmetode eller en kundekontometode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]