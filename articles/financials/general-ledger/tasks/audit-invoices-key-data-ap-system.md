---
title: Revidere fakturaer og nøkkeldata i AP-system
description: Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568854"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a>Revidere fakturaer og nøkkeldata i AP-system

[!include [task guide banner](../../includes/task-guide-banner.md)]

Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt. 

På siden Leverandørparametere kontrollerer du at alternativet Aktiver validering av fakturakontroll er valgt, at feltet Poster faktura med avvik er satt til Krev godkjenning, og at Linjekontrollpolicy-feltet er satt til Treveis samsvar.

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

