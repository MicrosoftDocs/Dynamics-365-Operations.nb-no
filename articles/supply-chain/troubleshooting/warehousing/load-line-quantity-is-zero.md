---
title: Du kan ikke bekrefte en forsendelse fordi belastningslinjer er et antall på null
description: Du kan ikke bekrefte en forsendelse fordi belastningslinjer er et antall på null.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5dc5f8962ba37d21d7ef505fea940dc8767a9d9295588cb0e12e9eebe379a35c
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012199"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Du kan ikke bekrefte en forsendelse fordi belastningslinjer er et antall på null

Feilkode: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Alle linjene i belastningen %1 har antall null.  
> Kan ikke bekrefte forsendelsen for lasten %1.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Systemet evaluerer om belastningslinjen kan sendes bekreftet, basert på arbeids-ID-ene som er opprettet, belastningslinjeantallet og underleveringsprosenten. Hvis systemet finner ut at det ikke finnes noen arbeids-ID-er, og hvis underleveringsprosenten er satt til 100 prosent, kan du ikke bekrefte forsendelsen.

Dette problemet kan for eksempel oppstå hvis arbeidet er avbrutt og underleveringsprosenten på belastningslinjen er 100 prosent.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Gå gjennom lastlinjene for å kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.
- Se gjennom belastningslinjene for å være sikker på at underleveringsprosenten og antallet samkjøres med det plukkede arbeidet.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gå gjennom lastlinjene for å kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer

Bruk følgende fremgangsmåte til å gå gjennom lastlinjene for å kontrollere at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Åpne belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Legg merke til verdien i feltet **Antall for arbeid opprettet**.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.
1. Hvis du finner en uoverensstemmelse, avbryter du det relevante arbeidet, konfigurer lokasjonsdirektivet på nytt og frigir belastningen på nytt. For instruksjoner kan du se [Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket](picked-quantity-is-not-on-final.md).
1. Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Se gjennom belastningslinjene for å være sikker på at underleveringsprosenten og antallet samkjøres med det plukkede arbeidet

Bruk følgende fremgangsmåte til å se gjennom belastningslinjene for å være sikker på at underleveringsprosenten og antallet samkjøres med det plukkede arbeidet.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Åpne belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.
1. Juster verdien i **Underlevering**-feltet eller **Antall**-feltet etter behov.

> [!TIP]
> Hvis problemet fremdeles ikke er løst, kan det hende at du må fullføre mer plukkarbeid for de tilknyttede salgsordrene eller overføringsordrene til det tilgjengelige antallet er samkjørt med belastningen eller forsendelsen.
