--- 
title: "Endre og kjøre format for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.openlocfilehash: 76915a7294e078d76ed3ca9c41755e12b0791f3c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Endre og kjøre format for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 4: Kjøre format).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Endre formatet for å fylle ut vedlegg til generering av meldinger i binærformat
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Kundefakturamodell i treet.
3. Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.
5. Klikk Utforming.
    * Du skal fylle ut fakturameldingen i de genererte utdataene som en XML-fil ved hjelp av UNICODE-koding.  
6. Klikk Legg til rot for å åpne nedtrekksdialogen.
7. Velg Felles\Fil i treet.
8. I Navn-feltet skriver du inn XML-melding.
    * XML-melding  
9. I Koding-feltet skriver du inn UTF-8.
    * UTF-8  
10. Klikk OK.
    * Konfigurer de genererte utdataene som en zippet fil.  
11. Klikk Legg til rot for å åpne nedtrekksdialogen.
12. Velg Felles\Mappe i treet.
13. Skriv inn ZIP-utdata i Navn-feltet.
    * ZIP-utdata  
14. Klikk OK.
15. Velg ZIP-utdata i treet.
    * Legg til vedlegg i den zippede genereringsfilen som filer med opprinnelige navn og filtyper.  
16. Klikk Legg til for å åpne nedtrekksdialogen.
17. Velg Felles\Fil i treet.
18. Skriv inn Tilknyttet fil i Navn-feltet.
    * Tilknyttet fil  
19. Klikk OK.
20. Velg ZIP-utdata\Tilknyttet fil i treet.
21. Klikk Legg til for å åpne nedtrekksdialogen.
22. Velg Tekst\Base64 i treet.
23. Klikk OK.

## <a name="map-new-format-elements-to-data-model"></a>Tilordne nye formatelementer til datamodell
1. Klikk kategorien Tilordning.
2. Utvid noden 'model' i treet.
3. Utvid modell\Fakturavedlegg i treet.
4. Velg ZIP-utdata\Tilknyttet fil\Base64 i treet.
5. I treet velger du modell\Fakturavedlegg\Filinnhold.
6. Klikk Bind.
7. Velg ZIP-utdata\Tilknyttet fil i treet.
8. Klikk Rediger filnavn.
9. Utvid noden 'model' i treet.
10. Utvid modell\Fakturavedlegg i treet.
11. Velg modell\Fakturavedlegg\Filnavn i treet.
12. Klikk Legg til datakilde.
13. Klikk Lagre.
14. Lukk siden.
15. Velg modell\Fakturavedlegg i treet.
16. Klikk Bind.
17. Klikk Lagre.
18. Lukk siden.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Kjøre den utformede rapporten for den valgte fakturaen
1. Klikk Kjør.
2. Utvid delen Poster som skal inkluderes ().
3. Klikk Filter.
4. Merk raden for feltet Kundefakturajournal og Salgsordre.
5. I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.
    * 000148  
6. Klikk OK.
7. Klikk OK.
    * Se gjennom de genererte utdataene. Vær oppmerksom på at i tillegg til fakturameldingen i XML-format, er det opprettet en enkelt fil for hvert vedlegg. Vedleggsfilene fylles ut med de zippede utdataene i binærformat.  


