---
title: Konfigurere TDS-registreringsnumre for juridiske enheter
description: Dette emnet forklarer hvordan du konfigurerer TDS-registreringsnumre (Tax Deducted at Source) for juridiske enheter.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023475"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="39311-103">Konfigurere TDS-registreringsnumre for juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="39311-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39311-104">Dette emnet forklarer hvordan du konfigurerer TDS-registreringsnumre (Tax Deducted at Source) for juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="39311-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="39311-105">Gå til **Organisasjonsstyring \> Organisasjoner \> Juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="39311-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="39311-106">[![Siden Juridiske enheter](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="39311-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="39311-107">Angi det permanente kontonummeret (PAN) for den juridiske enheten i feltet **Permanent kontonummer** i hurtigfanen **Avgiftsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="39311-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="39311-108">I feltet **Circle-nummer** angir du circle-nummeret til TDS-myndighetene.</span><span class="sxs-lookup"><span data-stu-id="39311-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="39311-109">I feltet **Ward-nummer** angir du ward-nummeret til TDS-myndighetene.</span><span class="sxs-lookup"><span data-stu-id="39311-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="39311-110">I **Saksbehandler**-feltet angir du detaljene for saksbehandleren for TDS-myndighetene.</span><span class="sxs-lookup"><span data-stu-id="39311-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="39311-111">I feltet **Fradragstype** velger du kategorien for fradragstype for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="39311-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="39311-112">Velg **Registrerings-ID-er** i handlingsruten for å åpne siden **Administrer adresser**.</span><span class="sxs-lookup"><span data-stu-id="39311-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="39311-113">Velg **Legg til** eller **Rediger** i hurtigfanen **Avgiftsinformasjon** for å åpne siden **Administrer avgiftsinformasjon**, der du kan vedlikeholde oppføringen for avgiftsregistrering.</span><span class="sxs-lookup"><span data-stu-id="39311-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="39311-114">[![Siden Administrer adresser](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="39311-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="39311-115">Angi registreringsnummeret i feltet **TAN-nummer (Tax Account Number)** i hurtigfanen **Kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="39311-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="39311-116">Dette nummeret må bestå av fire alfabetiske bokstaver, deretter fem numeriske tegn og deretter én alfabetisk bokstav.</span><span class="sxs-lookup"><span data-stu-id="39311-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="39311-117">Her er et eksempel: **AXDF87645F**.</span><span class="sxs-lookup"><span data-stu-id="39311-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="39311-118">I feltet **Navn eller beskrivelse** skriver du inn en beskrivelse av registreringsnummeret for kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="39311-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="39311-119">[![Siden Administrer avgiftsinformasjon](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="39311-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="39311-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39311-120">Close the page.</span></span>
