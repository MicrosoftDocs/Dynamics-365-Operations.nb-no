---
title: Oversikt over lean manufacturing
description: Denne artikkelen gir en oversikt over og beskrivelse av lean manufacturing-funksjonene i Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow, Kanban, KanbanQuantityOverview, KanbanAssignCard, KanbanCirculatingCards, KanbanRules, WHSKanbanWaveTableManagePickingListPool
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3da372e4e110b87322a7f2e974bd999c4c085234
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825801"
---
# <a name="lean-manufacturing-overview"></a>Oversikt over lean manufacturing

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over og beskrivelse av lean manufacturing-funksjonene i Dynamics 365 Supply Chain Management.

Lean-produksjon tilbyr verktøy som du kan bruke til å modellere lean-operasjoner. Disse verktøyene støtter og fremmer følgende konsepter og forretningsaktiviteter:
-   Opprett et grunnlag for lean-produksjon ved å modellere produksjons- og logistikkprosesser som produksjonsflyter.
-   Implementer et lean-pullsystem ved å bruke kanbaner til å signalisere behovskrav.
-   Overvåke og vedlikeholde kanban-jobber.

Arkitekturen for lean-produksjon består av produksjonsflyter, aktiviteter og kanban-regler. Disse strukturene er fullstendig integrert med prosessene i Supply Chain Management. Du kan bruke lean-produksjon i et produksjonsmiljø med blandet modus som kombinerer forskjellige strategier for forsyning, produksjon, leverandører. Disse strategiene omfatter produksjonsordrer, partiordrer for prosessindustrier, bestillinger og overføringsordrer.

| **Viktig**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Du kan bruke Supply Chain Management til å støtte implementeringen av lean-produksjon med kanbaner. En vellykket implementering av lean-prinsipper avhenger imidlertid av interne forretningsprosesser som du bruker, og faktiske produksjonsbetingelser og miljøet. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a> Modellere produksjons- og logistikkprosesser som produksjonsflyter
For å opprette et grunnlag for lean-produksjon modelleres produksjons- og logistikkprosesser som produksjonsflyter. Denne aktiviteten består av følgende oppgaver:
1.  Identifiser prosessene som du ønsker å implementere en strategi for lean-etterfylling for, og modellere deretter disse prosessene som produksjonsflyter. Deretter kan du analysere og strømlinjeforme prosessene. En av målene for en lean-implementering er å redusere avfall ved å forbedre flyten av materialer og informasjon.
2.  Definer en produksjonsflyt som en serie med aktiviteter som beskriver flyten av materialer. En overføringsaktivitet definerer flytting av et produkt eller produkter fra én plassering til en annen. En prosessaktivitet definerer en verdiskapende operasjon som utføres på et produkt.
3.  Opprett en versjon av produksjonsflyten som definerer kravene for takttid. Disse kravene beregner syklustiden for hver aktivitet i produksjonsflyten. Du kan opprette flere versjoner av produksjonsflyter og deretter bruke disse versjonene til å forbedre prosesser.

## <a name="using-kanbans-to-signal-demand-requirements"></a> Bruke kanbaner til å signalisere behovskrav
Et pull-system produserer varer bare når varer er nødvendige. Denne fremgangsmåten reduserer leveringstider og overflødig lager. Du kan bruke kanbaner til å planlegge, spore og behandle krav som er basert på produksjonsflyter. Hvis du vil opprette en kanban-struktur, oppretter du kanban-regler som definerer når kanbaner opprettes, og hvordan kravene oppfylles. Du kan opprette to typer kanban-regler. Produksjonsregler oppretter kanban-jobber for prosesser, og kanban-regler for uttak oppretter kanban-jobber for overføring. Du kan definere følgende etterfyllingsstrategier:
-   Kanban-regler med **Fast antall** er knyttet til et bestemt antall behandlingsenheter, som betyr at antall aktive Kanbaner er konstant. Når alle produktene fra en Kanban forbrukes og håndteringsenhetene tømmes manuelt, opprettes en ny Kanban av samme type. Når du oppretter et fast antall Kanban-regler, kan du beregne optimalt Kanban-antall og produktantall som brukes. Beregningen tar hensyn til prognose, faktisk etterspørsel fra åpne ordrer, leveringstid for å etterfylle varer og historiske behov.
-   **Planlagte** kanban-regler etterfyller behov som er beregnet av hovedplanlegging. Hovedplanlegging genererer planlagte Kanbaner som kan autoriseres til Kanbaner.
-   Kanban-regler for **hendelse** etterfyller behov som kommer fra salgsordrelinjer, stykklistelinjer for produksjon, Kanban-linjer eller minimumslagerinnstillinger. Når hendelses-Kanbaner genereres, knyttes de til kildebehov.

Når det opprettes Kanbaner, genereres én eller flere Kanban-jobber basert på Kanban-flytaktivitetene som er definert i Kanban-reglene.

## <a name="monitoring-and-maintaining-kanban-jobs"></a> Overvåke og vedlikeholde kanban-jobber
Lean-produksjon gir oversikt over gjeldende status for produksjonen og logistikkaktiviteter som er underlagt kanban-regler. Som et resultat kan du planlegge og prioritere følgende oppgaver:

-   Få en oversikt over den gjeldende kanban-jobbplanen.
-   Planlegge og opprett ny planlegging av kanban-jobber.
-   Spore og registrere statusen for kanban-jobber.

Listen nedenfor beskriver de spesialiserte kanban-tavlene:
-   Kanban-jobbplanlegging – gir en oversikt over Kanban-jobbene. Tavlen viser kanban-jobber og tilhørende status for én eller flere arbeidsceller. Jobbene vises etter planleggingsperioder (dager eller uker) som er definert i produksjonsflytmodellen. Tavlen viser også kapasitetsforbruket per planleggingsperiode slik at du kan overvåke den planlagte belastningen. Du kan endre statusen for kanban-jobber, foreta ny planlegging av Kanban-jobber i ulike planleggingsperioder og utføre andre oppgaver.
-   Kanban-tavle for overføringsjobber – Denne tavlen gir en oversikt over gjeldende overføringsjobber. Du kan oppdatere og registrere plukklister, starte og fullføre overføringsjobber og utføre andre oppgaver.
-   Kanban-tavle for prosessjobber – Denne tavlen er utviklet for å støtte den vanlige produksjonsflyten og gi en oversikt over den gjeldende situasjonen i én eller flere arbeidsceller. Fra denne tavlen kan Kanbaner prioriteres, plukkes eller produseres. Tavlen er også utformet for å støtte strekkodeskanning for rapportering av Kanbaner.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanban-jobber og integrasjon med prosesser for Supply Chain Management
Kanban-jobber er fullstendig integrert med prosesser for lagertransaksjoner i Supply Chain Management.
-   Du kan utføre plukkaktiviteter for å etterfylle materiale som brukes til å oppfylle kravene til kanban-jobber.
-   Du kan skrive ut Kanban-kort, sirkulerende kanban-kort og plukklister for å støtte bruken av Kanbaner. Disse dokumentene brukes til å representere, spore og registrer Kanban-jobber i lageret og på produksjonsgulvet.
-   Du kan registrere plukking og overføring av aktiviteter på lager ved å skanne strekkoder.

I tillegg støtter lean-produksjon innkjøps- og faktureringsprosesser for tjenester som er referert til av aktiviteter i underleveranser.
-   Du kan tilordne kjøpsavtalelinjer og tjenester til aktiviteter i underleveranser.
-   Du kan opprette periodiske bestillinger og mottaksmeldinger for å støtte kjøp og fakturering av tjenestene.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]