---
title: Butikkordreoppfyllelse
description: Denne artikkelen gir en oversikt over butikkordreoppfyllelse i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/16/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-10-30
ms.openlocfilehash: bf338c6d0b6a237cad2974d36c23238029fe9b38
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785079"
---
# <a name="store-order-fulfillment"></a>Butikkordreoppfyllelse

[!include [banner](includes/banner.md)]

Denne artikkelen gir en oversikt over butikkordreoppfyllelse i Microsoft Dynamics 365 Commerce.

Mange forhandlere vil optimalisere ordreoppfyllelsen ved å la butikker oppfylle ordrer. Ordreoppfyllelse på butikknivå kan bidra til å forenkle scenarier med for store lagre for en bestemt butikk, eller det kan være nødvendig med hensyn til logistikk i tilfeller der en butikk har ekstra kapasitet eller befinner seg nærmere avstand for levering til kunden. For å løse dette behovet, er en enhetlig ordreoppfyllelsesoperasjon tilgjengelig på salgsstedet.

Ordrer for oppfyllelse i en bestemt butikk har butikkens lager angitt i overskriften eller på linjene i ordren.

Ordrefullføringen på salgsstedet gir et enkelt arbeidsområde på salgsstedet som kan brukes til å behandle ordrer. Dette omfatter alt fra å godta ordren, merke den som sendt eller starte butikkplukking.

Følgende video gir en oversikt og demo av funksjoner for butikkinnfrielse i Dynamics 365 Commerce.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE5bRXE]

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Tilgang til enhetlig ordreoppfyllelse på salgsstedet

Ordreoppfyllelse [Operasjons-ID 928](pos-operations.md) kan brukes til å få tilgang til arbeidsområdet for butikkordreoppfyllelse på salgsstedet.

Ordreoppfyllelsesoperasjonen har ikke sin egen standard tillatelse, men i fremtiden vil brukerne kunne bruke tillatelsen **Tillat henting av ordre** for å starte operasjonen fra salgsstedet.

En konfigurasjonsinnstilling er tilgjengelig for å finne ut om en ordrelinje må godtas manuelt fra salgsstedet, på butikknivået. Hvis dette konfigurasjonsalternativet ikke er angitt, godtas ordrelinjer som standard. Hvis dette konfigurasjonsalternativet er aktivert, må brukerne på salgsstedet velge tillatelsen **Tillat godkjenning av ordre** for å godta ordrer fra salgsstedet.

Ordrelinjer kan også avvises fra salgsstedet. Avvisning av en ordrelinje betyr at den ikke blir oppfylt i butikken og sender ordrelinjen tilbake for ny tilordning til en annen butikk eller lager. Tillatelse for ordrelinjeavslag gis via **Tillat ordreavvisning**-tillatelsen.

## <a name="order-fulfillment-operation-parameters"></a>Parametre for ordreoppfyllelsesoperasjonen

Ordreoppfyllelse gir standardparametere som kan brukes i operasjonen når den kalles på salgsstedet. Når **Alle ordrer**-parameteren er konfigurert, vises alle ordrer når operasjonen brukes. Parameteren **Ordrer som skal leveres** viser bare ordrer som må sendes fra butikken, og **Ordrer for plukking** viser ordrer som skal plukkes i butikken.

## <a name="orders-for-fulfillment"></a>Ordrer for oppfyllelse

Ordreoppfyllelsesoperasjonen viser bare ordrer som skal plukkes i eller leveres fra gjeldende butikk. Ordrer for andre butikker som skal oppfyllese, vises ikke når du bruker ordreoppfyllelsesoperasjonen.

## <a name="line-selection"></a>Linjevalg

Linjene kan velges ved hjelp av **Velg**-funksjonen i handlingsruten. Når **Velg** er aktivert, kan flere linjer velges for behandling. Du kan fjerne valgte linjer ved å klikke den samme linjen på nytt.

## <a name="line-details"></a>Linjedetaljer

Linjedetaljer kan vises ved hjelp av undermenyen for linjedetaljer. Når denne menyen brukes, finnes det tre kategorier som viser tilleggsinformasjon for den valgte linjen. Den første kategorien, **Linjedetaljer**, viser detaljer om selve linjen, for eksempel det bestilte antallet og restantallet. Du finner flere detaljer, inkludert antall plukket, pakket og fakturert i tillegg til leveringsmåte og leveringsadresse. **Ordredetaljer**-kategorien gir ordrehodeinformasjon, inkludert kunde, kunde-ID, ordrenummer, ordretotal og saldo. **Lager**-kategorien viser informasjon for den valgte linjen i henhold til tilgjengelig fysisk lager, reservert lager og bestilt lager.

Hvis flere linjer er valgt, angir bare ordrelinjeundermenyen at flere linjer er valgt. Hvis du vil vise detaljer for én enkelt linje, fjerner du linjene til en linje gjenstår.

## <a name="pending-order-lines"></a>Ventende ordrelinjer

Samlet ordreoppfyllelse inkluderer muligheten til å godta ordrer manuelt. Som standard er ordrer for oppfyllelse i butikken allerede godtatt. Hvis imidlertid forretningsprosesser angir at en arbeider på butikknivå må godta ordrer, kan manuell godkjenning aktiveres på detaljhandelsnivå. Hvis du vil aktivere ordregodkjenning, kan du gå til **Retail og Commerce** \> **Kanaler** \> **Butikker** \> **Alle butikker**. Åpne ønsket butikk og i **Generell**-kategorien finner du **Ordreoppfyllelse**-underhodet. Denne underoverskriften har alternativet **Godta manuelt** som er satt til **Nei** som standard. Ved å angi dette alternativet til **Ja** og synkronisere endringene til kanaldatabasen, kan ordrelinjer gå gjennom godkjenningsprosessen.

Ansatte med **Tillat godkjenning av ordre**-tillatelsen kan åpne ordreoppfyllelse og velge linjer for godkjenning. Når linjene er godkjent, endre deres status fra **Ventende** til **Godkjent**, og resten av fullføringen ordreprosessen kan utføres. Når **Godta manuelt** er slått på, behandles ikke ordrene før de har blitt godkjent.

Ordrer for butikkhenting har aldri **Ventende**-tilstanden. Dette gjøres for å unngå et scenario der en kunde kommer i butikken og ordrelinjen ikke kan behandles fordi en arbeider med de riktige rettighetene ikke er tilgjengelig.

## <a name="accepted-order-lines"></a>Godkjente ordrelinjer

Ordrer med linjestatusen **Godkjent** kan gå gjennom resten av ordreoppfyllelsesprosessen på salgsstedet. Når en ordre er godtatt, kan gjenstående handlinger foretas mot ordrelinjen.

For eksempel, en godkjent ordrelinje kan velges og deretter plukkes direkte uten å gå gjennom plukk og pakking.

## <a name="line-actions"></a>Linjehandlinger

### <a name="pick"></a>Plukk

**Plukk**-kategorien for handlinger gis for å hjelpe med å plukke ordrelinjer fra hyller. Plukkhandlingen kan bare utføres på ordrelinjene som er godtatt tidligere.

**Handling: Plukking**

- **Resulterende salgsstedsstatus:** Plukking
- **Resulterende back office-status:** Ingen endring

Når en ordre er godtatt, kan linjer velges og merkes som **Plukking**. Å merke en linje som **Plukking** er en måte å vise at plukkarbeidet allerede utføres på en linje. Dette hindrer at to arbeidere forsøker å plukke de samme ordrelinjene samtidig.

**Handling: Skriv ut plukkliste**

- **Resulterende status:** Plukking
- **Resulterende back office-status:** Ingen endring

Plukklister kan skrives ut på salgsstedet for å hjelpe ansatte å utføre plukkeprosessen. En utskrevet plukkliste kan tas med av arbeideren som utfører plukkingen, og etter hvert som varene plukkes, kan arbeideren merke dem manuelt som plukket på plukklisten.

Plukklisteformatet konfigureres i Commerce og legges til kvitteringsprofilen. Hvis du vil ha mer informasjon om hvordan du konfigurerer kvitteringsprofiler, kan du se [Kvitteringsmaler og utskrift](receipt-templates-printing.md).

Hvis linjene er valgt, og en plukkliste skrives ut for disse linjene, oppdateres de automatisk med **Plukking**-statusen.

**Handling: Merk som plukket**

- **Resulterende status:** Plukket eller delvis plukket
- **Resulterende back office-status:** Plukket eller delvis plukket

Etter at den fysiske plukkprosessen er utført, kan linjer merkes med **Plukket**. Å velge en linje og merke den som **Plukket** utfører et sanntidskall for å oppdatere ordrelinjen. Etter at linjen er merket som **Plukket** på salgsstedet, oppdateres også statusen i back office til **Plukket** og lagertransaksjoner reflekterer at det angitte antallet er redusert.

Når ordrer behandles over tid, kan delvise antall behandles for en bestemt linje. Hvis en linje er merket og handlingen **Merk som plukket** er tatt, og antallet er større enn 1, blir brukeren bedt om antallet. Det gjenværende antallet som skal plukkes, fylles ut automatisk. Hvis mindre enn restantallet er angitt, blir statusen for linjen **Delvis plukket**. Når ordrelinjen oppdateres i back office, vil den også gjenspeile delvis plukket-statusen, og antallet som er angitt av brukeren, brukes for lageroppdateringen.

Hvis en ordrelinje blir plukket ved en feiltakelse, kan prosessen for å legge tilbake utføres på ordrelinjen i back office. Det er for øyeblikket ingen handling for å legge tilbake som støttes, på salgsstedet.

Ordrelinjer fra forskjellige ordrer kan velges og merkes som **Plukking**, skrives ut på samme plukkliste eller merkes som **Plukket**.

### <a name="pack"></a>Pakke

Ordrelinjer kan pakkes når som helst etter at ordrelinjen er godtatt.

**Handling: Skriv ut følgeseddelen**

- **Resulterende status:** Pakket eller delvis pakket
- **Resulterende back office-status:** Levert eller delvis levert

Denne handlingen merker linjene som pakket eller delvis pakket og skriver ut en følgeseddel. En følgeseddel kan skrives ut for å validere produktene som er pakket sammen. Følgeseddelformatet konfigureres i Commerce og legges til kvitteringsprofilen. Hvis du vil ha mer informasjon om hvordan du konfigurerer kvitteringsprofiler, kan du se [Kvitteringsmaler og utskrift](receipt-templates-printing.md).

**Handling: Merk som pakket**

- **Resulterende status:** Pakket eller delvis pakket
- **Resulterende back office-status:** Levert eller delvis levert

**Merk som pakket**-handlingen kan brukes til å angi at linjer er pakket uten å skrive ut en følgeseddel. Både **Skriv ut følgeseddel** og **Merk som pakket** resulterer i lagertransaksjoner i back office. Pakkelinjene på salgsstedet fører til at følgeseddeljournaler genereres i back office.

Hvis en ordrelinje er pakket ved en feiltakelse, må følgeseddeljournalen rettes i back office.

Bare linjer på den samme ordren og med samme leveringsmåte kan pakkes samtidig.

Alternativet for å merke butikkhentingslinjer som **Pakket** er for øyeblikket deaktivert. Denne funksjonen vil bli lagt til i en fremtidig versjon. Opprettingsprosessen for følgesedler blir forbedret for å støtte innsetting av tredjeparts forsendelsesinformasjon i følgeseddelprosessen.

### <a name="pick-up"></a>Plukk

Ordrer for henting i butikken kan plukkes direkte når de er hentet på salgsstedet. Butikkhentingsordrer krever ikke godkjenning.

**Handling: Henting**

- **Resulterende status:** Fakturert eller delvis fakturert
- **Resulterende back office-status:** Fakturert eller delvis fakturert

Hvis en linje er valgt for henting fra samlet ordreoppfyllelse, lastet hele ordren til salgsstedet og hele antallet for den valgte linjen merkes. Andre linjer i ordren lastes også i transaksjonsvisningen for salgsstedet, men med antallet merket som null.

Når linjer for plukking er lastet inn i transaksjonsvisningen, kan transaksjonen betales på vanlig måte.

Linjer som er fullstendig fakturert gjennom henting, vises ikke lenger i samlet ordrebehandling. Linjer som er delvis hentet, vil fortsatt vises i samlet ordreoppfyllelse til de er plukket i sin helhet.

Hvis en linje blir hentet ved en feiltakelse, må du utføre en retur for å rette feilen.

Bare linjer på den samme ordren og med samme leveringsmåte kan hentes samtidig.

### <a name="shipping"></a>Forsendelse

Ordrelinjer som skal sendes fra butikken, kan behandles gjennom felles ordrefullføring ved å bruke **Lever**-handlingen. Hvis manuell ordrelinjegodkjenning er konfigurert på kanalnivået, må ordrer godkjennes før forsendelse. Når en ordrelinje er godtatt og har statusen **Ventende** eller annen status, kan linjene sendes.

**Handling: Send**

- **Resulterende status:** Fakturert eller delvis fakturert
- **Resulterende back office-status:** Fakturert eller delvis fakturert

Linjer som sendes fra samlet ordreoppfyllelse, faktureres fra back office på lignende måte som om ordren faktureres direkte fra back office. Linjer som leveres fra samlet ordreoppfyllelse, lastes ikke inn i transaksjonsvisningen, og det utføres ingen betaling når linjene leveres.

Ordrelinjer som er fullstendig levert, vises ikke lenger i samlet ordreoppfyllelse. Linjer som er delvis sendt, vil fortsatt vises i samlet ordreoppfyllelse til de er sendt i sin helhet.

Bare linjer fra den samme ordren kan leveres samtidig. Hvis linjene fra den samme ordren har ulike leveringsmåter, kan de likevel merkes for forsendelse samtidig.

### <a name="reject"></a>Avvis

Linjer eller delvise linjer kan avvises. Dette gjør at de kan tildeles på nytt fra back office til en annen butikk eller annet lager. Linjene kan bare avvises hvis de ennå ikke er plukket eller pakket. Hvis du vil avvise en linje som allerede er plukket eller pakket, må linjen være uplukket eller upakket fra back office.

**Handling: Avvis**

- **Resulterende status:** Avvist
- **Resulterende back office-status:** Ingen endring

Du kan vise avviste ordrelinjer fra **Salgsordrebehandling og -spørring**-arbeidsområdet. Fjern personfilteret i arbeidsområdet for å vise alle avviste ordrelinjer på tvers av butikkene. **Avviste ordrelinjer**-kategorien under **Ordrer og favoritter**-delen viser ordrelinjedetaljene. I tillegg kan brukerne klikke på **Avviste ordrelinjer**-knappen under **Sammendrag**-delen og navigere til en salgsordrevisning. Dette viser alle ordrene som har én eller flere avviste ordrelinjer. Hvis Distributed Order Management (DOM) er aktivert, vil disse avviste ordrene bli automatisk tilordnet på nytt til de riktige butikkene for fullføring, men disse ordrelinjene kan også tilordnes på nytt manuelt. Hvis du vil gjøre dette, velger du linjen som viser **Oppfyllelsesstatus** som **Avvist** og endrer området/lageret etter behov. Klikk **Oppdater linje**-rullegardinmenyen og klikk **Tilbakestill oppfyllelsesstatus** for å endre oppfyllelsesstatusen fra **Avvist** til **Godkjent** eller **Ventende** avhengig av oppsettet av ordreoppfyllelse. Når oppfyllelsesstatusen er tilbakestilt, kan butikkarbeiderne vise ordrelinjene i POS.

## <a name="line-quantity-tracking"></a>Linjeantallsporing

En enkelt ordrelinje for antall som er større enn 1, kan behandles over tid, noe som fører til flere undertilstander for ordrelinjer. Hvis for eksempel en byggmester har et prosjekt som krever 500 bord, men byggmesteren henter bare eller får levert noen få bord på et tidspunkt i løpet av prosjektet, kan det være antall som blir plukket, pakket og sendt på samme tidspunkt.

Når en linje merkes, blir det gjenstående antallet for linjen automatisk utfylt og det antas at restantallet blir behandlet. Ved bruk av eksemplet ovenfor: Hvis 200 bord allerede er plukket og linjen for bord er valgt for plukking, fylles restantallet på 300 automatisk ut i antallet. Det samme gjelder hvis 200 bord allerede er fakturert. I så fall blir bare restantallet automatisk fylt ut.

Vi fortsetter med eksemplet ovenfor: hvis 200 bord merkes som pakket og levering er valgt, blir hele beløpet på 500 automatisk utfylt. Hvis bare 200 bord sendes, antar systemet at de tidligere pakkede bordene leveres, og at det pakkede antallet vil reduseres. Hvis 201 bord sendes, blir de pakkede bordene først redusert med det gjenværende enkeltbordet som blir redusert fra restantallet.

## <a name="line-statuses"></a>Linjestatuser

Ordrelinjer i salgsstedet har flere statuser for å vise tilstanden for ordrelinjen. Statusene i salgsstedet og back office samsvarer ikke i alle tilfeller. Ordrelinjestatus kan vises via salgsstedet med ordreoppfyllelsesoperasjonene. I back office kan du vise ordrelinjene fra ordredetaljene. Ordredetaljer kan nås via **Retail og Commerce** \> **Kunder** \> **Alle kundeordrer**. Velg **Ordre-ID** for å vise ordredetaljer. Fra ordredetaljer velger du **Salgsordre**-kategorien, og velger deretter **Detaljert status** under **Vis**-underoverskriften.

- **Ventende** – Ordrelinjer som er tilordnet til en butikk, men ennå ikke godkjent, har **Ventende**-status når de vises på salgsstedet. Linjer som venter på godkjenning på salgsstedet, får **Ordrebehandling** statusen i back office.
- **Godkjent** – Ordelinjer som er godkjent manuelt eller automatisk godkjent, får statusen **Godkjent** når de vises på salgsstedet. Linjer med **Godkjent**-status vises som **Ordrebehandling** i back office.
- **Plukking** – Linjer som for øyeblikket blir plukket på butikknivå, har statusen **Plukking**. De samme linjene, når de vises i back office, vises som **Ordrebehandling**.
- **Plukket** og **Delvis plukket** – Linjer som er plukket eller delvis plukket på salgsstedet, får statusen **Plukket** eller **Delvis plukket**. De samme linjene i back office vises også som **Plukket** eller **Delvis plukket**.
- **Pakket** og **Delvis pakket** – Linjer som er pakket eller delvis pakket på salgsstedet, får statusen **Pakket** eller **Delvis pakket**. De samme linjene i back office vises også som **Levert** eller **Delvis levert**.
- **Delvis fakturert** – Linjene som er delvis plukket eller delvis levert, får statusen **Delvis fakturert** på salgsstedet og i back office.
- **Fakturert** – Linjer som er fullstendig fakturert på salgsstedet, vises ikke lenger for oppfyllelse. Status for disse linjene i back office er **Fakturert**.

## <a name="order-fulfillment-filtering"></a>Ordreoppfyllelsesfiltrering

Ordreoppfyllelse på salgsstedet omfatter filtrering for å hjelpe brukeren med enkelt å finne det de trenger. Filtre kan endres via handlingsruten nederst på **Salgssted**-skjermen. Som standard brukes et **Leveringstype**-filter, basert på hvordan operasjonen er konfigurert. Hvis operasjonen er definert med **Alle ordrer**-parameteren, vil dette filteret brukes når du åpner ordreoppfyllelse. Det samme gjelder **Henting i butikk**- og **Send fra butikk**-parameteren. Andre filtre som kan brukes på ordreoppfyllelsesvisningen, omfatter:

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
