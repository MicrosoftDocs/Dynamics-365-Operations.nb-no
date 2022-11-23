---
title: Revider fakturaer og nøkkeldata i leverandørgjeld
description: Denne artikkelen viser hvordan du reviderer fakturaer og nøkkeldata i Leverandører.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4525534f906322c7fe4c232f0f6da5b308829087
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775222"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Revidere fakturaer og nøkkeldata i Leverandører

[!include [banner](../../includes/banner.md)]

Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. 

På siden **Leverandørparametere** kontrollerer du at alternativet **Aktiver validering av fakturakontroll** er valgt, at feltet **Poster faktura med avvik** er satt til **Krev godkjenning**, og at feltet **Linjekontrollpolicy** er satt til **Treveis samsvar**.

Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. Gå til **Alle bestillinger**.
2. Klikk **Ny**.
3. Angi en verdi i **Leverandørkonto**-feltet.
4. Klikk **OK**.
5. Klikk **Legg til linje**.
6. Skriv inn en verdi i **Varenummer**-feltet.
7. Klikk på **Innkjøp** i handlingsruten.
8. Klikk på **Bekreft**.

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
5. Klikk på **OK**.
6. Klikk på **Ja**.
7. Klikk på **Avstem produktkvitteringer**.
8. Klikk på **OK**.
9. Klikk på **Gå gjennom** i handlingsruten.
10. Klikk på **Samsvarende detaljer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
