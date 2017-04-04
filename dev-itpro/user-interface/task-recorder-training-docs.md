---
title: "Lage dokumentasjon eller opplæring ved hjelp av oppgaveopptak"
description: "Dette emnet forklarer hva Oppgaveregistrering og hjelpelinjer for aktiviteten er, hvordan du oppretter oppgaven innspillinger, og hvordan du tilpasser Microsoft aktivitet fører og inkludere dem i din hjelp."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Lage dokumentasjon eller opplæring ved hjelp av oppgaveopptak
Dette emnet forklarer hva Oppgaveregistrering og hjelpelinjer for aktiviteten er, hvordan du oppretter oppgaven innspillinger, og hvordan du tilpasser Microsoft aktivitet fører og inkludere dem i din hjelp.

<a name="learn-about-task-recorder"></a>Finn ut mer om oppgaveopptak
-------------------------

Oppgaveregistrering er en Microsoft Dynamics-365 for operasjoner verktøy som du kan bruke til å registrere handlingene som du utfører i brukergrensesnittet (UI) for produktet. Når du bruker oppgaveopptakeren, blir alt du gjør i brukergrensesnittet som kjøres mot serveren, for eksempel tilføying av verdier, endring av innstillinger og fjerning av verdier, tatt opp. Samlet kalles trinnene som du registrerer en *oppgaveregistrering*. Oppgaveopptak kan brukes på mange måter:

-   **Oppgaveopptak kan spilles av som oppgaveveiledninger.** Støttelinjer for aktiviteten er en integrert del av Dynamics-365 for operasjoner Hjelp-opplevelsen. En aktivitet guide er en kontrollert, veiledende, interaktiv opplevelse gjennom trinnene i en forretningsprosess. Brukeren blir veiledet gjennom hvert trinn ved hjelp av en popup-melding (eller «boble») som animeres i brukergrensesnittet og peker på elementet i brukergrensesnittet som brukeren skal bruke. "Boble" inneholder også informasjon om hvordan du arbeider med et element, for eksempel "Klikk her" eller "Angi en verdi i dette feltet." En veiledning for oppgaven kjøres mot brukerens gjeldende datasett og lagres dataene som er angitt i brukerens miljø.
-   **Aktivitet innspillinger kan vises som fremgangsmåter for trinnene i Hjelp-ruten.** Du kan bruke Hjelp-ruten for å søke etter og vise aktiviteten innspillinger. Du kan få tilgang til Hjelp-ruten ved å klikke på **?** Ikonet i det øverste navigasjonsfeltet, eller du kan bruke hurtigtastkombinasjonen, **Ctrl + Skift +?**. Du kan lese trinnene for en aktivitet registrere i Hjelp-ruten, eller du kan velge for å spille av innspillingen som en veiledning for aktiviteten slik at den leder deg gjennom Brukergrensesnittet.
-   **Du kan lagre oppgaveopptak i Forretningsprosessmodelerer.** Du kan lagre oppgaveopptaket på en linje i et hierarki i et Forretningsprosessmodelerer-bibliotek i Lifecycle Services (LCS). En liste over trinn og et flytskjema for forretningsprosess genereres fra opptaket. Aktivitet innspillinger som er lagret i et bibliotek for BPM kan vises i Dynamics 365 for operasjoner som hjelp.
-   **Du kan lagre oppgaveopptak som Word-dokumenter.** Dette gjør at du enkelt kan lage opplæringsveiledninger som skrives ut.

Du kan opprette din egen aktivitet innspillinger, spille aktiviteten innspillinger fra Microsoft eller endre innspillinger fra Microsoft oppgave for å gjenspeile din konfigurasjon. Hvis du vil ha mer informasjon om Oppgaveregistrering, se [Oppgaveregistrering i Dynamics 365 for drift](task-recorder.md).

## <a name="plan-your-task-recording"></a>Planlegge oppgaveopptaket
Husk følgende informasjon uansett om du lager et nytt oppgaveopptak eller baserer opptaket på et oppgaveopptak fra Microsoft.

-   Planlegg opptaket slik du hadde gjort med et videoopptak. Ta alle beslutninger på forhånd.
-   Gå gjennom forretningsprosessen én eller to ganger uten å ta den opp, for å forstå fremgangsmåten.
-   Når du går gjennom prosessen før du tar opp, legger du merke til hvor du bruker hurtigtaster eller **Enter**-tasten, slik at du kan unngå å bruke dem i selve opptaket.
-   Finn ut følgende:
    -   Vil du til gruppere trinn i deloppgaver? Deloppgaver skiller delene i en prosess visuelt. Hvis du for eksempel lager et opptak for opprettelse og frigivelse av et produkt, vil du kanskje gruppere trinnene som kreves for å opprette et produkt, og deretter gruppere trinnene som kreves for å frigi produktet. Deloppgaver gjør det også lettere å lese lange prosesser.
    -   Vil du legge til merknader, og i så fall, hvor? Se «Forstå de ulike typene merknader» nedenfor hvis du vil ha mer informasjon.
    -   Hvilke verdier vil du legge til i de ulike feltene mens du fullfører trinnene i forretningsprosessen? Det er en god idé å vite hva du skal velge eller angi når du går fremover, slik at du ikke går tilbake eller retter feil når du gjør opptak.

**Skriv inn beskrivelsen og merknadene på forhånd**

-   I begynnelsen av hvert oppgaveopptak er det et beskrivelsesfelt du kan bruke til å skrive inn en introduksjon til opptaket. Det er lurt å skrive og lagre beskrivelsen på forhånd i et eget dokument, slik at du kan kopiere og lime den inn i oppgaveopptaket når du gjør opptak. Dermed kan du bruke tid på å finpusse teksten før du gjør opptak. Hvis du kopierer og limer inn teksten, går hele opptaket raskere og enklere.
-   Du kan lage merknader for hvert trinn i et oppgaveopptak. Når du spiller av en oppgaveveiledning, vises merknader i «boblen» som notater over eller under teksten for trinnet. Når de vises som tekst i Hjelp-ruten, vises merknadene som innebygd tekst i trinn. Som med beskrivelsen er det lurt å skrive inn og lagre merknadene i et eget dokument. Når du tar opp oppgaven, kopierer og limer du inn merknadene fra dette dokumentet.

**Forstå de ulike typene merknader** Alle merknader er valgfrie. Bare legg dem til når de gir brukeren nyttig informasjon.

-   **Tittelen**: en merknad med en tittel som vises før trinn teksten som denne oppgaven recorder automatisk genererer. I håndboken for aktiviteten vises merknaden tittel over automatisk generert tekst. Bruk denne typen merknad til å forklare hvorfor brukeren gjør trinnet eller til å gi ytterligere kontekst.

Dette er redigeringsruten du ser når du legger til en merknad mens du lager opptaket. Angi en tittelmerknad i **Tittel**-boksen. 

[![skjerm 1](./media/screen1.png)](./media/screen1.png) 

Slik ser tittelmerknaden ut i «boblen» i oppgaveveiledningen. 

[![skjerm2](./media/screen2.png)](./media/screen2.png)

-   **Obs! ** En notatmerknad vises etter trinnteksten som oppgaveopptakeren genererer automatisk. I oppgaveveiledningen vises den bare hvis brukeren klikker **Vis mer**-koblingen i boblen i oppgaveveiledningen. Bruk denne typen merknad til å beskrive det en bruker må vite for å kunne fullføre trinnet.

Dette er redigeringsruten du ser når du legger til en merknad mens du lager opptaket. Angi en tittelmerknad i **Merknader**-boksen. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Dette er merknaden notater ser ut i "boble" i TV-guiden for oppgaven.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info-trinn**: disse merknadene som er opprettet ved å høyreklikke på en kontroll eller hvor som helst på et skjema &lt;**Oppgaveregistrering**&lt; ** Legg til info trinn. ** Info trinnene vises som et nummerert trinn på et hvilket som helst tidspunkt du sette det inn, selv om ingen handling ble spilt inn i Brukergrensesnittet. Du kan legge til et informasjonstrinn på skjemanivå eller et informasjonstrinn som er knyttet til en kontroll. Når et informasjonstrinn er knyttet til et skjema, vises «boblen» i oppgaveveiledningen et sted i skjemaet, uten peker, når oppgaveveiledningen spilles av. Når en info-trinn er knyttet til en kontroll, vil oppgaven guide "boble" peke til kontrollen når TV-guiden for oppgaven som skal spilles. I Hjelp-ruten vises informasjon om trinn merknad som nummererte trinn med teksten du skrev inn. Bruk informasjon om fremgangsmåte for å forberede brukeren for de neste trinnene beskriver fremgangsmåten som må gjøres utenfor Dynamics 365 for operasjoner, eller til å referere til andre innspillinger (selv om du ikke kan opprette hyperinks i merknader.).

**Avgjøre hvor langt opptaket skal være**

-   Brukeren kommer vanligvis til å lese eller spille av opptaket fra begynnelse til slutt, så ikke kombiner trinn eller oppgaver det er bedre å gjøre atskilt.
-   Ikke prøv å ta opp et langt scenario som strekker seg over flere underprosesser. «Betjene brukestøtte for butikkunde» er for eksempel for generelt. Del det opp i kortere oppgaver, for eksempel «Godta returer» og «Legg til i gavekort».
-   Hvis en oppgave kan utføres som en del av flere ulike forretningsprosesser, lager du et separat opptak for den, og så kan du henvise til det i de andre opptakene.
-   Hvis prosessen omfatter flere oppgaver som brukeren sannsynligvis gjør samtidig, kan du ha oppgavene i ett opptak, for eksempel «Konfigurere og tilordne funksjonalitetsprofiler».
-   Hvis det er noe noen gjør én gang (for eksempel konfigurasjon), og deretter en annen oppgave de kan gjøre like etterpå, men kan gjøre gjentatte ganger og separat, kan du dele dem opp i to oppgaveopptak.

**Bestemme hvor i Brukergrensesnittet for å starte en innspilling** siden du er på når du starter innspilling av en registrering på aktiviteten påvirker hvilken side som vises for TV-guiden for oppgaven. Hvis du vil at oppgaven innspillingen for å være oppført i Hjelp-ruten når en bruker klikker Hjelp på siden for finans-parametere, må du starte innspillingen på siden parametere for økonomimodulen. **Lagre opptak som AXTR-filer** Når du er ferdig med å lage eller redigere et oppgaveopptak, har du flere alternativer for hvordan du vil laste ned eller lagre opptaket. Du kan laste ned filen som en oppgaveopptakspakke (AXTR), laste den ned som en rå opptaksfil (XML), laste den ned som et Word-dokument, eller lagre filen i et LCS-bibliotek. Det er alltid lurt å lagre oppgaveopptaket som en oppgaveopptakspakkefil (AXTR). Dette gjør det enklere å vedlikeholde filen hvis fremgangsmåter eller merknader må endres senere. Hvis du vil laste ned filen som et Word-dokument, må du også lagre den som en oppgaveopptakspakkefil.

## <a name="create-your-task-recording"></a>Lage oppgaveopptaket
Fremgangsmåte for detaljert innføring i [hvordan du oppretter en aktivitet registrere](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopiere og tilpasse oppgaveopptak fra Microsoft
Du kan laste ned og redigere Microsofts aktivitet innspillinger for å bruke dem for din egen hjelpedokumentasjon eller opplæringsmateriell. Følg disse trinnene for å laste ned et oppgaveopptak fra Microsoft:

1.  I Dynamics 365 for operasjoner, åpne Oppgaveregistrering. Oppgaveopptakeren finner du på **Innstillinger**-menyen.
2.  Klikk **Vedlikehold av opptak** i ruten for oppgaveopptakeren.
3.  Under **Hvor er opptaket** klikker du **Det er i et LCS-bibliotek**.
4.  Klikk **Velg LCS-biblioteket**.
5.  Velg Microsoft global library.
6.  Velg biblioteknoden for forretningsprosess som er knyttet til oppgaveopptaket, i treet.
7.  Klikk **OK**.
8.  Klikk **Start**.
9.  Nå, gå gjennom innspillingen, endrer noe når du går til å registrere den på nytt. **Merk**: Hvis du bare trenger å endre teksten i en innspilling, kan du åpne innspillingen i **redigere merknader for en innspilling** modus, og deretter lagre den.
10. Når opptaket er avspilt til slutten, klikker du **Stopp** på oppgaveopptakslinjen øverst på skjermen.
11. Velg hvordan du vil lagre oppgaveopptaket.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Inkluder aktivitet innspillinger i Hjelp-ruten
Hvis du vil vise dine egne egendefinerte oppgaven innspillinger i Hjelp-ruten slik at de kan spilles av som oppgaven støttelinjer eller vises som tekst, må du lagre oppgaven innspillinger BPM biblioteket og Oppdater systemparametere din hjelp til å peke på BPM-biblioteket. Hvis du vil ha mer informasjon, se [koble til hjelpesystemet.](../get-started/help-connect.md)

<a name="see-also"></a>Se også
--------

[Hjelp for Dynamics 365 for operasjoner](..\get-started\help-overview.md)

[Koble til hjelp](..\get-started\help-connect.md)

[Oppgaveregistrering i Dynamics 365 for operasjoner](task-recorder.md)

[Nylig lagt til aktivitet Opptaker funksjoner](\core\get-started\recently-added-editing-features-in-task-recorder)

[Opprette nye biblioteker for opplæring for Dynamics AX i levetidstjenester ved hjelp av Oppgaveregistrering (ekstern link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Opprette rik hjelpeemner med Oppgaveregistrering (ekstern link)](https://mbspartner.microsoft.com/AX/Videos/970)


