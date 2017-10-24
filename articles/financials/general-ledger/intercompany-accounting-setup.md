---
title: Oppsett av konserninternt regnskap
description: "Dette emnet forklarer hvordan du setter opp konserninternt regnskap slik at du kan bruke konserninterne kladder for finansfordelinger og finansjournaler, for eksempel daglige journaler, leverandørfakturajournaler og betalingsjournaler."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9c5e73d97f6f52a417cb71dc5bfb57658765aaa1
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="intercompany-accounting-setup"></a>Oppsett av konserninternt regnskap

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du setter opp konserninternt regnskap slik at du kan bruke konserninterne kladder for finansfordelinger og finansjournaler, for eksempel daglige journaler, leverandørfakturajournaler og betalingsjournaler.

Konserninterne journaler kan opprettes i ulike scenarier, for eksempel daglige journaler, leverandørfakturajournaler, finansfordelinger og sentraliserte betalinger. Hvis du vil aktivere disse scenariene, må du definere konserninternt regnskap.

## <a name="define-main-accounts"></a>Definere hovedkontoer
Først må du opprette de konserninterne hovedkontoene som skal brukes til regnskapsoppføringer for betaling til og betaling fra. Det er lurt å bruke unike hovedkontoer for hvert firma for å forenkle avstemmingen og elimineringen av konserninterne regnskapsoppføringer. Hvis du bruker en handelspartner eller motpartsdimensjon til å den konserninterne parten, kan du definere denne dimensjonen som en fast dimensjon i hovedkontoen som er definert i Konserninternt regnskap. Når du definerer hovedkontoene, bør du sette feltet **Hovedkontotype** til **Balanse** på siden **Hovedkontoer**.

## <a name="define-journal-names"></a>Definere journalnavn
Deretter må du definere et journalnavn. Angi feltet **Journaltype** til **Daglig** på siden **Journalnavn**. Det er lurt å bruke et spesifikt journalnavn for konserninternt regnskap.

## <a name="define-intercompany-accounting-setup"></a>Definere oppsett av konserninternt regnskap
Siden **Konserninternt regnskap** brukes til å opprette par med juridiske enheter som kan utføre transaksjoner med hverandre. Oppsettet av konserninternt regnskap er delt, slik at oppsettet er synlig fra alle juridiske enheter. Når du oppretter et nytt par av juridisk enhet, sikrer du at du er klar over hvilken juridisk enhet som er definert som det opprinnelige firmaet kontra målfirmaet. Når du angir konserninterne transaksjoner, bestemmer transaksjonen hvilken juridisk enhet som starter eller er opprinnelsen for transaksjonen. Konserninternt regnskap er for eksempel satt opp for USMF (opprinnelig) og USSI (målet). Hvis en bruker er aktiv i USSI og angir en konsernintern transaksjon med USMF, posterer ikke transaksjonen fordi konserninternt regnskap bare defineres for USMF som avsender. Hvis et av firmaene kan være opprinnelsen for en transaksjon, må du opprette et nytt juridisk enhet-par for det gjensidige oppsettet. 

Velg **Debetkonto (skal betales fra)** og **Kreditkonto (skal betales til)** for både opprinnelig juridisk enhet og mål for juridisk enhet. Definer hvilket **journalnavn** som skal brukes når transaksjonen blir opprettet i målfirmaet. Journalen for det opprinnelige firmaet er allerede kjent fordi den velges av brukeren under oppretting av den konserninterne transaksjonen. 

Til slutt velger du hvilken juridisk enhet som skal motta regnskapet for beløp som støttes, for eksempel kontantrabatt eller realisert fortjeneste/tap for sentraliserte betalinger. 

En motsvarende relasjon kan enkelt defineres på siden **Konserninternt regnskap** ved hjelp av knappen **Opprett motsvarende relasjon** etter at det første paret av juridisk enhet er opprettet. Når det gjensidige paret opprettes, kopieres informasjonen for målfirmaet til det opprinnelige firmaet og vice versa. Journalen som er definert for målfirmaet, beholdes. De fleste organisasjoner bruker samme navnekonvensjonen for journalnavn, slik at journalnavnet er det samme. Hvis journalnavnet er forskjellig, vises en advarsel på feltet for å informere om at journalen ikke finnes, og du kan velge en annen journal.




