--- 
title: "Importere konfigurasjoner for å generere dokumenter med programdata"
description: "For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren \"ER Opprette en konfigurasjonsleverandør og merke den som aktiv\"."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 1637ba59525f5f8bd9fe41a00c34eca90f7a2751
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Importere konfigurasjoner for å generere dokumenter med programdata

[!include [task guide banner](../../includes/task-guide-banner.md)]

For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv".

Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument. I denne prosedyren må du importere de nødvendige ER-konfigurasjonene som er opprettet for eksempelfirmaet, Litware, Inc, og bruke dem til å generere elektroniske dokumenter. Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet. Før du begynner, last ned og lagre filene som er oppført i Hjelpemnet, «Generer elektroniske dokumenter og oppdater programdata med ER-verktøy» (generate-electronic-documents-update-application-data/). Filene er XML for Intrastat (modell), Intrastat (tilordning) XML og XML for Intrastat (format).

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
    * Trinnene i denne fremgangsmåten viser hvordan du bruker ER-funksjoner til å fullføre en oppdatering av programdata og hvordan du genererer en Intrastat-rapporten. Detaljer om rapporteringsprosessen arkiveres i tabellene programmet. For øyeblikket når rapporteringsprosessen Intrastat er aktivert i Intrastat-skjemaet, gjøres arkivering avhengig av hvordan programmert i eksisterende kildekoden. Du vil konfigurere en lignende ennå forenklet logikken i programmet data ved hjelp av bare ER rammeverket i denne prosedyren. Ingen endringer gjøres til kildekoden.   

## <a name="import-er-configurations"></a>Importere ER-konfigurasjoner
1. Klikk Rapporteringskonfigurasjoner.
2. Klikk Veksle.
3. Klikk Last fra XML-fil.
    * Import ER-modellkonfigurasjonen som inneholder datamodellen som skal brukes som datakilde for å generere Intrastat-rapporten. Du vil senere utvide denne modellen datadefinisjon for å bruke den for en oppdatering av programdata skal arkiveres detaljer om Intrastat rapportering prosessen.   
    * Klikk Bla gjennom og velg Intrastat (modell) XML-filen.  
4. Klikk OK.
5. Velg 'Intrastat (modell)' i treet.
6. Klikk Utforming.
7. Utvid 'For utgående dokument' i treet.
8. Utvid 'For utgående dokument\Transaksjoner' i treet.
    * Se gjennom strutkren i den importerte datamodellen. Vær oppmerksom på at rotelementet "For utgående dokument" er definert til å angi dataflyten for å hente data fra programmet og bruker den som en datakilde til å generere Intrastat-rapporten. 'Transaksjonene (postliste)' brukes til å vise listen over Intrastat-transaksjoner som må rapporteres. Fordi du vil arkivere rapporterte varekoder, trengs det den unike IDen for en enkelt varekode "Varekoden rec-id (Int64)" i denne dataflyten.   
9. Lukk siden.
10. Klikk Veksle.
11. Klikk Last fra XML-fil.
    * Import konfigurasjonen ER tilordning som angir dataflyten for å hente data fra programmet, og deretter bruke den til å generere Intrastat-rapporten. Du vil senere utvide denne modelltilordningsdefinisjonen for å hente data fra Intrastat-rapporten og bruke dem til oppdateringen av programdataene for å arkivere detaljer om Intrastat-rapporteringsprosessen.   
    * Klikk Bla gjennom og velg Intrastat (tilordning) XML-filen.  
12. Klikk OK.
13. Utvid 'Intrastat (modell)' i treet.
14. Velg 'Intrastat (modell)\Intrastat (tilordning)' i treet.
15. Klikk Utforming.
    * Legg merke til at gjeldende modell tilordningen inneholder verdien "som modell" i retning-feltet. Dette betyr at tilordning av denne modellen er utformet for å hente data fra programmet, og lagre den i datamodellen.  
16. Klikk Utforming.
17. Utvid 'Liste' i treet.
18. Utvid 'Transaksjoner= Liste' i treet.
    * Se gjennom strukturen i modelltilordningen som bruker datamodellen som er filtrert etter rotelementet, "For utgående dokument." Legg merke til at den tillagte datakilden "Liste" gir tilgang til de nødvendige programdataene, som er en liste med poster fra Intrastat-tabellen.  
19. Lukk siden.
20. Lukk siden.
21. Klikk Veksle.
22. Klikk Last fra XML-fil.
    * Import ER formatkonfigurasjonen som angir oppsettet for Intrastat-rapporten, og hvordan du fyller ut data i rapporten. Du vil senere utvide denne formatdefinisjonen for å plassere data fra Intrastat-rapporten i datamodellen og deretter bruke dem til å oppdatere programdataene for å arkivere detaljer om Intrastat-rapporteringsprosessen.   
    * Klikk Bla gjennom og velg Intrastat (format) XML-filen.  
23. Klikk OK.
24. Velg 'Intrastat (modell)\Intrastat (format)' i treet.
25. Klikk Utforming.
26. Klikk Vis/skjul.
27. Velg 'Fil\Deklarasjon' i treet.
28. Klikk kategorien Tilordning.
29. Velg 'Fil' i treet.
    * Se gjennom strukturen i formatet som brukes til å generere Intrastat-rapporten. Legg merke til at den er utformet til å generere en XML-fil ved hjelp av data fra datamodellen, som er basert på rotelementet "For utgående dokument". Kontroll at navnet på filen som genererte defineres i dialogboksen brukerskjemaet ("fn-datakilden som brukes for den).   
30. Lukk siden.


