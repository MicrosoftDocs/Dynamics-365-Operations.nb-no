---
title: Administrer utsetting arbeid i produksjon
description: "Dette emnet forklarer hvordan underleveranseoperasjoner skal behandles i Microsoft Dynamics 365 for Finance and Operations. Med andre ord, forklarer det hvordan produksjonsoperasjoner som er tildelt en ressurs er styrt av en leverandør."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 26feea4d86cf8b976f41342c8543594593c4b135
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="manage-subcontracting-work-in-production"></a>Administrer utsetting arbeid i produksjon

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan underleveranseoperasjoner skal behandles i Microsoft Dynamics 365 for Finance and Operations. Med andre ord, forklarer det hvordan produksjonsoperasjoner som er tildelt en ressurs er styrt av en leverandør.

I [produksjonsprosesser](production-process-overview.md), arbeidet kan gjøres av ressurser som eies eller administreres av leverandører. Leverandør ressurser brukes vanligvis til nivå periodiske overflødige behovet som bruke enn de som den disponible kapasiteten i et firma eier ressurser. Leverandøren vil kanskje også kunne tilby spesifikke [ressursfunksjoner](resource-capabilities.md) eller ressurser til en lavere pris.  

Avhengig av leverandør-ressurser som brukes i produksjonsprosessen, en [rute](routes-operations.md) har ofte flere logistikkrav, fordi materialet og halvferdige varer må først transporteres til leverandørens webområde. Resultatet av operasjonen underleveranse må deretter transporteres til lokasjonen som er tildelt til neste operasjon eller et lager for ferdige varer.  

Når utsetting operasjoner eller aktiviteter, kan de påvirke alle faser av operasjoner fra definisjonen av operasjonene som kreves i produksjonen, etterkalkulering, prognoser, planlegging og planlegging for administrasjon av logistikk for materialer, halvferdige varer og ferdigvarer. Til slutt krever disse ressursene sine egne prosesser for regnskap og kostnadskontroll.  

For interne ressurser fordeles vanligvis en fast kostnadssats for en periode. Derimot er kostnaden for underleveranse ressurser basert på kjøpsprisen for den tilknyttede tjenesten. Tjenesten er definert som et annet produkt, og brukes til å drive innkjøp og kjøpe prosesser for underleveranse behandlingshastigheten.  

Det er for øyeblikket ingen eksplisitte begrepet halvferdige produkter i Microsoft Dynamics 365 for Finance and Operations. For en produksjonsordre som krever mer enn én operasjon for å transformere råvarer til en ferdig vare, posteres den ferdige varen tilbake på lageret bare i den siste operasjonen. De halvferdige produktene som tidligere operasjoner produserer, er etterkalkulert i varer i arbeid (via), men de ikke bokført eller registrert på lager. Selv om du kan dele ruter og stykklister malstykklister i flere mindre enheter, øker antall varer, stykklister og ruter som må behandles i denne fremgangsmåten.  

Det finnes to metoder for modellering utsetting arbeid for produksjonsoperasjoner. Disse metodene er forskjellige på måten at subcontracting prosessen kan modelleres, slik at halvferdige varer representeres i prosessen, og måten kostnadskontroll administreres.

-   Underleverandører for ruteoperasjoner i produksjonsordrer eller ordrer for satsvis
    -   Serviceproduktet må være et lagerført produkt, og det må være del av stykklisten.
    -   Denne metoden støtter først inn, først ut (FIFO) eller standard kostpris.
    -   Halvferdige varer representeres av tjenesteproduktet i prosessen.
    -   Kostnadskontroll tildeler kostnader som er knyttet til arbeid fra underleverandør til materialkostnader.
-   Underleverandører for produksjonsflytaktiviteter i en lean-produksjon-flyt
    -   Tjenesten er et produkt som ikke er på lager, og det er ikke en del av stykklisten.
    -   Denne metoden bruker kjøpsavtaler som serviceavtaler.
    -   Denne metoden bruker backflush-etterkalkulering.
    -   Denne metoden tillater aggregerte og asynkrone innkjøp. (Materialflyt er uavhengig av innkjøpsprosessen.)
    -   Kostnadskontroll tildeler underleveranse arbeid i sin egen kostnad nedbryting-blokk.

## <a name="subcontracting-of-route-operations"></a>Utsetting av ruteoperasjoner
Hvis du vil bruke utsetting av ruteoperasjoner for produksjon eller satsvis ordrer, må tjenesteproduktet som brukes til innkjøp av tjenesten ,defineres som et produkt av typen **Tjeneste**. I tillegg må det ha en en varegruppe for modellen som har alternativet **Lagerført produkt** under **Lagerpolicy** satt til **Ja**. Dette alternativet angir om et produkt er etterkalkulert som lager på produktkvittering (**Lagerført produkt** = **Ja**), eller om produktet er utgiftsført på en resultatkonto (**Lagerført produkt** = **Nei**). Selv om dette kan virke motstridende, er det basert på det faktum at bare varer som har denne policyen oppretter lagertransaksjoner som kan brukes i kostnadskontroll å beregne planlagte kostnader og se de faktiske kostnadene når en produksjonsordre avsluttes.  

Hvis du vil bli vurdert i planleggings- og beregning, må tjenesten legges til Stykklisten. Stykklistelinjen må være av typen **Leverandør**, og det må tilordnes ruteoperasjonen som er tilordnet tjenesten. Denne ruteoperasjon må ha et kostark ressurs og ressursbehov som peker til en ressurs av **leverandøren** som kobler operasjonen og tjenesten som er relatert til den tilsvarende leverandørkontoen.  

Når denne konfigurasjonen brukes, opprettes en bestilling for relaterte tjenesteprodukt, basert på estimering av en produksjonsordre. Bestilling av tjenesten er brukt som forankring for underleveranse operasjoner. Underleveranse arbeidet kan administreres gjennom listesiden **Utsatt arbeid** i produksjonsstyring. Det utsatte arbeidet brukes til å levere råvarer og eventuelt et halvfabrikata til leverandøren som en forberedelse for operasjonen. Det brukes også til å motta det resulterende produktet for den utsatte operasjonen i vareankomst, der tjenesteproduktet brukes til å identifisere ankomsten av det halvferdige produktet. Når bestillingslinjen er mottatt, oppdateres produksjonsoperasjon som fullført.  

En produksjonsordre kan ha mange operasjoner, og hver operasjon kan tildeles til en annen leverandør. Derfor kan en produksjonsordre for ende-til-ende utløse flere bestillinger.

## <a name="subcontracting-of-production-flow-activities"></a>Utsetting av produksjonsflytaktiviteter
I [lean manufacturing](lean-manufacturing-overview.md)-løsningsmodeller er utsettingen av areid modellert som en tjeneste som er knyttet til en aktivitet i en [produksjonsflyt](tasks/create-production-flow-version.md) (emne i oppgaveguide). Derfor er denne typen utsetting også referert til som [aktivitetsbasert utsetting.](activity-based-subcontracting.md) En spesiell kostgruppetype, **Direkte utsetting**, er introdusert, og utsettingstjenester er ikke lenger en del av stykklisten over fullførte varer. Når du bruker lean manufacturing, er alle aktiviteter definert av kanbaner som kan være relatert til én eller flere produksjonsflytaktiviteter. Så langt høres den forklaringen ut akkurat som en forklaring på produksjonsordrer. Mens produksjonsordrene alltid må avsluttes med et ferdig produkt, kan du imidlertid opprette kanbaner for å levere halvferdig produkt. Du trenger ikke å introdusere et nytt produkt og stykklistenivå.  

Siden kanban-regler kan være svært dynamiske, kan du utforme forskjellige varianter av forsyning for samme produkt på en produksjonsflyt. Når du bruker lean utsetting, er materialflyten og finansflyten strengt atskilt. All materialflyt representeres av kanban-aktiviteter. Bestillinger for tjenesteprodukter og mottaksposteringer av disse tjenestene kan automatiseres, basert på statusen for kanban-jobber i produksjonsflyten. Kanban-jobber kan startes og fullføres selv før bestillingen er opprettet. Utsettingsdokumenter (bestilling og mottak av tjenesten) kan aggregeres etter periode og tjeneste. Antall kjøpsdokumenter og linjer kan derfor holdes lavt, selv i svært gjentatte operasjoner der leverandører gir underleveranser i en enkelt brikke flyt.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modell av utsetting i en produksjonsflyt

I en [lean produksjonsflyt](lean-manufacturing-modeling-lean-organization.md) kan en prosessaktivitet være definert som underleveranse når den er tildelt til en arbeidscelle (ressursgruppe) som har en enkelt leverandørressurs. Når en arbeidscelle er underleveranse, må relaterte prosessaktiviteter være koblet til en aktiv kjøpsavtalelinje som inneholder servicevaren og prisen på tjenesten. Serviceavtalen for aktiviteten definerer også beregningsforholdet mellom produktantallet for kanban-jobben og det resulterende serviceantallet. Du kan velge om tjenesteantallet er beregnet basert på hvor mange jobber, vareproduktantallet som er rapportert i prosjektene, eller det totale produktantallet (dette totale antallet inkluderer kasserte produkter).  

Overføringsaktiviteter kan også defineres som underleveranse. Denne definisjonen oppstår implisitt når du velger den ansvarlige parteb for levering i overføringsaktiviteten. Når du velger **Speditør** eller **Mottaker**, hvis tilsvarende kilden eller målet lageret er et leverandøradministrert lager, regnes aktiviteten som utsatt. Når du velger **Transportør**, er aktiviteten er alltid utsatt. Som utsatte prosessaktiviteter må en utsatt overføringsaktivitet være koblet til en serviceavtale før produksjonsflyten kan aktiveres.

### <a name="backflush-costing"></a>Backflush-etterkalkulering

Kostnadsregnskapet for underleveransearbeid er fullstendig integrert i etterkalkuleringen for lean manufacturing-løsningen (backflush-etterkalkulering). Når bestillingsmottak for tjenesten er postert, eller fakturering skjer, fordeles kostnaden for tjenesten på produksjonsflyten. Variansen for underleveranser beregnes for backflush-etterkalkulering ved motpostering av subcontracting blokken med standardkostnader for produktene som er mottatt mot de faktiske mottatt og fakturert serviceantall.

## <a name="material-supply-for-subcontracted-operations"></a>Regning forsyning for underleveranseoperasjoner
Halvferdige varer og andre relaterte materialer må overføres til stedet der arbeidet utføres fysisk. Når du bruker utsatte operasjoner og aktiviteter, er denne overføringen ofte knyttet til ekstra transport til et område som drives av leverandøren. Ved å tildele materiale i stykklisten for den utsatte operasjonen, kan du deklarere at materialet må samles inn plasseringen av ressursgruppen for den tildelte ressursen. Hovedplanlegging eller lean-etterfylling klargjør deretter materialet til denne plasseringen.  

Hvis du vil modellere lageret som er plassert hos en leverandør, er det en beste praksis i bransjen å definere et lager som administreres av leverandøren. Du kan enkelt definere et leverandøradministrert lager ved å opprette et nytt lager og tilordne leverandørkontoen. For å dokumentere at materialet må overføres til leverandøren før du kan utføre en operasjon, bør du tildele det leverandøradministrerte lageret til innleveringslageret for ressursgruppen som inneholder ressursen.  

For å etterfylle materialet i dette lageret kan du bruke flere strategier:

-   Overføringsordrer
-   Overfør journaler
-   Kanbaner for uttak
-   Direkte innkjøp til leverandørlokasjonen

Halvferdige produkter er unntaket for denne regelen. Hvis du vil overføre halvferdige produkter, er du begrenset til disse alternativene:

-   For produksjons- og partiordrer, kan halvferdige varer bare overføres logisk ved å bruke plukklistejournalen fra listesiden **Utsatt arbeid**. Denne journalen oppretter et leveringsmerknadsdokument som kan brukes til å overføre halvferdige produkter og råvarer til leverandøren.
-   Overføring av halvferdige varer er dokumentert ved mottak av Kanbaner uttak eller produksjon på leverandør plassering for underleveranse operasjoner i produksjonsflyter. For å forme en eksplisitt overføringsaktivitet kan du avslutte en produksjonskanban med en ekstra overføringsaktivitet.

**Merk:** En produksjonsrute for en enkelt produksjonsordre kan ikke krysse flere områder. Denne regelen gjelder også for det usatte arbeidet. Derfor må lagrene som representerer de leverandøradministrerte materialeplasseringene, være definert i det samme området som de interne ressursene som brukes i ruten. Selv om produksjonsflyter kan krysse av områder, kan de ikke transporter halvferdige varer fra ett område til et annet, fordi operasjonen antyder en endring i kostnadskontekst.  

Det utgående lageret, og plasseringen av en utsatt ressursgruppe fordeles vanligvis direkte til lageret, og plasseringen av det neste trinnet i operasjonen i ruten eller produksjonsflyten. Dette oppsettet bidrar til å redusere mengden av jobbrapportering som oppstår, eller antallet ekstra overføringer operasjonene som må modelleres.




