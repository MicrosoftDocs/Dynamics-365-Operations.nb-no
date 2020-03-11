---
title: Utgående lageroperasjon på salgsstedet
description: Dette emnet beskriver funksjonene til utgående lageroperasjoner på salgsstedet (POS).
author: hhaines
manager: annbe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c3e50d20162340c599fb6719ae6f45654dba990a
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071885"
---
# <a name="outbound-inventory-operation-in-pos"></a>Utgående lageroperasjon på salgsstedet

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

I Microsoft Dynamics 365 Commerce versjon 10.0.10 og senere erstatter innkommende og utgående operasjoner på salgsstedet (POS) den plukkede og mottatte operasjonen.

> [!NOTE]
> I versjon 10.0.10 og senere legges eventuelle nye funksjoner i POS-programmet som er relatert til mottak av butikklager mot bestillinger og overførings ordrer, til innkommende operasjoner. Hvis du for øyeblikket bruker en plukk- og mottaksoperasjon i POS, anbefaler vi at du utvikler en strategi for flytting fra den operasjonen til de nye innkommende og utgående operasjonene. Selv om plukk- og mottaksoperasjonen ikke blir fjernet fra produktet, vil det ikke være flere investeringer i den, fra et funksjonelt eller ytelsesperspektiv etter versjon 10.0.9.

## <a name="prerequisite-configure-an-asynchronous-document-framework"></a>Forutsetning: konfigurere et asynkront dokumentrammeverk

Den utgående operasjonen omfatter ytelsesforbedringer som sikrer at brukere som har store mengder mottaksposter på tvers av mange butikker eller firmaer, og store lagerdokumenter, kan behandle disse dokumentene til et Commerce Headquarters uten å oppleve tidsavbrudd eller feil. Disse forbedringene krever at du bruker et asynkront dokumentrammeverk.

Når du bruker et asynkront dokumentrammeverk, kan du utføre utgående dokumentendringer fra POS til Commerce Headquarters og deretter gå videre til andre oppgaver mens behandlingen til Commerce Headquarters forekommer i bakgrunnen. Du kan kontrollere statusen for et dokument ved hjelp av dokumentlistesiden **Utgående operasjon** i POS for å sikre at posteringen var vellykket. I POS-programmet kan du også bruke listen over aktive dokumenter for utgående operasjoner til å se dokumenter som ikke kunne posteres til Commerce Headquarters. Hvis et dokument mislykkes, kan POS-brukere gjøre endringer i det og deretter prøve å behandle det på nytt i Commerce Headquarters.

> [!IMPORTANT]
> Det asynkrone dokumentrammeverket må konfigureres før et firma prøver å bruke den utgående operasjonen i POS.

Fullfør fremgangsmåten nedenfor for å konfigurere et asynkront dokumentrammeverk.

### <a name="create-and-configure-a-number-sequence"></a>Opprette og konfigurere en nummerserie

1. Gå til **Organisasjonsadministrasjon \> Nummerserier \> Nummerserier**.
2. På **Nummerserier**-siden oppretter du en nummerserie.
3. I feltene **Nummerseriekode** og **Navn** angir du brukerdefinerte verdier.
4. Velg **Legg til** på hurtigfanen **Referanser**.
5. I **Område**-feltet velger du **Handelsparametere**.
6. I **Referanse**-feltet velger du **Identifikator for Retail-dokumentoperasjon**.
7. På hurtigfanen **Generelt** i delen **Oppsett** setter du **Fortløpende** til **Nei** for å sørge for at det ikke blir noen ytelsesproblemer.

### <a name="create-and-schedule-two-batch-jobs-for-the-document-processing-and-monitoring-tasks"></a>Opprette og planlegge to satsvise jobber for dokumentbehandling og overvåkingsoppgaver

De satsvise jobbene du oppretter, vil bli brukt til å behandle dokumenter som mislykkes eller blir tidsavbrutt. De vil også bli brukt når antallet aktive lagerdokumenter som behandles fra POS, overskrider en systemkonfigurert verdi.

1. Gå til **Systemadministrasjon \> Forespørsler \> Satsvise jobber**.
2. Opprett to satsvise jobber på siden **Satsvis jobb**:

    - Konfigurer den ene jobben for å kjøre **RetailDocumentOperationMonitorBatch**-klassen.
    - Konfigurer den andre jobben for å kjøre **RetailDocumentOperationProcessingBatch**-klassen.

3. Planlegg at nye satsvise jobber skal kjøres regelmessig. Du kan for eksempel angi tidsplanen slik at jobbene kjøres hvert femte minutt.

## <a name="prerequisite-add-outbound-operation-to-the-pos-screen-layout"></a>Forutsetning: Legg til utgående operasjon i oppsett for POS-skjerm

Før organisasjonen kan bruke funksjonaliteten for utgående operasjoner, må den konfigurere POS-operasjonen **Utgående operasjon** på ett eller flere av [POS-skjermoppsettene](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts). Før du distribuerer den nye operasjonen i et produksjonsmiljø, må du kontrollere at du tester den grundig og lære opp brukerne for å bruke den.

## <a name="overview"></a>Oversikt

Med den utgående operasjonen kan POS-brukere utføre følgende oppgaver:

- Poster forsendelser for overføringsordredokumenter i tilfeller der brukerens butikk er det angitte utgående lageret.
- Vis informasjon om historiske overføringsordreforsendelser som ble postert av butikken.
- Opprett en ny utgående overføringsordreforespørsel.

Når den utgående operasjonen startes fra POS-programmet, vises en listesidevisning. Denne visningen viser åpne bestillings- og overføringsordredokumenter som har lagerlinjer som brukerens gjeldende butikk har planlagt å sende og innfri. For å finne og velge et dokument kan brukerne rulle opp listen eller bruke søkefunksjonen.

Listen for utgående lagerdokumenter har tre kategorier:

- **Aktiv** – Denne kategorien viser overføringsordrer med statusen **Forespurt** eller **Delvis sendt**. Ordrene inneholder linjer eller antall på linjer som må leveres av brukerens gjeldende butikk. Denne kategorien viser også ordrer som har statusen **Behandling i HQ** (det vil si at de venter på bekreftelse av vellykket postering fra Commerce Headquarters) eller **Behandling mislyktes** (det vil si at postering til Commerce Headquarters mislyktes, og brukeren må korrigere dataene og prvøe å sende ordrene på nytt).
- **Utkast** – Denne kategorien viser nye utgående overføringsordreforespørsler som brukerens butikk har opprettet. Dokumentene er imidlertid bare lagret lokalt. De er ennå ikke sendt til Commerce Headquarters for behandling.
- **Fullført** – Denne kategorien viser en liste over overføringsordredokumenter som butikken har fullstendig sendt i løpet av de siste sju dagene. Denne kategorien er bare til informasjon. All informasjon om dokumentene er skrivebeskyttede data for butikken.

Når du viser dokumenter i en av kategoriene, kan **Status**-feltet hjelpe deg med å forstå stadiet som dokumentet er i.

- **Utkast** – Overføringsordredokumentet er bare lagret lokalt i butikkens kanaldatabase. Ingen informasjon om overføringsordreforespørselen er ennå sendt til Commerce Headquarters.
- **Forespurt** – Bestillingen eller overføringsordren er opprettet i Commerce Headquarters, og er helt åpen. Brukerens gjeldende butikk har ennå behandlet eventuelle forsendelser mot dokumentet.
- **Delvis sendt** – Overføringsordredokumentet har én eller flere linjer eller delvise linjeantall som er postert som sendt av det utgående lageret. Disse sendte linjene kan mottas via den innkommende operasjonen.
- **Fullstendig levert** – Overføringsordren har hatt alle sine linjer og fulle linjeantall postert som sendt av det utgående lageret.
- **Pågår** – Denne statusen brukes til å informere enhetsbrukere om at det arbeides aktivt på dokumentet av en annen bruker.
- **Midlertidig stanset** – Denne statusen vises etter at **Stans mottak midlertidig** er valgt for å stoppe mottaksprosessen midlertidig.
- **Behandling i HQ** – Dokumentet ble sendt til Commerce Headquarters fra POS-programmet, men det er ennå ikke postert til Commerce Headquarters. Dokumentet går gjennom den asynkrone dokumentposteringsprosessen. Når dokumentet er postert i Commerce Headquarters, skal statusen oppdateres til **Fullstendig mottatt** eller **Delvis mottatt**.
- **Behandling mislyktes** – Dokumentet ble postert til Commerce Headquarters og avvist. **Detaljer**-ruten viser årsaken til posteringsfeilen. Dokumentet må redigeres for å løse dataproblemer, og deretter må det sendes på nytt til Commerce Headquarters for behandling.

Når du velger en dokumentlinje i listen, vises en **Detaljer**-rute. Denne ruten viser tilleggsinformasjon om dokumentet, for eksempel informasjon om levering og dato. En fremdriftsindikator viser hvor mange varer som fortsatt må behandles. Hvis dokumentet ikke ble behandlet i Commerce Headquarters, viser **Detaljer**-ruten også feilmeldinger som er relatert til feilen.

I dokumentlistesidevisningen kan du velge **Ordredetaljer** på applinjen for å vise dokumentdetaljene. Du kan også aktivere mottaksbehandling på kvalifiserte dokumentlinjer.

I dokumentlistevisning kan du også opprette en ny utgående overføringsordre for en butikk.

## <a name="transfer-order-shipping-process"></a>Sendeprosess for overføringsordre

Når du har valgt et overføringsordredokument i kategorien **Aktiv**, kan du velge **Ordredetaljer** for å begynne innfrielsesprosessen. Visningen **Fullstendig ordreliste** vises. Denne siden viser alle dokumentlinjene som inneholder varen. Den viser også detaljer om det bestilte antallet.

Hver skanning av en strekkode oppdaterer antallet i feltet **Leveres nå** med én enhet. Alternativt kan du angi et forsendelsesantall ved å velge **Send produkt** på applinjen, angi en vare-ID og deretter angi antallet. Hvis varen er lokasjonskontrollert, kan du bekrefte eller angi forsendelseslokasjonen for dokumentlinjen.

I visningen **Fullstendig ordreliste** kan du manuelt velge en linje i listen og deretter oppdatere antallet i **Leveres nå** for den valgte linjen i **Detaljer**-ruten.

### <a name="over-delivery-shipping-validations"></a>Valideringer av overleveringsforsendelser

Valideringer skjer under mottaksprosessen for dokumentlinjene. De omfatter valideringer for overlevering. Hvis en bruker prøver å motta mer beholdning enn det som ble bestilt på en bestilling, men enten overlevering ikke er konfigurert, eller hvis antallet som er mottatt, overskrider den overleveringstoleransen som er konfigurert for bestillingslinjen, får brukeren en feil og ikke tillatt å motta det overflødige antallet.

### <a name="shipping-location-controlled-items"></a>Sende lokasjonsstyrte varer

Hvis varene som sendes, er lokasjonsstyrt, kan brukere velge lokasjonen der de vil levere beholdningen under forsendelsesprosessen. Vi anbefaler at du konfigurerer en standard utsendelsesplassering for butikklageret, slik at denne prosessen blir mer effektiv. Selv om en standard lokasjon er konfigurert, kan brukere overstyre utsendelseslokasjonen på valgte linjer etter behov.

Operasjonen respekterer konfigurasjonen for **Tom tilgang tillatt** i lagringsdimensjonen **Sted** og krever ikke at en stedsdimensjon må angis hvis en tom tilgang konfigureres. Hvis det ikke er tillatt med tom tilgang for en vare, viser POS-programmet en feil og krever at det angis et sted før mottaket kan posteres.

### <a name="ship-all"></a>Send alle

Etter behov kan du velge **Lever alle** på applinjen for raskt å oppdatere antallet **Leveres nå** for alle dokumentlinjene til maksimumsverdien som er tilgjengelig for innfrielse for disse linjene.

### <a name="cancel-fulfillment"></a>Avbryt oppfyllelse

Du bør bare bruke funksjonen **Avbryt innfrielse** på applinjen hvis du vil gå tilbake til dokumentet og ikke vil lagre endringer. Du har for eksempel opprinnelig valgt feil dokument og vil ikke at noen av de tidligere sendingsdataene skal lagres.

### <a name="pause-fulfillment"></a>Stopp oppfyllelse midlertidig

Hvis du innfrir overføringsordren, kan du bruke funksjonen **Stans innfrielse midlertidig** hvis du vil ta en pause fra prosessen. Det kan for eksempel hende at du vil utføre en annen operasjon fra salgsstedet, for eksempel å ringe opp et kundesalg eller forsinke postering av forsendelsen til Commerce Headquarters.

Når du velger **Stans innfrielse midlertidig**, endres dokumentstatusen til **Midlertidig stanset**. Derfor vil brukerne vite at det er lagt inn data i dokumentet, men dokumentet er ennå ikke utført. Når du er klar til å gjenoppta innfrielsesprosessen, velger du det stansede dokumentet, og deretter velger du **Ordredetaljer**. Alle antall i **Leverer nå** som tidligere ble lagret, beholdes og kan vises fra visningen **Fullstendig ordreliste**.

### <a name="finish-fulfillment"></a>Fullfør oppfyllelse

Når du er ferdig med å angi alle **Leveres nå**-antallene for produkter, må du velge **Fullfør innfrielse** på applinjen for å behandle mottaket.

Når det brukes asynkron dokumentbehandling, sendes mottaket via et asynkront dokumentrammeverk. Hvor lang tid det tar å postere dokumentet, avhenger av størrelsen på dokumentet (antall linjer) og den generelle behandlingstrafikken som skjer på serveren. Denne prosessen skjer vanligvis i løpet av sekunder. Hvis dokumentpostering mislykkes, blir brukeren varslet via dokumentlisten **Utgående operasjon** i kategorien **Aktiv**, der dokumentstatusen vil bli oppdatert til **Behandling mislyktes**. Brukeren kan deretter velge det mislykkede dokumentet i POS for å vise feilmeldingene og årsaken til feilen i **Detaljer**-ruten. Et mislykket dokument forblir upostert og krever at brukeren går tilbake til dokumentlinjene ved å velge **Ordredetaljer** i POS. Brukeren må deretter oppdatere dokumentet med rettelser, basert på feilene. Når et dokument er rettet opp, kan brukeren prøve å behandle det på nytt ved å velge **Fullfør innfrielse** på applinjen.

## <a name="create-an-outbound-transfer-order"></a>Opprette en utgående overføringsordre

Fra POS kan brukere opprette nye overføringsordredokumenter. Hvis du vil starte prosessen, velger du **Ny** på applinjen mens du er i hoveddokumentlisten **Utgående operasjon**. Du blir deretter bedt om å velge et lager eller en butikk under **Overfør til** som det gjeldende lageret skal sende beholdningen til. Verdiene er begrenset til valget som er definert i konfigurasjonen av butikkens oppfyllingsgruppe. I en utgående overføringsforespørsel vil gjeldende butikk alltid være **Overfør fra**-lageret for overføringsordren. Denne verdien kan ikke endres.

Du kan angi verdier i feltene **Forsendelsesdato**, **Mottaksdato** og **Leveringsmåte** etter behov. Du kan også legge til et notat som skal lagres sammen med overføringsordrehodet, som et vedlegg til dokumentet i Commerce Headquarters.

Når hodeinformasjonen er opprettet, kan du legge til produkter i overføringsordren. Hvis du vil starte prosessen med å legge til varer og forespurte antall, kan du skanne strekkoder eller velge **Legg til produkt**.

Når linjer er angitt i den utgående overføringsordren, må du velge **Lagre** for å lagre dokumentendringene lokalt eller **Send forespørsel** for å sende inn ordredetaljene til Commerce Headquarters for videre behandling. Hvis du velger **Lagre**, lagres utkastdokumentet i kanaldatabasen, og utgående lager kan ikke kjøre dokumentet før det er behandlet via **Send forespørsel**. Du bør bare velge **Lagre** hvis du ikke er klar til å sende forespørselen til Commerce Headquarters for behandling.

Hvis et dokument lagres lokalt, finner du det i kategorien **Utkast** i dokumentlisten **Innkommende operasjon**. Mens et dokument er i **Utkast**-status, kan du redigere det ved å velge **Rediger**. Du kan oppdatere, legge til eller slette linjer etter behov. Du kan også slette hele dokumentet mens det er i **Utkast**-status ved å velge **Slett** i kategorien **Utkast**.

Når utkastdokumentet er sendt til et Commerce Headquarters, vises det i kategorien **Aktiv** med statusen **Forespurt**. På dette punktet kan bare brukere i utgående lager redigere dokumentet ved å velge **Utgående operasjon** i POS-programmet. Brukere i inngående lager kan vise overføringsordren i kategorien **Aktiv** i dokumentlisten **Innkommende operasjon**, men de kan ikke redigere eller slette den. Redigeringslåsen sikrer at ingen konflikter oppstår fordi en innkommende anmoder endrer overføringsordren samtidig som den utgående befrakten aktivt plukker og leverer ordren. Hvis det er nødvendig å foreta endringer fra den inngående butikken eller lageret etter at overføringsordren er sendt, skal den utgående speditøren kontaktes og bli bedt om å angi endringene.

Når dokumentet har statusen **Forespurt**, er det klart for innfrielse av det utgående lageret. Etter hvert som forsendelsen behandles ved hjelp av den utgående operasjonen, oppdateres statusen til overføringsordredokumentene fra **Forespurt** til **Fullstendig levert** eller **Delvis levert**. Når dokumentene har statusen **Fullstendig levert** eller **Delvis levert**, kan den inngående butikken eller lageret postere mottak mot dem ved hjelp av mottaksprosessen for innkommende operasjoner.

Fullstendig sendte overføringsordrer flyttes til kategorien **Fullstendig** i dokumentlisten **Utgående operasjon**. Der forblir de synlige for brukerne i den utgående butikken eller lageret i skrivebeskyttet modus i sju dager.

## <a name="related-topics"></a>Relaterte emner

[Inngående lageroperasjon på salgsstedet](pos-inbound-inventory-operation.md)
