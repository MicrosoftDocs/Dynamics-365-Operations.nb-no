---
title: Generere dokumenter som inneholder programdata
description: 'For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 4: endre format)".'
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2591f5b32417dd7517f76fc237d2337af64b3f61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745041"
---
# <a name="generate-documents-that-have-application-data"></a>Generere dokumenter som inneholder programdata

[!include [banner](../../includes/banner.md)]

For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 4: endre format)".



Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata. I denne prosedyren, kan du utføre ER-formatkonfigurasjonen for å generere Intrastat-rapporten og oppdatere programdata for arkivering detaljer om rapporteringsprosessen.



Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet. Før du begynner, kontroller at konteksten for firmaets DEMF land er BEL (Belgia).


## <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere
1. Gå til Avgift > Oppsett > Utenrikshandel > Utenrikshandelsparametere.
2. Klikk kategorien Nummerserier.

    Arkiverer detaljer om Intrastat-rapporteringsprosessen. Vi må identifisere poster i hvert arkiv vi har opprettet. En bestemt nummerserie må konfigureres for dette.  

3. Velg referansen "ID for Intrastat-arkiv".
4. Skriv inn en verdi i feltet Nummerserie.

    Angi eller velg verdien "Fore_2" i Nummerseriekode-feltet.  

5. ResolveChanges nummerseriekoden.
6. Klikk Lagre.
7. Lukk siden.

## <a name="run-modified-er-format"></a>Kjør modifisert ER-format
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid 'Intrastat (modell)' i treet.
3. Velg 'Intrastat (modell)\Intrastat (format)' i treet.
4. Klikk Kjør.
5. Skriv inn 'intrastat2.xml' i feltet Angi filnavn.
6. Klikk OK.

## <a name="review-er-format-executions-results"></a>Gå gjennom resultatene av kjøringen av ER-formatet
Se gjennom den genererte XML-filen.  
1. Lukk siden.
2. Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.

    Åpmne dette skjemaet med Intrastat-transaksjoner som er inkludert i det genererte elektroniske dokumentet.  

3. Klikk Intrastat-arkiv.

    Siden det utførte ER-formatet må inneholder innstillinger for oppdatering av programdata, ble detaljer om den fullførte Intrastat-rapporten arkivert. I dette skjemaet kan du se hovedposten for det opprettede arkivet.  

4. Klikk Detaljer.

    I dette skjemaet kan du se detaljene for det opprettede arkivet.  

5. Lukk siden.
6. Lukk siden.
7. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]