---
title: Definere ordreoppfyllelse for butikker
description: Dette emnet gir en oversikt over hvordan butikkordreoppfyllelse settes opp.
author: rubencdelgado
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5cdf7b2655f62b693a8f2bc137c690fbc43b16a7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796444"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Definere ordreoppfyllelse for butikker

[!include [banner](includes/banner.md)]

Mange forhandlere vil optimalisere ordreoppfyllelsen ved å la butikker oppfylle ordrer. Ordreoppfyllelse på butikknivå kan bidra til å forenkle scenarier med for store lagre for en bestemt butikk, eller det kan være nødvendig med hensyn til logistikk i tilfeller der en butikk har ekstra kapasitet eller befinner seg nærmere avstand for levering til kunden. For å løse dette behovet, er en enhetlig ordreoppfyllelsesoperasjon tilgjengelig på salgsstedet.

Ordrer for oppfyllelse i en bestemt butikk har butikkens lager angitt i overskriften eller på linjene i ordren.

Ordrefullføringen på salgsstedet gir et enkelt arbeidsområde på salgsstedet som kan brukes til å behandle ordrer. Dette omfatter alt fra å godta ordren, merke den som sendt eller starte butikkplukking.

## <a name="set-up-the-order-fulfillment-operation"></a>Konfigurere ordreoppfyllelsesoperasjonen

Ordreoppfyllelse [Operasjons-ID 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations) kan brukes til å få tilgang til arbeidsområdet for butikkordreoppfyllelse på salgsstedet.

Følg trinnene i [Legge til operasjonen i en knappegruppe](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) for å angi hvilken parameter du vil bruke når ordreoppfyllelse startes på salgsstedet. Som standard er **Alle ordrer** valgt når du har angitt ordeoppfyllelsesoperasjonene. Når operasjonen er konfigurert med denne parameteren, vises alle ordrelinjer for oppfyllelse i gjeldende butikk. Også **Ordrer som skal leveres** er tilgjengelig, som kan tilordnes til en knapp og brukes når brukeren bare ønsker å se ordrene som skal leveres fra butikken. Til slutt er det **Ordrer for plukking**. Når denne aktiveres på salgsstedet, vises bare ordrene som skal plukkes i butikken. De forskjellige parameterne kan tilordnes til forskjellige knapper for å gi brukeren en rekke måter å vise ordreoppfyllelse på.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Gi brukere tilgang til ordreoppfyllelse på salgsstedet

Ordreoppfyllelsesoperasjonen har ikke sin egen standard tillatelse, men i fremtiden vil brukerne kanskje trenge tillatelsen **Tillat henting av ordre** for å starte operasjonen fra salgsstedet.

En konfigurasjonsinnstilling er tilgjengelig for å finne ut om en ordrelinje må godtas manuelt fra salgsstedet, på butikknivået. Hvis dette konfigurasjonsalternativet ikke er angitt, godtas ordrelinjer som standard. Hvis dette konfigurasjonsalternativet er aktivert, må brukerne på salgsstedet ha tillatelsen **Tillat godkjenning av ordre** for å godta ordrer fra salgsstedet.

### <a name="enable-manual-order-acceptance"></a>Aktivere manuell ordregodkjenning

Som standard er ordrelinjer som er tilordnet til en butikk, merket som **Godkjent**. Dette betyr at det blir antatt at de oppfylles fra den tilordnede butikken og vil ikke være underlagt ytterligere tilordning. I noen tilfeller ønsker forhandlerne å godta ordrer manuelt før de kan oppfylles. Hvis for eksempel en butikk har få ansatte og ikke kan oppfylle ordrer, godtar butikksjefen bare så mange ordrer for behandling som de mener kan behandles på en bestemt dag. Før en ordre er godkjent, kan den tilordnes på nytt av back office til en annen butikk. Slik gir også ordregodkjenning en måte å angi at en ordre er bekreftet av en butikk og skal oppfylles.

Ordrelinjer for henting i butikk er merket som **Ventende** og er ikke underlagt godkjenning.

Hvis du vil slå på manuell godkjenning for ordrelinjer, går du til **Retail og Commerce** \> **Kanaler** \> **Butikker** \> **Alle butikker**. Velg butikken, og klikk i butikk-ID-en for å vise detaljer for butikken. Klikk **Rediger**. På **Generelt**-hurtigkategorien finner du **Ordreoppfyllelse**-underoverskriften og endrer **Godta manuelt** fra **Nei** til **Ja**.

### <a name="enable-reject-order-line-capability"></a>Aktivere funksjonen for ordrelinjeavvisning

Ordrelinjer kan også avvises fra salgsstedet. Avvisning av en ordrelinje betyr at den ikke blir oppfylt i butikken og sender ordrelinjen tilbake for ny tilordning til en annen butikk eller lager. Tillatelsen for ordrelinjeavvisning gis via **Tillat ordreavvisning**-tillatelsen i tillatelsesgruppen for salgssted som er knyttet til arbeideren. Mens de avviser en linje, kan forhandlerne kreve at de ansatte gir en grunn for avvisningen. Dette kan gjøres ved hjelp av infokoder av **Aktivitet for informasjonskode**-typen **Ordreoppfyllelse** og tilordne informasjonskoden til **Avvis ordrelinje** i funksjonalitetsprofilen tilknyttet kanalen.

> [!NOTE]
> Bare informasjonskoder av **Aktivitet for informasjonskode**-typen **Ordreoppfyllelse** kan tilordnes til **Avvis ordrelinje**-handlingen.

### <a name="synchronize-changes-to-the-channel-database"></a>Synkronisere endringer til kanaldatabasen

Etter at operasjonen er tilordnet til en knappegruppe, de riktige tillatelsene er tilordnet og kanalen er konfigurert, må endringene synkroniseres til kanaldatabasen. Dette gjør du ved å gå til **Retail og Commerce** \> **IT for Retail og Commerce** \> **Distribusjonsplan**. Velg plan "1090, Kasser" for å synkronisere knappegruppeendringene, og klikk deretter **Kjør nå**. Synkroniser så tillatelsesendringer ved å velge "1060, Stab", og klikk deretter **Kjør nå**. Synkroniser så kanalendringer ved å velge "1070, Kanalkonfigurasjon", og klikk deretter **Kjør nå**. Synkroniser til slutt den nylig opprettede informasjonskoden for avvisningsårsak ved å velge "1110, Global konfigurasjon" og klikk **Kjør nå**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Bruke ordreoppfyllelse på salgsstedet

Åpne salgsstedet og velg ordreoppfyllelsesoperasjonen. Avhengig av hvordan det er konfigurert, er alle linjer, ordrelinjer for plukking eller ordrelinjer for forsendelse angitt.

### <a name="order-fulfillment-view"></a>Ordreoppfyllelsesvisningen

Ordreoppfyllelsesvisningen angir ordrelinjen for oppfyllelse i butikken, og omfatter følgende kolonner:

- Ordrenummer
- Produktnummer
- beskrivelse
- Bestilt antall
- Ønsket leveringsdato
- Kundenavn
- Oppfyllelsesstatus

Ytterligere informasjon for en bestemt ordrelinje kan vises ved å velge ordrelinjen og deretter åpne undermenyen rett under den påloggede brukeren / skiftinformasjonen som vises i salgsstedshodet. Denne menyen inneholder 2 kategorier: én for linjedetaljer og én for ordredetaljer. Kategorien for linjedetaljer inneholder følgende informasjon:

- Bestilt antall
- Restantallet som skal leveres/plukkes
- Plukket antall
- Pakket antall
- Fakturert antall (allerede plukket eller sendt)
- Leveringsmåte
- Leveringsadresse

Detaljer-undermenyen har også en kategori som gir flere ordrenivådetaljer, blant annet:

- Kundenavn
- Kunde-ID
- Ordrenummer
- Ordretotal
- Ordresaldo

Nederst i ordreoppfyllelsesvisningen er en handlingsrute. Den viser alle handlingene som kan utføres mot en ordrelinje. Hvis en handling ikke er tilgjengelig basert på linjens status, blir denne handlingen utilgjengelig.

Som standard vil ordrer ha statusen **Godkjent**. Ordrestatusen kan vises som en kolonne i listen over ordrelinjer. Hvis **Godta manuelt** er konfigurert på kanalnivå, vises alle linjer som skal sendes, som **Ventende** og må godkjennes før de kan bli oppfylt. Ordrer for butikkhenting er **Ventende** som standard og trenger ikke å bli godkjent.

### <a name="order-fulfillment-line-actions"></a>Handlinger for ordreoppfyllelseslinjer

- **Rediger** – Hvis en ordrestatus er venter, kan den bare redigeres på salgsstedet. Ordrer som allerede er delvis plukket, pakket eller fakturert, kan ikke redigeres fra ordreoppfyllelsesvisningen.
- **Godta** – Hvis **Godta manuelt** er konfigurert på kanalnivået, må linjer først godkjennes før de kan gå gjennom ordrefullføringsprosessen.
- **Velg** – Plukkalternativet støtter flere handlinger. **Plukking** oppdaterer statusen for ordrelinjen, slik at andre i butikken ikke prøver å plukke den samme linjen. **Skriv ut plukkliste** skriver ut en plukkliste for den valgte linjen eller linjene og oppdaterer statusen til **Plukking**. Plukklisteformater styres som en del av kvitteringsformater. Hvis du vil ha mer informasjon om hvordan du konfigurerer kvitteringsformater, kan du se [Kvitteringsmaler og utskrift](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Til slutt **Merk som plukket** indikerer at linjen er plukket. **Merk som plukket** starter tilsvarende lagertransaksjoner i back office. Valg av handlinger kan utføres samtidig for flere ordrelinjer på tvers av ordrer og for alle leveringsmåter.
- **Avvis** – Linjer eller delvise linjer kan avvises. Dette gjør at de kan tildeles på nytt fra back office til en annen butikk eller annet lager. Linjene kan bare avvises hvis de ennå ikke er plukket eller pakket. Hvis du vil avvise en linje som allerede er plukket eller pakket, må linjen være uplukket eller upakket fra back office.
- **Pakke** – Pakkealternativet støtter to handlinger: **Skriv ut følgeseddel** skriver ut en følgeseddel for de valgte linjene, og **Merk som pakket** vil merke linjene som pakket og merke linjene som levert i back office. Bare ordrelinjer som tilhører den samme ordren og har samme leveringsmåte kan pakkes samtidig. Følgeseddelformater styres som en del av kvitteringsformater. Hvis du vil ha mer informasjon om hvordan du konfigurerer kvitteringsformater, kan du se [Kvitteringsmaler og utskrift](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Send** – Forsendelseshandlingen markerer valgte linjer som **Levert** i back office. Når en linje er fullstendig levert, vises den ikke lenger i ordreoppfyllelsesvisningen.
- **Plukk** – Plukkhandlingen legger til linjene i transaksjonsvisningen for plukking. Hvis det finnes andre linjer i ordren som for øyeblikket ikke blir plukket, legges de til i transaksjonsvisningen med antall null. Når en linje er fullstendig plukket, vises den ikke lenger i ordreoppfyllelsesvisningen.

### <a name="order-fulfillment-filtering"></a>Ordreoppfyllelsesfiltrering

Ordreoppfyllelse på salgsstedet omfatter filtrering for å hjelpe brukeren med enkelt å finne det de trenger. Filtre kan endres i handlingsruten nederst på **Salgssted**-skjermen. Som standard brukes et **Leveringstype**-filter, basert på hvordan operasjonen er konfigurert. Hvis operasjonen er definert med **Alle ordrer**-parameteren, vil dette filteret brukes når du åpner ordreoppfyllelse. Det samme gjelder **Henting i butikk**- og **Send fra butikk**-parameteren. Andre filtre som kan brukes på ordreoppfyllelsesvisningen, omfatter:

- Kundenummer
- Kundenavn
- Kundens e-postadresse
- Ordrenummer
- Leveringsmåte
- Kvitteringsnummer
- Kanalreferanse-ID
- Opprinnelig butikknummer
- Linjestatus
- Opprettet dato
- Leveringsdato
- Mottaksdato


[!INCLUDE[footer-include](../includes/footer-banner.md)]
