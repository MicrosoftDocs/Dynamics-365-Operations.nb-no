---
title: Oversikt over tilbudsforespørsler (RFQ-er)
description: Dette emnet gir en oversikt over tilbudsforespørsler (RFQ-er). Organisasjoner utsteder en tilbudsforespørsel når de ønsker å motta konkurrerende tilbud fra flere leverandører for varer eller tjenester de må kjøpe.
author: kamaybac
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTable, PurchRFQCaseTableListPage, PurchRFQCompare, PurchRFQReplyTable, PurchRFQVendReplyTableListPage, BOMExpandPurchRFQ, PurchRFQReplyFollowupItem, PurchRFQCaseVend, PurchRFQReplyFollowup, PurchRFQCaseAmendmentInfo, PurchRFQReplyFollowupCase, PurchRFQReplyStatus, PurchRFQCaseReplyFields, PurchRFQAddQuestionnaire, PurchRFQAmendmentWizard, PurchRFQReplyTableStatus, PurchRFQReplyTableListPage, PurchRFQCancelWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2154
ms.assetid: 3936996e-d943-46ca-8385-84c042990f1d
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48830c975f1bdfd953f57e7c0b6601a78e3a521b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910045"
---
# <a name="requests-for-quotation-rfqs-overview"></a>Oversikt over tilbudsforespørsler (RFQ-er)

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over tilbudsforespørsler (RFQ-er). Organisasjoner utsteder en tilbudsforespørsel når de ønsker å motta konkurrerende tilbud fra flere leverandører for varer eller tjenester de må kjøpe. I en tilbudsforespørsel ber du leverandører om å oppgi prisene og leveringstidene for vareantallene du angir.
Du kan også spørre leverandører om de kan angi om det finnes diverse tillegg, for eksempel leveringskostnader, eller om det er mulig med rabatter for store bestillinger eller tidlig betaling av leverandørfakturaen.

RFQ-prosessen består av følgende oppgaver:

1. Opprette og sende en tilbudsforespørsel til én eller flere leverandører.
1. Motta og registrere bud (svar på tilbudsforespørsler).
1. Overføre bud du godtar på en bestilling, kjøpsavtale eller innkjøpsrekvisisjon.

Illustrasjonen nedenfor viser en oversikt over forespørselsprosessen.

[![RFQ-prosess](./media/rfq-process-458x1024.jpg)](./media/rfq-process.jpg)

Du kan opprette en tilbudsforespørselssak fra planlagte bestillinger, fra en innkjøpsrekvisisjon eller ved manuell oppføring. Tilbudsforespørselssaken er basisdokumentet du bruker til å utstede en tilbudsforespørsel til hver leverandør.

Når du har klargjort tilbudsforespørselssaken og lagt til leverandører, velger du **Send** (**Send og publiser** for offentlig sektor) for tilbudsforespørselssaken. Det genereres en RFQ-journal for hver leverandør som du har sendt tilbudsforespørselen til. Du kan konfigurere utskriftsinnstillingene for sendingshandlingen for å skrive ut en rapport for hver leverandør til et arkiv eller sende en rapport til e-postadressen for hver leverandør. Tilbudsforespørselsjournalen for hver leverandør kan dessuten brukes til å generere en rapport som du kan sende eller sende på nytt til en leverandør senere. Du kan også konfigurere handlingen Send slik at den genererer et svarark som leverandøren kan fylle ut.

Dette emnet dekker prosessen for å håndtere tilbudsforespørsler når leverandørsamarbeid ikke er brukt. Hvis systemet er definert for leverandørsamarbeid, kan leverandører legge inn bud direkte i Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Leverandørsamarbeid med kunder](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations) og [Leverandørsamarbeid med eksterne leverandører](vendor-collaboration-work-external-vendors.md).

Hvis du må endre en tilbudsforespørsel etter at du har sendt den, kan du sende tilbudsforespørselen på nytt til leverandører når du er ferdig, ved hjelp av de to tilleggshandlingene: Opprett og Fullfør.

Når du mottar bud via e-post, kan du angi dem på siden **Tilbudsforespørsler**.

Hvis en ny gjentakelse av et svar fra en leverndør er nødvendig, velger du **Retur** på siden **Tilbudsforespørsel**. Returhandlingen genererer en ny journal og en rapport som blir skrevet ut, arkivert, og sendt i henhold til utskriftsinnstillingene.

Hvis du har lagt til poengkriterier i tilbudsforespørselssaken, vil tilbudsforespørselsen ha et poengpanel der du kan gi poeng. De totale resultatene vises i tilbudsforespørselen når du sammenligner svarene på siden **Sammenlign svar**. På siden **Sammenlign svar** kan du også sammenligne andre svardata, for eksempel linjepris, leveringsdato og totalpris.

Når du har valgt et bud eller et antall linjer i et bud, kan du godta alle eller noen linjer og avvise resten. Journaler for godkjenning, journaler for avslag og tilhørende rapporter genereres og skrives ut, arkiveres og sendes i henhold til utskriftsinnstillingene. Når du godkjenner et bud eller bestemte linjer i et bud, genereres en kjøpsavtale eller en bestilling, eller en innkjøpsrekvisisjon oppdateres, avhengig av kjøpstypen i tilbudsforespørselen. Du kan opprette en forretningsavtale som du senere kan bruke for alle svarene, uavhengig av om du har godkjent eller avvist dem.

En tilbudsforespørselssak har to statuser: lavest og høyest. Du kan vise statusen på listesiden for **Alle tilbudsforespørsler**. Den laveste statusen er det minst avanserte stadiet for en linje i tilbudsforespørselssaken, og den høyeste statusen er det mest avanserte stadiet for en linje i tilbudsforespørselssaken. For eksempel si at en tilbudsforespørselssak med tre linjer er sendt til to leverandører, slik at det finnes to tilbudsforespørsler hver med tre linjer. Alle linjer er **sendt**. Nå angis et bud fra en av leverandørene, og tilbudsforespørselslinjene får statusen **Mottatt**. Dette innebærer at ut av de tre linjene i tilbudsforespørselssaken, er alle **Sendt** for én tilbudsforespørsel og **Mottatt** for en annen tilbudsforespørsel. Den laveste statusen vil være **sendt,** og den høyeste statusen er **mottatt.**

Disse statusene beskrives nærmere i senere i dette emnet.

## <a name="setting-up-rfq-functionality"></a>Konfigurere funksjonalitet for tilbudsforespørsel

Før du kan opprette en tilbudsforespørselssak, må du angi informasjon om tilbudsforespørsler på siden **Parametere for innkjøp og leverandører**. Når du oppretter en tilbudsforespørselssak, kan du angi standardverdier som kopieres til forespørselen. Du kan angi følgende standardverdier:

- Innkjøpstypen for nye forespørsler: **bestilling** eller **kjøpsavtale**
- Utløpsdatoen og tidsforskyvningen fra dagen tilbudsforespørselssaken er opprettet.
- Forespørselstype, som kan bruke en bestemt poengberegningsmetode på tilbudsforespørselssaken.
- Leveringsinformasjon og betalingsbetingelser.

Du kan overstyre disse verdiene for en bestemt tilbudsforespørselssak.

Du må også konfigurere endringsprosessen. Som en del av denne konfigurasjonen kan du aktivere feltlås. Når feltlåsing er aktivert, må en innkjøpsansvarlig som ønsker å endre en tilbudsforespørsel først velge **Opprett** i delen **Endring** i fanen **Tilbud** for tilbudsforespørselssaken. Etter at tilbudsforespørselssaken er oppdatert med endringen, må innkjøpsansvarlig fullføre prosessen ved å velge **Fullfør**. Fullfør-handlingen genererer en e-postmelding som varsler leverandørene om den endrede tilbudsforespørselen.

Du velger malen som skal brukes for e-postvarsling som sendes til leverandører, på siden **Parametere for innkjøp og leverandører**. Når en mal opprettes i **E-postmaler**, kan den inneholde følgende tokener:

- %RFQ-sak%
- %Årsak til retur av bud%
- %Årsak til endring%
- %Endring klargjort av%
- %Company%
- %RFQ-saksnavn%
- %Dato og klokkeslett for utløpsdato%
- %Date%

Tokenet %Årsak til retur av bud% og %Årsak til endring% erstattes med tekst som innkjøpsansvarlig kan skrive inn når han eller hun fullfører endringen i veiviseren for **endring**. Verdiene for tokenene %Endring klargjort av% og %Company% hentes automatisk fra tilbudsforespørselen. Tokenet %Date% erstattes av dagens dato.

Hvis du vil avbryte en tilbudsforespørsel etter at den er sendt, kan du gjøre det fra tilbudsforespørselssaken. En e-postmal kreves for å sende annulleringsmeldingen til leverandørens kontaktpersoner. Malen må være valgt på siden **Parametere for innkjøp og leverandører**. Når malen er opprettet, kan den inneholde følgende erstatningstokener:

- %Årsak til annullering%
- %RFQ-sak%
- %Tilbudsforespørsel annullert av%
- %Company%
- %RFQ-saksnavn%
- %Date%

Tokenet % Årsak til annullering% erstattes med tekst som den innkjøpsansvarlige kan skrive inn i veiviseren for **annullering**. Tokenet %Date% erstattes av dagens dato.

Hvis du vil bruke årsakskoder på et bud for å angi hvorfor det ble avvist eller godtatt, må du definere årsakskoder på **Leverandørårsaker**-siden.

Du kan konfigurere hvordan utskrevne eller lagrede tilbudsforespørseldokumenter skal se ut, på **Skjemaoppsett**-siden i innkjøp og leverandører.

> [!NOTE]
> For en konfigurasjon for offentlig sektor må du bruke endingsprosessen for å endre en forespørsel som allerede er sendt. Når det sendes en forespørsel, er feltene låst.
Hvis du vil gjøre endringer i forespørselen, må du derfor velge **Opprett** for å starte endringsprosessen, som beskrevet tidligere. Låsevirkemåten kontrolleres av alternativet **Lås tilbudsforespørsler når de er sendt** på siden **Parametere for innkjøp og leverandører**. Som standard er denne parameteren satt til **Ja**, og for en konfigurasjon av offentlig sektor kan denne standardinnstillingen ikke endres. Derfor, selv om endringsprosessen kan behandles manuelt i en ikke-offentlig konfigurasjon, må den brukes for offentlig konfigurasjon.

Når du oppretter en tilbudsforespørselssak av typen Bestilling og legger til en lagervare i tilbudsforespørselen, opprettes det en lagertransaksjon med tilgangsstatusen **Tilbud tilgang**. Bare linjer i saker om tilbudsforespørsel som har denne statusen, tas hensyn til når du bruker en hovedplan for å beregne forsyninger. Hvis du vil at hovedplanen skal ha med linjer i saker om tilbudsforespørsel som forventet mottak, må du konfigurere dette i oppsettet av hovedplanlegging.

En innkjøpssjef eller -agent kan opprette og vedlikeholde forespørselstyper i samsvar med innkjøpskravene i organisasjonen. Hver forespørselstype kan knyttes til en poengsummetode. Poengberegningsmetoder består av et sett med vilkår som kan brukes når du gir poeng til bud. Du må definere forespørselstyper, poengberegningsmetode og poengkriterier på siden **Forespørselstype** og **Poengberegningsmetode**.

## <a name="choose-default-fields-to-include-in-vendor-rfq-reply-forms"></a><a name="default-reply-fields"></a>Velg standardfelt som skal tas med i svarskjemaer for leverandørtilbudsforespørsel

Du kan angi spesifikke typer informasjonen du vil motta fra leverandører når de svarer på (byr på) en tilbudsforespørsel. Felt som du merker som standard, er inkludert i det elektroniske skjemaet som er tilgjengelig for leverandørsamarbeid. Slik endrer du disse innstillingene:

1. Hvis du ikke allerede har gjort det, kan du bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-siden til å aktivere funksjonen *Velg felt for tilbudsforespørsel som skal inkluderes i svarskjemaer for leverandørtilbudsforespørsel*.
1. Gå til **Innkjøp og leverandører > Oppsett > Parametere for innkjøp og leverandører**.
1. Åpne fanen **Tilbudsforespørsel**.
1. Velg koblingen for svarfeltene for **Standard tilbudsforespørsler** under overskriften **Definer standardverdier for tilbudsforespørsler**.
1. Dialogboksen for **Standard svarfelt i tilbudsforespørsel** åpnes.
1. Delen **Felt for tilbudsforespørsel som er inkludert i svarskjemaer for leverandørtilbudsforespørsel** inneholder en glidebryter for hvert felt som er tilgjengelig for bruk i svarskjemaer for tilbudsforespørsler. Felt som er satt til *Ja* i denne delen, inkluderes (sammen med verdiene) i svarskjemaer for tilbudsforespørsel. Sett glidebryteren til *Nei* for hvert felt der du vil forhindre at leverandører ser data når de ser gjennom bud. Dette gir deg muligheten til å angi estimerte eller forventede verdier under registrering av tilbudsforespørsel for interne formål uten at leverandøren ser hva som er registrert.

Du kan overstyre disse innstillingene for individuelle tilbudsforespørsler etter behov.

## <a name="creating-and-sending-an-rfq"></a>Opprette og sende en tilbudsforespørsel

Du oppretter en tilbudsforespørselssak, velger leverandørene du vil skal by på tilbudsforespørselssak, og sender deretter tilbudsforespørselen til leverandørene. Du kan bruke utskriftsinnstillinger til å rute forespørselsrapporten og svararkrapportene til det foretrukne målet.

Du kan manuelt opprette en tilbudsforespørselssak for innkjøpstypen **Bestilling** eller innkjøpstypen **Kjøpsavtale**.

Hvis tilbudsforespørselssaken er av typen **Bestilling**, skjer følgende avvik fra andre typer tilbudsforespørselssaker:

- Når du oppretter linjer i saker om tilbudsforespørsel, genereres lagertransaksjoner som har tilgangsstatusen **Tilbud tilgang**.
- Når du godkjenner et bud, genereres en bestilling.

Hvis tilbudsforespørselen er av typen **Kjøpsavtale**, skjer følgende avvik fra andre tilbudsforespørselssaker:

- Tilbudsforespørselssaken brukes for en avtale om å kjøpe et spesifikt antall eller en verdi av et produkt over tid. Du må velge datointervallet som gjelder for kjøpsavtalen, og navnet på personen som administrerer kjøpsavtalen.
- Når du godkjenner et bud, genereres en kjøpsavtale.

Hvis tilbudsforespørselssaken blir generert fra en innkjøpsrekvisisjon, tilordnes typen **innkjøpsrekvisisjon** automatisk. Du kan ikke opprette en tilbudsforespørselssak manuelt for typen **Innkjøpsrekvisisjon**.

Du kan opprette en tilbudsforespørselssak fra en innkjøpsrekvisisjon bare hvis statusen for innkjøpsrekvisisjonen er **Til vurdering** og du er tildelt den neste arbeidsflytoppgaven. Linjene i innkjøpsrekvisisjonen oppdateres automatisk når du godtar linjer fra bud (svar på tilbudsforespørsler) som du mottok fra leverandører. Du kan ikke fullføre, avvise, godkjenne eller utføre andre handlinger for innkjøpsrekvisisjonen før rekvisisjonslinjen oppdateres med en godtatt tilbudsforespørselslinje eller tilbudsforespørselssaken avbrytes.

Når du oppretter en tilbudsforespørselssak, kan du velge en forespørselstype. Forespørselstypen bestemmer settet med poengkriterier som brukes til å gi poeng på forespørselssvar på tilbudsforespørselssaken.

Du kan legge til et spørreskjema i en tilbudsforespørselssak. Dette spørreskjemaet vises deretter i alle forespørselssvar når du har sendt forespørselen. Det er en obligatorisk oppgave å fullføre spørreskjemaet før budet kan sendes.

Selv om det er angitt standardverdier, kan du endre innstillingene **Felt for tilbudsforespørsel som er inkludert i svarskjemaer for leverandørtilbudsforespørsel** for hver enkelt tilbudsforespørsel etter behov. Dette gjør du ved å opprette eller åpne en tilbudsforespørsel. Gå deretter til Handling-ruten, åpne fanen **Tilbud**, gå til delen **Svar** og velg **Angi standardsvar for tilbudsforespørsel**. Dialogboksen **Standard svarfelt i tilbudsforespørsel** åpnes, og dette fungerer på samme måte som når du angir standardinnstillinger for svarskjemaer for leverandørtilbudsforespørsler, bortsett fra at endringene her bare vil påvirke gjeldende tilbudsforespørsel. Hvis du vil ha mer informasjon om hvordan du aktiverer denne funksjonaliteten og hvordan den fungerer, kan du se [Velge standardfelt som skal tas med i svarskjemaer for leverandørtilbudsforespørsel](#default-reply-fields).

Det finnes tre måter å velge leverandørene som du vil legge til en forespørselssak:

- Legg til leverandørene enkeltvis.
- Søk etter alle leverandører som oppfyller bestemte vilkår.
- Legg automatisk til alle leverandører som er godkjent for innkjøpskategoriene som brukes på linjer i saker om tilbudsforespørsel.

Når tilbudsforespørselssaken er klar, velger du **Send**. Send-handlingen genererer journaler og rapporter som blir skrevet ut, arkivert, og sendt i henhold til utskriftsinnstillingene.

Hvis du satte **Bruk leverandør til omberegning av priser** og **Bruk leverandørspesifikk vareinformasjon** til **Ja** på siden **Sender tilbudsforespørsel** da du sendte tilbudsforespørselen til en leverandør, angis noe leverandørspesifikk informasjon automatisk i tilbudsforespørselen for denne leverandøren.

## <a name="amending-an-rfq-case"></a>Endre en tilbudsforespørselssak

Noen ganger må du endre en tilbudsforespørselssak etter at du har sendt den. Du kan for eksempel være nødt til å endre en tilbudsforespørselssak hvis leveringsdatoene er endret, eller hvis du vil ha flere produkter eller et annet antall produkter. Du kan konfigurere endringsprosessen slik at den er mer restriktiv eller mindre restriktiv.

Hvis du konfigurerer endringsprosessen slik at den blir mer restriktiv, må du, før du kan endre feltene i en RFQ-sak som allerede er sendt, velge **Opprett** i RFQ-saken for å starte en endring. Når du har fullført endringene, må du velge **Fullfør**. Du blir deretter veiledet gjennom prosessen med å legge til informasjon i e-postmeldingen som sendes for å varsle leverandører om endringen. Den oppdaterte tilbudsforespørselsrapporten som inneholder en merknad om endringen, legges automatisk til i e-postmeldingen.

Hvis du konfigurerer endringsprosessen slik at den er mindre restriktiv, trenger du ikke velge **Opprett** før du kan endre feltene i en tilbudsforespørselssak som allerede er sendt. Du må imidlertid manuelt legge til en endringsmerknad i tilbudsforespørselen og sende saken på nytt. Vær oppmerksom på at denne fremgangsmåten kan bare brukes hvis ingen av svarene (budene) er endret. Hvis du har angitt et svar, og det er i en **Mottatt**-tilstand, er **Send**-knappen utilgjengelig. I så fall må du velge **Opprett** og **Fullfør**, slik du må du i den mer restriktive prosessen. Svaret tilbakestilles deretter for å gjenspeile endringene i tilbudsforespørselssaken.

Hvis leverandører bruker grensesnittet for leverandørsamarbeid til å legge inn bud, må du alltid bruke endringsprosessen til å varsle leverandører om endringer i tilbudsforespørselssaken. Denne prosessen forhindrer en situasjon der leverandører byr på en utdatert tilbudsforespørselssak mens budet er under behandling. Hvis du vil ha mer informasjon om leverandørsamarbeid, kan du se [Leverandørsamarbeid med eksterne leverandører](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors).

Hvis du vil invitere flere leverandører til å by, og ingen endringer er gjort i tilbudsforespørselssaken, kan du bruke **Send**-knappen. Leverandørene du har lagt til, vises på **Send**-siden, og de mottar e-postinvitasjonen.

## <a name="receiving-and-registering-rfq-replies"></a>Motta og registrere svar på tilbudsforespørsler (bud)

Når du sender en tilbudsforespørsel, opprettes det automatisk et svarark. Når du mottar bud på en tilbudsforespørsel, må du angi dem via **Tilbudsforespørsel**-siden ved å klikke handlingen **Rediger svar på tilbudsforespørsel.** Dermed kan du legge inn budinformasjonen i et eget budskjema. **Svarfremdrift** er først **Ikke startet**. Når du klikker **Rediger svar på tilbudsforespørsel,** er fremdriftsstatusen **Innkjøper oppdaterer** til budet er sendt. Klikk på **Send** når du har registrert nødvendig informasjon for budet. Statusen til svarfremdriften endres til **Sendt av innkjøper.** Når leverandørsamarbeid er aktivert, oppdateres **svarfremdriften** tilsvarende når leverandøren samhandler med budet. Statusen endres deretter fra **Leverandør oppdaterer** til **Rapportert av leverandør**. Når budet er sendt, opprettes en journal som **Mottatt**. Svaret (budet) må sendes for å kunne registreres som mottatt, og bare deretter kan det viderebehandles som godkjent eller avvist.

Hvis du må oppdatere budet, bør du gå gjennom den samme prosessen som ovenfor, og sende på nytt.

Legg merke til at redigering av **Tilbudsforespørsel**-skjemaet bare er tillatt for informasjon som er knyttet til behandling av budet, ikke til å legge inn budet. Hvis du vil angi eller endre budet, klikker du **Rediger svar på tilbudsforespørsel.**

Når du legger inn budinformasjonen, og hvis tilbudsforespørselssaken gir alternative linjer, kan du legge til alternative linjer for linjer som bare har en innkjøpskategori og ingen varekatalog angitt. Klikk på **Legg til alternativ** for å legge til alternative linjer.

Hvis du har skrevet inn et svar, men krever et nytt tilbud fra leverandøren, kan du returnere tilbudsforespørselen. Det genereres en ny journal og en rapport, som kan sendes til leverandøren.

Du kan se en oversikt over alle tilbudsforespørsler og statusen deres: **Sendt, Mottatt, Godtatt, Avslått, Annullert, Avvist** på siden **Oppfølging av tilbudsforespørsel**.

### <a name="accepting-and-rejecting-bids-and-transferring-accepted-bids-to-downstream-documents"></a>Godta og avvise bud, og overføre godtatte bud til nedstrøms dokumenter

Når du har identifisert det beste budet, for eksempel budet som gir best totalpris, kan du godta det. Du kan godta flere linjer i et bud og avvise andre.
Du kan også godta linjer fra forskjellige leverandører. Vær oppmerksom på at hvis du godtar noen linjer, blir du bedt å avvise alle de andre linjene. Hvis du ønsker å godta andre linjer, må du derfor velge **Avbryt** når du blir bedt om det. Statusen for svaret på tilbudsforespørselen for hver leverandør som du godtar bud eller linjer fra, blir oppdatert til **Godkjent**.

Hvis du, mens du klargjør bestillingen eller kjøpsavtalen, må du legge til en ekstra linje i forespørselen, kan du gjøre det ved å klikke **Legg til linje** i rutenettet på **Tilbudsforespørsel**-siden. Du kan bare vise og redigere denne linjen på **Tilbudsforespørsel**-siden. Den vil være synlig på budsiden når den er godtatt.

Når du godtar et bud eller en eller flere linjer i et bud, opprettes en bestilling eller kjøpsavtale automatisk. Du kan deretter avvise budene fra de andre leverandørene.

I svaret kan du legge til en årsakskode for å forklare hvorfor du godkjente eller avviste et bud.

Når du godkjenner et bud av typen **Innkjøpsrekvisisjon**, vil innkjøpsrekvisisjonslinjene bli oppdatert med følgende informasjon som viser informasjonen om godkjente budet:

- Enhetspris
- Rabattprosent
- Rabattbeløp
- Innkjøpsgebyrer
- Linjetillegg
- Leverandør
- Eksternt nummer
- Ekstern beskrivelse

Tabellen nedenfor viser hvordan forespørselsstatusen endres etter som du godtar eller avviser bud fra leverandørene.

## <a name="statuses--highest-and-lowest"></a>Statuser – høyest og lavest

I fanen Leverandør i tilbudsforespørselssaken kan du se linjene med den høyeste og laveste statusen for en bestemt leverandør. Når leverandøren er lagt til, og ingen linjer er sendt ennå, blir både den laveste og den høyeste statusen <strong>opprettet</strong>. Når tilbudsforespørselen sendes til leverandøren med alle linjer, blir statusen for de to linjene <strong>Sendt</strong>. Hvis noen av linjene i et bud fra en leverandør er godkjent og andre avvist, får de avviste linjene den laveste statusen som er <strong>Avvist</strong>, og de godkjente linjene får den høyeste statusen som er <strong>Godkjent</strong>.

På linjene i saker om tilbudsforespørsel kan du se den høyeste og laveste statusen per linje på tvers av alle leverandører. Hvis du har sendt en linje for alle leverandørene i tilbudsforespørselssaken, og ingen har svart ennå, er både den laveste og høyeste statusen **Sendt.** Når minst én leverandør svarer, endres den høyeste statusen til **Mottatt**. Hvis du legger til en ny leverandør i saken, endres den laveste statusen til **Opprettet**.

Den høyeste og den laveste statusen for tilbudsforespørselssaken er en aggregering av statusen i fanen \<Leverandør og fanen Linjer.

Statusene rangeres på denne måten fra laveste til høyeste: opprettet, sendt, mottatt, avslått, godtatt, avvist, annullert.

Tabellen nedenfor viser hvordan statusen til tilbudsforespørselssaken endres når du oppretter en tilbudsforespørselssak med linjer og sender den til leverandører.

| **Handling**                                | **Laveste status for tilbudsforespørselssak** | **Høyeste status for tilbudsforespørselssak** | **Laveste status for sakslinje for tilbudsforespørsel** | **Høyeste status for sakslinje for tilbudsforespørsel** |
|-------------------------------------------|----------------------------|-----------------------------|---------------------------------|----------------------------------|
| Opprett hodet og linjen for tilbudsforespørselssak.      | Opprettet                    | Opprettet                     | Opprettet                         | Opprettet                          |
| Send tilbudsforespørsler til alle leverandører i tilbudsforespørselssaken. | Sendt                       | Sendt                        | Sendt                            | Sendt                             |
| Legg til en annen leverandør.                       | Opprettet                    | Sendt                        | Opprettet                         | Sendt                             |
| Send tilbudsforespørselen til den andre leverandøren.        | Sendt                       | Sendt                        | Sendt                            | Sendt                             |

Alle linjene i den tilbudsforespørsler som er knyttet til tilbudsforespørselssaken, vil ha tilstanden **Sendt**.

Tabellen nedenfor viser hvordan forespørselsstatusen endres når du mottar bud og registrerer informasjonen i svararket for tilbudsforespørselen.

| **Handling**                                               | **Laveste status på tvers av alle linjer for alle tilbudsforespørsler** | **Høyeste status på tvers av alle linjer for alle tilbudsforespørsler** | **Laveste status for hode for tilbudsforespørselssak** | **Høyeste status for hode for tilbudsforespørselssak** | **Laveste status for sakslinje for tilbudsforespørsel** | **Høyeste status for sakslinje for tilbudsforespørsel** |
|----------------------------------------------------------|------------------------------------------------|-------------------------------------------------|-----------------------------------|------------------------------------|---------------------------------|----------------------------------|
| Registrer én leverandørs bud for en tilbudsforespørsel, og lagre det.        | Sendt                                           | Mottatt                                        | Sendt                              | Mottatt                           | Sendt                            | Mottatt                         |
| Registrer den andre leverandørens bud for en tilbudsforespørsel, og lagre det. | Mottatt                                       | Mottatt                                        | Mottatt                          | Mottatt                           | Mottatt                        | Mottatt                         |


I eksemplet nedenfor du kan se den høyeste og laveste statusen på tilbudsforespørselssaken der ett bud er mottatt og det andre budet er godtatt. Når et mottatt bud avvises, endres den laveste statusen fra mottatt til avvist på hodet og linjen for tilbudsforespørselssaken.


|            <strong>Handling</strong>             | <strong>Laveste status på tvers av alle linjer for alle tilbudsforespørsler</strong> | <strong>Høyeste status på tvers av alle linjer for alle tilbudsforespørsler</strong> | <strong>Laveste status for hode for tilbudsforespørselssak</strong> | <strong>Høyeste status for hode for tilbudsforespørselssak</strong> | <strong>Laveste status for sakslinje for tilbudsforespørsel</strong> | <strong>Høyeste status for sakslinje for tilbudsforespørsel</strong> |
|------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------|-------------------------------------------------|----------------------------------------------|-----------------------------------------------|
| Godta et av budene. (eller minst én linje) |                          Mottatt                           |                           Godtatt                           |                    Mottatt                    |                    Godtatt                     |                   Mottatt                   |                   Godtatt                    |
|           Avvis alle de andre budene.           |                          Avslått                           |                           Godtatt                           |                    Avslått                    |                    Godtatt                     |                   Avslått                   |                   Godtatt                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]