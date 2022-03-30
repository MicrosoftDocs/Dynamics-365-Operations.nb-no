---
title: Journalføre posterte journaloppføringer
description: Denne fremgangsmåten viser hvordan du journalfører posterte journaloppføringer.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400881"
---
# <a name="journalize-posted-journal-entries"></a>Journalfør posterte journaloppføringer

[!include [banner](../../includes/banner.md)]

Journalføringsprosessen i økonomimodulen brukes til å gruppere og rapportere posterte bilagsoppføringer for økonomimodulen. På grunnlag av kriteriene du oppgir, genererer behandlingen en liste over bilag som bruker en unik nummerserie, og som har verdien for **Journalnummer** i økonomimodulen som referanse.

Følg denne fremgangsmåten for å journalføre posterte journaloppføringer. Denne prosedyren bruker demonstrasjonsdatafirmaet **USMF**.

1. Gå til **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.
2. Velg en verdi i feltet **Utvidet finansjournal**. Hvis du velger **Ja**, blir rapportutdataene forskjellige.
3. Velg om perioden kan lukkes hvis journalføringsprosessen ikke har blitt kjørt. Hvis du velger **Ja**, kan ikke perioden lukkes før journalføringsprosessen er fullført for denne perioden.
4. Lukk siden.
5. Gå til **Økonomimodul** \> **Periodiske oppgaver** \> **Journalføring**, og velg **Filter**
6. Velg raden for filterkriteriene som du vil definere.
7. Angi eller velg filterkriteriene i **Kriterier**-feltet.
8. Velg **OK** for å lukke siden.
9. Velg **OK** for å starte journalføringsprosessen. En rapport blir generert når prosessen er fullført.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
