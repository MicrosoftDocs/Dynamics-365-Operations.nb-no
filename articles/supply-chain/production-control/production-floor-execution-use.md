---
title: Hvordan arbeidere bruker grensesnittet for produksjonsutførelse
description: Dette emnet beskriver hvordan du bruker grensesnittet for produksjonsutførelse fra synspunktet til en arbeider.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 38bc07d37b5c51f143846110c87cff9952d52b0e
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500796"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Hvordan arbeidere bruker grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Grensesnittet for produksjonsutførelse er optimalisert for berøringsinteraksjon. Utformingen gir visuell kontrast som oppfyller tilgjengelighetskravene for Shop Floor-miljøer. Den har alle de samme funksjonene som jobbkortenheten. Det gjør imidlertid også at flere jobber kan startes parallelt fra en jobbliste. (Denne funksjonen er også kjent som *bunting av jobber*). I tillegg kan arbeidere fra en jobbliste åpne en veiledning som ble opprettet i Microsoft Dynamics 365-veiledningen. På denne måten kan de finne en visuell veiledning i en HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Logge på grensesnittet for produksjonsutførelse som en arbeider

Før arbeidere kan begynne å bruke enheten, må en leder eller teknisk stab forberede den og åpne den riktige siden i Dynamics 365 Supply Chain Management. Hvis du vil ha mer informasjon om hvordan du definerer enheten, kan du se [Definere en enhet for å kjøre grensesnittet for produksjonsutførelse](production-floor-execution-setup.md).

Når enheten er forberedt, vises påloggingssiden på den. Denne siden viser informasjon om statusen for jobber for den lokale arbeidscellen. Denne informasjonen oppdateres med jevne mellomrom. På siden bruker arbeidere kort-IDer til å logge på. Selv om arbeidere ikke trenger å ha en brukerkonto for Supply Chain Management, må de ha en *tidregistrert arbeider*-konto de kan bruke når de logger på.

![Påloggingsside for grensesnittet for produksjonsutførelse](media/pfei-sign-in-page.png "Påloggingsside for grensesnittet for produksjonsutførelse")

De gjenværende delene i dette emnet beskriver hvordan arbeiderne samhandler med grensesnittet.

## <a name="all-jobs-tab"></a>fanen Alle jobber

fanen **Alle jobber** inneholder en jobbliste som viser alle produksjonsjobbene som har statusen *Ikke startet*, *Stoppet* eller *Startet*. (Dette fanenavnet kan tilpasses og kan være et annet for systemet ditt.)

![fanen Alle jobber](media/pfei-all-jobs-tab.png "fanen Alle jobber")

Jobblisten inneholder følgende kolonner: Tallene samsvarer med tallene i den forrige illustrasjonen.

1. **Velgerkolonne** – kolonnen lengst til venstre bruker hakemerker for å angi jobber som er valgt av arbeideren. Arbeidere kan velge flere jobber i listen samtidig. Hvis du vil velge alle jobbene i listen, merker du av i kolonneoverskriften. Når en enkelt jobb er valgt, vises detaljer om denne jobben i den nedre delen av siden.
1. **Jobbstatuskolonne** – denne kolonnen bruker symboler for å angi statusen for hver jobb. Jobber som ikke har symbol i denne kolonnen, har statusen *ikke startet*. En grønn trekant angir jobber med statusen *startet*. To gule loddrette linjer angir jobber som har statusen *stoppet*.
1. **Kolonne med høy prioritet** – denne kolonnen bruker utropstegn for å angi jobber med høy prioritet.
1. **Ordre** – denne kolonnen viser produksjonsordrenummeret for en jobb.
1. **Beskrivelse** – denne kolonnen viser en beskrivelse av operasjonen som en jobb er en del av.
1. **Ønsket** – denne kolonnen viser antallet som det er planlagt at en jobb skal produsere.
1. **Startet** – denne kolonnen viser antallet som allerede er startet for en jobb.
1. **Fullført** – denne kolonnen viser antallet som allerede er fullført for en jobb.
1. **Kassert** – denne kolonnen viser antallet som allerede er kassert for en jobb.
1. **Gjenstående** – denne kolonnen viser antallet som det gjenstår å fullføre for en jobb.

## <a name="active-jobs-tab"></a>Aktive jobber-fanen

**Aktive jobber**-fanene viser en liste over alle jobber som den påloggede arbeideren allerede har startet. (Dette fanenavnet kan tilpasses og kan være et annet for systemet ditt.)

![Aktive jobber-fanen](media/pfei-active-jobs-tab.png "Aktive jobber-fanen")

Listen over aktive jobber inneholder følgende kolonner:

- **Velgerkolonne** – kolonnen lengst til venstre bruker hakemerker for å angi jobber som er valgt av arbeideren. Arbeidere kan velge flere jobber i listen samtidig. Hvis du vil velge alle jobbene i listen, merker du av i kolonneoverskriften. Når en enkelt jobb er valgt, vises detaljer om denne jobben i den nedre delen av siden.
- **Ordre** – denne kolonnen viser produksjonsordrenummeret for en jobb.
- **Beskrivelse** – denne kolonnen viser en beskrivelse av operasjonen som en jobb er en del av.
- **Ønsket** – denne kolonnen viser antallet som det er planlagt at en jobb skal produsere.
- **Startet** – denne kolonnen viser antallet som allerede er startet for en jobb.
- **Fullført** – denne kolonnen viser antallet som allerede er fullført for en jobb.
- **Kassert** – denne kolonnen viser antallet som allerede er kassert for en jobb.
- **Gjenstående** – denne kolonnen viser antallet som det gjenstår å fullføre for en jobb.

## <a name="my-machine-tab"></a>Min maskin-fanen

I **Min maskin**-fanen kan arbeidere velge et aktivum som er koblet til en maskinressurs i filteret som er angitt i **Alle jobber**-fanen. Arbeidere kan deretter vise statusen og tilstanden for det valgte aktivumet ved å lese verdier for opptil fire valgte tellere og lister over nylige meldinger og registrerte nedetider. Arbeidere kan også be om vedlikehold for det valgte aktivumet og registrere og redigere nedetid for maskinen. (Dette fanenavnet kan tilpasses og kan være et annet for systemet ditt.)
 
![Min maskin-fanen](media/pfei-my-machine-tab.png "Min maskin-fanen")

**Min maskin**-fanen har følgende kolonner. Tallene samsvarer med tallene i den forrige illustrasjonen.

1. **Maskinaktivum** – Velg maskinaktivumet du vil spore. Begynn med å skrive inn et navn du vil velge fra en liste over samsvarende aktiva, eller velg forstørrelsesglassikonet for å velge fra en liste over alle aktiva som er knyttet til ressursene som er i filteret for jobblisten.

    > [!NOTE]
    > Brukere av Supply Chain Management kan tilordne en ressurs til hvert aktivum etter behov på **Alle aktiva**-siden (ved å bruke rullegardinlisten **Ressurs** i **Anleggsmiddel**-fanen). Hvis du vil ha mer informasjon, kan du se [Opprette et aktivum](../asset-management/objects/create-an-object.md).

1. **Innstillinger** – Velg tannhjulikonet for å åpne en dialogboks der du kan velge hvilke tellere du vil vise for det valgte maskinaktivumet. Verdiene for disse tellerne vises øverst i **Aktivastyring**-fanen. På **Innstillinger**-menyen (som vises på skjermbildet nedenfor) kan du aktivere opptil fire tellere. For hver teller du vil aktivere, bruker du oppslagsfeltet øverst i flisen til å velge en teller. Oppslagsfeltet viser alle tellerne som er knyttet til aktivumet som er valgt øverst på **Aktivastyring**-siden. Angi at hver teller skal overvåke **Aggregert**-verdien eller den siste **Faktisk**-verdien for telleren. Hvis du for eksempel angir en teller som sporer hvor mange timer maskinen har kjørt, setter du den til **Aggregert**. Hvis du angir at en teller skal måle sist oppdaterte temperatur eller trykk, setter du den til **Faktisk**. Velg **OK** for å lagre innstillingene og lukke dialogboksen.

    ![Min maskin-fanen](media/pfei-my-machine-tab-settings.png "Min maskin-fanen")

1. **Be om vedlikehold** – Velg denne knappen for å åpne en dialogboks der du kan opprette en melding. Du kan gi en beskrivelse og en merknad. En bruker av Supply Chain Management blir gjort oppmerksom på forespørselen og kan deretter konvertere meldingen til en arbeidsordre for vedlikehold.
1. **Registrer nedetid** – Velg denne knappen for å åpne en dialogboks der du kan registrere nedetid for maskin. Du kan velge en årsakskode og angi en dato / et tidsrom for nedetiden. Registreringen av nedetid for maskin brukes til å beregne effektiviteten til maskinaktivumet.
1. **Vis eller rediger** – Velg denne knappen for å åpne en dialogboks der du kan redigere eller vise eksisterende poster for nedetid.


## <a name="starting-and-completing-production-jobs"></a>Starte og fullføre produksjonsjobber

Arbeidere starter en produksjonsjobb ved å velge en jobb i **Alle jobber**-fanen og deretter velge **Start jobb** for å åpne **Start jobb**-dialogboksen.

![Dialogboksen Start jobb](media/pfei-start-job-dialog.png "Dialogboksen Start jobb")

Arbeidere bruker **Start jobb**-dialogboksen til å bekrefte produksjonsantallet, og starter deretter jobben. Arbeidere kan justere antallet ved å merke av i **Antall**-feltet og deretter bruke det numeriske tastaturet som vises. Arbeidere velger deretter **Start** for å begynne å arbeide på jobben. Dialogboksen **Start jobb** lukkes, og jobben legges til i fanen **Aktive jobber**.

Arbeidere kan starte en jobb som har en hvilken som helst status. Når en arbeider starter en jobb som har statusen *ikke startet*, vises **Antall**-feltet i dialogboksen **Start jobb** først hele antallet. Når en arbeider starter en jobb som har statusen *Startet* eller *Stoppet* viser **Antall**-feltet først restantallet.

## <a name="reporting-good-quantities"></a>Rapportere korrekte antall

Når en arbeider fullfører eller delvis fullfører en jobb, kan de rapportere korrekte antall som ble produsert ved å velge en jobb i fanen **Aktive jobber** og deretter velge **Rapportfremdrift**. I dialogboksen **Rapportfremdrift** angir arbeideren deretter det korrekte antallet ved hjelp av det numeriske tastaturet. Antallet er tomt som standard. Når et antall er angitt, kan arbeideren oppdatere statusen for jobben til *pågår*, *stoppet* eller *fullført*.

![Dialogboksen Rapportfremdrift](media/pfei-report-progress-dialog.png "Dialogboksen Rapportfremdrift")

## <a name="reporting-scrap"></a>Rapportere svinn

Når en arbeider fullfører eller delvis fullfører en jobb, kan de rapportere svinn som ble produsert ved å velge en jobb i fanen **Aktive jobber** og deretter velge **Rapportere svinn**. I dialogboksen **Rapportere svinn** angir arbeideren deretter svinnantall ved hjelp av det numeriske tastaturet. Arbeideren velger også en årsak (*ingen*, *maskin*, *operatør* eller *materiale*).

![Dialogboksen Rapportere svinn](media/pfei-report-scrap-dialog.png "Dialogboksen Rapportere svinn")

## <a name="completing-a-job-and-starting-a-new-job"></a>Fullføre en jobb og starte en ny jobb

Vanligvis fullfører arbeidere en jobb ved å velge én eller flere gjeldende jobber i fanen **Aktive jobber** og deretter velge **Rapportfremdrift**. Deretter angir du antallet som ble produsert (korrekt antall), og setter statusen til *Fullført*. Hvis mer enn én jobb ble valgt, bruker en arbeider **Forrige** - og **Neste**-knappene til å flytte mellom dem. For å starte en ny jobb velger arbeideren den i fanen **Alle jobber** og velger deretter **Start jobb**.

En arbeider kan også starte en ny jobb mens den forrige jobben fremdeles er åpen. Igjen velger arbeideren den nye jobben i fanen **Alle jobber** og velger deretter **Start jobb**. I dette tilfellet informerer imidlertid dialogboksen **Start jobb** arbeideren om at de for øyeblikket arbeider med en jobb, og de må derfor enten stoppe eller fullføre denne jobben før de starter den nye jobben.

## <a name="working-on-multiple-jobs-in-parallel"></a>Arbeide med flere jobber parallelt

Én arbeider kan arbeide med flere jobber samtidig (det vil si parallelt). I dette tilfellet kalles samlingen av jobber som arbeideren arbeider med, en *jobbunt*. Arbeideren kan legge til nye jobber i bunten, eller fullføre én eller flere jobber i bunten. Følgende to scenarier viser hvordan en arbeider kan arbeide med jobber parallelt.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Scenario 1: En arbeider som ikke har noen aktive jobber, vil starte to jobber og arbeide med dem parallelt

Arbeideren velger de to jobbene i fanen **Alle jobber** og velger deretter **Start jobb**. Dialogboksen **Start jobb** viser begge valgte jobber, og arbeideren kan justere antallet som skal startes i hver jobb. Deretter bekrefter arbeideren dialogboksen og kan starte begge jobbene.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Scenario 2: En arbeider som har to aktive jobber, vil starte en tredje jobb, og arbeide på den parallelt med de to andre

Arbeideren velger den tredje jobben i fanen **Alle jobber** og velger deretter **Bunt**. I dialogboksen **Bunt** kan arbeideren justere antallet som skal startes. Deretter bekrefter arbeideren dialogboksen ved å velge **Bunt**.

## <a name="working-on-indirect-activities"></a>Arbeide på indirekte aktiviteter

Indirekte aktiviteter er aktiviteter som ikke er direkte knyttet til en produksjonsordre. Indirekte aktiviteter kan være fleksibelt definert, som beskrevet i [Definere indirekte aktiviteter for timeregistrering](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

For eksempel Shannon, en produksjonsarbeider hos Contoso, vil delta på et firmamøte, og møter regnes som en indirekte aktivitet. Et av følgende to scenarioer gjelder:

- **Shannon arbeider på én eller flere aktive jobber.** Shannon velger **Aktivitet**, identifiserer aktiviteten (møtet) og bekrefter valget. En melding som vises, informerer henne om at hun har pågående jobber. Fra meldingen kan Shannon velge å fullføre eller stoppe jobbene som hun arbeider med før hun går til møtet.
- **Shannon har ingen aktive jobber.** Shannon velger **Aktivitet**, identifiserer aktiviteten (møtet) og bekrefter valget. Hun er nå registrert som å være på møtet.

I begge scenarioene, etter at Shannon bekrefter sitt valg, går hun enten til påloggingssiden eller en side som venter på at hun skal bekrefte at hun har returnert fra den indirekte aktiviteten. Hvilken side som vises, er avhengig av konfigurasjonen av grensesnittet for produksjonsutførelse. (Hvis du vil ha mer informasjon, kan du se [Konfigurere grensesnittet for produksjonsutførelse](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Registrere pauser

Arbeidere kan registrere pauser. Pauser kan være fleksibelt definert, som beskrevet i [Lønn basert på registreringer](pay-based-on-registrations.md).

En arbeider registrerer en pause ved å velge **Pause** og deretter velge kortet som representerer pausetypen (for eksempel lunsj). Når arbeideren har bekreftet valget, viser enheten enten påloggingssiden eller en side som venter på at arbeideren skal bekrefte at de er returnert fra pausen. Hvilken side som vises, er avhengig av konfigurasjonen av grensesnittet for produksjonsutførelse. (Hvis du vil ha mer informasjon, kan du se [Konfigurere grensesnittet for produksjonsutførelse](production-floor-execution-configure.md).)

## <a name="opening-instructions"></a>Åpne instruksjoner

Arbeidere kan åpne et dokument som er knyttet til en jobb, ved å velge **Instruksjoner**. Knappen **Instruksjoner** er bare tilgjengelig hvis et dokument er knyttet til jobben i hoveddataene. Et dokument som er knyttet til et produkt på siden **Frigitte produkter** i Supply Chain Management, vil for eksempel være tilgjengelig for arbeidere for åpning i kjøringsgrensesnittet for produksjon.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Åpne blandet virkelighet-veiledninger for HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kan bidra til å gi de ansatte praktisk læring som bruker blandet virkelighet. Du kan definere standardiserte prosesser der trinnvise instruksjoner leder de ansatte til verktøyene og delene de trenger, og viser de ansatte hvordan de skal bruke disse verktøyene i virkelige situasjoner. Her er en oversikt over prosessen.

1. Hver gang en arbeider åpner en jobbliste i kjøringsgrensesnittet for produksjon, finner grenesnittet alle de relevante veiledningene for jobbene som vises.
1. Arbeideren velger **Veiledninger** for å vise listen over veiledninger.
1. Arbeideren velger en relevant veiledning i listen.
1. Kjøringsgrensesnittet for produksjon viser en QR-kode for den valgte veiledningen.
1. Arbeideren tar på en HoloLens og ser på QR-koden for å starte veiledningen.
1. Arbeideren jobber seg gjennom veiledningen for å lære oppgaven.

Hvis du vil ha mer informasjon om hvordan du oppretter, tilordner og bruker veiledninger for HoloLens, kan du se [Formidle veiledninger for blandet virkelighet for arbeidere i produksjonen](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]