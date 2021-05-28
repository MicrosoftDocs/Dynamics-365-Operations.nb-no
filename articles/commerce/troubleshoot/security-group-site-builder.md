---
title: Kan ikke konfigurere en sikkerhetsgruppe for Commerce-områdebygger under første distribusjon
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når sikkerhetsgruppen for Commerce-områdebyggeren for Microsoft Azure Active Directory (Azure AD) ikke vises som et alternativ når du oppretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under første distribusjon av en ny e-handelsleier.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020738"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="c5147-103">Kan ikke konfigurere en sikkerhetsgruppe for Commerce-områdebygger under første distribusjon</span><span class="sxs-lookup"><span data-stu-id="c5147-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5147-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når sikkerhetsgruppen for Commerce-områdebyggeren for Microsoft Azure Active Directory (Azure AD) ikke vises som et alternativ når du oppretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under første distribusjon av en ny e-handelsleier.</span><span class="sxs-lookup"><span data-stu-id="c5147-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="c5147-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c5147-105">Description</span></span>

<span data-ttu-id="c5147-106">Når du oppretter e-handelskomponentene som en del av prosessen med å distribuere en ny e-handel-leietaker som inneholder komponenten for commerce site builder, vises ikke sikkerhetsgruppen i Azure AD som et alternativ i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5147-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5147-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="c5147-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="c5147-108">Klargjøre e-handelsområdet med en bruker i riktig leietaker</span><span class="sxs-lookup"><span data-stu-id="c5147-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="c5147-109">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="c5147-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="c5147-110">Følg instruksjonene i [Opprett en grunnleggende gruppe og legg til medlemmer ved hjelp av Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) under den leietakeren som LCS-prosjektet for e-handel er klargjort for.</span><span class="sxs-lookup"><span data-stu-id="c5147-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="c5147-111">Gå til [LCS](https://lcs.dynamics.com/), og logg på med en konto som deler samme leietaker som sikkerhetsgruppen for Azure AD du akkurat opprettet.</span><span class="sxs-lookup"><span data-stu-id="c5147-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="c5147-112">Kontoen må ha tilgang til å vise sikkerhetsgruppen for Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c5147-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="c5147-113">Fullfør trinnene i oppsettet for å konfigurere e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="c5147-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="c5147-114">Når du klargjør e-handelskomponentene, skal sikkerhetsgruppen nå vises som et alternativ i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5147-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="c5147-115">Hvis du vil være sikker på at feltet i dialogboksen er fylt ut med listen med sikkerhetsgrupper, må du velge **Angi** etter at du har angitt navnet på sikkerhetsgruppen for Azure AD du opprettet.</span><span class="sxs-lookup"><span data-stu-id="c5147-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="c5147-116">Søkeresultatene viser alle sikkerhetsgruppene for Azure AD som starter med søketeksten, og som brukeren har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="c5147-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="c5147-117">Du kan bruke en kortere søketerm for å tillate bredere søkeresultater.</span><span class="sxs-lookup"><span data-stu-id="c5147-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5147-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c5147-118">Additional resources</span></span>

[<span data-ttu-id="c5147-119">Opprette en grunnleggende gruppe og legge til medlemmer ved hjelp av Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c5147-119">Create a basic group and add members using Azure Active Directory</span></span>](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="c5147-120">Distribuere en ny e-handelsleier</span><span class="sxs-lookup"><span data-stu-id="c5147-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)