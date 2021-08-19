---
title: Du kan ikke bekrefte en forsendelse fordi det er null antall
description: Du kan ikke bekrefte en forsendelse fordi det er null antall
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712892"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Du kan ikke bekrefte en forsendelse fordi det er null antall

Feilkode: LoadLineOppdateringUpdatedToZero

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Belastningslinjen for varen %1 og forsendelsen %2 er oppdatert til å ha nullantall på grunn av underleveringsoppsett, noe som gjør at du ikke kan levere noen antall for denne varen.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Systemet evaluerer om det plukkede antallet er innenfor de forventede grensene, basert på plukket antall, belastningslinjeantall og underleveringsprosent. Hvis systemet finner ut at det plukkede antallet på belastningslinjen er 0 (null), kan du ikke bekrefte forsendelsen. Dette problemet kan for eksempel oppstå hvis arbeidet er avbrutt og underleveringsprosenten på belastningslinjen er 100 prosent.

## <a name="resolution"></a>Oppløsning

Kontroller belastningslinjene for å være sikker på at underleveringsprosenten og antallet samkjøres med det plukkede arbeidet.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.
1. Juster verdien i **Underlevering**-feltet eller **Antall**-feltet etter behov.

> [!TIP]
> Hvis problemet fremdeles ikke er løst, kan det hende at du må fullføre mer plukkarbeid for de tilknyttede salgsordrene eller overføringsordrene til det tilgjengelige antallet er samkjørt med belastningen eller forsendelsen.
