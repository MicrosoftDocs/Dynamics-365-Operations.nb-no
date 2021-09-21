---
title: Dimensjonslokasjon kan ikke være tom hvis serienummer er angitt
description: Hvis du får denne feilen når du bekrefter en forsendelse etter at du har opprettet en overføringsordre for en serievare, er feltet Standard mottakssted tomt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477236"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Feil ved bekreftelse av forsendelse etter oppretting av en overføringsordre for en serievare

## <a name="symptoms"></a>Symptomer

Hvis du oppretter en overføringsordre for en serievare ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og etter at arbeidet er fullført, prøver du å bekrefte forsendelsen, får du følgende feilmelding:

> Dimensjonslokasjon kan ikke være tom hvis dimensjonsserienummer er angitt.

## <a name="cause"></a>Årsak

Dette skjer fordi feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret.

## <a name="resolution"></a>Løsning

Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret. Kontroller at denne plasseringen er nummerskiltkontrollert.
