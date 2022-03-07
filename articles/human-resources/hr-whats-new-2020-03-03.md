---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (3. mars 2020)?
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 3. mars 2020.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e39e0c55fddffa99b0a86dba52da120b1ba0d1b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051143"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (3. mars 2020)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.2955. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse-løsningen er nå tilgjengelig med følgende endringer:

En ny Dataverse-løsning vil snart være tilgjengelig med følgende endringer:

| Beskrivelse | Vekslepenger |
| ----------------------------------------- | --- |
| Endringer i enheten **Jobb/stilling** | **Kompensasjonsområde** lagt til</br>**Finansdimensjoner** lagt til |
| Endringer i **Arbeider**-enheten | **Navnerekkefølge** lagt til</br>**Arbeider hjemmefra** lagt til</br>**Språk** lagt til</br>**Ansiennitetsdato** lagt til</br>**Jubileumsdato** lagt til</br>**Opprinnelig ansettelsesdato** lagt til |
| Endringer i **Ansettelse**-enheten | **Finansdimensjoner** lagt til</br>**Avslutningsårsak** lagt til</br>**Avslutningsdato** endret navn fra **Overgangsdato**</br>**Prøvedato** lagt til |
| Endringer i **Arbeideradresse**-enheten | **Gateadresse** lagt til</br>**Adresselinje 1**, **Adresselinje 2** og **Adresselinje 3** merket for avskriving |
| Nye enheter for oppsett av variabel kompensasjon | **Type variabel kompensasjonsplan**</br>**Variabel plan for kompensasjon**</br>**Overdragelsesregler**</br>**Nivå for variabel kompensasjonsplan** |
| Ny enhet, **Ansettelse i arbeiderkalender** | **Arbeidskalenderenhet** lagt til |
| Ny enhet, **Lønnstillingsdetaljer** | **Lønnsstillingsdetaljer** lagt til |
| Ny **Tittel**-enhet | **Tittel** lagt til. Den nye **Tittel**-enheten blir tatt med i synkroniseringsprosessen mellom Human Resources og Dataverse. Det blir i utgangspunktet ikke referert fra enhetene **Stilling** eller **Jobb**. |

De neste ukene vil disse enhetsendringene være tilgjengelige i alle miljøer. Slik installerer du den nyeste Dataverse-løsningen for Human Resources manuelt:

1.  Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com).

2.  Velg **Miljøer**.

3.  Finn miljøet du vil oppgradere. Miljøet må samsvare med **miljønavn** i **Common Data Service**-informasjonsdelen i **Om**-skjemaet i Human Resources.

4.  Velg miljøet for å vise miljødetaljer.

5.  Velg **Administrer løsninger** på handlingslinjen øverst. Et nytt leservindu åpner og navigerer til **Administrasjonssenter for Dynamics 365** i konteksten til miljøet ditt.

6.  I **Løsning**-listen velger du **Dynamics 365 Human Resources Anker**.

7.  Velg **Oppgrader** hvis du vil bruke den nyeste løsningen.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Importproblemer med Permisjonsregistrering-dataenheten (406082)

Du kan nå registrere en ansatt i en ny permisjonsplan av samme type, så lenge den nye registreringsdatoen er senere enn den utløpte registreringsdatoen for den tidligere planen.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Problem med eksportering av bidragssatser i 401k payrollWorkerEnrolledBenefitDetail-enheten i DMF (420700)

Denne endringen korrigerer eksportfunksjonaliteten for **payrollWorkerEnrolledBenefitDetail**-enheten for å gjenspeile de gjeldende verdiene for arbeidsgivers bidrag.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Hvis du søker i det strømlinjeformede Arbeider-skjemaet, kan det vises en melding om at Person-feltet fylles ut (402525)

Når du søker etter en ansatt, vil du ikke lenger få melding om at du må fylle ut **Person**-feltet.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Merknad-feltverdi gjengis ikke i skjemaet Legg til flere kompetanser (380134)

Denne endringen retter opp et problem når du tilpasser skjemaet **Legg til flere kompetanser** i ansattselvbetjeningen.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Flere faste kompensasjonsplaner utløper ikke når ansatte overføres (389466)

Med denne endringen vil alle aktive faste kompensasjonsposter for den gamle stillingen utløpe på overgangsdatoen.

## <a name="in-preview"></a>I forhåndsvisning

Følgende forhåndsversjonsfunksjoner er tilgjengelige fra 3. februar 2020:

- **Forhåndsversjonsfunksjoner for permisjon og fravær** – For mer informasjon, se [Forhåndsversjonsfunksjoner for permisjon og fravær](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Forhåndsversjonsfunksjonen Fordelsbehandling** – For mer informasjon, inkludert kjente problemer, se [Oversikt over Fordelsbehandling](hr-benefits-management-overview.md).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]