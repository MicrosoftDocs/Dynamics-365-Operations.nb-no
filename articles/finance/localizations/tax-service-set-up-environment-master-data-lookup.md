---
title: Konfigurer et miljø for hoveddataoppslag
description: Dette emnet beskriver hvordan du konfigurerer miljøet for å bruke oppslagsfunksjonen for hoveddata i avgiftsberegning.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869088"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Konfigurer et miljø for hoveddataoppslag

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du konfigurerer miljøet for å bruke oppslagsfunksjonen for hoveddata i avgiftsberegning.

1. Konfigurer Power Platform-integrering i Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Microsoft Power Platform-integrering – oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Konfigurer Dynamics 365 Finance og Microsoft Dataverse. Hvis du vil ha mer informasjon, kan du se [Skaffe løsningen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Godkjenning og autorisasjon](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Importer *forutsetning for avgiftstjenesteløsningen for virtuelle enheter* fra [virtuell enhet for avgiftstjeneste](https://go.microsoft.com/fwlink/?linkid=2158160).
4. Konfigurer Dynamics 365 Regulatory Configuration Service (RCS). 
5. Opprett en serviceforespørsel for at Microsoft skal kunne aktivere testversjonering av følgende funksjoner:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. I Finance går du til arbeidsområdet **Funksjonsstyring** og aktiverer følgende funksjoner:

      - (Forhåndsversjon) Støtte for Dataverse-datakilder for elektronisk rapportering
      - (Forhåndsversjon) Støtte for Dataverse-datakilder for avgiftstjeneste
      - (Forhåndsvisning) Globaliseringsfunksjoner

5. Logg på RCS ved å bruke en leieradministratorkonto.
6. Gå til **Elektronisk rapportering** > **Tilkoblede programmer**. 
7. Velg **Ny** for å legge til en oppføring, og angi følgende feltinformasjon. 

   - Angi et navn i **Navn**-feltet.
   - I **Type**-feltet velger du **Dataverse**.
   - I **Program**-feltet angir du URL-adressen for Dataverse.
   - I **Leier**-feltet angir du leieren.
   - I feltet **Egendefinert URL-adresse** angir du URL-adressen for Dataverse og legger til "/api/data/v9.1" etter den.

8. Velg **Kontroller tilkobling**, og fullfør tilkoblingsprosessen. 

   [![Kontroller tilkobling-knappen](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Gå til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**, og importer avgiftskonfigurasjoner fra [Avgiftskonfigurasjoner](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Agiftskonfigurasjoner-siden, Avgiftsdatamodell-treet](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Gå til **Tilordning av modell for avgiftsbelagt dokument** eller til **Tilordning av Dataverse-modell** hvis du bruker en Microsoft-konfigurasjon,. og velg deretter oppføringen du opprettet i trinn 7, i feltet **Tilkoblet program**.
11. Sett **Standardalternativ for modelltilordning** til **Ja**.

   [![Modelltilordning-siden](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
