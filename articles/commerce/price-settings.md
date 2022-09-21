---
title: Prissettingsinnstillinger
description: Denne artikkelen beskriver de ulike innstillingene for prisings- og rabattstyring i Microsoft Dynamics 365 Commerce headquarters.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 79130e0ef285d6bd5e544f2d6a6368c0393fa7fa
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474049"
---
# <a name="pricing-settings"></a>Prissettingsinnstillinger

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver de ulike innstillingene for prisings- og rabattstyring i Microsoft Dynamics 365 Commerce headquarters. Disse innstillingene gjør at organisasjoner kan definere prissettingsvirkemåten i Commerce-løsningen for å oppfylle bestemte forretningsbehov.

## <a name="company-level-pricing-settings"></a>Prissettingsinnstillinger på firmanivå

De fleste prissettingsinnstillingene er på firmanivå og er i **Handelsparametere \> Priser og rabatter** i Commerce headquarters.

### <a name="best-price-and-compound-concurrency-control-model"></a>Beste pris og sammensatt modell for samtidighetskontroll

Innstillingen **Beste pris og sammensatt modell for samtidighetskontroll** fastsetter hvordan prissettingsmotoren behandler flere rabatter i samtidighetsmodusen **beste pris** eller **sammensatt**. 

Hvis parameteren er satt til **Beste pris og sammensatt innen prioritet, aldri sammensatt på tvers av prioriteter**, blir alle **sammensatte** rabatter som har samme prisingsprioritet, sammensatt. Det sammensatte resultatet konkurrerer deretter med alle **beste pris**-rabatter som har samme prisingsprioritet. Den beste prisen brukes, og alle rabatter som har lavere prisingsprioritet, ignoreres.

Hvis parameteren er satt til **Beste pris bare innen prioritet, alltid sammensatt på tvers av prioriteter**, blir alle **sammensatte** rabatter behandlet som **beste pris**-rabatter. Bare én rabatt vinner i en prisingsprioritet. Hvis denne ene rabatten er en **beste pris**-rabatt eller **sammensatt** rabatt, blir den sammensatt med alle de ekstra **beste pris**-rabattene eller **sammensatte** rabattene som har lavere prisingsprioritet.

### <a name="discount-compound-behavior"></a>Rabattsammensatt virkemåte

Innstillingen **Rabattsammensatt virkemåte** fastsetter hvordan prissettingsmotoren beregner flere sammensatte rabatter.

Hvis parameteren er satt til **Sammensatt**, brukes én rabatt på en annen på en kumulativ måte. Hvis den er satt til **Sammensatt av den opprinnelige prisen**, behandles alle rabatter uavhengig av hverandre og brukes på samme opprinnelige pris.

La oss for eksempel si at du vil sette sammen to rabatter på 10 og 20 prosent for et produkt med en opprinnelig pris på USD 100. Hvis du setter parameteren **Rabattsammensatt virkemåte** til **Sammensatt**, blir den endelige prisen USD 72 (USD 100 &times; 90 % &times; 80 %). Hvis du setter den til **Sammensatt av den opprinnelige prisen**, blir den endelige prisen USD 70 (USD 100 – USD 10 – USD 20).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Aktiver konkurranse mellom eksklusiv terskel og andre periodiske rabatter

Hvis parameteren **Aktiver konkurranse mellom eksklusiv terskel og andre periodiske rabatter** er satt til **Ja**, gjør prissettingsmotoren at eksklusive terskelrabatter konkurrerer med eksklusive ikke-terskelrabatter. Prisingsprioritet gjelder fremdeles. Virkemåten til **beste pris**-terskelrabatter og **sammensatte** terskelrabatter endres ikke. De konkurrerer med andre ord ikke med ikke-terskelrabatter.

### <a name="manual-line-discount-and-system-discount"></a>Manuell linjerabatt og systemrabatt

Innstillingen **Manuell linjerabatt og systemrabatt** fastsetter hvordan prissettingsmotoren bruker en manuell linjerabatt og en systemrabatt på den samme linjen. Den manuelle linjerabatten kan settes sammen med systemrabatten eller den kan erstatte systemrabatten. Når den manuelle linjerabatten og systemrabatten settes sammen, tar beregningslogikken hensyn til innstillingen **Rabattsammensatt virkemåte**. En manuell sluttrabatt som gjelder for hele ordren, tar ikke hensyn til denne innstillingen.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Behold varer på samme salgslinje for rabattprisavrunding

Noen ganger kan ikke beløpet i et kvantumsrabattbeløp deles likt på det kvalifiserende antallet (for eksempel hvis rabattbeløpet er USD 10 for tre innkjøpte enheter). I disse tilfellene fastsetter innstillingen **Behold varer på samme salgslinje for rabattprisavrunding** hvordan prissettingsmotoren bruker og distribuerer rabattbeløpet. Hvis parameteren er satt til **Ja**, brukes rabattbeløpet i sin helhet og deles ikke opp. Hvis den er satt til **Nei**, deles rabattbeløpet på det kvalifiserende antallet og rundes av. Et rabattbeløp på USD 10 for tre enheter deles for eksempel opp i USD 3,33 for første enhet, USD 3,33 for andre enhet og USD 3,34 for tredje enhet.

### <a name="apply-discounts-to-key-in-price-products"></a>Bruk rabatter for tast inn pris-produkter

Innstillingen **Bruk rabatter for tast inn pris-produkter** avgjør om rabatter kan brukes sammen med «tast inn priser» som angis på salgsstedet. Innstillingen **Tast inn pris** i produktkonfigurasjonen avgjør om og hvordan et produkt støtter inntastingsprisen.

### <a name="apply-discounts-to-price-overrides"></a>Bruk rabatter for prisoverstyringer

Innstillingen **Bruk rabatter for prisoverstyringer** avgjør om rabatter kan brukes sammen med prisoverstyringer.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Distribuer rabatter for billigste rabatter

Når det gjelder samlerabatter som bruker beregningstypen Billigst, avgjør innstillingen **Distribuer rabatter for billigste rabatter** om prissettingsmotoren skal distribuere rabatten på tvers av linjer.

Hvis parameteren er satt til **Nei**, brukes rabatten bare på de billigste linjene. Hvis du for eksempel har en samlerabatt der du får én gratis hvis du kjøper to, er den billigste varen gratis, mens de to andre varene har full pris. En kunde som i dette tilfellet returnerer begge fullprisvarene, får likevel den tredje varen gratis. Dette scenarioet kan føre til tap for forhandleren.

Hvis parameteren er satt til **Ja**, distribuerer prissettingsmotoren rabatten på tvers av alle aktuelle linjer. Denne innstillingen kan bidra til å redusere tapet ved returer.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Beregn flerlinjepriser og -rabatter manuelt

Innstillingen **Beregn flerlinjepriser og -rabatter manuelt** styrer hvorvidt prissettingsmotoren bruker forsinket pris- og rabattberegning for salgsstedsprogrammet og telefonsenterkanalen. Hvis parameteren er satt til **Ja**, beregner ikke prissettingsmotoren samkjøpsrabatter (for eksempel kvantumsrabatter, terskelrabatter og samlerabatter) umiddelbart hver gang en salgsordre opprettes eller redigeres i salgsstedsprogrammet eller telefonsenterkanalen.

> [!NOTE]
> I Commerce versjon 10.0.30 og tidligere styrer innstillingen **Beregn flerlinjepriser og -rabatter manuelt** bare telefonsenterkanalen. Den separate innstillingen **Beregn flere varerabatter manuelt** i funksjonalitetsprofilen styrer virkemåten til prisberegningen i salgsstedsprogrammet. I Commerce versjon 10.0.31 konsolideres de to innstillingene til én innstilling på firmanivå.

### <a name="retention-period-in-days"></a>Bevaringsperiode i dager

Innstillingen **Bevaringsperiode i dager** angir hvor mange dager etter utløpsdatoen (hvis en utløpsdato er angitt) eller den deaktiverte datoen (hvis en utløpsdato ikke er angitt) en rabatt skal slettes systematisk. Hvis parameteren er satt til **0** (null), skjer ingen automatisk sletting.

> [!NOTE]
> I Commerce versjon 10.0.30 og tidligere kalles denne innstillingen **Antall dager som de utløpte rabattene skal slettes etter**.

### <a name="coupon-bar-code"></a>Kupongstrekkode

Innstillingen **Kupongstrekkode** fastsetter den bestemte strekkoden som skal brukes til å generere kupongstrekkoder. Brukere kan velge en av de forhåndsdefinerte strekkodene som er konfigurert på siden **Strekkodeoppsett**. Hvis du vil ha mer informasjon om strekkoder og strekkodemasker, kan du se [Definere strekkoder](set-up-bar-codes.md) og [Definere strekkodemasker](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kupongkoden må utlignes manuelt for å returnere transaksjoner

Innstillingen **Kupongkoden må utlignes manuelt for å returnere transaksjoner** gjelder bare for returtransaksjoner som det ikke er gitt salgskvittering for. Sett parameteren til **Nei** hvis kupongkoder skal brukes automatisk på transaksjonen. Sett den til **Ja** hvis kupongkoder må legges til i transaksjonen manuelt.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Bruk salgsavtaler definert for organisasjonen

Hvis parameteren **Bruk salgsavtaler definert for organisasjonen** er satt til **Ja** for bedrift-til-bedrift-ordrer (B2B), bruker prissettingsmotoren salgsavtalen som er definert for organisasjonen i brukerens kundehierarki, til å fastsette den kontraktbaserte prisen. Hvis parameteren er satt til **Nei** eller kundehierarkiet ikke er definert, leter prissettingsmotoren etter salgsavtaler som er definert for brukeren, for å fastsette den kontraktbaserte prisen. Hvis du vil ha mer informasjon om kundehierarkier for B2B-e-handel, kan du se [Administrere B2B-forretningspartnere ved hjelp av kundehierarkier](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Prissettingsinnstillinger på kanalnivå

Innstillingene nedenfor gjør at organisasjoner kan styre prissettingsvirkemåten i bestemte salgskanaler.

### <a name="enable-order-price-control"></a>Aktiver ordrepriskontroll

Du finner parameteren **Aktiver ordrepriskontroll** i hurtigfanen **Generelt** på siden **Konfigurasjon for telefonsenter**. Innstillingen avgjør om prissettingsmotoren fremtvinger en begrensning for prisoverstyringsoperasjonen i telefonsenterkanalen. Den fungerer sammen med innstillingen **Tillat prisjustering** på produktnivå.

Hvis ordrepriskontroll er deaktivert, kan alle telefonsenterbrukere foreta prisendringer på salgslinjer i telefonsenterkanalen, uavhengig av om tilsvarende produkter tillater prisjustering.

Hvis ordrepriskontroll er aktivert, er det bare produkter der parameteren **Tillat prisjustering** er satt til **Ja**, som tillater prisoverstyringer i salgsordrer for telefonsenterkanalen, og en årsakskode må oppgis på tilsvarende salgslinjer. En telefonsenterbruker kan bare endre salgsprisen opptil verdien for **Kostnadspåslagsprosent** som er definert i **Detaljhandel og handel \> Kanaloppsett \> Telefonsenteroppsett \> Overstyr tillatelser**. Hvis en prisoverstyring overskrider denne prosentsatsen, må brukeren sende inn en forespørsel, som deretter behandles via en forhåndsdefinert Commerce-arbeidsflyt for gjennomgang og godkjenning. Hvis du vil ha mer informasjon om hvordan du oppretter Commerce-arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Prissettingsinnstillinger på produktnivå

Følgende innstillinger fremtvinger prissettingsregler på produktnivået, og du finner innstillingene på siden **Produktkonfigurasjon** for organisasjonen.

### <a name="allow-price-adjust"></a>Tillat prisjustering

Hvis parameteren **Tillat prisjustering** er satt til **Ja**, kan en prisoverstyring brukes på produktet i salgsordrer for telefonsenterkanalen.

### <a name="key-in-price"></a>Tast inn pris

Innstillingen **Tast inn pris** avgjør om en inntastingspris er obligatorisk når et produkt legges til i en salgstransaksjon på salgsstedet. Den definerer også tilsvarende prisverdibegrensninger.

### <a name="zero-price-valid"></a>Nullpris gyldig

Innstillingen **Nullpris gyldig** avgjør om forhåndsdefinerte, systemberegnede eller manuelt justerte salgspriser for et produkt kan være 0 (null). Sett parameteren til **Ja** hvis en pris på null er tillatt. Denne innstillingen kan også angis på kategorinivået fra hierarkiet for handelsprodukt.

### <a name="prevent-all-discounts"></a>Hindre alle rabatter

Hvis du setter parameteren **Hindre alle rabatter** til **Ja**, forhindrer du at alle typer rabatter (inkludert manuelle rabatter) brukes på et produkt. Denne innstillingen kan også angis på kategorinivået fra hierarkiet for handelsprodukt.

> [!NOTE]
> Denne innstillingen begrenser ikke operasjonen for prisoverstyring, fordi den operasjonen angir basisprisen og behandles ikke som en rabatt.

### <a name="prevent-manual-discounts"></a>Hindre manuelle rabatter

Hvis du setter parameteren **Hindre manuelle rabatter** til **Ja**, forhindrer du at de manuelle linjerabattene eller transaksjonsrabattene brukes på et produkt. Alle andre rabatter kan fortsatt brukes. Denne innstillingen kan også angis på kategorinivået fra hierarkiet for handelsprodukt.

> [!NOTE]
> Denne innstillingen begrenser ikke operasjonen for prisoverstyring, fordi den operasjonen angir basisprisen og behandles ikke som en rabatt.

### <a name="prevent-retail-discounts"></a>Hindre detaljhandelsrabatter

Hvis parameteren **Hindre detaljhandelsrabatter** er satt til **Ja**, kan ikke rabattene **enkel**, **antall**, **terskel**, **samlerabatt** og **forsendelse** brukes på et produkt. Alle andre rabatter (inkludert manuelle rabatter) kan fortsatt brukes.

### <a name="prevent-tender-based-discounts"></a>Hindre rabatter basert på betalingsmiddel

Hvis parameteren **Hindre rabatter basert på betalingsmiddel** er satt til **Ja**, kan ikke en **betalingsmiddelbasert** rabatt brukes på et produkt. Alle andre rabatter (inkludert manuelle rabatter) kan fortsatt brukes.

Forhandlere velger ofte å utelate noen produkter, for eksempel nye varer eller varer med stor etterspørsel, fra varebaserte rabatter (for eksempel enkle rabatter og kvantumsrabatter). Hvis kunden betaler ved hjelp av det foretrukne betalingsmiddelet, kan det imidlertid likevel hende at de ønsker å bruke betalingsmiddelbaserte rabatter. Forhandlere kan oppnå dette resultatet ved å sette parameterne **Hindre alle rabatter** og **Hindre rabatter basert på betalingsmiddel** til **Nei** og parameterne **Hindre detaljhandelsrabatter** og **Hindre manuelle rabatter** til **Ja**.

## <a name="deprecated-or-removed-settings"></a>Avskrevne eller fjernede innstillinger

Følgende prissettingsinnstillinger er fjernet eller planlagt for fjerning fra Dynamics 365 Commerce.

| Innstilling | Årsak til avskrivning eller fjerning | Avskrivnings- eller fjerningsstatus |
|---------|-----------------------------------|-------------------------------|
| Håndtering av rabattoverlapping | Vi har lagt til denne innstillingen i Commerce-parametere for å styre hvordan prissettingsmotoren søker etter og fastsetter den beste rabattkombinasjonen. Alternativet **Beste rabatt** tvinger gjennom alle mulige rabattkombinasjoner under prisingsberegning. Alternativet **Beste ytelse** er et optimalisert alternativ som bruker en heuristisk algoritme og en marginal verdirangeringsmetode til å prioritere, evaluere og fastsette den beste rabattkombinasjonen til rett tid. Alternativet **Balansert beregning** i kodegrunnlaget fungerer på samme måten som **Best ytelse**. Derfor er det egentlig et duplisert alternativ. For å forbedre ytelsen blir prissettingsmotoren oppdatert slik at den bare bruker **Best ytelse** som standardalternativ. Derfor er ikke denne innstillingen lenger aktuell. | Avskrevet i versjon 10.0.21 og fjernes i oktober 2022. |
| Tillat prisjusteringer for å øke produktpris | Vi la til denne innstillingen for å styre hvorvidt prisjusteringsfunksjonen kan øke produktpriser. Hvis parameteren er deaktivert, kan organisasjoner bruke prisjusteringsfunksjonen bare til å angi en enhetspris for et produkt slik at den er lavere enn basisprisen og salgsprisen i forretningsavtalen. Vi avskrev denne innstillingen fordi prisjusteringsfunksjonen er oppdatert slik at det støtter toveisjusteringer (økning eller reduksjon) som standard. | Avskrevet i versjon 10.0.30 og fjernes i oktober 2023. |
| Aktiver prisrapport for detaljhandelsbutikk | Vi la til denne innstillingen for å styre hvorvidt funksjonen **Prisrapport** er tilgjengelig for bruk på siden for butikkonfigurasjon. Vi avskrev denne innstillingen fordi siden for butikkonfigurasjons er oppdatert slik at den alltid har **Prisrapport** som standardfunksjon. | Avskrevet i versjon 10.0.31 og fjernes i oktober 2023. |
| Bruk dagens dato til å beregne priser | Standard prismotor for Dynamics 365 Supply Chain Management støtter prisberegningen som er basert på den ønskede forsendelsesdatoen eller ønsket mottaksdato sammen med dagens dato. Commerce-prissettingsmotoren støtter bare prisingsberegning som er basert på dagens dato. For kunder som bruker både Supply Chain Management- og Commerce-funksjoner, la vi til denne innstillingen og anbefaler at kunder alltid setter den til **Ja**, slik at de to prissettingsmotorene kan fungere sammen. Vi avskrev denne innstillingen fordi den ikke fundamentalt endrer beregningsvirkemåten og er derfor overflødig. | Avskrevet i versjon 10.0.31 og fjernes i oktober 2023. |
| Maksimumspris | Vi la til denne innstillingen i funksjonalitetsprofilen for å styre hvorvidt bare produkter som har en salgspris som er under den angitte maksimumsprisen, kan selges via salgsstedet i bestemte butikker. Vi avskrev denne innstillingen på grunn av lav funksjonsbruk. | Avskrevet i versjon 10.0.31 og fjernes i oktober 2023. |
| Bruk rabatter for enhetspris | Denne innstillingen var ment å styre hvorvidt priser og rabatter skal rundes av på enhetsprisnivå eller salgslinjenivå under prisingsberegning. Vi avskrev den fordi den ikke brukes noe sted i det gjeldende kodegrunnlaget. | Avskrevet i versjon 10.0.31 og fjernes i oktober 2023. |
| Beregn flere varerabatter manuelt | Vi la til denne innstillingen for å styre hvorvidt prissettingsmotoren skal bruke forsinket prisberegning for detaljhandelsbutikkanalen. Hvis parameteren er satt til **Ja**, beregner ikke prissettingsmotoren samkjøpsrabatter (for eksempel kvantumsrabatter, terskelrabatter og samlerabatter) umiddelbart hver gang en salgsordre opprettes eller redigeres i salgsstedsprogrammet. Vi besluttet å konsolidere denne innstillingen med en lignende innstilling i Commerce-parametere for å lage en omnikanalkontroll. | Avskrevet i versjon 10.0.31 og fjernes i oktober 2023. |

Hvis du vil ha en fullstendig liste over fjernede eller avskrevne funksjoner i Dynamics 365 Commerce, kan du se [Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
