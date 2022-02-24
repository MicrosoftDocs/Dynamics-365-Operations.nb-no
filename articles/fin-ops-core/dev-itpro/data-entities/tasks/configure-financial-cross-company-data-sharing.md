---
title: Konfigurere økonomisk datadeling mellom firmaer
description: Denne fremgangsmåten viser hvordan du konfigurerer, aktiverer, validerer og løser konflikter ved deling av data mellom firmaer.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aeb9e85d3263d78a8412bd3c300dae8bb1d840ef
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685199"
---
# <a name="configure-financial-cross-company-data-sharing"></a>Konfigurere økonomisk datadeling mellom firmaer

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du konfigurerer, aktiverer, validerer og løser konflikter ved deling av data mellom firmaer. Den bruker USMF-firmaet og malen for deling av økonomiske data.

Denne oppgaveveiledningen krever Dynamics AX-plattform 7.1 eller nyere.

1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Arbeidsområder > Databehandling**.
2. Klikk **Importer**.
3. Skriv inn en verdi i **Navn**-feltet.
4. Velg pakketype i feltet **Kildedataformat**. Klikk **Last opp**. Gå til plasseringen til malpakkefilen for deling av økonomiske data, og velg filen.
5. Klikk **Lagre**.
6. Merk den valgte raden i listen. Velg datadelingspolicyen som nettopp ble opprettet.  
7. Klikk **Importer**.
8. Klikk **Lukk**.
9. Oppdater siden.
10. Lukk siden.
11. Lukk siden.
12. Lukk siden.
13. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Oppsett > Konfigurer datadeling mellom firmaer**.
14. Finn og velg **Betalingsdager** i listen.
15. Klikk **Legg til**.
16. Merk den valgte raden i listen.
17. Skriv inn USSI i feltet **Firma**.
18. Klikk **Legg til**.
19. Skriv inn USMF i feltet **Firma**.
20. Klikk **Lagre**.
21. Klikk på **Aktiver**.
22. Klikk **Ja**.
23. Klikk på **Finn delingsproblemer**.
24. Klikk **Ja**.
25. Klikk på **Oppdater feltverdi**.
26. Klikk på **Bruk verdi fra firma 1**.
27. Oppdater siden.
28. Lukk siden.

