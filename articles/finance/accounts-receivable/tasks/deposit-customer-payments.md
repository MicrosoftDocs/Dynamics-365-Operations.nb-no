---
title: Innbetale kundebetalinger
description: Betale inn kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140193"
---
# <a name="deposit-customer-payments"></a>Innbetale kundebetalinger

[!include [banner](../../includes/banner.md)]

Betale inn kundebetalinger. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Moduler > Kunder > Betalinger > Betalingsjournal** i navigasjonsruten.
2. Velg **Ny**.
3. I **Navn**-feltet velger du **CustPay** i rullegardinmenyen.
4. Velg **Linjer**.
5. Velg kunden du registrerer betalingen for, i **Konto**-feltet.
6. Angi betalingsbeløpet i **Kredit**-feltet. Du kan velge å la beløpet stå tomt, og la programmet beregne det ved å velge fakturaene som ble betalt.  
7. Skriv inn en verdi i **Betalingsreferanse**-feltet. Betalingsreferansen kan være sjekknummeret for betalingen du angir. Betalingsreferansen er nødvendig hvis du skal inkludere betalingen på et betalingsbilag.  
8. Merk av for Bruk et betalingsbilag. Hvis betalingen skal inkluderes i innbetalingen, kan du endre denne innstillingen til Ja.  
9. Velg **Ny**.
10. Velg kunden for den neste betalingen i **Konto**-feltet.
11. Angi betalingsbeløpet i **Kredit**-feltet.
12. Skriv inn en verdi i **Betalingsreferanse**-feltet.
13. Merk av for **Bruk et betalingsbilag**.
14. Velg **Poster**. Betalinger må være postert før betalingsbilaget kan genereres. Dette sikrer at betalingene ikke endres etter at betalingsbilaget er generert.  
15. Velg **Funksjoner**.
16. Velg **Betalingsbilag**.
17. Velg **OK**. Den første siden brukes til å opprette betalingsbilaget.  
18. Velg **OK**. Det andre trinnet er å skrive ut betalingsbilaget, men dette trinnet er ikke nødvendig.  

