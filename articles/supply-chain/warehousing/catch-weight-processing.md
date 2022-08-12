---
title: Produktbehandling for faktisk vekt med lagerstyring
description: Denne artikkelen beskriver hvordan du bruker arbeidsmaler og lokasjonsdirektiver for å bestemme hvordan og hvor arbeid utføres i lageret.
author: perlynne
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy, TMSLoadBuildWorkbench, WHSCatchWeightTagRegistration, WHSCatchWeightTagFullDimDiscrepancies, WHSCatchWeightTagChangeWeightDropDownDialog, WHSCatchWeightLinkWorkLineTagDropDownDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 881c3c4aa655a5ad30adffce108ba2fc3e6691c5
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070417"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Behandling av Faktisk vekt-produkt med lagerstyring

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>Funksjonseksponering

Hvis du vil bruke lagerstyring til å behandle faktisk vekt-produkter, må du bruke en lisenskonfigurasjonsnøkkel for å aktivere funksjonen. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**. I **Konfigurasjonsnøkler**-fanen viser du deretter **Handel \> Lager- og transportstyring** og merker av for **Faktisk vekt for lager**.

> [!NOTE]
> Både lisenskonfigurasjonsnøkkelen for **Lager- og transportstyring** og lisenskonfigurasjonsnøklene for **Behandle distribusjon \> Faktisk vekt** må være aktivert i tillegg. Hvis du vil angi konfigurasjonsnøklene for faktisk vekt, må du også aktivere funksjonen ved hjelp av arbeidsområdet **Funksjonsbehandling**. Hovedfunksjonen som må aktiveres, er **Behandling av Faktisk vekt-produkt med lagerstyring**. To relaterte, men valgfrie funksjoner som du kanskje vil aktivere, er **Lagerstatusendringer for faktisk vekt-produkter** og **Bruk eksisterende variabel vekt-koder ved rapportering av produksjonsordrer som ferdigstilte**.

Når lisenskonfigurasjonsnøkkelen er aktivert, kan du velge **Faktisk vekt** når du oppretter et frigitt produkt. Du kan også knytte det frigitte produktet til en lagringsdimensjonsgruppe som parameteren **Bruk lagerstyringsprosesser** er valgt for.

Før du kan bruke produktet i Lagerstyring, må du definere noen grunnleggende produktspesifikke innstillinger for faktisk vekt:

- Definer den pålydende vektomregningen mellom faktisk vekt-enheten (boks) og lagerenheten (kilogram \[kg\]) som en del av enhetskonverteringsdefinisjonen.
- Definer toleransene for minste og største vekt som en del av oppsettet for faktisk vekt-enheten.
- Definer en sekvensgruppe for enhet der faktisk vekt-enheten er definert som laveste lagerføringsenhet (SKU).
- Definer en policy for behandling av faktisk vekt-varer.

Hvis du vil ha mer informasjon, se [Definere og vedlikeholde faktisk vekt-varer](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Transaksjonsjusteringer

Siden vekten på lagerbeholdningen når den kommer inn på et lager kan være forskjellig fra vekten når den utstedes fra lageret, må behandlingen av faktisk vekt-produkt justere beholdningen.

> [!NOTE]
> Mobilenhetsaktivitet vil bare utløse transaksjonsjusteringer hvis metoden for utgående vektavvik for varens policy for behandling av faktisk vekt-varer er **Tillat vektavvik**.

### <a name="example-1"></a>Eksempel 1

Under produksjonsprosessen **Rapporter som fullført** registreres den innkommende vekten for et nummerskilt som inneholder åtte bokser med et faktisk vekt-produkt, som 80,1 kg. Nummerskiltet lagres deretter i området for ferdigvarer, og i løpet av lagringsperioden reduseres vekten noe.

Senere i salgsordreplukkingsprosessen blir vekten for det samme nummerskiltet registrert som 79,8 kg. Derfor har du nå en vektforskjell som en del av det fysiske dimensjonssettet.

I dette tilfellet justerer systemet automatisk forskjellen ved å postere en transaksjon for den manglende 0,3 kg.

### <a name="example-2"></a>Eksempel 2

I definisjonen er et produkt konfigurert til å godta en minimumsvekt på 8 kg og en maksimumsvekt på 12 kg for faktisk vekt-enheten **Boks**.

Du har to bokser med produktet, og de har en registrert vekt på 16 kg. Hvis en lagermedarbeider plukker og veier én av boksene, og vekten blir registrert til 9 kg, vil den gjenværende boksen veie 7 kg. Fordi 7 kg er under minimumsvekten, foretar systemet en automatisk justering for å øke vekten på lagerbeholdningen med 1 kg.

Hvis du vil definere kontoene som disse justeringene posteres til, kan du gå til **Kostnadsstyring \> Oppsett for policyer for finansintegrering \> Postering**. I **Lager**-fanen kan du så definere følgende kontoer:

- Tapskonto for faktisk vekt
- Overskuddskonto for faktisk vekt

## <a name="catch-weight-item-handling-policy"></a>Policy for behandling av faktisk vekt-varer

Policyen for behandling av faktisk vekt-varer definerer to primære lagerstyringsflyter for varene: når vekten på varene blir registrert, og hvordan de blir registrert.

Du kan definere når vekten blir registrert for salgs- og overføringsordrebehandling. Vekten kan bli registrert under én av følgende prosesser:

- **Plukking** – Vekten blir registrert under de innledende plukkarbeidslinjene i ordrearbeidet.
- **Pakking** – Vekten blir registrert under manuell pakking. (Du må sende varene til en pakkestasjon.)

Hvis den faktiske vekten blir registrert på pakkestasjonen under containerpakkeprosessene, blir ikke lagermedarbeidere bedt om å registrere vekten under plukkearbeidet. I stedet brukes gjennomsnittlig vekt på det fysiske lageret som vekt for den plukkede beholdningen som går til pakkeområdet. Dette konseptet gjelder også for faktisk vekt-varer som spores av koder. For varer som spores av koder, bestemmer disse parameterne når koden registreres. Koden kan registreres ved plukking ved hjelp av mobilenheten eller under manuell pakking.

> [!NOTE]
> Ettersom **Emballasje**-alternativet fører til at beholdningen oppdateres med gjennomsnittlig plukket vekt, kan dette utløse et avvik som kan føre til en justering av fortjeneste/tap for faktisk vekt og/eller et avvik mellom lagerbeholdningsvekten og faktisk vekt-kode-vekten.

For interne prosesser, som telling og justering, kan du definere om vekten skal registreres. Hvis den ikke registreres, brukes pålydende vekt. Andre alternativer lar deg registrere vekt per faktisk vekt-enhet og per opptellingsantall.

Du kan også definere hvordan vekten blir registrert. I én av de to hovedflytene spores faktisk vekt-koder og brukes til å registrere vekten. I den andre flyten spores ikke faktisk vekt-koder.

- **Ja** – Varen bruker faktisk vekt-koder. Hvert kodenummer representerer én faktisk vekt-enhet (boks), og vekt og annen informasjon er knyttet til koden. For utgående prosesser brukes vekten som er knyttet til koden.
- **Nei** – Varen bruker ikke faktisk vekt-koder. Innkommende og utgående veieprosesser er basert på den faktiske vekten som registreres under hver prosess.

Prosessen med å spore faktisk vekt-koder kan brukes for varer som ikke endrer vekt i lagringsperioden. Vekten registreres bare under den innkommende lagerprosessen. Under den utgående prosessen skannes bare faktisk vekt-kodene, og vekten som er knyttet til kodene, brukes i den utgående transaksjonsbehandlingen.

En annen viktig parameter som er relatert til behandlingen av faktisk vekt-koder, er **Sporingsmetode for faktisk vekt-kodedimensjon**. Koder kan enten spores delvis eller fullstendig. Hvis en kode spores delvis, spores produktdimensjoner, sporingsdimensjoner og lagerstatus. Hvis en kode spores fullstendig, spores produktdimensjoner, sporingsdimensjoner og **alle** lagringsdimensjoner.

Når en vare spores av kode, finnes parameteren **Registreringsmetode for utgående kode**. Du kan angi denne parameteren slik at du alltid blir bedt om koden på utgående transaksjoner fra mobilenheten. Du kan også angi parameteren slik at du bare blir spurt om koder når de er nødvendige. Det er for eksempel fem faktisk vekt-koder på lager på et gitt nummerskilt, og du har angitt at du vil plukke alle fem kodene fra nummerskiltet. I dette tilfellet, hvis **Registreringsmetode for utgående kode**-parameteren settes til **Bare be om kode ved behov**, plukkes de fem kodene automatisk. Du trenger ikke skanne hver kode. Hvis parameteren settes til **Alltid be om kode**, må du skanne hver kode, selv om alle fem kodene blir plukket.

> [!NOTE]
> Som regel registreres koder og oppdateres bare fra menyelementene for mobilenhet. Men det finnes noen få scenarier der koder registreres et annet sted (for eksempel fra den manuelle pakkestasjonen). Generelt bør menyelementene for mobilenheter brukes for all lageraktivitet hvis det brukes koder.

### <a name="how-to-capture-catch-weight"></a>Registrere faktisk vekt

**Når sporing av faktisk vekt-koder brukes**, må en kode alltid opprettes for hver faktisk vekt-enhet som mottas, og hver kode må alltid være knyttet til en vekt.

For eksempel **Boks** er faktisk vekt-enheten, og du får én pall med åtte bokser. I dette tilfellet må det opprettes åtte unike faktisk vekt-koder, og en vekt må knyttes til hver kode. Avhengig av den innkommende faktisk vekt-koden, kan enten vekten på alle åtte boksene registreres og gjennomsnittlig vekt kan deretter distribueres til hver boks, eller en unik vekt kan registreres for hver boks.
Når du bruker funksjonen **Bruk eksisterende variabel vekt-koder ved rapportering av produksjonsordrer som ferdigstilte** med prosessen aktivert via et menyelement for mobilenhet, blir lageret oppdatert basert på eksisterende informasjon om variabel vekt-kode. Som et resultat ber ikke mobilappen Lagerstyring om å registrere variabel vekt-kodedataene som en del av en produksjonsrapport som en ferdig operasjon.

**Når sporing av faktisk vekt-koder ikke brukes**, kan vekten registres for hvert dimensjonssett (for eksempel for hver(t) nummerskilt og sporingsdimensjon). Vekten kan også registreres basert på et aggregert nivå, for eksempel fem nummerskilt (paller).

For metodene for registrering av utgående vekt lar alternativet **Per faktisk vekt-enhet** deg angi at veiingen skal utføres for hver faktisk vekt-enhet (for eksempel per eske). Du kan bruke alternativet **Per plukkenhet** til å angi at vekten skal registreres basert på antallet som skal plukkes (for eksempel tre esker). Merk at for produksjonslinjeplukking og interne flytteprosesser brukes gjennomsnittlig vekt hvis alternativet **Ikke registrert** brukes.

Det er definert flere vektregistreringsmetoder i policyen for behandling av faktisk vekt-varer. Hver parameter for vektregistreringsmetode brukes i forskjellige transaksjoner. I tabellen nedenfor finner du en oversikt over hvilke parametere som brukes av hvilke transaksjoner.

| Metode                                     | Transaksjon                                |
|--------------------------------------------|--------------------------------------------|
| Registreringsmetode for utgående vekt           | Salgsplukking, overføringsplukking            |
| Registreringsmetode for produksjonsplukkvekt | Produksjonsplukking, produksjonsforbruk |
| Registreringsmetode for bevegelsesvekt           | Bevegelse                                   |
| Når vektkorrigering skal registreres       | Justeringer, opptelling                      |
| Registreringsmetode for opptellingsvekt           | Opptelling                                   |
| Registreringsmetode for lageroverføringsvekt | Lageroverføring                         |

For å forhindre at plukkeprosessene i lagerstyringen henter vekt som fører til justeringer av fortjeneste/tap for faktisk vekt, kan du bruke variansmetoden for utgående vekt. Variansmetoden for utgående vekt gjelder under følgende mobilenhetsprosesser: salgsplukking, overføringsplukking, produksjonsplukking, bevegelser, opptelling og lageroverføringer. Du kan bruke alternativet **Begrens vektavvik** hvis vekten til faktisk vekt-varen ikke svinger under lageroppbevaringen, og hvis justeringer av fortjeneste/tap for faktisk vekt ikke er nødvendig. Du kan bruke alternativet **Tillat vektavvik** hvis vekten kan svinge, og hvis justeringer av fortjeneste/tap for faktisk vekt er nødvendig når en vektvariasjon registreres.

## <a name="unsupported-scenarios"></a>Scenarier som ikke støttes

Ikke alle arbeidsflyter støtter behandling av faktisk vekt-produkter med lagerstyring. Følgende begrensninger gjelder for øyeblikket. De gjelder for alle faktisk vekt-varer, uansett om de er merket.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfigurere faktisk vekt-produkter for lagerstyringsprosesser

- Bare formelbehandling støttes for faktisk vekt-produkter (ikke stykkliste).
- Faktisk vekt-produkter kan ikke knyttes til en sporingsdimensjonsgruppe ved hjelp av Eier-dimensjonen.
- Faktisk vekt-produkter kan ikke brukes som tjenester.
- Faktisk vekt-produkter kan bare brukes som lagerførte produkter når de er del av varemodellgruppen.
- Faktisk vekt-produkter kan ikke brukes sammen med funksjonen for sporing Aktiv i salgsprosess.
- Faktisk vekt-produkter kan ikke brukes sammen med funksjonen for registrering av serienumre. Derfor kan ikke produkter overføres fra en "tom" til et serienummer som en del av plukkingen/pakkingen.
- Faktisk vekt-produkter kan ikke brukes sammen med funksjonen for registrering av serienumre før forbruk.
- Faktisk vekt-produkter som er variantaktivert, kan ikke brukes sammen med funksjonen for å konvertere variantmåleenhet.
- Faktisk vekt-produkter kan ikke merkes som et produktsett for handel.
- Faktisk vekt-produkter kan bare brukes sammen med en enhetssekvensgruppe som har faktisk vekt-håndteringsenheter, og som har faktisk vekt-enheten som laveste sekvens.
- Oppsettet for strekkoder for faktisk vekt-produkter støtter ikke oppsett av variabel vekt.

### <a name="order-processing"></a>Ordrebehandling

- Oppretting av forhåndsvarsel for forsendelse (ASN/pakkestrukturer) støtter ikke vektinformasjon.
- Ordreantallet må vedlikeholdes basert på faktisk vekt-enheten.

### <a name="inbound-warehouse-processing"></a>Innkommende lagerbehandling

- Mottak av nummerskilt krever at vekten tilordnes under registreringen fordi vektinformasjon ikke støttes som en del av forhåndsvarslet for forsendelse. Når faktisk vekt-kodeprosesser brukes, må kodenummeret tilordnes manuelt per faktisk vekt-enhet.
- Innkommende kvalitetskontrollarbeid støttes ikke for faktisk vekt-produkter. Hvis konfigurert, blir kvalitetskontrollarbeidet hoppet over.

### <a name="inventory-and-warehouse-operations"></a>Beholdning og lageroperasjoner

- Manuell oppretting av karanteneordrer støttes ikke for faktisk vekt-produkter.
- Manuell flytting av beholdning som er knyttet til åpent arbeid, støttes ikke for faktisk vekt-produkter.
- Nummerskiltlasting for å initialisere lagerlagring støttes ikke for faktisk vekt-produkter.
- Partibalanseringsprosesser støttes ikke for faktisk vekt-produkter.
- Behandling av negativt fysisk lager støttes ikke for faktisk vekt-produkter.
- Lagermerking kan ikke brukes for faktisk vekt-produkter.

### <a name="outbound-warehouse-processing"></a>Utgående lagerbehandling

- Funksjonen for gruppeplukking støttes ikke for faktisk vekt-produkter.
- Plukk og pakk-lagerbehandling støttes ikke for faktisk vekt-produkter.
- For faktisk vekt-produkter kan arbeid som er definert i en arbeidsmal, ikke utføres automatisk.
- For faktisk vekt-produkter støtter ikke systemet manuell pakkestasjonsbehandling der plukkarbeid for pakket container opprettes etter containere er lukket.
- Funksjonen for stykkevis skanning støttes ikke for faktisk vekt-produkter.

### <a name="production-processing"></a>Produksjonsbehandling

- For faktisk vekt-produkter støttes bare partiordrer for formelprodukter.
- Kanban-funksjonen støttes ikke for faktisk vekt-produkter.
- Serienumre for faktisk vekt-produkter kan ikke registreres før forbruk.
- Funksjonen for tilbakeføring av nummerskilt fra produksjon støttes ikke for faktisk vekt-produkter.
- For faktisk vekt-produkter kan ferdigmelding ikke registreres etter serienummer.

### <a name="transportation-management-processing"></a>Transportstyringbehandling

- Behandling av arbeidsområde for lastplanlegging støttes ikke for faktisk vekt-produkter.
- Transportforespørselslinjer støttes ikke for faktisk vekt-produkter.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andre begrensninger og virkemåter for behandling av faktisk vekt-produkter med lagerstyring

- Under plukkeprosesser der brukeren ikke blir bedt om å identifisere sporingsdimensjoner, utføres vekttilordningen basert på gjennomsnittlig vekt. Denne virkemåten oppstår når for eksempel en kombinasjon av sporingsdimensjoner brukes på samme sted og, etter en bruker behandler plukking, bare én sporingsdimensjonsverdi er igjen på lokasjonen.
- Når lager er reservert for et faktisk vekt-produkt som er konfigurert for Warehouse Management-prosesser (WMS), gjøres reservasjonen basert på den minste vekten som er definert, selv om dette antallet er det siste behandlingsantallet på lager. Denne virkemåten er forskjellig fra den for varer som ikke er konfigurert for WMS. Det er ett unntak fra denne begrensningen. Når det siste behandlingsantallet for et faktisk vekt-produkt som er serienummerkontrollert, plukkes, brukes den faktiske vekten for produksjonsplukking.
- Prosesser som bruker vekten som en del av kapasitetsberegninger (bølgeterskler, maksimale arbeidsinndelinger, maksimumsverdier for beholder, lokasjonsbelastningskapasitet og så videre), bruker ikke den faktiske vekten for lageret. I stedet er prosessene basert på den fysiske håndteringsvekten som er definert for produktet.
- Generelt støttes ikke funksjonen for handel for faktisk vekt-produkter.
- For faktisk vekt-produkter kan ikke lagerstatus oppdateres fra **Lagerstatusendring**.

### <a name="catch-weight-tags"></a>Faktisk vekt-koder

En kode for faktisk vekt kan opprettes ved hjelp av en prosess i mobilappen Lagerstyring, den kan opprettes manuelt i skjemaet **Lagerstyring > Forespørsler og rapporter > Faktisk vekt-kode**, eller den kan opprettes ved hjelp av en dataenhetsprosess. Hvis en kode for faktisk vekt blir knyttet til en innkommende kildedokumentlinje, for eksempel bestillingslinjen, registreres koden. Hvis linjen brukes til utgående behandling, blir koden oppdatert som levert. Du kan vise alle de historiske registreringshendelsene for faktisk vekt-kode via alternativet for **Registrering av faktisk vekt-kode** fra siden **Faktisk vekt-kode**.

Du kan bruke alternativet **Endre faktisk vekt-kode** til å oppdatere vektverdien for en varig faktisk vekt-kode manuelt. Legg merke til at vekten for lagerbeholdningen ikke blir justert som en del av denne manuelle prosessen, men du kan lett bruke siden **Beholdningsavvik for varer med faktisk vekt-kode** til å slå opp eventuelle avvik mellom de gjeldende aktive faktisk vekt-kodene og den gjeldende lagerbeholdningen.

Andre manuelle alternativer er **Registrer kode** på en kildedokumentlinje og **Registrer arbeid** mot et eksisterende lagerarbeid.

I tillegg til begrensningene som for øyeblikket gjelder for faktisk vekt-produkter, har kodede, faktisk vekt-produkter andre begrensninger som gjelder for øyeblikket.

- Alle manuelle oppdateringer av lager (det vil si oppdateringer som ikke utføres ved hjelp av en mobilenhet), må inkludere tilsvarende manuelle oppdateringer i de tilknyttede faktisk vekt-kodene fordi disse oppdateringene ikke utføres automatisk. Manuelle justeringsjournaler oppdaterer for eksempel lager, men ikke de tilknyttede faktisk vekt-kodene.
- Du må manuelt oppdatere faktisk vekt-koder for å gjenspeile etterfyllingsarbeidsbevegelser. Dette skyldes at systemet ikke kan registrere vekt under behandling av etterfyllingsarbeid, og registrerer derfor gjennomsnittlig vekt i stedet.
- Mottak av kombinerte nummerskilt støttes ikke for øyeblikket for kodede faktisk vekt-varer.
- Behandlingen av salgsreturordremottak kan registrere faktisk vekt-koder. Prosessen validerer imidlertid ikke at den returnerte koden er den samme koden som opprinnelig ble sendt for en salgsordre.
- Menyelementet for mobilenhet som har aktivitetskoden **Registrer materialforbruk**, støtter for øyeblikket ikke registrering av faktisk vekt-koder.
- Selv om opptellingsprosesser støttes for kodede faktisk vekt-varer, er de begrenset. Du kan for eksempel bruke alternativene for mobilenheter til opptelling av kodede faktisk vekt-varer, og gjennomsnittsvekten brukes. Faktisk vekt-koder oppdateres imidlertid ikke automatisk av opptellingstransaksjonen. Når opptellingstransaksjonen er fullført, må faktisk vekt-kodene oppdateres manuelt slik at de gjenspeiler lageret. Hvis varer som ikke var på et sted opprinnelig, telles opp på dette stedet, brukes den nominelle vekten.
- Skiltnummerkonsolidering støtter ikke kodede faktisk vekt-varer for øyeblikket.
- Funksjonen for tilbakeføring av arbeid støttes ikke for faktisk vekt-varer som spores etter kodenummer.

> [!NOTE]
> Informasjonen ovenfor om faktisk vekt-koder er bare gyldig hvis faktisk vekt-produktet har en sporingsmetode for faktisk vekt-kodedimensjon som spores fullstendig (det vil si hvis parameteren **Sporingsmetode for faktisk vekt-kodedimensjon** i policyen for behandling av faktisk vekt-varer settes til **Produktdimensjoner, sporingsdimensjoner og alle lagringsdimensjoner**). Hvis faktisk vekt-varen bare spores delvis av koder (det vil si hvis parameteren **Sporingsmetode for faktisk vekt-kodedimensjon** i policyen for behandling av faktisk vekt-varer settes til **Produktdimensjoner, sporingsdimensjoner og lagerstatus**), gjelder flere begrensninger. Siden synlighet går tapt mellom koden og lageret i dette tilfellet, støttes ikke enkelte andre scenarier.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]