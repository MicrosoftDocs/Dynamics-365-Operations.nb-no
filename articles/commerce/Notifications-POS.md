---
title: Vise ordrevarslinger på salgsstedet (POS)
description: Dette emnet beskriver hvordan du aktiverer ordrevarslinger på salgsstedet og varselrammeverket.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7166afdb43c7e835170c5768a0767f2943222b19c00c7d0aaf067263845651f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714144"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Vise ordrevarslinger på salgsstedet (POS)

[!include [banner](includes/banner.md)]

Butikkmedarbeidere kan tilordnes ulike oppgaver i butikken, for eksempel fullføre ordrer eller utføre lagermottak eller lagertellinger. Salgsstedsklienten (POS) er ett enkelt program som gjør det mulig for ansatte å bli varslet disse om oppgavene. Varslingsrammeverket i POS hjelper med dette ved at forhandlerne kan konfigurere rollebaserte meldinger. Disse meldingene bare konfigureres for salgsstedsoperasjoner som starter i Dynamics 365 Retail med programoppdatering 5.

Systemet kan vise meldinger for operasjonen for *orderoppfyllelse*, og fra og med Commerce-versjon 10.0.18 kan varslinger også vises for operasjonen *tilbakekallingsordren*. Men fordi rammeverket er utformet for å være utvidbar, kan utviklerne til slutt kunne [skrive en varslingsbehandler](dev-itpro/extend-pos-notification.md) for alle typer operasjoner, og vise meldingene for operasjonen på salgsstedet.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Aktivere varslinger for ordreoppfyllelse eller tilbakekalle ordreoperasjoner

Hvis du vil aktivere varslinger for operasjonen for ordreoppfyllelse eller tilbakekalling av ordre, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Operasjoner**.
1. Søk etter operasjonen **Ordreoppfyllelse** eller operasjonen **Tilbakekalling av ordre**, og deretter velger du **Aktiver varslinger** for operasjonen for å angi at varslingsrammeverket bør lytte til den som styrer denne operasjonen. Hvis handleren er implementert, vises deretter meldinger for denne operasjonen på salgsstedet.
1. Gå til **Detaljhandel og handel \> Ansatte \> Arbeidere**.
1. Velg fanen **Commerce**, velg en arbeiderrad, og velg deretter **POS-tillatelser**. Velg hurtigfanen **Varslinger** for å utvide den, og legg deretter til operasjonene du har aktivert varslinger for. Hvis du konfigurerer én varsling for en arbeider, må du kontrollere at verdien **Visningsrekkefølge** er satt til **1**. Hvis du konfigurerer mer enn én operasjon, angir du verdiene for **Visningsrekkefølge** for å angi i hvilken rekkefølge varslingene skal vises. 

      Varslinger vises bare for operasjoner som blir lagt til i hurtigfanen **Varslinger**. Du kan legge til operasjoner bare hvis det er merket av for **Aktiver varslinger** for de operasjonene som har blitt valgt på siden **POS-operasjoner**. I tillegg vises meldinger for en operasjon bare til arbeidere hvis operasjonen er lagt til POS-tillatelsene for disse arbeiderne.

    > [!NOTE]
    > Meldinger kan overstyres på brukernivå. Hvis du vil gjøre dette, åpner du arbeiderens post, velger **Salgsstedstillatelser**, og redigerer deretter brukerens varslingsabonnement.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**. I feltet **Varslingsintervall**, angir du hvor ofte meldinger skal trekkes. For noen meldinger, må salgsstedet foreta sanntidsanrop til back office-programmet. Disse anropene bruker datakapasiteten til back office-programmet. Når du angir varslingsintervallet, bør du derfor vurdere både dine forretningskrav og virkningen av sanntidsanrop til back office-programmet. Verdien **0** (null) slår av alle varslinger.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**. Velg planeb **1060** (**Stab**) for å synkronisere varslingsinnstillingene, og velg deretter **Kjør nå**. Velg **1070** (**Kanalkonfigurasjon**) for å synkronisere tillatelsesintervallet, og så **Kjør nå**.

## <a name="view-notifications-in-the-pos"></a>Vise varslinger på salgsstedet

Når du har fullført trinnene ovenfor, kan arbeiderne se meldingene på salgsstedet. Du kan vise varslingene ved å velge varslingsikonet i hjørnet øverst til høyre på salgsstedet. Et varslingspanel vises, og viser meldinger for operasjonene som er konfigurert for arbeideren. 

For operasjonen **ordreoppfyllelse** vil varslingspanelet vise følgende grupper:

- **Henting i butikk** – Denne gruppen viser hvor mange enkeltstående ordrelinjer som er planlagt for henting fra den gjeldende butikken. Du kan velge nummeret på gruppen for å åpne operasjonen **Ordreoppfyllelse** med et filter, slik at det bare viser de aktive ordrelinjene som er definert for henting fra den gjeldende butikken.
- **Forsendelse fra butikk** – Denne gruppen viser antallet individuelle ordrelinjer som er konfigurert til å sendes fra brukerens gjeldende butikk. Du kan velge nummeret på gruppen for å åpne operasjonen **Ordreoppfyllelse** med en filtrert visning som bare viser de aktive ordrelinjene som er definert for forsendelse fra den gjeldende butikken.

For operasjonen **tilbakekalling av ordre** vil varslingspanelet vise følgende grupper:

- **Ordrer som skal oppfylles** – Denne gruppen viser antallet ordrer som er konfigurert enten for henting eller innfrielse av forsendelse for brukerens gjeldende butikk. Du kan velge nummeret på gruppen for å åpne operasjonen **Tilbakekall ordre** med en filtrert visning som bare viser de åpne ordrene som må oppfylles av brukerens gjeldende butikk, enten for plukking i butikk eller forsendelse fra butikkscenarioer.
- **Ordrer som skal hentes** – Denne gruppen viser hvor mange ordrer som er planlagt for henting fra den gjeldende butikken. Du kan velge nummeret på gruppen for å åpne operasjonen **Tilbakekall ordre** med en filtrert visning som bare viser de åpne ordrene som må oppfylles for kundehenting fra brukerens gjeldende butikk.
- **Ordrer som skal sendes** – Denne gruppen viser antall ordrer som skal sendes fra brukerens gjeldende butikk. Du kan velge nummeret på gruppen for å åpne operasjonen **Tilbakekall ordre** med en filtrert visning som bare viser de åpne ordrene som må oppfylles for forsendelse fra brukerens gjeldende butikk.

For både varslinger av typen ordreoppfyllelse og tilbakekalling av ordre endres varslingsikonet for å angi at det finnes nye varslinger, og antallet for de tilsvarende gruppene blir oppdatert ettersom nye ordrer hentes av prosessen. Men selv om gruppene oppdateres med jevne mellomrom, kan salgsstedbrukere når som helst oppdatere gruppene manuelt ved å velge **Oppdater** ved siden av gruppen. Til slutt, hvis en gruppe har en ny vare, som den gjeldende arbeideren ikke har sett, viser gruppen et ikon som angir at denne gruppen har en ny vare.

## <a name="enable-live-content-on-pos-buttons"></a>Aktiver aktivt innhold på salgsstedsknapper

Salgsstedsknappene kan nå vise et tall som kan hjelpe arbeiderne med å finne ut hvilke oppgaver som krever umiddelbar oppmerksomhet. Hvis du vil vise dette tallet på en salgsstedsknapp, må du fullføre oppsettet for meldinger som er beskrevet tidligere i dette emnet (det vil si du må aktivere meldinger for en operasjon, definere et intervall for varsling og oppdatere gruppen for salgsstedstillatelse for arbeideren). I tillegg du må åpne rutenettet for knappen, se på egenskapene til knappen, og merke av for **Aktiver aktivt innhold**. I feltet **Innholdjustering** kan du velge om tellingen vises i øvre høyre hjørne av knappen (**Øverst til høyre**) eller i midten (**Midtstill**).

> [!NOTE]
> Det aktive innholdet kan bare aktiveres for operasjoner hvis avmerkingsboksen **Aktiver varslinger** er valgt for på siden **Salgsstedoperasjoner**, som beskrevet tidligere i dette emnet.

Illustrasjonen nedenfor viser innstillingene for aktivt innhold i rutenettet for knappen.

![Innstillinger for aktivt innhold i utforming for knappegruppe.](./media/ButtonGridDesigner.png "Innstillinger for aktivt innhold i utforming for knappegruppe")

Hvis du vil vise varslingsantallet på en knapp, må du kontrollere at riktig skjermoppsett oppdateres. Hvis du vil bestemme skjermoppsettet som brukes av POS, velger du **Innstillinger**-ikonet øverst til høyre, og noterer **Skjermoppsett-ID** og **Oppsettsoppløsning**. Med Edge-leseren går du nå til **Skjermoppsett**-siden i , finner **Skjermoppsett-ID** og **Oppsettsoppløsning** som ble identifisert ovenfor, og merker av for **Aktiver direkte innhold**. Gå til **Retail og Commerce \> IT for Retail og Commerce \> Distribusjonsplan** og kjør 1090 (registre)-jobben for å synkronisere oppsettsendringer.

![Finne skjermoppsettet som brukes av salgsstedet.](./media/Choose_screen_layout.png "Finne skjermoppsettet")

Illustrasjonen nedenfor viser resultatet av å velge **Øverst til høyre** og **Midtstill** i feltet **Innholdsjustering** for knapper i ulike størrelser.

![Aktivt innhold på salgsstedsknapper.](./media/ButtonsWithLiveContent.png "Aktivt innhold på salgsstedsknapper")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
