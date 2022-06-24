---
title: Systemkrav
description: Denne artikkelen viser systemkravene for Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07d14dfe0e6b53c9489c284520a24b97d9887fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879344"
---
# <a name="system-requirements"></a>Systemkrav

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen viser systemkravene for Microsoft Dynamics 365 Human Resources. Det beskriver også landene og områdene der Human Resources er tilgjengelig, og informasjon om språk og lokalisering for Human Resources-data.

## <a name="supported-web-browsers"></a>Nettlesere som støttes

Brukere kan få tilgang til Microsoft Dynamics 365 Human Resources ved å bruke følgende nettlesere som kjører på de angitte operativsystemene: 

*   Microsoft Edge (nyeste offentlig tilgjengelig versjon) i Windows 10
*   Internet Explorer 11 i Windows 10, Windows 8.1 eller Windows 7
*   Google Chrome (nyeste offentlig tilgjengelig versjon)
*   Apple Safari (nyeste offentlig tilgjengelig versjon)

Du finner den nyeste versjonen av hver nettleser ved å gå til programvareprodusentens nettsted. 

## <a name="special-considerations"></a>Spesielle hensyn

* For at Oppgaveopptaker skal kunne ta skjermbilder og inkludere dem i Microsoft Word-dokumenter, må du installere en forhåndsversjon av Chrome-tillegget.
* Redigeringsprogrammet for arbeidsflyt startes som et ClickOnce-program. Bare Microsoft Edge og Internet Explorer (på en støttet versjon av Microsoft Windows) støtter ClickOnce-programmer. ClickOnce-redigeringsprogrammet for arbeidsflyt krever en 64-biters kompatibelt operativsystem.
* Hvis du vil forhåndsvise PDF-filer, anbefaler vi at du bruker moderne nettlesere som Microsoft Edge (siste offentlig tilgjengelige versjon) på Windows 10 eller Google Chrome (siste offentlig tilgjengelige versjon) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-nettbrett.

## <a name="network-requirements"></a>Nettverkskrav

* Human Resources er utformet for nettverk med ventetid på 250 til 300 millisekunder (ms) eller mindre. Dette er ventetiden fra en nettleserklient til Microsoft Azure-datasenteret som er vert for Human Resources. Det anbefales at du tester nettverksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test av ventetid for Azure").
* Krav til båndbredde for Human Resources avhenger av scenarioet. Vanlige scenarioer krever en båndbredde på mer enn 50 kilobyte per sekund (kbps).
 
> [!WARNING]
> Ikke beregne krav til båndbredde fra en klientplassering ved å multiplisere antallet brukere med minimum båndbreddekrav. Samtidig bruk av en bestemt plassering er svært vanskelig å beregne. Kunder som er bekymret for krav til båndbredde, kan bruke en prøveversjon av Human Resources.

## <a name="supported-microsoft-office-applications"></a>Microsoft Office-programmer som støttes

* Hvis du vil kjøre Microsoft Word- eller Microsoft Excel-tilleggene, må du ha Microsoft Office 2016 for Windows eller Mac installert. Hvis du vil ha mer informasjon om versjonskrav, kan du se [Feilsøke Office-integrering](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Feilsøke Office-integrering").
* Hvis du vil vise dokumenter som er generert av funksjonen Eksporter til Excel eller Eksporter til Word, må ha Microsoft Office 2007 eller nyere installert.

## <a name="regional-availability-languages-and-localization"></a>Regional tilgjengelighet, språk og lokalisering

Du kan laste ned en PDF-fil med landene, områdene og språkene Human Resources støtter, på [Internasjonal tilgjengelighet for Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> Selv om brukergrensesnittet er lokalisert til andre språk, lagres alle brukerdata på språket de ble lagt inn på. Du kan opprette e-postmeldinger og maler på andre språk, men data som planleggingsinformasjon er bare tilgjengelig på engelsk for øyeblikket.

Hvis du er utvikler og interessert i å lage lands- eller områdespesifikke tilpasninger, eller hvis du vil opprette en løsning for et land eller område som ikke støttes av Microsoft for øyeblikket, kan du se [Globalisering](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
