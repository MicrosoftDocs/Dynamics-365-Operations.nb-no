--- 
title: Registrere varer for en vare for en grunnleggende lageraktivitet ved hjelp av en journal for vareankomst
description: "Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker \"grunnleggende lageraktiviteter\" i lagerstyringsmodulen."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registrere varer for en vare for en grunnleggende lageraktivitet ved hjelp av en journal for vareankomst

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen. Dette gjøres vanligvis av en mottaksassistent. Du kan kjøre denne prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises.  Hvis du ikke bruker USMF, må du ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen. Varen på linjen må lagres, og den må ikke bruke produktvarianter, og kan ikke ha sporingsdimensjoner. Og varene må være tilknyttet en lagringsdimensjonsgruppe der område og lager er aktive.


## <a name="create-item-arrival-journal-header"></a>Opprette et hode for vareankomstjournal
1. Gå til Lagerstyring > Loggoppføringer > Vareankomst > Vareankomst.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
    * Hvis du bruker USMF, kan du velge WHS. Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.  
4. Skriv inn en verdi i Følgeseddel-feltet.
    * Dette er følgeseddel-IDen fra følgeseddelen som er utstedt av leverandøren. Legg til et unikt nummer.  
5. Velg bestillingen i Nummer-feltet i Nummer-feltet.
6. Klikk OK.

## <a name="add-lines-to-item-arrival-journal"></a>Legge til linjer i journal for vareankomst
1. Klikk Funksjoner.
2. Klikk Opprett linjer.
    * Linjene kan angis manuelt i denne journalen, eller opprettes automatisk. Dette viser hvordan du oppretter dette automatisk.  
3. Merk av eller fjern merket i boksen Initialiser antall.
    * Dette vil initialisere antallet på journallinjene med antallet som ikke er registrert fra bestillingslinjen.  
4. Klikk OK.

## <a name="post-the-journal"></a>Poster journalen
1. Klikk Poster.
2. Klikk OK.

## <a name="generate-the-product-receipt"></a>Generere produktkvitteringen
1. Klikk Funksjoner.
2. Klikk Produktkvittering.
3. Klikk OK.


