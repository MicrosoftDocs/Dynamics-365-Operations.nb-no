---
title: Behandling av distribuert ordre (DOM)
description: Dette emnet beskriver DOM-funksjonaliteten i Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 442a7449e0b28e1086d50ab68dbaf85370fce8ea6e178dd91ad972a2b47d7de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717703"
---
# <a name="distributed-order-management-dom"></a>Behandling av distribuert ordre (DOM)

[!include [banner](includes/banner.md)]

I dette nye paradigmet for handelsoperasjoner forsøker forhandlere å formidle tilpasset kundeengasjement, omnikanalopplevelser og problemfrie samhandlinger. Veldig mange alternativer er tilgjengelige, og derfor vil brukerne handle der de får den beste opplevelsen. I mange tilfeller er priser og produkter ikke lenger de mest avgjørende faktorene for forbrukere.

For å forbedre kundeopplevelsen må forhandlerne ha oversikt over lagerbeholdningen i sanntid på tvers av alle kanalene sine. En enkel helhetlig oversikt over hele beholdningen kan bidra til å optimalisere oppfyllelse av ordre, fordeling og distribusjon. Derfor blir bruk og implementering av et DOM-system stadig viktigere for forhandlere.

DOM optimaliserer oppfyllelse av ordrer på tvers av et avansert nettverk av systemer og prosesser. Det avhenger av én global visning av beholdningen på tvers av hele organisasjonen for å administrere ordrer på en smart måte, slik at de blir oppfylt nøyaktig og på en mer kostnadseffektiv måte. Ved å forbedre effektiviteten til en forhandlers forsyningskjede, bidrar DOM til at forhandleren oppfyller kundeforventninger på en bedre måte.

Illustrasjonen nedenfor viser livssyklusen til en salgsordre i et DOM-system.

![Livssyklus for salgsordre i konteksten til DOM.](./media/flow.png "Livssyklus for salgsordre i konteksten til DOM")

## <a name="set-up-dom"></a>Definer DOM

1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
2. Vis **Handel**-noden i fanen **Konfigurasjonsnøkler**, og merk deretter av for **Behandling av distribuert ordre**.
3. Gå til **Detaljhandel og handel \> Behandling av distribuert ordre \> Oppsett \> DOM-parametere**.
4. Angi følgende verdier i fanen **Generelt**:

    - **Aktiver behandling av distribuert ordre** – Sett dette alternativet til **Ja**.
    - **Bekreft bruk av Bing-kart for DOM** – Sett dette alternativet til **Ja**.


        > [!NOTE]
        > Du kan sette dette alternativet til **Ja** bare hvis alternativet **Aktiver Bing-kart** i fanen **Bing-kart** på siden **Delte handelsparametere** (**Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**) også er satt til **Ja**, og hvis en gyldig nøkkel er angitt i feltet **Nøkkel for Bing-kart**.
        >
        > Med portalen [Utviklersenter for Bing-kart](https://www.bingmapsportal.com/) kan du begrense tilgangen på API-nøklene for Bing-kart til et sett med domener du angir. Ved hjelp av denne funksjonen kan kunder definere et strengt sett med referanseverdier eller IP-adresseområder som nøkkelen vil bli validert mot. Forespørsler som stammer fra tillatelseslisten din, behandles på vanlig måte, mens forespørsler utenfra listen din vil returnere en tilgang som ikke fikk svar. Det er valgfritt å legge til domenesikkerhet i API-nøkkelen, og nøkler som forblir uendret, vil fortsette å fungere. Tillatelseslisten for en nøkkel er uavhengig av alle de andre nøklene, noe som gjør at du kan ha atskilte regler for hver av nøklene dine. Distribuert ordrebehandling støtter ikke oppsett av domeneegenskaper som det refereres til.


    - **Oppbevaringsperiode i dager** – Angi hvor lenge oppfyllelsesplanene som DOM-kjøringer genererer, skal beholdes i systemet. Den satsvise jobben **Oppsett for jobb for sletting av DOM-oppfyllelsesdata** sletter alle oppfyllelsesplaner som er eldre enn antallet dager du angir her.
    - **Avvisningsperiode (i dager)** – Angi hvor lang tid det må gå før en avvist ordrelinje kan tilordnes til samme lokasjon.

5. Angi følgende verdier i fanen **Problemløser**:

    - **Maksimalt antall forsøk på automatisk oppfyllelse** – Angi hvor mange ganger DOM-motoren skal forsøke å formidle en ordrelinje til en lokasjon. Hvis DOM-motoren ikke kan formidle en ordrelinje til en lokasjon på det angitte antallet forsøk, blir ordrelinjen flagget som et unntak. Motoren vil deretter hoppe over den linjen i senere kjøringer til statusen tilbakestilles manuelt.
    - **Områderadius for lokal butikk** – Angi en verdi. Dette feltet bidrar til å fastslå hvordan lokasjoner blir gruppert og vurdert som like når det gjelder avstand. Hvis du for eksempel angir **100**, vurderes hver butikk eller distribusjonssenter innen en avstand på 100 km av oppfyllelsesadressen som like når det gjelder avstand.
    - **Problemløsertype** – Velg en verdi. To typer i problemløsere følger med Commerce: **Produksjonsproblemløser** og **Forenklet problemløser**. For alle maskiner som kjører DOM (det vil si alle servere som er en del av DOMBatch-gruppen), må **Produksjonsproblemløser** velges. Produksjonsproblemløseren krever den spesielle lisensnøkkelen som er lisensiert og distribuert i produksjonsmiljøer som standard. For ikke-produksjonsmiljøer må denne lisensnøkkelen distribueres manuelt. Hvis du vil distribuere lisensnøkkelen manuelt, gjør du følgende:

        1. I Microsoft Dynamics Lifecycle Services åpner du det delte aktivabiblioteket, velger **Modell** som aktivatype og laster ned **DOM-lisensfilen**.
        1. Start Microsoft IIS-behandling, høyreklikk på **AOSService-nettsted**, og velg deretter **Utforsk**. Et Windows Utforsker-vindu åpnes på **\<AOS service root\>\\webroot**. Noter deg banen for \<AOS Service root\> fordi du skal bruke den i neste trinn.
        1. Kopier konfigurasjonsfilen i katalogen **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin**.
        1. Gå til klienten Hovedkvarter og åpne siden **DOM-parametere**. Velg **Produksjonsproblemløser** i feltet **Problemløsertype** i fanen **Problemløser**, og bekreft at det ikke vises noen feilmeldinger.


        > [!NOTE]
        > Den forenklede problemløseren blir formidlet slik at forhandlere kan teste DOM-funksjonen uten å måtte distribuere spesiallisensen. Organisasjoner bør ikke bruke den forenklede problemløseren i produksjonsmiljøer.
        >
        > Produksjonsproblemløseren forbedrer ytelse (for eksempel hvor mange ordrer og ordrelinjer som kan behandles i en kjøring) og sammenfall av resultater (ettersom en bunke med ordrer kanskje ikke gir det beste resultatet i noen scenarioer). Noen regler, for eksempel regelen **Delvise ordrer** og regelen **Maksimalt antall steder** krever produksjonsproblemløseren.
     
6. Gå tilbake til **Retail og Commerce \> Behandling av distribuert ordre \> Oppsett \> DOM-parametere**.
7. I fanen **Nummerserier** tilordner du de nødvendige nummerseriene for de ulike DOM-enhetene.

    > [!NOTE]
    > Før nummerseriene kan tilordnes til enheter, må de defineres på siden **Nummerserier** (**Organisasjonsstyring \> Nummerserier \> Nummerserier**).

8. DOM-funksjonen støtter definisjonen av ulike typer DOM-regler, og organisasjoner kan konfigurere flere regler, avhengig av deres forretningsbehov. DOM-regler kan defineres for en gruppe med lokasjoner eller individuelle lokasjoner, og for en bestemt produktkategori, produkt eller variant. Hvis du vil opprette gruppering av lokasjoner som må brukes for DOM-reglene, gjør du følgende:

    1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Oppfyllelsesgrupper**.
    2. Velg **Ny**, og angi et navn og en beskrivelse for den nye gruppen.
    3. Velg **Lagre**.
    4. Velg **Legg til linje** for å legge til ett lokasjon i gruppen. Velg eventuelt **Legg til linjer** for å legge til flere lokasjoner.
    
    > [!NOTE]
    > I Commerce versjon 10.0.12 og høyere må **muligheten til å angi lokasjoner, som Forsendelse eller Plukking, som er aktivert i en oppfyllelsesgruppe**, være aktivert i arbeidsområdet **Funksjonsbehandling**.
    >
    > Denne funksjonen legger til nye konfigurasjoner på siden **Oppfyllelsesgruppe** slik at du kan definere om lageret kan brukes til forsendelse, eller om kombinasjonen lager/butikk kan brukes til forsendelse, plukking eller begge deler. 
    >
    > Hvis du aktiverer funksjonen, oppdateres alternativene som er tilgjengelige for lokasjonsvalg når du oppretter plukk- eller forsendelsesordrer på salgsstedet.
    >
    > Når du aktiverer funksjonen, blir også sider i salgsstedsoperasjoner oppdatert når operasjonen Send alle eller Send valgte blir valgt.

9. Hvis du vil definere regler, går du til **Detaljhandel og handel \> Behandling av distribuert ordre \> Oppsett \> Administrer regler**. Følgende DOM-regler støttes for øyeblikket:

    - **Regel for minimumslager** – Denne regeltypen lar organisasjoner "ringe inn" et bestemt antall av et produkt for andre formål enn oppfyllelse av ordren. Organisasjoner vil for eksempel ikke at DOM skal vurdere hele beholdningen som er tilgjengelig i en butikk for oppfyllelse av ordren. De vil i stedet reservere deler av beholdningen for butikkunder. Når denne regeltypen brukes, kan du definere minimumslageret som skal beholdes for en kategori av produkter, et individuelt produkt eller en produktvariant per lokasjon eller gruppe med lokasjoner.
    - **Prioritetsregel for oppfyllelseslokasjon** – Denne regeltypen lar organisasjoner definere et hierarki av lokasjoner for å opprette prioriteten som DOM-motoren vurderer når den prøver å identifisere oppfyllelseslokasjoner for bestemte produkter. Det gyldige området av prioriteter er 1 til 10, der 1 er den høyeste prioriteten og 10 er den laveste prioriteten. lokasjoner som har høyere prioritet, vurderes før lokasjoner som har lavere prioritet. Hvis regelen er definert som en regel med hard begrensning, formidles ordrer bare til lokasjoner som prioriteter er definert for.
    - **Regel for delvise ordrer** – Denne regelen lar organisasjoner definere om en ordre eller ordrelinjer delvis kan oppfylles. Følgende parametere er tilgjengelige:

        - **Oppfylle delvise ordrer?** – Hvis dette alternativet er satt til **Ja**, kan DOM oppfylle bare en del av antallet på en ordrelinje. Denne delvise oppfyllelsen oppnås ved å dele opp ordrelinjen.
        - **Oppfylle delvise linjer?** – Hvis dette alternativet er satt til **Ja**, kan DOM oppfylle et delvist antall ordrelinjer. Denne delvise oppfyllelsen oppnås ved å dele opp ordrelinjen.
        - **Bare oppfylle ordre fra én lokasjon?** – Hvis dette alternativet er satt til **Ja**, sørger DOM for at alle linjer i en ordre blir oppfylt fra ett lokasjon.


        Tabellen nedenfor forklarer virkemåten når en kombinasjon av disse parameterne er definert.

        | Kombinasjonsnummer | Oppfylle delvise ordrer | Oppfylle delvise linjer | Bare oppfylle ordre fra én lokasjon | Beskrivelse |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Ja                    | Ja                   | Ja                                  | Noen få linjer i ordren kan oppfylles, og enkeltlinjer kan delvis oppfylles, men alle linjene må være fra samme lokasjon i en forekomst av DOM-kjøringen. (Denne kombinasjonen støttes for øyeblikket ikke.) |
        | 2    | Ja                    | Nei                    | Ja                                  | Noen få linjer i ordren kan oppfylles, men enkeltlinjer kan ikke delvis oppfylles, og alle de oppfylte linjene må være fra samme lokasjon i en forekomst av DOM-kjøringen. (Denne kombinasjonen støttes for øyeblikket ikke.) |
        | 3    | Ja                    | Ja                   | Nei                                   | Noen få linjer i ordren kan oppfylles, enkeltlinjer kan ikke delvis oppfylles, og hver linje kan oppfylles fra mer enn ett lokasjon i en forekomst av DOM-kjøringen. |
        | 4\*  | Nei                     | Gjelder ikke        | Nei                                   | Alle ordrelinjer må oppfylles, individuelle linjer ikke kan oppfylles delvis, og hver ordrelinje kan oppfylles fra en annen lokasjon. |
        | 5\*  | Nei                     | Gjelder ikke        | Ja                                  | Alle ordrelinjer må oppfylles, individuelle linjer ikke kan oppfylles delvis, og alle ordrelinjene kan leveres fra bare ett lokasjon. |
        | 6\*  | Nei                     | Gjelder ikke        | Nei                                   | Denne kombinasjonen fungerer som kombinasjon 4, fordi **Oppfyll delvise linjer** ikke kan settes til **Ja** når **Oppfyll delvise ordrer** er satt til **Nei**. |
        | 7\*  | Nei                     | Gjelder ikke        | Ja                                  | Denne kombinasjonen fungerer som kombinasjon 5, fordi **Oppfyll delvise linjer** ikke kan være **Ja** når **Oppfyll delvise ordrer** er **Nei**. |
        | 8    | Ja                    | Nei                    | Nei                                   | Noen få linjer i ordren kan oppfylles, men enkeltlinjer kan ikke delvis oppfylles, og de ulike ordrelinjene kan oppfylles fra mer enn ett lokasjon i en forekomst av DOM-kjøringen. |
        | 9\*  | Nei                     | Gjelder ikke        | Ja                                  | Alle ordrelinjer må oppfylles, og alle ordrelinjene må oppfylles fra bare ett lokasjon. |

        \* Hvis **Oppfyll delvise ordrer** er satt til **Nei**, vil **Oppfyll delvise linjer** alltid bli vurdert til å settes til **Nei**, uavhengig av hvordan verdien faktisk er satt.

        > [!NOTE]
        > I Retail versjon 10.0.5 ble verdien for parameteren **Bare oppfylle ordre fra én lokasjon** endret til **Maksimale oppfyllelseslokasjoner**. I stedet for å tillate at en bruker konfigurerer om ordrer bare kan oppfylles fra én lokasjon, eller oppfylles fra så mange lokasjoner som mulig, kan brukere nå angi om oppfyllelse kan være fra et bestemt sett med lokasjoner (opptil 5) eller fra så mange steder som den kan oppfylles. Dette gir større fleksibilitet når det gjelder hvor mange lokasjoner ordren kan oppfylles fra. Denne regelen fungerer bare med produksjonsproblemløseren. 

   - **Regel for frakoblet oppfyllelseslokasjon** – Denne regelen lar organisasjoner angi en lokasjon eller en gruppe lokasjoner som frakoblet eller utilgjengelig for DOM, slik at ordrer ikke kan tilordnes til de lokasjonene for oppfyllelse.
    - **Regel for maksimalt antall avvisninger** – Denne regelen lar organisasjoner definere en terskel for avvisninger. Når terskelen er nådd, vil DOM-prosessoren merke en ordre eller en ordrelinje som et unntak, og utelate den fra videre behandling.

        Etter at ordrelinjene er tilordnet til en lokasjon, kan lokasjonen avvise en tilordnede ordrelinje, fordi lokasjonen kanskje ikke kan oppfylle den linjen av en eller annen grunn. Avviste linjer blir merket som et unntak, og de blir lagt tilbake i utvalget for behandling i den neste kjøringen. I løpet av den neste kjøringen vil DOM prøve å tilordne den avviste linjen til en annen lokasjon. Den nye lokasjonen kan også avvise den tilordnede ordrelinjen. Denne syklusen med tilordning og avslag kan forekomme flere ganger. Når antallet avvisninger når terskelen som er definert, vil DOM markere ordrelinjen som et fast unntak, og linjen vil ikke bli valgt flere ganger for ny tilordning. DOM vil vurdere ordrelinjen en gang til for ny tilordning bare hvis en bruker tilbakestiller statusen for ordrelinjen manuelt.

   - **Regel for maksimal avstand** – Denne regelen lar organisasjoner definere maksimumsavstanden som en lokasjon eller gruppe med lokasjoner kan være for å oppfylle ordren. Hvis overlappende regler for maksimal avstand er definert for en lokasjon, bruker DOM den laveste maksimumsavstanden som er definert for den lokasjonen.
    - **Regel for maksimalt antall ordrer** – Denne regelen lar organisasjoner definere det maksimale antallet ordrer som en lokasjon eller gruppe med lokasjoner kan behandle i løpet av en dag i kalenderen. Hvis det maksimale antallet ordrer er tilordnet til en lokasjon på én dag, vil ikke DOM tilordne flere ordrer til den lokasjonen resten av den kalenderdagen.

   Her er noen av de vanlige attributtene som kan defineres for alle de foregående regeltypene:

   - **Startdato** og **Sluttdato** – Hver regel kan gjøres datoeffektiv ved hjelp av disse feltene.
   - **Deaktivert** – Bare regler som har verdien **Nei** for dette feltet, blir vurdert i en DOM-kjøring.
   - **Hard begrensning** – En regel kan defineres som en hard begrensning eller ikke en hard begrensning. Alle DOM-kjøringer går gjennom to gjentakelser. I den første gjentakelsen behandles hver regel som en regel med hard begrensning, uavhengig av innstillingen til dette feltet. Med andre ord blir hver regel brukt. Det eneste unntaket er regelen **Prioritet for lokasjon**. I den andre gjentakelsen fjernes reglene som ikke ble definert som regler for hard begrensning, og ordren eller ordrelinjene som ikke ble tilordnet til lokasjoner da alle reglene ble tatt i bruk, blir tilordnet til lokasjoner.

10. Oppfyllelsesprofiler brukes til å gruppere en samling med regler, juridiske enheter, salgsordreopprinnelser og leveringsmåter. Alle DOM-kjøringer gjelder for en bestemt oppfyllelsesprofil. På denne måten kan organisasjoner definere og kjøre et sett med regler for et sett med juridiske enheter for ordrer som har bestemte salgsordreopprinnelser og leveringsmåter. Hvis ulike sett med regler må kjøres for ulike typer salgsordreopprinnelser eller leveringsmåter, kan oppfyllelsesprofilene derfor defineres i henhold til dette. Gjør følgende for å konfigurere oppfyllelsesprofiler:  

    1. Gå til **Detaljhandel og handel \> Behandling av distribuert ordre \> Oppsett \> Oppfyllelsesprofiler**.
    2. Velg **Ny**.
    3. Angi verdier i feltene **Profil** og **Beskrivelse**.
    4. Velg alternativet **Bruk resultat automatisk**. Hvis du setter dette alternativet til **Ja**, blir resultatene av DOM-kjøringen for profilen brukt automatisk på salgsordrelinjer. Hvis du setter det til **Nei**, kan resultatene bare vises i oppfyllelsesplanen. De brukes ikke på salgsordrelinjene.
    5. Hvis du vil at DOM-profilen skal kjøres for ordrer som har alle salgsordreopprinnelser, inkludert ordrer der salgsordreopprinnelsen ikke er definert, setter du alternativet **Behandle ordrer med tom salgsopprinnelse** til **Ja**. Hvis du vil kjøre profilen for bare noen få salgsordreopprinnelser, kan du definere dem på siden **Salgsopprinnelser**, som forklart senere.

    > [!NOTE]
    > I Commerce versjon 10.0.12 og høyere må **muligheten til å tilordne en oppfyllelsesgruppe til en oppfyllelsesprofil** være aktivert i arbeidsområdet **Funksjonsbehandling**. 
    >
    > Denne funksjonen legger til en ny konfigurasjon på siden **Oppfyllelsesprofil** som kan knyttes til én oppfyllelsesgruppe. 
    >
    > Hvis du velger oppfyllelsesgruppen, vil DOM-reglene for den oppfyllelsesprofilen fungere effektivt i forhold til forsendelseslagrene som er inkludert i oppfyllelsesgruppen. 
    > 
    > Hvis du vil bruke denne funksjonen effektivt, må du kontrollere at det finnes én oppfyllelsesgruppe som inneholder alle forsendelsene, og deretter knytter du denne oppfyllelsesgruppen til oppfyllelsesprofilen.
    
    6. Velg **Legg til** i hurtigfanen **Juridiske enheter**, og velg deretter en juridisk enhet.
    7. Velg **Legg til** i hurtigfanen **Regler**, og velg deretter regelen som skal kobles til profilen.
    8. Gjenta de forrige to trinnene til alle de nødvendige reglene er knyttet til profilen.
    9. Velg **Lagre**.
    10. Velg **Leveringsmåter** i fanen **Oppsett** i handlingsruten.
    11. Velg **Ny** på siden **Leveringsmåter**.
    12. Velg den juridiske enheten i **Firma**-feltet. Listen over selskaper er begrenset til de juridiske enhetene du har lagt til tidligere.
    13. Velg leveringsmåten som skal knyttes til denne profilen, i feltet **Leveringsmåte**. En leveringsmåte kan ikke være knyttet til flere aktive profiler.
    14. Gjenta de forrige to trinnene til alle de nødvendige leveringsmåtene er knyttet til profilen.
    15. Lukk siden **Leveringsmåter**.
    16. Velg **Salgsordreopprinnelser** i fanen **Oppsett** i handlingsruten.
    17. Velg **Ny** på siden **Salgsopprinnelser**.
    18. Velg den juridiske enheten i **Firma**-feltet. Listen over selskaper er begrenset til de juridiske enhetene du har lagt til tidligere.
    19. Velg salgsopprinnelsen skal knyttes til denne profilen, i feltet **Salgsopprinnelse**. En salgsopprinnelse kan ikke være knyttet til flere aktive profiler.
    20. Gjenta de forrige to trinnene til alle de nødvendige salgsopprinnelsene er knyttet til profilen.
    21. Lukk siden **Salgsopprinnelse**.
    22. Sett alternativet **Aktiver profil** til **Ja**. Hvis det finnes feil i oppsettet, mottar du en advarsel.

## <a name="dom-processing"></a>DOM-behandling

DOM kjøres bare i en satsvis jobb. Hvis du vil konfigurere den satsvise jobben for DOM-kjøringer, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Behandling av distribuert ordre \> Satsvis behandling \> Oppsett for DOM-prosessorjobb**.
1. Velg en profil som DOM må kjøres for, i feltet **Oppfyllelsesprofil** i hurtigfanen **Parametere**.
1. Velg en konfigurert satsvis gruppe i feltet **Satsvis gruppe** i hurtigfanen **Kjør i bakgrunnen**.
1. Skriv inn et navn for den satsvise jobben i feltet **Oppgavebeskrivelse**.
1. Velg **Regelmessighet** og definer regelmessigheten for den satsvise jobben.
1. Velg **OK**.

Under behandling vil DOM vurdere ordren og ordrelinjene som beskrevet her:

- Ordrelinjer som oppfyller kriteriene for salgsordreopprinnelse, leveringsmåter og juridisk enhet, slik det er definert i DOM-profilen, og som også oppfyller noen av disse kriteriene:

    - De er opprettet fra handelskanaler.
    - De har aldri blitt formidlet av DOM.
    - De har blitt formidlet av DOM før, men de er merket som unntak, og er lavere enn den maksimale terskelen for forsøk.
    - Leveringsmåten ikke henting eller elektronisk levering.
    - De er ikke merket for levering.
    - De er ikke utelatt manuelt.

- Ordrer som ikke er på vent

Etter at DOM har tatt i bruk reglene, lagerbegrensningene og optimaliseringen, velges lokasjonen som er nærmest kundens leveringsadresse.

![Salgsordrekriterier.](./media/ordercriteria.png "Salgsordrekriterier")

## <a name="results-of-dom-runs"></a>Resultater av DOM-kjøringer

Hvis oppfyllelsesprofilen er satt til **Bruk automatisk**, vil resultatene av kjøringen brukes automatisk på salgsordrelinjene, og oppfyllelsesplanen kan vises separat. Hvis oppfyllelsesprofilen imidlertid ikke er satt til **Bruk automatisk**, kan resultatene av kjøringen bare ses fra visningen av oppfyllelsesplanen. 

Hvis du vil vise alle oppfyllelsesplanene som er generert, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Behandling av distribuert ordre \> Behandling av distribuert ordre**.
2. Velg flisen **Oppfyllelsesplaner** i arbeidsområdet **Behandling av distribuert ordre**.
3. Velg IDen for den aktuelle ordreoppfyllelsesplanen for å vise oppfyllelsesplanen.

    Delen med ordredetaljer for oppfyllelsesplanen viser de opprinnelige salgsordrelinjene som var en del av kjøringen. I tillegg til de standard feltene på salgsordrelinjen, inneholder delen med ordredetaljer også følgende tre DOM-relaterte felt:

    - **Oppfyllelsestype** – Dette feltet angir om ordrelinjene er fullstendig formidlet, delvis formidlet eller ikke formidlet i det hele tatt til en lokasjon.
    - **Deling** – Dette feltet angir om en salgsordrelinje har blitt delt og formidlet til forskjellige lokasjoner.
    - **Antall oppfyllelseslokasjoner** – Dette feltet angir hvor mange oppfyllelseslinjer som ble opprettet for en salgsordrelinje (basert på antallet lokasjoner som den opprinnelige salgsordrelinjen ble formidlet til).

    Delen med ordreoppfyllelsesdetaljer viser tilordningen av de opprinnelige salgsordrelinjene til ulike lokasjoner, sammen med deres antall.

## <a name="order-line-actions-and-statuses"></a>Handlinger og statuser for ordrelinje

Følgende beskriver innstillinger på ordrelinjen. Hvis du vil åpne ordrelinjen, går du til **Detaljhandel og handel \> Kunder \> All salgsordrer**.
- Hvis du setter alternativet **Utelat fra DOM-behandling** i fanen **Generelt** på salgsordrelinjen til **Ja**, blir ordren eller ordrelinjen utelatt fra DOM-behandlingen.
- Feltet **DOM-status** i fanen **Generelt** for salgsordrelinjen kan settes til én av følgende verdier:

    - **Ingen** – Ordrelinjen har aldri blitt formidlet.
    - **Fullført** – Ordrelinjen er formidlet og knyttet til en lokasjon.
    - **Unntak** – Ordrelinjen er formidlet, men kan ikke knyttes til en lokasjon. Unntak har flere undertyper som kan vises i DOM-arbeidsområdet:

        - **Antall ikke tilgjengelig** – Det finnes ingen tilgjengelig lagerbeholdning for å tilordne ordren til lokasjonene.
        - **Maksimalt antall avvisninger** – Ordrelinjen har nådd maksimalterskelen for avvisninger.
        - **Dataendringskonflikt** – Salgsordrelinjen er endret siden ordren ble formidlet. Derfor kan ikke oppfyllelsesplanen brukes i ordren.
        - **Spesifikt unntak for ordrelinje** – Det finnes flere unntak på ordrelinjen.

- Under registrering av salgsordren, kan DOM kjøres i en interaktiv modus. Mens du registrerer en ordrelinje, kan du velge **Oppdater linje** etter at du har angitt produkt og antall, og deretter velger du **Foreslå oppfyllelseslokasjon** under **DOM**. Dermed vises det en liste over lokasjoner som er basert på DOM-regler som kan oppfylle antallet på ordrelinjen. Denne listen er sortert etter avstand. Velg en lokasjon for å angi det aktuelle området og lageret på salgsordrelinjen. For at denne funksjonen skal fungere, må det finnes en eksisterende, aktiv oppfyllelsesprofil som samsvarer med salgsopprinnelsen og leveringsmodusen på salgslinjen.
- Hvis du vil vise DOM-kjøringsloggene for en salgsordrelinje, velger du **Salgsordrelinje**, og deretter velger du **Vis DOM-logger** under **DOM**. DOM-loggene viser alle hendelsene og loggene som ble generert av DOM-kjøringen. Loggene kan hjelpe deg med å forstå hvorfor en bestemt lokasjon ble tilordnet til ordrelinjen, og hvilke regler og begrensninger som ble vurdert som en del av tilordningen. DOM-loggene er også tilgjengelige i fanen **Behandle** på nivå i salgsordrehodet.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Kjøre en oppryddingsjobb for DOM-oppfyllelsesplaner

Mens DOM-behandlingen kjører, opprettes oppfyllelsesplaner. Over tid vil systemet oppbevare mange oppfyllelsesplaner. Hvis du vil styre hvor mange oppfyllelsesplaner systemet oppbevarer, kan du konfigurere en satsvis jobb som sletter gamle oppfyllelsesplaner er basert på verdien **Oppbevaringsperiode i dager**.

1. Gå til **Detaljhandel og handel \> Behandling av distribuert ordre \> Satsvis behandling \> Oppsett for jobb for sletting av DOM-oppfyllelsesdata**. 
1. Velg en konfigurert satsvis gruppe i feltet **Satsvis gruppe**.
1. Velg **Regelmessighet** og definer regelmessigheten for den satsvise jobben.
1. Velg **OK**.

## <a name="more-information"></a>Mer informasjon

Her er et par ting du bør vurdere når du bruker DOM-funksjonen:

- DOM ser for øyeblikket bare på ordrer som er opprettet fra handelskanaler. Salgsordrer blir identifisert som salgsordrer når alternativet **Handelssalg** er satt til **Ja**.
- Microsoft har ikke testet DOM med avanserte lagerstyringsfunksjoner. Kunder og partnere må være forsiktige med å fastslå om DOM er kompatibel med de avanserte funksjonene og prosessene for lagerstyring som er relevante for dem.
- DOM er tilgjengelig bare på skyversjonen av Commerce. Funksjonen støttes ikke i lokale distribusjoner.


[!INCLUDE[footer-include](../includes/footer-banner.md)]