---
title: Nummerskilt må angis for denne lokasjonen
description: Hvis du får denne feilen når etter at du har opprettet en overføringsordre for et WMS-aktivert lager, er Standard mottakssted tomt for et transittlager.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477167"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Lisensiering av spesifikasjonsfeil ved bekreftelse av forsendelse for en overføringsordre

## <a name="symptoms"></a>Symptomer

Hvis du oppretter en overføringsordre ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og deretter prøver å bekrefte leveringen etter at arbeidet er fullført, kan du få følgende feilmelding:

> Nummerskilt må angis for denne lokasjonen.

## <a name="cause"></a>Årsak

Dette skjer fordi feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret.

## <a name="resolution"></a>Løsning

Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret. Kontroller at denne plasseringen er nummerskiltkontrollert.
