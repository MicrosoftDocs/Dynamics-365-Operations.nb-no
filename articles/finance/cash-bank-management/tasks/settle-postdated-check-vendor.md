---
title: Utligne en etterdatert sjekk for en leverandør
description: Utlign en etterdatert sjekk som er utstedt til en leverandør, når banken har avregnet sjekktransaksjonen etter at sjekken er forfalt og avregnet av banken.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e3816a2f1c95d568a173cb07daad0473703da9c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779508"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Utligne en etterdatert sjekk for en leverandør

[!include [banner](../../includes/banner.md)]

Utlign en etterdatert sjekk som er utstedt til en leverandør, når banken har avregnet sjekktransaksjonen etter at sjekken er forfalt og avregnet av banken. 

Fullfør den følgende prosedyren før du starter en ny.

1) Definere etterdaterte sjekker

2) Registrere og postere en etterdatert sjekk for en leverandør



Rollen til denne prosedyren er kasserer. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.

1. Gå til **Leverandører > Betalinger > Etterdaterte sjekker for leverandør**.
2. Klikk **Utlign**.
3. Klikk **Utligne avregningsoppføringer**.
    * Utlign leverandørkontoen for sjekktransaksjonen.  
4. Lukk siden.
5. Gå til **Økonomimodul > Journaloppføringer > Økonomijournaler**.
6. Velg **Alle** i **Vis**-feltet.
7. Merk eller fjern merket for **Bare vis brukeropprettet**.
8. Merk den valgte raden i listen.
9. Klikk **Linjer**.
10. Klikk på **Bilag**.
11. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
