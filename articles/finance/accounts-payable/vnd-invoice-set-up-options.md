---
title: Oppsettsalternativer for automatisering av leverandørfakturaer (forhåndsversjon)
description: Dette emnet beskriver alternativene som er tilgjengelige for å definere og konfigurere automatisering av leverandørfakturaer.
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: articl
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: eedc5ae1ed20da4c506b3510eaeac32c0ada3b70
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2020
ms.locfileid: "3905028"
---
# <a name="setup-options-for-vendor-invoice-automation-preview"></a>Oppsettsalternativer for automatisering av leverandørfakturaer (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver alternativene som er tilgjengelige for å definere og konfigurere automatisering av leverandørfakturaer. Funksjoner for fakturaautomatisering bruker følgende typer oppsettsparametere:

- Parametere for å sende importerte leverandørfakturaer til arbeidsflytsystemet og samsvare posterte produktkvitteringslinjer til ventende leverandørfakturalinjer.
- Parametere for bakgrunnsoppgaver for prosessautomatisering. Rammeverket for prosessautomatisering brukes til å sende importerte leverandørfakturaer til arbeidsflytsystemet. Det brukes også til automatisk å samsvare posterte produktkvitteringslinjer med ventende leverandørfakturalinjer. Forskjellige forretningsprosesser bruker dette rammeverket til å definere hvor ofte den valgte prosessen kjører. De tilgjengelige hyppighetene for bakgrunnsprosessene **Samsvar produktkvitteringen med fakturalinjer** og **Send leverandørfakturaer til arbeidsflyt** inkluderer **Time** og **Daglig** .

Hvis du vil konfigurere eller vise informasjon om en bakgrunnsoppgave, kan du gå til **Systemadministrasjon \> Oppsett \> Prosessautomatisering** og velge kategorien **Bakgrunnsoppgave** .

Hvis du vil oppnå en berøringsfri automatisering fra importprosessen via postering av leverandørfaktura, må du definere en arbeidsflyt for leverandørfaktura. Hvis du vil konfigurere en arbeidsflyt, går du **Leverandører > Oppsett > Arbeidsflyter for leverandør** . Hvis du vil sikre at fakturaen kan behandles fra start til slutt uten manuell behandling, må du inkludere en automatisk posteringsoppgave i arbeidsflytkonfigurasjonen. .

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parametere for sending av importerte leverandørfakturaer til arbeidsflytsystemet

Spesifikke parametere brukes for å sende importerte leverandørfakturaer til arbeidsflytsystemet. I tillegg brukes noen parametere til å samsvare posterte produktkvitteringslinjer med ventende leverandørfakturalinjer. I kategorien **Automatisering av leverandørfaktura** på siden **Parametere for leverandør** er parameterne du må angi, delt mellom følgende deler:

- Arbeidsflyt for leverandørfakturaer
- Kontrollere mottakssedler automatisk

Følgende parametere er tilgjengelige:

- **Send automatisk importerte fakturaer til arbeidsflyt** – Hvis du setter dette alternativet til **Ja** , sendes importerte fakturaer automatisk til arbeidsflytsystemet. Hvis dette alternativet er satt til **Nei** , må fakturaene sendes manuelt. Hvis du setter dette alternativet til **Ja** , aktiverer du en berøringsfri prosess fra importresultatene via postering.

    Du kan bare sette dette alternativet til **Ja** hvis det er angitt en aktiv arbeidsflyt for leverandørfaktura for den juridiske enheten. Hvis du vil konfigurere en arbeidsflyt, går du **Leverandører \> Oppsett \> Arbeidsflyt for leverandør** .

- **Samsvar produktkvitteringer med fakturalinjer før automatisk sending** – Hvis du setter dette alternativet til **Ja** , kan ikke den importerte fakturaen sendes automatisk til arbeidsflytsystemet før det samsvarende antallet produktkvitteringer er lik fakturaantallet. Ved å sette dette alternativet til **Ja** , aktiverer du automatisk samsvar av posterte produktkvitteringer med fakturalinjer som en treveis kontrollpolicy er definert for. Prosessen vil kjøre til det samsvarende produktkvitteringsantallet er lik fakturaantallet. På dette tidspunktet sendes fakturaen automatisk til arbeidsflytsystemet.

    Alternativet for å tilordne produktkvitteringer til fakturalinjer før automatisk sending er tilgjengelig bare hvis det er merket av for alternativ **Aktiver validering av fakturakontroll** . Når dette alternativet er valgt, blir alternativet for **automatisk samsvar av produktkvitteringer med fakturalinjer** valgt.

- **Krev at beregnede totaler er lik de importerte totalene for automatisk sending av arbeidsflyt** – Hvis du setter dette alternativet til **Ja** , kan ikke fakturaen sendes automatisk til arbeidsflytsystemet før totalene som beregnes for fakturaen, tilsvarer de importerte totalene. Hvis dette alternativet er satt til **Nei** , kan fakturaen sendes automatisk til arbeidsflytsystemet, men den kan ikke posteres før de beregnede totalene er rettet, slik at de samsvarer med de importerte totalene. Hvis du ikke importerer fakturabeløpet eller mva-beløpet, skal dette alternativet settes til **Nei** .
- **Samsvar automatisk produktkvitteringer med fakturalinjer** – Hvis du setter dette alternativet til **Ja** , kan bakgrunnsbehandling brukes til å utføre automatisk samsvar med posterte produktkvitteringer med fakturalinjer som en treveis kontrollpolicy er definert for. Denne prosessen vil bli kjørt til det samsvarende antallet produktkvitteringer er lik fakturaantallet, eller til verdien i feltet for **antallet ganger å forsøke automatisk samsvar** er nådd. Prosessen kan kjøres før fakturaen er sendt til arbeidsflytsystemet.

    Dette alternativet er bare tilgjengelig hvis alternativet **Aktiver validering av fakturakontroll** er valgt.

    Hvis du setter alternativet **Samsvar produktkvitteringer med fakturalinjer før automatisk samsvar** til **Ja** , kan ikke dette alternativet settes til **Nei** . Hvis du setter dette alternativet til **Nei** , må du først sette alternativet **Samsvar produktkvitteringer med fakturalinjer før automatisk samsvar** til **Nei** .

- **Antall ganger å forsøke automatisk samsvar** – Velg antall ganger som systemet skal prøve å samsvare produktkvitteringer med en fakturalinje før prosessen mislykkes. Når det angitte antallet forsøk er nådd, fjernes fakturaen fra automatiseringsbehandlingen.
- **Valider bare når det samsvarende antallet produktkvitteringer er lik fakturaantallet** – Hvis du velger dette alternativet valideres fakturakontroll automatisk bare når det samsvarende antallet produktkvitteringer for fakturalinjen tilsvarer fakturaantallet for fakturalinjen. Hvis det ikke er merket av for dette alternativet, valideres fakturakontroll hver gang systemet automatisk samsvarer en produktkvitteringslinje med en fakturalinje.
