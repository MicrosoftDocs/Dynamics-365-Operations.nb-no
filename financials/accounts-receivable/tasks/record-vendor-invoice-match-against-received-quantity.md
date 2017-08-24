--- 
title: "Registrere leverandørfaktura og avstemme mot mottatt antall"
description: "Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 3b0ba3a29514351a89cf83f1ce7a3e147626e721
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Registrere leverandørfaktura og avstemme mot mottatt antall

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


