---
title: Rapportere en produksjonsordre som avsluttet
description: Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9b676ffefa9fd4b8d66a5c35012630295f8a263
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828616"
---
# <a name="report-a-production-order-as-finished"></a>Rapportere en produksjonsordre som avsluttet

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den sjette fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="report-a-production-order-as-finished"></a>Rapportere en produksjonsordre som avsluttet
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Startet.  
2. Klikk på Produksjonsordre i handlingsruten.
3. Klikk på Rapporter som fullført.
    * På denne siden kan du bekrefte antallet av det ferdige produktet som skal rapporteres som fullført.  
4. Klikk på fanen Generelt.
5. Angi Antall korrekte til "18".
6. Angi Antall feil til 2.
7. Velg "Materiale" i Feilårsak-feltet.
8. Merk av eller fjern merket i avmerkingsboksen Avslutt jobb.
9. Merk av eller fjern merket i boksen Godtar feil.
10. Klikk på OK.

## <a name="verify-the-report-as-finished-journal"></a>Verifisere ferdigmeldingsjournalen
1. Klikk på Vis i handlingsruten.
2. Klikk på Ferdigmeldt.
3. Merk den valgte raden i listen.
4. Klikk på koblingen i den valgte raden i listen.
    * Ferdigmeldingsjournalen er postert. Hvis du vil foreta justeringer i journalen, kan du manuelt opprette en ny journal der du kan gjøre endringer.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]