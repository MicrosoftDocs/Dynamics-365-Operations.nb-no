---
title: Beregne og justere merverdiavgift på en leverandørfaktura
description: Dette emnet forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139973"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Beregne og justere merverdiavgift på en leverandørfaktura

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura. Hvis det opprinnelige kildedokumentet viser forskjellige mva-beløp som er beregnet, kan du justere disse beløpene før postering. Denne oppgaven bruker demonstrasjonsfirmaet DEMF.

1. Gå til **Moduler > Leverandører > Fakturaer > Fakturajournal** i navigasjonsruten.
2. Velg **Ny**.
3. I **Navn**-feltet i den nye raden velger du et alternativ fra rullegardinmenyen.
4. Velg **Linjer** i handlingsruten.
5. Angi de ønskede verdiene i **Konto**-feltet.
6. Skriv inn en verdi i **Faktura**-feltet.
7. Angi et tall i **Kredit**-feltet.
8. Angi ønskede verdier i **Motkonto**-feltet.
9. Velg **Merverdiavgift**.
10. Angi et tall i feltet **Totalt faktisk mva-beløp**.
11. Mva-beløp kan justeres per mva-kode i kategorien **Justering**.
12. Velg **Tilbakestill faktiske fra beregnede beløp**.
13. Velg **OK**.
14. Velg **Lagre**.

