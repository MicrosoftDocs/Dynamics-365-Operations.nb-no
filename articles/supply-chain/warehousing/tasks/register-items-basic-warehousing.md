---
title: Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst
description: Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.
author: Mirzaab
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76dd2bfd57db7dfd5c2baf59a864e59a509a64e0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577798"
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