---
title: Registrere mottaket av varene i bestillingen
description: Denne artikkelen forklarer hvordan du registrerer mottak av varer direkte i en bestilling.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882467"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Registrere mottaket av varene i bestillingen

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan du registrerer mottak av varer direkte i en bestilling. Det er også mulig å registrere produktmottak i lageret, og deretter registrere det senere på bestillingen. Denne oppgaven gjøres vanligvis av en innkjøpsagent eller en leverandørkoordinator. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Eksemplet inneholder fremgangsmåte for å opprette en enkel bestilling, slik at du kan spille av prosedyren som en oppgaveveiledning. Hvis du bruker fremgangsmåten på dine egne data, begynner du med underoppgaven **Registrere varemottak**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Klargjøre en ny bestilling for mottak av varer
1. Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Bestillinger > Alle bestillinger**.
2. Velg **Ny**.
3. Angi `US-101` i **Leverandørkonto**-feltet.
4. Velg **OK**.
5. Angi `M0001` i feltet **Varenummer**.
6. I **Antall**-feltet angir du `5`.
7. Klikk på **Innkjøp** i handlingsruten.
8. Velg **Bekreft**.

## <a name="record-receipt-of-goods"></a>Registrere varemottak
1. Klikk på **Mottak** i handlingsruten.
2. Velg **Produktkvittering**. **Antall**-feltet lar deg velge forskjellige alternativer for antallet som du vil motta. Hvis et antall for eksempel er registrert på lageret tidligere, kan du velge **Registrert antall**. I dette eksemplet bruker du verdien **Bestilt antall**.
3. Utvid seksjonen **Oversikt**.
4. Skriv inn en verdi i **Produktkvittering**-feltet. Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.  
5. Vis **Linjer**-delen.
6. Sett verdien for **Antall** til 4. Her kan du fortsatt manuelt angi antallet som blir mottatt for hver linje i ordren.  
7. Velg **OK**. Varene er nå registrert som mottatt i bestillingen, og en produktkvitteringsjournal er opprettet som dokument for å gjenspeile dette. Du kan bruke handlingen Produktmottak for å vise journaler som er opprettet med bestillingen, og se hva som er mottatt og når.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]