--- 
title: Registrere mottaket av varene i bestillingen
description: "Denne fremgangsmåten viser hvordan du registrerer mottak av varer direkte i en bestilling."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Registrere mottaket av varene i bestillingen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du registrerer mottak av varer direkte i en bestilling. Det er også mulig å registrere produktmottak i lageret, og deretter registrere det senere på bestillingen. Denne oppgaven gjøres vanligvis av en innkjøpsagent eller en leverandørkoordinator. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Eksemplet inneholder fremgangsmåte for å opprette en enkel bestilling, slik at du kan spille av prosedyren som en oppgaveveiledning. Hvis du bruker fremgangsmåten på dine egne data, begynner du med underoppgaven Registrere varemottak.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Klargjøre en ny bestilling for mottak av varer
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Angi US-101 i Leverandørkonto-feltet.
4. Klikk OK.
5. Angi M0001 i feltet Varenummer.
6. Angi 5 i Antall-feltet.
7. Klikk Kjøp i handlingsruten.
8. Klikk Bekreft.

## <a name="record-receipt-of-goods"></a>Registrere varemottak
1. Klikk Motta i handlingsruten.
2. Klikk Produktkvittering.
    * Antall-feltet lar deg velge forskjellige alternativer for antallet som du vil motta. Hvis et antall for eksempel er registrert på lageret tidligere, kan du velge Registrert antall.  I dette eksemplet bruker du verdien Bestilt antall.   
3. Skriv inn en verdi i Produktkvittering-feltet.
    * Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.  
4. Vis Linjer-delen.
5. Sett verdien for Antall til 4.
    * Her kan du fortsatt manuelt angi antallet som blir mottatt for hver linje i ordren.  
6. Skjul Linjer-delen.
7. Klikk OK.
    * Varene er nå registrert som mottatt i bestillingen, og en produktkvitteringsjournal er opprettet som dokument for å gjenspeile dette. Du kan bruke handlingen Produktmottak for å vise journaler som er opprettet med bestillingen, og se hva som er mottatt og når.  


