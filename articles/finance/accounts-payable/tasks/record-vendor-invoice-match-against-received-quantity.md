---
title: Registrere leverandørfaktura og avstemme mot mottatt antall
description: Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778684"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Registrere leverandørfaktura og avstemme mot mottatt antall

[!include [banner](../../includes/banner.md)]

Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. 

På siden **Leverandørparametere** kontrollerer du at alternativet **Aktiver validering av fakturakontroll** er valgt, at feltet **Poster faktura med avvik** er satt til **Krev godkjenning**, og at feltet **Linjekontrollpolicy** er satt til **Treveis samsvar**.

Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. Gå til **Alle bestillinger**.
2. Klikk på **Ny**.
3. Klikk på rullegardinknappen i **Leverandørkonto**-feltet for å åpne oppslaget.
4. Angi en verdi i **Leverandørkonto**-feltet.
5. Klikk på **OK**.
6. Klikk på **Legg til linje**.
7. Skriv inn en verdi i **Varenummer**-feltet.
8. Klikk på **Innkjøp** i handlingsruten.
9. Klikk på **Bekreft**.

## <a name="post-a-product-receipt"></a>Postere en produktkvittering
1. Klikk på **Motta** i handlingsruten.
2. Klikk på **Produktkvittering**.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i feltet **Produktkvittering**.
5. Klikk på **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Registrere og samsvare en leverandørfakturaer med en produktkvittering
1. Klikk på **Faktura** i handlingsruten.
2. Klikk på **Faktura**.
3. Skriv inn en verdi i **Nummer**-feltet.
4. Klikk på **Standard fra: Bestilt antall** for å åpne dialogboksen.
5. Velg et alternativ i feltet **Standardantall for linjer**.
6. Klikk på **OK**.
7. Klikk på **Ja**.
8. Klikk på **Avstem produktkvitteringer**.
9. Klikk på **OK**.
10. Klikk på **Gå gjennom** i handlingsruten.
11. Klikk på **Samsvarende detaljer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
