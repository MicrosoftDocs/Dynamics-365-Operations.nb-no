---
title: "Tilbudsforespørsler (RFQ-er)"
description: "Dette emnet gir en oversikt over tilbudsforespørsler (RFQ-er). Organisasjoner utsteder en tilbudsforespørsel når de ønsker å motta konkurrerende tilbud fra flere leverandører for varer eller tjenester de må kjøpe."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 42ab7beb8a269cd37fd9100385bd302e4945c1e0
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---

# <a name="requests-for-quotation-rfqs"></a>Tilbudsforespørsler (RFQ-er)

[!include[banner](../includes/banner.md)]

Dette emnet gir en oversikt over tilbudsforespørsler (RFQ-er). Organisasjoner utsteder en tilbudsforespørsel når de ønsker å motta konkurrerende tilbud fra flere leverandører for varer eller tjenester de må kjøpe. I en tilbudsforespørsel ber du leverandører om å oppgi prisene og leveringstidene for vareantallene du angir. Du kan også spørre leverandører om de kan angi om det finnes diverse tillegg, for eksempel leveringskostnader, eller om det er mulig med rabatter for store bestillinger eller tidlig betaling av leverandørfakturaen.

RFQ-prosessen består av følgende oppgaver:

1. Opprette og sende en tilbudsforespørsel til én eller flere leverandører.
2. Motta og registrere svar på tilbudsforespørsler (bud).
3. Overføre bud du godtar på en bestilling, kjøpsavtale eller innkjøpsrekvisisjon.

Illustrasjonen nedenfor viser en oversikt over forespørselsprosessen.

[![RFQ-prosess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Du kan opprette en tilbudsforespørsel fra planlagte bestillinger, fra en innkjøpsrekvisisjon eller ved manuell oppføring. Tilbudsforespørselen du oppretter, kalles en RFQ-sak. RFQ-saken er basisdokumentet du bruker til å utstede en tilbudsforespørsel til hver leverandør.

Når du har klargjort RFQ-saken og lagt til leverandører, velger du **Send** i RFQ-saken. Det genereres en RFQ-journal for hver leverandør som du har sendt tilbudsforespørselen til. Du kan konfigurere innstillingene for utskriftsbehandling for sendingshandlingen for å skrive ut en rapport for hver leverandør til et arkiv eller sende en rapport til e-postadressen for hver leverandør. Tilbudsforespørselsjournalen for hver leverandør kan dessuten brukes til å generere en rapport som du kan sende eller sende på nytt til en leverandør senere. Du kan også konfigurere handlingen Send slik at den genererer et svarark som leverandøren kan fylle ut.

Dette emnet dekker prosessen for å håndtere tilbudsforespørsler når leverandørsamarbeid ikke er brukt. Hvis systemet er definert for leverandørsamarbeid, kan leverandører legge inn bud direkte i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Hvis du vil ha mer informasjon, kan du se [Leverandørsamarbeid med kunder](vendor-collaboration-work-customers-dynamics-365-operations.md).
 
Hvis du må endre en tilbudsforespørsel etter at du har sendt den, kan du sende tilbudsforespørselen på nytt til leverandører når du er ferdig, ved hjelp av de to tilleggshandlingene: Opprett og Fullfør.

Når du mottar bud via e-post, må du angi dem på siden **Svar på tilbudsforespørsel**. Hvis du velger alternativet **Kopier data til svar**, kopieres data som antall og datoer fra tilbudsforespørselssaken til svaret. Du kan endre disse dataene slik at de gjenspeiler leverandørens bud.

Hvis en ny gjentakelse av et svar er nødvendig for en leverandør, velger du **Retur** på siden **Svar på tilbudsforespørsel**. Returhandlingen genererer en ny journal og en rapport som blir skrevet ut, arkivert, og sendt i henhold til innstillingene for utskriftsbehandling.

Hvis du har lagt til poengkriterier i tilbudsforespørselssaken, vil forespørselssvaret ha et poengpanel der du kan gi poeng. De totale resultatene vises når du sammenligner svarene på siden **Sammenlign svar**. På denne siden kan du også sammenligne andre svardata, for eksempel linjepris, leveringsdato og totalpris.

Når du har valgt et bud eller delvise bud, kan du godta dem og avvise resten. Journaler for godkjenning, journaler for avslag og tilhørende rapporter genereres og skrives ut, arkiveres og sendes i henhold til innstillingene for utskriftsbehandling. Når du godkjenner et bud eller bestemte linjer i et bud, genereres en kjøpsavtale eller en bestilling, eller en innkjøpsrekvisisjon oppdateres, avhengig av kjøpstypen i tilbudsforespørselen. Du kan opprette en forretningsavtale som du senere kan bruke for alle svarene, uavhengig av om du har godkjent eller avvist dem.

Statusen for en tilbudsforespørsel vises i toppteksten for tilbudsforespørselen og avhenger av statusen til tilbudsforespørselslinjene. Statusen angir i hvilken utstrekning du har behandlet tilbudsforespørselen. Hver tilbudsforespørsel har to statusverdier: lavest og høyest. Den laveste statusen er det minst avanserte stadiet for en linje i tilbudsforespørselen, og den høyeste statusen er det mest avanserte stadiet for en linje i tilbudsforespørselen. Hvis det minst avanserte stadiet i en tilbudsforespørsel for eksempel er for en linje som er opprettet, er **Opprettet** den laveste statusen for tilbudsforespørselen. Hvis det mest avanserte stadiet i tilbudsforespørselen er for en linje som er sendt til leverandører, er **Sendt** den høyeste statusen for tilbudsforespørselen. Statusene oppdateres automatisk når du behandler en tilbudsforespørsel.

Du kan vise de laveste og høyeste statusene for et tilbudsforespørselshode på **Alle tilbudsforespørsler**-siden. Du kan vise de laveste og høyeste statusene for en tilbudsforespørselslinje i kategorien **Linjer** på siden **Tilbudsforespørsler**.

Her er rekkefølgen til statusene for behandling av en tilbudsforespørsel:

1. **Opprettet**
2. **Sendt**
3. **Mottatt**
4. **Godkjent**, **Annullert** eller **Avvist**

Disse statusene beskrives nærmere i senere i dette emnet.

## <a name="setting-up-rfq-functionality"></a>Konfigurere funksjonalitet for tilbudsforespørsel

Før du kan opprette en tilbudsforespørselssak, må du angi informasjon om tilbudsforespørsler på siden **Parametere for innkjøp og leverandører**. Når du oppretter en tilbudsforespørselssak, kan du angi standardverdier som kopieres til forespørselen. Du kan angi følgende standardverdier:

- Innkjøpstypen for nye forespørsler: **bestilling** eller **kjøpsavtale**
- Utløpsdato og -klokkeslett
- Leveringsinformasjon og betalingsbetingelser
- Felt som skal inkluderes i svar på tilbudsforespørsel

Du kan overstyre disse verdiene for en bestemt tilbudsforespørselssak.

Du må også konfigurere endringsprosessen. Som en del av denne konfigurasjonen kan du aktivere feltlås. Når feltlåsing er slått på, må en innkjøpsansvarlig som ønsker å endre en tilbudsforespørsel først klikke på **Opprett** i delen **Endring** av kategorien **Forespørsel**. Etter at tilbudsforespørselen er oppdatert med endringen, må innkjøpsansvarlig deretter fullføre prosessen ved å velge **Ferdigstill**. Fullfør-handlingen genererer en e-postmelding som varsler leverandørene om den endrede tilbudsforespørselen.

Du velger malen som skal brukes for e-postvarsling som sendes til leverandører, på siden **Parametere for innkjøp og leverandører**. Når en mal opprettes, kan den inneholde følgende tokener:

- %RFQ-sak%
- %Årsak til retur av bud%
- %Årsak til endring%
- %Endring klargjort av%
- %Firma%
- %RFQ-saksnavn%
- %ExpiryDateTime%
- %Dato%

Tokenet %Årsak til retur av bud% og %Årsak til endring% erstattes med tekst som innkjøpsansvarlig kan skrive inn når han eller hun fullfører endringen i veiviseren for **endring**. Verdiene for tokenet %Endring klargjort av% og %Firma% hentes automatisk fra tilbudsforespørselen. Tokenet %Dato% erstattes av dagens dato.

En e-postmal er også nødvendig hvis du avbryter en tilbudsforespørsel etter at den er sendt. Denne e-postmalen brukes til å sende annulleringsmeldingen til leverandørens kontaktpersoner. Malen må være valgt på siden **Parametere for innkjøp og leverandører**. Når malen er opprettet, kan den inneholde følgende erstatningstokener:

- %Årsak til annullering%
- %RFQ-sak% 
- %Tilbudsforespørsel annullert av%
- %Firma%
- %RFQ-saksnavn%
- %Dato%

Tokenet % Årsak til annullering% erstattes med tekst som den innkjøpsansvarlige kan skrive inn i veiviseren for **annullering**. Tokenet %Dato% erstattes av dagens dato.

Hvis du vil bruke årsakskoder på et svar på tilbudsforespørsel for å angi hvorfor et bud ble avvist eller godtatt, må du definere årsakskoder på **Leverandørårsaker**-siden.

Du kan konfigurere hvordan utskrevne eller lagrede tilbudsforespørseldokumenter skal se ut, på **Skjemaoppsett**-siden i innkjøp og leverandører.

> [!NOTE]
> For en konfigurasjon for offentlig sektor må du bruke endingsprosessen for å endre en forespørsel som allerede er sendt. Når det sendes en forespørsel, er feltene låst. Hvis du vil gjøre endringer i forespørselen, må du derfor velge **Opprett** for å starte endringsprosessen, som beskrevet tidligere. Låsevirkemåten kontrolleres av alternativet **Lås tilbudsforespørsler når de er sendt** på siden **Parametere for innkjøp og leverandører**. Som standard er denne parameteren satt til **Ja**, og for en konfigurasjon av offentlig sektor kan denne standardinnstillingen ikke endres. Derfor, selv om endringsprosessen kan behandles manuelt i en ikke-offentlig konfigurasjon, må den brukes for offentlig konfigurasjon.

Når du oppretter en tilbudsforespørsel for en bestilling og legger til en lagervare i tilbudsforespørselen, opprettes det en lagertransaksjon med tilgangsstatusen **Tilbud tilgang**. Bare tilbudsforespørselslinjer som har denne statusen, tas hensyn til når du bruker en hovedplan for å beregne forsyninger. Hvis du vil at hovedplanen skal ha med tilbudsforespørselslinjene som forventet mottak, må du konfigurere dette i oppsettet av hovedplanlegging.

En innkjøpssjef eller -agent kan opprette og vedlikeholde forespørselstyper i samsvar med innkjøpskravene i organisasjonen. Hver forespørselstype kan knyttes til en poengsummetode. Poengberegningsmetoder består av et sett med vilkår som kan brukes når du gir poeng til bud. Du må definere forespørselstyper, poengberegningsmetode og poengkriterier på siden **Forespørselstype** og **Poengberegningsmetode**.

## <a name="creating-and-sending-an-rfq"></a>Opprette og sende en tilbudsforespørsel

Du oppretter en tilbudsforespørsel, velger leverandørene du vil skal by på tilbudsforespørselen, og sender deretter tilbudsforespørselen til leverandørene. Du kan bruke utskriftsbehandling til å rute forespørselsrapporten og svararkrapportene til det foretrukne målet.

Du kan opprette en tilbudsforespørsel for innkjøpstypen **Bestilling** eller innkjøpstypen **Kjøpsavtale**.

Hvis tilbudsforespørselen er av typen **Bestilling**, skjer følgende:

- Når du oppretter tilbudsforespørselslinjer, genereres lagertransaksjoner som har tilgangsstatusen **Tilbud tilgang**.
- Når du godkjenner et bud, genereres en bestilling.

Hvis tilbudsforespørselen er av typen **Kjøpsavtale**, skjer følgende:

- Tilbudsforespørselen brukes for en avtale om å kjøpe et spesifikt antall eller en verdi av et produkt over tid. Du må velge datointervallet som gjelder for kjøpsavtalen, og navnet på personen som administrerer kjøpsavtalen.
- Når du godkjenner et bud, genereres en kjøpsavtale.

Hvis forespørselen blir generert fra en innkjøpsrekvisisjon, tilordnes typen **innkjøpsrekvisisjon** automatisk. Du kan ikke opprette en tilbudsforespørsel manuelt for typen **Innkjøpsrekvisisjon**.

Du kan opprette en tilbudsforespørsel fra en innkjøpsrekvisisjon bare hvis statusen for innkjøpsrekvisisjonen er **Til vurdering** og du er tildelt den neste arbeidsflytoppgaven. Linjene i innkjøpsrekvisisjonen oppdateres automatisk når du godtar linjer fra forespørselsvar (bud) som du mottok fra leverandører. Du kan ikke fullføre, avvise, godkjenne eller utføre noen andre handlinger for innkjøpsrekvisisjonen, mens tilbudsforespørselen behandles.

Når du oppretter en tilbudsforespørsel, kan du velge en forespørselstype. Forespørselstypen bestemmer settet med poengkriterier som brukes til å gi poeng på svar på forespørselen.

Du kan legge til et spørreskjema i en tilbudsforespørselssak. Dette spørreskjemaet vises deretter i alle svar når du har sendt forespørselen.

Det finnes tre måter å velge leverandørene som du vil legge til en forespørselssak:

- Legg til leverandørene enkeltvis.
- Søk etter alle leverandører som oppfyller bestemte vilkår.
- Legg automatisk til alle leverandører som er godkjent for innkjøpskategoriene som brukes på forespørselslinjene.

Når tilbudsforespørselssaken er klar, velger du **Send**. Send-handlingen genererer journaler og rapporter som blir skrevet ut, arkivert, og sendt i henhold til innstillingene for utskriftsbehandling.

Hvis du satte **Bruk leverandør til omberegning av priser** og **Bruk leverandørspesifikk vareinformasjon** til **Ja** på siden **Sender tilbudsforespørsel** da du sendte tilbudsforespørselen til leverandører, angis noe leverandørspesifikk informasjon automatisk. Du kan endre denne informasjonen på siden **Svar på tilbudsforespørsel**.

Tabellen nedenfor viser hvordan forespørselsstatusen endres når du oppretter en tilbudsforespørsel og sender den til leverandører.

| Handling                             | Laveste status for tilbudsforespørselshode | Høyeste status for tilbudsforespørselshode                        | Laveste status for tilbudsforespørselslinje | Høyeste status for tilbudsforespørselslinje |
|------------------------------------|--------------------------|--------------------------------------------------|------------------------|-------------------------|
| Opprett tilbudsforespørselshodet og -linjen.    | Opprettet                  | Opprettet                                          | Opprettet                | Opprettet |
| Send tilbudsforespørselen til en bestemt leverandør. | Sendt                     | Sendt                                             | Sendt                   | Sendt |
| Legg til en annen leverandør.                | Opprettet                  | Sendt (Tilbudsforespørselen er bare sendt til én leverandør.) | Opprettet                | Sendt |
| Send tilbudsforespørselen til den andre leverandøren. | Sendt                     | Sendt                                             | Sendt                   | Sendt |

> [!NOTE]
> Du kan legge til flere leverandører i en tilbudsforespørsel når som helst, og de laveste og høyeste statusene oppdateres for å gjenspeile de nye leverandørene. Hvis du for eksempel har mottatt bud fra alle leverandørene og godtatt minst én linje i et bud, er den laveste statusen i tilbudsforespørselshodet **Avvist**, og den høyeste statusen er **Godtatt**. Hvis du legger til en ny leverandør, er **Opprettet** nå den laveste statusen for en linje. Den laveste statusen i tilbudsforespørselshodet oppdateres derfor til **Opprettet**, men den høyeste statusen forblir **Godtatt**.

## <a name="amending-an-rfq"></a>Endre en tilbudsforespørsel

Noen ganger må du endre en tilbudsforespørsel etter at du har sendt den. Du kan for eksempel være nødt til å endre en tilbudsforespørsel hvis leveringsdatoene er endret, eller hvis du vil ha flere produkter eller et annet antall produkter. Du kan konfigurere endringsprosessen slik at den er mer restriktiv eller mindre restriktiv.

Hvis du konfigurerer endringsprosessen slik at den blir mer restriktiv, må du, før du kan endre feltene i en RFQ-sak som allerede er sendt, velge **Opprett** i RFQ-saken for å starte en endring. Når du har fullført endringene, må du velge **Fullfør**. Du blir deretter veiledet gjennom prosessen med å legge til informasjon i e-postmeldingen som sendes for å varsle leverandører om endringen. Den oppdaterte tilbudsforespørselsrapporten som inneholder en merknad om endringen, legges automatisk til i e-postmeldingen.

Hvis du konfigurerer endringsprosessen slik at den er mindre restriktiv, trenger du ikke velge **Opprett** før du kan endre feltene i en tilbudsforespørselssak som allerede er sendt. Du må imidlertid manuelt legge til en endringsmerknad i tilbudsforespørselen og sende saken på nytt. Vær oppmerksom på at denne fremgangsmåten kan bare brukes hvis ingen av svarene (budene) er endret. Hvis du har angitt et svar, og det er i en **Mottatt**-tilstand, er **Send**-knappen utilgjengelig. I så fall må du velge **Opprett** og **Fullfør**, slik du må du i den mer restriktive prosessen. Svaret tilbakestilles deretter for å gjenspeile endringene i tilbudsforespørselssaken. 

Hvis leverandører bruker grensesnittet for leverandørsamarbeid til å legge inn bud, må du alltid bruke endringsprosessen til å varsle leverandører om endringer i tilbudsforespørselssaken. Dette kravet forhindrer en situasjon der leverandører byr på en utdatert tilbudsforespørselssak mens budet er under behandling. Hvis du vil ha mer informasjon om leverandørsamarbeid, kan du se [Leverandørsamarbeid med eksterne leverandører](vendor-collaboration-work-external-vendors.md). 

Hvis du vil invitere flere leverandører til å by, og ingen endringer er gjort i tilbudsforespørselssaken, kan du bruke **Send**-knappen. Leverandørene du har lagt til, vises på **Send**-siden, og de mottar e-postinvitasjonen.

## <a name="receiving-and-registering-rfq-replies"></a>Motta og registrere svar på tilbudsforespørsler (bud)

Når du sender en tilbudsforespørsel, opprettes det automatisk et svarark. Når du mottar svar (bud) på en tilbudsforespørsel, må du angi informasjon fra hver leverandør i et leverandørspesifikt svarark for tilbudsforespørsel. Hvis du har lagt til poengkriteriene, kan du gi poeng til svarene. Du kan deretter sammenligne leverandørbudene og rangere dem i henhold til poengkriteriene, for eksempel beste totalpris eller beste totale leveringstid.

Hvis et spørreskjema er knyttet til tilbudsforespørselssaken, må du manuelt angi svarene på spørsmålene i svararket.

Du kan også angi alternative linjer hvis tilbudsforespørselssaken tillater alternative linjer. På hurtigfanen **Innkjøpstilbudslinjer** velger du **Legg til linje**. Deretter skriver du inn produktinformasjonen, for eksempel varenummeret eller innkjøpskategorien, antall, pris og rabatt.

Hvis du har skrevet inn et svar, men krever et nytt tilbud fra leverandøren, kan du sende tilbudsforespørselen på nytt. En ny journal og rapport genereres, og du kan bruke dem til å be om endringer fra leverandøren.

Du kan se en oversikt over alle tilbudsforespørsler og statusen deres på siden **Oppfølging av tilbudsforespørsel**.

Tabellen nedenfor viser hvordan forespørselsstatusen endres når du mottar bud og registrerer informasjonen i svararket for tilbudsforespørselen.

| Handling                                         | Status for laveste bud | Høyeste budstatus | Laveste status for tilbudsforespørselshode | Høyeste status for tilbudsforespørselshode | Laveste status for tilbudsforespørselslinje | Høyeste status for tilbudsforespørselslinje |
|------------------------------------------------|-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Registrer én leverandørs bud, og lagre det.        | Sendt              | Mottatt           | Sendt                     | Mottatt                  | Sendt                   | Mottatt |
| Registrer den andre leverandørens bud, og lagre det. | Mottatt          | Mottatt           | Mottatt                 | Mottatt                  | Mottatt               | Mottatt |

> [!NOTE]
> Hvis du returnerer et bud til en leverandør for å foreta videre forhandlinger, er laveste og høyeste status fortsatt **Mottatt**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Godta og avvise bud, og overføre godtatte bud til nedstrøms dokumenter

Når du har identifisert det beste budet, for eksempel budet som gir best totalpris, kan du godta det. Du kan godta flere linjer i et bud og avvise andre. Du kan også godta linjer fra forskjellige leverandører. Vær oppmerksom på at hvis du godtar noen linjer, blir du bedt å avvise alle de andre linjene. Hvis du ønsker å godta andre linjer, må du derfor velge **Avbryt** når du blir bedt om det. Statusen for svaret på tilbudsforespørselen for hver leverandør som du godtar bud eller linjer fra, blir oppdatert til **Godkjent**. 

Når du godtar et bud eller bestemte linjer i et bud, opprettes en bestilling eller kjøpsavtale automatisk. Du kan deretter avvise budene fra de andre leverandørene.

I svaret kan du legge til en årsakskode for å forklare hvorfor du godkjente eller avviste et bud.

Når du godkjenner et tilbudsforespørselssvar av typen **Innkjøpsrekvisisjon**, oppdaterer linjene i tilbudsforespørselssvaret linjene i innkjøpsrekvisisjonen med følgende informasjon:

- Enhetspris
- Rabattprosent
- Rabattbeløp
- Innkjøpsgebyrer
- Linjetillegg
- Leverandør
- Eksternt nummer
- Ekstern beskrivelse

Tabellen nedenfor viser hvordan forespørselsstatusen endres etter som du godtar eller avviser bud fra leverandørene.

| Handling                      | Status for laveste bud | Høyeste budstatus | Laveste status for tilbudsforespørselshode | Høyeste status for tilbudsforespørselshode | Laveste status for tilbudsforespørselslinje | Høyeste status for tilbudsforespørselslinje |
|-------------------------    |-------------------|--------------------|--------------------------|---------------------------|------------------------|-------------------------|
| Godta et av budene.     | Mottatt          | Godtatt           | Mottatt                 | Godtatt                  | Mottatt               | Godtatt |
| Avvis alle de andre budene.  | Avslått          | Godtatt           | Avslått                 | Godtatt                  | Avslått               | Godtatt |

