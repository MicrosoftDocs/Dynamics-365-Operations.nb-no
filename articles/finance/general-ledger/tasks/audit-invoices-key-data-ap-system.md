---
title: Revidere fakturaer og nøkkeldata i Leverandører
description: Dette emnet viser hvordan du reviderer fakturaer og nøkkeldata i Leverandører.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6188b10327e4827cf5752fa56c3d491ef315b955
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204767"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Revidere fakturaer og nøkkeldata i Leverandører

[!include [banner](../../includes/banner.md)]

Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. 

På siden **Leverandørparametere** kontrollerer du at alternativet Aktiver validering av fakturakontroll er valgt, at feltet **Poster faktura med avvik** er satt til **Krev godkjenning**, og at feltet **Linjekontrollpolicy** er satt til **Treveis samsvar**.

Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. Gå til **Alle bestillinger**.
2. Klikk **Ny**.
3. Angi en verdi i **Leverandørkonto**-feltet.
4. Klikk **OK**.
5. Klikk **Legg til linje**.
6. Skriv inn en verdi i **Varenummer**-feltet.
7. Klikk **Innkjøp** i handlingsruten.
8. Klikk **Bekreft**.

## <a name="post-a-product-receipt"></a>Postere en produktkvittering
1. Klikk **Motta** i handlingsruten.
2. Klikk **Produktkvittering**.
3. Skriv inn en verdi i feltet **Produktkvittering**.
4. Klikk **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Registrere og samsvare en leverandørfakturaer med en produktkvittering
1. Klikk **Faktura** i handlingsruten.
2. Skriv inn en verdi i **Nummer**-feltet.
3. Klikk **Standard fra: Bestilt antall** for å åpne dialogboksen.
4. Velg et alternativ i feltet **Standardantall for linjer**.
5. Klikk **OK**.
6. Klikk **Ja**.
7. Klikk **Avstem produktkvitteringer**.
8. Klikk **OK**.
9. Klikk **Gå gjennom** i handlingsruten.
10. Klikk **Samsvarende detaljer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]