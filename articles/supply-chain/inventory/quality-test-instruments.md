---
title: Testinstrumenter for kvalitetsstyring
description: Dette emnet beskriver hvordan du oppretter testinstrumenter som kan brukes for tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021738"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="faf44-103">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="faf44-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="faf44-104">Dette emnet beskriver hvordan du oppretter testinstrumenter som kan brukes for tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="faf44-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="faf44-105">Du bruker siden **Testinstrumenter** til å definere og vise detaljer om enhetene som brukes til å utføre tester på kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="faf44-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="faf44-106">Testinstrumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="faf44-106">Test instruments are optional.</span></span> <span data-ttu-id="faf44-107">De kan imidlertid hjelpe kvalitetsarbeidere med å vite hvilket verktøy eller hvilket verktøy de bør bruke til å utføre en bestemt test.</span><span class="sxs-lookup"><span data-stu-id="faf44-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="faf44-108">Eksempel på testinstrument</span><span class="sxs-lookup"><span data-stu-id="faf44-108">Test instrument example</span></span>

<span data-ttu-id="faf44-109">Du utfører ulike tester på elektriske komponenter.</span><span class="sxs-lookup"><span data-stu-id="faf44-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="faf44-110">Noen tester er for spenningsutgangen for komponentene, én test er for temperaturen, og én test er for vekten.</span><span class="sxs-lookup"><span data-stu-id="faf44-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="faf44-111">Forskjellige verktøy, enheter eller utstyr brukes til å utføre hver test.</span><span class="sxs-lookup"><span data-stu-id="faf44-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="faf44-112">En spenningsmåler brukes for eksempel brukes til å måle spenning, et termometer for å måle temperatur og en vekt brukes til å måle vekten.</span><span class="sxs-lookup"><span data-stu-id="faf44-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="faf44-113">Du kan konfigurere hver av disse enhetene som et testinstrument, og angi måleenheten som testresultatene skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="faf44-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="faf44-114">Resultater fra denne spenningsmåleren registreres for eksempel i volt, resultater fra termometeret registreres i grader og resultater fra vekten registreres i pund eller kilogram.</span><span class="sxs-lookup"><span data-stu-id="faf44-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="faf44-115">Opprette et testinstrument</span><span class="sxs-lookup"><span data-stu-id="faf44-115">Create a test instrument</span></span>

1. <span data-ttu-id="faf44-116">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testinstrumenter**.</span><span class="sxs-lookup"><span data-stu-id="faf44-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="faf44-117">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="faf44-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="faf44-118">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="faf44-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="faf44-119">**Testinstrument** – Angi en unik ID eller et unikt navn for testinstrumentet.</span><span class="sxs-lookup"><span data-stu-id="faf44-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="faf44-120">**Beskrivelse** – Angi en detaljert beskrivelse av testinstrumentet.</span><span class="sxs-lookup"><span data-stu-id="faf44-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="faf44-121">**Enhet** – Velg enheten som instrumentet måler resultater i.</span><span class="sxs-lookup"><span data-stu-id="faf44-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="faf44-122">**Presisjon**-feltet angis automatisk, basert på enheten du velger.</span><span class="sxs-lookup"><span data-stu-id="faf44-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="faf44-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="faf44-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="faf44-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="faf44-124">Additional resources</span></span>

- [<span data-ttu-id="faf44-125">Kvalitetsstyringstest</span><span class="sxs-lookup"><span data-stu-id="faf44-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="faf44-126">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="faf44-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
