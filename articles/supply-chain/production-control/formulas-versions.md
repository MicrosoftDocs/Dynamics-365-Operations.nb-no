---
title: Formler og formelversjoner
description: Dette emnet gir informasjon om formler og formelversjoner. En formel definerer materialer, ingredienser og utfall av en bestemt prosess i prosessproduksjon. Formler brukes til å planlegge og produsere produkter i prosessproduksjon.
author: cvocph
manager: AnnBe
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbffc298ff5d2442092f8f0c987b7e79a7934a84
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "350119"
---
# <a name="formulas-and-formula-versions"></a>Formler og formelversjoner

[!include [banner](../includes/banner.md)]

En formel definerer materialer, ingredienser og utfall av en bestemt prosess i prosessproduksjon. Sammen med den tilsvarende ruten definerer formelen hele prosessen i prosessproduksjon. Formler brukes til å planlegge og produsere produkter i prosessproduksjon.

En formel består av ingrediensene og mengdene som kreves for å produsere en bestemt mengde av en formelobjekt. Avhengig av oppgaven du utfører, kan du få tilgang til formelfunksjonalitet fra Lager- og lagerstyring eller Produktinformasjonstyring.

## <a name="formulas-and-formula-lines"></a>Formler og formellinjer
En formel består av en eller flere formellinjer som identifiserer ingrediensene eller elementene som utgjør formelen. En formellinje kan inneholde artikler om stykklister, formelelementer, catchvektvarer, kjøpte varer, samprodukter eller biprodukter. Fordi mange elementer brukes i flere produkter, kan et element brukes i mer enn én formel.

Et eksempel på en formel er oppsrkiften for en sjokoladekake. Ingrediensene for denne formelen bruker flere linjer, for eksempel mel, sukker, egg, smør og sjokoladebiter. Ingrediensene for en sjokoladekake inneholder ingredienser som sannsynligvis brukes i andre formler. Når du lager sjokoladekake kan det bli rester, slik som smuler, eller noen av kakene kan stekes for mye eller for lite. Disse elementene kan settes opp som samprodukter eller biprodukter, avhengig av produksjonsoperasjonene.

Når du oppretter en formellinje, bruker du linjetypen til å angi hvordan systemet skal håndtere linjen når du kjører hovedplanlegging og produserer batchordrer. Hver linjetype gir et forskjellig resultat. Den følgende tabellen beskriver linjetypene du kan velge: 

| Linjetype     | beskrivelse  |
|---------------|--------------|
| Element          | Velg **Element** når elementet er en råvare eller en halvfabrikate som plukkes fra lageret eller når elementet er en tjeneste. |
| Fantom       | Velg **Phantom** når du vil eksplodere eventuelle lavere nivåformelelementer som finnes på formellinjer. Når du estimerer batchordren, og formelelementer utvides, oppføres komponentelementene som som formellinjer på batchordren. I tillegg tilføres de tilsvarende ruter til produksjonsruten. Formelelementer utvides ved hjelp av gjeldende konfigurasjon. Når du bruker **Phantom**-linjetype, kan du håndtere produksjon og målkonfigurasjon som oppstår ved ulike formelnivåer. Hvis du velger **Phantom** for et produkt på hurtigkategorien **Ingeniør** i siden **Frigitte produktdetaljer** og deretter bruker dette produktet i en formel, vil linjetypene for formellinjen endres til **Phantom**. Du kan ikke velge **Phantom** for catchvektvarer eller for elementer hvor produksjonstypen er et **Samprodukt**, **Biprodukt** eller **Planlagt element**. |
| Tilknyttet forsyning | Velg **Festet forsyning** for å lage en batchordre, produksjonsordre, kanban, overføringsordre eller innkjøpsordre for ingrediensen som finnes på formellinjen. Den relaterte ordren er bestemt ut fra innstillingene for standardbestillingen og produksjonstypen av ingrediensen, og opprettes når du estimerer batchordren. De nødvendige ingrediensmengder er reservert for batchordren. |
| Leverandør        | Velg **Leverandør** hvis produksjonsprosessen bruker en underleverandør, og du vil opprette en underproduksjon eller innkjøpsordre for underleverandøren. Tjenesten eller arbeidet som underleverandøren utfører, må opprettes ved hjelp av et formelelement eller tjenesteelement. Du kan feste elementet til det overordnede elementet som en formellinje. Ruten må inneholde en operasjon som er tilordnet underleverandørens operasjonsressurs. Denne operasjonen festes til formellinjen ved å bruke **Oper. nr.** . |

## <a name="formula-versions"></a>Formelversjoner
Når du oppretter en ny formel, må du først opprette en formelversjon før du legger til linjeposter og deres spesifikke egenskaper. Hver formel må ha minst én versjon. **Godkjent**-knappen på en formelversjon blir bare tilgjengelig etter at en versjonsoppføring har blitt lagret. Hver formelversjonsoppføring er knyttet til en eller flere samprodukter og biprodukter, som kan produseres etter hvert som du produserer det ferdige produktet. Mange produkter kan lages fra de samme ingrediensene i ulike batchstørrelser, i flere, eller ved å bruke ulikt utbytte. Du kan opprette så mange versjoner av en formel som du trenger.

For å administrere flere aktive formelversjoner, bruk effektive datoperioder eller "fra" kvantitetsfelt. Flere aktive formelversjoner kan bare eksistere dersom datoperioden og "fra" mengden ikke overlapper.

I motsetning til stykklister (BOM), hvor en BOM ofte er assosiert med mange BOM-versjoner, finnes det kun én formelversjon per formel. Husk at bare én formelversjon kan aktiveres for dekningsmålene og kvantiteten for et gitt produkt. Imidlertid kan mange formelversjoner eksistere av andre grunner, og du kan manuelt velge dem når du oppretter en batchordre.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Godkjenn og aktiver formler og formelversjoner
Formler og formelversjoner må godkjennes før de kan brukes til planlegging og produksjon. Formler aktiveres vanligvis før de brukes. Under produksjonen kan du imidlertid velge en formelversjon som er godkjent, men som ikke er aktivert.

For å hjelpe å sikre en formel eller formelversjon kan du sette **Hindre redigering** og **Hindre fjerning av godkjennelse**-paremetere på **Parametere for produksjonskontroll**-siden.

Hvis du velger **Hindre redigering** og formelen er godkjent vil ingen felt på formellinjen kunne slettes eller redigeres. Men hvis du fjerner godkjenningen av formelen, kan du slette og endre formellinjene. Du kan også opprette nye formler og nye formelversjoner.

Hvis du velger **Hindre fjerning av godkjennelse** kan du ikke fjeren godkjennelsen for en godkjent formel eller formelversjon. Du kan imidlertid opprette nye formler og nye formularversjoner, og du kan fjerne aktiveringen av formelversjonen.

Du kan legge til flere kontrollnivåer ved å bruke funksjonen for elektronisk signering. Når en bruker er satt opp slik at en elektronisk signatur kreves ved formelgodkjenning, vises en **Signatur**-side når formelen er aktivert. Brukeren må være autorisert til å signere elektronisk, og sertifikatet må valideres før endringen kan forpliktes. Hvis signaturen ikke kan godkjennes, nekter godkjenning eller fjerning av godkjenning, og endringen som initierte godkjenning eller fjerning av godkjenning, returneres godkjennelsen til sin opprinnelige tilstand.

## <a name="use-the-scalable-feature"></a>Bruk funksjonen Skalerbar
Skalerbar-funksjone er kun tilgjengelig hvis alle elementkomponentene i formelen er satt til **Variabelt forbruk** Denne funksjone er ikke tilgjengelig for elementkomponenter som er satt til **Fast forbruk** eller **Trinnvist forbruk**. Når Skalerbar-funksjonen brukes, hvis du endrer en ingrediens i en formel, vil mengden andre ingredienser du velger justeres tilsvarende. Størrelsen på formelen justeres også. På samme måte, hvis du endrer formelformat, endres mengden av alle skalerbare ingredienser. Denne funksjonen er spesielt beregnet for opprettelse av formler og vedlikehold. Det indikerer ikke om mengden av en ingrediens skal skaleres opp eller ned på en batchordre.

## <a name="use-step-consumption"></a>Bruk Trinnvist forbruk
Trinnvist forbruk eliminerer kravet om at du må legge inn en mengde i kategorien **Formellinje** for en ingrediens. I stedet er Trinnvist forbruk konfiguert så den har **Fra serier**-verdi og en **Mengde**-verdi. Informasjonen fra Trinnvist forbruk per serieoppføring som tilfredstiller mengden for batchordren velges. Trinnvist forbruk er nyttig når forbruksrates ikke er lineær med hensyn til batchordrestørrelse og øker kun kravet når en bestemt mengdegrense er oppfylt. For å aktivere denne funksjonen for en ny formel, se under **Forbruksberegning**-gruppen, endre formelinnstillingen for gjeldende ingrediens fra **Standard** til **Trinnvis**. Du spesifiserer forbruksmetoden i kategorien **Oppsett** i siden **Formellinje**.
