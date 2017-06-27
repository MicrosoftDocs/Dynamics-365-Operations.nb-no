---
title: Oversikt  over standard kostnadskonvertering
description: "Denne artikkelen inneholder en prosessoversikt som hjelper deg med å definere og kjøre en standard kostnadskonvertering. Trinnene skal fullføres etter at du har oppfylt forhåndskravene for en standard kostnadskonvertering."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 6e223c2d9a683d7b92b73d3fe3d3c8b22684d22c
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="standard-cost-conversion-overview"></a>Oversikt  over standard kostnadskonvertering

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder en prosessoversikt som hjelper deg med å definere og kjøre en standard kostnadskonvertering. Trinnene skal fullføres etter at du har oppfylt forhåndskravene for en standard kostnadskonvertering. 

Bruk siden **Standard kostnadskonverteringer** til å konvertere lagermodellen for et parti valgte varer fra en faktisk kostnad til standard kostnad. Konverteringsprosessen går ut på å utføre en nødvendig lagerlukking, utføre flere trinn i løpet av en overgangsperiode, som er definert av en startdato for overgang og en dato for planlagt konvertering, samt utføre konverteringen og en tilhørende lagerlukking.

-   Lagerlukking før overgangsperioden − Lagerlukking er et nødvendig trinn, for den utligner varens åpne transaksjoner for den gamle vurderingsmetoden. I løpet av overgangsperioden kan du angi og postere tilbakedaterte transaksjoner, som fakturaer, slik at du kan lukke den forrige perioden. Lagerlukkingsdatoen må være en dag før startdatoen for overgang slik at det blir et rent brudd med den gamle vurderingsmetoden.
-   Konverteringstrinn i løpet av overgangsperioden − Bruk siden **Standard kostnadskonverteringer** til å opprette en konverteringspost som også inneholder den brukerdefinerte ID-en for en ny etterkalkuleringsversjon. Du identifiserer varene som krever konvertering, og angir deretter varenes ventende standardkostnader i den nye etterkalkuleringsversjonen. Du utfører en kontroll av de valgte varene for å finne problemer som kan forhindre konvertering, og deretter utfører du en ny kontroll. Når varene har bestått kontrollen, endrer du statusen fo rkonverteringsposten til **Klar**. På den planlagte konverteringsdatoen utfører du konverteringen og eventuelt en lagerlukking. Varens lagerbevegelser i løpet av overgangsperioden blir postert og vurdert i henhold til den gamle lagermodellen. Etter at konverteringen er fullført, revalueres deretter lagerbevegelsene til standardkostnaden.
-   Lagerlukking før konverteringen − Lagerlukkingen kan tas med som en del av konverteringen på den planlagte konverteringsdatoen, eller den kan utføres som et separat trinn før konverteringen.

Når konverteringsprosessen er fullført, baseres lagermodellen for hver vare på standardkostnaden, og varens standardkostnad blir aktivert. Påfølgende lagertransaksjoner blir vurdert etter varens standardkostnad. I tillegg konverterer systemet varens fysiske lagertransaksjoner for mottak og avganger til standardkostnad basert på konverteringsdatoen. Systemet konverterer også varens økonomiske lagerbeholdning til standardkostnad, og posterer verdiforskjellen som en lagerrevaluering. Eventuelle transaksjoner som foregår etter konverteringen, vurderes etter varens standardkostnad. Du kan ikke angi tilbakedaterte transaksjoner før konverteringsdatoen, for en lagerlukking må utføres en dag før konverteringsdatoen. En konvertering kan bare utføres hvis en lagerlukking ble utført en dag før. Denne lagerlukkingen kan ikke avbrytes.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Definer en standard kostnadskonverteringspost og den tilhørende kostversjonen
Bruk siden **Standard kostnadskonverteringer** til å opprette en konverteringspost. Du kan bare opprette en ny konverteringspost når de eksisterende konverteringspostene er fullført. Lengden på den planlagte overgangsperioden defineres av startdato for overgangen og den planlagte konverteringsdatoen. En planlagt overgangsperiode kan være så kort som én dag. En planlagt overgangsperiode bidrar til å sikre at konverteringen har nok tid til å fullføre alle trinnene. En lagerlukking må gjennomføres på en dato som er før startdatoen for overgangen, slik at utligningene er fullført før du starter konverteringsprosessen. Hvis du vil forsikre deg om at startdatoen for overgangen og lagerlukkingsdatoen er riktig justert, kan du enten endre startdatoen for overgangen til én dag etter en eksisterende lagerlukking eller utføre en lagerlukking. Når du angir en konverteringspost, angir du også en brukerdefinert ID for en ny kostversjon som vil inneholde standardkostnad for konverterte varer. Når du lagrer konverteringspostinformasjon, blir etterkalkuleringsversjonen opprettet automatisk.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Gjennomgå og endre de nye etterkalkuleringsversjonene for konverteringsposten
Den nye etterkalkuleringsversjonen er dedikert til konverteringsposten, noe som gjenspeiles i etterkalkuleringstypen **Konvertering**. Den dedikerte etterkalkuleringsversjonen ligner på en etterkalkuleringsversjon for standardkostnader, og den inneholder varekostpostene for varer som er knyttet til konverteringsposten. Den dedikerte etterkalkuleringsversjonen for en konverteringspost har følgende innstillinger, som du bør gå gjennom og endre i de ulike kategoriene etter behov:

-   **Etterkalkuleringstype:** Dette feltet skal settes til **Standardkostnad**.
-   **Versjon:** Identifikatoren gjenspeiler informasjonen som er angitt i konverteringsposten for etterkalkuleringsversjons-ID-en.
-   **Navn:** Navnet er tomt som standard. Du kan skrive inn et navn hvis du vil.
-   **Blokker:** Dette feltet skal settes til **Ingen**. Du kan angi kostnadsposter i kostversjonen til du endrer statusen til konverteringsposten til **Klar**. Statusen **Klar** betyr at det valgte elementet er kontrollert, og at endringer til kostnadsposter ikke bør være tillatt.
-   **Blokkaktivering:** Dette feltet skal settes til **Ja**. Du kan ikke aktivere en uavsluttet kostnadspost manuelt i den dedikerte kostversjonen. Aktivering skjer når du har gjennomført konverteringen.
-   **Fra dato:** − Fra-datoen gjenspeiler den planlagte konverteringsdatoen som er angitt i konverteringsposten.
-   **Område:** La dette feltet stå tomt, slik at kostnadsposter kan angis for alle områder.
-   **Tillat pristype-feltgruppe:** Sett dette feltet til **Ja**, slik at bare kostnadsprisposter kan angis.
-   **Tilbakefallsprinsipp:** Sette dette feltet til **Ingen**. Endre tilbakefallsprinsippetet til **Aktiv** hvis du vil ha kostnadsinformasjon som er aktivert i andre etterkalkuleringsversjoner. Kostbnadsinformasjon om komponenter, kostnadskategorier og indirekte kostnader kan for eksempel være påkrevd for å beregne kostnader for produserte varer.
-   **Etterkalkuleringsversjon for tilbakefall:** La dette feltet stå tomt.

Varekostnadsinformasjon i den dedikerte etterkaluleringsversjonen kan bare vedlikeholdes fra siden **Standard kostnadskonverteringer**. Du kan ikke bruke siden **Oppsett av etterkalkuleringsversjon** eller **Vedlikehold av etterkalkuleringsversjon** til å beregne kostnader for etterkalkuleringsversjonen under konvertering. Du kan imidlertid bruke disse sidene til å vedlikeholde den dedikerte etterkalkuleringsversjonen når du har fullført konverteringsprosessen.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Identifiser varene som skal konverteres til standardkostnad.
Bruk siden **Standard kostnadskonverteringer** til å identifisere de individuelle varene som skal konverteres til standardkostnad. Du kan legge til flere elementer ved hjelp av siden **Legg til varer i standard kostnadskonvertering**. Generelt bør du ta med alle produserte varer i en enkelt konverteringspost slik at kostnadene blir beregnet på rett måte.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Angi eller beregne den ventende standardkostnaden for hver vare som konverteres
Bruk **Varepris**-siden til å angi uavsluttede standardkostnader i den dedikerte etterkalkuleringsversjonen for kjøpte varer og overføringsvarer. Kostnadsposter gjelder bare for stedet, og du må angi varens uavsluttede kostpriser for hvert sted. Bruk **Varepris**-siden til å beregne uavsluttede standardkostnader for produserte varer. De uavsluttede kostnadene for en produsert vare bør beregnes for hvert produksjonssted, hvis ikke stedet representerer et overføringssted. I slike tilfeller bør de uavsluttede kostnadene angis manuelt. Noen varer kan ha produktdimensjoner som farge, størrelse eller konfigurasjon. På siden **Standard kostnadskonverteringer** viser avmerkingsboksen **Bruk kostpris etter variant** standardkostnaden for hver kombinasjon av produktdimensjoner. Når merket er fjernet fra avmerkingsboksen, trenger du bare å angi en ventende kostnad for varen.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Kontrollere og løse eventuelle problemer for varene som konverteres
Bruk rapporten **Kontroller for standard kostnadskonvertering** til å rapportere problemer for varer som konverteres. Hvis det ikke er problemer med varen, endres statusen i konverteringsposten til **Kontrollert**. Hvis en vare har problemer, må du løse problemene og deretter kjøre rapporten på nytt til statusen for varen endres til **Kontrollert**. Hvis du ikke kan løse problemet innen rimelig tid, kan du slette varen fra konverteringsposten og konvertere varen senere.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Endre statusen til konverteringsposten til Klar
Når du endrer statusen til konverteringsposten til **Klar**, utfører systemet en sluttkontroll før en standard kostnadskonvertering kjøres. Statusen endres bare til **Klar** når følgende vilkår er oppfylt:

-   Hver vare i konverteringsposten har statusen **Kontrollert**.
-   En lagerlukking ble utført på en dato som er én dag før startdatoen for overgangen. Hvis du vil forsikre deg om at startdatoen for overgangen og lagerlukkingsdatoen er riktig justert, kan du enten endre startdatoen for overgangen til én dag etter en eksisterende lagerlukking eller utføre en lagerlukking.

## <a name="7-back-up-the-database-before-conversion"></a>7. Sikkerhetskopiere databasen før konvertering
Sikkerhetskopien sørger for at du kan gjenopprette databasen hvis det oppstår feil i konverteringen.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Utføre konverteringen når konverteringsposten har statusen Klar
Konverteringsprosessen krever at det gjennomføres lagerlukking på en dato som er én dag før den planlagte konverteringsdatoen. Dette kravet sørger for at tilbakedaterte transaksjoner ikke kan angis i overgangsperioden. Hvis det ikke er gjennomført lagerlukking, blir du spurt om du vil gjennomføre den som en del av konverteringsprosessen. Konverteringen håndterer ett element om gangen. Den starter med de laveste varene i en produktstruktur, basert på varens lavnivåkode. Når en vare er konvertert, endres statusen i konverteringsposten til **Konvertert**. Hvis konverteringsprosessen blir avbrutt, har varer som ikke er konvertert, fremdeles statusen **Kontrollert**. En vellykket konverteringsprosess har følgende innvirkninger:

-   Statusen til konverteringsposten endres fra **Klar** til **Fullført**, og statusen for hver valgte vare endres fra **Kontrollert** til **Konvertert**.
-   Varemodellgruppen for konverterte varer endres slik at den gjenspeiler en ny gruppe som har en standard kostnadslagermodell.
-   Standardkostnader for konverterte varer er aktivert i den dedikerte etterkalkuleringsversjonen.
-   Etterkalkuleringstypen til etterkalkuleringsversjonen endres fra **Konverstering** til **Standardkostnad**, og etterkalkuleringsversjonen fungerer nå som alle andre etterkalkuleringsversjoner for standardkostnader.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Validere og avstemme lagerverdiene for de konverterte varene
I rapporten **Avviksanalyserapport** kan du analysere revalueringsavvik, og i rapporten **Lagerverdi** kan du vise lagerverdi på en bestemt dato.

-   Analyser revalueringsavvik. Bruk rapporten **Avviksanalyserapport** til å vise lagerrevalueringsavvik for de konverterte varene. Du kan også bruke siden **Standard kostnadstransaksjoner** til å vise lagerrevalueringstransaksjoner for de konverterte varene som har lager.
-   Analyser lagerverdien før startdatoen for overgangen. Bruk rapporten **Lagerverdi** til å vise lagerverdier for de konverterte varene. For til-datoen for rapporten kan du bruke en dato som er én dag før startdatoen for overgangen.
-   Analyser lagerverdien før startdatoen for konverteringen. Bruk rapporten **Lagerverdi** til å vise lagerverdier for de konverterte varene. Som til-datoen for rapporten kan du bruke en dato som er én dag før konverteringsdatoen.
-   Analyser lagerverdien på konverteringsdatoen. Bruk **Lagerverdi**-rapporten til å vise lagerverdier fra og med konverteringsdatoen. Både fra-datoen og til-datoen for rapporten må samsvare med konverteringsdatoen. Rapportens utvalgskriterier bør gjenspeile de konverterte varene.
-   Analyser tilbakedaterte lagerbevegelser. Bruk **Lagerverdi**-rapporten til å vise tilbakedaterte lagerbevegelser som ble angitt etter konverteringen. Fra-datoen og til-datoen i rapporten bør stemme overens med startdatoen for overgangen og konverteringsdatoen (minus én dag). Rapportens utvalgskriterier bør gjenspeile de konverterte varene. Rapporten viser lagerbevegelser som ble utført for standardkostnad i løpet av overgangsperioden.


<a name="see-also"></a>Se også
--------

[Forutsetninger for standard kostnadskonvertering](prerequisites-standard-cost-conversion.md)




