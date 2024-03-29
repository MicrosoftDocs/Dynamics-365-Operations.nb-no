---
title: Generere dokumenter som inneholder programdata
description: 'For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren ER generere dokumenter med oppdatering av programdata (del 4: endre format).'
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0f4fe5c948d1d6ea7c306a37d629c6e381dbd00
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290462"
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
