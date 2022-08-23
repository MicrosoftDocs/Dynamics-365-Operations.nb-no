---
title: ER Bruke dokumentbehandlingsfiler i formatutdata (del 4 – Kjøre format)
description: Denne artikkelen beskriver hvordan du konfigurerer et elektronisk rapporteringsformat slik at det bruker dokumentbehandlingsfiler i ER-utdata. (Del 4)
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
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
ms.openlocfilehash: 3d4e26d15ea287c99cac85bf383e09c15729d37a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290972"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>ER Bruke dokumentbehandlingsfiler i formatutdata (del 4 – Kjøre format)

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å bruke dokumentbehandlingsfiler (vedlegg) i ER-utdata. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke dokumentbehandlingsfiler i formatutdata (del 3: Opprette format).

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Legge til nødvendige vedlegg for salgsordre for én enkelt faktura
1. Gå til Kunder > Fakturaer > Åpne kundefakturaer.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Faktura-feltet med verdien CIV-000148.
    * CIV-000148  
3. Klikk på for å følge koblingen for den valgte fakturaen.
    * CIV-000148  
4. Klikk på for å følge koblingen i feltet Salgsordre.
    * 000148  
5. Velg alternativet Hode i feltet Linjer eller hode.
    * Velg toppteksten for å angi at dette vil være målet for å legge til vedlegg.  
6. Klikk på Vedlegg.
    * Legg til noen filer som vedlegg for denne salgsordren. Bruk filene med dokumenttyper som støttes av dokumentbehandling (med filtypen DOCX, DPF, XML, JPG osv.). Bla gjennom og velg filer som skal legges ved og ytterligere behandles med den tilknyttede fakturaen i den elektroniske ER-meldingen.  
7. Klikk på Ny.
8. Klikk på Fil.
9. Klikk på Ny.
10. Klikk på Fil.
11. Lukk siden.
12. Lukk siden.
13. Lukk siden.
14. Lukk siden.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Kjøre den utformede rapporten for den valgte fakturaen
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Kundefakturamodell i treet.
3. Utvid Kundefakturamodell\Kundefakturamodell (egendefinert) i treet.
4. Velg Kundefakturamodell\Kundefakturamodell (egendefinert)\Eksempelmelding for elektronisk faktura i treet.
5. Klikk på Kjør.
6. Utvid delen Poster som skal inkluderes ().
7. Klikk på Filter.
8. Merk raden for feltet Kundefakturajournal og Salgsordre.
9. Skriv inn 000148 i Kriterier-feltet.
    * I kriteriefeltet Salgsordre skriver du inn ordrenummeret 000148.  
10. Klikk på OK.
11. Klikk på OK.
    * Se gjennom de genererte utdataene. Legg merke til at for hvert vedlegg er det opprettet en enkelt XML-node. Innholdet i vedlegget blir fylt ut i XML-utdataene i MIME (base64)-tekstformat.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
