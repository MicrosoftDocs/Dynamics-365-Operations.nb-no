---
title: Stykklister og formler
description: Dette emnet inneholder informasjon om stykklister og formler, som er en sentral del av definisjonen av produktene og produktvariantene.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5a24136c9fad3f1de68158cbd14a60b0ebd147b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211704"
---
# <a name="bills-of-materials-and-formulas"></a>Stykklister og formler

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om stykklister og formler, som er en sentral del av definisjonen av produktene og produktvariantene. Stykklister og formler angir nødvendige materialer eller ingredienser for et bestemt produkt. Formler kan også angi koprodukter og biprodukter som er mottatt i en bestemt produksjonskontekst. 

<a name="bills-of-materials"></a>Stykklister
------------------

En stykkliste (BOM) definerer komponentene som kreves for å produsere et produkt. Komponentene kan være råmaterialer, halvfabrikata eller ingredienser. I noen tilfeller kan det refereres til tjenester i en stykkliste. Stykklister beskriver imidlertid vanligvis *materialressursene* som kreves.  

Når den kombineres med en rute eller produksjonsflyt som beskriver operasjonene og ressursene som kreves for å lage et produkt, danner stykklisten grunnlaget for beregning av estimert kost for produktet.  

En stykkliste er en enkeltenhet som beskrives med følgende informasjon:

-   BOM-ID
-   Navn på stykklisten
-   Stykklistelinjene som beskriver komponentene og ingrediensene
-   Stykklisteversjoner, som definerer produktet og perioden som stykklisten kan brukes i

Én stykkliste beskriver ett nivå som identifiseres med en unik ID. Komponenter kan ha sine egne stykklister som stykklisteversjoner refererer til. Du kan vise og redigere hele hierarkiet med stykklister for et bestemt produkt i stykklisteutforming.

### <a name="formulas-co-products-and-by-products"></a>Formler, koprodukter og biprodukter

En formel er en undertype av stykklister som vanligvis brukes til prosessproduksjon. I tillegg til komponenter og ingredienser beskriver en formel koprodukter og biprodukter. I den faktiske versjonen krever definisjonen av koprodukter og biprodukter for formelen formelversjonen. En formel er vanligvis definert for ett bestemt ferdig produkt (et formel- eller planleggingselement) som er definert i formelversjonen.

### <a name="boms-in-the-product-lifecycle"></a>Stykklister i livssyklusen for produktet

I livssyklusen for produktet kan mange typer stykklister opprettes av ulike årsaker:

-   **Stykkliste for skisse/utkast** – Denne stykklisten gir et estimatutkast for nødvendig materiale i en tidlig utformingsfase, og gjør det enklere å beregne et grovt anslag for kostnad og estimerte produktattributter. Denne stykklisten brukes vanligvis ikke i ERP (Enterprise Resource Planning).
-   **Stykkliste for ingeniørarbeid** – Denne stykklisten brukes vanligvis når du utformer produkter som er basert på eksisterende produktporteføljer. Stykklister for ingeniørarbeid er strukturert for å forenkle utformingsprosessen og gruppere komplekse produkter i konstruksjonsmoduler. Når det gjelder enkle produkter, går det kanskje an å bruke stykklister for ingeniørarbeid i den faktiske produksjonsprosessen. Når det gjelder andre produkter, må imidlertid stykklisten for ingeniørarbeid konverteres til en faktisk produksjonsstykkliste. Vanligvis vises stykklister for ingeniørarbeid som fantomer i stykklistehierarkiet. Selv om stykklister for ingeniørarbeid kan brukes til planlegging og utførelse av produksjonsoperasjoner, kan denne tilnærmingsmåten føre til ineffektivitet, særlig i gjentatte operasjoner der mange ordrer opprettes.
-   **Stykkliste for planlegging** – Denne stykklisten brukes til å planlegge materialbehov. Behovet for komponenter og ingredienser beregnes basert på behovet for de ferdige produktene. Slik som stykklister for etterkalkulering kan stykklister for planlegging representere en bestemt blanding av materiale som brukes i en periode.
-   **Produksjonsstykkliste** – Dette er den faktiske stykklisten som brukes i en bestemt produksjon. En produksjonsstykkliste må ta hensyn til de faktiske ressursene som brukes til å produsere produktet. Når en produksjonsordre, partiordre eller Kanban opprettes, blir de mange nivåene med stykklister som vises som fantomer, slått sammen til ett nivå og fordelt over operasjonene for ordren.
-   **Stykkliste for etterkalkulering** – Denne stykklisten brukes til å beregne estimert kost for et produkt. Du kan for eksempel bruke en stykkliste for etterkalkulering når standardkost brukes, eller når den estimerte planlagte kostnaden for et bestemt produkt beregnes. Stykklister for etterkalkulering kan referere til en bestemt blanding av materialer og ressurser som forventes å bli brukt. Du kan derfor bruke stykklisten for etterkalkulering til å opprette en representativ estimert kost for en periode og unngå avvik over tid.

Hvilke typer stykkliste som faktisk brukes i en implementering, er avhengig av implementeringen og også forretningsscenarier og behov. I enkle implementeringer kan en stykkliste for planlegging, produksjonsstykkliste og stykkliste for etterkalkulering modelleres som én stykkliste. Et større sett med stykklistetyper blir sannsynligvis nødvendig i miljøer med hyppige tekniske endringer og flere alternative ruter.

### <a name="approval-of-boms-and-formulas"></a>Godkjenning av stykklister og formler

Hver stykkliste og formel kan godkjennes eller ikke godkjennes separat. Godkjenning av en stykkliste eller formel skjer vanligvis når den første relevante stykklisteversjonen er godkjent. I enkelte forretningsscenarier kan imidlertid disse godkjenningene være ulike trinn i prosessen og kan omfatte ulike prosesseiere.  

Legg merke til at hvis en stykkliste ikke godkjennes, blir alle tilknyttede stykklisteversjoner også ikke godkjent.

## <a name="bom-and-formula-versions"></a>Stykkliste- og formelversjoner
Hvis du vil knytte en bestemt stykkliste eller formel til en produktvariant som kan produseres, må du opprette en stykkliste- eller formelversjon. Gyldigheten til stykklisteversjoner og formelversjoner kan begrenses etter periode, antall, område, bestemte produktdimensjoner og andre kriterier. Formelversjoner har ytterligere viktige attributter, for eksempel avkastning, koprodukt- og biproduktdefinisjoner og kostnadsdistribusjonsinstruksjonene for formelen.

### <a name="approval-of-bom-and-formula-versions"></a>Godkjenning av stykkliste- og formelversjoner

Før en stykklisteversjon kan brukes i planleggingen eller produksjonsprosessen, må den godkjennes. Når en stykklisteversjon er godkjent, kan den tilknyttede stykklisten også godkjennes, avhengig av brukerens valg og godkjenningsrettigheter. Legg merke til at en stykklisteversjon bare kan godkjennes hvis den tilknyttede stykklisten selv er godkjent.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Aktivering av standard stykkliste- eller formelversjon

Hvis du vil angi en bestemt stykkliste eller formel som standard stykklisteversjon eller formelversjon som skal brukes av hovedplanlegging eller brukes til å opprette produksjonsordrer, må du aktivere versjonen. Når en versjon er aktivert, kontrolleres unikheten i versjonen for de angitte betingelsene (for eksempel periode, område eller antall). Du får en feilmelding hvis versjonen som du prøver å aktivere, er i konflikt med en versjon som allerede er aktiv. Du må deretter enten deaktivere versjonen som er i konflikt, eller endre versjonsbegrensningene (vanligvis perioden) for å unngå en tvetydig aktivering.

### <a name="product-change-with-case-management"></a>Produktendring med saksbehandling

Produktendringssaken for godkjenning og aktivering av nye eller endrede stykklister og stykklisteversjoner gjør det enkelt å få en oversikt over begrensningene for stykklisteversjonen. Du kan også godkjenne og aktivere alle stykklister og formler som er knyttet til en bestemt endring for én aktiveringsdato.

### <a name="alternative-bom-versions"></a>Alternative stykklisteversjoner

Noen ganger skal ikke den aktive stykklisteversjonen eller formelversjonen brukes i prognoser, salg eller et overordnet produkt. I slike tilfeller kan du velge en bestemt godkjent stykkliste som en del av behovet (prognoselinje, salgslinje eller stykklistelinje) hvis det finnes en godkjent stykklisteversjon eller formelversjon for den alternative stykklisten eller formelen.  

Når planlagte ordrer, produksjonsordrer eller Kanbaner opprettes, kan planleggeren eller arbeidslederen bruke en godkjent stykklisteversjon som er gyldig på ønsket dato for planlagt produksjon til å planlegge eller produsere et bestemt produkt. Stykklisteversjonen som brukes, trenger ikke å aktiveres som standard stykklisteversjonen.

## <a name="bom-and-formula-lines"></a>Stykkliste- og formellinjer
En stykklistelinje opprettes for hvert materiale, hver tjeneste eller hver ingrediens. Linjen definerer det planlagte forbruket av den angitte produktvarianten, og definerer også ulike attributter som er knyttet til det planlagte forbruket.  

Stykklistelinjer kan ha følgende linjetyper: **Vare**, **Fantom**, **Tilknyttet forsyning**, **Leverandør**.

### <a name="item"></a>Vare

Velg linjetypen **Vare** for materialer eller tjenester som forbrukes direkte, og som ikke krever ytterligere nedbrytning eller tilknyttet forsyning.

### <a name="phantom"></a>Fantom

Velg linjetypen **Fantom** når du vil bryte ned eventuelle stykklistevarer på lavere nivå som er på stykklistelinjen. I hovedplanlegging, i planlagt kostnadsberegning eller i estimering av en produksjonsordre som bruker stykklistelinjer av typen **Fantom**, erstattes den overordnede stykklistelinjen som refererer til en produktvariant som har en fantomstykkliste av komponentvarene som er oppført som stykklistelinjer i denne stykklisten, i henhold til hva som er fastsatt av den gjeldende aktive stykklisteversjonen for denne produktvarianten. Hvis produktvarianten har en gjeldende aktiv rute, flettes operasjonene i denne ruten med den overordnede ruten.  

Legg merke til at fantomer vanligvis brukes til å forenkle konstruksjonsprosessen. Omfattende bruk av fantomstykklister på mange nivåer påvirker ytelsen, særlig i scenarier med mye gjentakende produksjon. For å forbedre ytelsen bør du unngå dype hierarkier med fantomer. Bruk i stedet forhåndsoppdelte produksjonsstykklister og ruter.

### <a name="pegged-supply"></a>Tilknyttet forsyning

Velg linjetypen**Tilknyttet forsyning** når du vil opprette en underproduksjon, en hendelse-Kanban for stykklistelinje eller en direkte bestilling for en produktvariant som stykklistelinjen refererer til. Underproduksjonen, hendelses-Kanbanen eller bestillingen blir opprettet når du estimerer produksjonsordren. Det obligatoriske vareantallet reserveres automatisk for den forbrukende produksjonsordren.

### <a name="vendor"></a>Leverandør

Velg linjetypen **Leverandør** hvis produksjonsprosessen bruker en underleverandør og du vil at en underproduksjon eller bestilling skal opprettes automatisk for underleverandøren.  

**Merknad om underleveranseoperasjoner i en stykkliste:** Tjenesten eller arbeidet som utføres av underleverandøren, må opprettes som en servicevare som spores i beholdning. Du må knytte servicevaren til den overordnede varen som en stykklistelinje. Ruten må inneholde en operasjon som er tilordnet underleverandørens operasjonsressurs.



