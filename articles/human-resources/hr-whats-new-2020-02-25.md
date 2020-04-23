---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (25. februar 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 720b4e03549a059c8945bec9d27de9cdcaada488
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092758"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (25. februar 2020)?

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.2927. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Aktivere Saksbehandling-navigering og enhet for rammeverk for databehandling (DMF) (414754)

Denne forhåndsvisningsfunksjonen muliggjør ytterligere navigering til saksbehandlingstilfeller. Du kan aktivere denne forhåndsvisningsfunksjonen i arbeidsområdet **Funksjonsbehandling**. Disse menypunktene vises i **Samsvar**-arbeidsområdet for Dynamics 365 Human Resources. Med denne endringen kan Human Resources ha tilgang til følgende:

- Alle saker
- Mine saker
- Mine åpne tilfeller
- Mine forfalte tilfeller
- Saker tilordnet til meg via arbeidsflyt

Sammen med disse nye visningene i saker kan DMF-enheten **Saksdetalj** også være tilgjengelig.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Aktivere relasjonsdefinisjoner i den globale adresseboken (414762)

Relasjoner er nå aktivert i den globale adresseboken. Før frigivelsen denne uken, viste **Relasjon**-faktaboksen alle systemdefinerte relasjoner. Nå kan du definere disse relasjonene i den globale adresse bok-siden.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>En stilling kan fjernes når det finnes aktive kompensasjonsposter for stillingen (414568)

Med denne endringen vises det en advarsel når du prøver å slette en stilling, og en arbeider har en aktiv kompensasjonspost for den samme stillingen. Når dette skjer, må du oppdatere den faste kompensasjonsposten for den ansatte før du fjerner stillingen.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Medarbeidersamtale-arbeidsflyt legger iblant til godkjenninger fra personer som ikke er en del av prosessen (414171)

Denne endringen løser et problem der flere godkjenningsdeltakere legges til i medarbeidersamtalen.

## <a name="worker-position-assignment-not-created-in-common-data-service-when-selected-on-the-new-worker-dialog-413479"></a>Tilordninger for arbeiderstilling opprettes ikke i Common Data Service når valgt i dialogboksen Ny arbeider (413479)

Denne endringen korrigerer et problem når du ansetter en ny arbeider og tilordner den nyansatte gjennom dialogboksen **Ny arbeider**. Nå vil stillingstilordningen gjenspeiles i Common Data Service.

## <a name="coming-soon"></a>Kommer snart

### <a name="updated-common-data-service-solution"></a>Oppdatert Common Data Service-løsning

En ny Common Data Service-løsning vil snart være tilgjengelig med følgende endringer:

| Beskrivelse | Vekslepenger |
| ----------------------------------------- | --- |
| Endringer i enheten **Jobb/stilling** | **Kompensasjonsområde** lagt til</br>**Finansdimensjoner** lagt til |
| Endringer i **Arbeider**-enheten | **Navnerekkefølge** lagt til</br>**Arbeider hjemmefra** lagt til</br>**Språk** lagt til</br>**Ansiennitetsdato** lagt til</br>**Jubileumsdato** lagt til</br>**Opprinnelig ansettelsesdato** lagt til |
| Endringer i **Ansettelse**-enheten | **Finansdimensjoner** lagt til</br>**Avslutningsårsak** lagt til</br>**Avslutningsdato** endret navn fra **Overgangsdato**</br>**Prøvedato** lagt til |
| Endringer i **Arbeideradresse**-enheten | **Gateadresse** lagt til</br>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving |
| Nye enheter for oppsett av variabel kompensasjon | **Type variabel kompensasjonsplan**</br>**Variabel plan for kompensasjon**</br>**Overdragelsesregler**</br>**Nivå for variabel kompensasjonsplan** |
| Ny enhet, **Ansettelse i arbeiderkalender** | **Arbeidskalenderenhet** lagt til |
| Ny enhet, **Lønnstillingsdetaljer** | **Lønnsstillingsdetaljer** lagt til |
| Ny **Tittel**-enhet | **Tittel** lagt til. Den nye **Tittel**-enheten blir tatt med i synkroniseringsprosessen mellom Human Resources og Common Data Service. Det blir i utgangspunktet ikke referert fra enhetene **Stilling** eller **Jobb**. |

De neste ukene vil disse enhetsendringene være tilgjengelige i alle miljøer. Slik installerer du den nyeste Common Data Service-løsningen for Human Resources manuelt:

1.  Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com).

2.  Velg **Miljøer**.

3.  Finn miljøet du vil oppgradere. Miljøet må samsvare med **miljønavn** i **Common Data Service**-informasjonsdelen i **Om**-skjemaet i Human Resources.

4.  Velg miljøet for å vise miljødetaljer.

5.  Velg **Administrer løsninger** på handlingslinjen øverst. Et nytt leservindu åpner og navigerer til **Administrasjonssenter for Dynamics 365** i konteksten til miljøet ditt.

6.  I **Løsning**-listen velger du **Dynamics 365 Human Resources Anker**.

7.  Velg **Oppgrader** hvis du vil bruke den nyeste løsningen.

## <a name="in-preview"></a>I forhåndsvisning

Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:

- **Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).