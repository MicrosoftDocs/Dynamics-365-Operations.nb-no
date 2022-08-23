---
title: Registreringsside for kredittkort viser en feil i betalingsprosessen
description: Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når delen Betalingsmåte ikke er lastet inn og viser en feilmelding.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269762"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Registreringsside for kredittkort viser en feil i betalingsprosessen

[!include [banner](../../includes/banner.md)]

Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når delen **Betalingsmåte** ikke er lastet inn og viser en feilmelding.

## <a name="description"></a>beskrivelse

Når du åpner betalingssiden til en nettbutikk, blir ikke delen **Betalingsmåte** lastet og følgende feilmelding vises: "Noe gikk galt. Prøv på nytt senere."

![Feil i betalingsmodul.](media/payment-module-error.jpg)

## <a name="resolution"></a>Løsning

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Vent til bufferen for Commerce Scale Unit utløper

Betalingstjenesteinnstillingene på betalingssiden til den elektroniske butikken hurtigbufres på Commerce Scale Unit, og det kan ta opptil 15 minutter å vises på e-handelsområdet. Disse innstillingene for betalingstjenesten inkluderer endringer i forretningskonto-IDen, sky-API-nøkkelen og ulike konfigurasjonsinnstillinger som er knyttet til betalingsmåten.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en nettkanal](../channel-setup-online.md)
