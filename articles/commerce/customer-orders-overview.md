---
title: Kundeordrer på salgssted (POS)
description: Dette emnet gir informasjon om kundeordrer på salgssted (POS). Kundeordrer er også kjent som spesialbestillinger. Emnet inneholder en beskrivelse av relaterte parametere og flyter for transaksjonen.
author: josaw1
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9e5770de82638e6cef6d4c1dffd1dc85549fb11f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414630"
---
# <a name="customer-orders-in-point-of-sale-pos"></a>Kundeordrer på salgssted (POS)

[!include [banner](includes/banner.md)]

Dette emnet gir informasjon om hvordan du oppretter og administrerer kundeordrer på salgssted (POS). Kundeordrer kan brukes til å registrere salg der kunder vil hente produkter på en senere dato, hente produkter et annet sted eller få varer tilsendt. 

Omnikanal for handel gir mulighet for kundeordrer og spesialordrer, eller spesialordrer, for å møte ulike behov. Her er noen vanlige scenarier:

- En kunde ønsker produkter som skal leveres til en bestemt adresse på en bestemt dato.
- En kunde ønsker å plukke opp produkter fra en butikk eller lokasjon som er forskjellig fra butikken eller plasseringen der kunden kjøpte disse produktene.
- En kunde i en butikk ønsker å bestille produkter i dag og hente dem fra samme butikk på en senere dato.

Forhandlere kan bruke kundeordrer for å minimere tapt salg som ellers kan forårsakes av lagernedetid, fordi varene kan leveres eller hentes på et annet tidspunkt eller sted.

## <a name="set-up-customer-orders"></a>Definer kundeordrer
Før du prøver å bruke kundebestillingsfunksjonalitet i POS, må du sørge for at du fullfører alle nødvendige konfigurasjoner i Commerce Headquarters.

### <a name="configure-modes-of-delivery"></a>Konfigurere leveringsmåter

Hvis du vil bruke kundeordrer, må du konfigurere leveringsmåter som butikkanalen kan bruke. Du må definere minst én leveringsmåte som kan brukes når ordrelinjer sendes til en kunde fra en butikk. Du må også definere minst én hentemåte som kan brukes når ordrelinjer hentes fra butikken. Leveringsmåter defineres på siden **Leveringsmåter** i Commerce Headquarters. Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsmåter for handelskanaler, kan du se [Definere leveringsmåter](https://docs.microsoft.com/dynamics365/commerce/configure-call-center-delivery#define-delivery-modes).

![Siden leveringsmåter](media/customer-order-modes-of-delivery.png)


### <a name="set-up-fulfillment-groups"></a>Definere oppfyllelsesgrupper

Noen butikker eller lagerlokasjoner vil kanskje ikke kunne innfri kundeordrer. Ved å konfigurere oppfyllelsesgrupper kan en organisasjon angi hvilke butikker og lagerlokasjoner som skal vises som alternativer for brukere som oppretter kundeordrer i POS. Oppfyllelsesgrupper konfigureres på siden **Oppfyllelsesgrupper**. Organisasjoner kan opprette så mange oppfyllelsesgrupper de krever. Når en oppfyllelsesgruppe er definert, er den koblet til en butikk ved hjelp av en knapp i kategorien **Oppsett** i handlingsruten på siden **Butikker**.

I Commerce versjon 10.0.12 og nyere kan organisasjoner definere om lager- eller butikkombinasjonene som er definert i oppfyllelsesgrupper, kan brukes til forsendelse, henting eller begge deler. Derfor har butikken mer fleksibilitet for å styre lager- og butikkalternativene som vises for brukere som oppretter en ordre for henting i forhold til en ordre for forsendelse. Hvis du vil dra nytte av disse konfigurasjonsalternativene, må du aktivere funksjonen **Mulighet til å angi lokasjoner, som Forsendelse eller Henting, som er aktivert i en oppfyllelsesgruppe**. Hvis et lager som er knyttet til en oppfyllelsesgruppe, ikke er en butikk, kan det bare konfigureres som forsendelseslokasjon. Det kan ikke brukes når ordrer for henting er konfigurert i POS.

![Siden oppfyllelsesgrupper](media/customer-order-fulfillment-group.png)

### <a name="configure-channel-settings"></a>Konfigurere kanalinnstillinger

Når du arbeider med kundeordrer i POS, må du vurdere noen av innstillingene til butikkanalen. Disse innstillingene finner du på siden **Butikker** i Commerce Headquarters.

- **Lager** – Dette feltet angir lageret som brukes til å oppfylle ordrer som er konfigurert for forsendelse fra butikken.
- **Tilordning for oppfyllelsesgruppe** – Velg denne knappen (i kategorien **Oppsett** i handlingsruten) for å koble til oppfyllelsesgruppene det refereres til, for å vise alternativer for hentelokasjoner eller forsendelsesopprinnelse når kundeordrer opprettes i POS.
- **Bruk destinasjonsbasert avgift** – Dette alternativet angir om forsendelsesadressen brukes til å fastslå avgiftsgruppen som er brukt på ordrelinjer som er sendt til kundens adresse.
- **Bruk kundebasert avgift** – Dette alternativet angir om mva-gruppen som er definert for kundens leveringsadresse, brukes til å definere avgift for kundeordrer som opprettes i POS for levering til kundens hjem.

![Butikkanaloppsett på siden Butikker](media/customer-order-all-stores.png)

### <a name="set-up-customer-order-parameters"></a>Definere kundeordreparametere

Før du prøver å opprette kundeordrer i POS, må du konfigurere de aktuelle parameterne i Commerce Headquarters. Du finner disse parameterne i kategorien **Kundeordrer** på siden **Handelsparametere**.

- **Standard ordretype** – Du kan angi ordretypen som skal tilordnes som standard til kundeordrer som er opprettet i POS. Disse kundeordrene kan enten være salgsordrer eller tilbudsordrer. Uansett hva som er standard ordretype, kan brukerne fremdeles opprette både salgsordrer og kundeordrer fra POS.
- **Standard innbetalingsprosent** – Angi prosentandelen av det totale ordrebeløpet som kunden må betale som et innskudd før en ordre kan bekreftes. Avhengig av deres tilgangsnivå, kan butikkmedarbeidere overstyre beløpet ved å bruke operasjonen **Overstyring av innbetaling** i POS, hvis denne operasjonen er konfigurert for transaksjonsskjermoppsettet.
- **Leveringsmåte for henting** – Angi leveringsmåten som skal brukes på salgsordrelinjer som er konfigurert for henting i POS.
- **Leveringsmåte for utlevering** – Angi leveringsmåten som skal brukes på salgsinjer som anses som utleveringsordrelinjer når en blandet handlekurv opprettes, der noen av linjene blir hentet eller levert, og andre linjer blir utført av kunden umiddelbart.
- **Prosent for annulleringstillegg** – Hvis et tillegg skal brukes når en kundebestilling annulleres, angir du beløpet for det tillegget.
- **Kode for annulleringstillegg** – Angi kundetilleggskoden som skal brukes når det blir brukt et annulleringstillegg på annullerte kundeordrer i POS. Tilleggskoden definerer den økonomiske posteringslogikken for annulleringstillegget.
- **Kode for forsendelsestillegg** – Hvis alternativet **Bruk avanserte automatiske tillegg** er satt til **Ja**, har denne parameterinnstillingen ingen virkning. Hvis alternativet er satt til **Nei**, blir brukerne bedt om å angi et forsendelsestillegg manuelt når de oppretter kundeordrer i POS. Bruk denne parameteren til å tilordne en kundetilleggskode som skal brukes for ordrer når brukere angir et forsendelsestillegg. Tilleggskoden definerer den økonomiske posteringslogikken for forsendelsestillegget.
- **Bruk avanserte automatiske tillegg** – Sett dette alternativet til **Ja** for å bruke systemberegnede automatiske tillegg når kundeordrer opprettes i POS. Disse automatiske tilleggene kan brukes til å beregne forsendelsestillegg eller andre ordre- eller varespesifikke tillegg. Hvis du vil ha mer informasjon om hvordan du konfigurerer og bruker avanserte automatiske tillegg, kan du se [Avanserte automatiske tillegg for omnikanal](https://docs.microsoft.com/dynamics365/commerce/omni-auto-charges).

![Kategorien kundeordrer på siden Handelsparametere](media/customer-order-parameters.png)

### <a name="update-transaction-screen-layouts-in-pos"></a>Oppdatere transaksjonsskjermoppsett i POS

Kontroller at [skjermoppsettet](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) i POS er konfigurert til å støtte oppretting og behandling av kundeordrer, og at alle påkrevde POS-operasjoner er konfigurert. Her er noen av POS-operasjonene som anbefales for å støtte oppretting og administrasjon av kundeordrer på riktig måte:
- **Send alle produkter** – Denne operasjonen brukes til å angi at alle linjene i transaksjonskurven skal sendes til et mål.
- **Send alle valgte produkter** – Denne operasjonen brukes til å angi at valgte linjer i transaksjonskurven skal sendes til et mål.
- **Hent alle produkter** – Denne operasjonen brukes til å angi at alle linjene i transaksjonskurven blir hentet fra en valgt butikklokasjon.
- **Hent alle valgte produkter** – Denne operasjonen brukes til å angi at valgre linjer i transaksjonskurven blir hentet fra en valgt butikklokasjon.
- **Utlever alle produkter** – Denne operasjonen brukes til å angi at alle linjene i transaksjonskurven skal utføres. Hvis denne operasjonen brukes i POS, blir kundeordren konvertert til en hentesalgstransaksjon.
- **Utlever valgte produkter** – Denne operasjonen brukes til å angi at de valgte linjene i transaksjonskurven skal utføres av kunden på kjøpstidspunktet. Denne operasjonen er bare nyttig i et scenario for [hybrid ordre](https://docs.microsoft.com/dynamics365/commerce/hybrid-customer-orders).
- **Tilbakekall ordre** – Denne operasjonen brukes til å søke etter og hente kundeordrer, slik at POS-brukere kan redigere, annullere eller utføre oppgaver knyttet til oppfyllelse i dem etter behov.
- **Endre leveringsmåte** – Denne operasjonen kan brukes til raskt å endre leveringsmåten for linjer som allerede er konfigurert for forsendelse, uten at brukerne må gå gjennom flyten Lever alle produkter eller Send valgte produkter på nytt.
- **Overstyring av innbetaling** – Denne operasjonen kan brukes til å endre innbetalingsbeløpet som kunden skal betale for den valgte kundeordren.

![Operasjoner på transaksjonsskjermbildet i POS](media/customer-order-screen-layout.png)

## <a name="working-with-customer-orders-in-pos"></a>Arbeide med kundeordrer i POS

### <a name="create-a-customer-order-for-products-that-will-be-shipped-to-the-customer"></a>Opprette en kundeordre for produkter som skal leveres til kunden

1. Legg til en kunde i transaksjonen i transaksjonsskjermbildet i POS.
2. Legg til produkter i handlevognen.
3. Velg **Valgt for forsendelse** eller **Send alle** for å levere produktene til en adresse på kundekontoen.
4. Velg alternativet for å opprette en kundeordre.
5. Bekreft eller endre Send fra-lokasjonen, bekreft eller endre leveringsadressen, og velg en forsendelsesmetode.
6. Angi kundens leveringsdato for ønsket ordre.
7. Bruk betalingsfunksjonene til å betale for alle beregnede beløp som forfaller, eller bruke operasjonen **Overstyring av innbetaling** til å endre beløpene som forfaller, og deretter bruke betalingen.
8. Hvis den fullstendige ordresummen ikke ble betalt, angir du et kredittkort som skal registreres for saldoen som forfaller i ordren, når den faktureres.

### <a name="create-a-customer-order-for-products-that-the-customer-will-pick-up"></a>Opprette en kundeordre for produkter som kunden skal hente

1. Legg til en kunde i transaksjonen i transaksjonsskjermbildet i POS.
2. Legg til produkter i handlevognen.
3. Velg **Valgt for henting** eller **Hent alle** for å starte ordrehentingskonfigurasjonen.
4. Velg butikklokasjonen der kunden skal hente de valgte varene.
5. Velg en hentedato.
6. Bruk betalingsfunksjonene til å betale for alle beregnede beløp som forfaller, eller bruke operasjonen **Overstyring av innbetaling** til å endre beløpene som forfaller, og deretter bruke betalingen.
7. Hvis hele ordresummen ikke ble betalt, velger du om kunden skal utføre betalingen senere (ved henting), eller om et kredittkort skal tokeniseres nå, og deretter brukes og registreres ved henting.

### <a name="edit-an-existing-customer-order"></a>Rediger en eksisterende kundeordre

Detaljhandelsesordre som er opprettet i den nettbaserte kanalen eller butikkanalen, kan kalles tilbake og redigeres i POS etter behov.

> [!IMPORTANT]
> Ordrer som opprettes i en telefonsenterkanal, kan ikke redigeres via POS hvis innstillingen [Aktiver ordreoppfylelse](https://docs.microsoft.com/dynamics365/commerce/set-up-order-processing-options#enable-order-completion) er aktivert for telefonsenterkanalen. Hvis du vil sikre riktig betalingsbehandling, må ordrer som kom fra en telefonsenterkanal, og som bruker funksjonen for å aktivere ordreoppfyllelse, redigeres via telefonsenterappen i Commerce Headquarters.

I Commerce versjon 10.0.13 og tidligere kan brukere redigere støttede kundeordrer via POS bare hvis ordrene er helt åpne. Hvis noen av linjene i en ordre allerede er behandlet for oppfyllelse (plukking, pakking og så videre), blir ordren låst for redigering i POS.

> [!NOTE]
> I Commerce versjon 10.0.14 lar en funksjon som er frigitt i [offentlig forhåndsvisning](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms), POS-brukere redigere kundeordrer via POS, selv om noen av ordrene allerede er oppfylt. Ordrer som er helt fakturert, kan imidlertid fremdeles ikke redigeres via POS. Hvis du vil teste denne forhåndsvisningsfunksjonen og gi ekstra tilbakemelding, aktiverer du funksjonen **(forhåndsvisning) Rediger delvis fullførte ordrer i Point of Sale** i arbeidsområdet **Funksjonsbehandling**. Kundeordrer som kom fra en telefonsenterkanal, og som bruker funksjonen for å aktivere ordreoppfyllelse, kan ikke redigeres selv etter at denne funksjonen er aktivert.

1. Velg **Tilbakekall ordre**.
2. Bruk **Søk** til å angi filtre for å finne ordren, og velg deretter **Bruk**.
3. Velg ordren i resultatlisten, og velg deretter **Rediger**. Hvis knappen **Rediger** er utilgjengelig, er ordren i en tilstand der den ikke kan redigeres.
4. Utfør eventuelle nødvendige endringer i kundeordren fra transaksjonskurven. Noen endringer kan være forbudt under redigering.
5. Fullfør redigeringsprosessen ved å velge en betalingsoperasjon.
6. Hvis du vil avslutte redigeringsprosessen uten å lagre endringer, kan du bruke operasjonen **Annuller transaksjon**.



### <a name="cancel-a-customer-order"></a>Annullere en kundeordre

1. Velg **Tilbakekall ordre**.
2. Bruk **Søk** til å angi filtre for å finne ordren, og velg deretter **Bruk**.
3. Velg ordren i resultatlisten, og velg deretter **Annuller**. Hvis knappen **Annuller** er utilgjengelig, er ordren i en tilstand der den ikke lenger kan annulleres.
4. Hvis annulleringstillegg er konfigurert, bekrefter du dem. Du kan justere annulleringsgebyrene før du bekrefter dem etter behov. 
5. Fullfør annulleringsprosessen fra transaksjonskurven ved å velge en betalingsoperasjon. Hvis innskudd som ble betalt, overstiger annulleringstillegget, kan refusjonsbetalinger forfalle.
6. Hvis du vil avslutte annulleringsprosessen uten å lagre endringer, kan du bruke operasjonen **Annuller transaksjon**.

## <a name="finalizing-the-customer-order-shipment-or-pickup-from-pos"></a>Fullføre kundeordreforsendelsen eller hente fra POS

Etter at en ordre er opprettet, vil varene bli hentet av kunden fra en butikklokasjon eller levert, avhengig av konfigurasjonen av ordren. Hvis du vil ha mer informasjon om denne prosessen, kan du se dokumentasjonen for å [oppfyllelse av butikkordre](https://docs.microsoft.com/dynamics365/commerce/order-fulfillment-overview).

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asynkron transaksjonsflyt for kundeordrer

Kundeordrer kan opprettes i POS i synkron eller asynkron modus. Hvis du oppdager ytelsesspørsmål eller brukerforsinkelser når du oppretter kundeordrer i POS, bør du vurdere å aktivere oppretting av asynkrone ordrer.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>La kundeordrer opprettes i asynkron modus

1. På siden **Funksjonsprofiler** i Commerce Headquarters velger du funksjonsprofilen som samsvarer med butikken du vil konfigurere.
2. På **Generelt**-hurtigfanen angir du **Opprett kundeordre i asynkron modus** til **Ja**.

Når alternativet **Opprett kundeordre i asynkron modus** er satt til **Ja**, opprettes alltid kundeordrer i asynkron modus, selv om Retail Transaction Service (RTS) er tilgjengelig. Hvis du setter dette alternativet til **Nei**, opprettes alltid kundeordrer i synkron modus ved hjelp av RTS. Når kundeordrer opprettes i asynkron modus, trekkes de ut og opprettes som detaljhandelstransaksjoner i Commerce Headquarters fra Commerce Pull-jobber (P-jobber). De tilsvarende salgsordrene for detaljhandelstransaksjonene opprettes når **Synkroniser ordrer** kjøres manuelt eller via en satsvis prosess.

## <a name="additional-resources"></a>Tilleggsressurser

[Hybride kundeordrer](hybrid-customer-orders.md)
