---
title: Oppgradering av enkelt bilag og revaluering av valuta
description: "Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører. Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Oppgradering av enkelt bilag og revaluering av valuta

[!include[banner](../includes/banner.md)]


Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører. Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.

Bruk fremgangsmåten nedenfor når du oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.

1.  Kjør prosessene for revaluering av utenlandsk valuta for kunder og leverandører før du oppgraderer til Dynamics 365 for Operations. Sett **Metode**-feltet til **Fakturadato**. Det opprettes en revalueringstransaksjon som tilbakefører den siste revalueringen av utenlandsk valuta. De åpne transaksjonene verdsettes derfor etter sin opprinnelige regnskapsvaluta.
2.  Oppgrader til Dynamics 365 for Operations versjon 1611.
3.  Kjør prosessene for revaluering av utenlandsk valuta for leverandører og kunder på nytt. Denne gangen setter du **Metode**-feltet til **Standard**. Det opprettes en ny revalueringstransaksjon som er basert på gjeldende valutakurser. Denne transaksjonen registreres urealisert fortjeneste/tap og riktig finanskonto.





