---
title: Kontantstrømprognose (forhåndsversjon)
description: Dette emnet beskriver funksjonen for kontantstrømprognoser.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3e9237980144ea65e1ff5135e277151970dbfdbb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208611"
---
# <a name="cash-flow-forecast-preview"></a>Kontantstrømprognose (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kontantstrøm er avgjørende for alle bedrifter. Selv lønnsomme firmaer kan stå i fare for å gå konkurs hvis de ikke opprettholder kontantstrømmen for å dekke umiddelbare behov. Muligheten for kontantstrømprognoser i Finance Insights kan hjelpe firmaer med å overvåke og behandle kontantsaldoene effektivt. Denne funksjonen bruker maskinlæring til å hjelpe bedrifter med å lage en mer presis prognose for kontantstrømmer enn tidligere. Den kan også hjelpe ledere å ta beslutninger som optimaliserer salgsmuligheter i konteksten til den gjeldende likviditetsbeholdningen. 

For de fleste firmaer er det en kjedelig, repeterende og manuell prosess å behandle kontantstrøm og kjøre kontantstrømprognoser. De fleste firmaer er avhengige av Microsoft Excel-løsninger som har varierende grad av kompleksitet. Utfordringene ved å lage nøyaktige prognoser for kontantstrøm omfatter følgende:

- Data er ikke tilgjengelige for beslutningstakere fordi de er spredt over flere steder, inkludert følgende: 
  - Regnskaps- eller ressursplanleggingssystemet
  - Programvare for økonomisk planlegging
  - Excel
  - Andre programmer 
- Prognoser er basert på intern kunnskap som er i «siloer» i hvert domene eller hver avdeling.
- Det er usikkert og vanskelig å måle nøyaktigheten til kontantstrømprognoser etter at finansen er realisert.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Detaljer om funksjonen for kontantstrømprognoser
Funksjonen for kontantstrømprognoser omfatter følgende funksjonalitet. 

- Gjør det enkelt å integrere kontantstrømdata fra eksterne systemer i Dynamics 365 Finance. Kontantstrømprognoser kan også bruke rammeverket for import/eksport av data. Dette rammeverket gjør det enkelt å integrere med Excel OData. Du kan også kombinere data fra flere kilder for å opprette en omfattende kontantstrømløsning. 

- Innfører intelligent likviditetsbeholdning. Likviditetsbeholdning opprettes på grunnlag av kundens betalingsatferd for å forutsi når et firma kan forvente kontanter på kontoene. Den analyserer også de historiske mønstrene til betalende leverandører, for å forutsi når fremtidige fakturaer og ordrer sannsynligvis blir betalt. 

- Innfører intelligente kontantstrømprognoser for langsiktige prognoser ved hjelp av tidsserieprognoser gjennom automatisert integrasjon med AI Builder.

- Gir mulighet til å lagre bestemt kontantstrømbeholdning eller -prognoser, redigere dem og deretter enkelt sammenligne og måle prognosens ytelse i forhold til den faktiske finansen.

- Gjør at det kan foretas hva-skjer-hvis-analyse gjennom sammenligning av øyeblikksbilder. Du kan for eksempel opprette flere øyeblikksbilder som representerer et optimistisk, et pessimistisk og det mest realistiske perspektivet på kontantstrømmen, og deretter sammenligne og vise forskjellene.

- Du kan vise kontantstrømprognosen i flere valutaer, på tvers av juridiske enheter, og filtrere og vise kontantstrøm som er knyttet til en bankkonto. 

- Lar deg filtrere og vise bankkontoer som er knyttet til finansdimensjoner.

Funksjonaliteten for kontantstrømprognose i Dynamics 365 Finance gjør det enklere for organisasjonen å transformere kjedelig, kompleks og repeterende kontantstrømprognose til en enkel, automatisert prosess. Når du automatiserer de kjedeligste aspektene ved kontantstrømprognoser, kan du fokusere på avgjørende beslutningstaking for å oppnå ønskede forretningsresultater.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Definere dimensjoner for kontantstrømprognoser
En ny fane på siden **Oppsett for kontantstrømprognose** lar deg styre hvilke finansdimensjoner du vil bruke i arbeidsområdet **Kontantstrømprognose**. Denne fanen vises bare når funksjonen for kontantstrømprognose er aktivert. 

I fanen **Dimensjoner** velger du dimensjoner som skal brukes til filtrering, fra listen over dimensjoner, og bruker piltastene til å flytte dem til høyre kolonne. Du kan bare velge to dimensjoner til filtrering av data for kontantstrømprognose. 

#### <a name="privacy-notice"></a>Personvernerklæring
Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]