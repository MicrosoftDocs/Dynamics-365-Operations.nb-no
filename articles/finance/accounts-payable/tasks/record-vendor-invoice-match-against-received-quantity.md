---
title: Registrere leverandørfaktura og avstemme mot mottatt antall
description: Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 352e188dcd25b486a1284be6958f44a5543f222c358153557366f9bdcc209f05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722917"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Registrere leverandørfaktura og avstemme mot mottatt antall

[!include [banner](../../includes/banner.md)]

Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. 

På siden Leverandørparametere kontrollerer du at alternativet Aktiver validering av fakturakontroll er valgt, at feltet Poster faktura med avvik er satt til Krev godkjenning, og at Linjekontrollpolicy-feltet er satt til Treveis samsvar.

Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. Gå til Alle bestillinger.
2. Klikk Ny.
3. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
4. Angi en verdi i Leverandørkonto-feltet.
5. Klikk OK.
6. Klikk Legg til linje.
7. Skriv inn en verdi i Varenummer-feltet.
8. Klikk Kjøp i handlingsruten.
9. Klikk Bekreft.

## <a name="post-a-product-receipt"></a>Postere en produktkvittering
1. Klikk Motta i handlingsruten.
2. Klikk Produktkvittering.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i feltet Produktkvittering.
5. Klikk OK.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Registrere og samsvare en leverandørfakturaer med en produktkvittering
1. Klikk Faktura i handlingsruten.
2. Klikk Faktura.
3. Skriv inn en verdi i Nummer-feltet.
4. Klikk Standard fra: Bestilt antall for å åpne dialogboksen.
5. Velg et alternativ i feltet Standardantall for linjer.
6. Klikk OK.
7. Klikk Ja.
8. Klikk Avstem produktkvitteringer.
9. Klikk OK.
10. Klikk Gå gjennom i handlingsruten.
11. Klikk Samsvarende detaljer.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]