---
title: Handlekurvmodul
description: Denne artikkelen dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f3bf61d03d6e318494a13af6721028ac573d7424
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277065"
---
# <a name="cart-module"></a>Handlekurvmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen. Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.

Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest. Den støtter også koblingen **Tilbake til shopping**. Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.

Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området. 

Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.

![Eksempel på en handlekurvmodul på Fabrikam-området.](./media/cart2.PNG)

Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området. I dette eksemplet er det et behandlingsgebyr for en linjevare.

![Eksempel på en handlekurvmodul med et behandlingsgebyr for et linjeelement.](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Egenskaper og spor for handlekurvmodul

| Egenskap | Verdier | beskrivelse |
|----------------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En overskrift for handlekurven, for eksempel "Handlepose" eller "Varer i handlekurven". |
| Vis feil for utsolgte varer | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, viser handlekurvsiden lagerrelaterte feil. Vi anbefaler at du setter denne egenskapen til **Sann** hvis det brukes beholdningskontroller på stedet. |
| Vis forsendelseskostnader for linjevarer | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, viser handlekurvlinjer forsendelseskostnadene, hvis denne informasjonen er tilgjengelig. Denne funksjonen støttes ikke i Fabrikam-temaet fordi brukere velger bare levering i kasseflyten. Denne funksjonen kan imidlertid aktiveres i andre arbeidsflyter hvis den gjelder. |
| Vis tilgjengelige kampanjer| **Sann** eller **Usann** | Hvis egenskapen er satt til **Sann**, viser handlekurven tilgjengelige kampanjer basert på varene i handlekurven. Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.16. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler som kan brukes i handlekurvmodulen

- **Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen. Meldingene drives av innholdsbehandlingssystemet (CMS). Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."
- **Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Den lar brukere angi en plassering for å finne butikker i nærheten. Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).

## <a name="module-properties"></a>Modulegenskaper

Følgende innstillinger for handlevognmodulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:

- **Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).
- **Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen. Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.

> [!IMPORTANT]
> I Dynamics 365 Commerce 10.0.14 versjonen og senere samles varer i handlekurven basert på innstillingene som er definert i den elektroniske funksjonalitetsprofilen for nettbutikken i Commerce Headquarters. Hvis du vil ha mer informasjon om hvordan du oppretter en nettbasert funksjonalitetsprofil og angir egenskapene som kreves for aggregering, kan du se [Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit. Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Legge til en handlekurvmodul på en side

Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Velg fragment** velger du **Handlekurv**-modulen.
1. Under **Navn på fragment** angir du navnet **Handlevognfragment**, og deretter velger du **OK**.
1. Velg **Handlevogn**-sporet.
1. I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.
1. I **Handlevogn**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.
1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn på malen.
1. Velg **Brødtekst**-sporet i disposisjonstreet, velg ellipseknappen (**…**), og velg deretter **Legg til fragment**.
1. I dialogboksen **Velg fragment** velger du **Handlevognfragmentet**, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Velg en mal** velger du malen du opprettet, angir et sidenavn, og deretter velger du **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)

[Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md)

[Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
