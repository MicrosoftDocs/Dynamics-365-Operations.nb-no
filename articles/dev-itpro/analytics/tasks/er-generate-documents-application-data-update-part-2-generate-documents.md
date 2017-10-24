--- 
title: Generere dokumenter med oppdatering av programdata for elektronisk rapportering (ER)
description: "For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren \"ER generere dokumenter med oppdatering av programdata (del 1: importere konfigurasjoner)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: c724ce3c39ed7097a5a842b44a095628dcdfa131
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Generere dokumenter med oppdatering av programdata for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 1: importere konfigurasjoner)".



Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument. I denne prosedyren skal du kjøre den ER-importerte formatkonfigurasjonen som er opprettet for eksempelfirmaet Litware, Inc. for å generere elektroniske dokumenter.



Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet. 



Før du begynner, må du endre land konteksten for firmaets DEMF fra DEU (Tyskland) til BEL (Belgia). Klikk Organisasjonsadministrasjon > Organisasjoner > Juridiske enheter for å oppdatere landkoden i primæradressen for den juridiske enheten DEMF. Start programmet på nytt.


## <a name="run-imported-er-format"></a>Kjør importert ER-format
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid 'Intrastat (modell)' i treet.
3. Velg 'Intrastat (modell)\Intrastat (format)' i treet.
4. Klikk Kjør.
    * Kjør utkastversjonen av formatkonfigurasjonen ER å generere Intrastat-rapporten.  
5. Skriv inn 'intrastat.xml' i feltet Angi filnavn.
    * Angi navnet på filen.  
6. Klikk OK.
    * Se gjennom den genererte XML-filen.  
7. Lukk siden.
8. Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.
    * Åpmne dette skjemaet for å vise Intrastat-transaksjonene som er inkludert i det genererte elektroniske dokumentet.  
9. Klikk Intrastat-arkiv.
    * Fordi det utførte ER-fomatet ikke inneholder innstillinger for oppdatering av programdata, ble detaljer om den fullførte Intrastat-rapporten ikke arkivert.  
10. Lukk siden.
11. Lukk siden.


