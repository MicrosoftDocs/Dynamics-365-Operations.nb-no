---
title: Definere og bruke leverandørbetalinger med metoden betal-når-betalt
description: Dette emnet forklarer hvordan du oppretter betal når-betalt (PWP), slik at du kan frigi delvise leverandørbetalinger basert på kundebetalinger.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284119"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Definere og bruke leverandørbetalinger med metoden betal-når-betalt

[!include [banner](../includes/banner.md)]

Når du godkjenner en leverandør som skal jobbe som underleverandør, kan du holde tilbake betalingen til leverandøren til du er betalt av kunden for prosjektet. For å støtte dette scenariet kan du definere etterbetalingsvilkår når du definerer bestillingen hos leverandøren.

Når en kunde for eksempel betaler et beløp på en prosjektfaktura, kan du frigi hele eller deler av leverandørfakturabeløpet. Bare definer etterbetalingsvilkår som angir at leverandøren blir betalt etter at du mottar en prosentdel av den tilknyttede betalingen fra kunden. Hvis du mottar delbetaling fra en kunde, kan du frigi noen av de relaterte leverandørfakturaene for betaling manuelt.

Følgende eksempel beskriver prosessen når etterbetalingsvilkår brukes.

## <a name="example"></a>Eksempel

Organisasjonen din godtar å levere en kunde 100 datamaskiner som har programvare installert, for en pris på USD 150,00 per datamaskin. Deretter leier du inn en leverandør for å gi deg datamaskinene der programvaren er installert. Ifølge avtalen må kunden godkjenne kvaliteten på datamaskinene før han betaler organisasjonen. Organisasjonens policy er å tilbakeholde betalingen til leverandører inntil kunden har betalt deg. Derfor definerer du prosjektet slik at det har en etterbetalingsprosent på 100.

Leverandøren sender deg 100 datamaskiner som har programvare installert, sammen med en faktura for 10 000,00 USD. Fordi etterbetalingsvilkår er satt opp for prosjektet, betaler du ikke leverandøren ved mottak av datamaskinene. I stedet sender du datamaskinene til kunden, sammen med en faktura for 15 000,00. Kunden undersøker datamaskinene og godkjenner hele beløpet på prosjektfakturaen.

Når du har mottatt hele betalingen fra kunden, betaler du leverandøren hele beløpet på leverandørfakturaen, 10 000,00.

## <a name="set-up-pwp-terms-for-a-project"></a>Definere etterbetalingsvilkår for et prosjekt

Når du definerer etterbetalingsvilkår for et prosjekt, må du angi, som en prosent, minimumsbeløpet som en kunde må betale for prosjektet før du betaler leverandøren. Terskelbeløpet beregnes automatisk på kundefakturaene for prosjektet. Hvis du vil konfigurere terskelprosenten for etterbetalingsvilkår, gjør du følgende:

1. Gå til **Prosjektstyring og regnskap** \> **Projekter** \> **Alle prosjekter**.
2. Finn og åpne prosjektet du vil definere etterbetalingsvilkår for.
3. Klikk **Legg til linje** på hurtigfanen **Leverandøravtaler**.
3. Velg ett av følgende alternativer i **Kontokode**-feltet:

    - **Tabell** – Etterbetalingsvilkårene gjelder én leverandør.
    - **Gruppe** – Etterbetalingsvilkårene gjelder alle leverandører i en leverandørgruppe.
    - **Alle** – Etterbetalingsvilkårene gjelder alle leverandører.

4. Hvis du valgte **Tabell** eller **Gruppe** i det forrige trinnet, velger du leverandøren eller leverandørgruppen som etterbetalingsvilkårene gjelder for, i feltet **Leverandør/leverandørgruppe**. Hvis du valgte **Alle** i forrige trinn, kan ikke feltet **Leverandør/leverandørgruppe** redigeres.
5. Hvis det også er definert betingelser for leverandørbevaring for leverandøren i prosjektet, velger du regel-IDen for bevaringsbetingelsene i feltet **Betingelser for leverandørbevaring**.
6. I feltet **Terskelprosent for etterbetaling** skriver du inn terskelprosent for prosjektet. Prosenten du skriver inn for prosjektet, angir minimumsbeløpet som kunden må betale deg før du betaler leverandøren.

## <a name="create-a-po-that-has-pwp-terms"></a>Opprette en bestilling som har etterbetalingsvilkår

Når du posterer en faktura fra leverandøren og leverandøren er underlagt etterbetalingsvilkår, vises disse vilkårene på bestillingslinjene. Følg denne fremgangsmåten for å opprette en bestilling som har etterbetalingsvilkår.

1. Gå til **Innkjøp og leverandører** \> **Bestillinger** \> **Alle bestillinger**.
2. Velg **Ny** i handlingsruten. Deretter angir du den nødvendige informasjonen i dialogboksen **Opprett bestilling**, og velger **OK**.

    Du kan også åpne en eksisterende bestilling på listesiden **Alle bestillinger**.

4. På **Bestilling**-siden i hurtigfanen **Bestillingslinjer** ser du gjennom detaljene på bestillingslinjen for leverandøren. Alternativet **Betal når betalt** blir valgt automatisk, og verdien i feltet **Terskelprosent for etterbetaling** kopieres automatisk fra feltet **Terskelprosent for etterbetaling** på **Prosjekter**-siden.
6. Hvis du ikke vil bruke etterbetalingsvilkår for leverandøren for en bestillingslinje, fjerner du merket for alternativet **Betal når betalt**. I dette tilfellet blir **Terskelprosent for etterbetaling**-feltet for bestillingslinjen tilbakestilt til 0 (null).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Oppdatere en kundebetaling og betale leverandøren

Når leverandøren fullfører arbeid på prosjektet og sender deg en faktura, må du se gjennom prosjektstatusen og kundefakturaene for å se om etterbetalingsvilkårene er oppfylt for prosjektet. Hvis etterbetalingsvilkårene for leverandøren er oppfylt, kan du fastslå hvilke linjer som skal betales på leverandørfakturaen, basert på kundebetalingene for prosjektet. Hvis du bestemmer deg for å betale leverandøren selv om etterbetalingsvilkårene ikke ble oppfylt, kan du overstyre etterbetalingsvilkårene på siden **Leverandørfaktura med betal når betaling er mottatt**.

1. Gå til **Prosjektstyring og regnskap** \> **Forespørsler og rapporter** \> **Oppbevaringsforespørsler** \> **Leverandørfaktura med betal når betaling er mottatt**.
2. Angi verdier for å finne leverandørfakturaen du vil se gjennom, på siden **Leverandørfaktura med betal når betaling er mottatt**, og velg deretter **Søk**.
3. Velg linjene du vil endre, på hurtigfanen **Leverandørfakturalinjer**.
4. Hvis **Betal når betalt**-betingelsene er oppfylt for fakturalinjen, velger du **Frigi leverandørbetaling**. Alternativet **Betal når betalt** er umerket, og verdien for feltet **Klar til betaling** endres til **Ja**.
