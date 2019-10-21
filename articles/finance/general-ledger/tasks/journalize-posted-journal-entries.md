---
title: Journalføre posterte journaloppføringer
description: Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e20229ca910aa0d7d820434c22edf5a27030bba5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175565"
---
# <a name="journalize-posted-journal-entries"></a>Journalføre posterte journaloppføringer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer. Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.

1. I **Navigasjonsrute** går du til **Moduler > Økonomimodul > Finansoppsett > Parametere for økonomimodul**.
2. Feltet **Utvidet finansjournal** kan settes til Ja eller Nei. Hvis Ja, blir rapportutdataene forskjellige.
3. Velg om perioden kan lukkes hvis journalføringsprosessen ikke har blitt kjørt. Hvis dette alternativet er satt til Ja, kan ikke perioden lukkes før journalføringsprosessen er fullført for denne perioden.  
4. Lukk siden.
5. Gå til **Moduler > Økonomimodul > Periodiske oppgaver > Journalføring** i **Navigasjonsruten**.
6. Klikk **Filter**.
7. Uthev raden med filterkriteriene som du vil definere.
8. Angi eller velg filterkriteriene i **Kriterier**-feltet.
9. Klikk på **OK** for å lukke filtersiden.
10. Klikk på **OK** for å starte journalføringsprosessen. En rapport blir generert når prosessen er fullført.  
