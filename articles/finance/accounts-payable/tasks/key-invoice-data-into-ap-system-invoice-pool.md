---
title: Registrere fakturadata i AP-systemet ved hjelp av fakturapulje
description: Denne artikkelen beskriver hvordan du bruker ankomstregistrering til å opprette fakturaer.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc3f1107a9564120aae77a75e6232879bf3c51af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858447"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Registrere fakturadata i AP-systemet ved hjelp av fakturapulje

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker ankomstregistrering til å opprette fakturaer. Bruk deretter fakturapuljen for å samsvare fakturaen med en bestilling og fullføre kostnaden på leverandørens fakturaside.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Bestillinger**.
2. Velg **Ny** for å opprette en bestilling.
3. I feltet **Leverandørkonto** velger du en leverandør fra rullegardinlisten. Velg for eksempel leverandør **1001**.
4. Velg **OK**.
5. Velg varenummeret for tjenesten i rullegardinlisten i **Varenummer**-feltet. Velg for eksempel **S0001**. Nettbeløpet er USD 75.00.  Dette er beløpet vi forventer å se på fakturaen.  
6. Velg **Innkjøp** i handlingsruten.
7. Velg **Bekreft**.

## <a name="create-and-post-and-invoice"></a>Opprette og postere en faktura
1. Gå til **Moduler > Leverandører > Fakturaer > Ankomstregistrering** i navigasjonsruten.
2. Velg **Ny**.
3. Åpne oppslaget for å velge navnet på ankomstregistreringen du vil bruke.
4. Velg navnet på ankomstregistreringen du vil bruke.
5. Velg **Linjer** for å åpne registeret og angi utgiftslinjer.
6. Velg en leverandør i oppslaget. Velg for eksempel leverandør **1001**.
7. I **Faktura**-feltet angir du fakturanummeret.
8. Skriv inn en verdi i **Beskrivelse**-feltet.
9. Angi et tall i **Kredit**-feltet.
10. I **Bestilling**-feltet åpner du rullegardinlisten for å velge bestillingen du opprettet tidligere.
11. Merk en godkjenner i rullegardinlisten i **Godkjent av**-feltet, og klikk på **Velg** for å velge denne godkjenneren.
12. Velg **Poster**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Åpne en faktura fra utvalget og sammenlign den med en bestilling for å fullføre fakturaprosessen
1. Gå til **Moduler > Leverandører > Fakturaer > Fakturapulje** i navigasjonsruten.
2. Velg **Bestilling** for å opprette en leverandørfaktura fra fakturaen i puljen.
3. Velg fakturaen du vil se gjennom.
4. Velg **Oppdater samsvarsstatus** for å fullføre samsvaret.
5. Velg **Alternativer** i handlingsruten.
6. Velg **Endre visning**.
7. Velg **Rutenettvisning**.
8. Velg **Poster**.
9. Lukk siden.
10. Gå til **Moduler > Leverandører > Leverandører > Leverandører** i navigasjonsruten.
11. Velg leverandøren som var på bestillingen. Velg for eksempel leverandør **1001**.
12. Velg **Leverandør** i handlingsruten.
13. Velg **Transaksjoner**.
14. Merk fakturaen som du opprettet. Ankomstregistreringsavsetningen ble tilbakeført og postert til den aktuelle kontoen for utgiften.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
