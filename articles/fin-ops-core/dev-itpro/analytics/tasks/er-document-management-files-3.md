---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 3 – Opprette format)
description: Denne artikkelen beskriver hvordan du konfigurerer et elektronisk rapporteringsformat slik at det bruker dokumentbehandlingsfiler i ER-utdata. (Del 3)
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
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: b70f5ed74fd701be79daebbd2a8f246a0a0ab95e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290942"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER Bruke dokumentbehandlingsfiler i formatutdata (del 3 – Opprette format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i alle firmaer.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 2: Utvide datamodell).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="create-a-format-to-process-invoices"></a>Opprette et format for å behandle fakturaer
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk på Rapporteringskonfigurasjoner.
3. Utvid Kundefakturamodell i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
    * Du vil opprette et format for å generere elektroniske meldinger med informasjon om filer som er knyttet til en salgsordre som er relatert til en faktura for elektronisk behandling.  
5. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
6. I feltet Ny angir du Format basert på datamodellen Kundefakturamodell (egendefinert).
7. I Navn-feltet skriver du inn Eksempelmelding for elektronisk faktura.
    * Eksempelmelding for elektronisk faktura  
8. Angi eller velg en verdi i feltet Definisjon av datamodell.
    * InvoiceCustomer  
9. Klikk på Opprett konfigurasjon.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Utforme et format for å fylle ut vedlegg til generering av en melding i MIME-format
1. Klikk på Utforming.
2. Klikk på Legg til rot for å åpne nedtrekksdialogen.
3. Velg XML\Element i treet.
4. I Navn-feltet skriver du inn Faktura.
    * Faktura  
5. Klikk på OK.
6. Klikk på Legg til for å åpne nedtrekksdialogen.
7. Velg XML\Attributt i treet.
8. Skriv inn Salgsordre i Navn-feltet.
    * Salgsordre  
9. Klikk på OK.
10. Klikk på Legg til attributt.
11. Skriv inn Fakturanummer i Navn-feltet.
    * Fakturanummer  
12. Klikk på OK.
13. Klikk på Legg til attributt.
14. Skriv inn Fakturabeløp i Navn-feltet.
    * Fakturabeløp  
15. Klikk på OK.
16. Klikk på Legg til for å åpne nedtrekksdialogen.
17. Velg XML\Element i treet.
18. I Navn-feltet skriver du inn Vedlagte dokumenter.
    * Vedlagte dokumenter  
19. Klikk på OK.
20. Velg Faktura\Vedlagte dokumenter i treet.
21. Klikk på Legg til element.
22. I Navn-feltet skriver du inn Dokument.
    * Dokument  
23. Klikk på OK.
24. Velg Faktura\Vedlagte dokumenter\Dokument i treet.
25. Klikk på Legg til for å åpne nedtrekksdialogen.
26. Velg XML\Attributt i treet.
27. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
28. Klikk på OK.
29. Klikk på Legg til for å åpne nedtrekksdialogen.
30. Velg XML\Element i treet.
31. Skriv inn Filinnhold i Navn-feltet.
    * Filinnhold  
32. Klikk på OK.
33. Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold i treet.
34. Klikk på Legg til for å åpne nedtrekksdialogen.
35. Velg Tekst\Base64 i treet.
36. Klikk på OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Tilordne formatelementer til datamodell som datakilde
1. Velg Faktura\Salgsordre i treet.
2. Klikk på fanen Tilordning.
3. Utvid noden 'model' i treet.
4. Velg modell\Salgsordrenummer(SalesId) i treet.
5. Klikk på Bind.
6. Velg Faktura\Fakturanummer i treet.
7. Utvid modell\Grunnlagsfaktura(InvoiceBase) i treet.
8. Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturanummer(Id) i treet.
9. Klikk på Bind.
10. Velg Faktura\Fakturabeløp i treet.
11. Velg modell\Grunnlagsfaktura(InvoiceBase)\Fakturabeløp(Amount) i treet.
12. Klikk på Bind.
13. Utvid modell\Fakturavedlegg i treet.
14. I treet velger du modell\Fakturavedlegg\Filinnhold.
15. Velg Faktura\Vedlagte dokumenter\Dokument\Filinnhold\Base64 i treet.
16. Klikk på Bind.
17. Velg modell\Fakturavedlegg\Filnavn i treet.
18. Velg Faktura\Vedlagte dokumenter\Dokument\Filnavn i treet.
19. Klikk på Bind.
20. Velg modell\Fakturavedlegg i treet.
21. Velg Faktura\Vedlagte dokumenter\Dokument i treet.
22. Klikk på Bind.
23. Klikk på Lagre.
24. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
