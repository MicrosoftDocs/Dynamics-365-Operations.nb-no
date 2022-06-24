---
title: Beregne og justere merverdiavgift på en leverandørfaktura
description: Denne artikkelen forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura i Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868380"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Beregne og justere merverdiavgift på en leverandørfaktura

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura. Hvis det opprinnelige kildedokumentet viser forskjellige mva-beløp som er beregnet, kan du justere disse beløpene før postering. Denne oppgaven bruker demonstrasjonsfirmaet DEMF.

1. Gå til **Leverandører > Fakturaer > Fakturajournal**.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
