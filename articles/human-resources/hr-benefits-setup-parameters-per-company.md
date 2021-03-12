---
title: Konfigurer parametere for Fordelsbehandling per firma
description: Konfigurer parametere for Fordelsadministrasjon per firma i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "4984606"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="e34e1-103">Konfigurer parametere for Fordelsbehandling per firma</span><span class="sxs-lookup"><span data-stu-id="e34e1-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="e34e1-104">For hver organisasjon som tilbyr fordeler, må du konfigurere innstillinger for bekreftelse-e-poster for fordeler.</span><span class="sxs-lookup"><span data-stu-id="e34e1-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="e34e1-105">Konfigurere e-postinnstillinger for bekreftelse</span><span class="sxs-lookup"><span data-stu-id="e34e1-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="e34e1-106">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="e34e1-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="e34e1-107">I kategorien **Fordelsbehandling** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="e34e1-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="e34e1-108">Felt</span><span class="sxs-lookup"><span data-stu-id="e34e1-108">Field</span></span> | <span data-ttu-id="e34e1-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e34e1-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e34e1-110">**Send e-postbekreftelse**</span><span class="sxs-lookup"><span data-stu-id="e34e1-110">**Send confirmation email**</span></span> | <span data-ttu-id="e34e1-111">Når denne funksjonen er aktivert, sendes det en bekreftelses-e-post til ansatte når de sjekker ut fra fordelsregistreringen i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="e34e1-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="e34e1-112">**Mal for e-postbekreftelse**</span><span class="sxs-lookup"><span data-stu-id="e34e1-112">**Confirmation email template**</span></span> | <span data-ttu-id="e34e1-113">Velg e-postmalen for organisasjonen som skal brukes ved sending av registreringsbekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="e34e1-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="e34e1-114">Hvis du ikke velger en mal, blir følgende generelle e-post sendt:</span><span class="sxs-lookup"><span data-stu-id="e34e1-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="e34e1-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="e34e1-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="e34e1-116">Gratulerer!</span><span class="sxs-lookup"><span data-stu-id="e34e1-116">Congratulations!</span></span> <span data-ttu-id="e34e1-117">Du har fullført fordelsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="e34e1-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="e34e1-118">Takk,</span><span class="sxs-lookup"><span data-stu-id="e34e1-118">Thank you,</span></span><br><span data-ttu-id="e34e1-119"><Company/Org name>-fordeler.</span><span class="sxs-lookup"><span data-stu-id="e34e1-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="e34e1-120">**Standard e-postadresse for avsender**</span><span class="sxs-lookup"><span data-stu-id="e34e1-120">**Default email sender address**</span></span> | <span data-ttu-id="e34e1-121">E-postadressen som skal brukes når du sender e-postmeldingen med bekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="e34e1-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="e34e1-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e34e1-122">Select **Save**.</span></span>