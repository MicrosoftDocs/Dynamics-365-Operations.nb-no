---
title: Overføre aktuell beholdning på lageret
description: Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen.
author: yufeihuang
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf5a3711cfcd6e5a2ddce09af8569ea26c3502c8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580798"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Overføre aktuell beholdning på lageret

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom prosessen med å opprette og postere en lageroverføringsjournal for registrere flytting av en vare fra en lokasjon i et lager til en annen. Du må ha en lagerjournalnavn definert for lageroverføringer før du starter dette. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsdataselskapet USMF ved hjelp av eksempelverdiene som vises, eller du kan bruke dine egne data hvis du har produkter og lokasjoner definert. Disse oppgavene vil vanligvis utføres av en lageransatt.


## <a name="create-an-inventory-transfer-journal"></a>Opprette en beholdningsoverføringsjournal
1. I **navigasjonsruten** går du til **Beholdningsstyring > Journaloppføringer > Varer > Overføring**.
2. Klikk på **Ny**.
3. Angi eller velg en verdi i **Navn**-feltet.
4. Klikk på **OK**. Det er muligheten til å angi Fra- og Til-dimensjoner for hver journallinje. Disse er nødvendige for denne journaltypen. Du kan overføre varer til lokasjoner ved hjelp av andre regler. I dette eksemplet skal vi overføre en vare innenfor samme lager, fra en nummerskiltkontrollert lokasjon til en lokasjon som ikke er nummerskiltkontrollert.   

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Klikk på **Ny** i hurtigfanen **Journallinjer**.
2. Angi eller velg en verdi i **Varenummer**-feltet. Hvis du bruker USMF, kan du velge 'A0001'.  
3. Angi eller velg en verdi i feltet **Fra site**. Hvis du bruker USMF, kan du velge 2.  
4. Angi eller velg en verdi i feltet **Til site**. Hvis du bruker USMF, kan du velge 2.  
5. Angi eller velg en verdi i feltet **Fra lager**. Hvis du bruker USMF, kan du velge 24.  
6. Angi eller velg en verdi i feltet **Til lager**. Hvis du bruker USMF, kan du velge 24.  
7. Angi eller velg en verdi i **Fra lokasjon**-feltet. Hvis du bruker USMF, kan du velge FL-001.  
8. Angi eller velg en verdi i **Til lokasjon**-feltet. Hvis du bruker USMF, kan du velge BULK-001.  
9. Angi et tall i **Antall**-feltet.
10. Klikk på fanen **Lagerdimensjoner** i hurtigfanen **Linjedetaljer**.
11. Angi eller velg en verdi i **Nummerskilt**-feltet i **Fra lagerdimensjoner**. Hvis du bruker USMF, kan du velge 24.  
12. Klikk på **Lagre**.

## <a name="post-the-inventory-transfer-journal"></a>Postere beholdningsoverføringsjournalen
1. Klikk på **Poster** i **handlingsruten**.
2. Klikk på **OK**.

## <a name="view-inventory-transactions"></a>Vis lagertransaksjoner
1. Klikk på **Beholdning**.
2. Klikk på **Transaksjoner**. Her kan du se transaksjonene som ble opprettet da du posterte journalen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]