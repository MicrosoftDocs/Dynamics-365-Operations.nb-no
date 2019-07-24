---
title: Behandling av Faktisk vekt-produkt med lagerstyring
description: Dette emnet beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.
author: perlynne
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 85b6cad04032877b63b4da3a097cae82c63f36ad
ms.sourcegitcommit: bf05924747368a5204c4c70882e3347bfa295e29
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2019
ms.locfileid: "1633089"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Behandling av Faktisk vekt-produkt med lagerstyring

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a>Funksjonseksponering

Hvis du vil bruke lagerstyring til å behandle faktisk vekt-produkter, må du bruke en lisenskonfigurasjonsnøkkel for å aktivere funksjonen. (Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**. I **Konfigurasjonsnøkler**-kategorien viser du deretter **Handel \> Lager- og transportstyring** og merker av for **Faktisk vekt for lager**.)

> [!NOTE]
> Både lisenskonfigurasjonsnøkkelen for **Lager- og transportstyring** og lisenskonfigurasjonsnøklene for **Behandle distribusjon \> Faktisk vekt** må være aktivert i tillegg.

Når lisenskonfigurasjonsnøkkelen er aktivert, kan du velge **Faktisk vekt** når du oppretter et frigitt produkt. Du kan også knytte det frigitte produktet til en lagringsdimensjonsgruppe som parameteren **Bruk lagerstyringsprosesser** er valgt for.

Før du kan bruke produktet i Lagerstyring, må du definere noen grunnleggende produktspesifikke innstillinger for faktisk vekt:

- Definer den pålydende vektomregningen mellom faktisk vekt-enheten (boks) og lagerenheten (kilogram \[kg\]) som en del av enhetskonverteringsdefinisjonen.
- Definer toleransene for minste og største vekt som en del av oppsettet for faktisk vekt-enheten.
- Definer en sekvensgruppe for enhet der faktisk vekt-enheten er definert som laveste lagerføringsenhet (SKU).
- Definer en policy for behandling av faktisk vekt-varer.

Hvis du vil ha mer informasjon, se [Definere og vedlikeholde faktisk vekt-varer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transaksjonsjusteringer

Siden vekten på lagerbeholdningen når den kommer inn på et lager kan være forskjellig fra vekten når den utstedes fra lageret, må behandlingen av faktisk vekt-produkt justere beholdningen.

**Eksempel 1**

Under produksjonsprosessen **Rapporter som fullført** registreres den innkommende vekten for et nummerskilt som inneholder åtte bokser med et faktisk vekt-produkt, som 80,1 kg. Nummerskiltet lagres deretter i området for ferdigvarer, og i løpet av lagringsperioden reduseres vekten noe.

Senere i salgsordreplukkingsprosessen blir vekten for det samme nummerskiltet registrert som 79,8 kg. Derfor har du nå en vektforskjell som en del av det fysiske dimensjonssettet.

I dette tilfellet justerer systemet automatisk forskjellen ved å postere en transaksjon for den manglende 0,3 kg.

**Eksempel 2**

I definisjonen er et produkt konfigurert til å godta en minimumsvekt på 8 kg og en maksimumsvekt på 12 kg for faktisk vekt-enheten **Boks**.

Du har to bokser med produktet, og de har en registrert vekt på 16 kg. Hvis en lagermedarbeider plukker og veier én av boksene, og vekten blir registrert til 9 kg, vil den gjenværende boksen veie 7 kg. Fordi 7 kg er under minimumsvekten, foretar systemet en automatisk justering for å øke vekten på lagerbeholdningen med 1 kg.

Hvis du vil definere kontoene som disse justeringene posteres til, kan du gå til **Kostnadsstyring \> Oppsett for policyer for finansintegrering \> Postering**. I **Lager**-kategorien kan du så definere følgende kontoer:

- Tapskonto for faktisk vekt
- Overskuddskonto for faktisk vekt

## <a name="catch-weight-item-handling-policy"></a>Policy for behandling av faktisk vekt-varer

Policyen for behandling av faktisk vekt-varer definerer to primære lagerstyringsflyter for varene: når vekten på varene blir registrert, og hvordan de blir registrert.

Du kan definere når vekten blir registrert for salgs- og overføringsordrebehandling. Vekten kan bli registrert under én av følgende prosesser:

- **Plukking** – Vekten blir registrert under de innledende plukkarbeidslinjene i ordrearbeidet.
- **Pakking** – Vekten blir registrert under manuell pakking. (Du må sende varene til en pakkestasjon.)

Hvis den faktiske vekten blir registrert på pakkestasjonen under containerpakkeprosessene, blir ikke lagermedarbeidere bedt om å registrere vekten under plukkearbeidet. I stedet brukes gjennomsnittlig vekt på det fysiske lageret som vekt for den plukkede beholdningen som går til pakkeområdet.

For interne lagerstyringsprosesser som telling og justering er det mulig å definere om vekten skal registreres eller ikke. Hvis den ikke registreres, brukes pålydende vekt.

Du kan også definere hvordan vekten blir registrert. I én av de to hovedflytene spores faktisk vekt-koder og brukes til å registrere vekten. I den andre flyten spores ikke faktisk vekt-koder.

- **Ja** – Varen bruker faktisk vekt-koder. Hvert kodenummer representerer én faktisk vekt-enhet (boks), og vekt og annen informasjon er knyttet til koden. For utgående prosesser brukes vekten som er knyttet til koden.
- **Nei** – Varen bruker ikke faktisk vekt-koder. Innkommende og utgående veieprosesser er basert på den faktiske vekten som registreres under hver prosess.

Prosessen med å spore faktisk vekt-koder kan brukes for varer som ikke endrer vekt i lagringsperioden. Vekten registreres bare under den innkommende lagerprosessen. Under den utgående prosessen skannes bare faktisk vekt-kodene, og vekten som er knyttet til kodene, brukes i den utgående transaksjonsbehandlingen.

### <a name="how-to-capture-catch-weight"></a>Registrere faktisk vekt

Når sporing av faktisk vekt-koder brukes, må en kode alltid opprettes for hver faktisk vekt-enhet som mottas, og hver kode må alltid være knyttet til en vekt.

For eksempel **Boks** er faktisk vekt-enheten, og du får én pall med åtte bokser. I dette tilfellet må det opprettes åtte unike faktisk vekt-koder, og en vekt må knyttes til hver kode. Avhengig av den innkommende faktisk vekt-koden, kan enten vekten på alle åtte boksene registreres og gjennomsnittlig vekt kan deretter distribueres til hver boks, eller en unik vekt kan registreres for hver boks.

Når sporing av faktisk vekt-koder ikke brukes, kan vekten registres for hvert dimensjonssett (for eksempel for hver(t) nummerskilt og sporingsdimensjon). Vekten kan også registreres basert på et aggregert nivå, for eksempel fem nummerskilt (paller).

For metodene for registrering av utgående vekt kan du definere om veiingen utføres for hver faktisk vekt-enhet (det vil si per boks), eller om vekten blir registrert basert på antallet som plukkes (for eksempel tre bokser). Merk at for produksjonslinjeplukking og interne flytteprosesser brukes gjennomsnittlig vekt hvis alternativet **Ikke registrert** brukes.

For å begrense plukkeprosessene i lagerstyringen fra å hente vekt som resulterer i justeringer av fortjeneste/tap for faktisk vekt, kan variansmetoden for utgående vekt brukes.

## <a name="supported-scenarios"></a>Scenarier som støttes

Ikke alle arbeidsflyter støtter behandling av faktisk vekt-produkter med lagerstyring. Følgende begrensninger gjelder for øyeblikket.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfigurere faktisk vekt-produkter for lagerstyringsprosesser

- For faktisk vekt-produkter kan ikke lagringsdimensjonsgruppen for varer endres (slik at lagerstyringsprosesser kan brukes for dem).
- Bare formelbehandling støttes for faktisk vekt-produkter (ikke stykkliste).
- Faktisk vekt-produkter kan ikke knyttes til en sporingsdimensjonsgruppe ved hjelp av Eier-dimensjonen.
- Faktisk vekt-produkter kan ikke brukes som tjenester.
- Faktisk vekt-produkter kan bare brukes som lagerførte produkter når de er del av varemodellgruppen.
- Faktisk vekt-produkter kan ikke brukes sammen med funksjonen for sporing Aktiv i salgsprosess.
- Faktisk vekt-produkter kan ikke brukes sammen med funksjonen for registrering av serienumre. Derfor kan ikke produkter overføres fra en "tom" til et serienummer som en del av plukkingen/pakkingen.
- Faktisk vekt-produkter kan ikke brukes sammen med funksjonen for registrering av serienumre før forbruk.
- Faktisk vekt-produkter som er variantaktivert, kan ikke brukes sammen med funksjonen for å konvertere variantmåleenhet.
- Faktisk vekt-produkter kan ikke merkes som et produktsett for detaljhandel.
- Faktisk vekt-produkter kan bare brukes sammen med en enhetssekvensgruppe som har faktisk vekt-håndteringsenheter, og som har faktisk vekt-enheten som laveste sekvens.
- For faktisk vekt-produkter kan lagerenheten konverteres til faktisk vekt-enheten bare hvis konverteringen gir et nominelt antall som er mer enn 1.
- Oppsettet for strekkoder for faktisk vekt-produkter støtter ikke oppsett av variabel vekt.
 
### <a name="order-processing"></a>Ordrebehandling

- Oppretting av forhåndsvarsel for forsendelse (ASN/pakkestrukturer) støtter ikke vektinformasjon.
- Ordreantallet må vedlikeholdes basert på faktisk vekt-enheten.
 
### <a name="inbound-warehouse-processing"></a>Innkommende lagerbehandling

- Mottak av nummerskilt krever at vekten tilordnes under registreringen fordi vektinformasjon ikke støttes som en del av forhåndsvarslet for forsendelse. Når faktisk vekt-kodeprosesser brukes, må kodenummeret tilordnes manuelt per faktisk vekt-enhet.
 
### <a name="inventory-and-warehouse-operations"></a>Beholdning og lageroperasjoner

- Manuell oppretting av karanteneordrer støttes ikke for faktisk vekt-produkter.
- Manuell flytting av beholdning som er knyttet til arbeid, støttes ikke for faktisk vekt-produkter.
- Konsolidering av nummerskilt støttes ikke for faktisk vekt-produkter.
- Nummerskiltlasting for å initialisere lagerlagring støttes ikke for faktisk vekt-produkter.
- Partibalanseringsprosesser støttes ikke for faktisk vekt-produkter.
- Behandling av negativt fysisk lager støttes ikke for faktisk vekt-produkter.
- Lagermerking kan ikke brukes for faktisk vekt-produkter.
 
### <a name="outbound-warehouse-processing"></a>Utgående lagerbehandling

- Funksjonen for gruppeplukking støttes ikke for faktisk vekt-produkter.
- Plukk og pakk-lagerbehandling støttes ikke for faktisk vekt-produkter.
- For faktisk vekt-produkter kan arbeid som er definert i en arbeidsmal, utføres automatisk.
- Funksjonen for tilbakeføring av arbeid støttes ikke for faktisk vekt-produkter.
- For faktisk vekt-produkter støttes ikke manuell pakkestasjonbehandling der arbeid opprettes etter beholdere er lukket.
- Funksjonen for stykkevis skanning støttes ikke for faktisk vekt-produkter.
 
### <a name="production-processing"></a>Produksjonsbehandling

- For faktisk vekt-produkter støttes bare partiordrer for formelprodukter.
- Kanban-funksjonen støttes ikke for faktisk vekt-produkter.
- Serienumre for faktisk vekt-produkter kan ikke registreres før forbruk.
- Funksjonen for tilbakeføring av nummerskilt støttes ikke for faktisk vekt-produkter.
- For faktisk vekt-produkter kan ikke ferdigmelding registreres etter serienummer.

### <a name="transportation-management-processing"></a>Transportstyringbehandling

- Behandling av arbeidsområde for lastplanlegging støttes ikke for faktisk vekt-produkter.
- Transportforespørselslinjer støttes ikke for faktisk vekt-produkter.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andre begrensninger og virkemåter for behandling av faktisk vekt-produkter med lagerstyring

- Under plukkeprosesser der brukeren ikke blir bedt om å identifisere sporingsdimensjoner, utføres vekttilordningen basert på gjennomsnittlig vekt. Denne virkemåten oppstår når for eksempel en kombinasjon av sporingsdimensjoner brukes på samme sted og, etter en bruker behandler plukking, bare én sporingsdimensjonsverdi er igjen på lokasjonen.
- Når lager er reservert for et faktisk vekt-produkt som er konfigurert for lagerstyringsprosesser, gjøres reservasjonen basert på den minste vekten som er definert, selv om dette antallet er det siste behandlingsantallet på lager. Denne virkemåten er forskjellig fra den for varer som ikke er konfigurert for lagerstyringsprosesser.
- Prosesser som bruker vekten som en del av kapasitetsberegninger (bølgeterskler, maksimale arbeidsinndelinger, maksimumsverdier for beholder, lokasjonsbelastningskapasitet og så videre), bruker ikke den faktiske vekten for lageret. I stedet er prosessene basert på den fysiske håndteringsvekten som er definert for produktet.
- Generelt støttes ikke funksjonen for detaljhandel for faktisk vekt-produkter.
 
### <a name="catch-weight-tags"></a>Faktisk vekt-koder

Funksjonen for faktisk vekt-koder støttes for øyeblikket bare som en del av følgende scenarier:

- Ved behandling av bestillingsmottak i lagerapp.
- Ved behandling av lastemottak via lagerapp.
- For nummerskiltmottak som er knyttet til bestillingslasting, kreves vekttilordning under mottaksprosessen. For overføringsordremottak brukes derimot vekten fra forsendelsesdataene for overføringsordren.
- For overføringsordrevare og linjemottak som kommer fra et ikke-lagerstyringsprosesslager.
- Behandlingen av salgsreturordremottak kan registrere faktisk vekt-koder, men behandlingen valideres ikke hvis kodene er de samme kodene som opprinnelig ble sendt for en bestemt salgsordrelinje.
- Ved behandling av en lagerstatus som er endret ved hjelp av lagerappen.
- Når en lageroverføring gjøres ved å bruke lagerappen.
- Ved behandling av justering inn og ut via lagerappen.
- Når plukkarbeid behandles for salgs- og overføringsordrer. (Vær oppmerksom på at faktisk vekt-koder ikke kan registreres for produksjonskomponentplukking.)
- Når plukket antall reduseres fra lastlinjer, uavhengig av om containere brukes.
- Når produkter pakkes i containere på en pakkestasjon.
- Når containere åpnes på nytt.
- Når formelprodukter rapporteres som ferdig ved å bruke lagerappen.
- Når transportlaster behandles ved hjelp av lagerappen.

En kode for faktisk vekt kan enten opprettes ved hjelp av en lagerappprosess, som opprettes manuelt i skjemaet, eller ved å opprette en dataenhetsprosess. Hvis en kode for faktisk vekt blir knyttet til en innkommende kildedokumentlinje, for eksempel bestillingslinjen, registreres koden. Hvis linjen blir brukt til utgående behandling. Koden vil bli oppdatert som levert.
