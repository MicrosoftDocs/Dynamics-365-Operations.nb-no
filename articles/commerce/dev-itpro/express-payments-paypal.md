---
title: Konfigurere ekspressbetalinger for PayPal
description: Denne artikkelen beskriver hvordan du konfigurerer ekspressbetalinger for PayPal for å oppnå raskere betalingsfunksjonalitet i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b69b7384992fb86370ff6881824a7d2c9a77d2c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905288"
---
# <a name="configure-express-payments-for-paypal"></a>Konfigurere ekspressbetalinger for PayPal

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer ekspressbetalinger for PayPal for å oppnå raskere betalingsfunksjonalitet i Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| PayPal-lommebok | Kundeopplevelsen og integreringen som støttes av PayPal-koblingen. Den kan også kalles PayPal-knappen. |
| Lommebok | En betalingstype som ikke omfatter tradisjonelle betalingsegenskaper, for eksempel BIN-området (Bank Identification Number) og utløpsdatoen, som brukes til å skille mellom kreditt- og debetkorttyper. |
| Betalingsekspress | En Commerce-modul som støtter raskere betalingsfunksjonalitet når støttede betalingsmetoder brukes. Denne artikkelen dekker bruken av betalingsekspressmodulen med PayPal. |

Dynamics 365 Commerce tilbyr en ut av bruksklar integrering for PayPal-lommeboken. Når Dynamics 365 Payment Connector for PayPal er konfigurert, vises PayPal-knappen som en betalingsmetode du kan velge når du skal betale for en bestilling på nettet. Når brukere velger PayPal, sendes de direkte til PayPal der de fullfører betalingen, og deretter returneres de til nettbutikken for å fullføre bestillingen. Med betaling via PayPal kan kunder bruke betalingskontoinformasjonen til å fylle ut betalingsskjemaet på forhånd, slik at de kan fullføre betalingsprosessen raskere.

Commerce har lagt til en betalingsekspressmodul for å legge til rette for ekspressbetaling. Betalingsekspressmodulen kan brukes i et fragment som kan tas med på en betalings- eller handlekurvside. Når PayPal er konfigurert, brukes den samme Dynamics 365 Payment Connector for PayPal-koblingsreferansen for både betalingsekspressalternativet og det vanlige betalingsalternativet.

## <a name="paypal-checkout-in-commerce"></a>PayPal-betaling i Commerce

### <a name="prerequisites"></a>Forutsetninger

Konfigurer PayPal-lommeboken for miljøet ditt som beskrevet i [Dynamics 365 Payment Connector for PayPal](../paypal.md).

Hvis du bruker PayPal som et alternativ i den vanlige betalingsflyten (der brukere angir kontoinformasjonen manuelt uten å bruke forhåndsutfyllingshandlingene for betalingsekspress), følger du konfigurasjonsinstruksjonene i [Betalingsmodul](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Betalingsekspressmodul med PayPal

Betalingsekspressmodulen fungerer med støttende betalingsmetoder, slik at kunder på nettstedet kan betale raskere ved å forhåndsutfylle kontoinformasjonen for betalingstjenesten i løpet av betalingsprosessen. Betalingsekspressmodulen bruker den konfigurerte betalingskoblingen til å fylle ut betalingsskjemaet på forhånd med brukerkontoinformasjon, for eksempel adresse, kontaktinformasjon og valgt betalingsmetode.

Når PayPal-ekspressbetaling brukes og en bruker velger PayPal-knappen i betalingsekspressdelen på betalingssiden, åpnes et iFrame-vindu for PayPal-betaling. Brukeren logger seg deretter på PayPal-kontoen for å bruke kontoens leveringsadresse, faktureringsadresse, e-postadresse og valgte PayPal-betalingsmetode for å betale for transaksjonen.

Etter at brukeren har fullført handlingen i PayPal-vinduet, sendes de tilbake til betalingssiden på Commerce-nettstedet, der betalingsskjemaet er forhåndsutfylt med de valgte detaljene. I betalingsekspressflyten blir det første leveringsalternativet som er tilgjengelig for leveringsadressen som returneres, fylt ut på forhånd for brukeren. Brukeren kan deretter se gjennom bestillingen og endre betalingsdetaljer før vedkommende velger **Bestill** for å fullføre bestillingen.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>Legge til betalingsekspressmodulen med PayPal i et fragment

Følg denne fremgangsmåten for å legge til betalingsekspressmodulen med PayPal i et fragment i Commerce-områdebygger.

1. Gå til nettstedet ditt.
1. I venstre navigasjonsrute velger du **Fragmenter**, og deretter velger du **Nytt**.
1. I dialogboksen **Nytt fragment** finner og velger du **Betalingsekspress**-modulen, og under **Fragmentnavn** skriver du inn et navn for fragmentet (for eksempel **Ekspressbetaling**).
1. Velg **OK** for å opprette fragmentet.
1. I disposisjonsvisningen velger du sporet for betalingsekspressmodulen du opprettet.
1. Velg **Overskrift** i egenskapsruten.
1. Skriv inn overskriftsteksten du vil skal vises for ekspressbetalingsdelen på nettstedet (for eksempel **Ekspressbetaling**), i feltet **Overskriftstekst** i dialogboksen **Overskrift**.
1. Velg overskriftsnivået (for eksempel **H2**) under **Overskriftsnivå**.
1. Velg **OK**.
1. Angi eller juster høyden på iFrame-elementet (for eksempel **60**) i feltet **Høyden på iFrame** i egenskapsruten.
1. Angi **PayPal** i feltet **Støttede betalingsmiddeltyper**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Legge til betalingsekspressfragmentet på betalingssiden

Følg denne fremgangsmåten for å legge til betalingsekspressfragmentet på betalingssiden i områdebygger.

1. Gå til nettstedet ditt.
1. Velg **Sider** i venstre navigasjonsrute, og velg deretter betalingssiden på nettstedet ditt.
1. Velg **Rediger** for å redigere siden.
1. I **Hoved**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.

    > [!NOTE]
    > Hvis det allerede finnes en beholdermodul som inneholder et betalingsfragment, flytter du betalingsekspressdelen slik at den vises ovenfor eksisterende betalingsbeholder i **Hoved**-sporet. Betalingsekspressdelen gjengis deretter ovenfor den vanlige betalingsbeholderen. Hvis du vil flytte en beholdermodul opp eller ned, velger du ellipsen (**...**), og deretter velger du **Flytt opp** eller **Flytt ned**.

1. Vi anbefaler at du konfigurerer egenskapsinnstillingene i egenskapsruten **Beholder** på følgende måte:

    - **Beholderoppsett** – Velg **Stablet**.
    - **Bredde** – Velg **Fyll beholder**.
    - **Underordnede som vises** – Velg **Tre**.

1. I **Beholder**-sporet velger du ellipsen (**...**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg et fragment** finner og velger du ekspressbetalingsfragmentet du opprettet, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Legge til betalingsekspressfragmentet på handlekurvsiden

Følg denne fremgangsmåten for å legge til betalingsekspressfragmentet på handlekurvsiden i områdebygger.

1. Gå til nettstedet ditt.
1. Velg **Sider** i venstre navigasjonsrute, og velg deretter handlekurvsiden på nettstedet ditt.
1. Velg **Rediger** for å redigere siden.
1. Finn beholderen som inneholder **Handlekurv**-modulen i **Hoved**-sporet. **Handlekurv**-modulen inneholder et **Betalingsekspress**-spor.
1. Velg **Betalingsekspress**-sporet, velg ellipsen (**...**), og velg deretter **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Betalingsekspress**-modulen, og deretter velger du **OK**.
1. Angi **Paypal** i feltet **Støttede betalingsmiddeltyper** i egenskapsruten.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="modes-of-delivery"></a>Leveringsmåter

Når betalingsekspressmodulen er konfigurert slik at den bruker PayPal, blir det første leveringsalternativet som returneres for leveringsadressen som ble valgt for PayPal-kontoen, fylt ut på forhånd. Brukere kan endre leveringsadressen hvis de ønsker det.

Rekkefølgen for leveringsmåten konfigureres i delen **Leveringsmåter** for kanalen i Commerce headquarters. Hvis du vil ha mer informasjon, kan du se [Definere leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Betalingsmodulen bruker også modulen for leveringsalternativer når leveringsmåter gjengis under betalingen. Hvis du vil ha mer informasjon, kan du se [Modul for leveringsalternativer](../delivery-options-module.md).

Leveringsmåter legges til i listen for nettbutikken i Commerce headquarters. Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**, og velg kanal-ID-en for butikken. Velg deretter **Oppsett \> Leveringsmåter**. Leveringsmåtene for modulen som vises i konfigurasjonen, vises på lignende måte på nettstedet. Hvis du vil legge til eller fjerne leveringsmåter for en detaljhandelskanal eller et produkt, velger du **Behandle leveringsmåter** i handlingsruten.

## <a name="additional-resources"></a>Tilleggsressurser

[Vanlige spørsmål om betalinger](payments-retail.md)

[Kassemodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)

[Definer leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Modul for leveringsalternativer](../delivery-options-module.md)
