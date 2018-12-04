---
title: "Filformater for betalingsmåter"
description: "Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b6ee0ceb9d773ad1f510a5d192a7094a37061808
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="file-formats-for-methods-of-payment"></a>Filformater for betalingsmåter

[!include [banner](../includes/banner.md)]

Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter.

Det finnes to metoder du kan bruke til å få filformater for bruk med betalingsmåten, ER-filformater (elektronisk rapportering) eller et X ++-filformater. Når du setter opp en betalingsmåte for en kunde eller leverandør, angir du hvilke filformater og standarder som skal brukes for betalinger og hvordan betalinger vil bli behandlet. Du kan velge blant følgende typer formater:

-   Eksporter
-   Importer
-   Retur
-   Remittering

### <a name="method-1-electronic-reporting-file-formats"></a>Metode 1: formater for elektronisk rapportering

For filformater som er basert på ER-konfigurasjoner, må du importere konfigurasjonene fra Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md). Når du har importert rapporteringskonfigurasjoner for disse filformatene, kan du velge de importerte formatene på siden **Betalingsmåter**. Prosessen med å importere og velge filformater for Europa ligner på fremgangsmåten for Japan. Hvis du vil ha mer informasjon, se [Aktivere JBA-betalingsfilformatet](tasks/jba-payment-file-format.md)

### <a name="method-2-x-file-formats"></a>Metode 2: X++-filformater

For å velge filformatene som er basert på X++-kode, kan du fullføre trinnene nedenfor.

1.  Gå til siden **Betalingsmåter**.
2.  På **Filformater**-hurtigfanen klikker du **Oppsett**.
3.  Velg kategorien som samsvarer med filformattypen.
4.  Velg et filformat fra **Tilgjengelig**-listen og flytt det til **Valgt**-listen med pilkontrollen.
5.  Lukk siden **Filformater for betalingsmåter**.
6.  På **Filformater**-hurtigfanen velger du filformatet som skal brukes for betalingsmåten, fra det aktuelle filformatfeltet. Alternativene for generell elektronisk rapportering skal settes til **Ingen** for X++-filformater.





