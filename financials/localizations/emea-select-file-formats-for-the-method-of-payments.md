---
title: "Filformater for betalingsmåter"
description: "Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 54af22f1f2ec779bf947ae584a3ae09c20e6a364
ms.lasthandoff: 03/31/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Filformater for betalingsmåter

Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter.

Det finnes to metoder du kan bruke til å få filformater for bruk med betalingen, elektroniske filformater for rapportering (ER) eller et X ++-filformater. Når du setter opp en betalingsmåte for en kunde eller leverandør, angir du hvilke filformater og standarder som skal brukes for betalinger og hvordan betalinger vil bli behandlet. Du kan velge mellom følgende typer formater:

-   Eksporter
-   Importer
-   Retur
-   Remittering

### <a name="method-1-electronic-reporting-file-formats"></a>Metode 1: Elektronisk rapportering-filformater

Filformater som er basert på ER konfigurasjoner, må du importere konfigurasjonene fra Lifecycle tjenester (LCS). Hvis du vil ha mer informasjon, se [laste ned elektronisk rapportering konfigurasjoner fra levetidstjenester](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Når du har importert rapportering konfigurasjoner for de filformater, importerte formatene vil være tilgjengelig til å velge på den **betalingsmåter for** siden. Prosessen med å importere og velge filformatene for Europa ligner på fremgangsmåten for Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Metode 2: X ++-filformater

For å velge filformatene som er basert på X ++-kode, kan du fullføre trinnene nedenfor.

1.  Gå til den **betalingsmåter for** siden.
2.  På den **filformater** hurtigfanen, klikker du **Setup**.
3.  Velg kategorien som samsvarer med filtypen format.
4.  Velg et filformat fra den **tilgjengelig** og flytte den til den **merket** liste med pil-kontrollen.
5.  Lukk den **filformater for betalingsmåter for** siden.
6.  På den **filformater** hurtigfanen, velger du filformatet du bruker for betalingsmåte fra det aktuelle filen format-feltet. Generelt elektronisk rapporteringsalternativer bør settes til **ingen** for X ++-filformater.



