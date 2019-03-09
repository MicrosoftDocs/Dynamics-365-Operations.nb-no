---
title: Vise ordrevarslinger på salgsstedet (POS)
description: Dette emnet beskriver hvordan du aktiverer ordrevarslinger på salgsstedet og varselrammeverket. Til slutt kan utviklere utvide disse meldingene til andre operasjoner enn ordreoppfyllelsesoperasjoner.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 41f16d13051f6095bdb04af1586ec06fe0ce93f6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "361343"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Vise ordrevarslinger på salgsstedet (POS)

[!include [banner](includes/banner.md)]

I moderne detaljhandelsmiljø har butikkansatte forskjellige oppgaver, for eksempel hjelpe kunder, slå inn transaksjoner, utføre lagertelling og motta ordrer i butikken. Salgsstedsklienten (POS) er ett enkelt program som gjør det mulig for ansatte å utføre disse oppgavene og mye mer. Fordi forskjellige oppgaver utføres i løpet av dagen, kan det hende at ansatte trenger å bli varslet når noe krever deres oppmerksomhet. Varslingsrammeverket i POS hjelper med dette ved at forhandlerne kan konfigurere rollebaserte meldinger. I Microsoft Dynamics 365 for Retail med programoppdatering 5 kan disse meldingene bare konfigureres for salgsstedsoperasjoner.

For øyeblikket kan systemet bare vise meldinger for ordreoppfyllelsesoperasjoner. Men fordi rammeverket er utformet for å være utvidbar, skal utviklerne til slutt kunne skrive en varslingsbehandler for alle typer operasjoner, og vise meldingene for operasjonen på salgsstedet.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Aktivere varslinger for ordreoppfyllelsesoperasjoner

Hvis du vil aktivere varslinger for ordreoppfyllelsesoperasjonene, bruk følgende fremgangsmåte.

1. Gå til **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Operasjoner**.
2. Søke etter operasjonen **Ordreoppfyllelse**, og merk av for **Aktiver varslinger** for å angi at varslingsrammeverket skal høre på handleren for denne operasjonen. Hvis handleren er implementert, vises deretter meldinger for denne operasjonen på salgsstedet.
3. Gå til **Handel** &gt; **Ansatte** &gt; **Arbeidere** &gt;. I kategorien Handel åpner du salgsstedstillatelser som er knyttet til arbeideren. Utvid hurtigfanen **Meldinger**, legg til operasjonen **Ordreoppfyllelse** og sett verdien til feltet **Visningsrekkefølge** til **1**. Hvis mer enn én melding er konfigurert, brukes dette feltet til å ordne meldingene. Meldinger som har en lavere verdi for **Visningsrekkefølge** vises over meldinger som har en høyere verdi. Meldinger som har **1** som verdi i **Visningsrekkefølge** vises øverst.

    Meldinger vises bare for operasjoner som er lagt til i hurtigfanen **Meldinger**, og der kan du bare legge til operasjoner det er merket av for **Aktiver varslinger** for disse operasjonene på siden **Salgsstedsoperasjoner**. I tillegg vises meldinger for en operasjon til arbeidere bare hvis operasjonen er lagt til POS-tillatelsene for disse arbeiderne.

    > [!NOTE]
    > Meldinger kan overstyres på brukernivå. Åpne arbeiderens post, velg **Salgsstedstillatelser**, og rediger deretter brukerens varslingsabonnement.

4. Gå til **Handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Funksjonalitetsprofiler**. I feltet **Varslingsintervall**, angir du hvor ofte meldinger skal trekkes. For noen meldinger, må salgsstedet foreta sanntidsanrop til back office-programmet. Disse anropene bruker datakapasiteten til back office-programmet. Når du angir varslingsintervallet, bør du derfor vurdere både dine forretningskrav og virkningen av sanntidsanrop til back office-programmet. Verdien **0** (null) slår av alle varslinger.
5. Gå til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**. Velg planeb **1060** (**Stab**) for å synkronisere varslingsinnstillingene, og velg deretter **Kjør nå**. Velg **1070** (**Kanalkonfigurasjon**) for å synkronisere tillatelsesintervallet, og så **Kjør nå**.

## <a name="view-notifications-in-the-pos"></a>Vise varslinger på salgsstedet

Når du har fullført trinnene ovenfor, kan arbeiderne se meldingene på salgsstedet. Du kan vise varslingene ved å trykke på varslingsikonet i øvre høyre hjørne av salgsstedet. Et varslingssenter vises med meldingene for ordeoppfyllelsesoperasjonen. Varslingssenteret skal vise følgende grupper i ordreoppfyllelsesoperasjonen:

- **Henting i butikk** – Denne gruppen viser hvor mange ordrer som har leveringsmodusen **Henting**, og at hentingen er planlagt fra gjeldende butikk. Du kan trykke nummeret til gruppen for å åpne siden **Ordreoppfyllelse**. I dette tilfellet, filtreres siden slik at den bare viser de aktive bestillingene som er definert for henting fra gjeldende butikk.
- **Send fra butikk** – Denne gruppen viser hvor mange ordrer som har leveringsmodusen **Forsendelse**, og at forsendelsen er planlagt fra gjeldende butikk. Du kan trykke nummeret til gruppen for å åpne siden **Ordreoppfyllelse**. I dette tilfellet, filtreres siden slik at den bare viser de aktive bestillingene som er definert for forsendelse fra gjeldende butikk.

Når nye ordrer tilordnes til butikken for oppfyllelse, endres varslingsikonet for å angi at det finnes nye meldinger, og antallet for de tilsvarende gruppene blir oppdatert. Men selv om gruppene oppdateres med jevne mellomrom, kan selgsstedbrukere når som helst oppdatere gruppene manuelt ved å velge knappen **Oppdater** ved siden av gruppen. Til slutt, hvis en gruppe har en ny vare, som den gjeldende arbeideren ikke har sett, viser gruppen et ikon som angir at denne gruppen har en ny vare.

## <a name="enable-live-content-on-pos-buttons"></a>Aktiver aktivt innhold på salgsstedsknapper

Salgsstedsknappene kan nå vise et tall som kan hjelpe arbeiderne med å finne ut hvilke oppgaver som krever umiddelbar oppmerksomhet. Hvis du vil vise dette tallet på en salgsstedsknapp, må du fullføre oppsettet for meldinger som er beskrevet tidligere i dette emnet (det vil si du må aktivere meldinger for en operasjon, definere et intervall for varsling og oppdatere gruppen for salgsstedstillatelse for arbeideren). I tillegg du må åpne rutenettet for knappen, se på egenskapene til knappen, og merke av for **Aktiver aktivt innhold**. I feltet **Innholdjustering** kan du velge om tellingen vises i øvre høyre hjørne av knappen (**Øverst til høyre**) eller i midten (**Midtstill**).

> [!NOTE]
> Det aktive innholdet kan bare aktiveres for operasjoner hvis avmerkingsboksen **Aktiver varslinger** er valgt for på siden **Salgsstedoperasjoner**, som beskrevet tidligere i dette emnet.

Illustrasjonen nedenfor viser innstillingene for aktivt innhold i rutenettet for knappen.

![Innstillinger for aktivt innhold i rutenettet for knappen](./media/ButtonGridDesigner.png "Innstillinger for aktivt innhold i rutenettet for knappen")

Illustrasjonen nedenfor viser resultatet av å velge **Øverst til høyre** og **Midtstill** i feltet **Innholdsjustering** for knapper i ulike størrelser.

![Aktivt innhold på salgsstedsknapper](./media/ButtonsWithLiveContent.png "Aktivt innhold på salgsstedsknapper")
