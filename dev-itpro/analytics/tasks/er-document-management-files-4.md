--- 
title: "Kjøre format for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)"
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6e1d7a54055829a1e9215a44f8eba346291f6717
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Kjøre format for å bruke dokumentbehandlingsfiler i formatutdata for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 3: Opprette format).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Legge til nødvendige vedlegg for salgsordre for én enkelt faktura
1. Gå til Kunder > Fakturaer > Åpne kundefakturaer.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Faktura-feltet med verdien CIV-000148.
    * CIV-000148  
3. Klikk for å følge koblingen for den valgte fakturaen.
    * CIV-000148  
4. Klikk for å følge koblingen i feltet Salgsordre.
    * 000148  
5. Velg alternativet Hode i feltet Linjer eller hode.
    * Velg toppteksten for å angi at dette vil være målet for å legge til vedlegg.  
6. Klikk Vedlegg.
    * Legg til noen filer som vedlegg for denne salgsordren. Bruk filene med dokumenttyper som støttes av dokumentbehandling (med filtypen DOCX, DPF, XML, JPG osv.). Bla gjennom og velg filer som skal legges ved og ytterligere behandles med den tilknyttede fakturaen i den elektroniske ER-meldingen.  
7. Klikk Ny.
8. Klikk Fil.
9. Klikk Ny.
10. Klikk Fil.
11. Lukk siden.
12. Lukk siden.
13. Lukk siden.
14. Lukk siden.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Kjøre den utformede rapporten for den valgte fakturaen
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Kundefakturamodell i treet.
3. Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.
5. Klikk Kjør.
6. Utvid delen Poster som skal inkluderes ().
7. Klikk Filter.
8. Merk raden for feltet Kundefakturajournal og Salgsordre.
9. Skriv inn 000148 i Kriterier-feltet.
    * I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.  
10. Klikk OK.
11. Klikk OK.
    * Se gjennom de genererte utdataene. Legg merke til at for hvert vedlegg er det opprettet en enkelt XML-node. Innholdet i vedlegget blir fylt ut i XML-utdataene i MIME (base64)-tekstformat.  


