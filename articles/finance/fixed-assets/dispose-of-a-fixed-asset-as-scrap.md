---
title: Fjerne et anleggsmiddel som svinn
description: Emnet beskriver prosessen med å eliminere transaksjoner for et anleggsmiddel som er fjernet som svinn.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 371cc2efa64916698da8e4230825c3c949920698
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975250"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Fjerne et anleggsmiddel som svinn

[!include [banner](../includes/banner.md)]

Emnet beskriver prosessen med å eliminere transaksjoner for et anleggsmiddel som er fjernet som svinn. Transaksjonstypene som kan elimineres, omfatter transaksjoner for innkjøpsprisen og den akkumulerte avskrivningen for et aktivum og andre transaksjoner for anleggsmidler. Eliminering av disse transaksjonene påvirker balansekontoer, for eksempel kontoer for anskaffelse, justering, avskrivningsjustering, revaluering, oppskrivning og nedskrivning.

| Transaksjon                                         | Debet (Dr.) | Kredit (Kred.) |
|-----------------------------------------------------|-------------|--------------|
| Dr. akkumulert avskrivning                        | X           |              |
| Kred. resultat for anleggsmiddel                          |             | X            |
| Dr. resultat for anleggsmiddel                          | X           |              |
| Kred. konto for anskaffelse av anleggsmiddel                 |             | X            |
| Dr. resultat for anleggsmidler (netto bokført verdi \[NBV\]) | X           |              |
| Kred. resultat for anleggsmiddel (netto bokført verdi)                    |             | X            |

> [!NOTE]
> Vi anbefaler at du samarbeider tett med firmaets økonomisjef eller revisor for å identifisere de riktige kontoene som skal brukes for hver transaksjonstype, og også kontrollere at avhendingsprosessen og transaksjonene som genereres, oppdaterer disse kontoene på riktig måte.

Før du avhender et anleggsmiddel som svinn, må du opprette finanskontoer som er knyttet til anleggsmiddelets anskaffelsesverdi, avskrivning for inneværende år, avskrivning for tidligere år og netto bokført verdi for anleggsmiddelet. Transaksjonstypene for anleggsmiddel vises på siden **Posteringsprofil for anleggsmidler** . Gå til **Anleggsmidler \> Oppsett \> Posteringsprofiler for anleggsmidler** , and deretter velger du **Svinn** i feltet over rutenettet i hurtigfanen **Avhending** . Illustrasjonen nedenfor viser en liste over transaksjonstyper for anleggsmidler på siden **Posteringsprofiler for anleggsmidler** .


[![Avhende et anleggsmiddel som svinn, fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

I eksemplet nedenfor ble et anleggsmiddel anskaffet 1. januar 2018, og det blir kassert 31. mars 2019.

- **Anskaffelsespris** : 24 000,00 amerikanske dollar (USD)
- **Levetid** : To år
- **Avskrivningsmetode** : Lineær levetid
- **Avskrivningsbeløp** : 1 000,00 amerikanske dollar per måned

Netto bokført verdi for et anleggsmiddel beregnes med følgende formel:

Netto bokført verdi = anskaffelsespris – avskrivning

I dette eksemplet ble anleggsmiddelet anskaffet og avskrevet i 15 måneder, fra januar 2018 til mars 2019. Derfor er netto bokført verdi for anleggsmiddelet 9 000,00 USD (24 000,00 USD – 15 000,00 USD).

[![Eksempel på avskrivning av anleggsmiddel](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Hvis du vil opprette en avhendingsjournal, går du til **Anleggsmidler \> Journaloppføringer \> Anleggsmiddeljournal** og velger **Linjer** i handlingsruten. Velg **Avhending – svinn** , og velg deretter en ID for anleggsmiddel. Hvis du ikke avhende anleggsmiddelet fullstendig, angir du ikke en verdi i **Debet** - eller **Kredit** -feltet.

[![Anleggsmiddeljournal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Svinntransaksjonen for avhending av anleggsmidler endrer feltverdiene for anleggsmiddeltablået på følgende måter:

- I **Saldo** -delen oppdateres **Status** -feltet til **Kassert** .
- I **Avgang** -delen blir feltet **Avhendingsdato** satt til datoen da anleggsmiddelet ble kassert.

[![Detaljer i anleggsmiddeljournal](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Illustrasjonen nedenfor viser anleggsmiddelsaldoen.

[![Anleggsmiddelsaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Illustrasjonen nedenfor viser bilaget som er postert.

[![Netto bokført verdi](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)
