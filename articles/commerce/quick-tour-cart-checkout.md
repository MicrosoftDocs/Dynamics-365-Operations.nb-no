---
title: Oversikt over sider for handlekurv og kasse
description: Dette emnet inneholder en oversikt over sider for handlekurv og kasse i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e450192025b29c655be49050aa3e61fc8acd898
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982974"
---
# <a name="cart-and-checkout-pages-overview"></a>Oversikt over sider for handlekurv og kasse

[!include [banner](includes/banner.md)]

Dette emnet inneholder en oversikt over sider for handlekurv og kasse i Microsoft Dynamics 365 Commerce.

Handlekurvsiden for et e-handelsområde viser alle varene som en kunde har lagt til i handlekurven. Handlekurvsiden bygges ved hjelp av handlemodulen. Handlekurvmodulen er en container som er vert for alle modulene som kreves for å vise varer i handlekurven. Handlekurvmodulen kan også bruke de andre modulene for å vise ordresammendraget og eventuelle kampanjekoder som er brukt på kundeordren.

Kassesiden for et webområde for e-handel viser en trinnvis flyt som kundene følger for å angi all informasjon som kreves for å legge inn en ordre. En kassemodul kan inneholde moduler som håndterer leveringsadressen, leveringsmetoder, faktureringsinformasjon, ordresammendrag og annen informasjon som er knyttet til kundeordrer.

## <a name="cart-page"></a>Handlevognside

Handlekurvsidene fungerer som handlepose og inneholder alle varene som er lagt til i handlekurven.

Illustrasjonen nedenfor viser et eksempel på en handlekurvside som ble bygd ved hjelp av modulbiblioteket og "Fabrikam"-temaet.

![Eksempel på en handlekurvside.](./media/cart2.PNG)

Hovedområdet på en handlekurvside viser alle varene som en kunde har lagt til i handlekurven. Alle gjeldende rabatter vises. Disse rabattene inkluderer komplekse rabatter. Eksempler inkluderer "Kjøp 3 varer og få 10 % avslag" eller "Kjøp en flaske og en ryggsekk for å få 10 % rabatt". Ordresammendragmodulen viser beløpet som forfaller etter at rabatter, levering, avgifter og så videre er påført. Det finnes også en promokodemodul som lar kunden bruke eller fjerne kampanjekoder.

En kunde kan handle anonymt eller som en pålogget bruker. Hvis en kunde er pålogget, beholdes varer i handlekurven mellom økter. På denne måten kan kunden fortsette å handle fra flere enheter.

Kunden kan gå videre til kassen fra handlekurven. En kunde kan starte utsjekking som en gjestebruker eller som en pålogget bruker.

Hvis du vil ha informasjon om hvordan du redigerer en handlekurv, se [Legge til en handlekurvmodul på en side](add-cart-module.md).

## <a name="checkout-page"></a>Utsjekkingsside

Utsjekkingssiden er der kunder angir informasjonen som kreves for å legge inn en ordre.

Illustrasjonen nedenfor viser et eksempel på en utsjekkingsside som ble bygd ved hjelp av modulbiblioteket.

![Eksempel på en utsjekkingsside.](./media/Checkout.PNG)

Hoveddelen av utsjekkingssiden er der all ordreinformasjon samles inn. Denne informasjonen omfatter leveringsadresse, leveringsalternativer og betalingsinformasjon. Kassen har en trinnvis flyt, fordi informasjonen må angis i en bestemt rekkefølge for å kunne behandles. Leveringsadressen må for eksempel angis før forsendelseskostnadene kan beregnes og betalingen kan autoriseres.

### <a name="shipping-address"></a>Leveringsadresse

Det kreves en forsendelsesadresse hvis varer må sendes. Formatet for forsendelsesadresser for hver nasjonal innstilling kan konfigureres i Dynamics 365 Commerce. Hvis varene for eksempel skal leveres til USA, må leveringsadressen inneholde en gateadresse, stat og postnummer (ZIP). Noe grunnleggende inndatavalidering utføres for felt for leveringsadresse, for eksempel validering for alfanumeriske tegn, maksimumslengde og tall. Selv om selve adressen ikke er bekreftet, kan denne verifiseringen utføres ved hjelp av tilpassede tredjepartstjenester.

Leveringsadressen brukes for alle varene i handlekurven som "forsendelse"-alternativet er valgt for. Hvis du bruker utsjekkingsflyten som er oppgitt i modulbiblioteket, kan ikke individuelle handlekurvvarer sendes til forskjellige adresser. Hvis du trenger denne funksjonen, kan den implementeres ved hjelp av tilpasning av kassemodulene.

Når leveringsadressen er angitt, vises forsendelsesmetodene som er tilgjengelige fra Dynamics 365 Commerce-nettbutikken. Forsendelsesmetodene og adressene de støtter, kan konfigureres i Commerce.

### <a name="payment"></a>Betaling

Neste trinn i utsjekkingsflyten er betalingen. I e-handel kan flere betalingsmåter brukes til å legge inn bestillinger, for eksempel kredittkort, gavekort og fordelspoeng. En kombinasjon av disse betalingsmåtene kan også brukes. Det kan være nødvendig med mer informasjon, avhengig av betalingsmåtene som brukes. En kredittkort betaling krever for eksempel en faktureringsadresse. Kredittkortbetalinger behandles ved hjelp av betalingskoblingen Adyen.

#### <a name="loyalty-points"></a>Fordelspoeng

Under betalingsflyten kan en kunde som er medlem av et fordelsprogram, og som har påløpte fordelspoeng, løse inn disse fordelspoengene for en ordre. Fordelspoengmodulen vises bare hvis kunden har et eksisterende fordelsmedlemskap. For ikke-medlemmer og gjestebrukere er denne modulen skjult.

#### <a name="gift-cards"></a>Gavekort

I modulbiblioteket kan du løse inn interne gavekort for en ordre. Hvis du vil bruke et internt gavekort, må kunden være pålogget. For ytterligere sikkerhet anbefaler vi at du tilpasser flyten ved hjelp av et personlig ID-nummer (PIN) for interne gavekort.

### <a name="signed-in-and-guest-users"></a>Påloggede brukere og gjestebrukere

Kunden kan fullføre utsjekkingsprosessen som en gjestebruker eller som en pålogget bruker. Hvis kunden logger på, hentes kontoopplysninger som lagrede leveringsadresser og lagrede kredittkortopplysninger automatisk.

### <a name="order-summary"></a>Ordresammendrag

Utsjekkingen viser et sammendrag av linjevarene i handlekurven, slik at kunden kan kontrollere ordren før han eller hun plasserer ordren. Linjeelementene kan ikke redigeres i løpet av utsjekkingsflyten. En kobling til handlekurven vises imidlertid i tilfelle brukeren ønsker å gå tilbake og redigere linjeelementer.

Etter at kunden har gitt leverings- og faktureringsinformasjon, viser ordresammendraget beløpet som forfaller etter fordelspoeng, gavekort og andre betalinger er brukt.

### <a name="order-confirmation-and-email"></a>Ordrebekreftelse og e-post

Når kunden legger inn en ordre, blir det oppgitt et bekreftelsesnummer. På dette stadiet er betalingen godkjent, men ikke belastet. Betalingen blir bare belastet når ordren er oppfylt (det vil si når den enten er levert eller plukket opp).

Når en ordre er opprettet, sendes det en e-post for ordrebekreftelse til kunden.

Hvis du vil ha mer informasjon om hvordan du redigerer en kasseside, se [Legge til en kassemodul på en side](add-checkout-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over startside](quick-tour-home-page.md)

[Oversikt over produktdetaljsider](quick-tour-pdp.md)

[Oversikt over kontobehandlingssider](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
