---
title: Fakturere for vedlikehold av aktiva som eies av kunden
description: Dette emnet beskriver hvordan du oppretter, behandler og fakturerer for vedlikeholdsarbeid på aktiva som kundene eier.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500460"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Fakturere for vedlikehold av aktiva som eies av kunden

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Med funksjonen *Arbeidsordrefakturering* kan du opprette, behandle og fakturere for vedlikeholdsarbeid på aktiva som kundene eier. Denne funksjonen lar deg utføre følgende oppgaver:

- Koble kunder til aktivaene de eier.
- Velg en kunde, og vis aktivaene som kunden eier, når du oppretter en arbeidsordre.
- Definer et hovedprosjekt for hver kunde.
- Registrer timer, varer, utgifter og gebyrer mot arbeidsordren, og opprett senere et fakturaforslag for kunden.

Funksjonen har i tillegg følgende funksjonalitet:

- Prosjektkontrakten fra et hovedprosjekt for en kunde kopieres automatisk til det relevante arbeidsordreprosjektet.
- Aktivastyring kan nå bruke prosjekttransaksjonstypen *gebyr* i både arbeidsordreprognoser og arbeidsordrejournaler.

## <a name="turn-on-the-customer-billing-feature"></a>Aktivere funksjonen for kundefakturering

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Prosjektstyring og regnskap*
- **Funksjonsnavn:** *Arbeidsordrefakturering*

## <a name="example-scenario"></a>Eksempelscenario

Hvis du vil vite hvordan denne funksjonen fungerer, kan du gå gjennom følgende eksempelscenario.

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke dette scenariet som en veiledning for å bruke funksjonen når du arbeider i et produksjonssystem. I så fall må du imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>Trinn 1: Opprette en ny prosjektkontrakt for kunden

1. Gå til **Prosjektstyring og regnskap \> Prosjekter \> Prosjektkontrakter**.
1. Velg **Ny** i handlingsruten.
1. I dialogboksen **Ny prosjektkontrakt** angir du følgende verdier:

    - **Navn:** *Pelican Wholesales*
    - **Finansieringstype:** *Kunde*
    - **Finansieringskilde:** *US-013* (*Pelican Wholesales)*

1. Velg **OK**.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>Trinn 2: Opprette et nytt hovedprosjekt for kunden

Hovedprosjektet du oppretter her, blir brukt når arbeidsordrer for kunden opprettes.

1. Gå til **Prosjektstyring og regnskap \> Prosjekter \> Alle prosjekter**.
1. Velg **Ny** i handlingsruten.
1. Angi følgende verdier i dialogboksen **Nytt prosjekt**:

    - **Prosjekttype:** *Tid og materialer*
    - **Prosjektnavn:** *Arbeidsordrer for Pelican Wholesales*
    - **Prosjektgruppe:** *TM*
    - **Prosjektkontrakt-ID:** *Pelican Wholesales* (kontrakten du opprettet tidligere)
    - **Startdato:** Velg dagens dato.

1. Velg **Opprett prosjekt**.
1. Det nye prosjektet åpnes. Noter verdien for **Prosjekt-ID**. Du må angi den senere.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>Trinn 3: Opprette en ny arbeidsordretype i Aktivastyring

1. Gå til **Aktivastyring \> Oppsett \> Arbeidsordre \> Arbeidsordretyper**.
1. Velg **Ny** i handlingsruten.
1. Det blir lagt til en ny post i listen. Angi følgende verdier for den:

    - **Arbeidsordretype:** *Service*
    - **Navn:** *Servicearbeidsordrer*
    - **Livssyklustilstand for arbeidsordre:** *Standard*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>Trinn 4: Koble kundekontoen til hovedprosjektet

Du må nå koble kundekontoen til hovedprosjektet i prosjektoppsettet i Aktivastyring.

1. Gå til **Aktivastyring \> Oppsett \> Arbeidsordrer \> Prosjektoppsett**.
1. I fanen **Hovedprosjekt** velger du **Legg til** for å legge til en linje.
1. På den nye linjen angir du følgende verdier:

    - **Kundekonto:** *US-013* (*Pelican Wholesales*)
    - **Prosjekt-ID:** Angi prosjekt-ID-en du noterte tidligere.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>Trinn 5: Koble prosjektgruppen og -typen til arbeidsordreprosjektet

Du skal fortsatt være på siden **Prosjektoppsett** (**Aktivastyring \> Oppsett \> Arbeidsordrer \> Prosjektoppsett**).

1. I fanen **Prosjektgruppe** velger du **Legg til** for å legge til en linje.
1. På den nye linjen angir du følgende verdier:

    - **Arbeidsordretype:** *Service* (arbeidsordretypen du opprettet tidligere)
    - **Prosjektgruppe:** *TM*

> [!NOTE]
> Prosjektkontrakten på arbeidsordreprosjektet arves alltid fra hovedprosjektet.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>Trinn 6: Koble et aktivum til kunde-ID-en

1. Gå til **Aktivastyring \> Aktiva \> Aktive aktiva**.
1. Angi *VE-102* i **Filter**-feltet, og velg å filtrere etter **Aktivum**.
1. Velg aktivumet for å åpne innstillingene for det.
1. I hurtigfanen **Kunde** angir du *US-013* (*Pelican Wholesales*) i **Kundekonto**-feltet.

    **Navn**-feltet oppdateres automatisk til *Pelican Wholesales*.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>Trinn 7: Opprette en ny arbeidsordre for aktivumet

1. Gå til **Aktivastyring \> Arbeidsordrer \> Aktive arbeidsordrer**.
1. Velg **Ny** i handlingsruten.
1. I dialogboksen **Opprett arbeidsordre** angir du følgende verdier:

    - **Arbeidsordretype:** *Service*
    - **Beskrivelse:** *Reparer lastebil*
    - **Kundekonto:** *US-013* (*Pelican Wholesales*)
    - **Aktivum:** *VE-102*

        > [!NOTE]
        > Oppslaget viser bare aktiva som er koblet til den valgte kundekontoen.

    - **Vedlikeholdsjobbtype:** *Reparasjon*
    - **Yrke:** *Mekaniker*
    - **Servicenivå:** *4*

1. Velg **OK**.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>Trinn 8: Gå gjennom arbeidsordren og begynne å arbeide på den

I denne delen skal du arbeide på arbeidsordren du opprettet i den forrige delen.

1. Følg denne fremgangsmåten for å kontrollere at hovedprosjektet er prosjektet *Arbeidsordre for Pelican wholesales*:

    1. Velg en linje i delen **Vedlikeholdsjobber for arbeidsordre**.
    1. Kontroller **Prosjekt-ID**-verdien i hurtigfanen **Linjedetaljer**. Det skal være et nummer med bindestrek i skjemaet *\<Parent-Project-ID\>-\<Project-ID\>*. Denne verdien er en kobling.
    1. Velg koblingen for prosjekt-ID for å åpne en side der du kan vise hovedprosjektet og prosjektnavnene.

1. Velg **Oppdater tilstand for arbeidsordre** i gruppen **Livssyklustilstand** i **Arbeidsordre**-fanen i handlingsruten.
1. Merk av for raden der feltet **Livssyklustilstand** er satt til *Pågår* i **Velg**-kolonnen i dialogboksen **Oppdater tilstand for arbeidsordre**.
1. Velg **OK**.
1. Velg **OK** i dialogboksen **Livssyklustilstand: InProgress**.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>Trinn 9: Postere timene som ble brukt på arbeidsordren, og opprette et nytt fakturaforslag

I denne delen skal du fortsette å arbeide på arbeidsordren du arbeidet på i den forrige delen.

1. Velg **Journaler** i **Prosjekt**-gruppen i **Arbeidsordre**-fanen i handlingsruten.

    Siden **Arbeidsordrejournaler** vises. Her kan du registrere tiden du har brukt på arbeidsordren.

1. Velg **Legg til linje** i hurtigfanen **Timer**.
1. Angi *4* i feltet **Timer** på den nye linjen.
1. Velg **Poster journaler** i handlingsruten.
1. Lukk siden **Arbeidsordrejournaler** for å gå tilbake til arbeidsordren.
1. Velg **Nytt fakturaforslag** i **Fakturering**-fanen i handlingsruten.
1. Merk av for **Velg** for hver linje du vil fakturere, under **Prosjekttransaksjoner** i dialogboksen **Opprett fakturaforslag**.
1. Velg **OK** for å lukke dialogboksen og vise det nye fakturaforslaget.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]