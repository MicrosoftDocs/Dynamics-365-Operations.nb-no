---
title: Inngående lageroperasjon på salgsstedet
description: Dette emnet beskriver funksjonene til inn kommende lageroperasjoner på salgsstedet (POS).
author: hhaines
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: a14b98cab78896d3a6c2e567cadc1ff9a991a278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018960"
---
# <a name="inbound-inventory-operation-in-pos"></a>Inngående lageroperasjon i salgsstedet

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 Commerce versjon 10.0.10 og senere erstatter innkommende og utgående operasjoner på salgsstedet (POS) den plukkede og mottatte operasjonen.

> [!NOTE]
> I Commerce versjon 10.0.10 og senere legges eventuelle nye funksjoner i POS-programmet som er relatert til mottak av butikklager mot bestillinger og overførings ordrer, til POS-operasjonen **Innkommende operasjon**. Hvis du for øyeblikket bruker en plukk- og mottaksoperasjon i POS, anbefaler vi at du utvikler en strategi for flytting fra den operasjonen til de nye innkommende og utgående operasjonene. Selv om plukk- og mottaksoperasjonen ikke blir fjernet fra produktet, vil det ikke være flere investeringer i den, fra et funksjonelt eller ytelsesperspektiv etter versjon 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Forutsetning: konfigurere et asynkront dokumentrammeverk

Den innkommende operasjonen omfatter ytelsesforbedringer som sikrer at brukere som har store mengder mottaksposter på tvers av mange butikker eller firmaer, og store lagerdokumenter, kan behandle disse dokumentene til et Commerce Headquarters uten å oppleve tidsavbrudd eller feil. Disse forbedringene krever at du bruker et asynkront dokumentrammeverk.

Når du bruker et asynkront dokumentrammeverk, kan du utføre innkommende dokumentendringer fra POS til Commerce Headquarters og deretter gå videre til andre oppgaver mens behandlingen til Commerce Headquarters forekommer i bakgrunnen. Du kan kontrollere statusen for et dokument ved hjelp av dokumentlistesiden **Innkommende operasjon** i POS for å sikre at posteringen var vellykket. I POS-programmet kan du også bruke listen over aktive dokumenter for innkommende operasjoner til å se dokumenter som ikke kunne posteres til Commerce Headquarters. Hvis et dokument mislykkes, kan POS-brukere gjøre endringer i det og deretter prøve å behandle det på nytt i Commerce Headquarters.

> [!IMPORTANT]
> Det asynkrone dokumentrammeverket må konfigureres før et firma prøver å bruke den innkommende operasjonen i POS.

Fullfør fremgangsmåten nedenfor for å konfigurere et asynkront dokumentrammeverk.

### <a name="create-and-configure-a-number-sequence"></a>Opprette og konfigurere en nummerserie

1. Gå til **Organisasjonsadministrasjon \> Nummerserier \> Nummerserier**.
2. På **Nummerserier**-siden oppretter du en nummerserie.
3. I feltene **Nummerseriekode** og **Navn** angir du brukerdefinerte verdier.
4. Velg **Legg til** på hurtigfanen **Referanser**.
5. I **Område**-feltet velger du **Handelsparametere**.
4. I **Referanse**-feltet velger du **Identifikator for Retail-dokumentoperasjon**.
5. På hurtigfanen **Generelt** i delen **Oppsett** setter du **Fortløpende** til **Nei** for å sørge for at det ikke blir noen ytelsesproblemer.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Opprette og planlegge to satsvise jobber for dokumentbehandling og overvåkingsoppgaver

> [!NOTE]
> I Commerce-versjon 10.0.13 og senere trenger du ikke å konfigurere disse satsvise jobbene via rammeverket for den satsvise jobben. Satsvise prosesser kan konfigureres fra **Detaljhandel og handel > IT for Detaljhandel og handel**-menyen. Bruk menyalternativene for **Overvåking av Retail-dokumentoperasjon** og **Behandling av Retail-dokumentoperasjon** til å konfigurere de satsvise jobbene.

De satsvise jobbene du oppretter, vil bli brukt til å behandle dokumenter som mislykkes eller blir tidsavbrutt. De vil også bli brukt når antallet aktive lagerdokumenter som behandles fra POS, overskrider en systemkonfigurert verdi.

1. Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**.
2. Opprett to satsvise jobber på siden **Satsvis jobb**:

    - Konfigurer den ene jobben for å kjøre **RetailDocumentOperationMonitorBatch**-klassen.
    - Konfigurer den andre jobben for å kjøre **RetailDocumentOperationProcessingBatch**-klassen.

2. Planlegg at nye satsvise jobber skal kjøres regelmessig. Du kan for eksempel angi tidsplanen slik at jobbene kjøres hvert femte minutt.

## <a name="prerequisite-add-inbound-operation-to-the-pos-screen-layout"></a>Forutsetning: Legg til innkommende operasjon i oppsett for POS-skjerm

Før organisasjonen kan bruke funksjonaliteten for innkommende operasjoner, må den konfigurere POS-operasjonen **Innkommende operasjon** på ett eller flere av [POS-skjermoppsettene](/dynamics365/unified-operations/retail/pos-screen-layouts). Før du distribuerer den nye operasjonen i et produksjonsmiljø, må du kontrollere at du tester den grundig og lære opp brukerne for å bruke den.

## <a name="overview"></a>Oversikt

Med den innkommende operasjonen POS-brukere utføre følgende oppgaver:

- Motta beholdning i butikklager fra enten bekreftede bestillingsdokumenter eller sendte overføringsordredokumenter.
- Vis informasjon om historiske lagermottak for en periode på sju dager etter at dokumentet er fullstendig mottatt.
- Opprett en ny inngående overføringsordreforespørsel.

Når den innkommende operasjonen startes fra POS-programmet, vises en listesidevisning. Denne visningen viser åpne bestillings- og overføringsordredokumenter som har lagerlinjer som er planlagt mottatt av den gjeldende butikken. For å finne og velge et bestemt dokument kan brukerne rulle opp listen eller bruke søkefunksjonen.

Listen for inngående lagerdokumenter har tre kategorier:

- **Aktiv** – Denne kategorien viser dokumenter som er helt eller delvis åpne, og som inneholder linjer eller antall på linjer som fortsatt må mottas.
- **Utkast** – Denne kategorien viser nye inngående overføringsordreforespørsler som butikken har opprettet. Dokumentene er imidlertid bare lagret lokalt. De er ennå ikke sendt til Commerce Headquarters for behandling.
- **Fullført** – Denne kategorien viser en liste over bestillinger eller overføringsordrer som butikken har fullstendig mottatt i løpet av de siste sju dagene. Denne kategorien er bare til informasjon. All informasjon om dokumentene er skrivebeskyttede data for butikken.

Når du viser dokumenter i en av kategoriene, kan **Status**-feltet hjelpe deg med å forstå stadiet som dokumentet er i.

- **Utkast** – Overføringsordredokumentet er bare lagret lokalt i butikkens kanaldatabase. Ingen informasjon om overføringsordreforespørselen er ennå sendt til Commerce Headquarters.
- **Forespurt** – Bestillingen eller overføringsordren er opprettet i Commerce Headquarters, og er helt åpen. Ingen mottak er ennå behandlet mot dokumentet. Når det gjelder dokumenter av typen bestilling, kan mottak begynne når som helst når statusen er **Forespurt**.
- **Delvis sendt** – Overføringsordredokumentet har én eller flere linjer eller delvise linjeantall som er postert som sendt av det utgående lageret. Disse sendte linjene kan mottas via den innkommende operasjonen.
- **Fullstendig levert** – Overføringsordren har hatt alle sine linjer og fulle linjeantall postert som sendt av det utgående lageret. Hele dokumentet kan mottas via den innkommende operasjonen.
- **Delvis mottatt** – Noen av linjene eller linjeantallene i bestillings- eller overføringsordredokumentet er mottatt av butikken, men noen linjer forblir åpne.
- **Fullstendig mottatt** – Alle linjer og antall i bestillings- eller overføringsordredokumentet er fullstendig mottatt. Dokumentene er bare tilgjengelige i kategorien **Fullstendig**, og er skrivebeskyttet av butikkbrukere.
- **Pågår** – Denne statusen brukes til å informere enhetsbrukere om at det arbeides aktivt på dokumentet av en annen bruker.
- **Midlertidig stanset** – Denne statusen vises etter at **Stans mottak midlertidig** er valgt for å stoppe mottaksprosessen midlertidig.
- **Behandling i HQ** – Dokumentet ble sendt til Commerce Headquarters fra POS-programmet, men det er ennå ikke postert til Commerce Headquarters. Dokumentet går gjennom den asynkrone dokumentposteringsprosessen. Når dokumentet er postert i Commerce Headquarters, skal statusen oppdateres til **Fullstendig mottatt** eller **Delvis mottatt**.
- **Behandling mislyktes** – Dokumentet ble postert til Commerce Headquarters og avvist. **Detaljer**-ruten viser årsaken til posteringsfeilen. Dokumentet må redigeres for å løse dataproblemer, og deretter må det sendes på nytt til Commerce Headquarters for behandling.

Når du velger en dokumentlinje i listen, vises en **Detaljer**-rute. Denne ruten viser tilleggsinformasjon om dokumentet, for eksempel informasjon om levering og dato. En fremdriftsindikator viser hvor mange varer som fortsatt må behandles. Hvis dokumentet ikke ble behandlet i Commerce Headquarters, viser **Detaljer**-ruten også feilmeldinger som er relatert til feilen.

I dokumentlistesidevisningen kan du velge **Ordredetaljer** på applinjen for å vise dokumentdetaljene. Du kan også aktivere mottaksbehandling på kvalifiserte dokumentlinjer.

I dokumentlistevisning kan du også opprette en ny forespørsel om innkommende overføringsordrer for en butikk. Dokumentene forblir i **Utkast**-status, og de kan justeres eller slettes til de sendes til Commerce Headquarters for behandling. Etter at de er sendt til Commerce Headquarters, kan overføringsordrelinjene ikke lenger endres fra POS-programmet.

## <a name="receiving-process"></a>Mottaksprosess

Når du har valgt et bestillings- eller et overføringsordredokument i kategorien **Aktiv**, kan du velge **Ordredetaljer** for å begynne mottaksprosessen.

Som standard vises visningen **Mottar nå**. Denne visningen er optimalisert for strekkodeskanning. Den kan brukes til å bygge en liste over varene som er skannet, slik at de varene kan mottas. Når du skal begynne mottaksprosessen, kan du begynne å skanne varestrekkoder.

Etter hvert som varestrekkoder skannes i visningen **Mottar nå**, validerer programmet varene mot det valgte bestillings- eller overføringsordredokumentet for å sikre at hver skannede vare samsvarer med en gyldig vare i dokumentet. I visningen **Mottark nå** brukes hver skanning av en strekkode til å representere mottaket av et antall på én enhet, med mindre et antall er innebygd i strekkoden. Du kan skanne strekkoder gjentatte ganger i denne visningen for å bygge en liste over alle varer og antallene for mottaket.

### <a name="example-scenario"></a>Eksempelscenario

En bruker mottar en bestilling som inneholder ti enheter av strekkode 5657900266. Brukeren kan skanne denne strekkoden ti ganger for å oppdatere feltet **Mottar nå** med én enhet per skanning. Når brukeren har fullført skanningene, viser feltet **Mottar nå** for varens linje at et antall på 10 ble mottatt.

I et scenario der vareantallet er stort, kan brukeren også foretrekke å angi antallet manuelt i stedet for å skanne strekkoden for hver vare som mottas. I dette tilfellet kan brukeren skanne strekkoden én gang for å legge til varen i listen **Mottar nå**. Brukeren kan deretter velge den tilknyttede linjen i visningen **Mottar nå** og kan deretter i **Detaljer**-ruten som vises til høyre på siden, oppdatere feltet **Mottaksantall** for varen.

Selv om visningen **Mottar nå** er optimalisert for strekkodeskanning, kan brukerne også velge **Motta produkt** på applinjen og deretter angi vare-ID-en eller strekkodedataene via en dialogboks. Når varen som ble lagt inn, er validert, blir brukeren bedt om å angi mottaksantallet.

Med visningen **Mottar nå** kan brukerne se hvilke produkter de mottar. Eventuelt kan visningen **Fullstendig ordreliste** brukes. Denne visningen viser hele listen over dokumentlinjer for det valgte bestillings- eller overføringsordredokumentet. Brukere kan manuelt velge linjer i listen og deretter gå til **Detaljer**-ruten og oppdatere feltet **Mottaksantall** for den valgte linjen. I visningen **Fullstendig ordreliste** kan brukere skanne strekkoder, eller de kan bruke funksjonen **Motta produkt** til å angi vare-ID-en eller strekkoden og data om det mottatte antallet uten først å måtte velge den tilsvarende varelinjen i listen.

### <a name="over-receiving-validations"></a>Valideringer av overmottak

Valideringer skjer under mottaksprosessen for dokumentlinjene. De omfatter valideringer for overlevering. Hvis en bruker prøver å motta mer beholdning enn det som ble bestilt på en bestilling, men enten overlevering ikke er konfigurert, eller hvis beløpet som er mottatt, overskrider den overleveringstoleransen som er konfigurert for bestillingslinjen, får brukeren en feil og ikke tillatt å motta det overflødige antallet.

Overmottak er ikke tillatt for overføringsordredokumenter. Brukere vil alltid motta feilmeldinger hvis de prøver å motta mer enn det som ble levert for overføringsordrelinjen.

### <a name="close-purchase-order-lines"></a>Lukke bestillingslinjer

Du kan lukke restantallet i en inn kommende bestilling i løpet av mottaksprosessen hvis speditøren har bekreftet at de ikke kan levere det fullstendige antallet som ble forespurt. Hvis du vil gjøre dette, må firmaet konfigureres til å tillate underlevering av bestillinger. I tillegg må en toleranseprosent for underlevering være definert for bestillingen.

Hvis du vil konfigurere firmaet slik at det tillater underlevering av bestillinger, kan du gå til **Innkjøp og leverandører** > **Konfigurer** > **Parametere for innkjøp og leverandører** i Commerce Headquarters. I kategorien **Levering** slår du på parameteren **Godta underlevering**. Kjør deretter distribusjonsplanjobben **1070** (**Kanalkonfigurasjon**) for å synkronisere endringene for innstillingene for kanalene.

Toleranseprosenter for underlevering for en bestillingslinje kan forhåndsdefineres for produkter som en del av produktkonfigurasjonene i Commerce Headquarters. De kan også angis eller overskrives på en bestemt bestilling i Commerce Headquarters.

Når en organisasjon har fullført konfigurasjon av underlevering for bestillingen, vil POS-brukerne se et nytt alternativ kalt **Lukk gjenværende antall** i ruten **Detaljer** når en innkommende bestillingslinje velges i operasjonen **Inngående lager**. Hvis brukeren lukker restantallet, utfører POS en validering for å kontrollere om antallet som lukkes, er innenfor toleransen for toleranseprosenten for underlevering som er definert på bestillingslinjen. Hvis toleransen for underlevering er overskredet vises det en feilmelding, og brukeren kan ikke lukke det gjenstående antallet før det tidligere mottatte antallet pluss antallet **Mottar nå**, oppfyller eller overgår minimumsantallet som må mottas, basert på toleranseprosenten for underlevering. 

Når **Lukk gjenværende antall** på en bestillingslinje er slått på og brukeren fullfører mottaket ved hjelp av handlingen **Fullfør mottak**, sendes en forespørsel om lukking til Commerce Headquarters, og antallet som ikke er mottatt for bestillingslinjen blir kansellert. På dette tidspunktet anses linjen som fullstendig mottatt. 

### <a name="receiving-location-controlled-items"></a>Motta lokasjonsstyrte varer

Hvis varene som blir mottatt, er lokasjonsstyrt, kan brukere velge lokasjonen der de vil motta varene under mottaksprosessen. Vi anbefaler at du konfigurerer en standard mottaksplassering for butikklageret, slik at denne prosessen blir mer effektiv. Selv om en standard lokasjon er konfigurert, kan brukere overstyre mottakslokasjonen på valgte linjer etter behov.

Operasjonen respekterer konfigurasjonen for **Tom tilgang tillatt** i lagringsdimensjonen **Sted** og krever ikke at en stedsdimensjon må angis hvis en tom tilgang konfigureres. Hvis det ikke er tillatt med tom tilgang for en vare, viser POS-programmet en feil og krever at det angis et sted før mottaket kan posteres.

### <a name="receive-all"></a>Motta alle

Etter behov kan du velge **Motta alle** på applinjen for raskt å oppdatere antallet **Mottar nå** for alle dokumentlinjene til maksimumsverdien som er tilgjengelig for mottak for disse linjene.

### <a name="receipt-of-unplanned-items-on-purchase-orders"></a>Mottak av ikke-planlagte varer på bestillinger

I Commerce versjon 10.0.14 og senere kan brukere motta et produkt som ikke opprinnelig var i bestillingen. Hvis du vil aktivere denne funksjonaliteten, aktiverer du valget for å **legge til linjer i bestillingen ved mottak til salgsstedet**.  

Denne funksjonen fungerer bare for bestillingsmottak. Det er ikke mulig å motta varer mot overføringsordrer når varene ikke tidligere ble bestilt og sendt fra det utgående lageret.

Brukere kan ikke legge til nye produkter i bestillingen under mottak til salgsstedet hvis [arbeidsflyt for endringsadministrasjon](../supply-chain/procurement/purchase-order-approval-confirmation.md) for bestillingen er aktivert i Commerce Headquarters. Hvis du vil aktivere endringsadministrasjon, må alle endringer i en bestilling først godkjennes før mottaket tillates. Fordi denne prosessen gjør det mulig for en mottaker å legge til nye linjer i bestillingen, vil mottak mislykkes hvis arbeidsflyt for endringsadministrasjon aktiveres. Hvis endringsadministrasjon aktiveres for alle bestillinger eller for leverandøren som er koblet til bestillingen som er aktiv på salgsstedet, kan ikke brukeren legge til nye produkter i bestillingen under mottak til salgsstedet.

Funksjonaliteten som gjør det mulig å legge til linjer, kan ikke brukes som en midlertidig løsning for å motta flere produktvolumer som allerede finnes i bestillingen. Overmottak styres gjennom standardinnstillinger for [overmottak](#over-receiving-validations) for produktlinjen på bestillingen.

Hvis valget for å **legge til linjer i bestillingen ved mottak til salgsstedet** er aktivert og en bruker mottar med **Innkommende operasjon** på salgsstedet, og hvis brukeren skanner eller taster en produktstrekkode eller et produktnummer som ikke gjenkjennes som en vare på gjeldende bestilling, men blir gjenkjent som en gyldig vare, mottar brukeren en melding om å legge til varen i bestillingen. Hvis brukeren legger til varen i bestillingen, regnes antallet som er angitt i **Mottar nå**, som det bestilte antallet for bestillingslinjen.

Når bestillingsmottaket er fullført og sendt til hovedkontoret for behandling, blir de tillagte linjene opprettet i hoveddokumentet for bestillingen. På bestillingslinjen i hovedkontoret vil det være et **Lagt til av salgssted**-flagg i kategorien **Generelt** på bestillingslinjen. Flagget **Lagt til av salgssted** angir at bestillingslinjen ble lagt til av mottaksprosessen for salgssted, at det ikke var en linje som var på bestillingen før mottak.

### <a name="cancel-receiving"></a>Avbryt mottak

Du bør bare bruke funksjonen **Avbryt mottak** på applinjen hvis du vil gå tilbake til dokumentet og ikke vil lagre endringer. Du har for eksempel opprinnelig valgt feil dokument og vil ikke at noen av de tidligere mottaksdataene skal lagres.

### <a name="pause-receiving"></a>Stopp mottak midlertidig

Hvis du mottar lagerbeholdningen, kan du bruke funksjonen **Stans mottak midlertidig** hvis du vil ta en pause fra mottaksprosessen. Det kan for eksempel hende at du vil utføre en annen operasjon fra salgsstedet, for eksempel å ringe opp et kundesalg eller forsinke postering av mottaket.

Når du velger **Stans mottak midlertidig**, endres dokumentstatusen til **Midlertidig stanset**. Derfor vil brukerne vite at det er lagt inn data i dokumentet, men dokumentet er ennå ikke utført. Når du er klar til å gjenoppta mottaksprosessen, velger du det stansede dokumentet, og deretter velger du **Ordredetaljer**. Alle antall i **Mottar nå** som tidligere ble lagret, beholdes og kan vises fra visningen **Fullstendig ordreliste**.

### <a name="review"></a>Se over

Før den endelige forpliktelsen av mottaket til Commerce Headquarters (HQ) kan du bruke funksjonen Gjennomgang til å validere det innkommende dokumentet. Denne gjennomgangen varsler deg om manglende eller uriktige data som kan føre til en behandlingsfeil, og gir deg muligheten til å rette opp problemer før du sender inn mottaksforespørselen. Hvis du vil aktivere funksjonen **Gjennomgang** på applinjen, aktiverer du funksjonen **Aktiver validering i innkommende og utgående lageroperasjoner på salgsstedet** via arbeidsområdet **Funksjonsbehandling** i Commerce Headquarters (HQ).

Funksjonen **Gjennomgang** validerer følgende problemer i et innkommende dokument:

- **Overmottak** – antallet som mottas nå, er større enn det bestilte antallet. Alvorsgraden til dette problemet bestemmes av overleveringskonfigurasjonen i Commerce Headquarters (HQ).
- **Undermottak** – antallet som mottas nå, er mindre enn det bestilte antallet. Alvorsgraden til dette problemet bestemmes av underleveringskonfigurasjonen i Commerce Headquarters (HQ).
- **Serienummer** – serienummer er ikke oppgitt eller validert for en serialisert vare som krever at et serienummer registreres på lageret.
- **Sted ikke angitt** – stedet er ikke angitt for en stedsstyrt vare der et tomt sted ikke er tillatt.
- **Slettede linjer** – ordren har linjer slettet av en Commerce Headquarters-bruker (HQ) som ikke er kjent for POS-appen.

Sett parameteren **Aktiver automatisk validering** til **Ja** i **Commerce-parametere** > **Lager** > **Butikklager**, for å få valideringen til å utføres automatisk når funksjonen **Fullfør mottak** velges.

### <a name="finish-receiving"></a>Slutt å motta

Når du er ferdig med å angi alle **Mottar nå**-antallene for produkter, må du velge **Fullfør mottak** på applinjen for å behandle mottaket.

Når brukere fullfører en bestillingskvittering, blir de bedt om å angi en verdi i feltet **Kvitteringsnummer** hvis denne funksjonaliteten er konfigurert. Denne verdien tilsvarer vanligvis ID-en på leverandørfølgeseddelen. **Kvitteringsnummer**-dataene blir lagret i produktkvitteringsjournalen i Commerce Headquarters. Kvitteringsnumre registreres ikke for overføringsordremottak.

Når det brukes asynkron dokumentbehandling, sendes mottaket via et asynkront dokumentrammeverk. Hvor lang tid det tar å postere dokumentet, avhenger av størrelsen på dokumentet (antall linjer) og den generelle behandlingstrafikken som skjer på serveren. Denne prosessen skjer vanligvis i løpet av sekunder. Hvis dokumentpostering mislykkes, blir brukeren varslet via dokumentlisten **Innkommende operasjon**, der dokumentstatusen vil bli oppdatert til **Behandling mislyktes**. Brukeren kan deretter velge det mislykkede dokumentet i POS for å vise feilmeldingene og årsaken til feilen i **Detaljer**-ruten. Et mislykket dokument forblir upostert og krever at brukeren går tilbake til dokumentlinjene ved å velge **Ordredetaljer** i POS. Brukeren må deretter oppdatere dokumentet med rettelser, basert på feilene. Når et dokument er rettet opp, kan brukeren prøve å behandle det på nytt ved å velge **Fullfør innfrielse** på applinjen.

## <a name="create-an-inbound-transfer-order"></a>Opprette en innkommende overføringsordre

Fra POS kan brukere opprette nye overføringsordredokumenter. Hvis du vil starte prosessen, velger du **Ny** på applinjen mens du er i hoveddokumentlisten **Innkommende operasjon**. Du blir deretter bedt om å velge et lager eller en butikk under **Overfør fra** som vil levere lageret til butikklokasjonen. Verdiene er begrenset til valget som er definert i konfigurasjonen av butikkens oppfyllingsgruppe. I en inngående overføringsforespørsel vil gjeldende butikk alltid være **Overfør til**-lageret for overføringsordren. Denne verdien kan ikke endres.

Du kan angi verdier i feltene **Forsendelsesdato**, **Mottaksdato** og **Leveringsmåte** etter behov. Du kan også legge til et notat som skal lagres sammen med overføringsordrehodet, som et vedlegg til dokumentet i Commerce Headquarters.

Når hodeinformasjonen er opprettet, kan du legge til produkter i overføringsordren. Hvis du vil starte prosessen med å legge til varer og forespurte antall, velger du **Legg til produkt**. I **Detaljer**-ruten kan du også legge til en linje spesifikk merknad for journallinjene. Disse merknadene vil bli lagret som et linjevedlegg.

Når linjer er angitt i den inngående overføringsordren, må du velge **Lagre** for å lagre dokumentendringene lokalt eller **Send forespørsel** for å sende inn ordredetaljene til Commerce Headquarters for videre behandling. Hvis du velger **Lagre**, lagres utkastdokumentet i kanaldatabasen, og utgående lager kan ikke kjøre dokumentet før det er behandlet via **Send forespørsel**. Du bør bare velge **Lagre** hvis du ikke er klar til å sende forespørselen til Commerce Headquarters for behandling.

Hvis et dokument lagres lokalt, finner du det i kategorien **Utkast** i dokumentlisten **Innkommende operasjon**. Mens et dokument er i **Utkast**-status, kan du redigere det ved å velge **Rediger**. Du kan oppdatere, legge til eller slette linjer etter behov. Du kan også slette hele dokumentet mens det er i **Utkast**-status ved å velge **Slett** i kategorien **Utkast**.

Når utkastdokumentet er sendt til et Commerce Headquarters, vises det i kategorien **Aktiv** med statusen **Forespurt**. På dette stadiet kan ikke brukere i den inngående butikken eller lageret lenger redigere det ønskede inngående overføringsordredokumentet. Bare brukere i utgående lager kan redigere dokumentet ved å velge **Utgående operasjon** i POS-programmet. Redigeringslåsen sikrer at ingen konflikter oppstår fordi en innkommende anmoder endrer overføringsordren samtidig som den utgående befrakten aktivt plukker og leverer ordren. Hvis det er nødvendig å foreta endringer fra den inngående butikken eller lageret etter at overføringsordren er sendt, skal den utgående speditøren kontaktes og bli bedt om å angi endringene.

Når dokumentet har statusen **Forespurt**, vises det i kategorien **Aktiv**. Det kan imidlertid ikke ennå mottas av den inngående butikken eller lageret. Når det utgående lageret har levert noen av eller alle overføringsordrene, kan den inngående butikken eller lageret postere mottak i POS. Når den utgående siden behandler overføringsordredokumentene, oppdateres statusen fra **Forespurt** til **Sendt** eller **Delvis sendt**. Når dokumentene har statusen **Sendt** eller **Delvis sendt**, kan den inngående butikken eller lageret postere mottak mot dem ved hjelp av mottaksprosessen for innkommende operasjoner.

## <a name="related-topics"></a>Relaterte emner

[Utgående lageroperasjon på salgsstedet](pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]