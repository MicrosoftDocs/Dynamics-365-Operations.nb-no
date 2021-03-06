---
title: Talent-systemkrav
description: Dette emnet viser kravene for Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462098"
---
# <a name="talent-system-requirements"></a>Talent-systemkrav

[!include [banner](includes/banner.md)]

Dette emnet beskriver krav for Microsoft Dynamics 365 Talent, inkludert Attract og Onboard. Det beskriver også landene og områdene der Talent er tilgjengelig, pluss informasjon om språk og lokalisering for Talent-data. I tillegg inneholder dette emnet oppdateringspolicyen for Talent.

## <a name="supported-web-browsers"></a>Nettlesere som støttes

Microsoft Dynamics 365 Talent kan kjøre i følgende nettlesere som kjører på de angitte operativsystemene: 

*   Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
*   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
*   Google Chrome (nyeste offentlig tilgjengelig versjon)
*   Apple Safari (nyeste offentlig tilgjengelig versjon)

Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted. 

> [!NOTE]
> * Hvis du vil ta skjermbilder som genereres fra Oppgaveopptaker, og inkludere dem i Microsoft Word-dokumenter, må du ha Chrome-tillegget installert. 
> * Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program. Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer. ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.
> * Hvis du vil forhåndsvise PDF-filer, anbefaler vi at du bruker moderne nettlesere som Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows 10 eller Google Chrome (siste offentlig tilgjengelige versjon) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-nettbrett.
>   Nettverkskrav
> * Dynamics 365 Talent er utformet for nettverk med ventetid på 250 til 300 millisekunder (ms) eller mindre. Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Talent. Vi anbefaler at du tester nettverksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test av ventetid for Azure").
> * Krav til båndbredde for Talent avhenger av scenarioet. De vanligste scenarier krever en båndbredde på mer enn 50 kilobyte per sekund (kbps).
> 
> [!WARNING]
> Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav. Samtidig bruk av en bestemt plassering er svært vanskelig å beregne. Kunder som er bekymret for krav til båndbredde, kan bruke en prøveversjon av Talent.

## <a name="supported-microsoft-office-applications"></a>Microsoft Office-programmer som støttes

* Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert. Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](../dev-itpro/office-integration/office-integration-troubleshooting.md "Feilsøke Office-integrering").
* Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.

## <a name="regional-availability-languages-and-localization"></a>Regional tilgjengelighet, språk og lokalisering

Du kan laste ned en PDF-fil med landene, områdene og språkene Talent støtter, på [Internasjonal tilgjengelighet for Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Selv om brukergrensesnittet er lokalisert til andre språk, lagres alle brukerdata på språket de ble lagt inn på. Du kan opprette e-postmeldinger og maler på andre språk, men data som planleggingsinformasjon er bare tilgjengelig på engelsk for øyeblikket.

Hvis du er utvikler og interessert i å lage lands- eller områdespesifikke tilpasninger, eller hvis du vil opprette en løsning for et land eller område som ikke støttes av Microsoft for øyeblikket, kan du se [Globalisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).



[!INCLUDE[footer-include](../includes/footer-banner.md)]