---
title: Definere kvalitetsordrer
description: "Denne fremgangsmåten viser hvordan du aktiverer en kvalitetsstyringsprosess der innkommende lager må kontrolleres umiddelbart etter ankomstregistrering."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-quality-orders"></a>Definere kvalitetsordrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du aktiverer en kvalitetsstyringsprosess der innkommende lager må kontrolleres umiddelbart etter ankomstregistrering. Fremgangsmåten vil vanligvis utføres av en kvalitetssjef. Prosessen omfatter oppretting av en kvalitetsgruppe, for å definere varene som skal testes, og en testgruppe for å gruppere testene som skal utføres, på varer i kvalitetsgruppen. Du kan kjøre denne veiledningen i demonstrasjonsdatafirmaet USMF.


## <a name="enable-quality-management"></a>Aktivere kvalitetsstyring
1. Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.
2. Klikk kategorien Kvalitetsstyring.
3. Sett alternativet Bruk kvalitetsstyring til Ja.
4. Klikk Rapportoppsett.
    * Rapportoppsett for kvalitetsstyring er allerede definert i USMF. Hvis dette ikke er gjort, kan du legge til nye linjer for de forskjellige rapporttypene og velg dokumenttypen som skal brukes for hver rapport.  
5. Lukk siden.
6. Lukk siden.

## <a name="create-a-test"></a>Opprette en test
1. Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Tester.
2. Klikk Ny.
3. Skriv inn en verdi i Test-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg Alternativ i Type-feltet.
    * I dette eksemplet velger vi "Alternativ" som vil gjøre det mulig å tilordne testresultatene basert på forhåndsdefinerte verdier.  
6. Klikk Lagre.
7. Lukk siden.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Opprette testvariabler for å definere hvordan testresultater registreres
1. Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Testvariabler.
2. Klikk Ny.
3. Skriv inn en verdi i Variabel-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Lagre.
6. Klikk Resultater.
7. Klikk Ny.
8. Skriv inn en verdi i Resultat-feltet.
9. Skriv inn en verdi i feltet Beskrivelse.
10. Velg Bestått i feltet Resultatstatus.
11. Klikk Lagre.
12. Klikk Ny.
13. Skriv inn en verdi i Resultat-feltet.
14. Skriv inn en verdi i feltet Beskrivelse.
15. Klikk Lagre.
16. Lukk siden.
17. Lukk siden.

## <a name="set-up-item-sampling"></a>Definere vareprøver
1. Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Vareprøve.
2. Klikk Ny.
3. Skriv inn en verdi i Vareprøve-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi et tall i Verdi-feltet.
    * Denne verdien er knyttet til spesifikasjonen av antall som er valgt i feltet ved siden av.  
6. Vis eller skjul delen Prosess.
7. Merk av for eller fjern merket for Full blokkering..
    * Hvis du velger dette alternativet, blokkeres hele parti- eller ordrelinjeantallet eller hvis en test mislyktes. Hvis du ikke merker den, blokkeres bare varene i kvalitetsordren.  
8. Klikk Lagre.
9. Lukk siden.

## <a name="create-a-quality-group"></a>Opprette en kvalitetsgruppe
1. Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Kvalitetsgrupper.
2. Klikk Ny.
3. Skriv inn en verdi i Kvalitetsgruppe-feltet.
    * Bruk et beskrivende navn som hjelper deg med å identifisere hvilken type varer gruppen inneholder (prøvekriterier).  
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Lagre.
6. Klikk Legg til varer.
7. Velg varenummerraden.
    * I dette eksemplet kjøres filtreringsfunksjonen basert på varenummeret.  
8. Skriv inn en verdi i Kriterier-feltet.
    * Skriv for eksempel T* for å filtrere på varenumrene som begynner med T.  
9. Klikk OK.
10. Klikk OK.
11. Klikk Varekvalitetsgrupper.
12. Lukk siden.
13. Lukk siden.

## <a name="create-a-test-group"></a>Opprette en testgruppe
1. Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Testgrupper.
2. Klikk Ny.
3. Skriv inn en verdi i Testgruppe-feltet.
    * Gi testgruppen et navn som hjelper deg med å huske hva slags tester som kjøres, og hvilke kvalitetsgruppe den skal være knyttet til. Hvis den for eksempel skal brukes med en kvalitetsgruppe som velger varer som begynner med "T", du kan kalle den "T-varetester".  
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg vareprøvelinjen som du opprettet før, i Vareprøve-feltet.
6. Finn og velg ønsket post i listen.
7. Klikk Legg til.
8. Angi et nummer i Sekvensnummer-feltet.
9. Velg testen du opprettet tidligere, i Test-feltet.
10. Finn og velg ønsket post i listen.
11. Klikk kategorien Test.
12. Velg testvariabelen du opprettet tidligere, i Variabel-feltet.
13. Finn og velg ønsket post i listen.
14. Klikk rullegardinknappen i Standardresultat-feltet for å åpne oppslaget.
15. Klikk koblingen i den valgte raden i listen.
16. Klikk Lagre.
17. Lukk siden.

## <a name="define-when-quality-orders-will-be-created"></a>Definere når kvalitetsordrer kan opprettes
1. Gå til Lagerstyring > Oppsett > Kvalitetskontroll > Kvalitetstilknytninger.
2. Klikk Ny.
3. Velg et alternativ i Referansetype-feltet.
4. Velg Gruppe i Varekode-feltet.
    * I dette eksemplet skal vi velge "Gruppe" og bruke kvalitetsgruppen vi opprettet før. Du kan også angi dette til "Tabell" for å angi varene manuelt, ellere velg "Alle" for å legge til alle varer i kvalitetsordren.  
5. I Vare-feltet velger du kvalitetsgruppen som du opprettet tidligere.
    * De tilgjengelige alternativene i Vare-feltet avhenger av hva du angir i Varekode-feltet.  
6. Finn og velg ønsket post i listen.
7. Vis eller skjul delen Prosess.
8. Velg et alternativ i Hendelsestype-feltet.
    * Dette er hendelsen som utløser testen. Alternativene som er tilgjengelig her, avhenger av hvilken prosess du valgte i feltet Referansetype.  
9. Velg et alternativ i Utførelse-feltet.
10. Vis eller skjul delen Kvalitetsordreprosess.
11. Klikk rullegardinknappen i feltet Hendelsesblokkering for å åpne oppslaget.
    * Dette feltet viser listen over prosesser som det er mulig å blokkere hvis kvalitetsordren fremdeles er åpen. Alternativene er avhengig av hva du valgte i feltet Hendelsestype.  
12. Klikk koblingen i den valgte raden i listen.
    * Dette vil være avhengig av de tidligere valgte verdiene. Velg om følgende prosesser må være blokkert mens du har åpne kvalitetsordrer som er koblet til en kildedokumentlinje.  
13. Vis eller skjul delen Spesifikasjoner.
14. Velg testgruppen du opprettet tidligere, i Testgruppe-feltet.
15. Finn og velg ønsket post i listen.
16. Klikk Lagre.
17. Lukk siden.

