---
title: Administrer utsetting arbeid i produksjon
description: "Dette emnet forklarer hvordan underleveranseoperasjoner skal behandles i Microsoft Dynamics 365 for operasjoner. Med andre ord, forklarer det hvordan produksjonsoperasjoner som er tildelt en ressurs er styrt av en leverandør."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Administrer utsetting arbeid i produksjon

Dette emnet forklarer hvordan underleveranseoperasjoner skal behandles i Microsoft Dynamics 365 for operasjoner. Med andre ord, forklarer det hvordan produksjonsoperasjoner som er tildelt en ressurs er styrt av en leverandør.

I [produksjonsprosesser](production-process-overview.md), arbeidet kan gjøres av ressurser som eies eller administreres av leverandører. Leverandør ressurser brukes vanligvis til nivå periodiske overflødige behovet som bruke enn de som den disponible kapasiteten i et firma eier ressurser. Leverandøren vil kanskje også kunne tilby spesifikke [ressursfunksjoner](resource-capabilities.md)eller ressurser til en lavere pris.  

Avhengig av leverandør-ressurser som brukes i produksjonsprosessen, en [route](routes-operations.md) har ofte flere logistikk krav, fordi materialet og halvferdige varer må først transporteres til leverandørens webområde. Resultatet av operasjonen underleveranse må deretter transporteres til lokasjonen som er tildelt til neste operasjon eller et lager for ferdige varer.  

Når utsetting operasjoner eller aktiviteter, kan de påvirke alle faser av operasjoner fra definisjonen av operasjonene som kreves i produksjonen, etterkalkulering, prognoser, planlegging og planlegging for administrasjon av logistikk for materialer, halvferdige varer og ferdigvarer. Til slutt krever disse ressursene sine egne prosesser for regnskap og kostnadskontroll.  

For interne ressurser fordeles vanligvis en fast kostnadssats for en periode. Derimot er kostnaden for underleveranse ressurser basert på kjøpsprisen for den tilknyttede tjenesten. Tjenesten er definert som et annet produkt, og brukes til å drive innkjøp og kjøpe prosesser for underleveranse behandlingshastigheten.  

Det er for øyeblikket ingen eksplisitte begrepet halvferdige produkter i Microsoft Dynamics 365 for operasjoner. For en produksjonsordre som krever mer enn én operasjon for å transformere råvarer til en ferdig vare, posteres den ferdige varen tilbake på lageret bare i den siste operasjonen. Halvferdige produktene som tidligere operasjoner gi er etterkalkulert i varer i arbeid (via), men de ikke bokført eller registrert på lager. Selv om du kan dele ruter og stykklister malstykklister i flere mindre enheter, øker antall varer, stykklister og ruter som må behandles i denne fremgangsmåten.  

Det finnes to metoder for modellering utsetting arbeid for produksjonsoperasjoner. Disse metodene er forskjellige på måten at subcontracting prosessen kan modelleres, slik at halvferdige varer representeres i prosessen, og måten kostnadskontroll administreres.

-   Underleverandører for ruteoperasjoner i produksjonsordrer eller ordrer for satsvis
    -   Service-produktet må være en lagerførte produkter, og det må være del av Stykklisten.
    -   Denne metoden støtter først inn, først ut (FIFO) eller standard kostpris.
    -   Halvferdige varer representeres av tjenesteprodukt i prosessen.
    -   Kostnadskontroll tildeler kostnader som er knyttet til arbeid fra underleverandør til material kostnader.
-   Underleverandører for produksjonsflytaktiviteter i en lean-produksjon-flyt
    -   Tjenesten er et produkt som ikke er på lager service, og det er ikke en del av Stykklisten.
    -   Denne metoden bruker kjøpsavtaler som serviceavtaler.
    -   Denne metoden bruker backflush-etterkalkulering.
    -   Denne metoden kan aggregert og asynkrone innkjøp. (Materialflyt er uavhengig av innkjøpsprosessen.)
    -   Kostnadskontroll tildeler underleveranse arbeid i sin egen kostnad nedbryting-blokk.

## <a name="subcontracting-of-route-operations"></a>Underleverandører for ruteoperasjoner
Hvis du vil bruke underleverandører for ruteoperasjoner for produksjon eller satsvis ordrer, service-produktet som brukes til innkjøp av tjenesten må defineres som et produkt av den **tjenesten** type. I tillegg må en varegruppe for modellen er den **Lagerført produkt** alternativet **lager policy** satt til **Ja**. Dette alternativet angir om et produkt er etterkalkulert som lager på produktkvittering (**Lagerført produkt** = **Ja**), eller om produktet er utgiftsført på en resultat-konto (**Lagerført produkt** = **ingen**). Selv om dette kan virke motstridende, er det basert på det faktum at bare varer som har denne policyen oppretter lagertransaksjoner som kan brukes i kostnadskontroll å beregne planlagte kostnader og se de faktiske kostnadene når en produksjonsordre avsluttes.  

Hvis du vil bli vurdert i planleggings- og beregning, må tjenesten legges til Stykklisten. Stykklistelinjen må være av den **leverandøren** type, og det må tilordnes ruteoperasjonen som er tilordnet tjenesten. Denne ruteoperasjon må ha et kostark ressurs og ressursbehov som peker til en ressurs av den **leverandøren** som kobler operasjonen og tjenesten som er relatert til den tilsvarende leverandørkontoen.  

Når denne konfigurasjonen brukes, opprettes en bestilling for relaterte tjenesteprodukt, basert på estimering av en produksjonsordre. Bestilling av tjenesten er brukt som forankring for underleveranse operasjoner. Underleveranse arbeidet kan administreres gjennom den **underleveranse arbeid** listesiden i produksjonsstyring. Underleveranse arbeidet brukes til å levere råvarer og eventuelt et halvfabrikata til leverandøren som en forberedelse for operasjonen. Det brukes også til å motta det resulterende produktet for underleveranse operasjonen i Vareankomst, der produktet service brukes til å identifisere ankomsten av halvferdige produktet. Når det mottas på bestillingslinjen, oppdateres produksjonsoperasjon som fullført.  

En produksjonsordre kan ha mange operasjoner, og hver operasjon kan tildeles til en annen leverandør. Derfor kan en produksjonsordre for ende-til-ende utløse flere bestillinger.

## <a name="subcontracting-of-production-flow-activities"></a>Underleverandører for produksjonsflytaktiviteter
Den [lean manufacturing](lean-manufacturing-overview.md)løsning modeller subcontracting arbeidet som en tjeneste som er knyttet til en aktivitet i en [produksjonsflyten](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (oppgaveemne for TV-guiden). Derfor denne typen utsetting er også referert til som [aktivitetsbaserte utsetting.](activity-based-subcontracting.md) En spesiell Kostnadstype gruppe, **direkte outsourcing**, er introdusert, og subcontracting tjenestene ikke er en del av Stykklisten av de ferdige varene. Når du bruker lean manufacturing, er alle aktiviteter som definert av Kanbaner som kan være relatert til én eller flere produksjonsflytaktiviteter. Så langt som forklaring lyder akkurat som en forklaring på produksjonsordrer. Mens produksjonsordrene må alltid avslutte med et ferdig produkt, kan du opprette Kanbaner for å levere en delvis ferdig produkt. Du trenger ikke å introdusere et nytt produkt og stykklistenivå.  

Kanban-regler kan være svært dynamisk, kan du utforme forskjellige varianter av forsyning for samme produkt på en produksjonsflyt. Når du bruker lean skilles strengt utsetting, materialflyt og økonomiske flyt. Alle materialflyt representeres av kanban-aktiviteter. Bestillinger for serviceprodukter og -mottak posteringer av disse tjenestene kan automatiseres, basert på statusen for kanban-jobber i produksjonsflyten. Kanban-jobber kan startes og fullføres selv før bestillingen er opprettet. Utsettingsdokumenter (bestilling og mottak av tjenesten) kan aggregeres av punktum og service. Antall kjøpsdokumenter og linjer kan derfor holdes liten, selv i svært gjentatte operasjoner der leverandører gir underleveranser i en enkelt brikke flyt.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modellering utsetting i en produksjonsflyt

I en [Lær produksjonsflyten](lean-manufacturing-modeling-lean-organization.md), en prosessaktivitet kan være definert som underleveranse når den er tildelt til en arbeidscelle (ressursgruppe) som har en enkelt leverandør-ressurs. Når en arbeidscelle er underleveranse, vil relaterte Prosessaktiviteter må være koblet til en aktiv kjøpsavtalelinjen som inneholder servicevaren og prisen på tjenesten. Serviceavtale for aktiviteten definerer også beregningen forholdet mellom produktantallet for kanban-jobben og det resulterende serviceantallet. Du kan velge om tjenesten antallet er beregnet basert på hvor mange jobber, god produktantallet som er rapportert i prosjektene eller totale produktantallet (denne totale antallet inkluderer kasserte produkter).  

Overføringsaktiviteter kan også defineres som underleveranse. Denne definisjonen oppstår implisitt når du velger Ansvarlig part for leverings i overføring aktiviteten. Når du velger **speditør** eller **mottaker**, hvis tilsvarende kilden eller målet lageret er et lager for leverandør-administrerte, regnes aktiviteten underleveranse. Når du velger **bærer**, aktiviteten er alltid underleveranse. Underleveranse Prosessaktiviteter, for eksempel en overføringsaktivitet for underleveranse må være koblet til en serviceavtale før produksjonsflyten kan aktiveres.

### <a name="backflush-costing"></a>Backflush-etterkalkulering

Kostnadsregnskap for underleveranse arbeid er fullstendig integrert i etterkalkulering for lean manufacturing-løsning (backflush-etterkalkulering). Når bestillingsmottak for tjenesten er postert, eller fakturering skjer, fordeles kostnaden for tjenesten på produksjonsflyten. Variansen for underleveranser beregnes for backflush-etterkalkulering ved motpostering av subcontracting blokken med standardkostnader for produktene som er mottatt mot de faktiske mottatt og fakturert serviceantall.

## <a name="material-supply-for-subcontracted-operations"></a>Regning forsyning for underleveranseoperasjoner
Halvferdige varer og andre relaterte materialer må overføres til stedet der arbeidet utføres fysisk. Når du bruker underleveranse operasjoner og aktiviteter, er denne overføringen ofte knyttet til flere transport til et område som drives av leverandøren. Ved å tildele materiale i Stykklisten for underleveranse operasjonen, kan du deklarere at materialet må samles inn plasseringen av ressursgruppen for den tildelte ressursen. Hovedplanlegging eller lean-etterfylling deretter Klargjør materiale til denne plasseringen.  

Hvis du vil modellere lageret som er plassert hos en leverandør, er det en beste praksis i bransjen til å definere et lager som administreres av leverandøren. Lett kan du definere et lager som leverandøren administreres ved å opprette et nytt lager og tilordning av leverandørkontoen. For å dokumentere dette materialet må overføres til leverandøren før du kan utføre en operasjon, bør du tildele leverandør-administrerte lageret til innleveringslageret for ressursgruppen som inneholder ressursen.  

For å etterfylle materialet i dette lageret, kan du bruke flere strategier:

-   Overføringsordrer
-   Overfør journaler
-   Uttak-Kanbaner
-   Direkte innkjøp til plasseringen for leverandør

Halvferdige produkter er det eneste unntaket for denne regelen. Hvis du vil overføre halvferdige produkter, er du begrenset til disse alternativene:

-   For produksjonen og kjørselen bestillinger, halvferdige varer kan bare overføres logisk ved å bruke plukklistejournalen fra den **underleveranse arbeid** listesiden. Denne kladden oppretter en leveringsmerknad dokument som kan brukes til å overføre halvferdige og råvarer til leverandøren.
-   Overføring av halvferdige varer er dokumentert ved mottak av Kanbaner uttak eller produksjon på leverandør plassering for underleveranse operasjoner i produksjonsflyter. For å forme en eksplisitt overføringsaktivitet, kan du avslutte en produksjons-kanban med en ekstra overføringsaktivitet.

**Merk:** en produksjonsrute for en enkelt produksjonsordre kan ikke på tvers av flere områder. Denne regelen gjelder også for underleveranse arbeidet. Derfor lagrene som representerer materialet leverandør-administrerte plasseringer må være definert i det samme området som de interne ressursene som brukes i ruten på nytt. Selv om produksjonsflyter kan på tvers av områder, kan de transport halvferdige varer fra ett område til et annet, fordi operasjonen antyder en endring i kostnad-kontekst.  

Utdata-lageret, og plasseringen av en underleveranse ressursgruppe fordeles vanligvis direkte til lageret, og plasseringen av det neste trinnet i operasjonen i rute- eller flyten. Dette oppsettet bidrar til å redusere mengden av jobben rapportering som oppstår eller tall flere overføring operasjonene som må være modellert.


