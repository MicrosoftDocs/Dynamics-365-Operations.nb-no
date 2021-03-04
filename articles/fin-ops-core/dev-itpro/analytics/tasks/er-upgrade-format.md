---
title: ER Oppgradere formatet ved å ta i bruk en ny, grunnleggende versjon av dette formatet
description: De fremgangsmåten nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan vedlikeholde en formatkonfigurasjon for elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17fe6d772040c73959685920743225c128421951
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684266"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>ER Oppgradere formatet ved å ta i bruk en ny, grunnleggende versjon av dette formatet

[!include [banner](../../includes/banner.md)]

De fremgangsmåten nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan vedlikeholde en formatkonfigurasjon for elektronisk rapportering (ER). Denne fremgangsmåten beskriver hvordan en egendefinert versjon av et format kan opprettes basert på formatet som mottas fra en konfigurasjonsleverandør (CP). Den forklarer også hvordan du bruker en ny, basisversjon av dette formatet.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåtene "Opprette en konfigurasjonsleverandør og merke den som aktiv" og "Bruke opprettet formatet for å generere elektroniske betalingsdokumenter". Denne fremgangsmåten kan utføres i firmaet GBSI.

## <a name="select-format-configuration-for-customization"></a>Velge formatkonfigurasjon for tilpassing
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.

    I dette eksemplet fungerer eksempelfirmaet Litware, Inc. (https://www.litware.com) som en konfigurasjonsleverandør som støtter formatkonfigurasjoner for elektroniske betalinger for et bestemt land.    Eksempelfirmaet Proseware, Inc (http://www.proseware.com) fungerer som en kunde i formatkonfigurasjonen som Litware, Inc. har angitt Proseware, Inc. bruker formater i bestemte områder i dette landet.  
2. Klikk Rapporteringskonfigurasjoner.
3. Klikk Vis filtre.
4. Bruk følgende filtre: Angi filterverdien "BACS (britisk fiktivt)" i Navn-feltet ved hjelp av filteroperatoren "begynner med".
  
    Den valgte formatkonfigurajonen BBS (Storbritannia fiktiv) eies av leverandøren Litware, Inc.  

5. Klikk Vis filtre.
6. Finn og velg ønsket post i listen.

    Versjonen av formatet med statusen Fullført brukes av Proseware, Inc. for tilpassing.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Opprette en ny konfigurasjon for det egendefinerte formatet for elektronisk dokument
Proseware, Inc. mottatte versjon 1.1 av BBS-konfigurasjon (Storbritannia fiktiv) som inneholder det innledende formatet for å generere elektroniske betalingsdokumenter fra Litware, Inc. i henhold til deres serviceabonnement. Proseware, Inc. vil begynne å bruke dette som standard for landet sitt, men noe tilpassing er nødvendig for å støtte bestemte områdekrav. Proseware, Inc. vil også beholde muligheten til å oppgradere et egendefinert format når det kommer en ny versjon av det (med endringer for å støtte nye landspesifikke krav) fra Litware, Inc, og de vil utføre oppgraderingen med lavest mulig kostnad.  

For å gjøre dette må Proseware, Inc. opprette en konfigurasjon ved hjelp av Litware, Inc. konfigurasjonen BBS (Storbritannia fiktiv) som grunnlag.  

1. Lukk siden.
2. Velg Proseware, Inc. for å gjøre dette til en aktiv leverandør.
3. Klikk Angi som aktiv
4. Klikk Rapporteringskonfigurasjoner.
5. Vis Betalinger (forenklet model) i treet.
6. Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.

    Velg konfigurasjonen BBS (Storbritannia fiktivt) fra Litware, Inc. Proseware, Inc. bruker versjon 1.1 som grunnlag for den tilpassede versjonen.  

7. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.

    Det lar deg opprette en ny konfigurasjon for et egendefinert betalingsformat.  

8. I det nye feltet angir du Avled fra navnet: BBS (Storbritannia fiktiv), Litware, Inc..

    Velg alternativet Avled for å bekrefte at bruken av BBS (Storbritannia fiktivt) som grunnlag for oppretting av den egendefinerte versjonen.  

9. Skriv inn BBS (Storbritannia fiktiv egendefinert ) i Navn-feltet.
10. I Beskrivelse-feltet skriver du inn BACS-leverandørbetaling (fiktivt Storbritannia egendefinert).

    Den aktive konfigurasjonsleverandøren (Proseware, Inc.) angis automatisk her. Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen. Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.  

11. Klikk Opprett konfigurasjon.

## <a name="customize-your-format-for-the-electronic-document"></a>Tilpasse formatet for det elektroniske dokumentet
1. Klikk Utforming.
2. Klikk Vis/skjul.
3. Klikk Vis/skjul.
4. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.
5. Klikk Legg til for å åpne nedtrekksdialogen.
6. Velg XML\Element i treet.
7. I Navn-feltet skriver du IBAN.
8. Klikk OK.
9. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\IBAN i treet.
10. Klikk Legg til for å åpne nedtrekksdialogen.
11. Velg Tekst\Streng i treet.
12. Klikk OK.
13. Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn\Streng i treet.
14. Angi 60 i feltet Maksimumslengde.
15. Klikk kategorien Tilordning.
16. Utvid noden 'model' i treet.
17. Utvid modell\Betalinger i treet.
18. Utvid modell\Betalinger\Kreditor i treet.
19. Utvid modell\Betalinger\Kreditor\Konto i treet.
20. I treet velger du modell\Betalinger\Kreditor\Konto\IBAN.
21. Velg Xml\Melding\Betalinger\Vare = modell.Betalinger\Leverandør\Bank\IBAN\Streng i treet.
22. Klikk Bind.
23. Klikk Lagre.

## <a name="validate-the-customized-format"></a>Validere det egendefinerte formatet
1. Klikk Valider.

    Validere oppsett for egendefinert format og endringer for datatilordning for å sikre at alle bindinger er i orden.  

2. Lukk siden.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Endre statusen for gjeldende versjon av egendefinert formatkonfigurasjon
Endre statusen for utformet formatkonfigurasjon fra Utkast til Fullført for å gjøre den tilgjengelig for generering av betalingsdokument.  

1. Klikk Endre status.

    Legg merke til at gjeldende versjon av den valgte konfigurasjonen har statusen Utkast.  

2. Klikk Fullført.
3. Skriv inn en verdi i feltet Beskrivelse.
4. Klikk OK.
5. Finn og velg ønsket post i listen.

    Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.1.1. Dette betyr at det er versjon 1 av egendefinerte BBS-format (Storbritannia fiktivt egendefinert), som er basert på versjon 1 av BBS-format (Storbritannia fiktivt), som er basert på versjon 1 av datamodellen Betalinger (forenklet modell).  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Teste det egendefinerte formatet for å generere betalingsfiler
Fullfør trinnene i fremgangsmåten "Bruke opprettet format for å generere elektroniske dokumenter for betalinger" i en parallel Finance and Operations-økt. Velg BBS-formatet (Storbritannia fiktiv egendefinert) i parametere for elektronisk betalingmåte. Kontroller at den opprettede betalingsfilen inneholder den nylig introduserte XML-noden som presenterer IBAN-kode i henhold til områdekrav.  

## <a name="update-the-existing-country-specific-configuration"></a>Oppdatere den eksisterende landspesifikke konfigurasjonen
Litware, Inc. må oppdatere BBS-konfigurasjonen (Storbritannia fiktiv) og bruke nye landkrav for administrasjon av formatet for det elektroniske dokumentet. Senere vil dette tas med i en ny versjon av denne konfigurasjonen, som vil tilbys for serviceabonnenter, inkludert Proseware, Inc.  

I virkelige relaterte prosesser for klargjøring av tjeneste kan hver versjon av BBS (Storbritannia fiktiv) importeres av Proseware, Inc. fra Litware, Inc. Litware, Inc. -konfigurasjonens LCS-repositorium. I denne fremgangsmåten skal vi simuler dette ved å oppdatere BBS (Storbritannia fiktiv) på vegne av en tjenesteleverandør.  

1. Lukk siden.
2. Velg Litware, inc-leverandør.
3. Klikk Angi som aktiv
4. Klikk Rapporteringskonfigurasjoner.
5. Vis Betalinger (forenklet model) i treet.
6. Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.

    Utkastversjonen som eies av Litware, Inc.-BBS-leverandøren (Storbritannia fiktiv), velges for å vise endringer for å støtte nye landspesifikke krav.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Lokalisere basisformatet for det elektroniske dokumentet
Gå ut ifra at det finnes nye landsspesifikke krav som skal støttes av Litware, Inc:  

- En verdi for kreditorens SWIFT-bankkode i hver betalingstransaksjon.
- En grense på 100 tegn for lengden på tekst for leverandørens navn i filen som genereres.  
- Nye landspesifikke krav  
- Velg utkastversjonen av den ønskede konfigurasjonen for å introdusere nødvendige endringer.  


1. Klikk Utforming.
2. Klikk Vis/skjul.
3. Klikk Vis/skjul.
4. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank i treet.
5. Klikk Legg til for å åpne nedtrekksdialogen.
6. Velg XML\Element i treet.
7. I Navn-feltet skriver du inn SWIFT.
8. Klikk OK.
9. Velg Xml\Melding\Betalinger\Vare\Leverandør\Bank\SWIFT i treet.
10. Klikk Legg til for å åpne nedtrekksdialogen.
11. Velg Tekst\Streng i treet.
12. Klikk OK.
13. Velg Xml\Melding\Betalinger\Vare\Leverandør\Navn\Streng i treet.
14. Angi 100 i feltet Maksimumslengde.
15. Klikk kategorien Tilordning.
16. Utvid noden 'model' i treet.
17. Utvid modell\Betalinger i treet.
18. Utvid modell\Betalinger\Kreditor i treet.
19. Utvid modell\Betalinger\Kreditor\Agent i treet.
20. I treet velger du modell\Betalinger\Kreditor\Agent\SWIFT.
21. Velg Xml\Melding\Betalinger\Vare = modell.Betalinger\Leverandør\Bank\SWIFT\Streng i treet.
22. Klikk Bind.
23. Klikk Lagre.

## <a name="validate-the-localized-format"></a>Validere det lokaliserte formatet
1. Klikk Valider.
2. Lukk siden.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Endre statusen for gjeldende versjon av basisformatkonfigurasjonen
Endre statusen for den oppdaterte grunnleggende formatkonfigurasjonen fra Utkast til Fullført for å gjøre den tilgjengelig for generering av betalingsdokumenter og oppdateringer av formatkonfigurasjoner som er avledet fra den.  

1. Klikk Endre status.

    Legg merke til at gjeldende versjon av den valgte konfigurasjonen har statusen Utkast.  

2. Klikk Fullført.
3. Skriv inn en verdi i feltet Beskrivelse.
4. Klikk OK.
5. Finn og velg ønsket post i listen.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Endre basisversjonen for den egendefinerte formatkonfigurasjonen

Proseware, Inc. blir informert om at en ny versjon 1.2 av BBS-konfigurasjon (Storbritannia fiktiv) er tilgjengelig for å generere elektroniske betalingsdokumenter i henhold til den nylig annonserte landspesifikke krav. Proseware, Inc. vil begynne å bruke det som standard for landet.  

For å gjøre dette må Proseware, Inc. endre den grunnleggende konfigurasjonsversjonen for den tilpassede BBS-konfigurasjonen (Storbritannia fiktiv egendefinert). Bruk den nye versjon 1.2 i stedet for versjon 1.1 av BBS (Storbritannia fiktiv).  

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Velg Proseware, Inc.-leverandøren for å merke den som aktiv.
3. Klikk Angi som aktiv
4. Klikk Rapporteringskonfigurasjoner.
5. Vis Betalinger (forenklet model) i treet.
6. Vis Betalinger (forenklet model)\BBS (Storbritannia fiktiv) i treet.
7. Velg Betalinger (forenklet model)\BBS (Storbritannia fiktiv)\BBS (Storbritannia fiktiv egendefinert) i treet.

    Velge BBS-konfigurasjonen (Storbritannia fiktiv egendefinert), som eies av Proseware, Inc.  

    Bruk utkastversjonen av den valgte konfigurasjonen for å introdusere nødvendige endringer.  

8. Klikk Rebaser.

    Velg den nye versjonen 1.2 av den grunnleggende konfigurasjonen som skal brukes som nytt grunnlag for oppdatering av konfigurasjonen.  

9. Klikk OK.

    Vær oppmerksom på at det er oppdaget noen konflikter under sammenslåing av den egendefinerte versjonen og en ny grunnleggende versjon, som representerer noen formatendringer som ikke kan slås sammen automatisk.  

## <a name="resolve-rebase-conflicts"></a>Løse rebaseringskonflikter
1. Klikk Utforming.
    
    Vær oppmerksom på at endringer i leverandørens tekstlengdegrense ikke kunne løses automatisk. Dette vises derfor i en konfliktliste. Følgende alternativer er tilgjengelige for hver konflikt av typen Oppdatering: – Bruk en tidligere basisverdi (knappen øverst i rutenettet) for å vise forrige basisversjonsverdi (0 i vårt tilfelle).  - Bruk en basisverdi (knappen øverst i rutenettet) for å vise den nye basisversjonverdien (100 i vårt tilfelle).  - Behold en egen (egendefinert) verdi (60 i vårt tilfelle).  Klikk Bruk basisverdi for å bruke den landspesifikke grensen på 100 tegn for tekstlengden for leverandørens navn.  

    Merk at Proseware, Inc. og Litware, Inc. har egendefinerte og lokale versjoner av dette formatet som bruker IBAN- og SWIFT-koder med relaterte komponenter som slås sammen automatisk i administrasjonsformat.  

2. Klikk Bruk basisverdi.

    Klikk Bruk basisverdi for å bruke den landspesifikke grensen på 100 tegn for leverandørnavn.  

3. Klikk Lagre.

    Lagring av formatet fjerner løste konflikter fra listen over konflikter.  

4. Lukk siden.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Endre statusen for den nye versjonen av den egendefinerte formatkonfigurasjonen
1. Klikk Endre status.

    Endre statusen for den oppdaterte, egendefinert formatkonfigurasjonen fra Utkast til Fullført. Dette vil gjøre formatkonfigurasjonen tilgjengelig for generering av betalingsdokumenter. Legg merke til at gjeldende versjon av den valgte konfigurasjonen har statusen Utkast.  

2. Klikk Fullført.
3. Skriv inn en verdi i feltet Beskrivelse.
4. Klikk OK.

    Vær oppmerksom på at den opprettede konfigurasjonen lagres som fullført versjon 1.2.2: versjon 2 av det grunnleggende BBS-formatet (Storbritannia fiktiv egendefinert), som er basert på versjon 2 av det grunnleggende BBS-formatet (Storbritannia fiktiv), som er basert på versjon 1 av datamodellen Betalinger (forenklet modell).  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Teste det egendefinerte formatet for generering av betalingsfiler
Fullfør trinnene i fremgangsmåten "Bruke opprettet format til å generere elektroniske dokumenter for betalinger" i en parallel Finance and Operations-økt. Velg det opprettede BBS-formatet (Storbritannia fiktiv egendefinert) i parametere for elektronisk betalingmåte. Kontroller at den opprettede betalingsfilen inneholder den nylig introduserte Proseware, Inc. XML-noden som presenterer IBAN-kontokode i henhold til områdekrav. Filen skal også inneholde den nylig introduserte Litware, Inc. XML-noden som presenterer SWIFT-bankkode i henhold til landkrav.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]