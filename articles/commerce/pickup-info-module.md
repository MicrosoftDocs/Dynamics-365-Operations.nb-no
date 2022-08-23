---
title: Modul for henteinformasjon
description: Denne artikkelen dekker henteinformasjonsmodulen og beskriver hvordan du legger den til på utsjekkingssider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 57633b7a23e581278ec0bc09ea146f5453570c4e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288413"
---
# <a name="pickup-information-module"></a>Modul for henteinformasjon

[!include [banner](includes/banner.md)]

Denne artikkelen dekker henteinformasjonsmodulen og beskriver hvordan du legger den til på utsjekkingssider i Microsoft Dynamics 365 Commerce.

Henteinformasjonsmodulen kan brukes i en kassemodulen til å vise henteinformasjon for ordre. Kunder kan se tilgjengelige hentedatoer og -tidspunkter, og deretter velge en passende tid for å hente ordren. En kunde kan for eksempel velge å hente en ordre klokken 15:00 den 21. mars fra San Francisco-butikken.

Hentetidspunkter for de aktuelle butikkene må konfigureres i Commerce Headquarters. Hvis du vil ha mer informasjon, kan du se [Opprette og oppdatere tidspunkter for kundehenting](dev-itpro/pickup-timeslots.md).

Hvis en henteinformasjonsmodul opprettes på en utsjekkingsside, men det ikke er definert noen tidspunkter for butikken som er valgt for henting, vil modulen vise informasjon, men brukeren vil ikke kunne velge noen tidspunkter. Tidspunkter er valgfrie og kreves ikke for å legge inn en ordre.

Hvis flere varer er valgt for henting på tvers av flere butikker, last henteinformasjonsmodulen brukeren velge et tidspunkt for hver butikk, forutsatt at tidspunktene er tilgjengelige for den.

> [!NOTE]
> Støtte for henteinformasjonsmodulen for tidspunkter og utsjekking er tilgjengelig i Dynamics 365 Commerce, versjon 10.0.15 og nyere.

Følgende illustrasjon viser et eksempel på valg av tidspunkt ved hjelp av henteinformasjonsmodulen på en utsjekkingsside.

![Eksempel på en henteinformasjonsmodul på en utsjekkingsside.](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Modulegenskaper

- **Overskrift** – Angi en overskrift for modulen.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Vis informasjon om tidspunkt etter at en ordre er bestilt

Etter at en ordre er bestilt, kan informasjon om det valgte tidspunktet vises i [ordrebekreftelsesmodulen](order-confirmation-module.md) og [ordredetaljmodulen](account-management.md#order-details-page). Begge disse modulene har en egenskap for **Vis tidspunktinformasjon**. Før de kan vise det valgte tidspunktet i løpet av ordreprosessen, må denne egenskapen settes til **sann**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Legg til en henteinformasjonsmodul for utsjekking på en side

Hvis du vil ha informasjon om hvordan du legger til en henteinformasjonsmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).

Følgende illustrasjon viser et eksempel på en betalingsside for e-handel som inkluderer tidspunkter for hentelinjevarer.

![Eksempel på en betalingsside for e-handel som inkluderer tidspunkter for hentelinjevarer.](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Tilleggsressurser

[Opprett og oppdater tidsrom for kundehenting](dev-itpro/pickup-timeslots.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Ordredetaljermodul](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
