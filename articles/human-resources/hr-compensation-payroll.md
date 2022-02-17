---
title: Klar til betaling
description: Dette emnet viser hvordan du merker en ansatt som klar til betaling i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 08/25/2021
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
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 825aa327cc1530675fad57be6fc1b4313f0cf998
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068976"
---
# <a name="ready-to-pay"></a>Klar til betaling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Hvis du vil merke en ansatt som klar til betaling, må du først aktivere funksjonaliteten for **(forhåndsversjon) lønnsintegrering** i funksjonsbehandling. Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

Ved hjelp av denne funksjonen kan personaleksperter forstå hvilke ansatte som er klare til lønnsbehandling og hvilke som krever handling før de forbrukes av en lønnsleverandør fra en tredjepart.

## <a name="mark-employee-as-ready-to-pay"></a>Merk en ansatt som Klar til betaling

Innsamling og validering av ansattinformasjon kan være tidkrevende og utsatt for feil. Ved hjelp av en metode som gjør det mulig for medarbeidere å gå gjennom og oppdatere ansattinformasjon på en enkel måte, bidrar Dynamics 365 Human Resources til å redusere tiden som brukes på å gjøre seg klar til behandle lønn.

Slik merker du en ansatt som Klar til betaling:

1. Åpne **Kompensasjonsstyring**. Det er to fliser i arbeidsområdet: 
    - **Ansatte er klare til betaling**
    - **Ansatte som ikke er klare til å betale**
    ![Arbeidsområdet Kompensasjonsstyring.](./media/hr-ready-to-pay-1-workspace.png)

2. Velg flisen **Ansatte som ikke er klare til å betale**.

3. Velg de ansatte som skal valideres. I **lønnskategorien** i gruppen **Klar til betaling** velger du **Valider**.
    ![Valider ansatte.](./media/hr-ready-to-pay-2-validate.png)

4. Hvis du vil gå gjennom resultatene, velger du **Resultater** i gruppen **Klar til betaling** i kategorien **Lønn**.

## <a name="validation"></a>Validering

Før en ansatt merkes som klar til betaling, valideres ansattes profil for fullføring.

![Valider resultatene.](./media/hr-ready-to-pay-3-results.png)

| Validering | Detaljer |
| --- | --- |
| **Parameter for adresseformål** | Bekrefter parameteren **Bruk lønnsadresser-formål** er valgt. |
| **Lønnsadresse** | Bekrefter at arbeiderprofilen har minst én adresse med formålet **lønnsbosted** eller **lønnsarbeidssted**, og det er bare én adresse per formål. |
| **Ansettelse** | Bekrefter om arbeideren har minst ett ansettelsesforhold (gjeldende, forrige eller fremtidig). |
| **Identifikasjonsnummer** | Bekrefter at feltet **Bruk identifikasjonstyper i lønnsbehandling** er **Ja** på siden **Human Resources-parametere**, og om identifikasjonstypen som er angitt i parameteren, er fylt ut i arbeidsprofilen. |
| **For- og etternavn** | Bekrefter at feltene **Navn** og **Etternavn** er fylt ut.|
| **Plassering** | Bekrefter at arbeideren har en stilling tilordnet. |
| **Fødselsdato** | Bekrefter at **Fødselsdag**-feltet er fylt ut. |
| **Kompensasjon** | Bekrefter at arbeideren er registrert i en fast kompensasjonsplan. |

Hvis én av disse valideringene mislykkes, kan du ikke merke den ansatte som klar til betaling.

Hvis **Klar til betaling**-feltet er **Nei**, betyr det at du må utføre en handling for å sikre at arbeidsprofilen er fullført. Dette vil ikke stoppe dataene fra å vises i en dataenhet. 

## <a name="process-automation"></a>Prosessautomatisering

Du kan automatisere valideringen av alle ansatte ved hjelp av [Prosessautomatisering](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation). I arbeidsområdet **Kompensasjonsstyring** går du til **Koblinger** \> **Parametere** \> **Prosessautomatiseringer**.

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
