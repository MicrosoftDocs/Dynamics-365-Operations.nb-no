---
title: Gavekortmodul
description: Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/02/2021
ms.topic: article
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
ms.openlocfilehash: 5a4aaf8e072f6547fe1dcf6fa156d2e144fd03ed806a2dc809a2cedb991461f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728345"
---
# <a name="gift-card-module"></a>Gavekortmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker gavekortmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.

Gavekortmoduler kan brukes i betalingsmoduler til å godta gavekort, som er en vanlig betalingsform som brukes i e-handelstransaksjoner. Gavekortmodulen støtter Dynamics 365-, SVS- og Givex-gavekort. SVS- og Givex-gavekort løses inn via betalingsleverandøren Adyen. Hvis du vil ha mer informasjon om støtte for eksterne gavekort som SVS og Givex, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md).

> [!NOTE]
> Støtte for innløsning av SVS- og Givex-gavekort under utsjekkingsflyten er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen. 

Det finnes to tilgjengelige gavekortmoduler:

- **Gavekort** – Denne modulen kan brukes på en betalingsside til å løse ut et gavekort som et betalingsmiddel. 
- **Kontroll av gavekortsaldo** – Denne modulen kan brukes på alle sider til å kontrollere saldoen på et gavekort. Denne modulen er tilgjengelig i Commerce versjon 10.0.14 og nyere.

> [!NOTE]
> Støtte for kontroll av gavekortsaldo er tilgjengelig i Dynamics 365 Commerce 10.0.14-versjonen.

Bildet nedenfor viser et eksempel på en gavekortmodul på en kasseside.

![Eksempel på en gavekortmodul.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modulegenskaper

- **Vis flere felt** – Denne egenskapen definerer hvilke felt som skal vises for gavekort i tillegg til gavekortnummeret, som alltid vises som standard. Noen gavekort støtter for eksempel visning av et personlig identifikasjonsnummer (PIN), og andre støtter visning av en PIN-kode og en utløpsdato. Alternativt kan denne egenskapen settes til "Ingen", som bare vil vise gavekortnummeret og ingen flere felt.

    Følgende verdier støttes:

    - PIN-kode
    - Utløpsdato
    - PIN-kode og utløpsdato 
    - None

- **Aktiver for gjestebrukere** – Når denne egenskapen er aktivert, kan gjestebrukere løse inn eller sjekke saldoer på gavekort. Dette egenskapen krever at anonym tilgang (gjestetilgang) for gavekort aktiveres i Commerce headquarters. Hvis du vil ha mer informasjon, kan du se [Aktiver gavekortbetalinger for gjestekassen](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> Egenskapen **Aktiver for gjestebrukere** er tilgjengelig fra og med Commerce, versjon 10.0.21. Den krever at Commerce-modulbibliotekpakken versjon 9.31 er installert.

## <a name="site-settings-for-gift-card-modules"></a>Områdeinnstillinger for gavekortmoduler

I Commerce-områdebygger under **Områdeinnstillinger \> Tillegg** er det en innstilling for gavekortmodulen kalt **Støttet gavekorttype**. Denne innstillingen støtter tre verdier:
- **Dynamics 365-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Dynamics 365-gavekort. Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.
- **SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen bare innløsning av Givex- og SVS-gavekort. Denne innstillingen støttes for påloggede og anonyme brukere på e-handelsområdet.
- **Dynamics 365-, SVS- og Givex-gavekort** – Når denne innstillingen brukes, tillater gavekortmodulen innløsning av Dynamics 365-, Givex- og SVS-gavekort. Denne innstillingen støttes bare for påloggede brukere på e-handelsområdet.

> [!IMPORTANT]
> Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.11-versjonen og er bare nødvendige hvis du trenger støtte for SVS- eller Givex-gavekort. Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Utvide interne gavekort til bruk i butikkfasader for e-handel på nettet

Interne gavekort er som standard ikke optimalisert for bruk i butikkfasader for e-handel på nettet. Før du tillater bruk av interne gavekort til betaling, bør du derfor konfigurere dem med utvidelser som gjør det sikrere å bruke dem. Her er gavekortområdene du bør utvide før du tillater bruk av interne gavekort i produksjon:

- **Gavekortnummer** – Nummerserier brukes til å generere gavekortnumre for interne gavekort. Siden nummerserier lett kan forutses, bør du utvide genereringen av gavekortnumre slik at tilfeldige, kryptografisk sikre strenger brukes for gavekortnumrene som utstedes.
- **GetBalance** – **GetBalance**-API-en brukes til å slå opp gavekortsaldoer. Som standard er denne API-en offentlig. Hvis en PIN-kode ikke kreves for å slå opp gavekortsaldoer, er det en risiko for at angrep med rå kraft kan bruke **GetBalance**-APIen til å prøve å slå opp gavekortnumre som har saldoer. Ved å implementere både PIN-krav til interne gavekort og API-begrensning, kan du redusere risikoen.
- **PIN-kode** – Som standard støtter ikke interne gavekort PIN-koder. Du bør utvide interne gavekort, slik at en PIN-kode kreves for å slå opp saldoer. Denne funksjonaliteten kan også brukes til å låse gavekort etter fortløpende feil forsøk på å angi PIN-kode.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Aktivere gavekortbetalinger for gjesteutsjekking

Som standard er ikke gavekortbetalinger aktivert for gjestutsjekking (anonym). Følg denne fremgangsmåten for å aktivere dem.

1. I Commerce Headquarters går du til **Retail og Commerce \> Kanaloppsett \> POS-oppsett \> POS \> POS-operasjoner**.
1. Merk og hold (eller høyreklikk) hodet i rutenettet, og velg deretter **Sett inn kolonner**.
1. Merk av for **AllowAnonymousAccess** i dialogboksen **Sett inn kolonner**.
1. Velg **Oppdater**.
1. For operasjonene **520** (gavekortsaldo) og **214** setter du verdien **AllowAnonymousAccess** til **1**.
1. Velg **Lagre**.
1. Kjør planleggerjobben **1090** for å synkronisere endringer i kanaldatabasen. 

## <a name="add-a-gift-card-module-to-a-page"></a>Legge til en gavekortmodul på en side

Hvis du vil ha informasjon om hvordan du legger til en gavekortmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Støtte for eksterne gavekort](./dev-itpro/gift-card.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
