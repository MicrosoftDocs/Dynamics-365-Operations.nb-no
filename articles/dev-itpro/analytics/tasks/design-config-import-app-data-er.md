---
title: Utforme ER-konfigurasjoner til å analysere innkommende dokumenter
description: Denne prosedyren viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å analysere et innkommende elektronisk dokument.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e5f826afa141c0851a963b33e40c58513e60a07
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "326107"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Utforme ER-konfigurasjoner til å analysere innkommende dokumenter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å analysere et innkommende elektronisk dokument. I denne prosedyren må du importere de nødvendige ER-konfigurasjonene som er opprettet for eksempelfirmaet, Litware, Inc, og bruke dem til å analysere innkommende elektroniske dokumenter. For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv."

Denne fremgangsmåten er opprettet for brukere med rollen som Systemansvarlig eller Utvikler av elektronisk rapportering. 

Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett. Før du begynner laster du ned og lagrer filene i emnet, "Analysere innkommende dokumenter for å oppdatere programdata" (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents). Filene er: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
2. Klikk Rapporteringskonfigurasjoner.
    * Dette scenariet vil bli brukt til å vise egenskapene for analyse av innkommende elektroniske dokumenter i XML-format: ERP-programmet (Dynamics 365 for Finance and Operations) ber om data fra webtjenesten (for eksempel http://efsta.org/ EFSTA fiscal service) og analyserer innkommende svar for å oppdatere programdata i henhold til dette. Den mest effektive måten å analysere på er å bruke et enkelt ER-format til tross for den forskjellige strukturen på forventede innkommende dokumenter i XML-format.   

## <a name="import-and-review-er-configurations"></a>Importere og gå gjennom ER-konfigurasjoner
Importer ER-konfigurasjonen som inneholder eksempeldatamodellen som er utviklet for å lagre detaljene for den innkommende filen.  
1. Klikk Veksle.
2. Klikk Last fra XML-fil.
    * Klikk Bla gjennom og velg EFSTA model.xml-filen.  
3. Klikk OK.
4. Velg modellen EFSTA i treet.
5. Klikk Utforming.
    * Se gjennom strutkren i den importerte datamodellen. Legg merke til at enumType-nummereringen er definert slik at den gjenkjenner følgende typer servicesvar: for å få bekreftelse om transaksjonens innsending, få informasjon om siste transaksjon som er sendt, og gjenkjenne svartyper som ikke støttes.   
6. Utvid Svar i treet.
    * Vær oppmerksom på at rotelementet Svar er definert for å angi hvilken type data som må tas fra et støttet servicesvar for å oppdatere programdata tilsvarende.   
7. Lukk siden.
    * Du vil importere ER-formatkonfigurasjonen som angir hvordan innkommende dokumenter analyseres for å lagre data i ER-datamodellen.   
8. Klikk Veksle.
9. Klikk Last fra XML-fil.
    * Klikk Bla gjennom og velg EFSTA format.xml-filen.  
10. Klikk OK.
11. Utvid modellen EFSTA i treet.
12. Velg 'EFSTA-modell\EFSTA-format' i treet.
13. Klikk Utforming.
14. Klikk Vis/skjul.
    * Merk at CASE-formatelementet brukes som roten og inneholder tre nestede FILE-elementer, som betyr at dette formatet er utformet for å analysere innkommende filer i flere formater.  
15. I treet velger du 'Svar\Transaksjonsfullføring\TraC'.
    * Legg merke til at svaret om den innsendte transaksjonen begynner fra rotelementet TraC.   
16. I treet velger du 'Svar\Siste transaksjonsforespørsel\Tra'.
    * Legg merke til at svaret om den siste innsendte transaksjonen begynner fra rotelementet Tra.   
17. I treet velger du 'Svar\Uventet svar\Tekst'.
    * Det tredje FILE-elementet med nestet TEXT-element er lagt til for å gjenkjenne andre typer svar som er forskjellige fra dem som er nevnt ovenfor.   
18. Klikk Tilordne format til modell.
    * Modelltilordningen inneholder definisjonen av dataflyt for å lagre detaljene om det analyserte inngående dokumentet ved hjelp av datamodellens elementer.  
19. Klikk Utforming.
20. Utvid 'format' i treet.
21. I treet utvider du 'format\Svar: Case(Responses)'.
    * Se gjennom strukturen i format-datakilden. Legg merke til at alle tre svartypene tilbys separat.   
22. I treet velger du 'format\Svar: Case(Responses)\aType'.
    * Datakildeelementet "aType" er lagt til for å angi svartypen og er bundet til datamodellelementet 'Type'.  
23. Klikk kategorien Valideringer.
24. I treet velger du 'Type = format.Responses.aType'.
    * Legg merke til at ER-valideringen er konfigurert for å informere brukeren om situasjonen når svarstrukturen ikke stemmer med bekreftelsen av transaksjonens innsending eller informasjonen om den siste transaksjonen som er sendt (svarsak som ikke støttes).   
25. Lukk siden.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Kjøre modelltilordning av ER-format som er konfigurert for analyse av innkommende filer
Du vil kjøre den opprettede modelltilordningen for testformål for å se hvordan det konfigurerte ER-formatet kommer til å analysere innkommende servicesvar. Dette trinnet bruker forskjellige XML-filer til å simulere ulike typer webservicesvar.   
1. Åpne filen Response1.xml i en XML-leser, for eksempel en webleser. Merk at denne filen inneholder bekreftelsesdetaljer om transaksjonen som er fullført ("TraC" er rotelementet).   
2. Klikk Kjør.
    * Klikk Bla gjennom og velg Response1.xml-filen.  
3. Klikk OK.
    * Se gjennom de genererte utdataene. Merk at svartypen er riktig gjenkjent og analysert (ERModelEnumDataSourceHandler#EFSTA model#enumType#C betyr transakasjonsfullføringssak).   
    * Åpne filen Response2.xml i en XML-leser. Merk at denne filen inneholder informasjon om den siste transaksjonen som er sendt ("Tra" er rotelementet).   
4. Klikk Kjør.
    * Klikk Bla gjennom og velg Response2.xml-filen.  
5. Klikk OK.
    * Se gjennom de genererte utdataene. Merk at svartypen er riktig gjenkjent og analysert (ERModelEnumDataSourceHandler#EFSTA model#enumType#R betyr systemomstartsak).   
    * Åpne filen Response3.xml i en XML-leser. Legg merke til at denne filen starter fra rotelementet TraZ og at denne strukturen ikke er konfigurert med ER-formatet.   
6. Klikk Kjør.
    * Klikk Bla gjennom og velg Response3.xml-filen.  
7. Klikk OK.
    * Se gjennom de genererte utdataene. Merk at svartypen er riktig gjenkjent som ikke-støttet (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Den tilsvarende meldingen er plassert i infologgen (i henhold til ER-valideringsinnstillingen), og det meste av datamodellen er ikke fylt ut.   
    * Åpne filen Response4.xml i en XML-leser. Legg merke til at strukturen i denne filen er nesten den samme som den analyserte Response1.xml, bortsett fra sekvensen av nestede elementer i rotelementet "TraC".   
8. Klikk Kjør.
    * Klikk Bla gjennom og velg Response4.xml-filen.  
9. Klikk OK.
    * Se gjennom de genererte utdataene. Merk at svartypen er riktig gjenkjent som ikke-støttet (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Den tilsvarende meldingen er plassert i infologgen, og det meste av datamodellen er ikke fylt ut. Dette skyldes at den gjeldende innstillingen for dette ER-formatet forutsetter en bestemt sekvens av nestede elementene i rotelementet på den innkommende filen.   
10. Lukk siden.
11. I treet velger du 'Svar\Transaksjonsfullføring\TraC'.
12. I feltet Analyserekkefølge for nestede elementer velger du Vilkårlige.
    * Velg Vilkårlige i feltet Analyserekkefølge for nestede elementer for å tillate enhver sekvens av nestede elementer for dette XML-rotelementet.  
13. Klikk Lagre.
14. Klikk Tilordne format til modell.
15. Klikk Kjør.
    * Klikk Bla gjennom og velg Response4.xml-filen.  
16. Klikk OK.
    * Se gjennom de genererte utdataene. Legg merke til at svartypen er nå gjenkjent som lik for Response1.xml-filen.  

