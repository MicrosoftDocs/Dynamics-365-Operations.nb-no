---
title: Kjøp av cXML-forbedringer
description: Funksjonen Kjøp av cXML-forbedringer bygger på den eksisterende eksternekatalogfunksjonaliteten, Utstempling, som brukes for innkjøpsrekvisisjoner.
author: dasani-madipalli
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d61087d21035e532ad86b6669626f55e8411a6f421bf69f817199e9063417761
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779620"
---
# <a name="purchasing-cxml-enhancements"></a>Kjøp av cXML-forbedringer

[!include [banner](../includes/banner.md)]

Funksjonen _Kjøp av cXML-forbedringer_ bygger på den [eksisterende eksterne katalogfunksjonaliteten](set-up-external-catalog-for-punchout.md) som brukes for innkjøpsrekvisisjoner. Denne eksisterende funksjonaliteten kalles _Utstempling_. Selv om en bestilling ikke trenger å starte fra en innkjøpsrekvisisjon, må det være en forbindelse mellom leverandøren i en bestilling og parameterne som brukes til å sende bestillingsdokumentet.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>Slå på funksjonen Kjøp av cXML-forbedringer

Du aktiverer funksjonen ved å åpne **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**-siden og søke etter funksjonen som heter *Kjøp av cXML-forbedringer*. Velg funksjonen, og velg deretter **Aktiver nå** for å slå den på.

Når du har aktivert funksjonen, bør du konfigurere innstillingene i følgende tre områder:

- **[cXML-parametere](#cxml-parameters)** – Bruk disse innstillingene til å definere noen globale parametere for funksjonaliteten for å sende bestillinger.
- **[Leverandøroppsett](#vendor-setup)** – Hvis cXML (Commerce eXtensible Markup Language) skal brukes som standard for alle nye bestillinger som opprettes for en leverandør, setter du alternativet **Send bestilling via cXML** til _Ja_ for denne leverandøren.
- **[Eksterne kataloger](#external-catalog-setup)** – Bruk de nye innstillingene for **Bestillingsegenskaper** for å definere formatet til bestillingsdokumentet og hvordan det sendes.

Illustrasjonen nedenfor inneholder en oversikt over denne konfigurasjonen.

![Områder for oppsett av cXML-funksjoner.](media/cxml-settings-areas.png "Områder for oppsett av cXML-funksjoner")

I tillegg må du definere den [satsvise jobben for bestillingsforespørsel ](#po-batch). Denne satsvise jobben brukes til å sende de bekreftede bestillingene.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Definere globale cXML-parametere

Bruk siden for **cXML-parametere** til å gjøre noen globale innstillinger som gjelder for funksjonaliteten for sending av bestillinger.

![side for parametere for cXML.](media/cxml-parameters.png "Side for parametere for cXML")

Gå til **Innkjøp og leverandører \> Oppsett \> cXML-behandling \> cXML-parametere**, og angi følgende parametere:

- **Testmodus for cXML** – Denne globale parameteren påvirker hvordan bestillinger sendes fysisk fra den satsvise jobben. Velg én av følgende verdier:

    - **Test** – I denne modusen kan den satsvise jobben kjøres, og XML-dokumentet for meldingen genereres, men blir ikke sendt. I stedet blir den lagret på bestillingsforespørselen for kontrollformål. Denne modusen er nyttig når du er i en første implementering og vil se hvordan data registreres i cXML-meldingen. Du vil kanskje også generere eksempelmeldinger som du kan sende til leverandører for innledende validering.
    - **Direkte** – I denne modusen bruker funksjonen [innstillinger for ekstern katalog](#external-catalog-setup) til å overføre hvert dokument fysisk til leverandøren.

- **Send oppdateringer for innkjøpsforespørsel** – Sett dette alternativet til *Ja* for å sende en oppdateringsmelding for bestillinger. Sett den til *Nei* for å hindre at meldingen sendes. De fleste leverandører foretrekker ikke å motta oppdateringsmeldinger. I stedet krever de at kundene kontakter dem via telefon eller e-post hvis en bestilling skal endres. Denne parameteren er en global parameter, og det kan ikke angis noen overstyring for hver leverandør i den eksterne katalogen. En bestilling vil bli merket som oppdatert hvis du posterer en bekreftelse nummer to på en bestilling, men den første bekreftelsen er allerede sendt og godkjent av leverandøren. Hvis det er en andre bekreftelse, men den første bekreftelsen ikke er sendt, blir den andre bekreftelsen behandlet som et nytt dokument. Du kan bekrefte en bestilling så mange ganger du vil, til en bekreftelse sendes. Den neste bekreftelsen blir deretter behandlet som en oppdateringsmelding.
- **Send sletting for innkjøpsforespørsel** – Sett dette alternativet til *Ja* for å sende en slettemelding for bestillinger. Sett den til *Nei* for å hindre at meldingen sendes. De fleste leverandører foretrekker ikke å motta slettemeldinger. I stedet krever de at kundene kontakter dem via telefon eller e-post hvis en bestilling ble sendt ved en feil. Denne parameteren er en global parameter, og det kan ikke angis noen overstyring for hver leverandør i den eksterne katalogen. En bestilling blir merket som slettet hvis du avbryter bestillingen i Supply Chain Management.
- **Arkivfil** – Angi filbanen der du vil eksportere og lagre arkiverte cXML-dokumenter. Banen brukes når du kjører slettingsfunksjonen fra siden **Bestillingsforespørsel**.
- **Maks tegn for gatelinje** – Angi maksimalt antall tegn som kan brukes i gatefeltet for adresser i cXML-dokumentet. Denne globale parameteren påvirker alle leverandører med mindre en overstyring er angitt for egenskapene for den eksterne katalogen.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Definere leverandørbestillinger som skal bruke cXML

Hver gang du bekrefter at en bestilling der alternativet **Send bestilling via cXML** er satt til _Ja_, genererer systemet automatisk cXML-meldingen og leverer den til leverandøren som er knyttet til bestillingen. Det finnes to måter å styre dette alternativet for bestillingene på:

- Hvis du vil definere en leverandør, slik at den automatisk bruker cXML for alle nye bestillinger som opprettes fra en rekvisisjon, går du til **Innkjøp og leverandører \> Leverandører \> Alle leverandører** og velger eller oppretter en leverandør for å åpne detaljsiden. På hurtigfanen **Bestillingsstandarder** setter du deretter alternativet **Send bestilling via cXML** til _Ja_. Hvis cXML også automatisk skal brukes for nye bestillinger som **ikke** er opprettet fra en rekvisisjon, må du også sette bestillingsegenskapen **ENABLEMANUALPO** til _Sann_ for den tilknyttede eksterne katalogen, som beskrevet i delen [Angi bestillingsegenskaper](#set-order-properties) senere i dette emnet.
- For individuelle bestillinger går du til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger** og velger eller oppretter en bestilling for å åpne detaljsiden. Bytt til visningen **Hode** og deretter, i hurtigfanen **Oppsett**, angir du alternativet **Send bestilling via cXML** etter behov.

![Standardinnstillinger for leverandørbestillinger.](media/cxml-order-defaults.png "Standardinnstillinger for leverandørbestillinger")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Opprette en ekstern katalog for å bruke cXML

På siden **Eksterne kataloger** kan du definere eksternordrefunksjonaliteten og funksjonaliteten for å sende bestillinger for hver av katalogene. For å finne de aktuelle innstillingene går du til **Innkjøp og leverandører \> Kataloger \> Eksterne kataloger**. Begynn med å [definere hver katalog som vanlig](set-up-external-catalog-for-punchout.md). Denne prosessen omfatter tilordning av en leverandør, valg av kategoriene som leverandøren har tillatelse til å levere, og aktivering av katalogen. Deretter konfigurerer du tilleggsinnstillingene som er beskrevet i denne delen.

> [!NOTE]
> Når du bekrefter en bestilling som kan sendes via cXML, slår systemet på leverandøren som er knyttet til bestillingen, og finner deretter den første aktive eksterne katalogen som er knyttet til denne leverandøren. Systemet bruker deretter innstillingene fra den eksterne katalogen til å sende bestillingen. Hvis det er definert flere eksterne kataloger, bruker systemet bare den første eksterne katalogen den finner, basert på leverandøren i bestillingen. Derfor anbefaler vi at du oppretter bare én ekstern katalog for hver leverandør.

![Innstillinger for ekstern katalog.](media/cxml-supplier-catalog.png "Innstillinger for ekstern katalog")

### <a name="set-the-punchout-protocol-type"></a>Angi protokolltype for eksternordre

På hurtigfanen **Generelt** på siden **Eksterne kataloger** setter du feltet **Protokolltype for eksternordre** til _cXML_. Dette alternativet er det eneste tilgjengelige alternativet, med mindre en partner har utvidet funksjonaliteten og gir et ekstra alternativ i utvidelsen.

Hvis du også bruker katalogen for eksternordre, må du også [angi meldingsformatet](set-up-external-catalog-for-punchout.md). Meldingsformatet brukes til å opprette forbindelsen til leverandøren i eksternordretransaksjonen fra rekvisisjonen. Når en bestilling er sendt, brukes ordreegenskapene til å opprette forbindelsen til en leverandør.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Angi bestillingsegenskaper

Funksjonen _Kjøp av cXML-forbedringer_ legger til en ny hurtigfane **Ordreegenskaper** for eksterne kataloger. Denne hurtigfanen gir et rutenett der du kan definere ordreegenskapene. Den inneholder også en verktøylinje. Denne verktøylinjen inneholder følgende tre knapper som du kan bruke til å behandle ordreegenskapene:

- **Standardegenskaper** – Når du oppretter en ny katalog, velger du denne knappen for å legge til en forhåndsdefinert samling av mest brukte egenskaper i rutenettet.
- **Ny** – Legg til en ny egenskap i rutenettet.
- **Slett** – Slett den gjeldende valgte egenskapen fra rutenettet. Hvis du sletter en standardegenskap ved en feiltakelse, velger du **Standardegenskaper** for å gjenopprette alle de manglende egenskapene.

Hver gang du legger til én eller flere egenskaper i rutenettet, bruker du kolonnen til høyre for å angi en verdi for hver av dem.

Bruk standardegenskapene på følgende måte:

- **BUYER\_COOKIE** – Dette sporingsfeltet kan brukes til å angi bestemt informasjon for selskapet. Med mindre du har en avtale med leverandøren om hvordan denne egenskapen brukes, har den ikke så mye betydning når det sendes en bestilling. Derfor bør du sette den til en enkel verdi.
- **DELIVERTO** – Når leveringsadressen angis i dokumentet fra bestillingen, brukes feltet **Kontaktinformasjon** til å angi **DeliverTo**-feltet i XML-meldingen. Hvis du krever at denne verdien er et navn på en forespørsel, og du angir bestiller-feltet i bestillings hodet, angir du en verdi _REQUESTER_ for denne egenskapen, slik at navnet på anmoderen blir angitt i **DeliverTo**-feltet i XML. I dette tilfellet kommer den primære e-postadressen og telefonnummeret som brukes, fra bestilleren i stedet for ordren.
- **DEPLOYMENTMODE** – Angi denne egenskapen i henhold til leverandørs krav. Verdiene er vanligvis _PRODUCTION_ eller _TEST_. Angi verdien basert på din kommunikasjon med leverandøren. Vanligvis må den samsvare med det tiltenkte systemet bak **ORDERCHECKURL**-verdien som leverandøren angir som en test eller et produksjonssystem.
- **FIXEDBILLADDRESSID** – Når feltet **addressID** i XML-meldingen er angitt, henter det lokasjonen som er angitt for adressen. Hvis ID-verdien du har kommunisert til leverandøren, er forskjellig fra verdien på adresselokasjonen av en eller annen grunn, kan du tvinge frem en overstyring ved å angi verdien her. Det antas at du bare vil bruke én adresse hos leverandøren, og at adressen er satt opp i leverandørens system. Faktureringsadressen er den viktigste faktura adressen som er angitt for den juridiske enheten i Supply Chain Management.
- **FIXEDSHIPADDRESSID** – Når feltet **addressID** i XML-meldingen er angitt, henter det lokasjonen som er angitt for adressen. Hvis ID-verdien du har kommunisert til leverandøren, er forskjellig fra verdien på adresselokasjonen av en eller annen grunn, kan du tvinge frem en overstyring ved å angi verdien her. Det antas at du bare vil bruke én adresse hos leverandøren, og at adressen er satt opp i leverandørens system. Forsendelsesadressen er adressen som er angitt i hodet i bestillingen. De fleste leverandører godtar bare hodeadresser, ikke linjeadresser. Selv om det er felt for linjeadresser i XML, blir de satt til hodeadressen.
- **FROM\_DOMAIN** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **FROM\_IDENTITY** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **ORDERCHECKURL** – Angi URL-adressen som bestillingsdokumentene skal overføres til. Denne URL-adressen starter med `https://` og leveres av leverandøren.
- **PAYLOAD\_ID** – Angi en prefiksverdi for nyttelast-IDen, som nødvendig for forretningsprosessene som finnes for den gjeldende leverandøren.
- **SENDER\_DOMAIN** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **SENDER\_IDENTITY** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **SHARED\_SECRET** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **STREETLENGTH** – Angi et nummer som representerer maksimalt antall tegn som leverandøren vil godta som et gatenavn. Hvis du angir en verdi her, overstyres verdien som er angitt på siden **cXML-parametere**. Systemet vil fjerne linjeskift og mellomrom for å forsøke å tilpasse standardadressen i Supply Chain Management til antall tegn som er angitt her. Andre tegn blir avkortet.
- **TO\_DOMAIN** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **TO\_IDENTITY** – Angi verdien som brukes til å sende bestillingsdokumenter. Denne verdien oppgis av leverandøren.
- **USERAGENT** – Angi en verdi som identifiserer systemet du bruker. Skriv for eksempel inn _Dynamics 365 Supply Chain Management_.
- **VERSION** – Angi et cXML-versjonsnummer hvis leverandøren ber om denne informasjonen. Standardversjonen er *1.2.008*. Denne versjonen er stabil og godtas av de fleste leverandører.
- **RESPONSETEXT** – Angi eventuell egendefinert tekst som du forventer at leverandøren skal returnere i cXML-svarmeldingen etter at ordren er sendt. På denne måten kan systemet merke meldingen som _Bekreftet_. Hvis svaret ikke samsvarer med standardtekst eller kundeteksten du angir her, blir forespørselen merket som _Feil_.
- **RESPONSETEXTSUB** – Sett denne egenskapen til _TRUE_ hvis du vil søke i leverandørsvarteksten for verdiene som er angitt i **RESPONSETEXT**-feltet. Leverandøren kan for eksempel returnere en lang streng som inneholder "OK" i svaret. I dette tilfellet kan du angi _OK_ i feltet **RESPONSETEXT** og angi **RESPONSETESTSUB** til _TRUE_ for å søke etter "OK" hvor som helst i svaret. Ordren kan deretter settes til _Bekreftet_.
- **CONTENTTYPE** – I et typisk katalogoppsett trenger du ikke å angi denne egenskapen. Hvis du mottar en server 500-feil fra leverandørens system når du sender en bestilling, kan du teste ved å sette denne egenskapen til _FALSE_. Denne verdien vil endre en innstilling i webforespørselen, og kan føre til at meldingen sendes for enkelte plattformer.
- **ENABLEHEADERS** – Sett denne egenskapen til _TRUE_ for å sende hoder sammen med bestillingen. Du må bare angi denne egenskapen hvis leverandøren krever det. Hvis du setter denne egenskapen til _TRUE_, legger du til ekstra egendefinerte egenskaper som er basert på navnene som leverandøren gir, og du kan starte dem med _H\__. Vanlige eksempler er **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** og **H\_ACTIONREQUEST**. Følgende egendefinerte egenskaper er inkludert i standardegenskapene:

    - **H\_USERID** – Hvis handelspartneren krever at du sender en bruker-ID som del av URL-adressen for å sende en bestilling, angir du verdien her.
    - **H\_PASSWORD** – Hvis handelspartneren krever at du sender et passord som del av URL-adressen for å sende en bestilling, angir du verdien her.

- **ENABLEMANUALPO** – Hvis denne egenskapen er satt til _TRUE_, vil disse bestillingene i manuell oppretting av bestillinger (det vil si når de ikke starter fra en rekvisisjon) arve innstillingen for alternativet **Send bestilling via cXML** fra leverandøren. Hvis denne egenskapen ikke er angitt, eller hvis den er satt til _FALSE_, vil ikke alternativet **Send bestilling via cXML** bli angitt på bestillingshodet for manuelt opprettede bestillinger. For bestillinger som opprettes fra en rekvisisjon, vil innstillingen for alternativet **Send bestilling via cXML** alltid arves fra leverandøren, uavhengig av innstillingen for denne egenskapen. Hvis du vil ha mer informasjon, kan du se delen [Definere leverandørbestillinger som skal bruke cXML](#vendor-setup) tidligere i dette emnet.
- **PUNCHOUTPOONLY** – Hvis denne egenskapen er satt til _TRUE_, vil bare innkjøpsrekvisisjonslinjer som er opprettet fra eksternordreprosessen, angi alternativet **Send bestilling via cXML** i bestilingshodet. I tillegg må innkjøpsrekvisisjonslinjetypen for alle linjene i bestillingen være en _Ekstern katalogvare_. Ellers kan ikke cXML-bestillingen opprettes.
- **PUNCHOUTSHIPTO** – Hvis denne egenskapen er satt til _TRUE_, legges standardadressen til den juridiske enheten til i forespørselsmeldingen om eksternordreoppsett når brukeren åpner en ekstern katalog. Denne adressen legges til som **ShipTo** -adresse. Leverandører vil bruke **ShipTo**-adressen til å vise prissetting basert på firmalokasjonen.
- **TRACEPUNCHOUT** – Sett denne egenskapen til _TRUE_ hvis du får en feilmelding når du prøver å bla til en ekstern katalog fra rekvisisjonen. Sporingsinformasjonen fylles deretter ut for **PunchOutSetupRequest**- og **PunchOutResponse**-meldingene som sendes mellom Supply Chain Management og leverandørområdet. Du kan vise denne informasjonen på siden for **meldingslogg for cXML-handlekurv**, som du kan åpne fra siden **Oppsett av ekstern katalog** for leverandørkatalogen som du har problemer med. Du bør bare sette denne egenskapen til _TRUE_ hvis du feilsøker, fordi den oppretter en stor kostnad i databasen for hver eksternordre. Hvis du vil ha mer informasjon, kan du se [Vise meldingsloggen for cXML-handlekurv for ekstern katalog for eksternordre](#message-log) senere i dette emnet.
- **REPLACENEWLINE** – Sett denne egenskapen til _TRUE_ hvis du får et problem fordi en leverandørs system sender en **PunchOutResponse**-melding som inneholder linjeskifttegn (\\n). Dette problemet kan oppstå hvis leverandørens meldinger analyseres via mellomvare eller en innkjøpshub. Hvis du har et problem med et nytt leverandøroppsett, setter du egenskapen **TRACEPUNCHOUT** til _TRUE_ for å vise **PunchOutResponse**-meldingen og avgjøre om XML-kodene er delt opp med linjeskifttegn.
- **POCOMMENTS** – Sett denne egenskapen til _TRUE_ hvis du vil at cXML-dokumentet skal ta med merknader som er knyttet til bestillingen i Supply Chain Management. Vedleggsteksten blir tatt med i meldingshodemerknadene i bestillingsmeldingen. Hvis du vil ha mer informasjon om hvordan systemet velger og behandler disse vedleggene, kan du se [Legge ved merknader i en bestilling](#attach-po-notes) senere i dette emnet.
- **VENDCOMMENTS** – Sett denne egenskapen til _TRUE_ hvis du vil at cXML-dokumentet skal ta med merknader som er knyttet til bestillingen i Supply Chain Management. Vedleggsteksten blir tatt med i meldingshodemerknadene i bestillingsmeldingen. Hvis du vil ha mer informasjon om hvordan systemet velger og behandler disse vedleggene, kan du se [Legge ved merknader i en bestilling](#attach-po-notes).
- **CLEANAMP** – Sett denne egenskapen til _TRUE_ hvis du får en feilmelding når du prøver å gjøre en eksternordre til en leverandør, og leverandørens retur-URL inneholder uriktig kodede &-tegn (\&).
- **PUNCHOUTTZ** – Sett denne egenskapen til _TRUE_ hvis leverandøren du arbeider med, bruker International Organization for Standardization (ISO) 8601-standarden til å utføre en bestemt validering av datoen/klokkeslettet for forespørselsmeldingen om eksternordre. Supply Chain Management bruker UTC-datoen (Coordinated Universal Time) i **PunchOutSetupRequest**-meldingen. Når du setter denne egenskapen til _TRUE_, legges derfor *+00:00* til i dato/klokkeslett-formatet.
- **WMSADDRESSID** – Sett denne egenskapen til _TRUE_ for å bruke lagernummeret på bestillingshodet som **addressID**-verdien i **ShipTo**-adressen for bestillingsforespørselen som er sendt til leverandøren. Hvis du angir en verdi for **FIXEDSHIPADDRESSID**-egenskapen, prioriteres denne verdien over denne verdien. Du bør derfor bruke én egenskap eller den andre til å angi **addressID**-verdien i **ShipTo**-adressen for dokumentet.
- **PUNCHOUTSHIPTOUSER** – Denne egenskapen fungerer sammen med **PUNCHOUTSHIPTO**-egenskapen. Hvis **PUNCHOUTSHIPTO** er satt til _TRUE_, blir adressen til den juridiske enheten hentet. Hvis **PUNCHOUTSHIPTOUSER** er satt til _TRUE_, brukes primæradressen fra eksternordrebrukeren i stedet for adressen til den juridiske enheten.

### <a name="activate-the-external-catalog"></a>Aktivere den eksterne katalogen

Når du er ferdig med å definere alle egenskapene og konfigurere andre innstillinger for den eksterne katalogen, går du tilbake til hurtigfanen **Generelt** på siden **Eksterne kataloger**, og deretter angir du alternativet **Aktiv** til *Ja*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Knytte merknader til en bestilling

Som nevnt i delen [Angi bestillingsegenskaper](#set-order-properties), hvis du vil at den leverte cXML skal inneholde tekst fra notater som er knyttet til de relevante bestillings- og/eller leverandørposter, kan du sette egenskapen **POCOMMENTS** og/eller **VENDCOMMENTS** til _TRUE_ i det eksterne katalogoppsettet. Denne delen inneholder mer detaljert informasjon om hvordan systemet velger og behandler disse vedleggene hvis du bruker dem.

Hvis du vil angi hvilke typer merknader systemet skal se etter, kan du gå til **Innkjøp og leverandører \> Oppsett \> Skjemaer \> Fra oppsett**. Deretter kan du i fanen **Bestilling** sette feltet **Ta med dokumenter av type** til merknadstypen som du ønsker å inkludere. Det er bare tekstnotater som tas med, og ikke dokumentvedlegg.

![Skjemaoppsett-siden.](media/cxml-form-setup.png "Skjemaoppsett-siden")

Vedlegg blir bare inkludert i en bestilling hvis **Type**-feltet er satt til verdien du velger i feltet **Ta med dokumenter av type**, og hvis **Begrensning**-feltet er satt til _Eksternt_. Hvis du vil opprette, vise eller redigere vedlegg for en bestilling, kan du gå til **Innkjøp og leverandører \> Alle bestillinger**, velge eller opprette en bestilling og deretter velge **Vedlegg**-knappen (bindersikonet) øverst til høyre.

![Tilknyttet merknad som er konfigurert til å sendes til en leverandør.](media/cxml-note-to-vendor.png "Tilknyttet merknad som er konfigurert til å sendes til en leverandør")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>Vise meldingsloggen for cXML-handlekurv for ekstern katalog for eksternordre

Når du setter feltet **Protokolltype for eksternordre** til _cXML_ for en ekstern katalog, vil systemet registrere en meldingslogg for handlekurvene som kommer tilbake fra leverandører. Denne loggen kan brukes til feilsøking og andre dataformål.

Hvis du vil åpne loggen for en ekstern katalog, velger du den relevante katalogen, og deretter velger du **Meldingslogg for cXML-handlekurv** i handlingsruten. **Meldingslogg for cXML-handlekurv** viser en liste over returnerte handlekurver, XMLen som er relatert til disse handlekurvene, og linjene som ble opprettet i den tilknyttede innkjøpsrekvisisjonen.

![Side for meldingslogg for cXML-handlevogn.](media/cxml-cart-message-log.png "Side for meldingslogg for cXML-handlekurv")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Angi eksterne elementer for den eksterne katalogen for ekternordre

Når du setter feltet **Protokolltype for eksternordre** til *cXML* for en ekstern katalog, kan du legge til egendefinerte eksterne elementer som blir satt inn på riktig sted i forespørsels-XML-meldingen.

Bruk følgende fremgangsmåte for å legge til eksterne elementer i en ekstern katalog.

1. Gå til **Innkjøp og leverandører \> Kataloger \> Eksterne kataloger**.
1. Velg relevant katalog.
1. På hurtigfanen **Meldingsformat**, i delen **Eksterne**, velger du **Legg til** for å legge til en rad i rutenettet for hvert eksterne element du vil ta med. I hver rad angir du feltene nedenfor:

    - **Navn** – Angi et navn for elementet. Denne verdien blir verdien for attributtet **name** for XML-elementet **Ekstern** som opprettes av hver rad. Vanligvis arbeider du med leverandøren din for å komme frem til et navn på hvert eksternt element.
    - **Verdi** – Velg en verdi for elementet. Denne verdien blir verdien for XML-elementet som opprettes av hver rad. Følgende verdier er tilgjengelige:

        - **Brukernavn** – Bruk navnet på brukeren som utfører eksternordren. Dette navnet er påloggingsnavnet for Supply Chain Management.
        - **Brukere-post** – Bruk e-postadressen til brukeren som utfører eksternordren. Denne adressen er adressen brukeren har definert i fanen **Konto** på siden **Brukeralternativer**.
        - **Tilfeldig verdi** – Bruk en unik, tilfeldig verdi.
        - **Brukerens fullstendige navn** – Bruk fullstendig navn på kontaktpersonen som er knyttet til brukeren som har tilgang til den eksterne katalogen.
        - **Fornavn** – Bruk fornavnet til kontaktpersonen som er knyttet til brukeren som har tilgang til den eksterne katalogen.
        - **Etternavn** – Bruk etternavnet til kontaktpersonen som er knyttet til brukeren som har tilgang til den eksterne katalogen.
        - **Telefonnummer** – Bruk det primære telefonnummeret til kontaktpersonen som er knyttet til brukeren som har tilgang til den eksterne katalogen.

![Innstillinger for eksternt element.](media/cxml-extrinsics.png "Innstillinger for eksternt element")

Brukeren eller administratoren vil ikke se de eksterne elementene fordi de ikke blir lagt til før brukeren utfører en eksternordre. De settes automatisk inn mellom **BuyerCookie**- og **BrowserFromPost**-elementene i forespørselsmeldingen for cXML-oppsett. Derfor trenger du ikke å angi dem manuelt i XML-filen når du konfigurerer den eksterne katalogen.

![Eksterne elementer som er lagt til i XML.](media/cxml-extrinsics-xml.png "Eksterne elementer som er lagt til i XML")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Opprette og behandle en bestilling

Når du oppretter en bestilling for en leverandør, vil den arve innstillingen fra alternativet **Send bestilling via cXML** fra denne leverandøren. Innstillingen vil imidlertid fortsatt være tilgjengelig i hurtigfanen **Oppsett** i visningen **Hode** i bestillingen, slik at du kan endre den senere etter behov.

![Bestilling angitt til å bruke cXML.](media/cxml-purchase-order.png "Bestilling angitt til å bruke cXML")

Når du oppretter en bestilling fra en innkjøpsrekvisisjon som kom fra en eksternordreflyt, fylles alle nødvendige linjedetaljer ut. Du kan deretter legge til bestillingslinjer manuelt eller kopiere dem fra andre bestillinger. Pass på at du angir alle nødvendige felt. Disse obligatoriske feltene inkluderer det eksterne referansenummeret, som er leverandørnummeret som skal brukes i cXML-meldingen.

![Eksempel på et eksternt referansenummer.](media/cxml-line-details.png "Eksempel på et eksternt referansenummer")

Når du er ferdig med å fylle ut alle detaljene for bestillingen, må du kontrollere at du bekrefter. Ingen melding sendes med mindre bestillingen er bekreftet. For å bekrefte bestillingen går du til handlingsruten i fanen **Kjøp** i gruppen **Handlinger** og velger **Bekreft**. 

Når bestillingen er bekreftet, kan du vise statusen til bekreftelsen via **Bestillingsbekreftelser**-journalene. På handlingsruten i fanen **Kjøp** i gruppen **Journaler** velger du gruppen **Bestillingsbekrefter**.

Hver bestilling kan ha mange bekreftelser. Hver bekreftelse er merket med et trinnvis nummer. I illustrasjonen nedenfor er bestillingen *00000275*, og bekreftelsen er *00000275-1*. Denne nummereringen gjenspeiler standard Supply Chain Management-funksjonalitet, der endringer i en bestilling, og derfor typen cXML-melding som skal sendes til leverandøren, identifiseres basert på bekreftelsen. Som illustrasjonen viser inneholder siden **Bestillingsbekreftelser** også feltene for **sendestatus for bestilling** og **Leverandørstatus for bestillingsforespørsel**. Hvis du vil ha mer informasjon om de ulike statusverdiene som du kanskje vil se på denne siden, kan du se delen [Overvåke bestillingsforespørsler](#monitor-po-requests) senere i dette emnet.

![Side for bestillingsbekreftelser.](media/cxml-po-confirmations.png "Side for bestillingsbekreftelser")

Hvis du vil vise mer informasjon om dokumentet, velger du **Bestillingsforespørsel** over rutenettet.

Siden **Bestillingsforespørsel** inneholder to rutenett. Rutenettet i den øvre delen av siden har én post for hver bestilling som er merket for sending. Rutenettet i fanen **Logg for bestillingsforespørsel** i den nedre delen av siden kan ha flere poster for den valgte bestillingen, for å angi statusen for hver bekreftelse. Følgende illustrasjon viser bestillingen 00000275 i det øvre rutenettet og dokument 00000275-1 i rutenettet i fanen **Logg for bestillingsforespørsel**.

![Side for bestillingsforespørsel.](media/cxml-po-request.png "Side for bestillingsforespørsel")

Hvis den satsvise jobben er definert og kjører, vil dokumentet bli sendt. Du kan vise statusendringen etter at dokumentet er sendt. I illustrasjonen nedenfor er feltet for **Sendestatus for bestilling** satt til _Sendt_. Feltet **Leverandørstatus for bestillingsforespørsel** er satt til _Bekreftet_ for å angi at leverandøren mottok dokumentet og kunne lese det og lagre det i systemet. Rutenettet i fanen **Logg for bestillingsforespørsel** viser klokkeslettet da dokumentet ble sendt. Hvis du vil ha mer informasjon om de ulike statusverdiene som du kanskje vil se på denne siden, kan du se delen [Overvåke bestillingsforespørsler](#monitor-po-requests).

![Statusmeldinger på siden for bestillingsforespørsel.](media/cxml-po-request-2.png "Statusmeldinger på siden for bestillingsforespørsel")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Planlegge den satsvise jobben for bestillingsforespørsel

Hvis du vil aktivere den satsvise jobben for sending av bestillingsforespørsler, går du til **Innkjøp og leverandører \> Oppsett \> cXML-behandling \> Bestillingsforespørsel** og deretter, i handlingsruten i fanen **Bestillingsforespørsel** i gruppen **Parti**, velger du **Send jobb** for å åpne dialogboksen for **klargjøring og sending av bestillingsforespørsel**. Du kan bruke denne dialogboksen til å angi regelmessigheten, akkurat som du vanligvis gjør for satsvise jobber i Supply Chain Management. Velg et intervall basert på ordrevolumet. Selv om du kan kjøre den satsvise jobben hvert minutt, er det antakelig best å sende parti gjennom hele arbeidsdagen basert på ordremottaksvinduer som samsvarer med leverandørens tidsplaner.

Leverandøren har for eksempel en policy som sier at alle ordrer som mottas innen kl. 13:00, vil bli sendt samme dag. I så fall kan det hende at du bare må kjøre partiet noen ganger i morgen for å kommunisere eventuelle ordrer du har. De gjenværende ordrene blir deretter sendt neste dag. Denne beslutningen er en ren virksomhetsbeslutning. Du kan gå gjennom den og angi parameterne for den i henhold til dette.

Prosessen vil se etter bestillingsforespørselsdokumenter med statusen *Venter*. Hvis du har en ordre som du må sende til en leverandør umiddelbart, kan du velge **Send jobb** og sette alternativet for **Satsvis behandling** til *Nei*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Overvåke bestillingsforespørsler

### <a name="view-the-status-of-a-purchase-order"></a>Vise statusen for bestillingen

Når ordrer som kan sendes via cXML, bekreftes, går de inn i _Vente_-status. Som det ble beskrevet under [Opprette og behandle en bestilling](#create-po) kan du vise bestillingsstatusen på siden **Bestillingsforespørsel**. Hver bestillingsforespørsel kan ha én av flere statuser, avhengig av parameterne og dataene. Denne delen beskriver de ulike statustypene og verdiene de kan ha. Denne informasjonen kan hjelpe deg med å styre problemer og forstå statusen til bestillingene.

![Betillingsstatus på siden for bestillingsforespørsel.](media/cxml-monitor-po-request.png "Betillingsstatus på siden for bestillingsforespørsel")

Rutenettet i den øvre delen av siden **Bestillingsforespørsel** kan vise følgende statusverdier:

- **Sendestatus for bestilling** – Dette feltet kan ha en av følgende verdier:

    - **Venter** – Dokumentet venter på å bli sendt.
    - **Sendt** – Dokumentet er sendt.
    - **Stoppet** – Dokumentet ble merket som _Stoppet_ før det ble sendt. (Hvis du vil merke et dokument som _Stoppet_, velger du **Stopp** i handlingsruten på siden **Innkjøpsforespørsel** .)
    - **Arkiv** – Dokumentet er tømt. (Hvis du vil slette et dokument, velger du **Tøm** i handlingsruten på siden **Innkjøpsforespørsel**.)

- **Leverandørstatus for bestillingsforespørsel** – Dette feltet kan ha en av følgende verdier:

    - **Venter** – Dokumentet venter på å bli sendt.
    - **Bekreftet** – Dokumentet er bekreftet som mottatt av leverandøren. Du kan se gjennom den detaljerte XML-meldingen som ble returnert fra leverandøren, ved å velge fanen **Svar-XML** på den nedre delen av siden.
    - **Feil** – Dokumentet ble sendt til leverandøren, men det oppstod en feil. Du kan se gjennom feilmeldingen ved å velge **Svar-XML** i den nedre delen av siden.

Rutenettet i fanen **Logg for bestillingsforespørsel** i den nedre delen av siden **Bestillingsforespørsel** kan vise følgende verdier:

- **Bestillingstype** – Dette feltet kan ha en av følgende verdier:

    - **Ny** – Linjen merkes som ny umiddelbart etter at bestillingen er bekreftet.
    - **Oppdatering** – Hvis en bekreftelse allerede er sendt og godkjent av leverandøren, blir den neste bekreftelsen merket som _Oppdatering_. Oppdateringer sendes bare hvis alternativet **Send oppdateringer om bestillingsforespørsler** er satt til *Ja* i de [globale cXML-parameterne](#cxml-parameters).
    - **Slett** – Hvis en bekreftelse allerede er sendt og godkjent av leverandøren, men bestillingen avbrytes, vil bekreftelsen som venter, bli merket som _Slett_. Slettinger sendes bare hvis alternativet for **Send sletting for bestillingsforespørsler** er satt til *Ja* i de [globale cXML-parameterne](#cxml-parameters).

- **Forespørselstidspunkt** – Tidspunktet da ordrebekreftelsen ble opprettet. Du kan sammenligne forespørselstiden med ordrestatustiden for å bestemme tiden mellom bekreftelsen og leverandørbekreftelsen.
- **Sendestatus for ordre** – Dette feltet er det samme som feltet for **Sendestatus for ordre** i den øvre delen av siden. Det gjentas her for å gjøre det enklere å vise statusen på bekreftelsesnivået. Hvis feltet **Bestillingstype** er satt til *Ny*, og bestillingen bekreftes på nytt før det sendes en bekreftelse, settes feltet for **Sendestatus for ordre** til *Arkiv*.
- **Tidspunkt for ordrestatus** – Tidspunktet da loggposten for bestillingsforespørselen sist ble oppdatert. (Oppdateringene omfatter statusendringer.)
- **Leverandørstatus for ordreforespørsel** – Dette feltet er det samme som feltet for **Leverandørstatus for ordreforespørsel** i den øvre delen av siden. Det gjentas her for å gjøre det enklere å vise statusen på bekreftelsesnivået.
- **Tidspunkt for ny sending** – Tidspunktet da posten ble sendt på nytt.
- **Antall nye sendinger** – Antall ganger posten er sendt på nytt. Et høyt antall angir flere feil og kan derfor tyde på et problem med dataoppsettet eller leverandørens dataoppsett.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Vise XMLen for en bestillingsforespørselsmelding

Hvis du vil vise XMLen for bestillingsforespørselsmelding, velger du fanen for **Forespør XML-tekst** nederst på siden for **Bestillingsforespørsel**. Informasjonen i denne fanen kan være nyttig under testing eller feilvalide ring. Hvis du vil gjøre det enklere å lese informasjonen, kan du vise den som en formatert melding. Kopier innholdet i fanen til en tekstfil, og vis det deretter i et XML-redigeringsprogram.

![fanen for Forespør XML-tekst.](media/cxml-request-xml-text.png "fanen for Forespør XML-tekst")

### <a name="view-the-details-of-the-vendor-response"></a>Vise detaljene for leverandørsvar

Hvis du vil vise innholdet i en leverandørbekreftelse eller feilsvar, velger du fanen **Svar-XML** nederst på siden **Bestillingsforespørsel**.

![fanen Svar-XML.](media/cxml-response-xml.png "fanen Svar-XML")

## <a name="additional-resources"></a>Tilleggsressurser

- [Definer en ekstern katalog for PunchOut e-procurement](set-up-external-catalog-for-punchout.md)
- [Bruke eksterne kataloger for PunchOut e-Procurement](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]