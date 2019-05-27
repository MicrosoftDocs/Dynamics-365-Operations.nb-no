---
title: Kalendere og hovedplanlegging
description: Dette emnet gir en oversikt over forsyningenkjedekalendere og hvordan de påvirker hovedplanlegging.
author: t-benebo
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: t-benebo
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 266eec2bb870be270b7796b35903a402e014c67c
ms.sourcegitcommit: 1f211ac6bd384fd8a2b5352104baf264d88f39b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538732"
---
# <a name="calendars-and-master-planning"></a>Kalendere og hovedplanlegging

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over forsyningenkjedekalendere og hvordan de påvirker hovedplanlegging.  Følgende forskjellige kalendere som brukes i hovedplanleggingsmotoren, forklares, inkludert hvordan de påvirker forsendelses- og mottaksdatoene i de planlagte ordrene. Til slutt gis det anbefalinger om tildeling, bruk og oppdatering av kalenderne.

## <a name="definition-of-a-calendar"></a>Definisjon av en kalender

Du kan definere en kalender til å bruke organisasjonen på siden i **Organisasjonsadministrasjon > Oppsett > Kalendere > Kalendere**. 

Hver datoregistrering i kalenderen kan være **åpne** eller **lukket** eller **basiskalender**. Dette er angitt i **Kontroll**-kolonnen på siden **Driftstider**. For hver dato: 
- **Åpne** - angir at arbeidet skal utføres på den valgte dagen. Kalenderen blir oppdatert i henhold til arbeidstidsmalen.
- **Lukket** - angir arbeidet som ikke utføres i løpet av dagen. 
- **Basiskalenderen** - angir at en bestemt dato vil arve arbeidstidene og åpnes/lukkes fra basiskalenderen. Derfor, når basiskalenderen oppdateres, vil den valgte kalenderen arve driftstider fra den. 

For lukkede datoer vil boksen **Lukket for plukk** automatisk være tilordnet. For åpne datoer kan du manuelt velge **Lukket for plukk**-alternativet. Dette angir at arbeidet skal utføres på datoen, men at levering ikke er utført. 

## <a name="calendars-that-affect-master-planning"></a>Kalendere som påvirker hovedplanlegging

### <a name="calendar-for-a-coverage-group"></a>Kalender for en dekningsgruppe
En dekningsgruppe angir et felles sett med parametere som brukes for etterfylling av varene som tilhører den angitte dekningsgruppen. 

For å legge til en kalender i en dekningsgruppe gå til **Hovedplanlegging > Oppsett > Dekning > Dekningsgrupper**. Finn dekningsgruppen som du vil tilordne kalenderen til, og merk av i **Kalender**-feltet.

Du kan tilordne dekningsgruppen på ulike sider: 
    - På siden **Detaljer om frigitt produkt** for et element. For å se dekningsgruppen for et element kan du gå til **Behandling av produktinformasjon > Produkter > Frigitte produkter** og velge varen for å gå til siden **Frigitt produktinformasjon**. Du kan se elementdekningsgruppen under hurtigkategorien **Planlegg**.
    - På siden **Varedekning**. I den frigitte produktinformasjonen klikk **Varedekning** for å gå til varedekningssiden. Du kan se forskjellige parametere for etterfylling, avhengig av området, lageret og produktdimensjonene i oversiktskategorien. Dekningsgruppen for hver vare arves fra dekningsgruppen på siden **Detaljer om frigitt produkt**. Dette kan overstyres ved å bruke **Bruk spesifikke innstillinger** eller **Overstyr gruppeinnstillinger** på **Generelt**-kategorien.
    - På siden **Parametere for hovedplanlegging**. Hvis en vare ikke har en dekningsgruppe angitt på den forrige siden, vil hovedplanlegging ta den generelle dekningsgruppen som er angitt i hovedplanleggingsparametere. Dette er definert i **Hovedplanlegging > Oppsett > Parametere for hovedplanlegging** i feltet **Generell dekningsgruppe**. 

### <a name="calendar-for-a-vendor"></a>Kalender for en leverandør
Hvis du vil angi virkedager for en leverandør, kan du tilordne en innkjøpskalender for leverandøren på siden **Bestillingsstandarder** for en leverandør. 

Hvis du vil angi en kalender for en leverandør, må du opprette kalenderen i **Organisasjonsadministrasjon > Kalendere > Kalendere**. Når kalenderen er opprettet, må du tilordne den til leverandøren. Gå til **Leverandører > Leverandører > Alle leverandører**, og velg leverandøren du vil tilordne kalenderen til. Deretter, på siden for leverandøren i hurtigkategorien **Bestillingsstandarder** tilordner du den nye innkjøpskalenderen ved hjelp av rullegardinmenyen. 

Kalenderen for en leverandør viser dagene de godtar plasseringen av bestillingen, og datoene når de kan levere ordrene til firmaet ditt. Derfor vil ordredatoer for innkjøpsordrer for leverandøren med en innkjøpskalender, bli datoer som er definert som åpne i kalenderen. Leveringsdatoene for disse ordrene vil også være i åpne dager, og derfor vil dette påvirke leveringstiden for den innkjøpte varen. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Definere leveringstiden for en innkjøpt vare

For å angi leveringstiden for innkjøp (og hvis bare virkedager skal tas med i betraktningen) for en vare, må du gå til siden for standard ordreinnstillinger for produktet, under **Behandling av produktinformasjon > Produkter > Frigitte produkter**, og velg **Standard ordreinnstillinger**. 

> [!Note]
> **Virkedager** under leveringstid for kjøp angir virkedager for leverandøren. En kalender for levering bare på tirsdager med leveringstid på 10 dager og boksen for virkedager merket, angir eksempelvis at det vil ta 10 uker (10 tirsdager) å levere varen.
Derfor vil det i de fleste tilfeller anbefales at det ikke velges virkedager for leveringstider for bestilling.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Definere leveringstider fra siden for forretningsavtale

Hovedplanlegging kan settes opp til å inkludere alle forretningsavtaler for leverandører. Forretningsavtaler er faste priser eller rabattavtaler som er definert for én eller flere kunder eller leverandører for salg eller kjøp av enkelte eller flere produkter. Gå til **Hovedplanlegging > Oppsett > Parametere for hovedplanlegging**, og i kategorien **Planlagte bestillinger** velg **Finn forretningsavtaler** for å inkludere forretningsavtalene ved planlegging. Hovedplanlegging kan velge leverandøren med **Minimum leveringstid** eller med **Laveste enhetspris**.

### <a name="calendar-for-a-warehouse"></a>Kalender for et lager
Du kan tilordne en kalender til et lager for å vise de åpne datoene for mottak og levering. Hvis ingen kalender er knyttet til et lager, antas det at den er åpen alle dager. 

> [!Note]
> Tilordning av en kalender til et transittlager har ingen innvirkning. Transittlagre brukes til å støtte overføringsordrer. De gjeldende forsendelses- eller mottaksdatoene for ordrene defineres av de åpne dagene i lageret "Fra" og "Til" og modusen for leveringskalenderen.

#### <a name="closed-for-pickup-policy"></a>Lukket for plukk-policy
Hvis du vil angi at et lager er åpent for mottak, men at plukking ikke er mulig, kan du bruke **Lukket for plukk-policyen** i lagerkalenderen. Dette gjelder også for kundehenting. 

### <a name="transport-calendar"></a>Transportkalender 
For å angi datoene som er tilgjengelige for forsendelsesoverføringsordrer fra et **Fra lager**, kan du tilordne en **Transportkalender**. Du kan definere en transportkalender per leveringsmåte eller per modus for levering og fra lager. Transportkalenderen er definert i **Salg og markedsføring > Oppsett > Distribusjon > Leveringsmåter**. Velg en leveringsmodus, og klikk på **Transportkalender**-knappen.

Du kan opprette en linje for hvert lager og hver leveringsmåte der kalenderen legges til kolonnen **Transportkalender**. Den angir transportkalenderen som vil bli brukt når varene sendes fra lageret med den angitte leveringsmåten. Hvis du vil bruke en transportkalender på alle forsendelser ved hjelp av en bestemt leveringsmåte, kan det bli opprettet en linje uten å angi lageret.  Den påvirker alle forsendelser som bruker den gitte leveringsmåten, uavhengig av lageret. 

Hvis ingen transportkalender er tilknyttet, antas det at alle dager er åpne for transport.

### <a name="calendar-for-a-customer"></a>Kalender for en kunde
For å angi datoene når en kunde kan motta leveringer, kan du tilordne en mottakskalender til kunden. Hvis ingen kalender er tilordnet til en kunde, antas det at kunden kan motta ordrer alle dager. Dette vil påvirke mottaksdatoen på salgsordrelinjene. Hvis du velger en dato i salgsordrelinjene som ikke er "åpen" i kundekalenderen, viser systemet at leveringsdatoen ikke er gyldig. 

Legg merke til at det er bare er mulig å inkludere én kalender per kunde. Hvis du vil inkludere en kalender for hver ulik adresse for en kunde, kan du opprette én kunde per adresse og deretter tilordne den aktuelle kalenderen. 

Den ønskede leveringsdatoen på salgsordrelinjene påvirkes av kundekalenderen og metoden for leveringsdatokontroll. Du kan lese mer om hvordan den tidligste leveringsdatoen beregnes, i [Ordrebekreftelse.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Leveringskalender for en juridisk enhet
For å angi datoene som en juridisk enhet kan sende varer, kan du definere en leveringskalender under **Organisasjonsstyring > Organisasjoner > Juridiske enheter**. Velg juridisk enhet, og legg til kalenderen i **Utenrikshandel og logistikk**-kategorien i **Leveringskalender**-feltet. Leveringskalenderen vil fungere som en kilde for standarder for alle lagerkalendere i den juridiske enheten. 

## <a name="how-calendars-affect-dates-in-planning"></a>Hvordan kalendere påvirker datoer i planleggingen

### <a name="order-date-of-a-planned-purchase-order"></a>Bestillingsdato for et bestillingsforslag 
Ordredatoen i et bestillingsforslag angir datoen da ordren ble plassert. Det vil være en åpen dato både i leverandørkalenderen og i dekningsgruppekalenderen. Noen ganger trenger leverandører noen dagers margin mellom når de mottar bestillingen, og når de kan sende varene. Disse datoene er angitt i leverandørens margindager. Men hvis den kjøpte varen tilordnes en dekningsgruppe med margindager, overstyrer disse margindagene leverandørens margindager.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Leveringsdato for et bestillingsforslag
Mottaksdatoen for et kjøp angir datoen du vil motta varene. Det vil være en åpen dato i kalenderen. Kalenderen som vil bli tatt hensyn til for å angi hvilke dager bestillingene kan mottas, er følgende, i rekkefølgen fra høyeste til laveste prioritet: 
    1. Leverandørens kalender
    2. Dekningsgruppekalender
    3. Lagerkalender for det mottakende lageret

Merk at dekningsgruppekalenderen kan angis på ulike sider og har følgende prioriteringsrekkefølge:
    1. Varedekningsgruppe på **Detaljer om frigitte produkter**-siden
    2. Varedekningsgruppe på **Varedekning**-siden
    3. Standard varedekningsgruppe i **Parametere for hovedplanlegging**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Forsendelsesdato for et overføringsforslag
Når du oppretter en overføringsordre mellom to lagre, er forsendelsesdatoen og mottaksdatoen inkludert i hodet for overføringsordren, sammen med "Fra"- og "Til"-lageret. Forskjellen mellom disse to datoene er forventet transporttid (i dager) mellom lagrene.

Forsendelsesdatoen for en planlagt overføringsordre angir datoen varene sendes fra lageret "Fra". Kalendere som brukes til å angi den tilgjengelige forsendelsesdatoen, vises etter prioritet: 
    1. Lagerkalenderen for "Fra"-lager
    2. Dekningsgruppekalender (se tilbakefallsordre for kalenderen ovenfor) Hvis det er angitt et lagerkalenderensett, vil forsendelsesdatoen være en åpen dato i kalenderen. Hvis det ikke er definert et lagerkalendersett, vil det ta dekningsgruppekalenderen. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Mottaksdato for et overføringsforslag
Mottaksdatoen for en overføringsordre angir datoen varene mottas i lageret "Til".

Kalendere som brukes til å angi den mottaksdato for de som vises etter prioritet: 
    1. Dekningsgruppekalender 
    2. Lagerkalenderen til "Til"-lageret Hvis det er et dekningskalendersett, vil mottaksdatoen være en åpen dato i kalenderen. Hvis det ikke er definert et dekningsgruppekalendersett, vil det ta lagerkalenderen. 

Når det letes etter forsendelses- og mottaksdatoer for den planlagte overføringen, vil marginene som er fastsatt av brukeren for forsendelse og mottak, også vurderes. 

## <a name="using-calendars-in-master-planning"></a>Bruke kalendere i hovedplanlegging

### <a name="assignment-of-scm-calendars"></a>Tilordning av SCM-kalender
Det er viktig å definere kalenderne for å identifisere virkedager i firmaet. Den beste implementeringen er å angi en kalender for hvert element med forskjellige virkedager. Med andre ord, alle eksterne kalendere (kunde, leverandør) og alle interne (lager, dekningsgruppe og leveringsmåten) som er knyttet til firmaet.

### <a name="recommendation-on-warehouse-calendars"></a>Anbefaling om lagerkalendere
Det anbefales å bruke én kalender per lager for å inkludere de spesifikke endringene som påvirker lageret. To eller flere lagre kan for eksempel ha samme virkedager, men en annen hentepolicy. I så fall er en kalender for hvert av lagrene med respektive hentepolicy beste implementering for systemet for å ta med de beste datoene for planlagte kjøps-, overførings- og produksjonsordrer. Hvis ingen lagerkalendere er angitt, kan juridisk enhet-kalenderen brukes som en kilde for standarder for lagerkalenderen. 

### <a name="recommendation-of-coverage-group-calendars"></a>Anbefaling for dekningsgruppekalendere
Når det gjelder dekningsgruppekalenderen, er det viktig å tenke på at den har en overstyrende virkemåte når det gjelder mottaksdatoer i hovedplanlegging. Derfor anbefales det å bruke den forsiktig. Spesielt er den nyttig når etterfylling må utføres på bestemte dager i uken. 

### <a name="updating-scm-related-calendars"></a>Oppdatere SCM knyttet til kalendere
Selv om det er viktig at alle relevante kalendere er tilordnet på sine respektive plasser (leverandør, kunde, lager, modus for levering eller dekningsgruppe), er det like viktig å oppdatere dem, slik at de gjenspeiler endringene. Systemet vil definere produksjon, overføring, innkjøp og salgsordredatoer avhengig av kombinasjonen av de tilordnede kalenderne. Det er lurt å avklare hvem som har ansvaret for å tildele og oppdatere kalenderne på de tilsvarende områder. Hvis det oppstår en nedbryting eller annen uvanlig endring i arbeidsdagene, er det viktig å oppdatere kalenderne i henhold til den. Alle aktiviteter som er avhengige av kalendere, for eksempel hovedplanlegging og produksjonsplanlegging, må kjøres på nytt når kalendere oppdateres. 
