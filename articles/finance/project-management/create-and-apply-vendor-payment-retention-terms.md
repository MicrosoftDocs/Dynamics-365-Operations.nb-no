---
title: Opprette og ta i bruk betingelser for tilbakeholdelse av leverandørbetaling
description: Dette emnet gir informasjon om hvordan du konfigurerer og opprettholder betingelser for tilbakeholdelse av leverandørbetalinger.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410253"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Opprette og ta i bruk betingelser for tilbakeholdelse av leverandørbetaling

[!include [banner](../includes/banner.md)] 

Det er nyttig å definere tilbakeholdelsesbetingelser for leverandørbetalinger for et prosjekt når organisasjonen ønsker å tilbakeholde en del av betalingene til en leverandør. Dette kan for eksempel være om du vil vente med å betale en leverandør til produktene de leverer, oppfyller forventningene dine. Betingelser for tilbakeholdelse av leverandørbetalinger kan spesifiseres når du forhandler om en leverandørkontrakt.

## <a name="create-vendor-payment-retention-terms"></a>Opprett betingelser for tilbakeholdelse av leverandørbetaling

Du kan prosenten av en leverandørbetaling som skal holdes tilbake, og prosenten av tidligere tilbakeholdte beløp som skal frigis. Beløp tilbakeholdes automatisk på leverandørfakturaer til kontrakten når angitt fullføringstilstand. Når du har definert betingelsene for tilbakeholdelse, kan du bruke dem på alle prosjekter for den aktuelle leverandøren.

Bruk følgende trinn for å konfigurere og vedlikeholde betingelser for tilbakeholdelse av leverandørbetalinger. 

1. Gå til **Prosjektstyring og regnskap** > **Tilbakeholdelse** > **Betingelser for tilbakeholdelse av leverandørbetaling**.
2. Velg **Ny** for å legge til en ny betingelse for tilbakeholdelse av leverandørbetaling. Verdien for **Regel-ID** for den nye betingelsen angis automatisk. 
3. Skriv inn en kort beskrivelse i **Beskrivelse**-feltet, gå til **Betingelser**-hurtigkategorien og velg **Legg til linje** for å angi betingelsesverdier for følgende:

   - **Prosent av leverte enheter**: Angi en fullføringsprosent for betingelsen. Beløp tilbakeholdes automatisk på leverandørfakturaer til fullføringsstadiet for prosjektet er lik den spesifiserte prosentdelen. Hvis du for eksempel angir 50,00, tilbakebeholdes beløp til prosjektet er 50 prosent fullført.
   - **Prosent som skal tilbakeholdes**: Angi prosenten av et leverandørfakturabeløp som skal tilbakeholdes. Hvis du for eksempel angir 10,00, tilbakeholdes 10 prosent av beløpet på en leverandørfaktura til prosjektet når fullføringsprosenten du valgte i feltet **Prosent av leverte enheter**.
   - **Prosent som skal frigis**: Velg **Legg til linje** for å angi prosenten av eventuelle tidligere tilbakeholdte beløp som skal frigis på det valgte nivået av prosjektfullføring.

> [!NOTE]
> Hvis du har flere milepæler for ulike nivåer av prosjektfullføring, angir du en egen linje med betingelse for tilbakeholdelse av leverandørbetaling for hver enkelt tilbakeholdelsesregel. Hver linje kan ha en egen prosentdel for tilbakeholdelse, og en egen prosentdel som skal frigis, for hvert angitte nivå av prosjektfullføring.

Når du har definert betingelsene for tilbakeholdelse for en leverandør, kan du bruke dem i et prosjekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Ta i bruk betingelser for tilbakeholdelse av leverandørbetalinger i et prosjekt

1. Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**, og åpne et prosjekt fra prosjektlistesiden.
2. Klikk **Legg til linje** på hurtigfanen **Leverandøravtaler**.
3. Velg ett av følgende alternativer i **Kontokode**-feltet: 

   - **Tabell**: Betingelsene for tilbakeholdelse av leverandørbetaling gjelder for én leverandør.
   - **Gruppe**: Betingelsene for tilbakeholdelse av leverandørbetaling gjelder alle leverandører i en leverandørgruppe.
   - **Alle**: Betingelsene for tilbakeholdelse av leverandørbetaling gjelder alle leverandører.

4. Velg leverandøren eller leverandørgruppen som betingelsene for tilbakeholdelse av leverandørbetaling gjelder for, i feltet **Leverandør/leverandørgruppe**. Hvis du valgte **Alle** i forrige trinn, er dette feltet utilgjengelig.
5. I **Betingelser for tilbakeholdelse for leverandør**-feltet velger du tilbakeholdelsesbetingelsene du opprettet i forrige prosedyre.
6. Hvis prosjektet også har etterbetalingsvilkår definert for leverandøren, angir du terskelprosenten for prosjektet i feltet **Terskelprosent for etterbetaling**.

Betingelsene for tilbakeholdelse av leverandørbetaling vises også på bestillinger du oppretter for leverandøren.
