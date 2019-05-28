---
title: Utligne en etterdatert sjekk fra en kunde
description: Du kan utligne en etterdatert sjekk etter at sjekken har blitt avregnet av banken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86cefaac99a1ce5aa777f4f62456c3248045cc27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566001"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Utligne en etterdatert sjekk fra en kunde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan utligne en etterdatert sjekk etter at sjekken har blitt avregnet av banken. Denne økonomiske transaksjonen avregner også mellomkontotransaksjonen for den etterdaterte sjekken. 

Følgende oppgaver må være fullført før du starter denne.

1) Definere etterdaterte sjekker

2) Registrere og postere en etterdatert sjekk for en kunde 



Rollen til denne oppgaveveiledningen er kasserer.



Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.

1. Gå til Kreditt og innkreving > Forespørsler og rapporter > Betalinger > Etterdaterte sjekker for kunde.
2. Klikk Utlign.
3. Klikk Utligne avregningsoppføringer.
    * Utlign kundekontoen for sjekktransaksjonen.  
4. Lukk siden.
5. Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.
6. Velg et alternativ i feltet Vis.
7. Merk eller fjern merket for Bare vis brukeropprettet.
8. Finn og velg ønsket post i listen.
9. Klikk Linjer.
10. Klikk Bilag.
11. Lukk siden.

