---
title: Redigere finansdimensjoner for detaljhandelstransaksjoner
description: Dette emnet beskriver hvordan du redigerer finansdimensjoner for detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010181"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="d27cf-103">Redigere finansdimensjoner for detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d27cf-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d27cf-104">Dette emnet beskriver hvordan du redigerer finansdimensjoner for detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d27cf-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="d27cf-105">Redigere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="d27cf-105">Edit financial dimensions</span></span>

<span data-ttu-id="d27cf-106">Følg denne fremgangsmåten for å redigere finansdimensjoner for detaljhandelstransaksjoner i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d27cf-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d27cf-107">Åpne siden **Konfigurasjon av finansdimensjoner for programintegrering**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="d27cf-108">Velg den aktive posten **Integrering av standarddimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="d27cf-109">I hurtigfanen **Finansdimensjoner** sørger du for at alle dimensjonene du vil redigere i Excel-regnearket, finnes i listen **Valgt**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="d27cf-110">Hvis du vil ha mer informasjon, kan du se [Dataenheter](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="d27cf-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="d27cf-111">Last ned og åpne Excel-filen fra siden **Utdrag**, siden **Detaljhandelstransaksjoner** eller flisen **Transaksjonsvalideringsfeil** i arbeidsområdet **Finans for handelsbutikk**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="d27cf-112">Hvis du vil endre finansdimensjonen for transaksjonen, velger du **Utforming**, og deretter velger du blyantsymbolet ved siden av raden **Transaksjon (kan overvåkes)**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="d27cf-113">Finn og merk av i feltet **FinancialDimensionDisplayValue**, velg en celle i hodedelen av Excel-regnearket, og velg deretter **Legg til etikett**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="d27cf-114">Merk en celle under cellen du merket i det forrige trinnet, velg **Legg til verdi**, og velg deretter **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="d27cf-115">Finansdimensjonene legges til i Excel-regnearket, og de kan deretter redigeres og publiseres.</span><span class="sxs-lookup"><span data-stu-id="d27cf-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="d27cf-116">Hvis du vil endre dimensjonene på transaksjonslinjene, velger du **Salgstransaksjoner (kan overvåkes)**, velger blyantsymbolet, og gjentar deretter trinn 6 og 7.</span><span class="sxs-lookup"><span data-stu-id="d27cf-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="d27cf-117">Hvis du vil endre dimensjonene på betalingslinjene, velger du **Betalingstransaksjoner (kan overvåkes)**, velger blyantsymbolet, og gjentar deretter trinn 6 og 7.</span><span class="sxs-lookup"><span data-stu-id="d27cf-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d27cf-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d27cf-118">Additional resources</span></span>

[<span data-ttu-id="d27cf-119">Redigere og overvåke hentesalgs- og kassastyringstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d27cf-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="d27cf-120">Rediger og overvåk nettordretransaksjoner og asynkrone kundeordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d27cf-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="d27cf-121">Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d27cf-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="d27cf-122">Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="d27cf-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
