---
title: Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst
description: Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3edf84135e675b6259972327f80c9b6a91821139
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254173"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen. Dette gjøres vanligvis av en mottaksassistent. Du kan kjøre denne prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises.  Hvis du ikke bruker USMF, må du ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen. Varen på linjen må være lagerført. Og varene må være tilknyttet en lagringsdimensjonsgruppe der område og lager er aktive.


## <a name="create-item-arrival-journal-header"></a>Opprette et hode for vareankomstjournal
1. Gå til Lagerstyring > Loggoppføringer > Vareankomst > Vareankomst.
2. Klikk på Ny.
3. Skriv inn en verdi i Navn-feltet.
    * Hvis du bruker USMF, kan du velge WHS. Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.  
4. Skriv inn en verdi i Følgeseddel-feltet.
    * Dette er følgeseddel-IDen fra følgeseddelen som er utstedt av leverandøren. Legg til et unikt nummer.  
5. Velg bestillingen i Nummer-feltet i Nummer-feltet.
6. Klikk på OK.

## <a name="add-lines-to-item-arrival-journal"></a>Legge til linjer i journal for vareankomst
1. Klikk på Funksjoner.
2. Klikk på Opprett linjer.
    * Linjene kan angis manuelt i denne journalen, eller opprettes automatisk. Dette viser hvordan du oppretter dette automatisk.  
3. Merk av eller fjern merket i boksen Initialiser antall.
    * Dette vil initialisere antallet på journallinjene med antallet som ikke er registrert fra bestillingslinjen.  
4. Klikk på OK.

## <a name="post-the-journal"></a>Poster journalen
1. Klikk på Poster.
2. Klikk på OK.

## <a name="generate-the-product-receipt"></a>Generere produktkvitteringen
1. Klikk på Funksjoner.
2. Klikk på Produktkvittering.
3. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]