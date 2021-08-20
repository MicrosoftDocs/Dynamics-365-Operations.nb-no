---
title: Utforme ER-konfigurasjoner for å importere data fra eksterne CSV-filer
description: Bruk denne prosedyren til å utforme konfigurasjoner for elektroniske rapportering (ER) for å importere data til en Finance and Operations-app fra en ekstern fil i CSV-format.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b42f0cf8c7260c85d405a5dfdcd50323ffee4d4528b982997a802b859ab8327b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747277"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>Utforme ER-konfigurasjoner for å importere data fra eksterne CSV-filer

[!include [banner](../../includes/banner.md)]

Bruk denne prosedyren til å utforme elektroniske rapportering (ER)-konfigurasjoner for å importere data til programmet fra en ekstern fil i CSV-format. I denne fremgangsmåten skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv."

Denne fremgangsmåten er opprettet for brukere med rollen som Systemansvarlig eller Utvikler av elektronisk rapportering. Disse trinnene kan fullføres ved hjelp av USMF-datasettet.

Du må også laste ned og lagre følgende filer lokalt: [Eksempler på elektronisk rapportering i Dynamics 365 Finance](https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Du kan konfigurere en prosess for å importere eksterne filer i XML-, TXT- eller CSV-format til tabellene i programmet. Først må du opprette en abstrakt datamodell som representerer de importerte dataene, fra et bedriftsståsted – en konfigurasjon for ER-datamodell blir opprettet for dette. Deretter må du definere en struktur for den importerte filen som tilordnes til den utformede datamodellen som måten for å portere data fra filen til den abstrakte datamodellen – en ER-formatkonfigurasjon opprettes for dette. Deretter må ER-datamodellkonfigurasjonen utvides med en ny modelltilordning som beskriver hvordan dataene fra den importerte filen og de faste dataene fra den abstrakte datamodellen brukes til å oppdatere programtabellene eller dataenhetene.
    * Følgende trinn viser hvordan eksternt sporede leverandørtransaksjoner importeres fra den eksterne CSV-filen for senere bruk i leverandørutligningen for 1099-skjemaer.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirma Litware, Inc. er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".
2. Klikk på Rapporteringskonfigurasjoner.
3. Bruk filteret 1099-betalingsmodell. Hvis du allerede har fullført prosedyren Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil for elektronisk rapportering (ER) og konfigurasjonen 1099-betalingsmodell er tilgjengelig i konfigurasjonstreet, hopper du over alle trinnene i neste underoppgave.

## <a name="add-a-new-er-model-configuration"></a>Legg til en ny ER-konfigurasjon

1. I stedet for å opprette en ny modell for å støtte dataimport, laster du inn filen 1099model.xml, som du lastet ned tidligere. Denne filen inneholder den egendefinerte datamodellen for leverandørers transaksjoner. Denne datamodellen er allerede tilordnet til de nødvendige datakomponentene.
2. Klikk på Veksle.
3. Klikk på Last fra XML-fil.
4. Klikk på Bla gjennom og gå til 1099model.xml-filen som du lastet ned tidligere.
5. Klikk på OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Legge til en ny ER-formatkonfigurasjonen som støtter dataimport

1. Velg 1099-betalingsmodell i treet.
2. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Format basert på datamodell 1099-betalingsmodell.
4. Velg Ja i feltet Støtter dataimport.
5. Trykk ESC for å lukke denne siden.
    * I stedet for å opprette et nytt ER-format for å støtte dataimport, laster du inn 1099formatcsv.xml-filen som du lastet ned tidligere. Denne filen inneholder det nødvendige ER-formatet som definerer strukturen på den innkommende CSV-filen, og tilordningen av denne strukturen til datamodellen til leverandørers transaksjoner.
6. Klikk på Veksle.
7. Klikk på Last fra XML-fil.
    * Klikk på Bla gjennom og gå til 1099formatcsv.xml-filen som du lastet ned tidligere.
8. Klikk på OK.
9. Utvid 1099-betalingsmodell i treet.
10. Velg 1099-betalingsmodell\For import av leverandørers transaksjoner (CSV) i treet .

## <a name="review-format-settings"></a>Se gjennom formatinnstillinger

1. Klikk på Utforming.
2. Klikk på Vis/skjul.
3. Aktiver Vis detaljer.
    * Det utformede formatet representerer den forventet strukturen for den eksterne filen i CSV-format.
4. Velg 'Innkommende: Fil\Rot: Sekvens' i treet.
    * For rotelementet av typen SEQUENCE er alternativet Ny linje - Windows (CR LF) valgt i feltet Spesialtegn. Basert på denne innstillingen, må hver linje i analysefilen betraktes som en egen oppføring.
5. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..*` i treet.
    * For rot\linjeelementet av typen SEQUENCE, er alternativet Én mange valgt i Multiplisitet-feltet. Basert på denne innstillingen, vises minst én linje i analysefilen.
6. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case` i treet.
    * Legg merke til at Rot\Linje\Typer-elementet av typen CASE er lagt til som nestet element i Rot\Linje-sekvensen. Fordi dette CASE-elementet inneholder 3 nestede sekvenselementer, antar denne innstillingen at vi forventer å møte 3 ulike typer av linjen i analysefilen.
7. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1` i treet.
    * Rot\Linje\Type\Hode-elementet av typen SEQUENCE inneholder det nestede STRING-elementet der verdien har blitt definert som den faste strengverdien. Denne sekvensen kommer til å analysere hodelinjen i analysefilen.
8. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)` i treet.
    * Rot\Linje\Typer\Post-elementet av typen SEQUENCE er konfigurert til å analysere transaksjonslinjene. Legg merke til at alternativet Egendefinert skilletegn er konfigurert som et komma. Dette betyr at kommaet brukes som skilletegn for et felt for denne typen linje i analysefilen.
    * Legg merke til at flere nestede elementer av forskjellige datatyper er lagt til for Rot\Linje\Typer\Post-elementet for å analysere transaksjonens linjer som atskilte felt. Legg merke til at alternativet Tilbudssøknad er konfigurert som "Ingen". Dette betyr at i analysefilen anses alle felt av denne typen som at de ikke har omsluttede tegn.
9. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime` i treet.
    * For eksempel Rot\Linje\Typer\Post\TransactionDate-elementet av typen DATETIME er konfigurert for å hente transaksjonens verdi for dato og klokkeslett fra analysefilen i M/d/åååå-formatet.
10. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1` i treet.
    * Legg merke til at Rot\Linje\Typer\Post\CountryCode-elementet av typen STRING er konfigurert slik at det har alternativet "Null en" i Multiplisitet-feltet. Denne innstillingen anser verdien i feltet CountryCode i analyselinjen som valgfri.
11. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)` i treet.
    * Merk at Rot\Linje\Typer\Post\Kommentar-elementet av typen SEQUENCE er konfigurert slik at det har alternativet "Alle" i feltet Tilbudssøknad og doble anførselstegn i feltet Tilbudsmerke. Det betyr at alle feltene av denne typen linjer i analysefilen (beskrevet med de nestede elementene: tekst av typen STRING) blir betraktet som omsluttet av doble anførselstegn.
12. Velg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1` i treet.
    * Rot\Linje\Typer\Ikke-analysert-elementet av typen SEQUENCE er konfigurert til å analysere transaksjonslinjene for strukturen som ikke samsvarer med strukturen som er beskrevet ovenfor, i det overordnede CASE-elementet.

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Se gjennom innstillingen for formattilordningen til datamodellen

1. Klikk på Tilordne format til modell.
    * Modelltilordningen Tilordning til modell fra CSV-format beskriver dataflyten for dataoverføringen fra den innkommende CSV-filen til datamodellen.
2. Klikk på Utforming.
3. Utvid 'format' i treet.
    * Legg merke til at det utformede formatet vises her som en datakildekomponent.
4. Utvid 'format\Innkommende: File(Incoming)' i treet.
5. Utvid 'format\Innkommende: File(Incoming)\Rot: Sequence(Root)' i treet.
6. Utvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)` i treet.
7. Utvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)` i treet.
8. Utvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)` i treet.
9. Utvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data` i treet.
10. Utvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)` i treet.
11. Velg `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)` i treet.
    * Legg merke til at obligatoriske og valgfrie formatelementer, for eksempel TransactionDate og CountryCode, ser annerledes ut i den forhåndsdefinerte datakildekomponenten for format.
12. Utvid 'Transaksjoner= '$both'' i treet.
    * Legg merke til at elementene i formatet som definerer strukturen for den importerte filen er bundet til elementene i datamodellen. Basert på disse bindingene lagres innholdet i den importerte CSV-filen under kjøring i den eksisterende datamodellen. Vær oppmerksom på bindingen til CountryRegion-elementet. For transaksjonselementer i den innkommende filen som ikke har angitt en landkodeverdi, fylles standard landkode "USA" ut i datamodellen.
13. Aktiver Vis detaljer.
14. Klikk på fanen Valideringer.
15. Klikk på Søk.
16. I Søk-feltet skriver du inn leverand.
17. Klikk på Søk etter neste.
    * Tilordning av dette formatet kan inneholde brukerdefinert logikk for å bekrefte nøyaktigheten av de importerte dataene fra et bedriftsståsted. Basert på innstillingen genereres det for eksempel en advarsel for enhver linje i importfilen som har en struktur som verken samsvarer med strukturen til hodelinjen eller transaksjonslinjen. Advarselen genereres i informasjonsloggen og informerer brukeren om dette tilfellet og indikerer sekvensnummeret for transaksjonen i filen.
18. Lukk siden.

## <a name="run-the-format-mapping"></a>Kjøre formattilordningen

For testformål kan du utføre formattilordningen med filen 1099entriescsv.csv som du lastet ned tidligere. De genererte utdataene viser informasjon som importeres fra den valgte CSV-filen og fylles ut i den egendefinerte datamodellen ved reell import.

1. Klikk på Kjør.
    * Klikk på Bla gjennom og gå til 1099entriescsv.csv-filen som du lastet ned tidligere.
2. Klikk på OK.
    * Legg merke til advarslene om linjer som ikke er godkjent. Linje 4 inneholder inntektsverdien som vises i det ikke-godkjente formatet, mens linje 7 ikke inneholder transaksjonsmerknadsteksten i doble anførselstegn.
    * Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen. Vær oppmerksom på at alle 7 linjene i den importerte CSV-filen ble behandlet. Feltenes titler linje 1 ble hoppet over, 4 transaksjoner ble riktig analysert, og 2 transaksjoner ble gjenkjent som ikke gyldige.
3. Lukk siden.
4. Lukk siden.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]