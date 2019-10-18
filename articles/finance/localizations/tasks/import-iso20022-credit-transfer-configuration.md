---
title: Importere konfigurasjon for ISO20022-kredittoverføring
description: Denne fremgangsmåten viser hvordan du importerer en konfigurasjon for elektronisk rapportering for leverandørbetalinger.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174986"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="d6a2f-103">Importere konfigurasjon for ISO20022-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="d6a2f-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6a2f-104">Denne fremgangsmåten viser hvordan du importerer en konfigurasjon for elektronisk rapportering for leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="d6a2f-105">Det tysk kredittoverføringsformatet ISO 20022 brukes som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="d6a2f-106">Denne prosedyren kan brukes for andre tilgjengelige elektroniske rapporteringsformat.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="d6a2f-107">Denne oppgaven ble opprettet ved hjelp av demonstrasjonsdatafirmaet DEMF, men du kan bruke et hvilket som helst demonstrasjonsdatafirma til å fullføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="d6a2f-108">Dette er den første av fem oppgaver, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d6a2f-109">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d6a2f-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d6a2f-111">I listen over tilgjengelige konfigurasjonsleverandører velger du Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="d6a2f-112">Klikk Angi som aktiv</span><span class="sxs-lookup"><span data-stu-id="d6a2f-112">Click Set active.</span></span>
4. <span data-ttu-id="d6a2f-113">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-113">Click Repositories.</span></span>
5. <span data-ttu-id="d6a2f-114">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-114">Click Open.</span></span>
6. <span data-ttu-id="d6a2f-115">Klikk Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-115">Click Show filters.</span></span>
7. <span data-ttu-id="d6a2f-116">Bruk følgende filtre: Angi filterverdien "ISO20022-kredittoverføring (DE)" i feltet Konfigurasjonsnavn ved hjelp av filteroperatoren "begynner med".</span><span class="sxs-lookup"><span data-stu-id="d6a2f-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="d6a2f-117">Du kan også finne konfigurasjonen i listen, velge den og deretter flytte den til importoppgaven.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="d6a2f-118">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-118">Click Import.</span></span>
    * <span data-ttu-id="d6a2f-119">Hvis Importer-knappen ikke er tilgjengelig, betyr det at konfigurasjonen allerede er importert.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="d6a2f-120">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-120">Click Yes.</span></span>

