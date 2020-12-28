---
title: Rapportere en produksjonsordre som avsluttet
description: Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93193e6365bcf82fbbf93af81e2581a358899fa1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434101"
---
# <a name="report-a-production-order-as-finished"></a>Rapportere en produksjonsordre som avsluttet

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den sjette fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="report-a-production-order-as-finished"></a>Rapportere en produksjonsordre som avsluttet
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Startet.  
2. Klikk Produksjonsordre i handlingsruten.
3. Klikk Rapporter som fullført.
    * På denne siden kan du bekrefte antallet av det ferdige produktet som skal rapporteres som fullført.  
4. Klikk kategorien Generelt.
5. Angi Antall korrekte til "18".
6. Angi Antall feil til 2.
7. Velg "Materiale" i Feilårsak-feltet.
8. Merk av eller fjern merket i avmerkingsboksen Avslutt jobb.
9. Merk av eller fjern merket i boksen Godtar feil.
10. Klikk OK.

## <a name="verify-the-report-as-finished-journal"></a>Verifisere ferdigmeldingsjournalen
1. Klikk Vis i handlingsruten.
2. Klikk Ferdigmeldt.
3. Merk den valgte raden i listen.
4. Klikk koblingen i den valgte raden i listen.
    * Ferdigmeldingsjournalen er postert. Hvis du vil foreta justeringer i journalen, kan du manuelt opprette en ny journal der du kan gjøre endringer.  

