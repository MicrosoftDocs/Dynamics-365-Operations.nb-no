---
title: "Vise ordrevarslinger på salgsstedet"
description: "Dette emnet beskriver hvordan du aktiverer ordrevarslinger på salgsstedet og varselrammeverket, som kan utvides til andre operasjoner."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Vise varslinger på salgsstedet

I dagens moderne detaljhandelsmiljø har butikkansatte forskjellige oppgaver, for eksempel hjelpe kunder, slå inn transaksjoner, utføre lagertelling og motta ordrer i butikken. Salgsstedsklienten (POS) gjør det mulig for ansatte å utføre disse oppgavene og mye mer, alt i ett enkelt program. Med forskjellige oppgaver som skal utføres i løpet av dagen, kan ansatte trenge å bli varslet når noe krever deres oppmerksomhet. Varslingsrammeverket i POS løser dette problemet ved at forhandlerne kan konfigurere rollebaserte meldinger. Disse meldingene kan bare konfigureres for POS-operasjoner med Dynamics 365 for Retail med programoppdatering 5.

Systemet gir nå muligheten til å vise varslinger for ordreoppfyllelsesoperasjonen, men rammeverket er utformet slik at det kan utvides. Utviklere vil dermed i fremtiden kunne skrive en varslingsbehandler for enhver operasjon og vise meldingene i POS.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Aktivere varslinger for ordreoppfyllelsesoperasjoner

Hvis du vil aktivere varslinger for ordreoppfyllelsesoperasjonene, se følgende fremgangsmåte:

 - Gå til **Operasjoner**-siden (**Handel** > **Kanaloppsett** > **Salgsstedsoppsett** > **Salgssted** > **Operasjoner**).
 - Søk etter ordreoppfyllelsesoperasjonen og merk av for **Aktiver varslinger** for denne operasjonen. Dette angir at varslingsrammeverket skal lytte til behandleren for ordreoppfyllelsesoperasjonen. Hvis behandleren er implementert, vises meldingene på salgssted, ellers vises ikke varslingene for denne operasjonen.
- Gå til POS-tillatelsene som er tilknyttet de ansatte, og under **Varslinger**-hurtigkategorien legger du til ordreoppfyllelsesoperasjonen med 1 som "Visningsrekkefølge". Når det er konfigurert mer enn én melding, brukes visningsrekkefølgen til å ordne meldingen fra topp til bunn med 1 øverst. Bare de operasjonene kan legges til som **Aktiver varslinger** er merket av for. Dessuten vises meldingene bare for operasjonene som er lagt til her, og bare for de ansatte som operasjonene er lagt til de tilsvarende salgsstedstillatelsene for. 

> [!NOTE]
> Varslinger kan overstyres på brukernivået ved å navigere til arbeiderens post og velge **Salgsstedstillatelser** og deretter redigere denne brukerens varslingsabonnement.

 - Gå til **Funksjonalitetsprofil**-siden (**Detaljhandel** > **Kanaloppsett** > **Salgsstedsoppsett** > **Salgsstedsprofiler** > **Funksjonalitetsprofiler**). Oppdater **varslingsintervall**-egenskapen for å angi intervallet som meldingene skal utføres med i minutter. Vi anbefaler at du setter denne verdien til 10 minutter for å unngå unødvendig kommunikasjon til hovedkontoret. Hvis du setter varslingsintervallet til 0, deaktiveres varslene.  

 - Gå til **Detaljhandel** > **IT for detaljhandel** > **Distribusjonsplan**. Velg plan "1060, stab" for å synkronisere varslingsinnstillingene, og klikk deretter **Kjør nå**. Deretter synkroniserer du tillatelsesintervallet ved å velge "1070-kanalkonfigurasjon" og klikker deretter **Kjør nå**. 

## <a name="view-notifications-in-pos"></a>Vise varslinger på salgssted

Når trinnene ovenfor er fullført, kan de ansatte, som varslingene er satt opp for, se meldingene i POS. Du kan vise varslingene ved å klikke på varslingsikonet i meldingslinjen for salgsstedet. Dette viser et varslingssenter med meldingene for ordeoppfyllelsesoperasjonen. Varslingssenteret skal vise følgende grupper i ordreoppfyllelsesoperasjonen: 

- **Ventende ordrer** – Denne gruppen viser antall ordrer i ventende tilstand, for eksempel ordrer som skal godkjennes av en salgsstedsarbeider som har de nødvendige tillatelsene for butikkfullføring. Ved å klikke på tallet på gruppen åpnes **Ordreoppfyllelse**-siden, filtrert for å vise bare ventende ordrer som er tilordnet til butikken for oppfyllelse. Hvis ordrene godkjennes automatisk for butikken, vil antallet for denne gruppen være null.

- **Henting i butikk** – Denne gruppen viser hvor mange ordrer som har leveringsmodusen **Henting**, og hentingen er planlagt fra gjeldende butikk. Ved å klikke på tallet på gruppen åpnes **Ordreoppfyllelse**-siden, filtrert for å vise aktive ordrer som er satt opp for å hentes fra gjeldende butikk.

- **Send fra butikk** – Denne gruppen viser hvor mange ordrer som har leveringsmodusen **Forsendelse**, og forsendelsen er planlagt fra gjeldende butikk. Ved å klikke på tallet på gruppen åpnes **Ordreoppfyllelse**-siden, filtrert for å vise aktive ordrer som er satt opp for å leveres fra gjeldende butikk.

Når det er nye ordrer som er tilordnet til butikken for oppfyllelse, endres varslingsikonet for å angi de nye meldingene og antallet tilsvarende grupper blir oppdatert. Brukeren kan også klikke oppdateringsikonet ved siden av operasjonsnavnet, og oppdatere antallet grupper umiddelbart. Antallet oppdateres også med det forhåndsdefinerte intervallet. En gruppe med et nytt element, som ikke er synlig for den gjeldende arbeideren, viser et ikon som angir at denne gruppen har en ny element. Ved å klikke på flisene i varslingene åpnes den bestemte operasjonen som dette varselet er konfigurert for. I scenariene ovenfor vil klikking på varslene åpne **Ordreoppfyllelse**-siden og sende de aktuelle parameterne: ventende ordrer, henting i butikk og send fra butikk. 

> [!NOTE]
> Varslinger for ventende order blir aktivert i en kommende oppdatering til Dynamics 365 for Retail. 


