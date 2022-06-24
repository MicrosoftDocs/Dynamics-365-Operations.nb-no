---
title: Vanlige spørsmål om lageretterkalkulering
description: Denne artikkelen gir noen svar på vanlige spørsmål om lageretterkalkulering i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 467839b1d0ca6788a92ae60d46686374d0a58046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850851"
---
# <a name="inventory-costing-faq"></a>Vanlige spørsmål om lageretterkalkulering

[!include [banner](../includes/banner.md)]

Denne artikkelen gir noen svar på vanlige spørsmål om lageretterkalkulering i Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Lagerlukking, justeringer og omberegning

### <a name="is-the-inventory-close-required"></a>Er lagerlukking nødvendig?

Hvis du har tenkt å bruke funksjonen for lagerarkivering, er lagerlukkingen nødvendig. Hvis du ikke planlegger å bruke funksjonen for lagerarkivering, anbefaler vi på det sterkeste at du fortsatt kjører lagerlukkingen, uansett hvilke kostnadsmodeller du bruker.

### <a name="how-often-should-the-inventory-close-be-run"></a>Hvor ofte skal lagerlukking kjøres?

Lagerlukking bør kjøres minst én gang per finansperiode. Hvis for eksempel finans er satt til en kalendermånedsbasert regnskapskalender, bør du kjøre lagerlukking én gang per måned.

### <a name="is-the-inventory-recalculation-required"></a>Er omberegning av lager nødvendig?

Nei, omberegning av lager er ikke nødvendig. Hvis du bruker en periodisk kostnadsmodell, for eksempel først inn, først ut (FIFO), sist inn, først ut (LIFO) eller avveid gjennomsnitt, bør du nøye vurdere om du vil kjøre omberegningen av lager. Det kan gi mer nøyaktige kostnader i de heuristiske modellene du har valgt.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Hvor ofte skal omberegning av lager kjøres?

Hvis du planlegger å kjøre lageromberegningen, anbefaler vi at du vurderer å kjøre den daglig som en satsvis prosess. Hvis organisasjonen ikke krever hyppig rapportering av lagerverdiene for periodiske kostnadsmodeller, kan du vurdere å kjøre lageromregningen sjeldnere.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Når skal jeg bruke lagerbeholdningsjustering på lukkings- og justeringssiden?

Lagerbeholdningsjustering kan bare justeres etter en lagerlukking er fullført. Den kjøres vanligvis for datoen etter siste lukking. Beholdningsjustering kan bare justere lager som fremdeles er tilgjengelig fra datoen når du kjører justeringen.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Når skal jeg bruke lagertransaksjonsjusteringen på lukkings- og justeringssiden?

Du bør bruke lagertransaksjonsjusteringen før du kjører en lagerlukking. Den brukes som regel til å korrigere feil mottak. Du kan ikke postere lagertransaksjonsjusteringen etter at en lagerlukking er kjørt og transaksjonen er utlignet.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Behandles bestillingsreturer som andre avganger under lagerlukking?

Ja. Et bestillingsmottak er et mottak som utlignes mot et mottak i den heuristiske modellen du velger for varen. Hvis du bruker en periodisk kostnadsmodell, kan du bruke merking til å overstyre den heuristiske kostnaden.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Hva skjer med salgsordrereturer under lagerlukking?

Når du kjører lagerlukkingen, behandles en salgsordreretur som et mottak i lageret. Avganger utlignes mot lageret basert på den heuristiske modellen du velger for varen.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Hvilken kostpris brukes på en salgsordreretur?

Når du oppretter en retur som er knyttet til en salgsordre, kopieres verdien av **Enhetspris**-feltet fra den opprinnelige salgsordren, og **Returkostpris**-feltet på returen settes til den justerte kostprisen fra den opprinnelige lagertransaksjonen for salgsordrelinjen som returneres. Hvis alternativet **Åpen verdi** for den relaterte lagertransaksjonen er satt til *Ja*, kan lagerlukkingen forårsake oppdateringer av avgangskostnaden på den opprinnelige salgsordren. Feltet **Returkostpris** oppdateres ikke i dette scenariet. Når du posterer en følgeseddel for en returordre, vil imidlertid systemet kontrollere kostprisen og bruke den oppdaterte kostnaden på returlagertransaksjonen.

Når det gjelder retur av en vare med standard kostpris som er relatert til en salgsordre, bruker systemet standardkostnaden fra tidspunktet for den opprinnelige salgsordren, selv om en ny standard kostpris er aktiv for varen.

Når du oppretter en retur som ikke er knyttet til en salgsordre, settes **Returkostpris**-feltet til den aktive vareprisen du har for varen i området du oppretter returordren for. Hvis du ikke har en aktiv kostpris i en kostversjon for varen, vil verdien være 0 (null). Hvis du lar verdien være 0 (null), får du en advarsel som angir at returparti-IDen eller returkostprisen ikke er angitt.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Hva er forventet ytelse for lagerlukking?

Mange faktorer kan påvirke ytelsen til lagerlukking. Disse faktorene omfatter det totale antallet varer, det totale antallet transaksjoner i perioden, lagermodellene du bruker, og antallet partihjelpeprogrammer som du konfigurerer i parameterne for beholdnings- og lagerstyring. Du kan forvente at lukkingen kan ta så lite som et par minutter eller så mye som flere timer. Det finnes ingen bestemt veiledning om hvor lang tid det skal ta å kjøre lukkingen. Du bør definere ikke-funksjonelle forretningskrav for lagerlukkingsytelsen og arbeide nøye med partneren din for å definere planen for kjøring av lagerlukkingsprosessen. Hvis du får uventet lav ytelse ved lagerlukkingsprosessen, bør du åpne en støtteforespørsel.

## <a name="costing-sheet-and-indirect-costs"></a>Etterkalkuleringsark og indirekte kostnader

### <a name="which-costing-models-support-the-costing-sheet"></a>Hvilke etterkalkuleringsmodeller støtter kostark?

Selv om kostarket vanligvis brukes i organisasjoner som bruker standardkost, kan du bruke det med alle kostnadsmodeller som er tilgjengelige i Supply Chain Management.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Kan jeg ha flere kostark for forskjellige deler av organisasjonen?

Nei Du kan bare ha ett kostark per juridisk enhet.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Kan jeg ha forskjellige kostark for hvert område?

Nei, du har ikke forskjellige kostark for hvert område. Du kan bare opprette ett kostark for hver juridiske enhet. Du kan imidlertid konfigurere totale noder, kostnadsgrupper eller indirekte kostnadsnoder per område. Denne konfigurasjonen er en manuell prosess, og du må vedlikeholde hierarkiet og varetilordningene i kostarket når det skjer organisasjons- eller driftsendringer. Hvis en enkelt vare produseres eller kjøpes på mer enn ett område, finnes det ingen mekanisme som gjør det mulig å behandle varen ulikt på kostarket for hvert område. Legg også merke til at alle indirekte kostnadskoder har en sats eller et tillegg som er definert i kostnadsversjonen. Kostnadene du definerer, er alltid stedsbestemte.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Kan jeg deaktivere og aktivere versjoner av kostarket?

Selv om ingen detaljert versjonshistorikk beholdes for kostarket, kan du gjøre endringer i kostarket og deretter, når du er klar, lagre og validere det. Det finnes ingen mekanisme som gjør det mulig å gå tilbake til en eldre versjon av kostarket eller vise endringene som ble gjort i kostarket. Hvis du starter endringer og ikke vil at de skal tre i kraft, kan du lukke siden uten å lagre og validere endringene. Du blir bedt om å forkaste endringene.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Kan jeg opprette indirekte kostnader for hver vare?

I kostarket kan du opprette indirekte kostnadskoder der feltet **Nodetype** er satt til *Tilleggsavgift*, *Sats* eller *Basert på utdataenhet*. Du kan deretter definere satsen eller tillegget, slik at det er spesifikt for et varenummer. Legg til en rad i rutenettet i hurtigkategorien **Sats** eller **Tilleggsavgift**. Sett **Gyldig for**-feltet til *Tabell* og **Relasjon**-feltet til det bestemte varenummeret.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Kan jeg opprette en indirekte kostnad som ikke er relatert til en bestemt vare?

Ja. Du kan opprette en indirekte kostnadskode der **Nodetype**-feltet er satt til *Basert på utdataenhet*. Du kan deretter sette feltet **Undertype** til *Kvalitet*, *Vekt* eller *Volum* for å angi antallet, vekten eller volumet for varen du produserer. Satsen du angir i hurtigkategorien **Sats**, brukes på undertypen du har valgt. Du angir for eksempel feltet **Undertype** til *Antall* og feltet **Sats** til *USD 1.00*, og deretter oppretter du en produksjons- eller partiordre for et antall på 10. I dette tilfellet blir den indirekte kostnaden som blir lagt til ferdigvaren, 10.00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Kan jeg bruke kostarket til å dele produksjonskostnadene etter timer og materialer?

Ja. Du kan opprette **Total**-noder på kostarket for å skille kostnadene ved hjelp av en hvilken som helst gruppering du velger. Du kan for eksempel opprette én **Total**-node med navnet *Timer* og en annen kalt *Materialer*. Legg til hver kodegruppe som er knyttet til timene, under **Timer**-noden. Legg til hver kostgruppe som er knyttet til materialene, under **Materialer**-noden.

## <a name="dimension-groups"></a>Dimensjonsgrupper

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Kan jeg administrere kostnaden på parti- eller serienummernivå?

Ja, hvis du bruker en periodisk kostnadsmodell, for eksempel FIFO, LIFO, LIFO-dato, avveid gjennomsnitt eller dato for avveid gjennomsnitt, kan du aktivere alternativet for **økonomisk lager** for dimensjonen **Parti** eller **Serienummer** i sporingsdimensjonsgruppen for å spore kostnader på et detaljert nivå.

### <a name="can-i-manage-costs-at-the-location-level"></a>Kan jeg administrere kostnader på lokasjonsnivå?

Nei, du kan ikke aktivere alternativet **Økonomisk lager** for **Lokasjon**-dimensjonen i lagringsdimensjonsgruppen. Hvis organisasjonen må spore kostnader på et mer detaljert nivå, kan du vurdere om du kan opprette virtuelle lagre, og velge alternativet **Økonomisk lager** for dimensjonen **Lager** i lagringsdimensjonsgruppen.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Skal jeg aktivere prosessalternativet Bruk lagerstyringsprosesser for lagringsdimensjonsgruppen?

Hvis du tror at du kanskje vil bruke de avanserte lagerstyringsfunksjonene i fremtiden, bør du aktivere alternativet **Bruk lagerstyringsprosesser**. Når du har lagret en lagringsdimensjonsgruppe, kan du ikke lenger endre innstillingen for **Bruk lagerstyringsprosesser** for den. Hvis du bestemmer deg for å bruke lagerstyringsprosesser senere, må du opprette et nytt lager der alternativet er aktivert. Det finnes ingen automatisert prosess som du kan bruke til å flytte alt lageret fra ett lager til et annet lager, eller til å kopiere tilknyttede konfigurasjoner til et nytt lager.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Kan jeg aktivere Bruk lagerstyringsprosesser for lagringsdimensjonsgruppen selv om jeg ikke planlegger å bruke avanserte lageraktiviteter?

Ja, selv om du ikke planlegger å bruke de avanserte lagerstyringsfunksjonene, kan du aktivere alternativet **Bruk lagerstyringsprosesser** for lagringsdimensjonsgruppen. For å opprette og behandle transaksjoner må du fullføre minimumskonfigurasjonen, for eksempel reserveringshierarkier og enhetssekvensgrupper. Innstillingene for avanserte lageraktiviteter ignoreres imidlertid vanligvis når du behandler plukklister, følgesedler og mottakssedler manuelt (for eksempel på salgsordre- og bestillingssidene).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Når bør jeg aktivere alternativet Fysisk beholdning for en lagrings- eller sporingsdimensjonsgruppe?

Du bør aktivere alternativet **Aktuell beholdning** for lagring og sporing av dimensjonsgrupper når du må holde detaljerte lagerposter basert på denne dimensjonen. Vanligvis spores også en hvilken som helst dimensjon som er aktiv, fysisk. Derfor spores alle mottak, avganger eller bevegelser av lageret av den valgte dimensjonen. Hvis en dimensjon ikke er obligatorisk (for nummerskiltet), kan du aktivere alternativet **Tomt mottak tillatt** og **Tom avgang tillatt** for at brukere skal kunne motta, utstede eller flytte beholdningen selv om dimensjonen ikke er angitt.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Når bør jeg aktivere alternativet Økonomisk lager for en lagrings- eller sporingsdimensjonsgruppe?

Du bør aktivere alternativet **Økonomisk beholdning** for lagrings- og sporingdimensjonsgrupper når du må holde detaljerte finansposter basert på denne dimensjonen. **Område**-dimensjonene spores alltid økonomisk, mens andre dimensjoner er valgfrie for økonomisk sporing. Hvis du bruker en periodisk kostnadsmodell, for eksempel FIFO, LIFO eller veid gjennomsnitt, angir aktivering av alternativet **Økonomisk lager** for en dimensjon at du bare vil foreta utligninger i tilfeller der mottak og avgang har de samme dimensjonsverdiene. Hvis du for eksempel aktiverer alternativet **Økonomisk lager** for **Lager**-dimensjonen, har du forskjellige kostnader i hvert lager, og mottak og avganger fra forskjellige lagre kan ikke utlignes.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Kan jeg foreta endringer i et produkt, en lagring eller en sporingsdimensjonsgruppe etter at det finnes transaksjoner?

Når du har opprettet en varemodellgruppe, kan du endre innstillingen for feltene **Dekningsplanlegg etter dimensjon**, **For innkjøpspriser** og **For salgspriser** hvi det er merket av for **Aktiv** for en dimensjon i varemodellgruppen. Ingen andre endringer er tillatt. Du kan for eksempel ikke aktivere eller deaktivere alternativene **Aktiv**, **Tom avgang tillatt**, **Tom tilgang tillatt**, **Fysisk beholdning** og **Økonomisk lager**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Kan jeg endre produktet, lagringen eller sporingsdimensjonsgruppen for et frigitt produkt?

Hvis lagerbeholdningen for et produkt er 0 (null), og alternativet **Verdi åpen** er satt til *Nei* for alle lagertransaksjonene, kan du endre lager- og sporingsdimensjonsgruppene på den frigitte produksjonssiden. Du kan ikke endre produktdimensjonsgruppen etter at posten er opprettet.

## <a name="item-model-groups"></a>Varemodellgrupper

### <a name="when-should-i-enable-the-stocked-product-option"></a>Når bør jeg aktivere alternativet Lagerført produkt?

Du bør aktivere alternativet **Lagerført produkt** for alle varer som spores i lageret. Når dette alternativet er aktivert, beholdes detaljerte lagertransaksjoner som sporer mottak og avgang av varen. Dette alternativet er vanligvis aktivert for alle materielle varer som du for eksempel oppbevarer i lageret. Du bør også aktivere dette alternativet hvis du planlegger å legge til en ikke-materiell vare, for eksempel en servicevare, i stykklistene eller formler. Hvis du ikke aktiverer alternativet **Lagerbeholdning**, spores ingen lagertransaksjoner i underfinans for beholdning, og varekostnadene blir vanligvis utgiftsbelagt i økonomimodulen. Dette alternativet brukes ofte for butikkutstyr eller tjenester som ikke er inkludert i stykklistene eller formlene.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Når bør jeg aktivere alternativet Poster aktuell beholdning?

Alternativet **Poster aktuell beholdning** aktiveres vanligvis når alternativet **Lagerført produkt** er aktivert. Når du aktiverer dette alternativet, sporer systemet den fysiske oppdateringen til varen på lagertransaksjonen. Dette alternativet brukes i koordinering med parametere i Leverandør, Kunde og Produksjonskontroll som angir at den fysiske oppdateringen skal opprette et bilag. Du aktiverer vanligvis dette alternativet når du vil at finans skal oppdateres hver gang du oppdaterer lageret fysisk. Hvis Supply Chain Management ikke er ditt system for økonomi, bør du deaktivere dette alternativet.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Når bør jeg aktivere alternativet Poster økonomisk lager?

Alternativet **Poster økonomisk lager** aktiveres vanligvis når alternativet **Lagerført produkt** er aktivert. Dette alternativet brukes i koordinering med parametere i Leverandør, Kunde og Produksjonskontroll som angir at den økonomiske oppdateringen skal opprette et bilag. Du vil vanligvis aktivere dette alternativet når du vil at finans skal oppdateres hver gang du oppdaterer lageret økonomisk (for eksempel ved å fakturere salgsordrer bestillinger eller avslutte en produksjonsordre). Hvis Supply Chain Management ikke er ditt system for økonomi, bør du deaktivere dette alternativet.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Når bør jeg aktivere alternativet Poster til utsatt inntektskonto ved salgslevering?

Du bruker alternativet **Poster til utsatt inntektskonto ved salgslevering** for å angi om du vil gjenkjenne omsetning i økonomimodulen når du posterer en følgeseddel for en salgsordre. Dette alternativet brukes vanligvis når du lang forsinkelse mellom følgeseddelen og fakturaen på en salgsordre, eller når det ikke er mulig å fakturere alle salgsordrene i perioden. Vanligvis deaktiverer du dette alternativet hvis du posterer salgsordrefakturaene rett etter at du har postert følgeseddelen. På denne måten kan du unngå å generere ekstra økonomimodulposteringer som tilbakeføres umiddelbart når du fakturerer en salgsordre.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Når bør jeg aktivere alternativet For avsetning av gjeld på produktkvittering?

I de fleste organisasjoner vil du aktivere alternativet **Gjeldsavsetning på mottaksseddel** for alle varemodellgrupper, uansett om du har et produkt som er på lager eller ikke er på lager. Dette alternativet brukes til å postere en avsetning til økonomimodulen, basert på produktmottakspris. Fordi det vanligvis er forsinkelse mellom postering av produktmottaket for en bestilling og postering av fakturaen, må de fleste organisasjoner gjenkjenne gjelden på balansen for å overholde lokale regler, for eksempel GAAP (Generally Accepted Accounting Practices). Hvis Supply Chain Management ikke er ditt system for økonomi, bør du deaktivere dette alternativet. Hvis organisasjonen bruker innkjøpskategorier på bestillinger, kan du styre avsetningskravet ved å aktivere alternativet **Avsett innkjøpsutgift ved mottak** for kategoripolicyregelen på siden **Innkjøpspolicyer**.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Hvordan kan jeg hindre en bruker i å postere produktkvitteringen for bestillingen hvis registrering av mottak ennå ikke er postert?

Du kan hindre en bruker i å postere et produktmottak for en bestilling hvis det ikke er registrert en bestilling ennå, ved å aktivere alternativet **Registreringsbehov** for varemodellgruppen. Dette alternativet brukes vanligvis i organisasjoner som bruker en mottaksprosess i to trinn, eller i scenarier der du må registrere et bunke- eller serienummer, for eksempel på varene du mottar. Alternativet **Registreringsbehov** gjelder *alle* lagertilganger for en vare, ikke bare for bestillinger. Den gjelder for eksempel for en lagerjournal som har et positivt antall og en ferdigmeldingsjournal for en produksjonsordre.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Hvordan kan jeg hindre en bruker i å postere en bestillingsfaktura hvis en mottaksseddel ennå ikke er postert?

Du kan hindre en bruker i å postere en produktfaktura for en bestilling hvis en bestillingsmottaksseddel ikke har oppstått enda, ved å aktivere alternativet **Mottar krav** for varemodellgruppen. Dette alternativet brukes vanligvis i organisasjoner som krever at mottak skal gjenkjennes fysisk i økonomimodulen for avsetning. Alternativet **Mottar krav** gjelder for *alle* lagertilganger for en vare, ikke bare for bestillinger. Den gjelder for eksempel for en lagerjournal som har et positivt antall og en ferdigmeldingsjournal for en produksjonsordre. Hvis organisasjonen bruker innkjøpskategorier på bestillinger, kan du styre mottakskravet ved å aktivere alternativet **Mottar krav** for kategoripolicyregelen på siden **Innkjøpspolicyer**.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Hvordan kan jeg hindre en bruker i å postere en følgeseddel for en salgsordre hvis en plukkliste ikke er postert ennå?

Du kan hindre en bruker i å postere en følgeseddel for salgsordre eller faktura hvis en salgsordreplukkliste ikke har oppstått enda, ved å aktivere alternativet **Plukkbehov** for varemodellgruppen. Dette alternativet brukes vanligvis i organisasjoner som utfører en fysisk plukkprosess i lageret (for eksempel ved å bruke lagerets mobilenhet til å utføre plukking). Alternativet **Plukkbehov** gjelder for *alle* lageravganger for en vare, ikke bare salgsordrer. Den gjelder for eksempel for en lagerjournal som har et negativt antall og en plukklistejournal for produksjonsordre.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Hvordan kan jeg hindre en bruker i å postere en salgsordrefaktura hvis følgeseddel for salgsordre ikke er postert ennå?

Du kan hindre en bruker i å postere en salgsordrefaktura hvis en salgsordreplukkliste ikke har oppstått enda, ved å aktivere alternativet **Fratrekkskrav** for varemodellgruppen. Dette alternativet brukes vanligvis i organisasjoner som utfører en fysisk emballasjeprosess i lageret (for eksempel ved å bruke mobilprogrammet Warehouse Management til å pakke eller generere et dokument som skal inkluderes med varene som sendes). Alternativet **Fratrekkskrav** gjelder for *alle* lageravganger for en vare, ikke bare salgsordrer. Den gjelder for eksempel for en lagerjournal som har et negativt antall og en plukklistejournal for produksjonsordre.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Kan jeg hindre at varer som er registrert, blir solgt?

Når en vare er registrert i lageret i Supply Chain Management, er antallet fysisk tilgjengelig for utstedelse i systemet. Hvis varer som er registrert, men ennå ikke mottatt, *ikke* er tilgjengelige for utstedelse av salgsordrer eller produksjonsordrer, kan du for eksempel vurdere å bruke lagerstatus, lagerblokkering, kvalitetsordrer, karanteneordrer eller reserveringsfunksjoner for å administrere forretningsprosessen.

## <a name="production-costing"></a>Produksjon - etterkalkulering

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Kan jeg bruke én kostnadsmodell for råvarer og en annen kostnadsmodell for ferdige varer?

Ja, du kan bruke forskjellige kostnadsberegningsmodeller for hver vare. Det er ikke vanlig at produsenter bruker en periodisk kostnadsberegningsmodell for råvarer, og standardkostnad for halvfabrikata og ferdigvarer.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Hvordan kan jeg redusere administrasjonskostnadene fra maskinkostnader?

For å redusere administrasjonskostnadene må du opprette ressurser og ressursgrupper for hver maskin i henhold til dine forretningsbehov. Hver ressurs eller ressursgruppe kan tilordnes kostnadskategorier for å kontrollere maskinkostnaden. Hver kostnadskategori kan kobles til en kostgruppe, og hver kostgruppe kan brukes som grunnlag for beregning av indirekte kostnader i kostarket.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Hvordan gjenkjenner jeg kostnader som er knyttet til forbruk av strøm (for eksempel vann-, strøm- eller gassforbruk) på kostnadsarket?

Du kan vanligvis gjenkjenne kostnader som er knyttet til forbruk av strøm, på to forskjellige måter:

- Opprett en linje i stykklisten eller formelen. Vanligvis opprettes denne linjen som en servicevare, og du kan angi måleenheten du bruker i forhold til antallet du produserer. På denne måten kan brukeren bruke et annet beløp under produksjonsprosessen. Du kan automatisk bruke varene basert på verdien du velger i **Trekkprinsipp**-feltet.
- Opprett en indirekte kostnad på kostarket. Denne fremgangsmåten brukes vanligvis til å fordele totalkostnad for forbruk av strøm på tvers av produksjonsprosessen. Du kan for eksempel bruke kostgruppen og absorpsjonsgrunnlaget til å skalere forbruket på grunnlag av materialer eller arbeid i ruten.

Du bør velge det beste alternativet, basert på rapporterings-, avstemmings- og driftskravene.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Kan jeg registrere ressursdetaljer i stykklisten eller formelen?

Ressursdetaljer kan bare registreres i en ruteoperasjon. Selv om du kan opprette en servicevare som skal representere en ressurs og tilordne en kostnad for å øke kostnadsberegningen for en ferdigvare, anbefaler vi vanligvis ikke denne fremgangsmåten. I stedet anbefaler vi at du oppretter en enkel rute som har én linje for å spore ressurskostnadene, og konfigurerer operasjonen slik at den forbrukes automatisk enten på begynnelsen eller slutten av produksjonsordren.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Kan jeg vise beregningsdetaljene hvis kostnaden er angitt manuelt?

Nei Hvis du angir prisen manuelt på siden **Varepris**, er ikke knappene **Vis beregningsdetaljer** og **Rapportberegningsdetaljer** tilgjengelige. Hvis du velger knappen **Opprullet kost per kostgruppe** for en kostpris som er angitt manuelt, vises en summert linje, og alle kostnader rulles opp til ferdigvaren.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Beregner systemet avvik på en produksjonsordre når jeg legger inn kostnaden manuelt?

Ja, systemet beregner avvik når du angir en standardkost manuelt. Når du imidlertid angir en standardkostnad manuelt i stedet for å beregne den, regnes all material-, rute- og indirekte kostnadsforbruk i produksjonsordren som et erstatningsavvik. Hvis det er flere avvik, for eksempel forbruk av ekstra materialer eller arbeid, vil de også bli registrert som avvik fra produksjonsstykklisten. Derfor anbefaler vi på det sterkeste at du alltid kjører en beregning for varer som har en stykkliste, en rute eller indirekte kostnader.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Hvordan kan jeg føre avvikene fra en delproduksjonsordre til den overordnede produksjonsordren?

Når du bruker en periodisk kostnadsmodell, for eksempel FIFO, LIFO eller avveid gjennomsnitt, gjenkjennes kostnadene fra en underproduksjon i den heuristiske modellen du har valgt for varene. Hvis du krever faktiske kostnader, må du vurdere å bruke merkingsprinsippet til å angi hvilken delproduksjon som skal utstedes til en overordnet produksjonsordre. Du kan også vurdere å bruke alternativet **Økonomisk lager** for **Parti**- eller **Serienummer**-dimensjonen i sporingsdimensjonsgruppen.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Hvordan påvirker trekkprinsippet forbruk?

Trekkprinsippet for en stykkliste, formel eller rutelinje styrer tidsberegningen og teknikken som brukes til å forbruke varen eller arbeidet. Hvis du velger *Start*, forbrukes varen eller arbeidet automatisk når du starter produksjonsordren. Hvis du velger *Ferdig*, forbrukes varen eller arbeidet automatisk når du rapporterer produksjonsordren som fullført. Hvis du velger *Manuell*, må en bruker plukke materialer manuelt eller registrere tiden i en jobb- eller rutekortjournal. Stykklister og formler har også et *Tilgjengelig på lokasjon*-alternativ. Hvis du velger dette alternativet, forbrukes varene automatisk etter at de er overført til produksjonsgulvlokasjonen.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Hvordan kjører jeg kostnadsberegninger hvis jeg har stykklister eller formler med flere nivåer?

Generelt anbefaler vi at du starter på laveste nivå i stykklistene eller formlene for beregningen. For å gjøre filtreringen enklere når du massekjører kostnadsberegninger, kan du bruke beregningsgrupper for å bidra til å skille produkter. Vi anbefaler også at du kjører den periodiske jobben *Beregn stykklistenivåer på nytt* før du begynner massekjøringskostnadsberegninger. Hver organisasjon bør vurdere produktsammensetningen og definere en strategi som oppfyller de spesifikke behovene til produkt- og stykkliste- eller formelstrukturene.

## <a name="transfer-order-costing"></a>Overføringsordrekostnad

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Finnes det en måte å tildele frakt til en overføringsordrekostnad på?

Du kan legge til tillegg i en overføringsordre for å legge til kostnader. Tilleggskoden definerer debet og kredit for tillegget du legger til. Først må du opprette tilleggskoder i modulen **Beholdningsstyring**. Hvis du vil legge til et tillegg i en overføringsordre, velger du **Tillegg** på overføringsordrelinjen som du vil legge til et tillegg i.

## <a name="variances"></a>Avvik

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Kan jeg behandle avvik på forskjellige måter, basert på området eller lageret?

Det er ingen mulighet til å konfigurere avvikskontoer etter område. Når du bruker standardkost på et frigitt produkt, kan du velge hovedkontoen som brukes til posteringer av standardkostavvik på **Postering**-siden. Du kan velge å konfigurere kontoene for én vare, en varegruppe eller alle varer. Du kan også konfigurere én kostgruppe, en gruppe med kostgrupper eller alle kostgrupper.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Kan jeg skille avvik som er resultatet av valutakurser, fra andre typer avvik?

Hvis et avvik er resultatet av en valutakursdifferanse mellom bestillingsprisen og standardkostnaden for en vare, er det ingen måte å skille valutakursdifferansen fra andre avvik.

## <a name="reporting"></a>Rapportering

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Hvor mange rapportkonfigurasjoner for lagerverdi kan jeg opprette og bruke?

Det er ingen begrensninger på hvor mange rapportkonfigurasjoner for lagerverdi du kan opprette. Du bør evaluere dine spesifikke rapporteringskrav og opprette så mange konfigurasjoner du trenger for å oppfylle disse kravene. Du trenger minst én rapportkonfigurasjon for lagerverdi for å kjøre rapporten eller lagringsalternativet for rapporten.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Kan jeg bruke lagerverdirapporten til å analysere kostnadene for en vare i hvert lager?

Ja. Du kan aktivere alternativet **Vis** eller **Total** for hver **Lager**-dimensjon i rapportkonfigurasjonen for lagerverdi. Rapporten vil imidlertid bare vise verdiene for dimensjoner der alternativet **Økonomisk lager** er aktivert for lagringsdimensjonsgruppen. For andre dimensjoner vil det vises tomme kolonner. Hvis du vil ha mer informasjon, kan du se [Eksempler og logikk for lagerverdirapport](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Hvordan kan jeg vise lagerantallet på en bestemt dato med avveid gjennomsnitt?

Du kan bruke rapporten **Aldersfordeling for lager**, som inneholder en **Gjennomsnittlig enhetskost**-kolonne som viser lageret per en bestemt dato. Hvis du vil ha mer informasjon, kan du se [Eksempler og logikk for rapport for aldersfordeling for lager](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Hvordan kan jeg vise hvilke mottakstransaksjoner som utlignes mot en avgangstransaksjon?

Du kan vise utligningene for en lagertransaksjon ved å velge **Utligninger** eller **Kostnadsutforsker** i kategorien **Lager** i handlingsruten på siden **Lagertransaksjon** eller **Lagertransaksjonsdetaljer**. Hvis du velger et mottak for å vise avgangene som er relatert til transaksjonen, vises ikke detaljene i kostnadsutforskeren. Detaljer vises bare hvis du velger en avgangstransaksjon.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Hvordan viser lagerverdirapporten varer som har et positivt fysisk antall og en negativ finansverdi?

Lagerverdirapporten deler fysiske og økonomiske beløp og antall inn i egne kolonner. Verdiene som vises i rapporten, er fra datoområdet du valgte da du kjørte rapporten. Hvor mye sammendrag som vises, avhenger av innstillingene du har valgt. Hvis en vare har transaksjoner som er fysisk mottatt og økonomisk frigitt, blir antallene og verdiene summert uavhengig. Hvis du valgte å vise detaljnivået som transaksjoner, vises rader for hvert mottak og hver avgang separat, og henholdsvis det fysiske og det økonomiske antallet og beløpene vises. Hvis du vil ha mer informasjon, kan du se [Eksempler og logikk for lagerverdirapport](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Hva har innvirkningen på lagrings- og sporingsdimensjonsgrupper i lagerverdirapporten?

Hvis du aktiverer alternativet **Finansverdier** for en dimensjon i en lagrings- eller sporingsdimensjonsgruppe, kan du velge alternativet **Visning** eller **Total** for dimensjonen i rapportkonfigurasjonen av lagerverdi. Hvis du velger alternativet **Vis** eller **Total** for en dimensjon der alternativet **Finansverdi** ikke er valgt, vil kolonnen være tom i rapportutdataene. Hvis du har aktivert alternativet **Finansverdi** for en dimensjon i en lagrings- eller sporingsdimensjonsgruppe, og du ikke velger alternativet **Vis** eller **Total** i rapportkonfigurasjonen av lagerverdi, vil systemet summere verdiene for de valgte dimensjonene der de spores økonomisk.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Kan jeg tilpasse de Power BI Embedded-rapportene for etterkalkulering?

Ja, brukere som har riktige sikkerhetstillatelser, kan oppdatere rapportutformingen for en hvilken som helst Power BI Embedded-rapport i Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Tilpasse innebygde rapporter i analytiske arbeidsområder](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Hvor kan jeg vise avviksanalyserapporten?

Du kan få tilgang til avviksanalyserapporten ved å gå til **Kostnadsstyring \> Forespørsler og rapporter \> Lagerregnskap – analyserapporter** eller **Kostnadsstyring \> Forespørsler og rapporter \> Produksjonsregnskap – analyserapporter**. Begge alternativene åpner den samme rapporten, og rapporten har samme virkemåte.

## <a name="item-prices-and-default-costs"></a>Varepriser og standardkostnader

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Kan jeg vedlikeholde kostnadene for hver produktvariant?

Ja. Du kan aktivere alternativet **Bruk kostpris etter variant** i hurtigkategorien **Behandle kostnader** på siden **Frigitt produkt** for å aktivere prissetting etter produktvariant. (Dette alternativet er bare tilgjengelig for produktstandarder.) På **Varepris**-siden (som du kan åpne fra siden **Etterkalkuleringsversjon** eller **Frigitt produkt**) kan du deretter velge **Dimensjonsvisning** for å angi om du vil vise dimensjonen **Konfigurasjon**, **Størrelse**, **Farge** eller **Stil**. Hvis du vil lagre oppsettet og bruke de valgte dimensjonene hver gang du åpner siden, aktiverer du alternativet **Lagre oppsett** og velger deretter **OK**. Du kan bare angi dimensjonene for varer der dimensjonene er aktive i produktdimensjonsgruppen.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Kan jeg vedlikeholde kostnadene for hvert lager?

Nei, du kan ikke vedlikeholde vareprisen etter lager. Du kan imidlertid vedlikeholde forretningsavtaler for innkjøpspriser eller salgspriser etter lager. Først velger du alternativet **For innkjøpspriser** eller **For salgspriser** for dimensjonen på siden **Lagringsdimensjonsgruppe**. Når du deretter oppretter forretningsavtalejournalen og åpner linjene for dimensjonene, velger du **Lager \> Visningsdimensjoner** for å velge hvilken dimensjon som skal vises i rutenettet. Hvis du vil lagre oppsettet og bruke de valgte dimensjonene hver gang du åpner siden, aktiverer du alternativet **Lagre oppsett** og velger deretter **OK**. Du kan bare angi dimensjonene for varer der dimensjonene er aktive i produktdimensjonsgruppen.

### <a name="what-are-price-charges"></a>Hva er pristillegg?

Pristillegg brukes til å legge til et fast beløp i enhetsprisen for vareprisen eller forretningsavtalen. Når du angir et beløp i **Pristillegg**-feltet, kan du også angi en verdi i feltet **Tilleggsantall**. Pristilleggene amortiseres over antall gebyrer du angir. Aktiver alternativet **Inkl. i enhetspris** hvis du vil ta med pristilleggene i enhetsprisen for varen. Dette alternativet er alltid aktivert for en standardkostnad.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Hvordan konfigurerer jeg priser for varer som finnes i flere valutaer?

Hvis du angir en standardpris i **Innkjøpspris**-feltet på **Frigitt produkt**-siden, antas det at den er i regnskapsvalutaen i finans for den juridiske enheten du er i. Hvis du angir en innkjøpspris i en etterkalkuleringsversjon der **Pristype**-feltet er satt til *Innkjøp*, antas det at prisen ligger i regnskapsvalutaen for den juridiske enheten. Når du oppretter en bestilling for en leverandør som har en annen valuta, konverterer systemet automatisk valutaen fra regnskapsvalutabeløpet til transaksjonsvalutaen ved hjelp av valutakursen du angir i feltet **Type valutakurs for regnskapsvaluta** i finans.

Når du oppretter en forretningsavtalejournal, kan du angi valutaen du uttrykker prisen i, på hver linje. Du kan opprette forretningsavtaler for flere valutaer, bestemte leverandører og mange andre kombinasjoner av faktorer. Hvis du oppretter en bestilling der det finnes en forretningsavtale for valutaen du har valgt, bruker systemet forretningsavtalen som har samsvarende valuta. Når du posterer transaksjoner, for eksempel produktmottak eller fakturaer, konverteres beløpet til finansmodulens regnskapsvaluta ved hjelp av den regnskapsvalutakursen du angir i finans.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Hvordan konfigurerer jeg kostnader for varer som finnes i flere valutaer?

Kostnader kan ikke konfigureres i mer enn én valuta. Kostnaden du angir for vareprisen eller standardkostnadene du angir i **Pris**-feltet i hurtigkategorien **Administrer kostnad** på siden **Frigitt produkt**, uttrykkes alltid i regnskapsvalutaen for finans for den juridiske enheten du har valgt.

Hvis organisasjonen bruker standardkostnad, bør du definere en strategi for å definere kostnadene når det finnes flere valutaer. Du bør også definere en prosess for regelmessig oppdatering av kostnaden for å redusere antall avvik som posteres.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Kan jeg bruke fortjenesteinnstillingen på Kostgruppe-siden til å beregne salgspriser?

Ja, du kan bruke **Profitt**-innstillingen på **Kostgruppe**-siden for å legge til en prosent når salgspriser beregnes ved hjelp av en kostnadsberegning. Hvis du vil ha mer informasjon, kan du se [BOM-beregninger](bom-calculations.md).

## <a name="marking"></a>Merking

### <a name="how-does-marking-affect-periodic-costing-models"></a>Hvordan påvirker merking periodiske kostnadsmodeller?

Hvis du bruker en periodisk kostnadsmodell, for eksempel FIFO, LIFO eller avveid gjennomsnitt, og du har merket en mottakstransaksjon mot en avgangstransaksjon, blir den heuritiske modellen for varen ignorert under lagerlukkingsprosessen. I stedet bruker systemet den faktiske kostnaden for mottaket for kostnaden av avgangen.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Hva skjer under lagerlukkingen når jeg bruker merking?

Når du merker mottak og avganger, vil lagerlukkingen utligne transaksjonene som er merket sammen. Når merkingen brukes til å opprette utligningen, settes **Prinsipp**-feltet på siden **Utligning** til *Merking*. Hvis en transaksjon merkes før den er fysisk eller økonomisk oppdatert, bruker avgangen det merkede mottakets kostnad i stedet for det glidende gjennomsnittet av kostprisen. Hvis transaksjonene er merket etter finansoppdageringen, vil beholdningslukking og justeringsprosessen justere avgangskostnaden slik at den samsvarer med mottakskostnaden.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Kan jeg merke transaksjoner manuelt når jeg bruker standard kostpris eller glidende gjennomsnitt?

Nei, du kan ikke merke mottak eller avganger manuelt når du bruker standard kostpris eller glidende gjennomsnitt. Hvis det merkes av for transaksjoner (for eksempel direktelevering eller konserninterne ordrer), blir merkingsposten stående, og det vil fungere som en hard reservasjon. Når du bruker standardkostnad eller glidende gjennomsnitt, har imidlertid ikke merkingen av poster noen innvirkning på kostnadene til varene.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Hvordan påvirker merkingen resultatregnskapet?

Når du merker en avgangstransaksjon mot et mottak, vil kostnaden for avgangen samsvare med det valgte mottaket. Når du fysisk og økonomisk posterer avgangen, vil posteringen påvirke kontoene **Solgte varers kostnad, levert** og **Solgte varers kost** som du angir i lagerposteringsprofilen. Hvis en transaksjon er merket etter den fysiske eller økonomiske oppdateringen, vil prosessen for *lukking og justering av beholdning* opprette en justering som har et samsvarende bilag som justerer kontoen **Solgte varers kostnad, fakturert** og motposterer til kontoen du angir for **Kostnad for enheter, fakturert** (lager).

### <a name="how-does-marking-affect-master-planning"></a>Hvordan påvirker merking hovedplanlegging?

Kategorien **Standardoppdatering** på siden **Hovedplanleggingsparametere** inneholder et felt kalt **Oppdater merking**. Alternativet du velger der, brukes når du autoriserer en planlagt bestilling som genereres av hovedplanlegging. Følgende alternativer er tilgjengelige:

- *Nei* – Systemet utfører ingen merking.
- *Standard* – Systemet merker mottak mot avganger i henhold til utligningen. En kravordre merkes mot en innfrielsesordre. Hvis det gjenstår kvanta på oppfyllelsen, merkes ikke oppfyllelsen.
- *Utvidet* – Systemet merker både kravordrene og innfrielsesordrene, uansett om det gjenstår kvanta forblir åpne på innfrielsesordren.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negativ beholdning

### <a name="when-should-i-allow-physical-negative-inventory"></a>Når skal jeg tillate fysisk negativt lager?

Generelt anbefaler vi ikke at du tillater fysisk negativt lager, fordi det ikke er mulig å ha mindre enn 0 (null) av en materiell vare i lageret. Forretningsprosessene i noen industrier og forretningsscenarier kan imidlertid begrense operasjoner som krever at lageret skal ha tillatelse til å gå fysisk negativt. Det kan for eksempel hende at forhandlere ikke vil hindre salget av en vare som blir tatt med til kassen, selv om systemet indikerer at ingen varer er tilgjengelige. Prosessprodusenter gir et annet eksempel. For disse produsentene kan beløpet som forbrukes, overskride det som er anbefalt i formelen. Eventuelt kan forbruket estimeres i stedet for nøyaktig, slik at forbruket overskrider beløpet på et bestemt sted, for eksempel en tank.

Hvis mulig bør du evaluere forretningsprosessen og prøve å forbedre den for å sikre at lageret ikke kan være negativt. Hvis du må tillate negativt lager, bør du ha en klar forretningsprosess for å rette opp det negative lageret, fordi det kan gå ut over etterkalkuleringen.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Når skal jeg tillate økonomisk negativt lager?

Generelt anbefaler vi at de fleste organisasjoner tillater økonomisk negativt lager. (I de fleste tilfeller behandles ikke bestillingsfakturaer før du kan sende varene.) Du bør aktivere dette alternativet når du har bestemte forretningsprosesser som krever at salgsprisen gjenspeiler den endelige kostnaden til en bestilling. Dette kravet kan for eksempel gjelde i en bestillingsindustri eller i bestemte områder der det er angitt i loven.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Hva skjer med kostnadene for avgangene når lageret er negativt?

Når lageret for varen er negativt, og du utsteder flere varer enn du fysisk har, bruker systemet standard varepris til å beregne det glidende gjennomsnittet hvis du bruker en periodisk kostnadsmodell, for eksempel FIFO, LIFO eller avveid gjennomsnitt. Hvis det ikke er angitt noen standardpris for varen, vil systemet utstede lageret med verdien 0 (null). Denne virkemåten kan føre til at fremtidige beregninger av løpende gjennomsnitt eller glidende gjennomsnitt er unøyaktige.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Kan jeg hindre at varer blir plukket, pakket eller solgt på salgsordrer og produksjonsordrer hvis det ikke er nok lagerbeholdning?

Ja. Vi anbefaler at du deaktiverer alternativet **Fysisk negativt** for varemodellgruppen for å hindre at varer blir plukket, pakket eller solgt på salgsordrer og produksjonsordrer.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Kan jeg hindre at varer blir fakturert på en salgsordre hvis ingen bestillinger er fakturert for den samme varen?

Ja. Vi anbefaler at du deaktiverer alternativet **Økonomisk negativt** for varemodellgruppen for å hindre at varer faktureres på en salgsordre hvis ingen bestillinger er fakturert for den samme varen.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Hvordan påvirker negativt lager finansforhold, for eksempel bruttofortjenestemargin?

Når du tillater at lageret kan være negativt, kan lagerverdien i balansen og kostnader for solgte varer i resultatregnskapet være undervurdert, spesielt hvis det ikke er konfigurert noen standardpris for varene. Derfor kan økonomisk rapportering og forholdstall som bruttofortjenestemarginer overvurderes, fordi kostnaden er feil. Hvis du bruker en periodisk kostnadsmodell, for eksempel FIFO, LIFO eller avveid gjennomsnitt, kan verdien av avgangene justeres når du kjører lagerlukkings- og justeringsprosessen etter at negativt lagerantall er rettet. Hvis du imidlertid bruker glidende gjennomsnitt, finnes det ingen måte å vurdere enkelttransaksjonene på nytt.

### <a name="how-should-i-correct-negative-inventory"></a>Hvordan retter jeg negativt lager?

Vi anbefaler at du ofte overvåker og retter negativt lager når organisasjonen eller forretningsbehovene tilsier at lageret kan være negativt. Du kan korrigere lagerverdiene ved å utføre en syklusopptelling, postere en justering eller postere en bevegelsesjournal. Hvis du må gjenkjenne den uventede fortjeningen på lager i en bestemt finanskonto, bør du planlegge å bruke en bevegelsesjournal. Hvis du bruker syklusopptellingen eller lagerjusteringsprosessen, posterer systemet lagerjusteringen til **Lagertilgang**-kontoen og motposteres til kontoen **Lagerutgift, fortjeneste** som du angir i lagerposteringsprofilen.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Må jeg opprette en ny vare hvis lageret er gått negativt, og jeg bruker glidende gjennomsnitt?

Nei Hvis organisasjonen tillater at lageret kan være fysisk negativt, og du bruker glidende gjennomsnitt som lagermodell, bruker systemet tilbakefallskostnadsserien som er tilordnet på siden **Parametere for beholdnings- og lagerstyring** for å bestemme hvordan kostnaden skal tilordnes avgangene. Generelt anbefaler vi at du unngår å tillate at lageret går fysisk negativt. Hvis du vil ha mer informasjon, kan du se de andre spørsmålene i delen [Negativ beholdning](#negative-inventory) i denne artikkelen.

## <a name="not-stocked-products"></a>Ikke lagerførte produkter

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Kan jeg postere plukklister for produkter som ikke er på lager?

Når du genererer en plukkliste for en salgsordre som inneholder varer som er i en varemodellgruppe som ikke er på lager, vil du ikke se noen linjer for varer som ikke er på lager. Du kan ikke bruke mobilappen Warehouse Management til å behandle varer som ikke er på lager.

Når du genererer en følgeseddel for en salgsordre som inneholder varer som er i en varemodellgruppe som ikke er på lager, angir du **Antall**-feltet til *Plukket antall og ikke-lagerførte produkter* slik at de inneholder varene som ikke er på lager i dokumentgenereringen. Hvis du velger *Alle*, blir bare lagerbeholdte varer tatt med i følgeseddelen.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Bør jeg bruke et produkt som ikke er på lager eller en kategori (salgskategori eller innkjøpskategori)?

Valget mellom et produkt som ikke er på lager og en kategori, avhenger av dine bestemte forretningskrav. Produkter som ikke er på lager, gir vanligvis mer kontroll over standardverdiene, for eksempel antall og priser på bestillinger og salgsordrer. Derfor foretrekkes produkter som ikke er på lager, i scenarier der samme produkt eller tjeneste blir kjøpt eller solgt mer enn én gang. Kategorier er nyttige i scenarier der prisen, varene, beskrivelsene og så videre er inkonsekvent fra transaksjon til transaksjon. Kategorier kan også brukes på et hvilket som helst produkt for å bidra til å klassifisere produkttypen som selges eller kjøpes.

## <a name="service-items"></a>Servicevarer

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Hva er forskjellen mellom en servicevare og et produkt som ikke er på lager?

En servicevare er en produkttype. Når du oppretter et nylig frigitt produkt, kan du angi **Produkttype**-feltet til enten *Vare* eller *Tjeneste*. *Varen* velges vanligvis for å angi at varen er materiell, mens *Tjeneste* vanligvis velges for å angi at varen er immateriell.

Et hvilket som helst frigitt produkt, uansett om det er en vare eller et serviceprodukt, kan lagerføres eller ikke-lagerføres. Innstillingen for lagerføring eller ikke-lagerføring styres av varemodellgruppen som du velger for det frigitte produktet. Når du velger en varegruppe som ikke er på lager, oppretter ikke systemet lagertransaksjoner for den tilknyttede salgsordren eller bestillingen.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Kan jeg ta med varer som ikke er på lager, i en stykkliste?

Nei, du kan ikke inkludere et frigitt produkt som er koblet til en varemodellgruppe der alternativet **Lager** er deaktivert i en stykkliste eller formel. Det spiller ingen rolle om **Produkttype**-felteter satt til *Vare* eller *Tjeneste*. Bare varer som er på lager, kan tas med på stykkliste- eller formellinjer.

## <a name="costing-modelspecific-questions"></a>Kostmodellspesifikke spørsmål

### <a name="which-costing-model-should-i-use"></a>Hvilken kostnadsmodell skal jeg bruke?

Kostnadsmodellene du bør velge, avhenger av forretningskravene. Før du velger en etterkalkuleringsmodell som skal brukes i Supply Chain Management, bør du validere at modellen er tillatt i dine lokale bestemmelser. Det anbefales at du validerer valget ditt med en bekreftet regnskapsfører i ditt område.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Kan jeg bruke mer enn én kostnadsmodell i organisasjonen?

Ja. Det er ingen begrensninger på hvor mange varemodellgrupper eller kostnadsmodeller du kan velge i Supply Chain Management.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Kan jeg bruke mer enn én kostnadsmodell for hver vare?

Nei Du kan bare velge én kostnadsmodell for hvert frigitt produkt. Denne virkemåten styres av varemodellgruppen. Hvis du må bruke mer enn én kostnadsmodell til å rapportere på lagerverdier, bør du vurdere å bruke tillegget Globalt lagerregnskap.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Når jeg bruker produksjonsutførelse, hvilken etterkalkuleringsmetode bør jeg bruke?

Kostnadsmodellene du bør velge, avhenger av forretningskravene. Det er ingen spesiell fordel eller ulempe i bruken av kostnadsmodeller når organisasjonen også bruker produksjonsutførelse.

### <a name="when-is-fefo-used"></a>Når brukes FEFO?

Først utløpt først ut (FEFO) er ikke en etterkalkuleringsmetode. I stedet er det en reservasjonsteknikk som ofte brukes i produksjonsorganisasjoner. Du kan aktivere FEFO-reservasjoner for en varemodellgruppe ved å aktivere **FEFO-datokontrollert**-alternativet og deretter velge en verdi i **Plukkekriterier**-feltet.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Er det ytelsesfordeler ved å velge én kostnadsmodell over en annen?

Generelt sett har kostnadsmodellen du velger for en vare, minimal innvirkning på den totale ytelsen til systemet. Tiden som kreves for å kjøre lagerlukkingen eller omberegningsprosessen, kan imidlertid påvirkes av lagerkostmodellen du velger. Hvis du for eksempel bruker standard kostpris eller glidende gjennomsnitt, har lagerlukkingsprosessen minimal innvirkning på systemet, fordi den ikke oppdaterer hver lagertransaksjon og oppretter utligninger. En periodisk kostnadsmodell, for eksempel FIFO, LIFO eller avveid gjennomsnitt, kan imidlertid øke tiden som kreves for å fullføre lagerlukkingsprosessen. Spesifikt kan lukkingsprosessen være lenger når du angir et høyt tall i feltet **Maksimalt antall gjentakelser som tillates per vare**-feltet eller et lavt antall i feltet **Minimumsbeløp tillatt** for *Lukk lager*-prosessen.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Når bør jeg bruke alternativet Fast mottakspris?

Når du merker av for **Fast mottakspris** på siden **Varemodellgruppe** for en vare, bruker systemet mottaksprisen som en standardkostnad for lagermottaket. Hvis det er forskjell mellom innkjøpsprisen og standard varekostpris som er konfigurert for et produkt, posteres differansen til fortjeneste ved **Fortjeneste på fast mottakspris** eller **Tap på fast mottakspris** og motposteres til kontoen **Motkonto for fast mottakspris**. (Alle disse kontoene er angitt i **Postering**-siden.)

Du bør merke av for **Fast mottakspris** når du bruker en periodisk kostnadsmodell som FIFO, LIFO eller avveid gjennomsnitt, og du krever at det spores et avvik i innkjøpspris i finans hvis prisen på et mottak er forskjellig fra standard varekost.

### <a name="moving-average"></a>Glidende gjennomsnitt

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Er glidende gjennomsnitt det samme som et flytende gjennomsnitt?

Termene glidende gjennomsnitt, flytende gjennomsnitt og løpende gjennomsnitt brukes ofte synonymt. Av disse betingelsene er glidende gjennomsnitt den eneste offisielle kostnadsmodellen som er tilgjengelig i Supply Chain Management. Selv om løpende gjennomsnittlig ikke er en offisiell kostnadsmodell, er det den teknikken som brukes når du bruker en periodisk kostnadsberegningsmodell, for eksempel FIFO, LIFO eller avveid gjennomsnitt. Begrepet flytende gjennomsnitt brukes ikke i Supply Chain Management og kan ha ulike konnotasjoner i andre systemer.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Hvordan kan jeg legge til rette for forskjellen mellom prisen på produktmottaket og fakturaprisen når jeg bruker glidende gjennomsnitt?

Når du bruker glidende gjennomsnitt, brukes den fysiske kostnaden (mottakspris) til å beregne det glidende gjennomsnittet for alle avgangstransaksjoner. Hvis det er en forskjell mellom den fysiske kostnaden (mottakspris) og den økonomiske kostnaden (fakturaprisen), posterer systemet automatisk differansen til hovedkontoen som er angitt for **Prisdifferanse for glidende gjennomsnitt** i kategorien **Lager** på siden **Lagerposteringsprofil**.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Hvor er prisdifferansen for glidende gjennomsnitt presentert i økonomimodulen?

Når det er en prisforskjell mellom postering for en fysisk oppdagering og en økonomisk oppdatering for et mottak, posteres differansen til hovedkontoen som er angitt for posteringstypen **Prisdifferanse for glidende gjennomsnitt** i kategorien **Lager** på siden **Lagerposteringsprofil**. Hvis du vil ha mer informasjon, kan du se [Glidende gjennomsnitt](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Når jeg bruker glidende gjennomsnitt, hva skjer hvis det er en avgang før mottaket?

Det kan vanligvis være en avgang før mottaket, enten fordi du tillater fysisk negativt lager for varemodellgruppen, eller fordi avgangen tilbakedateres. Hvis du vil ha mer informasjon, kan du se delen [Negativt lager](#negative-inventory) i denne artikkelen.

Hvis du sikkerhetskopierer transaksjoner, anbefaler vi at du nøye vurderer forretningsprosessen og operasjonene dine for å finne ut om det er en måte å unngå dette scenariet på. Hvis du tilbakedaterer en transaksjon for en vare som bruker glidende gjennomsnitt, tilordnes det gjeldende glidende gjennomsnittet til transaksjonen. Senere avganger som ikke er justert. Hvis du vil ha mer informasjon om glidende gjennomsnitt med tilbakedaterte transaksjoner, kan du se [Glidende gjennomsnitt](moving-average.md).

### <a name="standard-costing"></a>Standard etterkalkulering

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Hva er forskjellen mellom standard etterkalkulering og fast mottakspris?

Standardkostnad krever at du definerer en varepris og aktiverer kostnaden i en kostnadsversjon. Denne kostnaden brukes for alle mottak og avganger. Avvik for mottak til lager registreres i økonomimodulen ved hjelp av avvikskontoene for standard **kostpris som du angir i kategorien Standardkost** på siden **Lagerposteringsprofil**.

Når du bruker fast mottakspris, er imidlertid bare kostnaden for mottak faste, og systemet bruker kostnaden som du angir i hurtigkategorien **Behandle kostnader** på **Frigitt produkt**-siden. Forskjeller mellom standardkost og bestillingspris vil føre til at innkjøpsprisavvik posteres til resultatkontoene for fast mottakspris. Avganger bruker ikke fast mottakspris. I stedet vil avganger vurderes med glidende gjennomsnitt når du posterer (med mindre du bruker merking), og de vurderes på nytt til den heuristiske modellen du velger når du kjører lagerlukkingen.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Kan jeg bruke FEFO-reservasjoner med standard kostpris?

Ja, du kan bruke FEFO-reserveringer for en varemodellgruppe når du velger standard etterkalkulering. FEFO-reserveringer styrer reservasjonslogikken som brukes for fysisk håndtering av varene, mens standard etterkalkulering kontrollerer de fysiske og finansielle kostnadene for en vare.

### <a name="can-i-upload-pending-prices"></a>Kan jeg laste opp ventende priser?

Ja, du kan bruke Excel-tillegget eller Data Management Framework til å laste opp en ventende pris. Vi anbefaler at du bruker følgende enheter:

- Ventende varepriser (V2)
- Ventende enhetskostnader for rutekostnadskategori
- Beregningsfaktorer for etterkalkuleringsarknode (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Hvor ofte kan jeg oppdatere standardkostnaden for en vare?

Det er ingen grense for hvor ofte du kan aktivere en ny standardkostnad. Hvis du aktiverer en ny kostnad for en vare på samme dag som den siste kostnaden ble aktivert, bruker systemet den nyeste aktiverte kostnaden på nye transaksjoner eller oppdateringer (for eksempel oppdateringer for eksisterende transaksjoner).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Kan jeg deaktivere eller slette en aktivert kostnad?

Nei, du kan ikke deaktivere eller slette en aktivert kostnad. Hvis du har aktivert en kostnad feil, kan du aktivere en ny kostnad som har riktig kostnad.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Brukes beregningsgrupper med standardkostnad?

Beregningsgrupper kan brukes med alle varer, uansett hvilken varemodellgruppe du velger. Beregningsgruppene brukes under prosessen for kostnadsopprullering eller kostnadsberegning for å bestemme innstillingene som skal brukes for varene du kjører beregningen for. Hvis du vil ha mer informasjon om beregningsgrupper, kan du se [Beregningsgrupper for stykkliste](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Når skal jeg bruke en planlagt kostnadsversjon?

Etterkalkuleringsversjoner kan ha typen *Standardkostnad* eller *Planlagt kostnad*. Typen *Standardkostnad* brukes for kostnadene som er aktive i systemet, og posteres i transaksjoner. Typen *Planlagt kostnad* brukes til å kjøre simuleringer på kostnader, og påvirker ikke transaksjonskostnadene.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Kan totalkostnaden fra én enhet overføres til en annen enhet som salgskostnaden?

Det finnes ingen automatisert måte å kopiere kostnader fra ett firma til et annet på. I tillegg finnes det ingen automatisert måte å kopiere kostnader fra en innkjøpspris til en salgspris på. Hvis organisasjonen må fullføre en av disse oppgavene, må du vurdere om du kan bruke Data Management Framework til å eksportere data fra kostnadsversjonen og laste opp til et annet firma, enten som salgspris i etterkalkuleringsversjonen eller som en forretningsavtale. Manuell manipulering av filene kan være nødvendig.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Hva er den beste måten å kopiere planlagte kostnader til en standard kostnadsversjon på?

Du kan bruke **Kopier**-knappen på siden **Etterkalkuleringsversjoner** til å kopiere varepriser, kostkategoripriser eller indirekte kostnader fra én kostnadsversjon til en annen.
