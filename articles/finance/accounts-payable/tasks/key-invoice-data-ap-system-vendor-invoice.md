---
title: Hovedfakturadata i AP ved hjelp av en leverandørfaktura
description: Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).
author: abruer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ad75439bf3dfa1ed33e35fa9cfee153012e9f60
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716810"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Hovedfakturadata i AP ved hjelp av en leverandørfaktura

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen hjelper deg med å opprette en leverandørfaktura fra en bestilling og vise resultatene av å samsvare bestillingen, kvitteringen og fakturaen (treveis kontroll).


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Alle bestillinger**.
2. Klikk på **Ny**.
3. Klikk rullegardinknappen i **Leverandørkonto**-feltet for å åpne oppslaget.
4. Finn en leverandør å velge. Bla for eksempel ned til USA – 104.
5. Velg leverandør USA – 104.
6. Klikk **OK**.
7. Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.
8. Velg en lagervare. Velg for eksempel varenummer 1000.
9. Utvid hurtigfanen **Linjedetaljer**.
10. Klikk på kategorien **Oppsett**. Du kan overstyre kontrollpolicyen for å bruke ingen kontroll, toveis kontroll eller treveis kontroll.  
11. Klikk **Innkjøp** i handlingsruten.
12. Klikk **Bekreft**.

## <a name="receive-the-products"></a>Motta produktene
1. Klikk **Motta** i handlingsruten.
2. Klikk **Produktkvittering**.
3. I feltet **Produktkvittering** angir du produktkvitteringsnummeret. Skriv for eksempel inn PR123.
4. Klikk på **OK** for å postere produktkvitteringen.
5. Lukk siden.

## <a name="create-a-vendor-invoice"></a>Opprette en leverandørfaktura
1. I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Bestillinger er mottatt, men ikke fakturert**.
2. Velg bestillingen du opprettet.
3. Klikk på **Faktura** i handlingsruten.
4. Klikk på **Faktura**.
5. I feltet **Nummer** angir du fakturanummeret.
6. Skriv inn en verdi i feltet **Fakturabeskrivelse**.
7. Angi en dato i **Fakturadato**-feltet.
8. Angi 1200 i **Enhetspris**-feltet.
9. Klikk **Legg til linje**.
10. Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget.
11. Finn varenummeret for installasjonstillegget i listen. For eksempel S0001
12. Velg varenummeret for installasjonstillegget. Legg merke til at det ikke er utført kontroll etter at du har gjort endringene.  
13. Klikk på **Oppdater samsvarsstatus**.
14. Klikk **Gå gjennom** i handlingsruten.
15. Klikk **Samsvarende detaljer**. Den nye linjen med tjenester trenger ikke kontrolleres, så statusen forblir "Ikke utført".  
16. Velg produktkvitteringen for lagervaren du har mottatt. Linjen med produktkvitteringen ble samsvart, men det er ikke samsvar mellom antall eller pris, slik at den mislykkes.  
17. Angi et tall i **Enhetspris**-feltet. Nå som salgsprisen samsvarer, oppdateres statusen til Bestått. Hvis policyen tillater avvik, eller hvis samsvar bare er en advarsel, kan du fortsatt postere fakturaen.  
18. Lukk siden.
19. Klikk **Poster**.
20. Lukk skjemaet. Legg merke til at bestillingen ikke lenger er oppført som mottatt, men ikke fakturert.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
