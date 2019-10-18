---
title: Oversikt over produksjonsprosess
description: Dette emnet gir en oversikt over produksjonsprosessen. Den beskriver de ulike stadiene til produksjonsordrer, partiordrer og Kanbaner, fra oppretting av ordren til lukking av regnskapsperioden.
author: cvocph
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, OpResLifecycleManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b586a02d79fbbee698f32ab2ace3f86e7262fa7
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250029"
---
# <a name="production-process-overview"></a>Oversikt over produksjonsprosess

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over produksjonsprosessen. Den beskriver de ulike stadiene til produksjonsordrer, partiordrer og Kanbaner, fra oppretting av ordren til lukking av regnskapsperioden. 

Produksjonen av produkter, en prosess som også er kjent som produksjonens livssyklus, følger bestemte fremgangsmåter som er nødvendige for å fullføre produksjonen av en vare. Livssyklusen begynner med opprettelsen av produksjonsordren, partiordren eller Kanban. Den avsluttes med en ferdig, produsert vare som er klar for kunden eller en annen fase i produksjonen. Hvert trinn i livssyklusen krever ulike typer informasjon for å fullføre prosessen. Når hvert trinn fullføres, vil produksjonsordren, partiordren eller Kanban vise en endring i produksjonsstatusen. Ulike typer produkter krever forskjellige produksjonsprosesser.  

**Produksjonskontroll**-modulen er koblet til andre moduler, for eksempel **Behandling av produktinformasjon**, **Lagerstyring**, **Økonomimodul**, **Lagerstyring**, **Prosjektregnskap** og **Organisasjonsstyring**. Denne integreringen støtter informasjonsflyten som er nødvendig for å fullføre produksjonen av en ferdig vare.  

Produksjonsprosessen påvirkes vanligvis av kostnadsregnskaps- og beholdningsvurderingsmetodene som er valgt for en bestemt produksjonsprosess. Supply Chain Management støtter både faktiske kostnader (først inn, først ut \[FIFO\]; sist inn, først ut \[LIFO\]; glidende gjennomsnittet og periodisk avveid gjennomsnitt) og standardkostmetoder. Lean manufacturing implementeres basert på backflush-etterkalkuleringsprinsippet.  

Valget av kostnadsmålemetoder definerer også kravene til rapportering om material- og ressursforbruk under produksjonsprosessen. Faktiske kostnadsmetoder krever som regel nøyaktig rapportering på jobbnivå, mens periodiske kostnadsmetoder gir mindre detaljert rapportering av material- og ressursforbruk.

## <a name="mixed-mode-manufacturing"></a>Blandet modus-produksjon
Ulike produkter og produksjonstopologier krever bruk av forskjellige ordretyper. Supply Chain Management kan bruke forskjellige ordretyper i blandet modus. Med andre ord kan alle ordretyper forekomme under hele prosessen med å produsere ett ferdig produkt.

-   **Produksjonsordre** – Dette er den klassiske ordretypen for å produsere et bestemt produkt eller en produktvariant i et gitt antall på en bestemt dato. Produksjonsordrer er basert på stykklister og ruter.
-   **Partiordre** – Denne ordretypen brukes for prosessindustri og atskilte prosesser der produksjonskonverteringen er basert på en formel, eller der koprodukter og biprodukter kan være sluttprodukter, i tillegg til eller i stedet for hovedproduktet. Partiordrer bruker stykklister og ruter av typen **formel**.
-   **Kanban** – Kanbaner brukes til å signalisere gjentatte lean manufacturing-prosesser som er basert på produksjonsflyter, Kanban-regler og stykklister.
-   **Prosjekt** – Et produksjonsprosjekt kombinerer produkter og tjenester med en gitt tidsplan og et gitt budsjett. Produksjonsdelen av et prosjekt kan leveres via en av de andre ordretypene.

## <a name="manufacturing-principles"></a>Produksjonsprinsipper
Hvis du vil velge produksjonsprinsippet som passer best til et bestemt produkt og tilknyttet markedet, må du vurdere kravene til produksjon og logistikk, og også kundenes forventninger om leveringstider.

-   **Produser for lager** – Dette er det klassiske produksjonsprinsippet, der varer produseres for lager, basert på prognosen eller minimum lagerpåfyll (sistnevnte beregnes vanligvis basert på prognose eller historisk forbruk).
-   **Produksjon etter ordre** – Standardprodukter produseres etter ordre eller fullføres etter ordre. Selv om før-produksjon kan gjøres ved hjelp av prinsippet for å produsere for lager, utløses kostbare trinn i verdikjeden eller trinn som oppretter varianter, av en salgsordre eller overføringsordre.
-   **Konfigurer etter ordre** – Som ved prinsippet for produksjon etter ordre, utføres de endelige operasjonene i verdikjeden etter ordre. Den faktiske produktvarianten som produseres, er ikke forhåndsdefinert, men opprettes ved ordreregistreringen, basert på konfigurasjonsmodellen for salgsproduktet. Konfigurer etter ordre-prinsippet krever en del prosessamkjøring for en bestemt produktlinje.
-   **Produser på bestilling** – Prosesser for produksjon etter bestilling er vanligvis igangsatt av et prosjekt, og starter vanligvis med utviklingsfasen. I utviklingsfasen utvikles og beskrives de faktiske produktene som er nødvendige for å oppfylle ordren. Produksjonsordrer, partiordrer eller Kanbaner kan så opprettes for å produsere produktene.

## <a name="overview-of-the-production-life-cycle"></a>Oversikt over produksjonens livssyklus
Følgende trinn i produksjonslivssyklusen kan forekomme for alle ordretyper i blandet modus-produksjon. Men ikke alle er representert med en eksplisitt ordrestatus.

1.  **Opprettet** – Du kan opprette en produksjonsordre, partiordre eller Kanban manuelt, eller du kan konfigurere systemet for å generere dem basert på ulike behovssignaler. Hovedplanlegging oppretter produksjonsordrer, partiordrer eller Kanbaner ved autorisasjon av planlagte ordrer. Andre behovssignaler er salgsordrer eller tilknyttede forsyningssignaler fra andre produksjonsordrer eller Kanbaner. For Kanbaner med fast antall genereres behovssignaler når Kanbaner registreres som tomme.
2.  **Estimert** – Du kan beregne estimater for material- og ressursforbruk. Estimeringen genererer lagertransaksjoner for råmaterialer med statusen **I ordre**. Mottakene for hovedprodukter, koprodukter og biprodukter genereres når produksjonsordrer eller partiordrer estimeres. Hvis stykklisten inneholder linjer av typen **Tilknyttet forsyning**, genereres bestillinger for materialer eller underleveransetjenester og knyttes til produksjonsordren eller partiordren. Varer eller ordrer reserveres i henhold til reserveringsstrategien i produksjonsordren, og prisen på de ferdige varene beregnes basert på parameterinnstillingene.
3.  **Planlagt** – Du kan planlegge produksjon basert på operasjoner, individuelle jobber eller begge.
    -   **Grovplanlegging** – Denne planleggingsmetoden gir en anslagsvis, langsiktig plan. Ved å bruke denne metoden kan du tilordne start- og sluttdatoer til produksjonsordrer. Hvis produksjonsordrene er knyttet til ruteoperasjoner, kan du tilordne dem til kostnadssentergrupper.
    -   **Finplanlegging** – Denne planleggingsmetoden gir en detaljert plan. Hver operasjon sorteres inn i individuelle jobber som har bestemte datoer, tidspunkt og tilordnede driftsressurser. Hvis det brukes begrenset kapasitet, tilordnes jobber til operasjonsressurser basert på tilgjengelighet. Du kan vise og endre tidsplanen i et Gantt-diagram.
    -   **Kanban-plan** – Kanban-jobber planlegges på Kanban-plankortet eller planlegges automatisk basert på den automatiske planleggingskonfigurasjonen av Kanban-reglene.

4.  **Frigitt** – Du kan frigi produksjonsordren eller partiordren når tidsplanen er fullført og materialet kan plukkes eller klargjøres. Materialtilgjengelighetsjekken gjør det enklere for arbeidslederen å vurdere tilgjengeligheten av materiale for produksjonsordrene eller partiordrene. Du kan også skrive ut produksjonsordredokumenter, for eksempel plukklistene, jobbkortet, rutekortet og rutejobben. Når produksjonsordren frigis, endres ordrestatusen for å angi at produksjonen kan begynne. Når du bruker lagerstyring, vil en frigivelse av produksjonsordren eller partiordren frigi produksjonsstykklistelinjene til lagerstyring. Lagerbølger og lagerarbeid genereres deretter i henhold til oppsettet av lageret.
5.  **Klargjort**/**plukket** – Når alle materialer og ressurser er klargjort på produksjonsstedet, oppdateres produksjonsstykklistelinjene eller Kanban-linjer til statusen **Plukket**. Tilknyttede forsyningsordrer og tilknyttet lagerarbeid fullføres vanligvis på dette stadiet. Kanban-kortene eller jobbkortene som er nødvendige for å rapportere fremdrift for produksjonen, må tilordnes og skrives ut.
6.  **Startet** – Når en produksjonsordre, partiordre eller Kanban er startet, kan du rapportere forbruk av materialer og ressurser mot ordren. Systemet kan konfigureres til å postere automatisk materiale- og ressursforbruk som tilordnes til ordren, når ordren er startet. Denne fordelingen kalles forhåndstrekk, fremovertrekk eller autoforbruk. Du kan fordele materialer til produksjonsordrer eller partiordrer manuelt ved å opprette flere plukklistejournaler. Du kan også fordele arbeidskostnader og andre rutekostnader manuelt til ordren. Hvis du bruker grovplanlegging, kan du fordele disse kostnadene ved å opprette en rutekortjournal. Hvis du bruker finplanlegging, kan du fordele kostnadene ved å opprette en jobbkortjournal. Produksjonsordrer eller partiordrer kan startes i partier med det forespurte endelige antallet. I en produksjonsordre, partiordre eller Kanban kan jobbene som opprettes, startes og rapporteres separat via journaler, produksjonsutførelsesterminalen (MES-terminal) eller Kanban-tavlene.
7.  Rapporter fremdrift / **Fullfør** jobber – Bruk MES-terminalen, produksjonsjournaler, Kanban-kort eller mobilskannefunksjoner for å rapportere fremdriften for produksjon etter jobb eller ressurs. Forbruk av materialer og ressurser posteres, og statusen for de tilknyttede Kanbanene, produksjonsordrene og partiordrene kan oppdateres til **Mottatt** eller **Ferdigmeldt**. Plasseringsarbeid for lageret kan opprettes, avhengig av lageroppsettet.
8.  **Ferdigmeldt** (produktkvitteringen) – Når en produksjonsordre eller partiordre rapporteres som ferdig, oppdateres antallet av de fullførte, ferdige varene på lageret. Dette antallet inkluderer antall relevante koprodukter og biprodukter. Hvis du bruker VIA (varer i arbeid), lages det en finansjournal for å redusere VIA-kontoene og øke beholdningen av ferdigvarene. Når kostnadene for en produksjonsordre beregnes, posteres de faktiske kostnadene for produksjonen. Hvis material- og arbeidskostnadene som er knyttet til en produksjon, ikke allerede er fordelt i en journal eller ved forhåndstrekk, kan de fordeles automatisk gjennom backflushing. Tilordning gjennom backflushing omfatter etterfratrekk av lagertransaksjonsprosesser. Hvis produksjonsordren fullføres, merker du av for **Avslutt jobb** for å endre den gjenværende statusen til **Avsluttet**. Hvis ikke, lar du feltet stå tomt slik at ekstra antall som produseres, kan rapporteres.
9.  **Vurdering av kvalitet** – En produktkvittering kan føre til oppretting av kvalitetsordrer, avhengig av konfigurasjonen av testprosesser og kvalitetsreglene som opprettes for bestemte produkter. Siden en kvalitetsordre kan oppdatere lagerstatusen eller bunkeattributtene for de testede produktene, er kvalitetsvurderingen en obligatorisk prosess i mange bransjer.
10. **Plassert** og **Leveringsordre** – Etter produktmottaket og kvalitetsvurderingen dirigerer det valgfrie plasseringsarbeidet de mottatte produktene til neste forbrukspunkt, til et lager for ferdigvarer, eller til en leveringssone hvis det er leveringsordrekrav.
11. **Avsluttet**– Før avslutning av produksjonen beregnes det faktiske kostnader for antallet som ble produsert. Alle estimerte kostnader i forbindelse med materialer, arbeid og administrasjonskostnader tilbakeføres og erstattes med faktiske kostnader. Hvis du merker av for **Avslutt jobb** når du kjører kostnadsberegningen, endres produksjonsordrestatusen til **Avsluttet**. Denne statusen hindrer at det posteres tilleggskostnader til en fullført produksjonsordre.
12. **Periodisk avslutning** – Noen regnskapsprinsipper, som periodisk gjennomsnitt, backflush-etterkalkulering, FIFO eller LIFO, krever periodiske aktiviteter for å lukke lageret eller regnskapsperioden. Vanligvis prøver systemet å rapportere alt material- og ressursforbruk samt korrigeringer av lager og svinn, før periodene lukkes. Denne rapporteringen gjøres vanligvis ved hjelp av lagerbevegelsesjournaler eller justeringsjournaler. Målet er å vurdere det økonomiske resultatet til driftsenheter per periode. I noen tilfeller når tidkrevende produksjonsordrer brukes, som strekker seg over de økonomiske rapporteringsperiodene, brukes produksjonsjournaler til å rapportere produksjonsfremdriften og ressursforbruket ved utløpet av perioden.


<a name="additional-resources"></a>Tilleggsressurser
--------

[Tilbakemeldinger på produksjon](production-feedback.md)

[Produktkonfigurasjonsmodeller](../pim/product-configuration-models.md)

[Lean manufacturing](lean-manufacturing-overview.md)



