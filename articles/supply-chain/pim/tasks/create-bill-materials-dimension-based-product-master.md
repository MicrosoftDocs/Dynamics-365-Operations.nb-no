---
title: Opprette en stykkliste for en dimensjonsbasert produktstandard
description: For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820088"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Opprette en stykkliste for en dimensjonsbasert produktstandard

[!include [banner](../../includes/banner.md)]

For denne prosedyren skal du har fullført de 4 forrige veiledningene i disse trinnene med åtte registreringer. De 4 første registreringene definerer dataene som kreves for å fullføre denne prosedyren. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne oppgaven håndteres vanligvis av produktdesigneren.


## <a name="select-the-product"></a>Velg produkt
1. Klikk på Vedlikehold av frigitt produkt.
2. Klikk på Frigitte produkter.
3. Merk den valgte raden i listen.
    * Finn den frigitte produktstandarden med dimensjonsbasert konfigurasjonsteknologi, som du opprettet i den første oppgaveveiledningen i disse trinnene.  
4. Klikk på Utvikling i handlingsruten.
5. Klikk på Stykklisteversjon.

## <a name="create-new-bom-and-bom-version"></a>Opprette ny stykkliste og stykklisteversjon
1. Klikk på Ny.
2. Klikk på Stykkliste og stykklisteversjon.
3. Skriv inn en verdi i Navn-feltet.
    * Angi et område  
    * Vi angir ikke et bestemt område for stykklisten i denne prosedyren.  
4. Klikk på OK.
5. Klikk på Ny.
    * I denne fremgangsmåten skal vi legge til fire linjer i stykklisten. To linjer representerer kabelalternativer og to linjer representerer kabinettalternativer.  
6. Merk den valgte raden i listen.
7. Angi eller velg en verdi i Varenummer-feltet.
    * Velge varenummer A0001, HDMI 6' Kabler.  
8. Angi eller velg en verdi i feltet Konfigurasjonsgruppe.
    * Velg konfigurasjonsgruppen Kabel, som ble opprettet i veiledning 4 i disse trinnene.  
9. Klikk på Ny.
    * Velge varenummer A0002, HDMI 12' Kabler.  
10. Merk den valgte raden i listen.
11. Angi eller velg en verdi i Varenummer-feltet.
12. Angi eller velg en verdi i feltet Konfigurasjonsgruppe.
    * Velg konfigurasjonsgruppen Kabel.  
13. Klikk på Ny.
14. Merk den valgte raden i listen.
15. Angi eller velg en verdi i Varenummer-feltet.
    * Velge varenummer D0002 Kabinett.  
16. Angi eller velg en verdi i feltet Konfigurasjonsgruppe.
    * Velg konfigurasjonsgruppen Kabinett for denne stykklistelinjen.  
17. Klikk på Ny.
18. Merk den valgte raden i listen.
19. Angi eller velg en verdi i Varenummer-feltet.
    * Velg varenummer M0007 StandardCabinet som siste stykklistelinje.  
20. Angi eller velg en verdi i feltet Konfigurasjonsgruppe.
    * Velg konfigurasjonsgruppen Kabinett for den siste stykklistelinjen.  

## <a name="approve-and-activate"></a>Godkjenn og aktiver
1. Lukk siden.
2. Klikk på Godkjenn.
3. Angi eller velg en verdi i feltet Godkjent av.
4. Velg Ja i Vil du også godkjenne stykklisten? .
5. Klikk på OK.
6. Klikk på Aktiver.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]