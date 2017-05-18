---
title: "Tilbudsforespørsler"
description: "Denne artikkelen gir en oversikt over tilbudsforespørsler, som organisasjoner utsteder når de må kjøpe varer eller tjenester, og ønsker å motta konkurrerende tilbud fra flere leverandører. I en tilbudsforespørsel ber du leverandører om å oppgi prisene og leveringstidene for vareantallene du angir. Du kan også spørre leverandører om de kan angi om det finnes diverse tillegg, for eksempel leveringskostnader, eller om det er mulig med rabatter for store bestillinger eller tidlig betaling av leverandørfakturaen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 20ad50ab5c2dddf4fe07ebb5bb940954c0408f8d
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="request-for-quotations-rfqs"></a>Tilbudsforespørsler

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over tilbudsforespørsler, som organisasjoner utsteder når de må kjøpe varer eller tjenester, og ønsker å motta konkurrerende tilbud fra flere leverandører. I en tilbudsforespørsel ber du leverandører om å oppgi prisene og leveringstidene for vareantallene du angir. Du kan også spørre leverandører om de kan angi om det finnes diverse tillegg, for eksempel leveringskostnader, eller om det er mulig med rabatter for store bestillinger eller tidlig betaling av leverandørfakturaen.

Prosessen for tilbudsforespørsel omfatter følgende oppgaver:

-   Opprette og sende en tilbudsforespørsel til én eller flere leverandører
-   Motta og registrere svar på tilbudsforespørsler (bud)
-   Overføre godtatte bud på en bestilling, kjøpsavtale eller innkjøpsrekvisisjon

Illustrasjonen nedenfor gir en oversikt over forespørselsprosessen.  

[![Tilbudsforespørselsprosess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)  

Du kan opprette en tilbudsforespørsel fra planlagte bestillinger, fra en innkjøpsrekvisisjon eller fra en manuell oppføring. Tilbudsforespørselen du oppretter, kalles en tilbudsforespørselssak, og dette er det grunnleggende dokumentet du bruker til å utarbeide en tilbudsforespørsel til hver leverandør. Når du har klargjort tilbudsforespørselssaken og lagt til leverandørene, klikker du på **Send** i tilbudsforespørselssaken, og en tilbudsforespørselsjournal opprettes for hver leverandør som du har sendt en tilbudsforespørsel til. Du kan konfigurere innstillingene for utskriftsbehandling for sendingshandlingen for å skrive ut en rapport for hver leverandør til et arkiv eller sende en rapport til e-postadressen for hver leverandør. Tilbudsforespørselsjournalen for hver leverandør kan dessuten brukes til å generere en rapport som du kan sende eller sende på nytt til en leverandør senere. Du kan også konfigurere handlingen Send for å generere et svarark som leverandøren kan fylle ut.  

Hvis du må endre en tilbudsforespørsel etter at du har sendt den, kan du sende den på nytt til leverandøren når du er ferdig.  

Når du mottar bud, må du angi dem på siden **Svar på tilbudsforespørsel**. Hvis du velger alternativet **Kopier data til svar**, kopieres data som antall og datoer fra tilbudsforespørselssaken til svaret. Du kan endre disse dataene slik at de gjenspeiler leverandørens bud.  

Hvis en ny gjentakelse av et svar er nødvendig for en bestemt leverandør, klikker du **Retur**på siden**Svar på tilbudsforespørsel**. Returhandlingen genererer en ny journal og en rapport som blir skrevet ut, arkivert, og sendt i henhold til innstillingene for utskriftsbehandling.  

Hvis du har lagt til poengkriterier i tilbudsforespørselssaken, vil forespørselssvaret ha et poengpanel der du kan gi poeng. Den totale poengsummen vil vises når du sammenligner svarene på **Sammenlign svar**-siden, der du også kan sammenligne andre svardata, for eksempel linjepris, leveringsdato og totalpris.  

Når du bestemmer deg for et bud eller delvise bud, kan du godta dem og avvise resten. Journaler for godkjenning, journaler for avslag og tilhørende rapporter genereres. Disse blir skrevet ut, arkivert og sendt i henhold til innstillingene for utskriftsbehandling. Når du godkjenner et bud eller bestemte linjer i et bud, genereres en kjøpsavtale eller en bestilling, eller en innkjøpsrekvisisjon oppdateres, avhengig av typen tilbudsforespørsel. Du kan opprette en forretningsavtale som du senere kan bruke for alle svarene, uavhengig av om du har godkjent eller avvist dem.  

Statusen for en tilbudsforespørsel vises i toppteksten for tilbudsforespørselen og avhenger av statusen til tilbudsforespørselslinjene. Statusen angir i hvilken utstrekning du har behandlet tilbudsforespørselen. Hver tilbudsforespørselhar to statusverdier: lavest og høyest. Den laveste statusen er det minst avanserte stadiet for en linje i tilbudsforespørselen, og den høyeste statusen er det mest avanserte stadiet for en linje i tilbudsforespørselen. Hvis det minst avanserte stadiet i en tilbudsforespørsel for eksempel er for en linje som er opprettet, er **Opprettet** den laveste statusen for tilbudsforespørselen. Hvis det mest avanserte stadiet i tilbudsforespørselen er for en linje som er sendt til leverandører, er **Sendt** den høyeste statusen for tilbudsforespørselen. Statusene oppdateres automatisk når du behandler en tilbudsforespørsel.  

Du kan vise de laveste og høyeste statusene for et tilbudsforespørselshode på **Alle tilbudsforespørsler**-siden. Du kan vise de laveste og høyeste statusene for en tilbudsforespørselslinje i kategorien **Linjer** på siden **Tilbudsforespørsler**.  

Her er rekkefølgen til statusene for behandling av en tilbudsforespørsel:

1.  **Opprettet**
2.  **Sendt**
3.  **Mottatt**
4.  **Godkjent**/**Annullert**/**Avvist**

Statusene beskrives nærmere i senere i denne artikkelen.

## <a name="setting-up-rfq-functionality"></a>Konfigurere funksjonalitet for tilbudsforespørsel
Før du kan opprette en tilbudsforespørselssak, må du angi informasjon om tilbudsforespørsler på siden **Parametere for innkjøp og leverandører**. Når du oppretter en tilbudsforespørselssak, kan du angi standardverdier som kopieres til forespørselen. Du kan angi følgende standardverdier:

-   Innkjøpstypen for nye forespørsler: **bestilling** eller **kjøpsavtale**
-   Innstillinger for utløpsdato og -klokkeslett
-   Leveringsinformasjon og betalingsbetingelser.
-   Felt som skal inkluderes i svar på tilbudsforespørsel

Du kan overstyre disse verdiene for en bestemt tilbudsforespørselssak. Du må også konfigurere endringsprosessen. Som en del av denne konfigurasjonen kan du aktivere feltlås. Når feltlåsing er aktivert, må en innkjøpsansvarlig som ønsker å endre en tilbudsforespørsel først klikke **Opprett** i delen **Endring** i kategorien **Tilbud**. Når tilbudsforespørselen er oppdatert med endringen, må innkjøpsansvarlig fullføre prosessen ved å klikke på **Fullfør**. Dette genererer en e-postmelding som varsler leverandørene om den endrede forespørselen. Du velger malen for e-postvarsling som sendes til leverandører på siden **Parametere for innkjøp og leverandører**. Når en mal opprettes, kan den inneholde følgende tokener:

-   %Årsak til retur av bud%
-   %Årsak til endring%
-   %Endring klargjort av%
-   %Firma%

Tokenet %Årsak til retur av bud% og %Årsak til endring% erstattes med tekst som innkjøpsansvarlig kan skrive inn når han eller hun fullfører endringen i veiviseren for **endring**. Verdiene for tokenet %Endring klargjort av% og %Firma% hentes automatisk fra tilbudsforespørselen.  

Hvis du vil bruke årsakskoder på et svar på tilbudsforespørsel for å angi hvorfor et bud ble avvist eller godtatt, må du definere årsakskoder på **Leverandørårsaker**-siden.  

Du kan konfigurere hvordan utskrevne eller lagrede tilbudsforespørseldokumenter skal se ut, på **Skjemaoppsett**-siden i innkjøp og leverandører.  

Når du oppretter en tilbudsforespørsel for en bestilling og legger til en lagervare i tilbudsforespørselen, opprettes det en lagertransaksjon med tilgangsstatusen **Tilbud tilgang**. Bare tilbudsforespørselslinjer som har denne statusen, tas hensyn til når du bruker en hovedplan for å beregne forsyninger. Hvis du vil at hovedplanen skal ha med tilbudsforespørselslinjene som forventet mottak, må du konfigurere dette i oppsettet av hovedplanlegging.  

Som innkjøpssjef eller -agent kan du opprette og vedlikeholde forespørselstyper i samsvar med innkjøpskravene i organisasjonen. Hver forespørselstype kan ha poengberegningsmetoder. Poengberegningsmetoder består av et sett med vilkår som kan brukes når du gir poeng til bud. Du må definere forespørselstyper, poengberegningsmetode og poengkriterier på siden **Forespørselstype** og **Poengberegningsmetode**.

## <a name="creating-and-sending-an-rfq"></a>Opprette og sende en tilbudsforespørsel
Du oppretter en tilbudsforespørsel, velger leverandørene du vil skal by på tilbudsforespørselen, og sender deretter tilbudsforespørselen til leverandørene. Du kan bruke utskriftsbehandling til å rute forespørselsrapporten og svararkrapportene til det foretrukne målet.  

Du kan opprette en forespørsel for innkjøpstypen **Bestilling** eller **Kjøpsavtale**.  

Hvis forespørselen blir generert fra en innkjøpsrekvisisjon, tilordnes typen **innkjøpsrekvisisjon** automatisk. Du kan ikke opprette en tilbudsforespørsel manuelt for typen **Innkjøpsrekvisisjon**. Hvis tilbudsforespørselen er av typen **Bestilling**:

-   Når du oppretter tilbudsforespørselslinjer, genereres lagertransaksjoner som har tilgangsstatusen **Tilbud tilgang**.
-   Når du godkjenner et bud, genereres en bestilling.

Hvis tilbudsforespørselen er av typen **Kjøpsavtale**:

-   Tilbudsforespørselen brukes for en avtale om å kjøpe et spesifikt antall eller en verdi av et produkt over tid. Du må velge datointervallet som gjelder for kjøpsavtalen, og navnet på personen som administrerer kjøpsavtalen.
-   Når du godkjenner et bud, genereres en kjøpsavtale.

Du kan opprette en tilbudsforespørsel fra en innkjøpsrekvisisjon bare hvis statusen for innkjøpsrekvisisjonen er **Til vurdering**og du er tildelt den neste arbeidsflytoppgaven. Linjene i innkjøpsrekvisisjonen oppdateres automatisk når du godtar linjer fra forespørselsvar (bud) som du mottok fra leverandører. Du kan ikke fullføre, avvise, godkjenne eller utføre noen andre handlinger for innkjøpsrekvisisjonen, mens tilbudsforespørselen behandles.  

Når du oppretter en tilbudsforespørsel, kan du velge en bestemt forespørselstype. Forespørselstypen bestemmer settet med poengkriterier som brukes til å gi poeng på svar på forespørselen.  

Du kan legge til et spørreskjema i en tilbudsforespørselssak. Dette spørreskjemaet vises deretter i alle svar når du har sendt forespørselen.  

Det finnes tre måter å velge leverandørene som du vil legge til en forespørselssak:

-   Legg til leverandørene enkeltvis.
-   Søk etter alle leverandører som oppfyller bestemte vilkår.
-   Legg automatisk til alle leverandører som er godkjent for innkjøpskategoriene som brukes på forespørselslinjene.

Når tilbudsforespørselssaken er klar, klikker du **Send**. Send-handlingen genererer journaler og rapporter som blir skrevet ut, arkivert, og sendt i henhold til innstillingene for utskriftsbehandling.  

Hvis du merket av for **Bruk leverandør til omberegning av priser** og **Bruk leverandørspesifikk vareinformasjon** på siden **Sender tilbudsforespørsel** da du sendte forespørselen til leverandører, angis noe leverandørspesifikk informasjon automatisk. Du kan endre denne informasjonen på siden **Svar på tilbudsforespørsel**.  

Tabellen nedenfor viser hvordan forespørselsstatusen endres når du oppretter en tilbudsforespørsel og sender den til leverandører.

|                                    |                              |                                                 |                            |                             |
|------------------------------------|------------------------------|-------------------------------------------------|----------------------------|-----------------------------|
| **Handling**                         | **Laveste status for tilbudsforespørselshode** | **Høyeste status for tilbudsforespørselshode**                   | **Laveste status for tilbudsforespørselslinje** | **Høyeste status for tilbudsforespørselslinje** |
| Opprett tilbudsforespørselshodet og -linjen.    | Opprettet                      | Opprettet                                         | Opprettet                    | Opprettet                     |
| Send tilbudsforespørselen til en bestemt leverandør. | Sendt                         | Sendt                                            | Sendt                       | Sendt                        |
| Legg til en annen leverandør.                | Opprettet                      | Sendt (Tilbudsforespørselen er bare sendt til én leverandør.) | Opprettet                    | Sendt                        |
| Send tilbudsforespørselen til den andre leverandøren. | Sendt                         | Sendt                                            | Sendt                       | Sendt                        |

**Obs!** Du kan legge til flere leverandører i en tilbudsforespørsel når som helst, og de laveste og høyeste statusene endres for å gjenspeile de nye leverandørene. Hvis du for eksempel har mottatt bud fra alle leverandørene og godtatt minst én linje i et bud, er den laveste statusen i tilbudsforespørselshodet **Avvist**, og den høyeste statusen er **Godtatt**. Hvis du legger til en ny leverandør, er **Opprettet** nå den laveste statusen for en linje. Den laveste statusen i tilbudsforespørselshodet endres derfor til **Opprettet**, og den høyeste statusen forblir **Godtatt**.

## <a name="amending-an-rfq"></a>Endre en tilbudsforespørsel
Noen ganger må du endre en tilbudsforespørsel etter at du har sendt den. Dette kan skje fordi, for eksempel leveringsdatoene er endret, eller du vil ha flere produkter eller ulikt antall produkter. Du kan konfigurere endringsprosessen slik at den er mer restriktiv eller mindre restriktiv.  

Hvis du bruker den mer restriktive endringsprosessen, må du klikke **Opprett** i tilbudsforespørselssaken for å starte en endring før du kan endre feltene i tilbudsforespørselssaken. Når du har gjort endringene, klikker du **Fullfør**. Du blir deretter veiledet gjennom prosessen med å legge til informasjon i e-postmeldingen som sendes for å varsle leverandører om endringen. Den oppdaterte tilbudsforespørselsrapporten som inneholder en merknad om endringen, legges automatisk til meldingen.  

Hvis du bruker den mindre restriktive endringsprosessen, trenger du ikke opprette en endring før du kan endre feltene i tilbudsforespørselssaken som allerede er sendt. Du må imidlertid manuelt legge til en endringsmerknad i tilbudsforespørselen.

## <a name="receiving-and-registering-rfq-replies"></a>Motta og registrere svar på tilbudsforespørsler (bud)
Når du sender en tilbudsforespørsel, opprettes det automatisk et svarark. Når du mottar svar (bud) på en tilbudsforespørsel, må du angi informasjon fra hver leverandør i et leverandørspesifikt svarark for tilbudsforespørsel. Hvis du har lagt til poengkriteriene, kan du gi poeng til svarene. Du kan deretter sammenligne leverandørbudene og rangere dem i henhold til poengkriteriene, for eksempel beste totalpris eller beste totale leveringstid.  

Hvis et spørreskjema er knyttet til tilbudsforespørselssaken, må du manuelt angi svarene på spørsmålene i svararket.  

Hvis du må angi alternative linjer, og forespørselssaken tillater dette, klikker du **Legg til linje** i hurtigkategorien **Innkjøpstilbudslinjer**. Deretter skriver du inn produktinformasjonen, for eksempel varenummeret eller innkjøpskategorien, antall, pris og rabatt.  

Hvis du har skrevet inn et svar, men krever et nytt tilbud fra leverandøren, kan du sende tilbudsforespørselen på nytt. Dette genererer en ny journal og rapport som du kan bruke til å be om endringer fra leverandøren.  

Du kan se en oversikt over alle tilbudsforespørsler og statusen deres på siden **Oppfølging av tilbudsforespørsel**.  

Tabellen nedenfor viser hvordan forespørselsstatusen endres når du mottar bud og registrerer informasjonen i svararket for tilbudsforespørselen.

|                                                |                       |                        |                              |                               |                            |                             |
|------------------------------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Handling**                                     | **Status for laveste bud** | **Høyeste budstatus** | **Laveste status for tilbudsforespørselshode** | **Høyeste status for tilbudsforespørselshode** | **Laveste status for tilbudsforespørselslinje** | **Høyeste status for tilbudsforespørselslinje** |
| Registrer én leverandørs bud, og lagre det.        | Sendt                  | Mottatt               | Sendt                         | Mottatt                      | Sendt                       | Mottatt                    |
| Registrer den andre leverandørens bud, og lagre det. | Mottatt              | Mottatt               | Mottatt                     | Mottatt                      | Mottatt                   | Mottatt                    |

**Obs!** Hvis du returnerer et bud til en leverandør for å foreta videre forhandlinger, er laveste og høyeste status fortsatt **Mottatt**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Godta og avvise bud, og overføre godtatte bud til nedstrøms dokumenter

Når du har identifisert det beste budet, for eksempel budet som gir best totalpris, kan du godta det. Statusen til svaret på tilbudsforespørselen for denne leverandøren oppdateres til **Godtatt** . Når du godtar et bud eller bestemte linjer i et bud, opprettes en bestilling eller kjøpsavtale automatisk, og du kan avvise budene fra de andre leverandørene.  

Når du godkjenner et tilbudsforespørselssvar av typen **Innkjøpsrekvisisjon**, oppdaterer linjene i tilbudsforespørselssvaret linjene i innkjøpsrekvisisjonen med følgende informasjon:

-   Enhetspris
-   Rabattprosent
-   Rabattbeløp
-   Innkjøpsgebyrer
-   Linjetillegg
-   Leverandør
-   Eksternt nummer
-   Ekstern beskrivelse

I svaret kan du legge til en årsakskode for å forklare hvorfor du godkjente eller avviste et bud.  

Du kan godta flere linjer i et bud og avvise andre. Du kan også godta linjer fra forskjellige leverandører. Bare vær oppmerksom på at hvis du godtar noen linjer, blir du bedt å avvise alle de andre linjene. Hvis du ønsker å godta andre linjer, må du derfor klikke **Avbryt** når du mottar meldingen.  

Tabellen nedenfor viser hvordan forespørselsstatusen endres etter som du godtar eller avviser bud fra leverandørene.

|                         |                       |                        |                              |                               |                            |                             |
|-------------------------|-----------------------|------------------------|------------------------------|-------------------------------|----------------------------|-----------------------------|
| **Handling**              | **Status for laveste bud** | **Høyeste budstatus** | **Laveste status for tilbudsforespørselshode** | **Høyeste status for tilbudsforespørselshode** | **Laveste status for tilbudsforespørselslinje** | **Høyeste status for tilbudsforespørselslinje** |
| Godta et av budene. | Mottatt              | Godtatt               | Mottatt                     | Godtatt                      | Mottatt                   | Godtatt                    |
| Avvis de andre budene.  | Avslått              | Godtatt               | Avslått                     | Godtatt                      | Avslått                   | Godtatt                    |






