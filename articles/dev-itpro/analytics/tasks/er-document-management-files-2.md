--- 
title: "Utvide datamodell for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f3d494cc83b273eef071b23d0948b283ba85c17e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Utvide datamodell for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER Bruke dokumentbehandlingsfiler i formatutdata (del 1: Klargjøre datamodell).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Utvide datamodellen for å presentere dokumentbehandlingsfilene i modellen
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Utvid Kundefakturamodell i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
5. Klikk Utforming.
6. Velg Kundefakturamodell(InvoiceCustomer) i treet.
    * Vi vil utvide denne datamodellen for å vise alle filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.  
7. Klikk Ny for å åpne nedtrekksdialogen.
8. Skriv inn Fakturavedlegg i Navn-feltet.
    * Fakturavedlegg  
9. Velg Postliste i Varetype-feltet.
10. Klikk Legg til.
11. Klikk Ny for å åpne nedtrekksdialogen.
12. Skriv inn Filinnhold i Navn-feltet.
    * Filinnhold  
13. Velg Container i Varetype-feltet.
14. Klikk Legg til.
15. Klikk Ny for å åpne nedtrekksdialogen.
16. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
17. Velg Streng i Varetype-feltet.
18. Klikk Legg til.

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Tilordne nye datamodellelementer til Dynamics 365 for Finance and Operations, Enterprise edition-datakilder
1. Klikk Tilordne modell til datakilde.
2. Bruk hurtigfilteret til å filtrere på Definisjon-feltet med en verdi lik InvoiceCustomer.
    * InvoiceCustomer  
    * Vi vil tilordne nye modellelementer til aktuelle datakilder.  
3. Klikk Utforming.
4. Velg Fakturavedlegg i treet.
5. Utvid Fakturavedlegg i treet.
6. Velg Fakturavedlegg\Filnavn i treet.
7. Klikk Rediger.
8. Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i Formel-feltet.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klikk Lagre.
10. Lukk siden.
11. I treet velger du Fakturavedlegg\Filinnhold.
12. Klikk Rediger.
13. Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i Formel-feltet.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Klikk Lagre.
15. Lukk siden.
16. Velg Fakturavedlegg i treet.
17. Klikk Rediger.
18. Skriv inn 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i Formel-feltet.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klikk Lagre.
20. Lukk siden.
21. Klikk Lagre.
22. Lukk siden.
23. Lukk siden.
24. Lukk siden.
25. Klikk Endre status.
26. Klikk Fullført.
27. Klikk OK.


