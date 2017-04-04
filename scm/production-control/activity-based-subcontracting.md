---
title: Aktivitetsbaserte utsetting
description: Dette emnet beskriver, i detalj hvordan du bruker underleveranse aktiviteter i en produksjonsflyt for lean manufacturing.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Aktivitetsbaserte utsetting

Dette emnet beskriver, i detalj hvordan du bruker underleveranse aktiviteter i en produksjonsflyt for lean manufacturing.

I Microsoft Dynamics 365 for operasjoner, er det to fremgangsmåter for bruk av underleverandører: produksjonsordrer og lean manufacturing. I lean manufacturing-tilnærming, er subcontracting arbeidet modellert som en tjeneste som er knyttet til en aktivitet i en produksjonsflyt. En spesiell type kostgruppetype som heter **direkte outsourcing** er introdusert, og subcontracting tjenestene er ikke lenger en del av en stykkliste (BOM). Kostnadsregnskap for underleveranse arbeid er fullstendig integrert i etterkalkuleringsversjonen løsning for lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Produksjonsflyter som involverer underleverandører
Grunnleggende prinsippet med en produksjonsflyt, endres ikke når aktiviteter er underleveranse. Materiale fremdeles flyter mellom lokasjoner, Prosessaktiviteter Konverter materiale til produkter og overføringsaktiviteter flytte materiale eller produktene fra én plassering til en annen. Du kan forme plasseringene og arbeide celler som leverandøren administreres ved å tilordne en leverandørkonto til et lager eller en ressurs for en ressursgruppe.  

Basert på disse funksjonene, krever lean manufacturing ikke noen bestemte funksjoner for å støtte flyten av materialer og produkter. Alle mulige scenarier som involverer leverandører som leverandører av produksjon eller transport tjenester kan modelleres basert på arkitekturen i produksjonsflyt og aktiviteter.  

For eksempel fungerer en underleverandør fra et supermarked befinner seg på underleverandøren. Når håndteringsenheter er tømt på underleverandøren, returneres kanban-kortene til samlingen cellen med den neste følgeseddelen. Supermarked på underleverandøren fylles deretter. Overføringer til og fra underleverandøren kan modelleres som eksplisitt overføringsaktiviteter til å støtte en plukking og forsendelse. Hvis en eksplisitt registrering ikke er nødvendig for å støtte fysisk transport, kan overføring aktivitetene utelates.  

En underleverandør kan brukes til å fordele innlastingen i generell kapasitet for produksjonsflyten. For eksempel er en produksjonsflyt modellert ved hjelp av planlagte kanban-regler. Planleggeren bruker kanban planlegging brettet for å planlegge og laste inn nivå begge arbeidscellene på forespørsel. Planleggeren overvåker også konsoliderte forsyning tidsplanen for supermarked på den **forsyningsplanen** siden. Flere underleverandører kan modelleres i én eller flere produksjonsflyter, og det kan være flere kanban-regler som kan brukes til å gi det samme produktet til samme sted gjennom ulike aktiviteter. Planleggeren kan konvertere Kanbaner til en alternativ kanban-regel for å planlegge en kanban som opprinnelig ble opprettet for intern produksjon til en alternativ prosess. Faktisk har underleveranse karakteren av arbeidscellen ingen innvirkning på produksjonsflyten. Det samme arbeide prinsippet gjelder for to parallelle interne arbeidsceller eller to underleveranse celler.   

På samme måte som med andre aktiviteter i en produksjonsflyt, kan aktiviteter i underleveranser forbruker og angi inventoried, inventoried (arbeid pågår \[via\]), og halvferdige materialer og produkter. Prosesser for planlegging og utføring av aktiviteter i underleveranser er de samme i alle tilfeller. I tillegg behandle disse på samme måte som for interne prosesser.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Kjøpsprosessen for aktiviteter i underleveranser (tjenester)
Kjøpsprosessen for underleveranse aktiviteter er basert på den fysiske materialflyt som er registrert ved kanban fremdriften i prosjektet, for eksempel, starte eller fullføre. Økonomisk flyten, for eksempel kostnad for underleveranse arbeid er en Sekundærflyt som følger fysiske flyten. Kjøpsprosessen er en uavhengig prosess som gjør det mulig for manuell justering av kjøpsdokumentene i hvert trinn på samme tid. Her er kjøpsprosessen for aktiviteter i underleveranser:

1.  Opprette en kjøpsavtale. Kjøpsavtalen er opprettet for tjenesten og er koblet til aktiviteten i produksjonsflyten.
2.  Opprett en bestilling. Du kan opprette en frigivelsesordre for innkjøp for tjenesten, basert på de planlagte kanban-jobbene. Jobber for den samme tjenesten kan grupperes bestillingslinjer etter dag, uke eller måned. Bestillingen kan opprettes når som helst etter at kanban-jobbene er opprettet. Selv du kan opprette bestillingslinjer i ettertid. Dette alternativet velges vanligvis hvis en underleverandør tilbyr tjenester uten ytterligere varsel, basert på Kanbaner eller kanban-kortene som mottar underleverandøren. I dette tilfellet kan avvik mellom bestillingen og fakturaen minimeres.
3.  Generer kanban-kort, materiale og en plukkliste for å sende til underleverandøren til å klargjøre for behandling. Basert på detaljerte modellering av produksjonsflyten, gjøres klargjøring på kanban-tavlen for Prosessaktiviteter ved hjelp av plukklisten og forberedelse-funksjonen. Du kan også utføres forberedelsene på kanban-tavlen for overføring av jobber ved hjelp av plukkliste og start eller fullføring. For inventoried materiale, kan begge prosessene støttes av en WMS-plukking og forsendelse. Du kan opprette et fraktbrev ved behov.
4.  Generere kanban behandling av enheter og kanban-kort. Etter behandling returneres kort fra underleverandøren. Kortene inkluderer vanligvis en leveringsmerknad som angir det fysiske materialet som er levert. En referanse til angitte tjenester er ikke nødvendig. Ankomsten av materiale eller produktet hos kunden er registrert på kanban-tavlen, avhengig av kanban-kortene. (Enten kanban-tavlen for Prosessaktiviteter eller kanban-tavlen for overføring av jobber brukes, avhengig av aktivitetene som er modellert.).
5.  Opprette et mottak rådgivning. Mottaket veiledningen kan brukes til å erstatte en følgeseddel slip dokument for de mottatte tjenestene. Mottaket veiledningene kan genereres basert på fullførte kanban-jobber for subcontracting aktiviteten for en valgt periode. For hver jobbmottak opprettes veiledningene for den tilhørende bestillingslinjen. Mottaket rådgivning kan skrives ut og sendes til underleverandøren som en bekreftelse på mottaket.
6.  Generere en faktura.

Prosessen avsluttes når underleverandøren faktureres for en periode. Faktura-treff utføres mot mottak veiledningene som er opprettet. Fordi mottaket veiledningene representerer nøyaktig fysisk mottak av materiale, forenklet treveis samsvar.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurere aktiviteter for utsetting
Følgende avsnitt beskriver hvordan du konfigurerer aktiviteter for bruk av underleverandører.

### <a name="subcontracted-services"></a>Underleveranser

Betaling-element som brukes i aktivitetsbaserte utsetting må være et produkt som har følgende egenskaper:

-   **Produkttype:** Service
-   **Lagermodellgruppen:** ikke på lager

Dette kravet fremtvinger bruk av først inn, først ut (FIFO) lagermodell. **Merk:** kostnadsberegning av produktene som krever at det defineres standard kostpris for tjenesten. Det kreves en kjøpsavtale med leverandøren. Hvis ikke, vil tjenesten kan ikke brukes for aktivitetsbaserte utsetting.

### <a name="subcontracted-process-activities"></a>Underleveranse Prosessaktiviteter

Hvis du vil konfigurere en prosessaktivitet som en aktivitetstjenester, følger du denne fremgangsmåten.

1.  Konfigurere en Underleveransearbeid celle. Hvis du vil konfigurere en arbeidscelle som underleveranse, må du opprette en ressurs av den **leverandøren** skriver du inn og knytte den til arbeidscellen (ressursgruppe). En kostnadskategori for kjøring av den **direkte outsourcing** kostgruppetype skal tilordnes til arbeidscellen. Kostnadskategorier for oppsett og antall er ikke nødvendig.
2.  Når en prosessaktivitet er opprettet og knyttet til en Underleveransearbeid celle, må du konfigurere en tjeneste for aktiviteten før produksjonsflytversjonen kan aktiveres. Du fullfører dette trinnet i den **aktivitet****detaljer** siden. For aktiviteter som er knyttet til en Underleveransearbeid celle, den **vilkårene for tjenesten** hurtigfanen vises. Legge til en standardtjeneste som er gyldig for alle varer for utdata i denne hurtigfanen. Hvis bestemte produksjonsvarer krever ulike tjenester eller annen tjeneste beregningsparametere (for eksempel en annen tjeneste-forholdet), kan du legge til andre tjenester aktiviteten.

## <a name="subcontracted-transfer-activities"></a>Underleveranse overføringsaktiviteter
En overføringsaktivitet er konfigurert som en aktivitetstjenester, avhengig av den **Fraktet av** på overføringsaktivitet for. Følgende alternativer er tilgjengelige:

-   **Speditøren** -aktiviteten er en underleveranse Hvis overføringen fra lageret som administreres av en leverandør (som definert av en egenskap for lageret). Alle valgte innkjøpsavtaler for tjenester må ha samme leverandør-ID som lageret.
-   **Mottakeren** -aktiviteten er en underleveranse Hvis overføring til lageret administreres av en leverandør (som definert av en egenskap for lageret). Alle valgte innkjøpsavtaler for tjenester må ha samme leverandør-ID som lageret.
-   **Transportør** – er en underleveranse aktiviteten til en leverandør som gir tjenesten. For å være gyldig, må opprettes for lagerstyring operatør, og må ha en leverandørkonto som er tilordnet.

Som for Prosessaktiviteter, må du konfigurere en Standardtjeneste for underleveranse overføringsaktiviteter på den **vilkårene for tjenesten** hurtigfanen i den **aktivitet****detaljer** siden.

## <a name="service-quantity-calculation"></a>Beregning av tjenesteantall
Hele kjøpsprosessen er basert på en element-referansen for en tjeneste. Denne varereferanse måles i en enhet for en tjeneste. Tjenester er vanligvis måles i antall tjenester (enheter) eller i gang. Du kan bruke følgende metoder for å beregne serviceantallet, basert på registrert kanban-jobber er fullført:

-   **Beregningen er basert på antall jobber** – én kanban-jobben er lik *n* enheter av tjenesten, uavhengig av produktantallet som er angitt. I lean manufacturing tilsvarer én jobb én behandlingsenhet. Denne beregningsmåten gjelder for alle tjenester som har en fast pris per behandlingsenhet. Denne metoden gjelder derfor vanligvis for å overføre aktiviteter. Det kan imidlertid også bruke til å behandle aktiviteter som behandler hele behandling av enheter.
-   **Beregningen er basert på produktantallet** – hvor tjenesten er i forhold til produktantallet som er planlagt/angitt. Når det angitte produktantallet beregnes, kan antall feil være inkludert eller utelukket. Denne beregningsmåten brukes for alle saker der tjenesten prisen per enhet av behandlede produktet er avtalt.
-   **Beregningen er basert på aktiviteten** – ganger teoretiske aktiviteten beregnes, basert på behandlingstiden for aktiviteten, behandlet totalt antall og Produksjonsforhold av behandlede produktet. Denne beregningsmåten gjelder for tjenester som er betalt per time og har et avvik i tid per produkt behandlet.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostnadsregnskap underleveranser
Når mottaket rådgivning eller leverandør følgeseddel på en bestilling som ble opprettet for en produksjonsflyt (med andre ord, en bestilling som ble generert basert på kanban-jobber for aktiviteter i underleveranser) er bokført, etterkalkulert verdien av mottaket i VIA-kontoer for produksjonsflyten. Avvikene for fakturaer er også kostnadsberegnet til produksjonsflyten. En kostnadskategori for underleveranse arbeid har blitt innført. Denne kostnadskategorien aktivere gjennomsiktig sporing av verdien for underleveranse arbeid som er tildelt via og konsumert per periode.  

Backflush etterkalkulering for lean manufacturing på slutten av en kostnadsversjon periode beregner faktiske variansen av produktene som er produsert fra produksjonsflyten i etterkalkuleringsversjonen periode.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modellering overføringer som aktiviteter i underleveranser
Personer kan ofte vurdere transport ikke-produktivt og mener at den legger til noen verdi. Imidlertid kostnadene ved bruk av underleverandører er sammenlignet med intern produksjonskostnadene, kostnaden av ekstra transport aktiviteter må tas i betraktning. En produksjonsflyt som strekker seg over flere steder, og som krever transport tjenester bør modeller transport kostnader som en del av kostnaden for leverer varer til kunden. 

Aktivitetsbaserte utsetting i lean manufacturing, kan du integrere transportører og transport leverandører som flytte materialer og varer mellom plasseringen av en produksjonsflyt. Ved modellering en overføringsaktivitet, kan du tilordne en leverandør eller leverandør. Aktiviteter/overføringsjobben er basert på en tjeneste og kjøp avtalen, og du kan opprette bestillinger og mottak veiledningene, basert på de faktiske overføring av jobbene. Denne funksjonaliteten er den samme som funksjonaliteten for underleveranse Prosessaktiviteter.  

Derfor servicekostnader Dynamics 365 for operasjoner nå støtter stykklisteberegning som inkluderer transport services, oppretting av relaterte bestillinger, integrert mottak registrering og integrasjon av transport til etterkalkulering av produksjonsflyt.


