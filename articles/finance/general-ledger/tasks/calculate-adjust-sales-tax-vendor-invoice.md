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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994721"
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

