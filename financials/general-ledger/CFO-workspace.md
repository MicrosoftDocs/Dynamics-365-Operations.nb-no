---
title: "Legge til finansdimensjoner i CFO-arbeidsområdet"
description: "Dette emnet forklarer hvordan du legger til finansdimensjoner i CFO-arbeidsområdet, slik at de kan brukes for økonomi- og budsjettrapportene."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: nb-no
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Legge til finansdimensjoner i CFO-arbeidsområdet

[!include[banner](../includes/banner.md)]

Dette emnet forklarer hvordan du legger til finansdimensjoner i CFO-arbeidsområdet, slik at de kan brukes for økonomi- og budsjettrapportene. CFO-arbeidsområdet har en **Oversikt**-kategori og en **Økonomisk**-kategori. Rapportene i disse to kategoriene følges opp av to mål: LedgerActivityMeasure og BudgetActivityMeasure. I Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, oppdatering fra juli 2017, er det en relasjon mellom disse to målene og DimensionCombinationEntity-enheten. Derfor kan du velge dimensjoner.

1. I Finance and Operations, på **Enhetsbutikk**-siden, oppdaterer du målene **LedgerActivityMeasure** og **BudgetActivityMeasure**.
2. Åpne Programutforsker i Microsoft Visual Studio, og søk etter **LedgerCFO**.
3. Under **Ressurser** åpner du **LedgerCFOWorkspacePBIX**.
4. Når ressursen åpnes i Microsoft Power BI-skrivebordet, velger du **Hent data**, velger **SQL Server-database**, og velger deretter **Koble til**.
5. Angi servernavnet, og angi deretter **AxDW** som databasen. Velg **DirectQuery**, og velg deretter **OK**.
6. Søk etter og velg **LedgerActivityMeasure\_DimensionCombination**, og velg deretter **Last inn**.

    > [!TIP]
    > I **Felt**-listen gir du nytt navn til tabellen **Finansdimensjoner**, slik at den er enkel å identifisere.

7. Velg **Behandle relasjoner**, og velg deretter **Ny**.
8. I det første feltet velger du **Aktiviteter i øknomimodulen**, og deretter velger du **LedgerDimension**.
9. I det andre feltet velger du **LedgerActivityMeasure\_DimensionCombination** (eller **Finansdimensjoner** hvis du endret navnet på tabellen). Velg **DimensionCombinationRECID**-hodet.
10. I **Kardinalitet**-feltet velger du **Mange til en**.
11. Endre verdien **Kryssfiltreringsretning** til **Enkelt**.
12. Merk av for både **Gjør denne relasjonen aktiv** og **Anta referanseintegritet**, velg **OK**, og velg deretter **Lukk**.

    [![Opprette en relasjon](./media/Create-relationship.png)](./media/Create-relationship.png)

13. I **Felt**-listen skal du se tabellen og de tilgjengelige finansdimensjonene. Dra finansdimensjonene som du vil bruke, til rapportnivåfiltrene.
14. Lagre endringene.
15. I applikasjonsobjekttreet høyreklikker du prosjektet, og velger deretter **Synkroniser**.
16. Bygge prosjektet, og åpne deretter programmet for å vise resultatene.

    [![Fullført arbeidsområde](./media/workspace.png)](./media/workspace.png)

