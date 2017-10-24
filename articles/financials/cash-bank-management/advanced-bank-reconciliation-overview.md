---
title: Oversikt over avansert bankavstemming
description: Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen. Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33150777222faa97af7488c59ab13cb0fb9e8e2c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="17f07-104">Oversikt over avansert bankavstemming</span><span class="sxs-lookup"><span data-stu-id="17f07-104">Advanced bank reconciliation overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="17f07-105">Denne artikkelen beskriver flyten for den avanserte bankavstemmingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="17f07-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="17f07-106">Funksjonen for den avanserte bankavstemmingen lar deg importere bankkontoutdrag som kan avstemmes automatisk fra banktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="17f07-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="17f07-107">Funksjonen for avanserte bankavstemming lar deg importere bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="17f07-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="17f07-108">Det importerte bankkontoutdraget kan deretter avstemmes automatisk fra banktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="17f07-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="17f07-109">Her er noen av trinnene i flyten for den avanserte bankavstemmingen.</span><span class="sxs-lookup"><span data-stu-id="17f07-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="17f07-110">Definer import for bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="17f07-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="17f07-111">Importer bankkontoutdrag gjennom rammeverket for dataenhet.</span><span class="sxs-lookup"><span data-stu-id="17f07-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="17f07-112">Tre vanlige bankkontoutdragsformater er innebygd: ISO20022, BAI2 og MT940.</span><span class="sxs-lookup"><span data-stu-id="17f07-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="17f07-113">Funksjonen kan utvides til et hvilken som helst format.</span><span class="sxs-lookup"><span data-stu-id="17f07-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="17f07-114">Definer en nummerserie som skal brukes for avansert bankavstemming, og definer samsvarsregler for bankavstemmingen.</span><span class="sxs-lookup"><span data-stu-id="17f07-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="17f07-115">En samsvarsregel for avstemming er et sett kriterier som brukes til å filtrere bankkontoutdragslinjer og Microsoft Dynamics 365 for Finance and Operations, Enterprise edition-banktransaksjonslinjer under avstemmingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="17f07-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="17f07-116">Avhengig av firmaets praksis, kan du definere én eller flere samsvarsregler for å automatisere og optimalisere avstemmingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="17f07-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="17f07-117">Avstem bankkontoutdrag med banktransaksjoner i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="17f07-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="17f07-118">Utfør automatiske samsvaring og oppretting av avstemmingsjournaler.</span><span class="sxs-lookup"><span data-stu-id="17f07-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="17f07-119">Vis bankkontoutdrag og banktransaksjoner i Finance and Operations ved siden av hverandre.</span><span class="sxs-lookup"><span data-stu-id="17f07-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="17f07-120">Poster banktransaksjoner i Finance and Operations automatisk hvis de vises i et bankkontoutdrag, men ikke vises i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="17f07-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="17f07-121">Generer et avstemmingsutdrag.</span><span class="sxs-lookup"><span data-stu-id="17f07-121">Generate a reconciliation statement.</span></span>






