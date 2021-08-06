---
title: Klar til betaling
description: Dette emnet viser hvordan du merker en ansatt som klar til betaling i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
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
ms.openlocfilehash: f9aa9e60b51b1801c07981ad120cb77f65fee286
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/14/2021
ms.locfileid: "6560121"
---
# <a name="ready-to-pay"></a>Klar til betaling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Hvis du vil merke en ansatt som klar til betaling, må du først aktivere funksjonaliteten for **(forhåndsversjon) lønnsintegrering** i funksjonsbehandling. Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

Ved hjelp av denne funksjonen kan personaleksperter forstå hvilke ansatte som er klare til lønnsbehandling og hvilke som krever handling før de forbrukes av en lønnsleverandør fra en tredjepart.

## <a name="mark-employee-as-ready-to-pay"></a>Merk en ansatt som Klar til betaling

Innsamling og validering av ansattinformasjon kan være tidkrevende og utsatt for feil. Ved hjelp av en metode som gjør det mulig for medarbeidere å gå gjennom og oppdatere ansattinformasjon på en enkel måte, bidrar Dynamics 365 Human Resources til å redusere tiden som brukes på å gjøre seg klar til behandle lønn.

Slik merker du en ansatt som Klar til betaling:

1. Åpne **Kompensasjonsstyring**. Det er to fliser i arbeidsområdet 
    - **Ansatte er klare til betaling**
    - **Ansatte som ikke er klare til å betale**
    ![Arbeidsområdet Kompensasjonsstyring.](./media/hr-ready-to-pay-1-workspace.png)

2. Velg flisen **Ansatte som ikke er klare til å betale**.

3. Velg de ansatte som skal valideres. I **lønnskategorien** i gruppen **Klar til betaling** velger du **Valider**.
    ![Valider ansatte.](./media/hr-ready-to-pay-2-validate.png)

4. Hvis du vil gå gjennom resultatene, velger du **Resultater** i gruppen **Klar til betaling** i kategorien **Lønn**.

## <a name="validation"></a>Validering

Før en ansatt merkes som klar til betaling, validerer systemet en grunnleggende validering av profilens fullføring.

![Valider resultatene.](./media/hr-ready-to-pay-3-results.png)

Tabellen nedenfor inneholder mer informasjon om hver av valideringene som utføres. 

| Validering | Detaljer |
| --- | --- |
| Parameter for adresseformål | Validerer hvis parameteren **Bruk lønnsadresser-formål** er på. |
| Lønnsadresse | Validerer hvis arbeiderprofilen har minst én adresse med formålet "lønnsbosted" eller "lønnsarbeidssted", og det er bare én adresse per formål. |
| Ansettelse | Kontroller om arbeideren har minst ett ansettelsesforhold (gjeldende, forrige eller fremtidig). |
| Identifikasjonsnummer | Validerer hvis parameteren "Bruk identifikasjonstyper i lønnsbehandling" er ja, og hvis identifikasjonstypen som er angitt i parameteren, er fylt ut i arbeidsprofilen. |
| For- og etternavn | Validerer om arbeiderprofilen er gyldig, og kontrollerer om feltene **Navn** og **Etternavn** er fylt ut.|
| Plassering | Kontroller om arbeideren har en stilling tilordnet. |
| Fødselsdato | Validerer om arbeiderprofilen er gyldig, og kontrollerer om feltet **Fødselsdag** er fylt ut. |
| Kompensasjon | Kontroller om arbeideren er registrert i en fast kompensasjonsplan. |

Hvis én av disse valideringene mislykkes, kan du ikke merke den ansatte som klar til betaling.

Hvis **Klar til betaling**-feltet er **Nei**, betyr det at du må utføre en handling for å sikre at arbeidsprofilen er fullført. Dette vil ikke stoppe dataene fra å vises i en dataenhet. 

## <a name="known-issues"></a>Kjente problemer

- Du må deaktivere funksjonen **Strømlinjeformet ansattoppføring** i funksjonsbehandling. Flisene i arbeidsområdet for kompensasjonsstyring fungerer ikke riktig hvis du bruker denne funksjonen.
- I arbeiderskjemaet er **kategorien Lønn**, gruppen **Klar til betaling** tilgjengelig for alle brukerroller. 

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
