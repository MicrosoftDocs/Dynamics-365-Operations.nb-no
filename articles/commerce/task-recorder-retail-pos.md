---
title: Oppgaveopptaker og hjelp for Retail Modern POS (MPOS) og Cloud POS
description: Denne artikkelen beskriver hvordan du bruker Oppgaveopptaker i Retail Modern POS og Cloud POS.
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f9f3e17a6c67dc1cc1d4ba423ce258f2ed1d1ec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847606"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Oppgaveopptaker og hjelp for Retail Modern POS (MPOS) og Cloud POS

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker Oppgaveopptaker i Retail Modern POS og Cloud POS.

## <a name="overview"></a>Oversikt

Oppgaveopptaker i Retail Modern POS og Cloud POS er en ny løsning som ble bygd med fokus på høy hastighet. Den gir et fleksibelt Application Program Interface (API) for fleksibilitet og sømløs integrasjon med forbrukere av forretningsprosessregistreringer. I tillegg er Oppgaveopptaker-integrasjon med verktøyet Forretningsprosessmodelerer (BPM) på Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) implementert. Derfor kan brukere fortsette å produsere rike forretningsprosessdiagrammer fra opptak for å analysere og utforme programmene.

## <a name="architecture"></a>Arkitektur

Oppgaveopptaker kan registrere brukerhandlinger i klienten med nøyaktig gjengivelse. Hver kontroll er utstyrt for å varsle Oppgaveopptaker om utførelsen av en handling. Kontrollen varsler Oppgaveopptaker om at en hendelse oppstod og sender all relevant informasjon om den aktuelle brukerhandlingen i sanntid. Ved hjelp av denne informasjonen kan Oppgaveregistrering registrere typen brukerhandling (for eksempel en knapp klikkes, verdiregistrering eller navigasjon) og eventuelle data som er knyttet til handlingen (for eksempel inndataverdien og typen, skjemakontekst eller postkontekst). Oppgaveopptaker behandler informasjonen detaljert nok til å sikre at en avspilling av opptaket kan utføre de registrerte handlingene nøyaktig slik brukeren har utført dem. (Avspillingsfunksjonen er ennå ikke implementert i Moderne salgssted for detaljhandel eller Skybasert salgssted.)

## <a name="basic-configuration"></a>Grunnleggende konfigurasjon

Følg disse trinnene for å aktivere oppgaveopptak på salgssted.

1. Klikk **Retail og Commerce** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**.
2. Klikk kassen for å aktivere oppgaveopptak.
3. I kategorien **Register** i hurtigfanen **Generelt** angir du alternativet **Aktiver oppgaveregistrering** til **Ja**.
4. Klikk **Lagre**.
5. Gå til **Retail og Commerce** &gt; **IT for Retail og Commerce** &gt; **Distribusjonsplan**.
6. Velg jobben **Kasser (1090)**, og klikk deretter **Kjør nå**.

## <a name="create-a-recording"></a>Opprett et opptak

Følg denne fremgangsmåten for å opprette en ny registrering ved hjelp av oppgaveopptaker.

1. Start Retail Modern POS eller Cloud POS, og logg på.
2. På **Innstillinger**-siden, i delen **Oppgaveopptaker**, klikker du **Åpne Oppgaveregistrering**. Ruten **Oppgaveopptaker** vises. Du kan klikke **Lukk**-knappen (**X**) i øvre høyre hjørne for å lukke ruten **Oppgaveopptaker** før du begynner et nytt opptak. For å åpne ruten igjen gjentar du trinn 2.

    [![Rute for oppgaveopptaker.](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. Skriv inn et navn på og en beskrivelse av opptaket, og klikk deretter **Start**. Opptaksøkten begynner når du klikker **Start**.

    > [!NOTE]
    > Hvis du klikker **Lukk**-knappen (**X**) i øvre høyre hjørne når et opptak pågår, lukkes ruten **Oppgaveopptak**, men opptaksøkten avsluttes ikke. For å åpne ruten for oppgaveopptaker på nytt kan du klikke **Hjelp**-knappen (spørsmålstegn) øverst på skjermen.
    >
    > [![Spørsmålstegn.](./media/help.jpg)](./media/help.jpg)

4. Når du har klikket **Start**, går oppgaveopptak inn i opptaksmodus. Ruten for **oppgaveopptak** viser informasjon og kontroller som er knyttet til opptaksprosessen.
5. Utfør handlingene du vil utføre i grensesnittet for Retail Modern POS eller Cloud POS.
6. Klikk **Stopp** for å avslutte opptaksøkten.

## <a name="download-options"></a>Nedlastingsalternativer

Når du har avsluttet opptaksøkten, vises flere alternativer, slik at du kan laste ned opptaket.

[![Nedlastingsalternativer.](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Lagre på denne PC-en

Du kan bruke opptakspakken til å spille av en oppgaveveiledning, vedlikeholde opptaket eller redigere merknader i opptaket. (Denne funksjonen er ennå ikke implementert i Retail Modern POS og Cloud POS.)

### <a name="export-as-word-document"></a>Eksporter som Word-dokument

Du kan lagre opptaket som et Microsoft Word-dokument. Dokumentet inneholder trinnene du har tatt opp samt skjermbilder som er tatt.

### <a name="save-as-developer-recording"></a>Lagre som utvikleropptak

Rå opptaksfilen er nyttig for utviklerscenarioer, for eksempel generering av testkode. (Denne funksjonen er ikke implementert ennå.)

## <a name="recording-controls"></a>Opptakskontroller

[![Opptakskontroller.](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Stopp

Klikk **Stopp** for å avslutte opptaksøkten. Vær oppmerksom på at du ikke kan starte en økt på nytt når du har avsluttet den. Derfor må du sørge for at opptaket er fullført før det avsluttes.

### <a name="pause"></a>Stans midlertidig

Klikk **Stans midlertidig** for å stanse opptaksøkten midlertidig og fortsette med operasjonen. Trinnene du utfører når du har klikket **Stans midlertidig**, tas ikke opp.

### <a name="continue"></a>Fortsett

For å gjenoppta opptaksøkten når du har stanset midlertid, klikker du **Fortsett**.

### <a name="capture-screenshots"></a>Ta skjermbilder

Oppgaveopptaker kan ta skjermbilder av brukergrensesnittet for Retail Modern POS mens du tar opp en forretningsprosess. Hvis du vil aktivere opptaksfunksjonen for skjermbilde, kan du angi **Ta skjermbilder** til **Ja** og deretter kjøre opptaket. Når opptaket er fullført, klikker du på **Stopp** og laster ned Word-dokumentet. Dokumentet inneholder trinnene med relevante skjermbilder.

> [!NOTE]
> Funksjonen for å ta skjermbilder støttes ikke i skysalgssted.

### <a name="start-task-and-end-task"></a>Start oppgave og avslutt oppgave

Du kan angi begynnelsen og slutten av et sett med grupperte trinn ved hjelp av knappene **Start oppgave** og **Avslutt** **oppgave**. Klikk **Start oppgave** for å legge til et "Start oppgave"-trinn, og utfør deretter trinnene som skal tas med i gruppen. Når du er ferdig med å utføre trinnene for gruppen, klikker du **Avslutt oppgave**. Oppgavene hjelper deg med å organisere dine prosedyrer. Oppgaver kan nestes i andre oppgaver. På denne måten kan du organisere svært lange og kompliserte forretningsprosesser bedre.

## <a name="adding-annotations"></a>Å legge til merknader

En merknad er tilleggstekst du legger til et trinn i en registrering. Du kan for eksempel bruke merknader til å gi brukeren mer kontekst eller instruksjoner. Du kan legge til merknader før eller etter et trinn. Du kan legge til en merknad til et hvilket som helst trinn ved å klikke knappen **Rediger** (blyantsymbol) til høyre for trinnet.

[![Rediger-knappen for et trinn.](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Tekster og merknader

Du kan bruke feltene **Tekster** og **Merknader** til å legge til tekst som skal knyttes til et trinn i en oppgaveveiledning.

[![Tekst og merknader-felt.](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Tekst

Teksten du skriver inn i **Tekst**-feltet, vises *over* trinnteksten i oppgaveveiledningen. Denne plasseringen er egnet for tekst som du vil at brukeren leser før brukeren fullfører trinnet.

#### <a name="notes"></a>Notater

Teksten du skriver inn i **Merknader**-feltet, vises *under* trinnteksten i oppgaveveiledningen. Hvis brukeren skal lese merknadsteksten, må han/hun utvide trinnteksten i popup-vinduet. Denne plasseringen er egnet for valgfritt lesemateriale eller annen informasjon som kan være nyttig for brukeren, men som brukeren ikke trenger for å fullføre handlingen.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Hjelp i Retail Modern POS og Cloud POS

Hvis du vil vise dine egne oppgaveopptak i Hjelp-ruten i Retail Modern POS og Cloud POS, slik at de kan vises som tekst, må du lagre oppgaveopptakene i ditt eget Forretningsprosessmodeler-bibliotek og deretter oppdatere hjelpesystemparameterne slik at de peker mot Forretningsprosessmodeler-biblioteket ditt. Hvis du vil ha mer informasjon, kan du se [Connecting the help system](../fin-ops-core/fin-ops/get-started/help-connect.md). Hjelp for Retail Modern POS og Cloud POS søker i LCS i sanntid. Den søker gjennom alle BPM-biblioteker som er valgt i hjelpesystemparametere for Commerce, og viser de relevante resultatene. Du kan åpne **Hjelp**-menyen ved å klikke **Hjelp**-knappen (spørsmålstegn) øverst på skjermen og deretter skrive inn prosessnavnet ditt i søkeboksen og klikke på søkeknappen.

[![Hjelp-knappen.](./media/help.jpg)](./media/help.jpg)

Når du klikker en oppgaveveiledning i søkeresultatene, kan du se trinnene som en hjelpeartikkel eller eksportere trinnene til et Word-dokument.

> [!NOTE]
> Hjelp i Retail Modern POS og Cloud POS henter ikke frem oppgaveveiledninger i henhold til hvilket skjema du bruker eller hva du holder på med. Du må skrive inn prosessnavnet i søkeboksen, og deretter klikke **Søk**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]