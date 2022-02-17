---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 19. november 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i den frittstående versjonen av Microsoft Dynamics 365 Human Resources for 19. november 2021.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 618d90f95637002f444b334e16d3fef466dda65e
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087480"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 19. november 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Microsoft Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne utgivelsen inkluderer følgende feilrettinger. Endringer gjelder for Build-nummeret 8.1.4591.

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | Beskrivelse |
|---|---|---|
| 626178 | Navigasjon mangler fra arbeiderflisene i **Lederselvbetjening** | Dette problemet er nå løst. Navigeringen er tilgjengelig for å se rapportdetaljene i **Lederselvbetjening**. |
| 632573 | Det er ingen valideringsfeil ved lagring av et **Kurs** | Dette problemet er nå løst. Ved oppretting av et kurs der **Minimum antall deltakere** var høyere enn 0, var det fremdeles tillatt å lagre, selv om **Maksimalt antall deltakere** er 0. |
| 615955 | Feilen "Feltet **Formål** må fylles ut når det opprettes en ny rekrutteringsforespørselslokasjon. | Når du oppretter en adresse for en ny rekrutteringsforespørselslokasjon, vises feilen: "Feltet Formål må fylles ut." Med **Formål**-feltet er ikke tilgjengelig på siden. |
| 620797 | Tom **Kjønn**-feltfeil er villedende | Når et kjønn ikke angis for en personlig kontakt, viser rapporten "Klikk eller trykk her for å skrive inn tekst" – Dette er villedende, fordi ingenting kan angis i feltet. |
| 620800 | Koblingen for fordelsoppgave er skjult | Fordelsoppgaven kan ikke vises som standard i **Ansattselvbetjening**.  Det er lagt til en kobling til høyre for **Ansattselvbetjening** under **Koblinger**-delen |
| 629778 | Ytelsesproblem med CDS-integrering. | Autorisasjonsrelatert forespørsel om ytelsesproblem. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om hvordan du aktiverer eller deaktiverer funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
|---|---|---|
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Kommer snart
Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Dynamics 365 og bransjeskyer: 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
