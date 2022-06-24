---
title: Aktivitetsbasert utsetting
description: Denne artikkelen beskriver i detalj hvordan du bruker aktiviteter i underleveranser i en produksjonsflyt for lean manufacturing.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule, PlanActivityServiceDetails, PlanActivityServiceWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e53da46a27fd573ae7f7450fcf34ffd8ef43e3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890748"
---
# <a name="activity-based-subcontracting"></a>Aktivitetsbasert utsetting

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver i detalj hvordan du bruker aktiviteter i underleveranser i en produksjonsflyt for lean manufacturing.

I Microsoft Dynamics 365 Supply Chain Management er det to fremgangsmåter for utsetting: produksjonsordrer og lean manufacturing. I lean manufacturing-tilnærmingen er utsettingen av arbeid modellert som en tjeneste som er knyttet til en aktivitet i en produksjonsflyt. En spesiell kostgruppetype som heter **Direkte utsetting**, er introdusert, og utsettingstjenester er ikke lenger en del av en stykkliste. Kostnadsregnskapet for underleveransearbeid er fullstendig integrert i etterkalkuleringsløsningen for lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Produksjonsflyter som involverer underleverandører
Det grunnleggende prinsippet til en produksjonsflyt endres ikke når aktiviteter er underleveranser. Materiale flyter fremdeles mellom lokasjoner, prosessaktiviteter konverterer materiale til produkter, og overføringsaktiviteter flytter materiale eller produkter fra én lokasjon til en annen. Du kan modellere lokasjoner og arbeidsceller som leverandøradministrert ved å tilordne leverandørkontoen til et lager eller en ressurs for en ressursgruppe.  

Basert på disse funksjonene krever ikke lean manufacturing noen bestemte funksjoner for å støtte flyten av materialer og produkter. Alle mulige scenarier som involverer leverandører som leverandører av produksjons- eller transporttjenester, kan modelleres basert på arkitekturen i produksjonsflyt og aktiviteter.  

En underleverandør jobber for eksempel fra et supermarked som befinner seg hos underleverandøren. Når håndteringsenheter tømmes hos underleverandøren, returneres kanban-kortene til monteringscellen med den neste forsendelsen. Supermarkedet hos underleverandøren blir deretter etterfylt. Overføringer til og fra underleverandøren kan modelleres som eksplisitte overføringsaktiviteter for å støtte en plukkings- og forsendelsesprosess. Hvis en eksplisitt registrering ikke er nødvendig for å støtte den fysiske transporten, kan overføringsaktivitetene utelates.  

En underleverandør kan brukes til å belastningsfordele den overordnede kapasiteten for produksjonsflyten. En produksjonsflyt modelleres for eksempel ved hjelp av planlagte kanban-regler. Planleggeren bruker Kanban-plankortet til å planlegge og nivåbelaste begge arbeidscellene ved behov. Planleggeren overvåker også den konsoliderte forsyningsplanen for supermarkedet på siden **Forsyningsplan**. Flere underleverandører kan modelleres i én eller flere produksjonsflyter, og det kan være flere kanban-regler som kan brukes til å gi det samme produktet til samme sted gjennom ulike aktiviteter. Planleggeren kan konvertere Kanbaner til en alternativ Kanban-regel for å planlegge på nytt en Kanban som opprinnelig ble opprettet for intern produksjon til en alternativ prosess. Arbeidscellens underleveransetype har faktisk ingen innvirkning på produksjonsflyten. Det samme arbeidsprinsippet gjelder for to parallelle interne arbeidsceller eller to underleveranseceller.   

På samme måte som med andre aktiviteter i en produksjonsflyt, kan aktiviteter i underleveranser forbruke og levere lagervarer, ikke-lagervarer (arbeid pågår \[VIA\]), og halvfabrikata og produkter. Prosessene for planlegging og utføring av aktiviteter i underleveranser er de samme i alle tilfeller. I tillegg behandler disse det samme som prosessene for internt arbeid.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Kjøpsprosess for aktiviteter i underleveranser (tjenester)
Kjøpsprosessen for aktiviteter i underleveranser er basert på den fysiske materialflyten som er registrert ved Kanban-jobbfremdriften, for eksempel start eller fullfør. Den økonomiske flyten, for eksempel kostnad for underleveransearbeid, er en sekundærflyt som følger den fysiske flyten. Samtidig er kjøpsprosessen en uavhengig prosess som muliggjør manuell justering av kjøpsdokumentene av innkjøpsdokumenter i hvert trinn. Her er kjøpsprosessen for aktiviteter i underleveranser:

1.  Opprett en kjøpsavtale. Kjøpsavtalen er opprettet for tjenesten og er koblet til aktiviteten i produksjonsflyten.
2.  Opprett en bestilling. Du kan opprette en frigivelsesordre for innkjøp for tjenesten, basert på de planlagte kanban-jobbene. Jobber for den samme tjenesten kan grupperes i bestillingslinjer etter dag, uke eller måned. Bestillingslinjene kan opprettes når som helst etter at kanban-jobbene er opprettet. Bestillingslinjer kan også opprettes etter faktaene. Dette alternativet velges vanligvis hvis en underleverandør tilbyr tjenester uten ytterligere varsel, basert på Kanbaner eller kanban-kortene som underleverandøren mottar. I dette tilfellet kan avvik mellom bestillingen og fakturaen minimeres.
3.  Generer kanban-kort, materiale og en plukkliste som sendes til underleverandøren for å klargjøre for behandling. Basert på den detaljerte modelleringen av produksjonsflyten, gjøres klargjøringen på kanban-tavlen for prosessaktiviteter ved hjelp av plukklisten og forberedelsesfunksjonen. Klargjøringen kan også gjøres på kanban-tavlen for overføringsjobber ved hjelp av plukklisten og start eller fullføring. For lagerført materiale kan begge prosessene støttes av en lagerstyringsplukking og forsendelsesprosess. Du kan opprette et fraktbrev ved behov.
4.  Generer kanban-behandlingsenheter og kanban-kort. Etter behandling returneres kort fra underleverandøren. Kortene inkluderer vanligvis en leveringsmerknad som angir det fysiske materialet som er levert. En referanse til leverte tjenester er ikke nødvendig. Ankomsten av materiale eller produktet hos kunden er registrert på kanban-tavlen, avhengig av kanban-kortene. (Kanban-tavlen for prosessaktiviteter eller kanban-tavlen for overføringsjobber brukes, avhengig av aktivitetene som er modellert).
5.  Opprett en mottaksveiledning. Mottaksveiledningen kan brukes til å erstatte et følgeseddeldokument for de mottatte tjenestene. Mottaksveiledninger kan genereres basert på fullførte kanban-jobber for utsettingsaktiviteten for en valgt periode. For hvert jobbmottak opprettes veiledningene for den tilhørende bestillingslinjen. Mottaksveiledningen kan skrives ut og sendes til underleverandøren som en bekreftelse på mottaket.
6.  Generer en faktura.

Prosessen avsluttes når underleverandøren faktureres for en periode. Fakturakontrollen utføres mot mottaksveiledningene som opprettes. Fordi mottaksveiledningene representerer den nøyaktige fysiske tilgangen av materiale, er treveis samsvar forenklet.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurere aktiviteter for utsetting
Følgende avsnitt beskriver hvordan du konfigurerer aktiviteter for utsetting.

### <a name="subcontracted-services"></a>Underleveranser

Betalingselementet som brukes i aktivitetsbasert utsetting, må være et produkt som har følgende egenskaper:

-   **Produkttype:** Tjeneste
-   **Lagermodellgruppe:** Ikke lagerført

Dette kravet fremtvinger bruk av først-inn-først-ut-lagermodellen. **Merk:** Kostnadsberegning av produktene krever at det defineres standard kostpris for tjenesten. Det kreves en kjøpsavtale med leverandøren. Hvis ikke kan ikke tjenesten brukes for aktivitetsbasert utsetting.

### <a name="subcontracted-process-activities"></a>Prosessaktiviteter i underleveranser

Hvis du vil konfigurere en prosessaktivitet som en aktivitet i underleveranser, følger du denne fremgangsmåten.

1.  Konfigurer en arbeidscelle for underleveranse. Hvis du vil konfigurere en arbeidscelle som en underleveranse, må du opprette en ressurs av typen **Leverandør** og knytte den til arbeidscellen (ressursgruppen). En kostnadskategori for kjøretid av kostgruppetypen **Direkte utsetting** skal tilordnes til arbeidscellen. Kostnadskategoriene for oppsett og antall er ikke nødvendig.
2.  Etter at en prosessaktivitet er opprettet og knyttet til en arbeidscelle for underleveranse, må du konfigurere en tjeneste for aktiviteten før produksjonsflytversjonen kan aktiveres. Du fullfører dette trinnet på siden **Aktivitets** **detaljer**. For aktiviteter som er knyttet til en arbeidscelle for underleveranse, vises hurtigfanen **Tjenestevilkår**. Legg til en standardtjeneste som er gyldig for alle varer for utdata, i denne hurtigfanen. Hvis bestemte utdatavarer krever ulike tjenester eller andre parametere for serviceberegning (for eksempel et annet tjenesteforhold), kan du legge til andre tjenester i aktiviteten.

## <a name="subcontracted-transfer-activities"></a>Overføringsaktiviteter i underleveranser
En overføringsaktivitet er konfigurert som en aktivitet i underleveranse, avhengig av innstillingen for **Fraktet av** for overføringsaktiviteten. Følgende alternativer er tilgjengelige:

-   **Speditør** – Aktiviteten er en underleveranse hvis overføringen fra lageret administreres av en leverandør (som definert av en egenskap for lageret). Alle valgte innkjøpsavtaler for tjenester må ha samme leverandør-ID som lageret.
-   **Mottaker** – Aktiviteten er en underleveranse hvis overføringen til lageret administreres av en leverandør (som definert av en egenskap for lageret). Alle valgte innkjøpsavtaler for tjenester må ha samme leverandør-ID som lageret.
-   **Transportør** – Aktiviteten er en underleveranse til en leverandør som tilbyr tjenesten. For å være gyldig må en transportør opprettes for lagerstyring og må ha en tilordnet leverandørkonto.

Som for prosessaktiviteter må du konfigurere en standardtjeneste for overføringsaktiviteter i underleveranser på siden **Tjenestevilkår** hurtigfanen **Aktivitets** **detaljer**.

## <a name="service-quantity-calculation"></a>Beregning av tjenesteantall
Hele kjøpsprosessen er basert på en varereferanse for en tjeneste. Denne varereferansen måles i en måleenhet for en tjeneste. Tjenester måles vanligvis i antall tjenester (enheter) eller i tid. Du kan bruke følgende metoder for å beregne serviceantallet, basert på den registrerte fullføringen av kanban-jobber:

-   **Beregning som er basert på antall jobber** – Én kanban-jobb er lik *n* enheter av tjenesten, uavhengig av produktantallet som leveres. I lean manufacturing tilsvarer én jobb én behandlingsenhet. Denne beregningsmåten gjelder for alle tjenester som har en fast pris per behandlingsenhet. Denne metoden gjelder derfor vanligvis for overføringsaktiviteter. Den kan imidlertid også gjelde for behandlingsaktiviteter som behandler hele behandlingsenheter.
-   **Beregning som er basert på produktantallet** – Tjenesten er relativ til produktantallet som planlegges/leveres. Når det leverte produktantallet beregnes, kan antall feil inkluderes eller utelukkes. Denne beregningsmåten brukes for alle saker der tjenesteprisen per enhet av behandlet produkt er avtalt.
-   **Beregning som er basert på aktivitetstiden** – De teoretiske aktivitetstidene beregnes basert på behandlingstiden for aktiviteten, totalt behandlet antall og produksjonsforholdet for det behandlede produktet. Denne beregningsmåten gjelder for tjenester som er betalt per time og har et avvik i tid per behandlet produkt.

## <a name="cost-accounting-of-subcontracted-services"></a>Kostnadsregnskap for underleveranser
Når mottaksveiledningen eller en leverandørfølgeseddel på en bestilling som ble opprettet for en produksjonsflyt (med andre ord en bestilling som ble generert basert på kanban-jobber for aktiviteter i underleveranser) er postert, beregnes verdien av mottaket i VIA-kontoene for produksjonsflyten. Avvikene for fakturaer blir også kostnadsberegnet til produksjonsflyten. En kostnadskategori for underleveransearbeid har blitt innført. Denne kostnadskategorien muliggjør gjennomsiktig sporing av verdien for underleveransearbeid som er tilordnet til VIA og konsumert per periode.  

Backflush-etterkalkuleringen for lean manufacturing på slutten av en etterkalkuleringsperiode beregner de faktiske variansene av produktene som er produsert fra produksjonsflyten i etterkalkuleringsperioden.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelleringsoverføringer som aktiviteter i underleveranser
Folk vurderer ofte transport som ikke-produktiv og mener at den ikke tilfører noen verdi. Når kostnaden for underleveranser sammenlignes med de interne produksjonskostnadene, må det imidlertid tas hensyn til kostnaden for ekstra transportaktiviteter. En produksjonsflyt som strekker seg over flere steder og krever transporttjenester, bør modellere transportkostnaden som en del av kostnaden av å levere produktene til kunden. 

Med aktivitetsbasert utsetting i lean manufacturing kan du integrere transportører og transportleverandører som flytter materialer og produkter mellom lokasjonene i en produksjonsflyt. Ved å modellere en overføringsaktivitet kan du tilordne en transportør eller leverandør. Overføringsaktivitetene-/jobben er basert på en tjeneste og kjøpsavtale, og du kan opprette bestillinger og mottaksveiledninger basert på de faktiske overføringsjobbene. Denne funksjonaliteten er den samme som funksjonaliteten for prosessaktiviteter i underleveranser.  

Supply Chain Management støtter nå stykklisteberegning som inkluderer transporttjenester, oppretting av relaterte bestillinger, integrert mottaksregistrering og integrering av kostnader for transporttjeneste i etterkalkulering for produksjonsflyt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]