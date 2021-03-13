---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 5 - Endre og kjøre format)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det bruker dokumentbehandlingsfiler (vedlegg) i ER-utdata. (Del 5)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092494"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER Bruke dokumentbehandlingsfiler i formatutdata (del 5 - Endre og kjøre format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 4: Kjøre format).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Endre formatet for å fylle ut vedlegg til generering av meldinger i binærformat
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Kundefakturamodell i treet.
3. Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.
5. Klikk på Utforming.
    * Du skal fylle ut fakturameldingen i de genererte utdataene som en XML-fil ved hjelp av UNICODE-koding.  
6. Klikk på Legg til rot for å åpne nedtrekksdialogen.
7. Velg Felles\Fil i treet.
8. I Navn-feltet skriver du inn XML-melding.
    * XML-melding  
9. I Koding-feltet skriver du inn UTF-8.
    * UTF-8  
10. Klikk på OK.
    * Konfigurer de genererte utdataene som en zippet fil.  
11. Klikk på Legg til rot for å åpne nedtrekksdialogen.
12. Velg Felles\Mappe i treet.
13. Skriv inn ZIP-utdata i Navn-feltet.
    * ZIP-utdata  
14. Klikk på OK.
15. Velg ZIP-utdata i treet.
    * Legg til vedlegg i den zippede genereringsfilen som filer med opprinnelige navn og filtyper.  
16. Klikk på Legg til for å åpne nedtrekksdialogen.
17. Velg Felles\Fil i treet.
18. Skriv inn Tilknyttet fil i Navn-feltet.
    * Tilknyttet fil  
19. Klikk på OK.
20. Velg ZIP-utdata\Tilknyttet fil i treet.
21. Klikk på Legg til for å åpne nedtrekksdialogen.
22. Velg Tekst\Base64 i treet.
23. Klikk på OK.

## <a name="map-new-format-elements-to-data-model"></a>Tilordne nye formatelementer til datamodell
1. Klikk på fanen Tilordning.
2. Utvid noden 'model' i treet.
3. Utvid modell\Fakturavedlegg i treet.
4. Velg ZIP-utdata\Tilknyttet fil\Base64 i treet.
5. I treet velger du modell\Fakturavedlegg\Filinnhold.
6. Klikk på Bind.
7. Velg ZIP-utdata\Tilknyttet fil i treet.
8. Klikk på Rediger filnavn.
9. Utvid noden 'model' i treet.
10. Utvid modell\Fakturavedlegg i treet.
11. Velg modell\Fakturavedlegg\Filnavn i treet.
12. Klikk på Legg til datakilde.
13. Klikk på Lagre.
14. Lukk siden.
15. Velg modell\Fakturavedlegg i treet.
16. Klikk på Bind.
17. Klikk på Lagre.
18. Lukk siden.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Kjøre den utformede rapporten for den valgte fakturaen
1. Klikk på Kjør.
2. Utvid delen Poster som skal inkluderes ().
3. Klikk på Filter.
4. Merk raden for feltet Kundefakturajournal og Salgsordre.
5. I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.
    * 000148  
6. Klikk på OK.
7. Klikk på OK.
    * Se gjennom de genererte utdataene. Vær oppmerksom på at i tillegg til fakturameldingen i XML-format, er det opprettet en enkelt fil for hvert vedlegg. Vedleggsfilene fylles ut med de zippede utdataene i binærformat.  

