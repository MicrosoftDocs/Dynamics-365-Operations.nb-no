---
title: Konfigurere konsernintern prosjektfakturering
description: Dette emnet viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144285"
---
# <a name="configure-intercompany-project-invoicing"></a>Konfigurere konsernintern prosjektfakturering

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen. Denne oppgaven bruker USSI-datasettet.

1. Gå til **Moduler > Leverandører > Leverandører > Leverandører > Alle leverandører** i navigasjonsruten.
2. Finn og velg ønsket post i listen **Alle leverandører**.
3. Klikk på **Generelt** i handlingsruten.
4. Velg **Konsernintern**.
5. Angi **Aktiv** til **Ja** for å aktivere konsernintern handel.
6. Angi eller velg en verdi i **Kundefirma**-feltet.
7. Angi eller velg en verdi i **Min konto**-feltet.
8. Velg **Lagre**.
9. Lukk sidene for å gå tilbake til startsiden.
10. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Prosjektstyrings- og regnskapsparametere**.
11. Velg kategorien **Konsernintern**.
12. Flytt glidebryteren til **Ja** for å aktivere konsernintern ressursplanlegging og timeregistreringer.
13. Merk den valgte raden i listen.
14. Velg **Ny**.
15. Angi eller velg en verdi i feltet **Juridisk enhet som låner**.
16. Merk av for **Avsett inntekt**.
17. Angi eller velg en verdi i feltet **Standard timeregistreringskategori**.
18. Angi eller velg en verdi i feltet **Standard utgiftskategori**.
19. Velg **Lagre**.
20. Lukk siden.
21. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Postering > Finansposteringsoppsett**.
22. Velg et alternativ i feltet **Finanskontotyper**.
23. Velg **Ny**.
24. Angi de ønskede verdiene i **Hovedkonto**-feltet for den nye raden.
25. Velg **Lagre**.
26. Lukk siden.
27. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Overføringspris**.
28. Velg **Ny**.
29. Angi en dato i feltet **Gyldighetsdato**.
30. Angi eller velg en verdi i feltet **Juridisk enhet som låner**.
31. Velg et alternativ i feltet **Overføringsprismodell**.
32. Angi et tall i **Prissetting**-feltet.
33. Velg **Lagre**.

