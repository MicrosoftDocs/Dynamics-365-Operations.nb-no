---
title: Tilkoblede og frakoblede salgsstedsoperasjoner (POS)
description: Dette emnet inneholder informasjon om salgsstedsoperasjoner i Microsoft Dynamics 365 for Retail. Den angir hvor i programmet operasjonene kan startes, og om de er tilgjengelige i frakoblet modus.
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44a2ec48f868c803c80c8df8eb809bc2254e63da
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505102"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Tilkoblede og frakoblede salgsstedsoperasjoner (POS)

[!include [banner](includes/banner.md)]

De fleste handlinger som brukere utfører på salgsstedet (POS) anses som operasjoner. Operasjoner konfigureres og behandles i back office for Microsoft Dynamics 365 for Retail. Mange operasjoner kan legges til for knapper i POS-knappegruppen. Brukere kan deretter velge knappene for å aktivere operasjonene og utføre arbeidet. Andre operasjoner er en del av det primære POS-programmet, og startes fra knappene på skjermen eller som en del av andre arbeidsflyter eller prosesser.

Tabellen nedenfor gir informasjon om operasjonene som er tilgjengelige i Retail Modern POS og Cloud POS for Dynamics 365 for Retail. Tabellen angir også hvor i programmet operasjonene kan startes, og om de er tilgjengelige når POS er i frakoblet modus.

Enkelte operasjoner er ikke tilgjengelige i Retail Modern POS eller Cloud POS for Dynamics 365 for Retail. Noen av disse operasjonene kan være landsspesifikke operasjoner som krever ekstra tillegg og konfigurasjon. Andre er funksjoner fra Microsoft Dynamics AX 2012 som ikke støttes for øyeblikket.

Følgende kolonner angir hvor operasjonene kan startes:

- **Knappegruppe** – Operasjonen kan tilordnes til knapper i POS-knappegrupper, som er en del av et POS-skjermoppsett.
- **Transaksjonsskjerm** – Operasjonen kan startes fra POS-knappegrupper som er konfigurert på POS-transaksjonsskjermen.
- **Velkomstskjerm** – Operasjonen kan startes fra POS-knappegrupper som er konfigurert på POS-velkomstskjermen.

> [!NOTE]
> Operasjonene nedenfor gjelder for den nyeste versjonen av Dynamics 365 for Retail. Noen operasjoner kan ha blitt endret eller er kanskje ikke tilgjengelig i tidligere versjoner.

| ID | Operasjon | beskrivelse | Knappegruppe | Transaksjonskjermbilde | Velkomstskjermbilde | Tilgjengelig frakoblet | Spesifikk for nasjonal innstilling |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktiver enhet | Aktiver gjeldende enhet ved å tillate at en godkjent bruker angir tilkoblingsinformasjon og tilordner en enhet og kasse-ID. | Antall | Antall | Antall | Antall | Antall |
| 134 | Legg til tilknytning | Legg til en forhåndsvalgt tilknytning i en transaksjon. Velg tilknytningen på siden **Knappeegenskaper**. | Ja | Ja | Antall | Ja | Antall |
| 135 | Legg til tilknytning fra en liste | Legg til en tilknytning til en transaksjon ved å velge den i en liste. | Ja | Ja | Ja | Ja | Antall |
| 137 | Legge til en tilknytning for en kunde | Du kan legge til en tilknytning til en kunde på siden **Kundedetaljer**. | Antall | Antall | Antall | Ja | Antall |
| 138 | Fjerne tilknytning fra kunde | Du kan fjerne en tilknytning på siden **Kundedetaljer**. | Antall | Antall | Antall | Ja | Antall |
| 643 | Legg til kupongkode | Legg til en kupong ved å angi koden i POS. | Ja | Ja | Antall | Ja | Antall |
| 117 | Legg til fordelskort | Be brukeren om å angi et fordelskortnummer som skal legges til den gjeldende transaksjonen. | Ja | Ja | Antall | Ja | Antall |
| 136 | Legg til serienummer | Denne operasjonen lar brukeren angi et serienummer for det valgte produktet. | Ja | Ja | Antall | Ja | Antall |
| 1214 | Legg til leveringsadresse | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 519 | Legg til i gavekort | Legg til penger på det angitte gavekortet. | Ja | Ja | Antall | Antall | Antall |
| 6000 | Tillat å hoppe over bilagsregistrering | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 1212 | Deponer til bank | Registrer pengebeløpet som sendes til banken, og annen informasjon som for eksempel bankposenummeret. | Ja | Ja | Ja | Ja | Antall |
| 923 | Kontroll av banktotaler | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 915 | Tom operasjon | Denne operasjonen representerer en knapp som kan tilpasses og programmeres av en programvareutvikler til enhver operasjon som virksomheten trenger. | Ja | Ja | Ja | Ja | Antall |
| 1053 | Lukk skift usporet | Sett gjeldende skift til lukket usporet, og logg brukeren av. Et usporet skift lukkes for flere transaksjoner, men er fortsatt åpen for kasseoperasjoner, for eksempel fjerning av betalingsmidler og kasseoppgjør. | Ja | Ja | Ja | Antall | Antall |
| 310 | Beregn total | Når rabattberegning er forsinket, starter denne operasjonen beregningen for gjeldende transaksjon. | Ja | Ja | Antall | Ja | Antall |
| 642 | Utfør alle produkter | Sett leveringsmåten for alle linjer til **Utlevering**. | Ja | Ja | Antall | Ja\* | Antall |
| 641 | Utfør valgte produkter | Sett leveringsmåten for de valgte linjene til **Utlevering**. | Ja | Ja | Antall | Ja\* | Antall |
| 1215 | Endre passord | Denne operasjonen lar POS-brukeren endre passordet. | Ja | Ja | Ja | Antall | Antall |
| 123 | Endre måleenhet | Endre måleenheten for det valgte linjeelementet. | Ja | Ja | Antall | Ja | Antall |
| 639 | Fjern standard selger i transaksjon | Fjerne provisjonssalgsgruppen (selger) fra transaksjonen. | Ja | Ja | Antall | Ja | Antall |
| 106 | Fjern antall | Tilbakestill antallet på den valgte linjen til **1**. | Ja | Ja | Antall | Ja | Antall |
| 640 | Fjern selger på linje | Fjern provisjonssalgsgruppen (selger) fra den valgte linjen. | Ja | Ja | Antall | Ja | Antall |
| 121 | Fjern selger | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 1055 | Lukk skift | Avslutt gjeldende skiftet, skriv ut en Z-rapport og logg brukeren av systemet. | Ja | Ja | Ja | Nei | Nei |
| 139 | Fullfør transaksjon | Ber brukeren om å velge betalingsmåte | Ja | Ja | Nei | Ja | Nei |
| 620 | Opprett kundeordre | Konverter POS-transaksjonen til en kundeordre. | Ja | Ja | Nei | Ja\* | Nei |
| 925 | Kopier banksjekken | Denne operasjonen støttes ikke. | Gjelder ikke | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 620 | Opprett kundeordre | Konverter POS-transaksjonen til en kundeordre. | Ja | Ja | Antall | Ja\* | Antall |
| 621 | Opprett tilbud | Konverter POS-transaksjonen til et salgstilbud. | Ja | Ja | Antall | Ja\* | Antall |
| 636 | Opprett detaljhandelstransaksjon | Denne operasjonen lar brukeren opprette en standard salgstransaksjon når standard POS-virkemåte er å opprette kundeordrer. | Ja | Ja | Antall | Ja | Antall |
| 600 | Kunde | Legg til den angitt kunden i transaksjonen. | Antall | Antall | Antall | Ja | Antall |
| 11 00 | Innbetaling på kundekonto | Foreta en innbetaling på kundens konto. | Ja | Ja | Ja | Ja | Ja |
| 612 | Legg til kunde | Denne operasjonen lar brukeren opprette en ny kundepost. | Ja | Ja | Ja | Ja† | Antall |
| 603 | Fjern kunde | Fjern kunden fra gjeldende transaksjon. | Ja | Ja | Antall | Ja | Antall |
| 602 | Kundesøk | Denne operasjonen lar brukeren søke etter en kundepost ved å gå til kundesøkesiden i POS. | Ja | Ja | Ja | Ja | Antall |
| 609 | Kundetransaksjoner | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 917 | Databasetilkoblingsstatus | Denne operasjonen lar brukeren vise gjeldende tilkoblingsinnstillinger og bytte mellom tilkoblet og frakoblet modus. | Ja | Ja | Ja | Ja | Antall |
| 1200 | Rapporter startbeløp | Deklarer beløpet som ligger i kontantskuffen når dagen eller skiftet begynner. | Ja | Ja | Ja | Ja | Antall |
| 132 | Overstyring av innbetaling | Overstyr standard innbetaling for kundeordrer. | Ja | Ja | Antall | Ja\* | Antall |
| 913 | Deaktiver utformingsmodus | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 912 | Aktiver utformingsmodus | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 1217 | Demonteringssett | Del opp et sett i komponentproduktene. | Ja | Ja | Ja | Ja | Antall |
| 624 | Vis refunderingsbeløp | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 513 | Vis sum | Vis saldoen for transaksjonen i kundevisningen. | Ja | Ja | Ja | Ja | Antall |
| 623 | Rediger kunde | Rediger detaljene for gjeldende kunde. | Ja | Ja | Antall | Antall | Antall |
| 614 | Rediger kundeordre | Tilbakekall den valgte ordren, slik at den kan endres i POS. | Antall | Antall | Antall | Antall | Antall |
| 615 | Rediger tilbud | Tilbakekall det valgte tilbudet, slik at det kan endres i POS. | Antall | Antall | Antall | Antall | Antall |
| 518 | Utgiftskontoer | Registrer penger som fjernes fra kassaskuffen for uregelmessige utgifter. | Ja | Ja | Ja | Ja | Antall |
| 919 | Utvidet pålogging | Tilordne eller fjern tillatelse til å logge på ved å skanne en strekkode eller dra et kort. | Ja | Ja | Ja | Ja | Nei |
| 1201 | Flytoppføring | Denne operasjonen lar brukeren legge til mer penger i gjeldende skuff eller skift. | Ja | Ja | Ja | Ja | Antall |
| 1218 | Bruk opplåsing for ekstern enhet | Systemet bruker denne operasjonen internt for å låse opp POS-enheter. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 520 | Gavekortsaldo | Vis saldoen på et gavekort. | Ja | Ja | Antall | Antall | Antall |
| 708 | Deaktiver enhet | Deaktiver gjeldende enhet, slik at den ikke kan brukes som kasse på salgssted. | Antall | Antall | Antall | Antall | Antall |
| 517 | Inntektskontoer | Registrer penger som legges i kassaskuffen av andre grunner enn salg. | Ja | Ja | Ja | Ja | Antall |
| 801 | Beholdningsoppslag | Slå opp antall tilgjengelig, i ordre og tilgjengelig for ordre (ATP) for gjeldende butikk og andre tilgjengelige lokasjoner. | Ja | Ja | Ja | Antall | Antall |
| 122 | Fakturakommentar | Denne operasjonen lar brukeren skrive inn en kommentar om gjeldende transaksjon. | Ja | Ja | Antall | Ja | Antall |
| 511 | Utsted kreditnota | Utsted en kreditnota for å angi et bilag i stedet for en refusjon. | Ja | Ja | Antall | Antall | Antall |
| 512 | Utsted gavekort | Utsted et nytt gavekort for det angitte beløpet. | Ja | Ja | Antall | Antall | Antall |
| 625 | Utsted fordelskort | Utsted et fordelskort til en kunde, slik at kunden kan delta i butikkens fordelsprogram. | Ja | Ja | Ja | Antall | Antall |
| 300 | Linjerabattbeløp | Angi et rabattbeløp for et linjeelement i transaksjonen. Denne operasjonen brukes bare for varer som det gis rabatt på, og bare innenfor de angitte rabattrammene. | Ja | Ja | Antall | Ja | Antall |
| 301 | Linjerabatt i prosent | Angi en rabattprosent for et linjeelement i transaksjonen. Denne operasjonen brukes bare for varer som det gis rabatt på, og bare innenfor de angitte rabattrammene. | Ja | Ja | Antall | Ja | Antall |
| 703 | Lås kasse | Lås gjeldende kasse, slik at den ikke kan brukes, men ikke logg av gjeldende bruker. | Antall | Antall | Antall | Ja | Antall |
| 701 | Logg av | Logg gjeldende bruker av kassen. | Ja | Ja | Ja | Ja | Antall |
| 521 | Poengsaldo for fordelskort | Vis saldoen for poeng for det angitte fordelskortet. | Ja | Ja | Antall | Antall | Antall |
| 918 | Behandle skift | Vis en liste over skift som er aktive, suspendert eller blitt lukket usporet. | Ja | Ja | Ja | Antall | Antall |
| 914 | Minimer salgsstedvinduet | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 1000 | Åpne skuff | Utfører en "ikke salg"-operasjon og åpner den valgte kassaskuffen. | Ja | Ja | Ja | Ja | Antall |
| 928 | Ordreoppfyllelse | Denne operasjonen lar brukere plukke, pakke, sende eller tilbakekalle ordrer for butikken som er plukket. | Ja | Ja | Ja | Antall | Antall |
| 129 | Overstyr linjeproduktavgift | Overstyr avgiften på det valgte linjeelementet, og bruk en annen angitt avgift. | Ja | Ja | Antall | Ja | Antall |
| 130 | Overstyr linjeproduktavgift fra liste | Overstyr avgiften på det valgte linjeelementet, og bruk avgiften som brukeren velger fra en liste. | Ja | Ja | Antall | Ja | Antall |
| 127 | Overstyr transaksjonsavgift | Overstyr avgiften på transaksjonen, og bruk en annen angitt avgift. | Ja | Ja | Antall | Ja | Antall |
| 128 | Overstyr transaksjonsavgift fra liste | Overstyr avgiften på transaksjonen, og bruk avgiften som brukeren velger fra en liste. | Ja | Ja | Antall | Ja | Antall |
| 131 | Følgeseddel | Opprett en følgeseddel for den valgte ordren. | Antall | Antall | Antall | Antall | Antall |
| 710 | Par maskinvarestasjon | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 201 | Betal med kort | Godta et kort, for eksempel et kredittkort eller debetkort, som betaling. | Ja | Ja | Antall | Ja | Antall |
| 200 | Betal kontant | Godta kontanter som betaling. | Ja | Ja | Antall | Ja | Antall |
| 206 | Hurtigkontantbetaling | Fullfør transaksjonen med én berøring, og godta beløpet som forfaller i kontanter (nøyaktig beløp). | Ja | Ja | Antall | Ja | Antall |
| 204 | Lønnsslipp | Godta en sjekk som betaling. | Ja | Ja | Antall | Ja | Antall |
| 213 | Betal med kreditnota | Godta en kreditnota (bilag) som ble utstedt av butikken. | Ja | Ja | Antall | Antall | Antall |
| 203 | Betal i valuta | Godta betaling i ulike valutaer. | Ja | Ja | Antall | Ja | Antall |
| 202 | Betal via kundekonto | Belast kundekontoen med transaksjonen. Denne betalingsmåten er ikke gyldig for kundenordreinnskudd. | Ja | Ja | Antall | Antall | Antall |
| 214 | Betal med gavekort | Godta et gavekort som er utstedt av butikken. | Ja | Ja | Antall | Antall | Antall |
| 207 | Betal med fordelskort | Godta et fordelskort til betaling, og løs inn poeng mot kvalifiserte produkter. | Ja | Ja | Antall | Antall | Antall |
| 634 | Betalingshistorikk | Vis kundens betalingshistorikk for gjeldende kundeordre. | Ja | Ja | Antall | Antall | Antall |
| 803 | Plukk og mottak | Åpne siden **Plukk og mottak** der du kan velge ordrene som skal plukkes eller mottas i butikken. | Ja | Ja | Ja | Antall | Antall |
| 632 | Plukk alle produkter | Angi oppfyllingsmetoden til **Henting i butikk** for alle linjer. | Ja | Ja | Antall | Ja\* | Antall |
| 631 | Plukk valgte produkter | Angi oppfyllingsmetoden til **Henting i butikk** for valgte linjer. | Ja | Ja | Antall | Ja\* | Antall |
| 400 | Hurtigmeny | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 101 | Priskontroll | Denne operasjonen lar brukeren slå opp prisen for et bestemt produkt. | Ja | Ja | Ja | Ja | Antall |
| 104 | Prisoverstyring | Overstyr prisen på et produkt hvis produktet er konfigurert for å tillate prisoverstyringer. | Ja | Ja | Antall | Ja | Antall |
| 1058 | Skriv ut regnskapsår X | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 1059 | Skriv ut regnskapsår Z | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 927 | Skriv ut vareetikett | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 926 | Skriv ut hylleetikett | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 1056 | Skriv ut X | Skriv ut og X-rapport for gjeldende skift. | Ja | Ja | Ja | Antall | Antall |
| 103 | Produktkommentar | Legg til en kommentar til det valgte linjeelementet. | Ja | Ja | Antall | Ja | Antall |
| 100 | Produktsalg | Legg til et angitt produkt i transaksjonen. | Ja | Ja | Ja | Ja | Antall |
| 108 | Produktsøk | Denne operasjonen lar brukeren søke etter et produkt ved å gå til produktsøkesiden i POS. | Ja | Ja | Ja | Ja | Antall |
| 633 | Utløpsdato for tilbud | Denne operasjonen lar brukeren vise eller endre utløpsdatoen for et salgstilbud. | Ja | Ja | Antall | Ja\* | Antall |
| 627 | Omberegn | Beregn alle kundeordrelinjer og avgifter på nytt basert på gjeldende konfigurasjon. | Ja | Ja | Antall | Ja\* | Antall |
| 515 | Tilbakekall ordre | Denne operasjonen lar brukeren søke etter og tilbakekalle kundeordrer og salgstilbud. | Ja | Ja | Ja | Antall | Antall |
| 504 | Tilbakekall transaksjon | Denne operasjonen lar brukeren tilbakekalle en tidligere suspendert transaksjon fra gjeldende butikk. | Ja | Ja | Antall | Ja‡ | Antall |
| 305 | Innløs fordelspoeng | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |
| 635 | Refundering av forsendelseskostnader | Denne operasjonen lar brukeren refundere forsendelseskostnader for en avbrutt ordre. | Antall | Antall | Antall | Antall | Antall |
| 644 | Fjern kupongkode | Be brukeren om å fjerne kuponger ved å velge dem i en liste over kuponger som er knyttet til transaksjonen. | Ja | Ja | Antall | Ja | Antall |
| 1057 | Skriv ut Z på nytt | Skrive ut Z-rapporten for det forrige eller valgte skiftet. | Ja | Ja | Ja | Antall | Antall |
| 1216 | Angi et nytt passord | Denne operasjonen lar en bruker som har tillatelse for tilbakestilling av passord, tilbakestille passord for en annen ansatt ved hjelp av et midlertidig passord. | Ja | Ja | Ja | Antall | Antall |
| 1219 | Åpne URL-adresse på salgssted | Denne operasjonen gjør det mulig for en bruker å åpne en administratorkonfigurert URL-adresse på salgsstedet. | Ja | Ja | Ja | Ja | Antall | 
| 109 | Returprodukt | Utfør retur av enkeltprodukter. Det neste skannede produktet vises som et returprodukt som har negativt antall og pris. | Ja | Ja | Antall | Ja | Antall |
| 114 | Returtransaksjon | Tilbakekall en tidligere transaksjon etter kvitteringsnummer for å returnere noen av eller alle produktene. | Ja | Ja | Ja | Ja§ | Antall |
| 1211 | Deponer til safe | Utfør en deponering til safe, og flytt penger fra kassen til safen. | Ja | Ja | Ja | Ja | Antall |
| 516 | Salgsfaktura | Denne operasjonen lar kunden betale mot den valgte salgsfakturaen. | Ja | Ja | Antall | Antall | Antall |
| 502 | Selger | Denne operasjonen lar brukeren sette verdien **Salgstaker** på en salgsordre for kundeordrer i POS. | Ja | Ja | Antall | Ja\* | Antall |
| 2000 | Planlegg behandling | Denne operasjonen lar brukeren opprette, endre eller vise tidsplaner for ansatte. | Ja | Ja | Ja | Antall | Antall |
| 2001 | Planlegg forespørsler | Denne operasjonen lar brukeren be om fri, bytte av skift eller tilby skift til andre ansatte. | Ja | Ja | Ja | Antall | Antall |
| 622 | Søk i ordrer | Denne operasjonen lar brukere forhåndsdefinere POS-knapper til å utføre søk etter vare, kunde eller kategori. | Ja | Ja | Ja | Ja | Antall |
| 1213 | Søk etter leveringsadresse | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 709 | Velg maskinvarestasjon | Denne operasjonen lar brukeren velger en maskinvarestasjon i en liste over tilgjengelige maskinvarestasjoner. | Ja | Ja | Ja | Ja | Antall |
| 637 | Angi standard selger i transaksjon | Denne operasjonen kan brukeren velge én av de kvalifiserte provisjonssalgsgruppene (selgere) som standardselger for linjer som legges til senere. | Ja | Ja | Antall | Ja | Antall |
| 105 | Angi antall | Endre antallet i et linjeelement i transaksjonen. | Ja | Ja | Antall | Ja | Antall |
| 638 | Angi selger på linje | Denne operasjonen kan brukeren velge én av de kvalifiserte provisjonssalgsgrupper (selgere) for gjeldende valgte linje. | Ja | Ja | Antall | Ja | Antall |
| 630 | Lever alle produkter | Sett oppfyllingsmodus til **Levering** for alle linjeelementene. | Ja | Ja | Antall | Ja\* | Antall |
| 629 | Lever valgte produkter | Sett oppfyllingsmodus til **Levering** for de valgte linjene. | Ja | Ja | Antall | Ja\* | Antall |
| 115 | Vis journal | Vis butikkens journal. Du kan vise transaksjoner, skrive ut kvitteringer og gavekvitteringer og tilbakekalle for retur. | Ja | Ja | Ja | Ja\*\* | Antall |
| 802 | Lagerantall | Denne operasjonen lar brukeren opprette eller endre lagertellingsjournaler for fysisk beholdning eller syklustellinger. | Ja | Ja | Ja | Antall | Antall |
| 401 | Undermeny | Denne operasjonen omdirigerer brukeren til en annen koblet knappegruppe. | Ja | Ja | Ja | Ja | Antall |
| 1054 | Avbryt skift | Avbryt gjeldende skift, slik at et nytt eller annet skift kan aktiveres i gjeldende journal. | Ja | Ja | Ja | Antall | Antall |
| 503 | Suspender transaksjon | Avbryte gjeldende salgstransaksjon, slik at den kan tilbakekalles senere i butikken. | Ja | Ja | Antall | Ja‡ | Antall |
| 1004 | Oppgaveregistrering | Åpne Oppgaveopptaker for å registrere fremgangsmåter i POS. | Antall | Antall | Antall | Ja | Antall |
| 1052 | Kasseoppgjør | Denne operasjonen lar brukeren angi pengebeløpet i skuffen for hver enkelt tellende betalingsmåte. | Ja | Ja | Ja | Ja | Antall |
| 1210 | Fjerning av betalingsmidler | Denne operasjonen lar brukeren fjerne penger fra gjeldende skuff eller skift. | Ja | Ja | Ja | Ja | Antall |
| 920 | Tidsklokke | Denne operasjonen lar brukere stemple inn og ut fra arbeidsskift og pauser. | Ja | Ja | Ja | Antall | Antall |
| 302 | Totalt rabattbeløp | Angi et rabattbeløp for transaksjonen. Denne operasjonen gjelder bare for varer som det gis rabatt på, og bare innenfor de angitte rabattrammene. | Ja | Ja | Antall | Ja | Antall |
| 303 | Total rabattprosent | Angi en rabattprosent for transaksjonen. Denne operasjonen gjelder bare for varer som det gis rabatt på, og bare innenfor de angitte rabattrammene. | Ja | Ja | Antall | Ja | Antall |
| 501 | Transaksjonskommentar | Legg til en kommentar i gjeldende transaksjon. | Ja | Ja | Antall | Ja | Antall |
| 922 | Vis produktdetaljer | Åpne siden med produktdetaljer for det valgte linjeelementet. | Ja | Ja | Antall | Ja | Antall |
| 1003 | Vise rapporter | Vis rapporter som er konfigurert for gjeldende bruker. | Ja | Ja | Ja | Antall | Antall |
| 921 | Vis tidsklokkeoppføringer | Vis klokkeslettoppføringer for alle ansatte i butikken. | Ja | Ja | Ja | Antall | Antall |
| 211 | Annullert betaling | Annuller den valgte betalingslinjen fra transaksjonen. | Ja | Ja | Antall | Ja | Antall |
| 102 | Annullert produkt | Annuller det valgte linjeelementet fra transaksjonen. | Ja | Ja | Antall | Ja | Antall |
| 500 | Annuller transaksjon | Annuller gjeldende transaksjon. | Ja | Ja | Antall | Ja | Antall |
| 916 | Windows Workflow Foundation | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Antall |
| 924 | X-rapport for bankkort | Denne operasjonen støttes ikke. | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Gjelder ikke her | Ja |

\* Operasjonen er tilgjengelig i frakoblet modus bare når det opprettes et kundeordre eller et salgstilbud, og bare hvis frakoblet oppretting av kundeordrer eller salgstilbud er konfigurert i POS-funksjonalitetsprofilen. Operasjonen kan ikke utføres når ordrer opprettes ved hjelp av Real-time Service, eller når ordrer tilbakekalles eller redigeres.

† Operasjonen kan utføres i frakoblet modus bare når POS er konfigurert til å tillate frakoblet opprettelse av kunder i POS-funksjonalitetsprofilen.

‡ Når POS er frakoblet, kan bare suspenderte transaksjoner tilbakekalles bare fra den frakoblede databasen for gjeldende kasse. Brukere kan ikke suspendere og tilbakekalle transaksjoner på tvers av kasser.

§ Når salgsstedet er frakoblet, kan bare transaksjoner i gjeldende frakoblede database tilbakekalles for retur.

\*\* Når salgsstedet er frakoblet, kan bare transaksjoner i gjeldende frakoblede kanaldatabase vises i journalen.
