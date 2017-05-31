---
title: "Filformater for betalingsmåter"
description: "Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262514
ms.assetid: 72ea2018-5a49-419c-93d0-755e5ff2722f
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b3cf1d469998389895c137fa842b73adb0eeddc
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Filformater for betalingsmåter

[!include[banner](../includes/banner.md)]


Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter.

Det finnes to metoder du kan bruke til å få filformater for bruk med betalingsmåten, ER-filformater (elektronisk rapportering) eller et X ++-filformater. Når du setter opp en betalingsmåte for en kunde eller leverandør, angir du hvilke filformater og standarder som skal brukes for betalinger og hvordan betalinger vil bli behandlet. Du kan velge blant følgende typer formater:

-   Eksporter
-   Importer
-   Retur
-   Remittering

### <a name="method-1-electronic-reporting-file-formats"></a>Metode 1: formater for elektronisk rapportering

For filformater som er basert på ER-konfigurasjoner, må du importere konfigurasjonene fra Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Når du har importert rapporteringskonfigurasjoner for disse filformatene, kan du velge de importerte formatene på siden **Betalingsmåter**. Prosessen med å importere og velge filformater for Europa ligner på fremgangsmåten for Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Metode 2: X++-filformater

For å velge filformatene som er basert på X++-kode, kan du fullføre trinnene nedenfor.

1.  Gå til siden **Betalingsmåter**.
2.  På **Filformater**-hurtigfanen klikker du **Oppsett**.
3.  Velg kategorien som samsvarer med filformattypen.
4.  Velg et filformat fra **Tilgjengelig**-listen og flytt det til **Valgt**-listen med pilkontrollen.
5.  Lukk siden **Filformater for betalingsmåter**.
6.  På **Filformater**-hurtigfanen velger du filformatet som skal brukes for betalingsmåten, fra det aktuelle filformatfeltet. Alternativene for generell elektronisk rapportering skal settes til **Ingen** for X++-filformater.





