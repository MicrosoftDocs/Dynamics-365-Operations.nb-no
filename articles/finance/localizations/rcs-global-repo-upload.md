---
title: Opprette ER-konfigurasjoner i RCS og laste dem opp til det globale repositoriet
description: Dette emnet forklarer hvordan du oppretter en konfigurasjon for elektronisk rapportering (ER) i Microsoft RCS (Regulatory Configuration Services) og laster den opp til det globale repositoriet.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371261"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="87896-103">Opprette ER-konfigurasjoner i Regulatory Configuration Services (RCS) og laste dem opp til det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="87896-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87896-104">Du kan bruke Microsoft Regulatory Configuration Services (RCS) til å utforme konfigurasjoner for elektronisk rapportering (ER) og publisere dem slik at de kan brukes i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="87896-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="87896-105">Fremgangsmåtene nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller elektronisk rapportering kan opprette en avledet versjon av en ER-konfigurasjon som er konfigurert i en RCS-forekomst, og deretter laste opp den avledede konfigurasjonen til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="87896-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="87896-106">Før du kan fullføre de prosedyrene, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="87896-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="87896-107">Åpne en RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="87896-107">Access an RCS instance.</span></span>
- <span data-ttu-id="87896-108">Opprette en aktiv konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="87896-108">Create an active configuration provider.</span></span> <span data-ttu-id="87896-109">Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="87896-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="87896-110">Du må også kontrollere at det er klargjort et RCS-miljø for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="87896-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="87896-111">I en Finance and Operations-app går du til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="87896-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="87896-112">Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Ekstern konfigurasjon**, og deretter følger du instruksjonene for å klargjøre en.</span><span class="sxs-lookup"><span data-stu-id="87896-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="87896-113">Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til den ved å velge alternativet for pålogging.</span><span class="sxs-lookup"><span data-stu-id="87896-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="87896-114">Opprette en avledet versjon av en konfigurasjon i RCS</span><span class="sxs-lookup"><span data-stu-id="87896-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="87896-115">I arbeidsområdet **Elektronisk rapportering** kontrollerer du at du har en aktiv konfigurasjonsleverandør for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="87896-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="87896-116">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="87896-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="87896-117">Velg konfigurasjonen du vil avlede en ny versjon fra.</span><span class="sxs-lookup"><span data-stu-id="87896-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="87896-118">Du kan bruke filtreringsfeltet over treet til å begrense søket.</span><span class="sxs-lookup"><span data-stu-id="87896-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="87896-119">Velg **Opprett konfigurasjon** \> **Avled fra navn**.</span><span class="sxs-lookup"><span data-stu-id="87896-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="87896-120">Angi et navn og en beskrivelse, og velg deretter **Opprett konfigurasjon** for å opprette en ny avledet versjon.</span><span class="sxs-lookup"><span data-stu-id="87896-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="87896-121">Velg den nylig avledede konfigurasjonen, legg til en beskrivelse av versjonen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="87896-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="87896-122">Statusen for konfigurasjonen til er endret til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="87896-122">The status of the configuration to is changed to **Completed**.</span></span>

![Ny konfigurasjonsversjon i RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="87896-124">Når konfigurasjonsstatusen endres, kan du få en valideringsfeilmelding som er knyttet til de tilkoblede appene.</span><span class="sxs-lookup"><span data-stu-id="87896-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="87896-125">Hvis du vil deaktivere valideringen, velger du **Brukerparametere** i kategorien **Konfigurasjoner**, og deretter setter du alternativet **Hopp over validering ved konfigurasjonens statusendring og rebasering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="87896-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="87896-126">Laste opp en konfigurasjon til det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="87896-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="87896-127">Hvis du vil dele en ny eller avledet konfigurasjon med organisasjonen, kan du laste den opp til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="87896-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="87896-128">Velg den fullførte versjonen av konfigurasjonen, og velg deretter **Last opp til repositorium**.</span><span class="sxs-lookup"><span data-stu-id="87896-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="87896-129">Velg alternativet **Globalt (Microsoft)**, og velg deretter **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="87896-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Laste opp til alternativer for repositorium](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="87896-131">Velg **Ja** i bekreftelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="87896-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="87896-132">Oppdater beskrivelsen av versjonen etter behov, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="87896-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="87896-133">Statusen for konfigurasjonen oppdateres til **Dele**, og konfigurasjonen lastes opp til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="87896-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="87896-134">Derfra kan du arbeide med den på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="87896-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="87896-135">Importere den til Dynamics 365-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="87896-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="87896-136">Hvis du vil ha mer informasjon, kan du se [(ER) Importere konfigurasjoner fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="87896-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="87896-137">Hvis du vil dele den med en tredjepart eller en ekstern organisasjon, kan du se [RCS Dele konfigurasjoner for elektronisk rapportering (ER) med eksterne organisasjoner](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="87896-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Avledet versjon av Intrastat Contoso-konfigurasjon i det globale repositoriet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
