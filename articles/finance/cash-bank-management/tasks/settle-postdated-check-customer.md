---
title: Utligne en etterdatert sjekk fra en kunde
description: Du kan utligne en etterdatert sjekk etter at sjekken har blitt avregnet av banken.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e61ac6d6785dd0383d5e5dcaca4cc55bf6deb52
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780022"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Utligne en etterdatert sjekk fra en kunde

[!include [banner](../../includes/banner.md)]

Du kan utligne en etterdatert sjekk etter at sjekken har blitt avregnet av banken. Denne økonomiske transaksjonen avregner også mellomkontotransaksjonen for den etterdaterte sjekken. 

Følgende oppgaver må være fullført før du starter denne.

1) Definere etterdaterte sjekker

2) Registrere og postere en etterdatert sjekk for en kunde 



Rollen til denne oppgaveveiledningen er kasserer.



Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.

1. Gå til **Kreditt og innkreving > Forespørsler og rapporter > Betalinger > Etterdaterte sjekker for kunde**.
2. Klikk **Utlign**.
3. Klikk **Utligne avregningsoppføringer**.
    * Utlign kundekontoen for sjekktransaksjonen.  
4. Lukk siden.
5. Gå til **Økonomimodul > Journaloppføringer > Økonomijournaler**.
6. Velg et alternativ i feltet **Vis**.
7. Merk eller fjern merket for **Bare vis brukeropprettet**.
8. Finn og velg ønsket post i listen.
9. Klikk **Linjer**.
10. Klikk på **Bilag**.
11. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
