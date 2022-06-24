---
title: Eksperimentering i Dynamics 365 Commerce
description: Eksperimentering gjør det mulig å opprette, redigere og administrere sideoppsett og innholdsbehandling i områdebygger. Støtte for ende-til-ende-eksperimentering er aktivert for e-handelssider og enheter på en side.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946220"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimentering i Dynamics 365 Commerce
Bruk eksperimentering i Dynamics 365 Commerce for å validere hypoteser om effektiviteten til dine e-handelssider og ta avgjørelser med datadrevet selvtillit. Commerce støtter A/B-testing for sider, moduler og fragmenter, og lar deg måle virkningen av foreslåtte endringer på nettstedet ditt.

Du kan opprette, redigere og behandle side- og innholdsbehandling, kalt **variasjoner**, i områdebygger. Commerce integreres med tredjepartstjenester som du kan bruke til å opprette eksperimenter og behandlingsoppgaver. Sanntids hendelsesstrømmer som registreres i Commerce, aktiverer analyse som definerer eksperimentresultatene i tredjepartstjenesten. Du kan deretter bruke disse analysene for å hjelpe til med å støtte eller motbevise hypotesen din.

## <a name="set-up-prerequisites"></a> Definer forutsetninger

1. **Skaff riktig versjon av Commerce** – Oppgrader modulbibliotek, SDK for nettkanalutvidelse og Commerce Scale Unit til Commerce versjon 10.0.13 eller nyere.
1. **Konfigurer en eksperimenteringskobling** – En eksperimenteringskobling lar Commerce koble til tredjepartstjenester for å hente listen over eksperimenter og avgjøre når det skal vises et eksperiment for en bruker. Du kan kjøpe en tredjepartskobling fra [AppSource](https://appsource.microsoft.com). Følg installasjonsinstruksjonene fra utgiveren. Du kan også bruke eksempeltestkoblingen fra Commerce til å teste eksperimenteringsarbeidsflyten uten å måtte konfigurere en ekstern tjeneste. Hvis du vil ha mer informasjon, kan du se [Konfigurere og aktivere koblinger](e-commerce-extensibility/connectors.md). 
1. **Slå på flagget for eksperimenteringsfunksjonen i Commerce** – Du kan aktivere eksperimentering på leiernivået ved å gå til **Leierinnstillinger \> Funksjoner**, eller på områdenivå ved å gå til **Områdeinnstillinger \> Funksjoner**. Slå på **Eksperimentering**-flagget for å begynne å opprette modulvariasjoner. Hvis du deaktiverer dette flagget, stopper du alle eksperimenter fra å vises til brukere og fjerner alle redigeringsfunksjonene i områdebygger.
    
## <a name="experimentation-lifecycle"></a>Livssyklus for eksperimentering

Konfigurasjon av et eksperiment, oppretting av variasjoner og kjøring av et eksperiment er en gjentakende prosess. Diagrammet nedenfor illustrerer livssyklusen for eksperimentering i Commerce og tredjepartstjenesten. 

[ ![Livssyklus for eksperimentering.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Hvis du vil finne ut mer om hvert trinn i eksperimenteringsprosessen, kan du se artiklene nedenfor.
- [Identifisere en hypotese og fastslå måledataene for et eksperiment](experimentation-identify.md)
- [Definere et eksperiment](experimentation-setup.md)
- [Koble til og redigere et eksperiment](experimentation-connect-edit.md)
- [Forhåndsvise og publisere et eksperiment](experimentation-preview-publish.md)
- [Kjør og Overvåk et eksperiment](experimentation-run-monitor.md)
- [Fremme en variasjon og fullføre et eksperiment](experimentation-review-complete.md)

> [!NOTE]
> Hvis du vil vite hvor et eksperimenter er i livssyklusen, velger du **Eksperimenter** i den venstre navisjonsruten i områdebygger. En liste over eksperimenter vises med statusen for hvert eksperiment i både Commerce og tredjepartstjenesten. Hvis du vil ha mer informasjon, kan du se [Se gjennom statusen for et eksperiment](experimentation-status.md).

## <a name="next-step"></a>Neste trinn
[Identifisere en hypotese og fastslå suksessmåledataene for et eksperiment](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
