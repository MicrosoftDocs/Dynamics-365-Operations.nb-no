---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 2 - Utvide datamodell)
description: Dette artikkelen beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det bruker dokumentbehandlingsfiler (vedlegg) i ER-utdata. (Del 2)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 9d0d87d23bcdf537d638502fb5217f32fd1b328e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291002"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>ER Bruke dokumentbehandlingsfiler i formatutdata (del 2 - Utvide datamodell)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER Bruke dokumentbehandlingsfiler i formatutdata (del 1: Klargjøre datamodell).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Utvide datamodellen for å presentere dokumentbehandlingsfilene i modellen
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk på Rapporteringskonfigurasjoner.
3. Utvid Kundefakturamodell i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
5. Klikk på Utforming.
6. Velg Kundefakturamodell(InvoiceCustomer) i treet.
    * Vi vil utvide denne datamodellen for å vise alle filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.  
7. Klikk på Ny for å åpne nedtrekksdialogen.
8. Skriv inn Fakturavedlegg i Navn-feltet.
    * Fakturavedlegg  
9. Velg Postliste i Varetype-feltet.
10. Klikk på Legg til.
11. Klikk på Ny for å åpne nedtrekksdialogen.
12. Skriv inn Filinnhold i Navn-feltet.
    * Filinnhold  
13. Velg Container i Varetype-feltet.
14. Klikk på Legg til.
15. Klikk på Ny for å åpne nedtrekksdialogen.
16. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
17. Velg Streng i Varetype-feltet.
18. Klikk på Legg til.

## <a name="map-new-data-model-elements-to-data-sources"></a>Tilordne nye datamodellelementer til datakilder
1. Klikk på Tilordne modell til datakilde.
2. Bruk hurtigfilteret til å filtrere på Definisjon-feltet med en verdi lik InvoiceCustomer.
    * InvoiceCustomer  
    * Vi vil tilordne nye modellelementer til aktuelle datakilder.  
3. Klikk på Utforming.
4. Velg Fakturavedlegg i treet.
5. Utvid Fakturavedlegg i treet.
6. Velg Fakturavedlegg\Filnavn i treet.
7. Klikk på Rediger.
8. Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i Formel-feltet.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klikk på Lagre.
10. Lukk siden.
11. I treet velger du Fakturavedlegg\Filinnhold.
12. Klikk på Rediger.
13. Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i Formel-feltet.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Klikk på Lagre.
15. Lukk siden.
16. Velg Fakturavedlegg i treet.
17. Klikk på Rediger.
18. Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i Formel-feltet.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klikk på Lagre.
20. Lukk siden.
21. Klikk på Lagre.
22. Lukk siden.
23. Lukk siden.
24. Lukk siden.
25. Klikk på Endre status.
26. Klikk på Fullført.
27. Klikk på OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
