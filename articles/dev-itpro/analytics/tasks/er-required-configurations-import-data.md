--- 
title: "ER Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil"
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme konfigurasjoner for elektronisk rapportering (ER) for å importere data til Dynamics 365 for Finance and Operations, Enterprise Edition-programmet fra en ekstern fil."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6675f35c9ec163a620e63af32ecdbff02197d3c3
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme konfigurasjoner for elektronisk rapportering (ER) for å importere data til Dynamics 365 for Finance and Operations, Enterprise Edition-programmet fra en ekstern fil. I dette eksemplet skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet, Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen, "Opprette en konfigurasjonsleverandør og merke den som aktiv." Disse trinnene kan fullføres ved hjelp av USMF-datasettet. Du må også laste ned og lagre følgende filer lokalt ved hjelp av koblinger fra emnet Oversikt over elektronisk rapportering (https://go.microsoft.com/fwlink/?linkid=852550): 1099model.xml, 1099format.xml, 1099entries.xml, 1099entries.xlsx.

    * ER gir bedrifter muligheten til å konfigurere prosessen med å importere eksterne datafiler til tabeller i Dynamics 365 for Finance and Operations, Enterprise Edition i enten XML- eller TXT-format. Først må en abstrakt datamodell og en ER-datamodellkonfigurasjon utformes til å representere dataene du importerer. Deretter må du definere strukturen til filen du importerer, og metoden du vil bruke til å overføre dataene fra filen til den abstrakte datamodellen. ER-formatkonfigurasjonen som tilordnes til den utformede datamodellen, må opprettes for den abstrakte datamodellen. Deretter må datamodellkonfigurasjonen utvides med en tilordning som beskriver hvordan de importerte dataene beholdes som abstrakte datamodelldata og hvordan de brukes til å oppdatere tabeller i Dynamics 365 for Finance and Operations, Enterprise Edition.  ER-datamodellkonfigurasjonen må legges til med en ny modelltilordning som beskriver bindingen av datamodellen til programmets mål.  
    * Følgende scenario viser funksjonene for ER-dataimport. Dette inkluderer leverandørtransaksjoner som spores eksternt, og deretter importeres til Dynamics 365 for Finance and Operations, Enterprise Edition for å rapporteres senere i leverandørens utligning for 1099-skjema.   

## <a name="add-a-new-er-model-configuration"></a>Legg til en ny ER-konfigurasjon
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Bekreft at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".   
2. Klikk Rapporteringskonfigurasjoner.
    * I stedet for å opprette en ny modell for å støtte dataimport, laster du inn filen, 1099model.xml, som du lastet ned tidligere. Denne filen inneholder den egendefinerte datamodellen for leverandørers transaksjoner. Denne datamodellen er tilordnet til Dynamics 365 for Finance and Operations, Enterprise Edition-datakomponenter i AOT-dataenheten.   
3. Klikk Veksle.
4. Klikk Last fra XML-fil.
    * Klikk Bla gjennom og gå til 1099model.xml-filen som du lastet ned tidligere.  
5. Klikk OK.
6. Velg 1099-betalingsmodell i treet.

## <a name="review-data-model-settings"></a>Se gjennom innstillingene for datamodell
1. Klikk Utforming.
    * Denne modellen er utviklet for å representere leverandørenes transaksjoner fra et bedriftsståsted og er atskilt fra implementeringen i Dynamics 365 for Finance and Operations, Enterprise Edition.   
2. Utvid 1099-MISC i treet.
3. Velg 1099-MISC\Transaksjoner i treet.
4. Utvid 1099-MISC\Transaksjoner i treet.
    * Transaksjoner-elementet i denne modellen representerer enkelttransaksjoner. De underordnede elementene brukes til å angi nødvendige opplysninger, for eksempel leverandørkonto og transaksjonsdato, for hver transaksjon.   
5. Lukk siden.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Legge til en ny ER-formatkonfigurasjonen som støtter dataimport
    * Trinnene i denne delaktiviteten viser hvordan en ny formatkonfigurasjon kan opprettes for å styre dataimport fra eksterne filer.   
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I feltet Ny angir du Format basert på datamodell 1099-betalingsmodell.
3. Velg Ja i feltet Støtter dataimport.
4. Trykk ESC for å lukke denne siden.
    * I stedet for å opprette et nytt format for å støtte dataimport, laster du inn 1099model.xml-filen som du lastet ned tidligere. Denne filen inneholder den definerte strukturen på filen du importerer, og tilordningen av strukturen til den egendefinerte datamodellen til leverandørers transaksjoner.   
5. Klikk Veksle.
6. Klikk Last fra XML-fil.
    * Klikk Bla gjennom og gå til 1099format.xml-filen som du lastet ned tidligere.  
7. Klikk OK.
8. Utvid 1099-betalingsmodell i treet.
9. Velg 1099-betalingsmodell\Format for import av leverandørers transaksjoner i treet.

## <a name="review-format-settings"></a>Se gjennom formatinnstillinger
1. Klikk Utforming.
2. Aktiver Vis detaljer.
3. Klikk Vis/skjul.
4. Klikk Vis/skjul.
    * Det utformede formatet representerer den forventet strukturen for den eksterne filen. Denne filen må være i XML-format og ha rotelementet utligning. Hver leverandørtransaksjon er representert av transaksjonselementet som er definert til å ha null-til-mange-multiplisitet. Dette betyr at den innkommende filen kan inneholde alt fra null til mange transaksjoner. Nestede elementer for elementet "transaksjon" representerer attributtene for en enkelt transaksjon. Vær oppmerksom på at alle attributter, bortsett fra land, er merket som obligatorisk, noe som betyr at de må inkluderes i filen som importeres.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Se gjennom innstillingene for formattilordningen til datamodellen
1. Klikk Tilordne format til modell.
    * Tilordningen "For å importere leverandørenes transaksjoner" inneholder dataoverføringsreglene fra den innkommende XML-filen til den valgte delen av den egendefinerte datamodellen, som defineres ved å velge 1099-MISC-definisjonen.  
2. Klikk Utforming.
3. Aktiver Vis detaljer.
4. Utvid format: Post i treet.
5. Velg format: Post i treet.
    * Legg merke til at det utformede formatet vises her som en datakildekomponent.  
6. I treet utvider du format: Post\*utligning: XML-element 1..1 (utligning): Post.
7. I treet utvider du format: Post\*utligning: XML-element 1..1 (utligning): Post\transaksjon: XML-element 0..* (transaksjon): Postliste.
8. I treet utvider du format: Post\*utligning: XML-element 1..1 (utligning): Post\transaksjon: XML-element 0..* (transaksjon): Postliste\*leverandør: XML-element 1..1 (leverandør): Post.
9. I treet utvider du format: Post\*utligning: XML-element 1..1 (utligning): Post\transaksjon: XML-element 0..* (transaksjon): Postliste\land: XML-element 0..1 (land): Post.
10. I treet velger du format: Post\*utligning: XML-element 1..1 (utligning): Post\transaksjon: XML-element 0..* (transaksjon): Postliste\*leverandør: XML-element 1..1 (leverandør): Post.
    * Legg merke til at presentasjonen av obligatoriske og valgfrie formatelementer er forskjellige i den forhåndsdefinerte "format"-datakildekomponenten.  
11. I treet utvider du Transaksjoner: Postliste= format.utligning.$opplistet.
    * Legg merke til at elementene i formatet som definerer strukturen for den importerte filen er bundet til elementene i den egendefinerte datamodellen. Basert på disse bindingene lagres innholdet i den importerte XML-filen under kjøring i den eksisterende datamodellen. Vær oppmerksom på bindingen til landelementet. For transaksjonselementer i den innkommende filen som ikke inneholder slike elementer, fylles standard landkode "USA" ut i datamodellen.  
12. Klikk kategorien Valideringer.
    * Tilordning av dette formatet kan inneholde brukerdefinert logikk for å bekrefte nøyaktigheten av de importerte dataene fra et bedriftsståsted. For transaksjoner i importfilen uten en definert landskode (basert på innstillingen), genereres en advarsel i infologgen som informerer brukeren om saken og angir serienummeret for transaksjonen.  
13. Lukk siden.

## <a name="run-the-format-mapping-to-the-data-model"></a>Kjøre formattilordningen til datamodellen
    * Kjør denne formattilordningen for testformål. Bruk filen 1099entries.xml som du lastet ned tidligere. Du kan eksportere denne filen fra 1099entries.xlsx-arbeidsboken som brukes til å administrere leverandørtransaksjoner. De genererte utdataene importeres fra den valgte XML-filen og fyller ut den egendefinerte datamodellen ved reell import.  
1. Klikk Kjør.
    * Klikk Bla gjennom og gå til 1099entries.xml-filen som du lastet ned tidligere.  
2. Klikk OK.
    * Vær oppmerksom på advarselen om en manglende landkode for en transaksjon i den importerte filen.  
    * Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen.   
3. Lukk siden.
4. Lukk siden.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Se gjennom innstillingene for modelltilordningen til målene
1. Velg 1099-betalingsmodell i treet.
2. Klikk Utforming.
3. Klikk Tilordne modell til datakilde.
    * Tilordningen "For import for manuelle 1099-transaksjoner" er definert med retningstypen Til mål. Dette betyr at den er angitt for å støtte dataimport og inneholder innstillingen for regler som definerer hvordan den importerte eksterne filen og beholdt som abstrakte datamodelldata brukes til å oppdatere tabeller i Dynamics 365 for Finance and Operations, Enterprise Edition-programmet.  
4. Klikk Utforming.
5. Utvid modell: Datamodellen 1099-betalingsmodell i treet.
6. Utvid modell: Datamodellen 1099-betalingsmodell\Transaksjoner: Postliste i treet.
    * Legg merke til at den utformede modellen vises her som et datakildeelement. Under kjøring inneholder den dataene som importeres fra den eksterne filen. Flere tabeller ble lagt til som datakildeelementer for å sikre at de importerte dataene er i samsvar med dataene i gjeldende program, inkludert om leverandørkontoen for transaksjonen er tilgjengelig i systemet, om kombinasjonen av importland og delstatskoder finnes, og så videre.  
7. I treet velger du modell: Datamodellen 1099-betalingsmodell\Transaksjoner: Postliste\$mislykket: Beregnet felt = IF(OR(ISEMPTY(modell.Transaksjoner.$refs.leverandør), ISEMPTY(modell.Transaksjoner.$refs.leverandør1099), ISEMPTY(modell.Transaksjoner.$refs.boks1099), ISEMPTY(modell.Transaksjoner.$refs.land), ISEMPTY(modell.Transaksjoner.$refs.delstat), ISEMPTY(modell.Transaksjoner.$refs.sted)), sann, usann): Boolsk.
8. Klikk Rediger.
9. Klikk Rediger formel.
    * Når minst én validering mislykkes for én importert transaksjon, vil denne transaksjonen merkes som mislykkes ved datakildeattributtet "$mislyktes".  
10. Lukk siden.
11. Klikk Avbryt.
12. I treet velger du tax1099trans: Tabellen VendSettlementTax1099 poster= modell.Validert.
13. Klikk Rediger mål.
    * Dette ER-målet ble lagt til for å angi hvor de importerte dataene skal oppdatere programtabellene. I dette tilfellet er datatabellen VendSettlementTax1099 valgt. Fordi posthandlingen Sett inn post er valgt, settes de importerte transaksjonene inn i tabellen VendSettlementTax1099. Legg merke til at en enkelt modelltilordning kan inneholde flere mål. Dette betyr at de importerte dataene kan brukes til å oppdatere flere programtabeller samtidig. Tabeller, visninger og dataenheter kan brukes som ER-mål.   
    * Hvis tilordningen skal kalles fra et punkt i Dynamics 365 for Finance and Operations, Enterprise Edition-programmet (for eksempel knapp eller menyelement) som er spesielt utviklet for denne handlingen, skal ER-målet merkes som integreringspunktet. I dette eksemplet er dette punktet ERTableDestination#VendSettlementTax1099.  
14. Klikk Avbryt.
15. Klikk Vis alle.
16. Klikk Vis bare tilordnet.
17. I treet utvider du tax1099trans: Tabellen VendSettlementTax1099 poster= modell.Validert.
    * Legg merke til at datakildeelementet som inneholder de eneste godkjente transaksjonene, er bundet til det opprettede målet. Du kan filtrere de importerte transaksjonene for å hoppe over de som ikke er kompatible med programdataene.  
18. I treet velger du mislykket: Tabellen 'VendSettlementTax1099Entity poster= modell.Mislykket.
19. Klikk kategorien Valideringer.
    * Denne modelltilordningen kan inneholde brukerdefinert logikk for å bekrefte nøyaktigheten av de importerte dataene fra de eksisterende programdataene. For transaksjoner i den importerte filen med en leverandørkonto som ikke er i systemet (basert på gjeldende innstilling), genereres en advarsel i infologgen som informerer brukeren og angir den uriktige leverandørkontokoden.  
    * Legg merke til at alternativet Ettervalideringshandling kan brukes for hver validering, for å angi om importprosessen må fortsettes eller stoppes, og om de allerede utførte innsettingene/oppdateringene kan beholdes eller tilbakestilles.  
20. Klikk Vis bare tilordnet.
21. Klikk Vis alle.
22. Lukk siden.
    * Kjør denne modelltilordningen for å teste det utformede formatet og modelltilordningene. Bruk filen 1099entries.xml. Dataene fra den valgte filen importeres til systemet.  
23. Klikk Kjør.
    * Legg merke til at dialogboksen ikke inneholder flere spørsmål om formattilordningen som må brukes til å analysere den importerte filen og deretter overføre dataene til datamodellen. Dette skyldes at det i øyeblikket bare er ett format som bruker denne modellen, som er merket som utformet for å støtte dataimport.  
    * Definer bilags-IDen for å skille mellom importerte transaksjoner og andre transaksjoner som allerede er angitt manuelt eller importert.  
24. Skriv inn IMPORT-001 i feltet Angi bilags-ID.
    * Bla gjennom for å hente filen "1099entries.xml".  
25. Klikk OK.
    * Listen over genererte advarsler gir informasjon om feil leverandørkontoer, en feil 1099-bokskode for avgift, manglende landkoder, og så videre. Sammenlign denne listen over advarsler med innholdet som er inkludert i XML-filen som kjøres.  
26. Lukk siden.
27. Lukk siden.
28. Lukk siden.
29. Lukk siden.
30. Gå til Leverandører > Periodiske oppgaver > 1099-avgift > Leverandørutligning for 1099-skjema.
    * Dette skjemaet viser de kumulative transaksjonene i tabellen Tax1099Summary som er opprettet basert på importerte transaksjoner.  
31. Angi datoen som 2000-01-01 i feltet Fra dato.
32. Klikk Manuelle 1099-transaksjoner.
    * Dette skjemaet viser listen over transaksjoner som er lagt til manuelt, og transaksjonene vi nettopp importerte.  
33. Åpne bilagskolonnefilteret.
34. Angi en filterverdi for "IMPORT-001" i "Bilag"-feltet ved hjelp av filteroperatoren "begynner med".

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Se gjennom relasjonen mellom modell- og formattilordninger
1. Lukk siden.
2. Lukk siden.
3. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
4. Klikk Rapporteringskonfigurasjoner.
5. Velg 1099-betalingsmodell i treet.
    * Anta at du vil støtte import av de samme dataene, men fra et TXT-filformat.   
6. Klikk Opprett konfigurasjon for å åpne dialogboksen. 
7. I feltet Ny angir du Format basert på datamodell 1099-betalingsmodell.
8. Skriv inn Importer data fra TXT-fil i Navn-feltet.
9. Velg Ja i feltet Støtter dataimport.
10. Klikk Opprett konfigurasjon.
11. Klikk Utforming.
12. Klikk Tilordne format til modell.
13. Klikk Ny.
14. Angi eller velg en verdi i feltet Definisjon.
    * Velg alternativet 1099-MISC.  
15. Skriv inn Importer data fra TXT-fil i Navn-feltet.
16. Skriv inn Importer data fra TXT-fil i Beskrivelse-feltet.
17. Klikk Lagre.
18. Lukk siden.
19. Lukk siden.
20. Klikk Rediger.
    * Hvis du har installert hurtigreparasjonen KB 4012871 med støtte for TYSK modelltilordning i atskilte konfigurasjoner med mulighet til å angi ulike typer forutsetninger for å distribuere dem på forskjellige versjoner av Dynamics 365 for Finance and Operations, Enterprise edition (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), utfører du det neste trinnet "Aktivere flagget Standard for modelltilordning" for den angitte formatkonfigurasjonen. Ellers går du til neste trinn.  
21. Velg Ja i feltet Standard for modelltilordning.
22. Velg 1099-betalingsmodell i treet.
23. Klikk Utforming.
24. Klikk Tilordne modell til datakilde.
25. Klikk Kjør.
    * Hvis du har installert hurtigreparasjonen KB 4012871 med støtte for TYSK modelltilordning i atskilte konfigurasjoner med mulighet til å angi ulike typer forutsetninger for å distribuere dem på forskjellige versjoner av Dynamics 365 for Finance and Operations Enterprise edition (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 ), velger du den foretrukne modelltilordningen i oppslagsfeltet. Hvis du har ennå ikke har installert hurtigreparasjonen, går du til neste trinn siden tilordningen allerede er valgt av definisjonen av standard formatkonfigurasjon.  
    * Hvis du ikke har installert hurtigreparasjonen KB 4012871, legger du merke til at dialogboksen inneholder et ekstra spørsmål om modelltilordning som brukes til å analysere filen du importerer. Dataene blir deretter overført fra dialogboksen til datamodellen. For øyeblikket kan du velge hvilken formattilordning som må brukes, avhengig av typen fil du planlegger å importere.  
    * Hvis du har tenkt å kalle denne modelltilordningen fra et punkt i Dynamics 365 for Finance and Operations, Enterprise Edition som er spesielt utformet for handlingen, må ER-målet og formattilordningen være merket som en del av integreringen.  
26. Klikk Avbryt.
27. Lukk siden.
28. Lukk siden.


