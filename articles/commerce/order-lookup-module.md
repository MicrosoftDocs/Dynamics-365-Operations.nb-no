---
title: Ordreoppslagsmodul
description: Denne artikkelen dekker ordreoppslagsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8c60ed0c334bf09916dd633302c6d813ea6f16b6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281461"
---
# <a name="order-lookup-module"></a>Ordreoppslagsmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker ordreoppslagsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

Ordreoppslagsmodulen gir et skjema som kundene kan bruke til å slå opp ordrer de har lagt inn på et e-handelsområde. Den brukes som en del av funksjonen [Aktivere ordreoppslag for gjestebetalinger](order-lookup-guest.md). Ordreoppslagsmodulen kan brukes til å slå opp ordrer som er sendt via et e-handelsområde, salgsstedet eller et telefonsenter. Skjemaet kan hente ordrer som ble sendt både av gjestebrukere og av registrerte brukere.

Illustrasjonen nedenfor viser et eksempel på skjemaet som gjengis av ordreoppslagsmodulen. Når kunder fyller ut skjemaet og velger **Finn ordren din**, blir de sendt videre til ordredetaljersiden.

![Skjema for ordreoppslagsmodulen på en side.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Egenskaper for Ordreoppslagsmodul

| Egenskapsnavn     | Verdi     | beskrivelse |
|-------------------|-----------|-------------|
| Overskrift           | Tekst      | Overskriften som vises øverst i skjemaet (for eksempel "Finn din ordre"). |
| Rik tekst         | Rik tekst | Valgfri, forklarende tekst som vises under overskriften. |
| Type ordrestatus | Opplisting      | <p>Velg typen informasjon som skjemaet vil be om fra kunden i tillegg til ordrebekreftelses-IDen. Følgende verdier støttes for øyeblikket:</p><ul><li><b>E-post</b> – Skjemaet inneholder et felt der kunder kan angi e-postadressen de brukte da de la inn ordren.</li><li><b>Ingen</b> – Skjemaet vil ikke be om noen informasjon i tillegg til ordrebekreftelses-IDen.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Legge til en ordreoppslagsmodul på en side

Ordreoppslagsmodulen kan legges til i hoveddelen av en hvilken som helst side på e-handelsområdet. Hvis du vil bruke ordreoppslagsmodulen til å aktivere ordreoppslag for gjestebetalinger, må du huske på å legge den til en side som ikke krever at brukeren er logget på. Hvis du vil finne **Krever pålogging?**-innstillingen for en side i trevisningen for Commerce-områdbyggeren, velger du **Standardside (obligatorisk)**-sporet, og ser nederst i høyre rute.

## <a name="additional-resources"></a>Tilleggsressurser

[Aktivere ordreoppslag for gjestebetalinger](order-lookup-guest.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
