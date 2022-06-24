---
title: Konfigurere parametere for automatisering av innkrevingsprosess
description: Denne artikkelen beskriver parameterne som påvirker automatiserte innkrevingsprosesser, og gir retningslinjer for hvordan du definerer dem, slik at den automatiserte prosessen gjenspeiler dine hensikter og forventninger.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c5d0f801c47ef2d98d8ba410dc593bd7640839c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900049"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Konfigurere parametere for automatisering av innkrevingsprosess

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver parameterne som påvirker automatiserte innkrevingsprosesser, og gir retningslinjer for hvordan du definerer dem, slik at den automatiserte prosessen gjenspeiler dine hensikter og forventninger. Hvis du vil ha informasjon om hvordan du automatiserer innkrevingsprosesser, kan du se [Automatisering av innkrevingsprosess](collections-process-automate.md).

## <a name="general"></a>Generelt
Angi et nummer i **Prosent av kunder per satsvis oppgave** for å bestemme antallet satsvise oppgaver per automatisk prosess. Sett **Poster purringer automatisk** til **Ja**, slik at purrehandlingstypen posterer brevet under automatisering. Sett **Opprett aktiviteter for automatisering** til **Ja** for å opprette og lukke aktiviteter for handlingstyper som ikke er aktiviteter, for å vise alle automatiserte trinn som er utført på en konto. Definer antall dager innkrevingshistorikk skal lagres i **Dager for å beholde automatisering av innkrevingsprosesser**. Når en faktura kommer til det siste trinnet i innkrevingsprosessen, brukes den ikke til å opprette fremtidige handlingstyper for **Utelat faktura etter aktivering av siste prosesstrinn** er satt til **Ja**. Den nest eldste fakturaen bestemmer neste trinn for automatisk prosess for å sikre at handlingene for innkreving av automatisk behandling fortsetter. 

## <a name="payment-predictions"></a>Betalingsforutsigelser
Fra og med versjon 10.0.21 vil Kundebetalingsforutsigelser, som finnes Finance Insights, projisere om en faktura vil bli betalt til rett tid, for sent eller svært sent. Du kan konfigurere hver av disse kategoriene i Finance Insights. Hvis fakturaer prognostiseres til å betales for sent, er det viktig å starte innkrevingsprosessen før fakturaen forfaller. Disse prognosene kan brukes til å opprette innkrevingsaktiviteter når Automatisering av innkrevingsprosess kjøres. Sett **Aktiver kundebetalingsprognoser** til **Ja** for å bruke kundebetalingsforutsigelser til å opprette innkrevingsaktiviteter basert på sannsynligheten for at fakturaen vil bli betalt for sent. 

Hvis du vil ha mer informasjon om kundebetalingsforutsigelser og Finance Insights, kan du se [Kundebetalingsforutsigelser](payment-insights-overview.md).

Når modellen for kundebetalingsforutsigelser kjøres, tilordner den en prosent til forutsigelsen av fakturaen som betales til rett tid, for sent eller svært sent. Du kan bruke informasjonen til å starte innkrevingsaktiviteter automatisk ved hjelp av automatisering av innkrevingsprosess i tilfelle der sen betaling er forventet. Du kan vise disse prosentene på sidene **Betalingspredisjoner per kunde** eller **Betalingsprediksjoner per transaksjon** under **Kreditt og innkrevinger > Innkrevinger**. 

Hvis den gjennomsnittlige betalingsforutsigelsen for en kundefaktura er mindre enn benchmarkprosenten, opprettes det ingen aktivitet. Hvis fakturaprediksjonen er større enn eller lik benchmarkprosenten, opprettes én aktivitet per kunde. For **Forutsigelse: For sen**, angir du **benchmarkprosent** for når automatisering av innkrevingsprosesser skal opprette innkrevingsaktiviteter. Dette er en samleverdi av både for sent og svært sent. Velg en **Forretningsdokumentmal** som skal brukes for aktiviteten som ble opprettet, eller opprett en ny. Dette identifiserer **Type**, **Formål** og **Dager til aktiviteten lukkes**. Angi eventuelle **Merknader** som brukes som standard som beskrivelse når aktiviteten opprettes. For **Forutsigelse: Svært sen**, angir du **benchmarkprosent** for når automatisering av innkrevingsprosesser skal opprette innkrevingsaktiviteter for en kunde som sannsynligvis vil betale fakturaer svært sent. Velg en **Forretningsdokumentmal** som skal brukes for aktiviteten som ble opprettet. Dette identifiserer **Type**, **Formål** og **Dager til aktiviteten lukkes**. Angi eventuelle **Merknader** som brukes som standard som beskrivelse når aktiviteten opprettes. 

### <a name="example"></a>Eksempel
Hvis den sene benchmarkprosenten er satt til 60 %. Når kundebetalingsforutsigelser kjøres for hver faktura, tilordner systemet en prosentforutsigelsen betales til rett tid, for sent eller svært sent. Hvis betalingsforutsigelsen om at fakturaen vil bli betalt sent, er 59 % eller mindre, opprettes det ingen innkrevingsaktivitet for fakturaen av den automatiserte innkrevingsprosessen. Hvis kundebetalingsprediksjonen for en faktura er større enn eller lik 60 %, opprettes en innkrevingsaktivitet under automatisering av innkrevingsprosessen. 

> [!NOTE]
> Svært sen-forutsigelsen evalueres før sen-forutsigelsen, fordi svært sen omfatter fakturaer som sannsynligvis blir betalt for sent. Innkrevingsprosessen genererer bare én aktivitet hvis fakturaen både faller inn i for sen- og svært sen-benchmark. I så fall bruker systemet svært sen-aktiviteten og forretningsdokumentet, fordi svært sen prioriteres høyere. Andre handlinger som allerede er generert, blir ikke generert en gang til.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
