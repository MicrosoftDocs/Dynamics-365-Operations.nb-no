---
title: Leveringsalternativmodul
description: Denne artikkelen dekker moduler for leveringsalternativer og forklarer hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c3fb60c61878fc790a44178fabc8a7be5809806b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268454"
---
# <a name="delivery-options-module"></a>Leveringsalternativmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker moduler for leveringsalternativer og forklarer hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.

Med moduler for leveringsalternativer kan kunder velge en leveringsmodus, for eksempel forsendelse eller henting for bestillinger på nettet. Det kreves en forsendelsesadresse for å bestemme leveringsmåten. Hvis leveringsadressen endres, må leveringsalternativene hentes på nytt. Hvis en ordre bare omfatter varer som skal plukkes i en butikk, blir denne modulen automatisk skjult.

Hvis du vil ha informasjon om hvordan du konfigurerer leveringsmoduser, kan du se [Konfigurasjon av Internett-kanal](channel-setup-online.md) og [Definere leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Hver leveringsmodus kan ha et tilknyttet gebyr. Hvis du vil ha mer informasjon om hvordan du konfigurerer gebyrer for en nettbutikk, kan du se [Avanserte automatiske gebyrer for omnikanal](omni-auto-charges.md).

I Commerce versjon 10.0.13 er modulen for leveringsalternativer oppdatert for å støtte funksjonene **Hodegebyrer uten fordeling** og **Levering som et linjegebyr**. Hvis fordeling er deaktivert, er forventningen at arbeidsflyten for e-handel ikke tillater en blandet leveringsmodus for varene i handlekurven (det vil si at noen varer er valgt for forsendelse, men andre er valgt for henting). Funksjonen **Hodegebyrer uten fordeling** krever at flagget **Aktiver konsekvent behandling av leveringsmodus i kanal** er aktivert i Commerce Headquarters. Når funksjonsflagget er aktivert, brukes forsendelsesgebyrer på hodenivå eller linjenivå, avhengig av konfigurasjonen i Commerce Headquarters.

Oppsettet fra Fabrikam støtter en blandet leveringsmodus, der noen varer er valgt for forsendelse, men andre velges for plukking. I denne modusen blir forsendelsesgebyrer fordelt for alle varer som er valgt i leveringsmåten ved levering. For at en blandet leveringsmodus skal fungere, må du først konfigurere funksjonen **Hodegebyrer med fordeling** i Commerce Headquarters. Hvis du vil ha mer informasjon om denne konfigurasjonen, se [Fordele hodegebyrer for å matche salgslinjer](pro-rate-charges-matching-lines.md).

Hvis forsendelsesgebyrer gjelder for linjevarer, kan de vises på handlekurvlinjen for hver vare. Denne funksjonaliteten krever at egenskapen **Vis forsendelseskostnader for linjevare** er aktivert for både handlekurv- og kassemodulen. Hvis du vil ha mer informasjon, kan du se [Handlekurvmodul](add-cart-module.md) og [Kassemodul](add-checkout-module.md).

Illustrasjonen nedenfor viser et eksempel på en leveringsalternativer-modul på en kasseside.

![Eksempel på en modul for leveringsalternativer på en kasseside.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Egenskaper for modul for leveringsalternativer

| Egenskap | Verdier | beskrivelse |
|----------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En valgfri overskrift for modulen for leveringsalternativer. |
| Egendefinert CSS-klassenavn | Tekst | Et egendefinert CSS-klassenavn (gjennomgripende stilark) som skal brukes til å gjengi denne modulen, hvis tilgjengelig. |
| Alternativ for leveringsmåte for filter | **Ikke filtrer** eller **Ikke-leveringsmoduser** | En verdi som angir om modulen for leveringsalternativer skal filtrere ut alle leveringsmoduser som ikke er forsendelse. |
| Velge et leveringsalternativ automatisk | **Ikke filtrer**, **Velg leveringsalternativ automatisk og vis sammendrag** eller **Velg leveringsalternativ automatisk og ikke vis sammendrag** | Denne egenskapen bruker automatisk det første tilgjengelige leveringsalternativet til kassen, uten at brukeren behøver å velge det. Det bør bare brukes hvis det er ett tilgjengelig leveringsalternativ. Denne egenskapen støttes fra og med Commerce versjon 10.0.19-utgivelsen. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Legge til en modul for leveringsalternativer på en kasseside og angi de nødvendige egenskapene

En modul for leveringsalternativer kan bare legges til i en kassemodul. Hvis du vil ha mer informasjon om hvordan du konfigurerer modulen for leveringsalternativer og legger den til på en kasseside, se [Kassemodul](add-checkout-module.md).

> [!NOTE]
> Det kan hende at leveringshåndteringen blir inkonsekvent, eller at ufordelte tillegg på hodenivå ikke vises i e-handelskanalen. Hvis du vil ha informasjon om hvordan du løser disse problemene, kan du se [Aktiver konsekvent leveringsmåtehåndtering i e-handelskanaler](consistent-delivery-mode-handling.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)

[Oppsett av nettkanal](channel-setup-online.md)

[Avanserte automatiske tillegg for omnikanal](omni-auto-charges.md)

[Fordele hodegebyrer for å matche salgslinjer](pro-rate-charges-matching-lines.md)

[Definer leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
