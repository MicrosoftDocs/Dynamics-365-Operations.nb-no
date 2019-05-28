---
title: Konfigurere sikkerhet for SQL Server Reporting Services for lokale distribusjoner
description: Dette emnet inneholder informasjon om hvordan du konfigurerer SQL Server Reporting Services (SSRS) for en lokal distribusjon.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 166d419f16866f699b96013222ce8da147a5ec21
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548725"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>Konfigurere sikkerhet for SQL Server Reporting Services for lokale distribusjoner

[!include [banner](../includes/banner.md)]

Bruk fremgangsmåten i dette emnet til å konfigurere SQL Server Reporting Services (SSRS) for din distribusjon av Microsoft Dynamics 365 for Finance and Operations (lokalt).

1. Åpne programmet Reporting Services Configuration Manager.
2. Lar standardnavnet **Servernavn** være, som skal være navnet på gjeldende datamaskin, og **Rapportserverforekomst**, **MSSQLSERVER**.
3. Klikk **Koble til**.

    [![Tilkobling til konfigurasjon av rapporteringstjenester](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Klikk kategorien **Tjenestekonto** og kontroller at innstillingene samsvarer med grafikken nedenfor.

    [![Kategorien Tjenestekonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Klikk kategorien **URL for webtjeneste** og kontroller at innstillingene samsvarer med grafikken nedenfor.

    [![Kategorien URL for webtjeneste](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Klikk kategorien **Database** og kontroller at **Databasenavn** og **Legitimasjonsinnstillinger** samsvarer med grafikken nedenfor.

    > [!NOTE]
    > Du må opprette en ny database. Dette gjør du ved å klikke **Endre Database** og deretter kontrollere at det nye databasenavnet er: **DynamicsAxReportServer**.

    [![Kategorien Database](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Klikk kategorien **URL for webportal** og kontroller at innstillingene samsvarer med grafikken nedenfor.

    > [!NOTE]
    > Du må klikke **Bruk** for å opprette og konfigurere portalen.

    [![Kategorien URL for webportal](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Når portalen er konfigurert, vil kategorien **Webportal** samsvarer med grafikken nedenfor.

    [![Kategorien webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Klikk URL-adressene for rapportene for å vise SQL Server Reporting Services-webportalen.
9. Når du er i portalenområdet, oppretter du en ny mappe kalt **Dynamics**.

    [![Dynamics-mappe](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. I **Reporting Services Configuration Manager** klikker du kategorien **E-postinnstillinger** og kontrollerer at innstillingene samsvarer med grafikken nedenfor.

    [![Kategorien E-postinnstillinger](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Klikk kategorien **Utførelseskonto** og kontroller at innstillingene samsvarer med grafikken nedenfor.

    [![Kategorien Utførelseskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Ikke endre standardinnstillingene i kategorien **Krypteringsnøkler**.

    [![Kategorien Krypteringsnøkler](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Klikk kategorien **Abonnementinnstillinger** og kontroller at innstillingene samsvarer med grafikken nedenfor.

    [![Kategorien Abonnementinnstillinger](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Ikke endre standardinnstillingene i kategorien **Skaler ut distribusjon**.

    [![Kategorien Skaler ut distribusjon](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Ikke endre standardinnstillingene i kategorien **Power BI-integrering**.

    [![Kategorien Power BI-integrering](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Klikk **Avslutt** for å lukke **Reporting Services Configuration Manager**.

    [![Lukke Rreporting Services Configuration Manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
