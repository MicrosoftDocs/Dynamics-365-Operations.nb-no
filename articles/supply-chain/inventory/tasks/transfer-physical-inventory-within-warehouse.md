---
title: "Overføre aktuell beholdning på lageret"
description: "Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedb209ab111ed1fb6281fda2f4dea345e0905ef
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Overføre aktuell beholdning på lageret

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen. Du må ha en lagerjournalnavn definert for lageroverføringer før du starter dette. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsdataselskapet USMF ved hjelp av eksempelverdiene som vises, eller du kan bruke dine egne data hvis du har produkter og lokasjoner definert. Disse oppgavene vil vanligvis utføres av en lageransatt.


## <a name="create-an-inventory-transfer-journal"></a>Opprette en beholdningsoverføringsjournal
1. Gå til Overføring.
2. Klikk Ny.
3. Angi eller velg en verdi i Navn-feltet.
4. Klikk OK.
    * Det er muligheten til å angi Fra- og Til-dimensjoner for hver journallinje. Disse er nødvendige for denne journaltypen. Du kan overføre varer til lokasjoner ved hjelp av andre regler. I dette eksemplet skal vi overføre en vare innenfor samme lager, fra en nummerskiltkontrollert lokasjon til en lokasjon som ikke er nummerskiltkontrollert.   

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk Ny.
2. Angi eller velg en verdi i Varenummer-feltet.
    * Hvis du bruker USMF, kan du velge 'A0001'.  
3. Angi eller velg en verdi i feltet Fra site.
    * Hvis du bruker USMF, kan du velge 2.  
4. Angi eller velg en verdi i feltet Til site.
    * Hvis du bruker USMF, kan du velge 2.  
5. Angi eller velg en verdi i feltet Fra lager.
    * Hvis du bruker USMF, kan du velge 24.  
6. Angi eller velg en verdi i feltet Til lager.
    * Hvis du bruker USMF, kan du velge 24.  
7. Angi eller velg en verdi i Fra lokasjon-feltet.
    * Hvis du bruker USMF, kan du velge FL-001.  
8. Angi eller velg en verdi i Til lokasjon-feltet.
    * Hvis du bruker USMF, kan du velge BULK-001.  
9. Angi et tall i feltet Antall.
10. Klikk kategorien Lagerdimensjoner.
11. Angi eller velg en verdi i feltet Nummerskilt.
    * Hvis du bruker USMF, kan du velge 24.  
12. Klikk Lagre.

## <a name="post-the-inventory-transfer-journal"></a>Postere beholdningsoverføringsjournalen
1. Klikk Poster.
2. Klikk OK.

## <a name="view-inventory-transactions"></a>Vis lagertransaksjoner
1. Klikk Lager.
2. Klikk Transaksjoner.
    * Her kan du se transaksjonene som ble opprettet da du posterte journalen.  
