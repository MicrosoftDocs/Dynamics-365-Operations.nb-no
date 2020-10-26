---
title: Policyer for forsendelseskonsolidering
description: Dette emnet gir en oversikt over funksjonaliteten som gir fleksibel konfigurasjon av policyer for forsendelseskonsolidering.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 4afa037ce9e446402128e4908a61ed32a30ebd59
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986956"
---
# <a name="shipment-consolidation-policies"></a>Policyer for forsendelseskonsolidering

Prosessen for forsendelseskonsolidering som bruker policyer for forsendelseskonsolidering, tillater automatisk forsendelseskonsolidering under automatisk og manuell frigivelse til lageret. Den automatiserte konsolideringen som var tilgjengelig før denne funksjonen ble innført, hadde hardkodede felt og var basert på feltet **Konsolider forsendelse ved frigivelse til lager** som ble angitt for et lager.

Policyer for forsendelseskonsolidering brukes til følgende funksjonalitet:

- Den automatiserte satsvise jobben frigivelse-til-lager
- Kommandoen **Frigi til lager** i en salgsordre eller overføringsordre
- Den dedikerte siden **Frigi til lager**
- Kommandoen **Frigi til lager** på siden **Arbeidsområde for lastplanlegging**
- Den manuelle konsolideringen av forsendelser på sidene **Konsolider forsendelser** og **Arbeidsområde for forsendelseskonsolidering**

Før policyer for forsendelseskonsolidering ble innført, eksisterte konsolideringsfunksjonen som en innstilling på lagernivået. Alle ordrer for alle kunder fra ett lager ble behandlet som om de hadde samme konsolideringsbehov. Retningslinjer for forsendelseskonsolidering legger til støtte for scenarioer der forskjellige organisasjoner har forskjellige krav for forsendelseskonsolidering.

Spørringer brukes til å identifisere policyen for forsendelseskonsolidering som gjelder, og deretter bestemmer et redigerbart sett med felt hvordan belastningslinjene grupperes på forsendelsesnivået. (Dette mønsteret ligner på mønsteret som bølgemaler følger.) I tillegg er alternativet **Konsolider med eksisterende forsendelser** lagt til i hver policy. Når dette alternativet er aktivert, finner prosedyren *Frigi til lager* forsendelser for konsolidering ved å søke etter eksisterende forsendelser som ble opprettet basert på den samme konsolideringspolicyen. I dette tilfellet velger systemet en eksisterende forsendelse eller en som skal lastes inn, i stedet for å opprette en ny. Systemet vil imidlertid bare konsolidere med eksisterende forsendelser med statusen *Åpen* . Forsendelser som tilhører en lanseringsbølge med statusen *Frigitt* eller høyere, vurderes ikke som mål for konsolidering.

Når policyer for forsendelseskonsolidering er tilgjengelige, er innstillingen **Konsolider forsendelse ved frigivelse til lager** som tidligere var tilgjengelig på oppsettssiden **Lagere** , skjult. For å hjelpe deg med å gå til den nye funksjonen for forsendelseskonsolidering, oppretter en funksjon på siden **Policyer for forsendelseskonsolidering** en standard policy som automatisk inkluderer den gamle innstillingen for eksisterende lagre. Når denne standardpolicyen er opprettet, blir ikke innstillingen **Konsolider forsendelse ved frigivelse til lager** på oppsettssiden **Lagere** lenger vurdert.

Du kan bruke siden **Frigi til lager** til å overstyre den gjeldende konsolideringspolicyen manuelt på samme måte som du kan overstyre oppfyllelsespolicyer.

Du kan bruke kommandoen **Frigi \> Frigi til lager** på siden **Arbeidsområde for lastplanlegging** til å bygge utgående belastninger som er basert på salgsordre- og overføringsordrelinjer før du frigir til lageret. Disse lastene bruker samme konsolideringslogikk som ble introdusert sammen med konsolideringen av forsendelsespolicyer.

Du kan bruke siden **Arbeidsområde for forsendelseskonsolidering** til å konsolidere eksisterende forsendelser som ennå ikke er bekreftet, men som allerede er frigitt til lageret. Denne funksjonaliteten støtter scenarioer der den automatiserte frigivelsesprosessen, som har en egen forsendelseskonsolidering, kjøres flere ganger en dag, men potensielle flere konsolideringer identifiseres manuelt før forsendelsen til transportøren fullføres under bekreftelsesprosessen. Med denne funksjonen kan du konsolidere utgående forsendelser som opprettes fra salgsordre- eller overføringsordrelinjer når som helst etter at forsendelsene er frigitt til lageret, men før de bekreftes.

Siden **Arbeidsområde for forsendelseskonsolidering** fungerer som arbeidsområdet for lastplanlegging, der du kan vurdere flere forsendelser samtidig og tilordne en ikke-konsolidert ordre til en bestemt forsendelse. Du kan bruke maler for forsendelseskonsolidering til å vurdere foreslåtte konsolideringer flere ganger, og bekrefte dem. Noen regler er implementert for å hindre uautorisert konsolidering og advare deg om mulige feil.

## <a name="overview-of-new-functionality"></a>Oversikt over nye funksjoner

Denne delen beskriver sidene, kommandoene og funksjonene som endres eller legges til når du aktiverer og bruker funksjonen *Policyer for forsendelseskonsolidering* .

### <a name="shipment-consolidation-policies-page"></a>Siden Policyer for forsendelseskonsolidering

Policyer skilles etter arbeidsordretype. Typen **Salgsordrer** representerer forsendelser av typen _Salgsordre_ , og typen **Overføringsordrer** representerer forsendelser av typen _Utstedelse for overføring_ .

Hver policy for forsendelseskonsolidering har en spørring som definerer når den brukes, og et serienummer som bestemmer utføringsrekkefølgen. Konsolidering brukes for hver unike kombinasjon av de valgte feltene. En tilleggsparameter som angis, brukes til konsolidering med eksisterende (åpne) forsendelser. Policyene evalueres og brukes hver gang det opprettes en ny forsendelse (før bølgebehandling).

Hvis en policy mangler noen obligatoriske felt, eller hvis den inkluderer alle forbudte felt, merkes policyen som ugyldig i **Valgt** -delen. Listene over obligatoriske og forbudte felt er hardkodede og kan utvides.

Følgende liste viser de obligatoriske feltene. Ettersom forsendelser alltid deles opp basert på disse feltene, kan du ikke gruppere flere forsendelser som har ulike verdier for disse feltene.

- For salgsordrer:

    - **Kontonummer:** _WHSShipmentTable.AccountNum_
    - **Leveringsmottaker:** _WHSShipmentTable.DeliveryName_
    - **Postadresse (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Lager:** _WHSShipmentTable.InventLocationId_

- For overføringsordrer:

    - **Fra lager:** _InventTransferTable.InventLocationIdFrom_
    - **Til lager:** _InventTransferTable.InventLocationIdTo_

Følgende felt er ikke tilgjengelige for alle dokumenttyper. Disse feltene er ikke synlige i brukergrensesnittet (UI), og de kan ikke brukes til konsolidering.

- **Forsendelses-ID:** _WHSShipmentTable.ShipmentId_
- **Status:** _WHSShipmentTable.ShipmentStatus_
- **Policy for forsendelseskonsolidering:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Arbeidstransaksjonstype:** _WHSShipmentTable.WorkTransType_
- **Bølge-ID:** _WHSShipmentTable.WaveId_
- **Last-ID:** _WHSShipmentTable.LoadId_
- **Forsendelses-ID:** _WHSLoadLine.ShipmentId_
- **Last-ID:** _WHSLoadLine.LoadId_

Når du oppretter en policy, brukes settet med obligatoriske felt som standard som konsolideringsfeltene. Du kan imidlertid endre listen ved å bruke knappen Pil venstre og Pil høyre. (Prosessen ligner på prosessen som brukes til å velge metoder i bølgemaler.)

Verdiene som brukerne velger for disse feltene, brukes for alle nyopprettede forsendelser, eller de blir lagt til i eksisterende forsendelser ved konsolidering med disse forsendelsene. Når to forsendelser har samme verdi for et felt som er valgt for konsolidering av disse forsendelsene, blir forsendelsene konsolidert. Det samme prinsippet gjelder for alle etterfølgende konsolideringsfelt som er valgt. Hvis verdiene er forskjellige, vil den andre forsendelsen bli forkastet og velges for en ny forsendelse. Den automatiserte konsolideringsprosessen består av å opprette alle de unike verdi kombinasjonene for feltene for forsendelseskonsolidering, og deretter tilordne en forsendelse til den relevante kombinasjonen.

Ikke-valgte felt ignoreres under konsolideringsprosessen. Hvis to forsendelser har ulike verdier for et ikke-valgt felt, fjernes merket i feltet (det vil si at det er satt til tomt). Hvis begge forsendelsene har samme verdi for et ikke-valgt felt, fylles feltet ut.

Listen over konsolideringsfelt (det vil si felt som blir slettet hvis de har forskjellige verdier) er hardkodet. Listen inneholder alle felt som er initialisert fra en salgsordre- eller overføringsordrelinje når det opprettes en ny forsendelse. Hvis et felt ikke er initialisert fra en salgsordre- eller overføringsordrelinje, ignoreres det med andre ord når nye data legges til i en eksisterende forsendelse.

### <a name="release-to-warehouse-page"></a>Siden Frigi til lager

- Et nytt felt i det nedre rutenettet viser konsolideringspolicyen som ble brukt.
- Ved hjelp av en ny knapp kan du manuelt velge og/eller overstyre konsolideringspolicyen.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Kommandoen Frigi til lager på siden Arbeidsområde for lastplanlegging

- Logikken ble justert slik at den bruker brukte konsolideringspolicyer.
- Forsendelser konsolideres nå bare for én last.

### <a name="consolidate-shipments-page"></a>Siden Konsolider forsendelser

- Søket etter lignende forsendelser (det vil si kandidater for konsolidering) ble endret slik at det bruker felt som er valgt i policyen for forsendelseskonsolidering.
- Felt som har ulike verdier i forskjellige forsendelser, er nå satt til tom. (Tidligere ble verdiene fra den valgte basisforsendelsen brukt.)

### <a name="shipment-consolidation-workbench-page"></a>Siden Arbeidsområde for forsendelseskonsolidering

- Den nye funksjonaliteten replikerer prosessen for manuell konsolidering med en større skala.
- Nå kan du åpne denne siden fra menyen **Frigi til lager** i modulen **Lagerstyring** .
- Algoritmen analyserer eksisterende forsendelser som ennå ikke er sendt. Deretter foreslår den konsolideringen basert på feltene som er valgt i konsolideringspolicyene.

## <a name="comparison-of-functionality"></a>Sammenligning av funksjonalitet

Tabellen nedenfor viser hvordan forsendelseskonsolidering fungerer når du ikke bruker policyer for forsendelseskonsolidering, og når du bruker dem.

| Uten policyer for forsendelseskonsolidering | Med policyer for forsendelseskonsolidering |
|---|----|
| Gjelder ikke | Salgs- eller overføringsforsendelser som velges for konsolidering, må ha samme konsolideringspolicy som forsendelsen som blir opprettet, eller de må tilordnes til en åpen forsendelse (når alternativet **Konsolider med eksisterende forsendelser** er aktivert). |
| Prosedyren *Frigi til lager* søker ikke etter eksisterende forsendelser for å finne en forsendelse for konsolidering. Bare forsendelser som er opprettet av en gjeldende forekomst av prosedyren *Frigi til lager* , brukes til å finne en forsendelse for konsolidering. | Hvis alternativet **Konsolider med eksisterende forsendelser** er aktivert for en konsolideringspolicy som for øyeblikket brukes, søker prosedyren *Frigi til lager* gjennom eksisterende forsendelser som ble opprettet basert på den samme konsolideringspolicyen for å finne en forsendelse for konsolidering. Hvis du har to policyer, vil derfor aldri en forsendelse som opprettes basert på policy 2, konsolideres med en forsendelse som ble opprettet basert på policy 1. |
| Gjelder ikke | Hvis en liste med felt for konsolideringspolicy er tomme, eller hvis det ikke blir funnet en policy, opprettes det en ny forsendelse for hver salgsordre- eller overføringsordrelinje. |
| I dette konsolideringsfeltet defineres den unike kombinasjonen av verdier som brukes til å konsolidere forsendelser for en *overføringslinje* . (Alle andre felt ignoreres.)<ul><li>Ordrenummer (OrderNum)</li></ul> | I dette konsolideringsfeltet definerer felt den unike kombinasjonen av verdier som brukes til å konsolidere forsendelser for en *overføringslinje* . (Alle andre felt ignoreres.)<ul><li>Ordrenummer (OrderNum)</li><li>Leveringsmottaker (DeliveryName)</li><li>Postadresse (DeliveryPostalAddress)</li><li>ISO-landkode (CountryRegionISOCode)</li><li>Adresse (Address)</li><li>Område (InventSiteId)</li><li>Lager (InventLocationId)</li><li>Transportør (CarrierCode)</li><li>Transportørtjeneste (CarrierServiceCode)</li><li>Leveringsmåte (ModeCode)</li><li>Transportørgruppe (CarrierGroupCode)</li><li>Leveringsbetingelser (DlvTermId)</li></ul>Disse feltene er de eneste feltene som er tilgjengelige og initialisert når det opprettes en ny forsendelse. |
| I dette konsolideringsfeltet definerer felt den unike kombinasjonen av verdier som brukes til å konsolidere forsendelser for en *salgslinje* . (Alle andre felt ignoreres.)<ul><li>Ordrenummer (OrderNum)</li><li>Kundereferanse (CustomerRef)</li><li>Kunderekvisisjon (CustomerReq)</li><li>Leveringsbetingelser (DlvTermId)</li></ul> | I dette konsolideringsfeltet definerer felt den unike kombinasjonen av verdier som brukes til å konsolidere forsendelser for en *salgslinje* . (Alle andre felt ignoreres.)<ul><li>Ordrenummer (OrderNum)</li><li>Kontonummer (AccountNum)</li><li>Leveringsmottaker (DeliveryName)</li><li>Postadresse (DeliveryPostalAddress)</li><li>ISO-landkode (CountryRegionISOCode)</li><li>Adresse (Address)</li><li>Område (InventSiteId)</li><li>Lager (InventLocationId)</li><li>Transportør (CarrierCode)</li><li>Transportørtjeneste (CarrierServiceCode)</li><li>Leveringsmåte (ModeCode)</li><li>Transportørgruppe (CarrierGroupCode)</li><li>Megler-ID (BrokerCode)</li><li>Retning (LoadDirection)</li><li>Leveringsbetingelser (DlvTermId)</li><li>Kundereferanse (CustomerRef)</li><li>Kunderekvisisjon (CustomerReq)</li></ul>Disse feltene er de eneste feltene som er tilgjengelige og initialisert når det opprettes en ny forsendelse. |
| Gjelder ikke | Følgende konsolideringsfelt er obligatoriske for en *salgslinje* og kan ikke fjernes:<ul><li>Kontonummer (AccountNum)</li><li>Leveringsmottaker (DeliveryName)</li><li>Postadresse (DeliveryPostalAddress)</li><li>Lager (InventLocationId)</li></ul>Som standard blir disse feltene tilordnet når en ny policy opprettes. De kan ikke fjernes. |
| Prosedyren *Frigi laster til lager* på siden **Arbeidsområde for lastplanlegging** bruker sin egen kode til å opprette forsendelser og bølger. | Policyer for forsendelseskonsolidering brukes til å bestemme hvilke felt som skal evalueres for konsolidering. Forsendelser konsolideres bare for én last. |
| Du velger manuelt **Konsolider forsendelser** på siden **Alle forsendelser** , og deretter velger du en målbasisforsendelse. Filteret vil foreslå eventuelle eksisterende forsendelser som har tilsvarende verdier for flere nøkkelfelt. | Du velger manuelt **Konsolider forsendelser** på siden **Alle forsendelser** , og deretter velger du en målbasisforsendelse. Systemet vil foreslå andre eksisterende forsendelser ved å sammenligne verdiene for flere nøkkelfelt som er konfigurert for de aktuelle policyene for forsendelseskonsolidering. |
| Du kan bruke kommandoen **Konsolider forsendelser** på siden **Alle forsendelser** bare for én forsendelse. | Siden **Arbeidsområde for forsendelseskonsolidering** hjelper deg med å finne et sett med forsendelser som ennå ikke er i en sendt tilstand. Disse forsendelsene analyseres basert på flere nøkkelfelt som er konfigurert i policyene for forsendelseskonsolidering. Eventuelle forsendelser der verdiene i disse feltene samsvarer, foreslås for konsolidering.<p>Du kan vedlikeholde konsolideringen manuelt ved å fjerne forsendelser fra foreslåtte konsolideringer og/eller ved å legge til leveringer i dem. Det kan oppstå flere typer feil, men du kan overstyre noen av dem.</p> |
| **Utformingsmerknad:** Prosedyren *Frigi salgsordrer til lager automatisk* deler salgslinjer inn i grupper. Hver gruppe har sin egen unike verdi for **ReleaseToWarehouseId** , og behandles separat av prosedyren *Frigi til lager* . Denne fremgangsmåten oppretter nytt arbeid uavhengig av oppsettet for arbeidspause. | **Utformingsmerknad:** Prosedyren *Frigi salgsordrer til lager automatisk* tilordner samme verdi for **ReleaseToWarehouseId** til alle salgslinjer som behandles. Alle salgslinjer blir behandlet av prosedyren *Frigi til lager* samtidig. Hvis du vil sikre den tidligere virkemåten, må du konfigurere arbeidspause per forsendelses-ID. |

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)