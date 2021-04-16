---
title: Journalføre posterte journaloppføringer
description: Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.
author: aprilolson
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5028db1db2359a54d565fc299c9a3353a4cf8297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826160"
---
# <a name="journalize-posted-journal-entries"></a>Journalføre posterte journaloppføringer

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]