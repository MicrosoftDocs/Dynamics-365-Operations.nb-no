---
title: Utforme konfigurasjoner for å generere dokumenter med programdata
description: Denne artikkelen beskriver hvordan du utformer konfigurasjoner for elektronisk rapportering (ER) for å generere et elektronisk dokument. (Del 1 – importere konfigurasjoner).
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
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290552"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Utforme konfigurasjoner for å generere dokumenter med programdata

[!include [banner](../../includes/banner.md)]

For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 1: importere konfigurasjoner)".



Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument. I denne prosedyren skal du kjøre den ER-importerte formatkonfigurasjonen som er opprettet for eksempelfirmaet Litware, Inc. for å generere elektroniske dokumenter.



Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet. 



Før du begynner, må du endre land konteksten for firmaets DEMF fra DEU (Tyskland) til BEL (Belgia). Klikk på Organisasjonsadministrasjon > Organisasjoner > Juridiske enheter for å oppdatere landkoden i primæradressen for den juridiske enheten DEMF. Start programmet på nytt.


## <a name="run-imported-er-format"></a>Kjør importert ER-format
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid 'Intrastat (modell)' i treet.
3. Velg 'Intrastat (modell)\Intrastat (format)' i treet.
4. Klikk på Kjør.
    * Kjør utkastversjonen av formatkonfigurasjonen ER å generere Intrastat-rapporten.  
5. Skriv inn 'intrastat.xml' i feltet Angi filnavn.
    * Angi navnet på filen.  
6. Klikk på OK.
    * Se gjennom den genererte XML-filen.  
7. Lukk siden.
8. Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.
    * Åpmne dette skjemaet for å vise Intrastat-transaksjonene som er inkludert i det genererte elektroniske dokumentet.  
9. Klikk på Intrastat-arkiv.
    * Fordi det utførte ER-fomatet ikke inneholder innstillinger for oppdatering av programdata, ble detaljer om den fullførte Intrastat-rapporten ikke arkivert.  
10. Lukk siden.
11. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
