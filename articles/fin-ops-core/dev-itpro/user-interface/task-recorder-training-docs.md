---
title: Lage dokumentasjon eller opplæring med Oppgaveopptaker
description: Dette emnet forklarer hva Oppgaveopptaker og oppgaveveiledninger er, hvordan du oppretter oppgaveopptak og hvordan du tilpasser Microsoft-oppgaveveiledninger og inkluderer dem i hjelpen.
author: josaw1
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b92ef15fc9f3f6a5ebb6ba4ea4eae1a0f7488995
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687798"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Lage dokumentasjon eller opplæring med Oppgaveopptaker

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hva Oppgaveopptaker og oppgaveveiledninger er, hvordan du oppretter oppgaveopptak og hvordan du tilpasser Microsoft-oppgaveveiledninger og inkluderer dem i hjelpen.

> [!IMPORTANT]
> Du kan registrere dine egne oppgaveveiledninger for Dynamics 365 Human Resources, men du kan ikke lagre dem i et BPM-bibliotek (forretningsprosessmodellerer) eller åpne dem fra Hjelp-ruten nå. Du kan lagre dem lokalt eller på en nettverksplassering og deretter åpne og spille dem av ved hjelp av Oppgaveopptaker. 

<a name="learn-about-task-recorder"></a>Finn ut mer om oppgaveopptak
-------------------------

Oppgaveopptak er et verktøy du kan bruke til å registrere handlingene du utfører i brukergrensesnittet for produktet. Når du bruker oppgaveopptakeren, blir alt du gjør i brukergrensesnittet som kjøres mot serveren, for eksempel tilføying av verdier, endring av innstillinger og fjerning av verdier, tatt opp. Samlet kalles trinnene som du registrerer en *oppgaveregistrering*. Oppgaveopptak kan brukes på mange måter:

-   **Oppgaveopptak kan spilles av som oppgaveveiledninger.** Oppgaveopptak er en integrert del av hjelpeopplevelsen. En oppgaveveiledning er en styrt, veiledet, interaktiv opplevelse gjennom trinnene i en forretningsprosess. Brukeren blir veiledet gjennom hvert trinn ved hjelp av en popup-melding (eller «boble») som animeres i brukergrensesnittet og peker på elementet i brukergrensesnittet som brukeren skal bruke. "Boblen" gir også informasjon om hvordan du bruker elementet, for eksempel "Klikk her" eller "Angi en verdi i dette feltet". En oppgaveveiledning kjører mot brukerens gjeldende datasett, og dataene som angis, lagres i brukerens miljø.
-   **Du kan lagre oppgaveopptak som Word-dokumenter.** Dette gjør at du enkelt kan lage opplæringsveiledninger som skrives ut.

Du kan opprette dine egne oppgaveopptak, spille av oppgaveopptak fra Microsoft, eller endre oppgaveopptak fra Microsoft for å gjenspeile konfigurasjonen din. Hvis du vil ha mer informasjon om Oppgaveopptak, kan du se [Oppgaveopptak](task-recorder.md).

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
-   Du kan lage merknader for hvert trinn i et oppgaveopptak. Når du spiller av en oppgaveveiledning, vises merknader i «boblen» som notater over eller under teksten for trinnet. Når merknader vises som tekst i Hjelp-ruten, vises de som innebygd tekst i trinnet. Som med beskrivelsen er det lurt å skrive inn og lagre merknadene i et eget dokument. Når du tar opp oppgaven, kopierer og limer du inn merknadene fra dette dokumentet.

**Forstå de ulike typene merknader** Alle merknader er valgfrie. Bare legg dem til når de gir brukeren nyttig informasjon.

-   **TIttel**: En tittelmerknad vises før trinnteksten som oppgaveopptakeren genererer automatisk. I oppgaveveiledningen vises tittelmerknaden over den automatisk genererte teksten. Bruk denne typen merknad til å forklare hvorfor brukeren gjør trinnet eller til å gi ytterligere kontekst.

Dette er redigeringsruten du ser når du legger til en merknad mens du lager opptaket. Angi en tittelmerknad i **Tittel**-boksen. 

[![Redigeringsrute med tittelmerknad](./media/screen1.png)](./media/screen1.png) 

Slik ser tittelmerknaden ut i «boblen» i oppgaveveiledningen. 

[![Utseende på tittelmerknad i oppgaveveiledning](./media/screen2.png)](./media/screen2.png)

-   **Obs!** En notatmerknad vises etter trinnteksten som oppgaveopptakeren genererer automatisk. I oppgaveveiledningen vises den bare hvis brukeren klikker **Vis mer**-koblingen i boblen i oppgaveveiledningen. Bruk denne typen merknad til å beskrive det en bruker må vite for å kunne fullføre trinnet.

Dette er redigeringsruten du ser når du legger til en merknad mens du lager opptaket. Angi en tittelmerknad i **Merknader**-boksen. 

[![Redigeringsrute med merknad i boksen Merknader](./media/screen3.png)](./media/screen3.png) 

Slik ser notatmerknaden ut i "boblen" i oppgaveveiledningen.

[![Utseende på notatmerknad i oppgaveveiledning](./media/screen4.png)](./media/screen4.png)

-   **Informasjonstrinn**: Du oppretter disse merknadene ved å høyreklikke på en kontroll eller hvor som helst i et skjem &lt; **Oppgaveopptaker** &lt; **Legg til informasjonstrinn.** Informasjonstrinn vises som et nummerert trinn der du setter det inn, selv om ingen handling ble tatt opp i brukergrensesnittet. Du kan legge til et informasjonstrinn på skjemanivå eller et informasjonstrinn som er knyttet til en kontroll. Når et informasjonstrinn er knyttet til et skjema, vises «boblen» i oppgaveveiledningen et sted i skjemaet, uten peker, når oppgaveveiledningen spilles av. Når et informasjonstrinn er knyttet til en kontroll, peker "boblen" i oppgaveveiledningen mot kontrollen når oppgaveveiledningen spilles av. I Hjelp-ruten vises merknaden for et informasjonstrinn som et nummerert trinn med tekst du skrev inn. Bruk informasjonstrinn til å forberede brukeren på de neste trinnene, til å beskrive trinnene som må gjøres utenfor programmet, eller til å henvise til andre opptak (selv om du ikke kan bruke hyperkoblinger i merknader).

**Avgjøre hvor langt opptaket skal være**

-   Brukeren kommer vanligvis til å lese eller spille av opptaket fra begynnelse til slutt, så ikke kombiner trinn eller oppgaver det er bedre å gjøre atskilt.
-   Ikke prøv å ta opp et langt scenario som strekker seg over flere underprosesser. «Betjene brukestøtte for butikkunde» er for eksempel for generelt. Del det opp i kortere oppgaver, for eksempel «Godta returer» og «Legg til i gavekort».
-   Hvis en oppgave kan utføres som en del av flere ulike forretningsprosesser, lager du et separat opptak for den, og så kan du henvise til det i de andre opptakene.
-   Hvis prosessen omfatter flere oppgaver som brukeren sannsynligvis gjør samtidig, kan du ha oppgavene i ett opptak, for eksempel «Konfigurere og tilordne funksjonalitetsprofiler».
-   Hvis det er noe noen gjør én gang (for eksempel konfigurasjon), og deretter en annen oppgave de kan gjøre like etterpå, men kan gjøre gjentatte ganger og separat, kan du dele dem opp i to oppgaveopptak.

**Avgjøre hvor du skal starte et opptak i brukergrensesnittet** Siden du er på når du begynner å ta opp en oppgave, påvirker hvilken side oppgaveveiledningen vises for. Hvis du for eksempel vil at oppgaveopptaket skal vises i Hjelp-ruten når brukeren klikker på Hjelp på siden Parametere for økonomimodul, må du starte opptaket på siden Parametere for økonomimodul. **Lagre opptak som AXTR-filer** Når du er ferdig med å lage eller redigere et oppgaveopptak, har du flere alternativer for hvordan du vil laste ned eller lagre opptaket. Du kan laste ned filen som en oppgaveopptakspakke (AXTR), laste den ned som en rå opptaksfil (XML), laste den ned som et Word-dokument, eller lagre filen i et LCS-bibliotek. Det er alltid lurt å lagre oppgaveopptaket som en oppgaveopptakspakkefil (AXTR). Dette gjør det enklere å vedlikeholde filen hvis fremgangsmåter eller merknader må endres senere. Hvis du vil laste ned filen som et Word-dokument, må du også lagre den som en oppgaveopptakspakkefil.

## <a name="create-your-task-recording"></a>Lage oppgaveopptaket
Hvis du vil se de detaljerte trinnene i fremgangsmåten, kan du se [Ressurser for Oppgaveregistrering](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopiere og tilpasse oppgaveopptak fra Microsoft
Du kan laste ned og redigere oppgaveopptak fra Microsoft for å bruke dem i din egen hjelpedokumentasjon eller opplæringsmateriell. Følg disse trinnene for å laste ned et oppgaveopptak fra Microsoft:

1.  Åpne oppgaveopptak. Oppgaveopptakeren finner du på **Innstillinger**-menyen.
2.  Klikk **Vedlikehold av opptak** i ruten for oppgaveopptakeren.
3.  Under **Hvor er opptaket** klikker du **Det er i et LCS-bibliotek**.
4.  Klikk **Velg LCS-biblioteket**.
5.  Velg det globale Microsoft-biblioteket.
6.  Velg biblioteknoden for forretningsprosess som er knyttet til oppgaveopptaket, i treet.
7.  Klikk **OK**.
8.  Klikk **Start**.
9.  Nå kan du gå gjennom opptaket og endre eventuelle trinn ved å ta dem opp på nytt mens du går gjennom opptaket. **Obs!** Hvis du bare vil endre teksten i et opptak, kan du åpne det i modusen **Redigere en merknad i opptaket**, og deretter lagre det.
10. Når opptaket er avspilt til slutten, klikker du **Stopp** på oppgaveopptakslinjen øverst på skjermen.
11. Velg hvordan du vil lagre oppgaveopptaket.



<a name="additional-resources"></a>Tilleggsressurser
--------

[Hjelpesystem](../../fin-ops/get-started/help-overview.md)

[Koble til hjelpesystemet](../../fin-ops/get-started/help-connect.md)

[Oppgaveregistrering](task-recorder.md)

[Opprette rike hjelpeemner med oppgaveopptakeren (ekstern link)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]