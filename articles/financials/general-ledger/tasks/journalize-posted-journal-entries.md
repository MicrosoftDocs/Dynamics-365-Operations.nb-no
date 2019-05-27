---
title: Journalføre posterte journaloppføringer
description: Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547916"
---
# <a name="journalize-posted-journal-entries"></a>Journalføre posterte journaloppføringer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer. Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.

1. Valider innstillingene for journalføring under Økonomimodul > Finansoppsett > Parametere for økonomimodul.
2. Feltet Utvidet finansjournal kan settes til Ja eller Nei. Hvis Ja, blir rapportutdataene forskjellige.
3. Velg om perioden kan lukkes hvis journalføringsprosessen ikke har blitt kjørt.
    * Hvis dette alternativet er satt til Ja, kan ikke perioden lukkes før journalføringsprosessen er fullført for denne perioden.  
4. Lukk siden.
5. Gå til Økonomimodul > Periodiske oppgaver > Journalføring.
6. Klikk Filter.
7. Uthev raden med filterkriteriene som du vil definere.
8. Angi eller velg filterkriteriene i Kriterier-feltet.
9. Klikk OK for å lukke filtersiden.
10. Klikk OK for å starte journalføringsprosessen.
    * En rapport blir generert når prosessen er fullført.  

