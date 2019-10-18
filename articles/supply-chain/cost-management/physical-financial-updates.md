---
title: Fysiske og finansielle oppdateringer
description: Dette emnet gir en oversikt over hvilke typer transaksjoner som øker eller reduserer lagerantallet.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4360f9132d31c9d0038f51c68c1f6c3fcaaa2025
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250878"
---
# <a name="physical-and-financial-updates"></a>Fysiske og finansielle oppdateringer

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over hvilke typer transaksjoner som øker eller reduserer lagerantallet. 

Lagertransaksjoner kan oppdateres fysisk og finansielt i Dynamics 365 Supply Chain Management. Noen typer fysiske og finansielle transaksjoner øker lagerantallet, mens andre reduserer antallet.

## <a name="physical-increases"></a>Fysiske økninger
Når en fysisk transaksjon blir postert, er statusen til transaksjonsposten **Mottatt**. Følgende transaksjoner regnes som fysisk økning:

-   Bestillingsmottak
-   Retur av følgeseddel for salgsordre
-   Rapportere en produksjonsordre som avsluttet
-   Etter produkt på en produksjonsordreplukkliste

## <a name="financial-increases"></a>Finansiell økning
Når en finansiell tilgangstransaksjon blir postert, blir statusen til transaksjonsposten som øker antallet, satt til **Kjøpt**. Følgende transaksjoner regnes som finansiell økning:

-   Leverandørfaktura
-   Salgsordrefaktura for en retur
-   Produksjonsordrekostnad
-   Lagerjournaler med positivt antall, for eksempel bevegelse, resultat, opptelling, stykklister og overføring

## <a name="transactions-that-increase-quantity"></a>Transaksjoner som øker antallet
Transaksjoner som øker antallet posteres til løpende gjennomsnittlig kostpris. Beregnet løpende gjennomsnittlig kostpris basert på kostnaden til hver av disse transaksjonene for hver lagerdimensjon som spores økonomisk. Hvis du vil ha informasjon om løpende gjennomsnittlige kostpriser, se [Løpende gjennomsnittlig kostpris](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transaksjoner som reduserer antallet
Beregnet løpende gjennomsnitt for kostpris brukes når det posteres en transaksjon som reduserer antallet, uavhengig av lagermodellen som er tilknyttet den beholdningen. Transaksjonen som reduserer antallet, må ikke tidligere ha vært knyttet til en annen transaksjon før postering. Hvis den fysiske lagerbeholdningen blir negativ, brukes lagerkosten som er definert for varen på **Vare**-siden. 

> [!NOTE]
> Hvis multisite-funksjonalitet er aktivert, blir denne kostnaden i stedet den definerte lagerkostnaden som defineres for et område på siden **Standard ordreinnstillinger**.

## <a name="physical-issues-vs-financial-issues"></a>Fysisk avgang i forhold til økonomiske avganger
Når en fysisk avgangstransaksjon blir postert, er statusen til transaksjonsposten **Fratrukket**. Følgende transaksjoner regnes som fysisk avgang:

-   Plukklistejournal for produksjonsordre
-   Følgeseddel for salgsordre
-   Følgeseddel for bestillingsretur

Når en økonomisk transaksjon blir postert, er statusen til transaksjonsposten **Solgt**. Følgende transaksjoner regnes som økonomiske avganger:

-   Avslutte en produksjonsordre
-   Salgsordrefaktura
-   Leverandørfakturaretur
-   Lagerjournaler med negativt antall, for eksempel bevegelse, resultat, opptelling, stykklister og overføring

Transaksjoner som reduserer antallet posteres til løpende gjennomsnittlig kostpris. Prosedyren for lagerlukking er derfor nødvendig for å utligne avgangstransaksjoner mot tilgangstransaksjoner på grunnlag av lagermodellen som er tilordnet hver vare.
