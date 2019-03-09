---
title: Reiseregninger og flere godkjennere
description: Dette emnet gir informasjon om reiseregninger som må godkjennes av flere personer.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "362424"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="783e1-103">Reiseregninger og flere godkjennere</span><span class="sxs-lookup"><span data-stu-id="783e1-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="783e1-104">Avhengig av organisasjonens policyer for godkjenning av reiseregninger, kan det være at flere personer må godkjenne en utgiftsrapport som sendes av en ansatt.</span><span class="sxs-lookup"><span data-stu-id="783e1-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="783e1-105">Når du definerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for en eller flere godkjennere av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="783e1-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="783e1-106">Du kan for eksempel kreve at alle reiseregninger skal godkjennes først av lederen for den ansatte som sendte regningen og deretter av en leverandørkoordinator.</span><span class="sxs-lookup"><span data-stu-id="783e1-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="783e1-107">Hvis du vil kreve flere godkjennere for reiseregninger, kan du legge til arbeidsflytelementene på en av følgende måter:</span><span class="sxs-lookup"><span data-stu-id="783e1-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="783e1-108">Legge til ett godkjenningselement som har ett trinn.</span><span class="sxs-lookup"><span data-stu-id="783e1-108">Add one approval element that has one step.</span></span> <span data-ttu-id="783e1-109">Trinnet kan for eksempel kreve at en reiseregning tilordnes til en brukergruppe, og at det skal godkjennes av 50 prosent av brukergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="783e1-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="783e1-110">Legge til ett godkjenningselement som har flere trinn.</span><span class="sxs-lookup"><span data-stu-id="783e1-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="783e1-111">Godkjenningselementet kan for eksempel inneholde følgende:</span><span class="sxs-lookup"><span data-stu-id="783e1-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="783e1-112">Lederen til den ansatte som sendte inn reiseregningen godkjenner regningen.</span><span class="sxs-lookup"><span data-stu-id="783e1-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="783e1-113">Regnskapsassistenten kontrollerer kvitteringene og varene som står på reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="783e1-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="783e1-114">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="783e1-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="783e1-115">Legge til flere godkjenningselementer, der hvert element har ett trinn.</span><span class="sxs-lookup"><span data-stu-id="783e1-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="783e1-116">Du kan for eksempel legge til et eget godkjenningselement for hvert av følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="783e1-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="783e1-117">Lederen til den ansatte godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="783e1-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="783e1-118">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="783e1-118">The budget owner approves the expense report.</span></span>
