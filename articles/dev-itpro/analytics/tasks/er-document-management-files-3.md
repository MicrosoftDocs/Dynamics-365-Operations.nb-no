--- 
title: Opprette format for bruk av dokumentbehandlingsfiler i formatutdata
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6d5df842dbbf89f5df72c63919fc0bcbf811a09c
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-format-to-use-document-management-files-in-format-outputs"></a>Opprette format for bruk av dokumentbehandlingsfiler i formatutdata

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 2: Utvide datamodell).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="create-a-format-to-process-invoices"></a>Opprette et format for å behandle fakturaer
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Utvid Kundefakturamodell i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
    * Du vil opprette et format for å generere elektroniske meldinger med informasjon om filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.  
5. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
6. I feltet Ny angir du Format basert på datamodellen Kundefakturamodell (egendefinert).
7. I Navn-feltet skriver du inn Eksempelmelding for elektronisk faktura.
    * Eksempelmelding for elektronisk faktura  
8. Angi eller velg en verdi i feltet Definisjon av datamodell.
    * InvoiceCustomer  
9. Klikk Opprett konfigurasjon.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Utforme et format for å fylle ut vedlegg til generering av en melding i MIME-format
1. Klikk Utforming.
2. Klikk Legg til rot for å åpne nedtrekksdialogen.
3. Velg XML\Element i treet.
4. I Navn-feltet skriver du inn Faktura.
    * Faktura  
5. Klikk OK.
6. Klikk Legg til for å åpne nedtrekksdialogen.
7. Velg XML\Attributt i treet.
8. Skriv inn Salgsordre i Navn-feltet.
    * Salgsordre  
9. Klikk OK.
10. Klikk Legg til attributt.
11. Skriv inn Fakturanummer i Navn-feltet.
    * Fakturanummer  
12. Klikk OK.
13. Klikk Legg til attributt.
14. Skriv inn Fakturabeløp i Navn-feltet.
    * Fakturabeløp  
15. Klikk OK.
16. Klikk Legg til for å åpne nedtrekksdialogen.
17. Velg XML\Element i treet.
18. I Navn-feltet skriver du inn Vedlagte dokumenter.
    * Vedlagte dokumenter  
19. Klikk OK.
20. Velg Faktura\Vedlagte dokumenter i treet.
21. Klikk Legg til element.
22. I Navn-feltet skriver du inn Dokument.
    * Dokument  
23. Klikk OK.
24. Velg Faktura\Vedlagte dokumenter\Dokument i treet.
25. Klikk Legg til for å åpne nedtrekksdialogen.
26. Velg XML\Attributt i treet.
27. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
28. Klikk OK.
29. Klikk Legg til for å åpne nedtrekksdialogen.
30. Velg XML\Element i treet.
31. Skriv inn Filinnhold i Navn-feltet.
    * Filinnhold  
32. Klikk OK.
33. Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold i treet.
34. Klikk Legg til for å åpne nedtrekksdialogen.
35. Velg Tekst\Base64 i treet.
36. Klikk OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Tilordne formatelementer til datamodell som datakilde
1. Velg Faktura\Salgsordre i treet.
2. Klikk kategorien Tilordning.
3. Utvid noden 'model' i treet.
4. Velg modell\Salgsordrenummer(SalesId) i treet.
5. Klikk Bind.
6. Velg Faktura\Fakturanummer i treet.
7. Utvid modell\Grunnlagsfaktura(InvoiceBase) i treet.
8. Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturanummer(Id) i treet.
9. Klikk Bind.
10. Velg Faktura\Fakturabeløp i treet.
11. Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturabeløp(Amount) i treet.
12. Klikk Bind.
13. Utvid modell\Fakturavedlegg i treet.
14. I treet velger du modell\Fakturavedlegg\Filinnhold.
15. Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold\Base64 i treet.
16. Klikk Bind.
17. Velg modell\Fakturavedlegg\Filnavn i treet.
18. Velg Faktura\Vedlagte dokumenter\Dokument\Filnavn i treet.
19. Klikk Bind.
20. Velg modell\Fakturavedlegg i treet.
21. Velg Faktura\Vedlagte dokumenter\Dokument i treet.
22. Klikk Bind.
23. Klikk Lagre.
24. Lukk siden.


