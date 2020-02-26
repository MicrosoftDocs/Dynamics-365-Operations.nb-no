---
title: Prisstyring av detaljsalg
description: Dette emnet beskriver begrepene for å opprette og administrere salgspriser i Dynamics 365 Commerce.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f3f2616fd98b37576625d9586a1cda29ce1b89f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023594"
---
# <a name="retail-sales-price-management"></a>Salgsprisbehandling for Retail

[!include [banner](includes/banner.md)]

Dette emnet inneholder informasjon om prosessen med å opprette og administrere salgspriser i Dynamics 365 Commerce. Det fokuserer på begrepene som er involvert i denne prosessen, og viser virkningen av konfigurasjonsalternativene for salgspriser.

## <a name="terminology"></a>Terminologi

Følgende termer brukes i dette emnet.

| Semester | Definisjonen, bruk og merknader |
|---|---|
| Pris | Enhetsbeløpet som et produkt selges for i en salgsstedsklient eller på en salgsordre. I dette emnet refererer begrepet *pris* alltid til salgsprisen, ikke lagerprisen eller kostprisen. |
| Basispris | Prisen som er angitt i **Pris**-feltet for et frigitt produkt. |
| Pris for forretningsavtale | Prisen som er angitt på et produkt eller en variant ved hjelp av en forretningsavtale av typen **Pris (salg)**. |
| Beste pris | Når mer enn én pris eller rabatt kan brukes på et produkt, det minste prisbeløpet og/eller det største rabattbeløpet som gir lavest mulig nettobeløpet som kunden må betale. I dette emnet kalles begrepet beste pris alltid "beste pris." Den beste prisen er forskjellig fra, og bør ikke forveksles med **Beste pris**-opplistingsverdien for en rabatts samtidighetsmodus. |

## <a name="price-groups"></a>Prisgrupper

Prisgrupper er kjernen i pris- og rabattstyring i Commerce. Prisgrupper brukes til å tilordne priser og rabatter til detaljhandelsenheter (dvs. kanaler, kataloger og fordelsprogrammer). Siden prisgrupper brukes for all prissetting og alle rabatter, er det svært viktig at du planlegger hvordan du skal bruke dem før du begynner.

En prisgruppe er bare et navn, en beskrivelse, og eventuelt en prissettingsprioritet. Det viktigste å huske om prisgrupper er at de brukes til å behandle mange-til-mange-relasjoner som rabatter og priser har med detaljhandelsenheter.

Illustrasjonen nedenfor viser hvordan prisgrupper brukes. I denne illustrasjonen ser du at "Prisgruppe" bokstavelig talt er i sentrum av pris- og rabattstyring. Detaljhandelsenhetene som du kan bruke til å administrere differensielle priser og rabatter, vises til venstre, og de faktiske pris- og rabattpostene er til høyre.

![Prisgrupper](./media/PriceGroups.png "Prisgrupper")

Når du oppretter prisgrupper, bør du ikke bruke en enkelt prisgruppe for flere typer enheter for detaljhandel. Hvis ikke kan det være vanskelig å finne ut hvorfor en bestemt pris eller rabatt blir brukt på en transaksjon.

Som den røde stiplede linjen i illustrasjonen viser, støtter Commerce hovedfunksjonaliteten til Microsoft Dynamics 365 for en prisgruppe som er angitt direkte for en kunde. I dette tilfellet får du imidlertid bare salgsprisforretningsavtaler. Hvis du vil bruke kundespesifikke priser, anbefaler vi at du ikke definere prisgrupper direkte for kunden. I stedet bør du bruke tilknytninger.

De følgende delene gir mer informasjon om detaljhandelsenhetene som du kan bruke til å angi ulike priser når prisgruppene brukes. Konfigurasjonen av priser og rabatter for alle disse enhetene gjøres i to trinn. Denne fremgangsmåten kan utføres i begge rekkefølger. Den logiske rekkefølgen er imidlertid å definere prisgruppene på enhetene først, fordi dette er sannsynligvis et engangs oppsett som utføres under implementering. Deretter, når priser og rabatter opprettes, kan du angi prisgruppene på disse prisene og rabattene individuelt.

### <a name="channels"></a>Kanaler

I detaljhandelen er det svært vanlig å ha ulike priser i forskjellige kanaler. To primære faktorer som påvirker kanalspesifikke priser, er kostnader og lokale markedsforhold.

- **Kostnader** – Jo lengre unna en kanal er fra produktkilden, jo mer det koster det å lagre et produkt. Ferskvare har for eksempel en begrenset holdbarhet og bestemte produksjonskrav (for eksempel en vekstsesong). Om vinteren koster fersk salat sannsynlig mer i nordlige klimaer enn i sørlige klimaer. Hvis du angir priser for kanaler over et stort geografisk område, vil du sannsynligvis angi ulike priser i forskjellige kanaler.
- **Lokale markedsforhold** – en butikk som har en direkte konkurrent rett over gaten, vil være mye mer prisbevisst enn en butikk som ikke har en direkte konkurrent i nærheten.

### <a name="affiliations"></a>Tilknytninger

Den generelle definisjonen av en tilknytning er en kobling til eller tilknytning til en gruppe. I Commerce er tilknytninger grupper av kunder. Tilknytninger er et mye mer fleksibelt verktøy for prissetting og rabatter enn kjernekonseptet for kunde- og rabattgrupper i Microsoft Dynamics 365. Først kan en tilknytning brukes for både priser og rabatter, mens prissetting for ikke-detaljhandel har en annen gruppe for hver type rabatt og pris. Deretter kan en kunde tilhøre flere tilknytninger, men kan bare tilhøre én prisgruppe som ikke gjelder for detaljhandel, for hver type. Til slutt, selv om tilknytninger kan settes opp slik at de er koblet til en kunde, trenger de ikke det. En ad hoc-tilknytning kan brukes for anonyme kunder på salgsstedet. Et typisk eksempel på en anonym tilknytningsrabatt er senior- eller studentrabatt, der en kunde kan motta en rabatt bare ved vise et kort for gruppemedlemskap.

Selv om tilknytninger oftest er tilknyttet rabatter, kan du også bruke dem til å angi differensiell prising. Når en forhandler selger til en ansatt, kan det for eksempel hende at du vil endre salgsprisen i stedet for å bruke en rabatt på toppen av den vanlige prisen. Som et annet eksempel kan en forhandler som selger til både forbrukerkunder og bedriftskunder, tilby bedriftskunder bedre priser, basert på deres innkjøpsvolum. Tilknytninger muliggjør begge disse scenariene.

### <a name="loyalty-programs"></a>Fordelsprogrammer

Fordelsprogrammer er vanligvis bare en tilknytning som har et eget navn i forhold til priser og rabatter. Både priser og rabatter kan angis for et fordelsprogram, på samme måte som de kan angis for en tilknytning. Hvordan kunder mottar fordelspriser under en transaksjon eller en ordre, er imidlertid forskjellig fra hvordan de får tilknytningsprising. Kunder kan bare få fordelspriser hvis et fordelskort legges til en transaksjon. Når et fordelskort er lagt til en transaksjon, legges også fordelsprogrammet til. Fordelsprogrammet gir deretter spesialpriser og -rabatter.

Fordelsprogrammer kan ha flere nivåer, og rabattene kan være forskjellig for ulike lag. På denne måten kan forhandlere gi hyppige kunder større fordeler uten å plassere disse kundene manuelt i en spesialgruppe.

Fordelsprogrammer har flere funksjoner enn priser og rabatter. Når det gjelder prissetting og rabatter, er de imidlertid det samme som tilknytninger.

### <a name="catalogs"></a>Kataloger

Noen forhandlerne bruker fysiske eller virtuelle kataloger til å markedsføre produkter til, og prise dem for, fokuserte grupper av kunder. Som en del av sin forretningsmodell for å målrette markedsføring via en katalog, kan disse forhandlerne definere differensielle priser på de ulike katalogene. Microsoft Dynamics 365 støtter denne funksjonen ved at du kan definere katalogspesifikke rabatter og priser, på samme måte som du kan definere kanalspesifikke eller tilknytningsspesifikke rabatter. Når du redigerer en katalog, kan du knytte prisgrupper til katalogen, på samme måte som du kan knytte dem til en kanal, tilknytning eller fordelsprogrammet.

### <a name="best-practices-for-price-groups"></a>Gode fremgangsmåter for prisgrupper

Ikke bruk en prisgruppe for flere enhetstyper for detaljhandel. I stedet bruker du ett sett med prisgrupper for kanaler, et annet sett med prisgrupper for tilknytninger eller fordelsprogrammer, og så videre. Du kan bruke et prefiks eller suffiks i navnet på prisgruppen for å gruppere forskjellige typer prisgrupper du bruker, visuelt.

Unngå å definere prisgrupper direkte for en kunde. I stedet bruker du en tilknytning. På denne måten kan du tilordne alle typer priser og rabatter til kunder, ikke bare salgsprisforretningsavtaler.

## <a name="pricing-priority"></a>Prisingsprioritet

En prisingsprioritet alene er bare et tall og en beskrivelse. Prisingsprioriteter kan brukes på prisgrupper, eller de kan brukes direkte på rabatter. Når prisingsprioriteter blir brukt, kan en forhandler overstyre prinsippet om beste pris ved å kontrollere rekkefølgen som priser og rabatter brukes i for produkter. Et større nummer for prisingsprioritet evalueres før et lavere nummer for prisingsprioritet. I tillegg, hvis det finnes en pris eller rabatt med et hvilket som helst prioritetsnummer, ignoreres alle priser eller rabatter som har lavere prioritetstall.

Pris og rabatt kan komme fra to forskjellige prisingsprioriteter fordi prisingsprioriteter gjelder uavhengig for priser og rabatter.

Hvis du vil bruke prisingsprioritet for priser, må du tilordne en prisingsprioritet til en prisgruppe og deretter opprette en forretningsavtale for salgspris for denne prisgruppen.

Funksjonen for prisingsprioritet ble innført for å støtte scenariet der en forhandler ønsker å bruke høyere priser i et bestemt sett med butikker. En forhandler har for eksempel definert regionale priser for østkysten av USA, men ønsker høyere priser for enkelte produkter i New York City-butikker, fordi det koster mer å selge enkelte produkter i byen og/eller fordi det lokale markedet vil bære en høyere pris.

Som beskrevet i delen "Beste pris" i dette emnet, velger prissettingsmotoren for detaljhandel vanligvis den laveste av to priser. Derfor kan forhandleren vanligvis ikke bruke den høyeste av to priser i en butikk som inneholder prisgrupper for både østkysten og New York. For å løse dette problemet før funksjonen for prisingsprioritet ble innført, måtte forhandleren definere priser for hvert produkt to ganger og ikke tilordne begge prisgrupper. Alternativt måtte forhandleren opprette ekstra prisgrupper for å isolere produktene som har høyere priser fra produkter som har de vanlige, lavere prisene.

Med funksjonen for prisingsprioritet kan forhandleren imidlertid opprette en prisingsprioritet for butikkpriser som er høyere enn prisingsprioriteten for regionale priser. Forhandleren kan eventuelt opprette en prisingsprioritet bare for butikkpriser og holde regionale priser på standard prisingsprioritet, som er 0 (null). Begge oppsettene bidrar til å sikre at butikkpriser alltid brukes før regionale priser.

### <a name="pricing-priority-example"></a>Eksempel på prisingsprioritet

La oss se på et eksempel, der butikkpriser overstyrer andre priser.

En nasjonal forhandler fastsetter de fleste priser per område, og det har fire områder: Nord-øst, Sør-øst, Midt-vest og Vest. Det har identifisert flere høykostnadsmarkeder som støtter høyere priser. Disse markedene er i New York City, Chicago og San Francisco Bay-området.

I dette eksemplet skal vi gå nedover til Nord-øst-regionen. Butikk 1 er i Boston, og butikk 2 er i Manhattan. For Boston-butikken er to prisgrupper koblet til kanalen: Nord-øst og butikk 1. For Manhattan-butikken er tre prisgrupper koblet til kanalen: Nord-øst, NYC og butikk 2.

Forhandleren definerer to prisingsprioriteter: Høy kostnad har prioritetsnummer 5, og butikkpriser har prioritetsnummer 10. (Husk at prisingsprioritet som standard er 0 \[null\], og en pris eller rabatt som har et høyere prioritetsnummer, brukes før en pris eller rabatt som har et lavere prioritetsnummer.) For Nordøst-prisgruppen beholdes prisingsprioriteten på standardverdien **0** (null). For prisgruppen NYC er prisingsprioriteten satt til **5**, fordi New York City er et høykostnadsmarked. For prisgruppene Butikk 1 og Butikk 2 er prisingsprioriteten satt til **10**.

To produkter som forhandleren selger, er produkt 1, t-skjorte, og produkt 2, merkespesifikke dongeribukser.

| Produkt | Nordøst-pris | NYC-pris | Butikkpris |
|---|---|---|---|
| T-skjorte | USD 15 | Ikke angitt | Ikke angitt |
| Dongeribukser | USD 50 | USD 70 | Ikke angitt |

T-skjorten selger til samme pris (det vil si USD 15) i både Boston- og Manhattan-butikkene, fordi bare én pris er angitt i Nord-øst-prisgruppen som er koblet til begge kanaler. Dongeribuksene selger for USD 50 i Boston-butikken, fordi denne prisen er den eneste prisen som er tilgjengelig i denne butikken. To priser er imidlertid tilgjengelige i Manhattan-butikken: USD 50 og USD 70. Siden prisingsprioriteten 5 for prisgruppen NYC er høyere enn prisingsprioriteten 0 (null) for prisgruppen Nordøst, angis prisen som USD 70 i POS-systemet.

> [!NOTE]
> For hver prisingsprioritet kreves en full gjennomgang av logikken for prissettingsmotoren for detaljhandel. For å opprettholde ytelsen til pris- og rabattberegningen, bør du derfor bruke prisingsprioriteter forsiktig.

## <a name="types-of-prices"></a>Typer priser

I Microsoft Dynamics 365 kan du angi prisen på et produkt på tre steder:

- Direkte på produktet (basisprisen)
- I en forretningsavtale for salgspris
- I en prisjustering

Basisprisen og forretningsavtaleprisen er en del av kjernen i Dynamics 365 og er tilgjengelige selv om du ikke bruker Commerce. Funksjonen for prisjustering er bare tilgjengelig i Commerce. Neste del inneholder mer informasjon om hvert av disse alternativene for å angi priser, og forklarer hvordan alternativene fungerer sammen.

## <a name="setting-prices"></a>Angi priser

### <a name="base-price"></a>Basispris

Det er enklest å definere prisen for en vare direkte i produktet. Verdien du angir direkte på et produkt, kalles ofte basisprisen for produktet. Du angir basisprisen i **Pris**-feltet i **Selg**-kategorien på siden **Detaljer om frigitt produkt**. Verdien du angir, er i firmavaluta. Som standard er prisen for et antall på 1 for måleenheten som er angitt i **Enhet**-feltet i **Selg**-kategorien. Den faktiske prisen per enhet av et produkt er basert på måleenheten, prisantallet og valutaen.

Hvis et produkt har én pris for alle, tilbyr basisprisen den mest effektive måten å behandle prisen på produktet på. Selv om du bruker forretningsavtaler til å angi priser, kan du også angi basisprisen på et produkt. Hvis du ikke bruker en forretningsavtale av typen **Alle**, har du en tilbakefallspris som brukes når ingen forretningsavtale gjelder.

Hvis valutaene for en detaljhandelkanal er forskjellig fra firmaets valuta, bestemmes basisprisen i kanalen ved hjelp av valutaomregning for prisen som er angitt for produktet.

Selv om prisenheten ikke er et vanlig scenario, støtter prissettingsmotoren den. Hvis prisenheten er satt til en annen verdi enn **0** (null), er prisen per enhet lik pris ÷ prisenhet. Hvis et produkt for eksempel er USD 10,00 og prisenheten er 50, er prisen for et antall på 1 USD 0,20 (= USD 10,00 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Forretningsavtale for salgspris

Ved å bruke journal for forretningsavtaler kan du opprette forretningsavtaler for salgspris for hvert produkt. I Microsoft Dynamics 365 finnes det tre kundeområder for forretningsavtaler for salgspris: **Tabell**, **Gruppe** og **Alle**. Kundeområdet avgjør hvilke kunder en bestemt salgsprisforretningsavtale gjelder for.

En salgsprisforretningsavtale av typen **Tabell** er for en enkelt kunde som er angitt direkte i forretningsavtalen. Denne situasjonen er ikke et vanlig firma-til-kunde (B2C)-scenario. Men hvis det oppstår, bruker prissettingsmotoren **Tabell**-forretningsavtaler når den fastsetter prisen.

En salgsprisforretningsavtale av typen **Gruppe** er typen som brukes oftest med detaljhandelsfunksjonalitet. Utenfor Commerce er salgsprisforretningsavtaler av typen **Gruppe** for en enkelt kundegruppe. I Commerce er imidlertid begrepet for en kundegruppe utvidet slik at det er en mer generell prisgruppe. En prisgruppe kan kobles til en kanal, en tilknytning, et fordelsprogram eller en katalog. Hvis du vil ha detaljert informasjon om prisgrupper, kan du se delen "Prisgrupper" tidligere i dette emnet.

> [!NOTE]
> En forretningsavtalepris brukes alltid før basisprisen.

### <a name="price-adjustment"></a>Prisjustering

Som navnet tilsier, brukes en prisjustering til å endre prisen som enten ble satt direkte på produktet eller ved hjelp av en forretningsavtale. En prisjustering kan bare brukes til å redusere prisen, ikke heve den. En prisjustering er den anbefalte metoden for forhandler å opprette, spore og administrere prisavslag for sine produkter over tid.

Det finnes tre typer prisjusteringer: prosent rabatt, beløp rabatt av og pris. En prisjustering for typen prosent rabatt eller beløp rabatt brukes alltid på en salgstransaksjon. En prisjustering av pristypen brukes imidlertid bare hvis den justerte prisen er mindre enn prisen som ble angitt ved hjelp av basisprisen eller forretningsavtaleprisen. Hvis prisen som er angitt i en prisjustering, er større enn den ujusterte prisen, brukes derfor ikke prisjusteringen.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Bestemme prisen for et produkt i en transaksjon

Beregningen av pris og rabatt på en transaksjon bruker prinsippet for å finne den beste prisen for kunden. I henhold til dette prinsippet brukes den laveste prisen hvis det finnes mer enn én pris. I tillegg brukes kombinasjonen av rabatter som gir det største rabattbeløpet for hele transaksjonen. I noen tilfeller må mindre rabatt brukes på ett enkelt produkt, slik at flere rabatter kan brukes på andre produkter i transaksjonen.

Det eneste unntaket til prinsippet med å finne den beste prisen for kunden er et alternativ for samlerabatt med minst kostbare rabatter. Dette alternativet gir minst kostbare rabatter som favoriserer forhandleren når produkter er valgt og gruppert. Når en transaksjon inneholder flere varer enn det som kreves for å oppnå den minst kostbare rabatten, velger prissettingsmotoren produktene som gir minste mulige rabattbeløp for kunden.

Prissettingsmotoren returnerer tre priser for hvert produkt: basisprisen, forretningsavtaleprisen og den aktive prisen.

Basisprisen er bare egenskapen for produktet og er den samme for alle overalt.

Hvis alternativet **Finn neste** er satt til **Ja** i salgsprisforretningsavtalen, brukes den laveste prisen som blir funnet for gjeldende salgsprisforretningsavtaler, som forretningsavtaleprisen. Du finner forretningsavtaler ved å bruke prisgrupper eller **ALLE**-kontokoden. Forretningsavtalene kan også tilordnes direkte til en kunde. Hvis alternativet **Finn neste** er satt til **Ingen**, brukes den første forretningsavtaleprisen som blir funnet. Hvis ingen salgsprisforretningsavtaler blir funnet, settes forretningsavtaleprisen lik basisprisen.

Den aktive prisen beregnes ved å ta forretningsavtaleprisen og bruke den største prisjusteringen som gjelder for produktet. Hvis ingen prisjusteringer blir funnet, eller hvis den beregnede aktive prisen er større enn forretningsavtaleprisen, settes den aktive prisen lik forretningsavtaleprisen. Husk at du ikke kan øke prisen på et produkt ved hjelp av en prisjustering. Du finner de aktuelle prisjusteringene bare ved å bruke prisgrupper som er tilordnet til en kanal, katalog, tilknytning eller fordelskortprogrammet.

## <a name="category-price-rules"></a>Kategoriprisregler

Kategoriprisregler-funksjonen i Commerce gir deg en enkel måte å opprette nye forretningsavtaler for alle produktene i en kategori. Med denne funksjonen kan du også automatisk finne eksisterende forretningsavtaler for produkter i kategorien, og la dem utløpe.

Når du velger alternativet for å la eksisterende forretningsavtaler utløpe, oppretter systemet en ny forretningsavtalejournal for produkter i kategorien som har en aktiv forretningsavtale. Journalen må imidlertid posteres manuelt. Kategoriprisreglene kan bare finne eksisterende forretningsavtaler hvis du vil bruke den samme prisregelen (det vil si hvis du oppretter en ny prisregel som bruker den samme kategorien som var før). Hvis du ikke bruker den samme prisregelen, vil ikke de eksisterende forretningsavtalene bli utløpt.

Prisene kan økes eller reduseres ved hjelp av feltene **Prisregel** og **Prisgrunnlag** for kategoriprisreglene.

- Velg typen prisendring du vil bruke, i feltet **Prisregel**:

    - **Påslag** –En prosent av prisen grunnlag brukes til å beregne salgsprisen. Eksempel: Et produkt som koster 10,00 og selges for 15,00,, har et påslag på 50 prosent.
    - **Margin** – En prosent av salgsprisen som brukes til å beregne fortjenestebeløpet. Eksempel: Et produkt som koster 10,00 og selges for 15,00 har en fast margin på 33,3 prosent.
    - **Fast beløp** – Et beløp som legges til prisgrunnlaget som brukes til å beregne salgsprisen. Eksempel: Et produkt som koster 10,00 og selges for 15,00 har et fast beløp på 5,00.

- Velg pristypen du vil endre, i **Prisgrunnlag**-feltet:

    - **Basiskost** – Beløpet som forhandleren betalte til leverandøren.
    - **Basispris** – Salgsprisen før forretningsavtaler og prisjusteringer brukes.
    - **Gjeldende pris** – Salgsprisen etter forretningsavtaler og prisjusteringer brukes.

Du kan bruke de ekstra produktkategoriene sammen med kategoriprisreglene for enkelt å oppdatere priser for forskjellige produkter fra ulike produktkategorier.

## <a name="best-practices"></a>Anbefalte fremgangsmåter

Microsoft SQL Server Express brukes ofte til kanaldatabaser på grunn av kostnaden (gratis). Husk at SQL Server Express har maskinvarebegrensninger og begrensninger på datastørrelsen. Hvis du ikke planlegger på riktig måte, kan du raskt nå datastørrelsesgrensene for SQL Server Express. Denne vurderingen gjelder ikke bare for prising, men også for andre deler av produktet. Her følger noen nyttige tips som kan hjelpe deg med å redusere størrelsen på dataene:

- Hvis du bruker forretningsavtaler, og prisene endres, bør du la de gamle forretningsavtalene utløpe ved å angi en sluttdato. Over tid bidrar dette til å redusere antallet forretningsavtaler som holdes i kanaldatabaser. Den hjelper også å redusere mengden data som prisberegningsalgoritmen må arbeide med.
- Hvis prisene varierer etter produktvariant, kan du vurdere å bruke produktbasisprisen som prisen på den mest brukte varianten. Deretter kan du bruke forretningsavtaler bare for variantprisene som er unntak. Denne fremgangsmåten reduserer antall handelsavtaleposter. Ettersom det er så enkelt å importere data til Microsoft Dynamics 365, kan du bli fristet til å importere en forretningsavtale for hver variant av hver vare. Denne fremgangsmåten kan imidlertid gi mange forretningsavtaler som har samme verdi. Det kan derfor unødvendig øke størrelsen på dataene.
- Commerce behandler variant-spesifikke priser i rekkefølge fra mest spesifikke til minst spesifikke. Hvis en produktdimensjon ikke påvirker prisen, trenger du ikke definere forretningsavtaler for den. Hvis for eksempel et produkt er tilgjengelig i tre farger og fire størrelser, men prisen bare varierer etter størrelse. Hvis du definerer en forretningsavtale for hver variant, oppretter du 12 poster. I stedet kan du definere en forretningsavtale for hver størrelse og la fargedimensjonen stå tom. I dette tilfellet oppretter du bare fire poster.

    Hvis ikke alle verdier for en dimensjon gir en annen pris, kan du også definere en forretningsavtale for produktstandarden og la alle produktdimensjoner stå tomme. Deretter definerer du en egen forretningsavtale for hver dimensjonsverdi som fører til en annen pris. Hvis for eksempel størrelsen XXL har en høyere pris, men alle andre størrelser har samme pris, trenger du bare to forretningsavtaler: én for produktstandarden og én for størrelsen XXL.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Priser inkludert mva i forhold til salgspriser eksklusive mva

Når du angir salgspriser i Dynamics 365, angir du ikke om prisverdien er inklusiv eller eksklusiv mva. Verdien er bare prisen. Med innstillingen **Pris inkluderer merverdiavgift** for detaljhandelskanaler kan du imidlertid konfigurere kanaler slik at de inkluderer eller ekskluderer mva fra priser. Denne innstillingen er angitt på kanalen, og kan endres også i et enkelt firma.

Hvis du arbeider med både inklusive og eksklusive typer mva, er det svært viktig at du setter priser riktig, fordi totalbeløpet som kunden betaler, endres hvis innstillingen **Pris inkluderer merverdiavgift** på kanalen endres.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Forskjeller mellom prissetting for detaljhandel og prissetting for ikke-detaljehandel

En enkelt prissettingsmotor brukes til å beregne priser på tvers av alle kanaler: Telefonsenter, Detaljhandelbutikk og Nettbutikker. Dette bidrar til å muliggjøre enhetlig handel.

Prissetting for detaljhandel er utformet for å fungere med detaljhandelsenheter i stedet for enheter som ikke gjelder for detaljhandel. Det er spesielt utformet for å angi priser per butikk, ikke etter lager.

Prissettingsmotoren **støtter ikke** følgende prissettingsfunksjoner:

- Angivelse av priser etter lagringsdimensjoner for område eller område og lager støttes ikke. Hvis du bare angir områdedimensjonen i forretningsavtalene, ignorerer prissettingen for detaljhandel området og bruker forretningsavtalen på alle områder. Hvis du angir både område og lager, er virkemåten udefinert/ikke testet fordi det forventes at forhandlere bruker butikkprisgruppene til å kontrollere prisene for hver butikk/lager.
- Attributtbasert prissetting støttes ikke.
- Leverandørrabatt-overføring støttes ikke.

I tillegg støtter **bare** prissettingsmotoren for detaljhandel følgende prissettingsfunksjoner:

- Prisen er basert på produktdimensjoner, i rekkefølge fra den mest spesifikke variantprisen til minst spesifikke variantprisen til produktstandardprisen. En pris som er angitt ved hjelp av to produktdimensjoner (for eksempel farge og størrelse), brukes før en pris som angis ved hjelp av bare én produktdimensjon (for eksempel størrelse).
- Samme prisgruppe kan brukes til å kontrollere priser og rabatter.

## <a name="pricing-api-enhancements"></a>API-forbedringer for prising

Pris er en av de viktigste faktorene som styrer kjøpsavgjørelsene for mange kunder, og mange kunder sammenligner priser på ulike områder før de gjør et kjøp. For å bidra til å sikre at de gir konkurransedyktige priser, følger forhandleren nøye med på konkurrentene og utfører ofte kampanjer. For å hjelpe disse forhandlerne med å tiltrekke seg kunder, er det svært viktig at produktsøket, bla gjennom-funksjonen, listene og produktlister-siden viser de mest nøyaktige prisene.

I en kommende frigivelse av Commerce vil API-et for **GetActivePrices** returnere priser som inkluderer enkle rabatter (for eksempel rabatter som ikke er avhengige av andre varer i handlekurven). På denne måten er prisene som vises, nær det faktiske beløpet kundene skal betale for varer. Denne API-en inneholder alle typer enkle rabatter: tilknytningsbaserte, lojalitetsbaserte, katalogbaserte og kanalbaserte rabatter. I tillegg vil API-en returnere navnene og gyldighetsinformasjonen for de brukte rabattene, slik at forhandlerne kan gi en mer detaljert beskrivelse av prisen og skape en følelse av viktighet hvis rabattgyldigheten utløper snart.
