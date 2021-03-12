---
title: Opprette ER-konfigurasjoner i RCS og laste dem opp til det globale repositoriet
description: Dette emnet forklarer hvordan du oppretter en konfigurasjon for elektronisk rapportering (ER) i Microsoft RCS (Regulatory Configuration Services) og laster den opp til det globale repositoriet.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ef12c911c8953b181db1c0eff0874a3d8cfcb3da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005754"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="a8839-103">Opprette ER-konfigurasjoner i Regulatory Configuration Services (RCS) og laste dem opp til det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="a8839-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8839-104">Du kan bruke Microsoft Regulatory Configuration Services (RCS) til å utforme konfigurasjoner for elektronisk rapportering (ER) og publisere dem slik at de kan brukes i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="a8839-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="a8839-105">Fremgangsmåtene nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller elektronisk rapportering kan opprette en avledet versjon av en ER-konfigurasjon som er konfigurert i en RCS-forekomst, og deretter laste opp den avledede konfigurasjonen til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a8839-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="a8839-106">Før du kan fullføre de prosedyrene, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a8839-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="a8839-107">Åpne en RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="a8839-107">Access an RCS instance.</span></span>
- <span data-ttu-id="a8839-108">Opprette en aktiv konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="a8839-108">Create an active configuration provider.</span></span> <span data-ttu-id="a8839-109">Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a8839-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="a8839-110">Du må også kontrollere at det er klargjort et RCS-miljø for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="a8839-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="a8839-111">I en Finance and Operations-app går du til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a8839-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="a8839-112">Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Ekstern konfigurasjon**, og deretter følger du instruksjonene for å klargjøre en.</span><span class="sxs-lookup"><span data-stu-id="a8839-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="a8839-113">Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til den ved å velge alternativet for pålogging.</span><span class="sxs-lookup"><span data-stu-id="a8839-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="a8839-114">Opprette en avledet versjon av en konfigurasjon i RCS</span><span class="sxs-lookup"><span data-stu-id="a8839-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="a8839-115">I arbeidsområdet **Elektronisk rapportering** kontrollerer du at du har en aktiv konfigurasjonsleverandør for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="a8839-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="a8839-116">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a8839-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a8839-117">Velg konfigurasjonen du vil avlede en ny versjon fra.</span><span class="sxs-lookup"><span data-stu-id="a8839-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="a8839-118">Du kan bruke filtreringsfeltet over treet til å begrense søket.</span><span class="sxs-lookup"><span data-stu-id="a8839-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="a8839-119">Velg **Opprett konfigurasjon** \> **Avled fra navn**.</span><span class="sxs-lookup"><span data-stu-id="a8839-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="a8839-120">Angi et navn og en beskrivelse, og velg deretter **Opprett konfigurasjon** for å opprette en ny avledet versjon.</span><span class="sxs-lookup"><span data-stu-id="a8839-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="a8839-121">Velg den nylig avledede konfigurasjonen, legg til en beskrivelse av versjonen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8839-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="a8839-122">Statusen for konfigurasjonen til er endret til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="a8839-122">The status of the configuration to is changed to **Completed**.</span></span>

![Ny konfigurasjonsversjon i RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="a8839-124">Når konfigurasjonsstatusen endres, kan du få en valideringsfeilmelding som er knyttet til de tilkoblede appene.</span><span class="sxs-lookup"><span data-stu-id="a8839-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="a8839-125">Hvis du vil deaktivere valideringen, velger du **Brukerparametere** i kategorien **Konfigurasjoner**, og deretter setter du alternativet **Hopp over validering ved konfigurasjonens statusendring og rebasering** til **Ja**</span><span class="sxs-lookup"><span data-stu-id="a8839-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="a8839-126">Laste opp en konfigurasjon til det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="a8839-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="a8839-127">Hvis du vil dele en ny eller avledet konfigurasjon med organisasjonen, kan du laste den opp til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a8839-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="a8839-128">Velg den fullførte versjonen av konfigurasjonen, og velg deretter **Last opp til repositorium**.</span><span class="sxs-lookup"><span data-stu-id="a8839-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="a8839-129">Velg alternativet **Globalt (Microsoft)**, og velg deretter **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="a8839-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Laste opp til alternativer for repositorium](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="a8839-131">Velg **Ja** i bekreftelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="a8839-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="a8839-132">Oppdater beskrivelsen av versjonen etter behov, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8839-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="a8839-133">Statusen for konfigurasjonen oppdateres til **Dele**, og konfigurasjonen lastes opp til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a8839-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="a8839-134">Derfra kan du arbeide med den på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="a8839-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="a8839-135">Importere den til Dynamics 365-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="a8839-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="a8839-136">Hvis du vil ha mer informasjon, kan du se [(ER) Importere konfigurasjoner fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="a8839-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="a8839-137">Hvis du vil dele den med en tredjepart eller en ekstern organisasjon, kan du se [RCS Dele konfigurasjoner for elektronisk rapportering (ER) med eksterne organisasjoner](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="a8839-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Avledet versjon av Intrastat Contoso-konfigurasjon i det globale repositoriet](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="a8839-139">Slette en konfigurasjon fra det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="a8839-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="a8839-140">Fullfør fremgangsmåten nedenfor for å slette en konfigurasjon som organisasjonen har opprettet.</span><span class="sxs-lookup"><span data-stu-id="a8839-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="a8839-141">I arbeidsområdet **Elektronisk rapportering** kontrollerer du at konfigurasjonsleverandøren er **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a8839-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="a8839-142">Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a8839-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="a8839-143">Velg **repositorium** på den aktive konfigurasjonsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="a8839-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="a8839-144">Velg lagertypen **Global**, og velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="a8839-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="a8839-145">I hurtigfanen **Filter** finner du konfigurasjonen du vil slette, ved hjelp av **Filter**-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="a8839-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="a8839-146">I hurtigfanen **Versjon** velger du versjonen av konfigurasjonen du vil slette, og deretter velger du **Slett**:</span><span class="sxs-lookup"><span data-stu-id="a8839-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Slette en konfigurasjon fra det globale repositoriet](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="a8839-148">Velg **Ja** i bekreftelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="a8839-148">In the confirmation message box, select **Yes**.</span></span>

    ![Slette bekreftelsesmelding for konfigurasjonsversjon](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="a8839-150">Konfigurasjonsversjonen blir slettet, og bekreftelsesmeldingen vises.</span><span class="sxs-lookup"><span data-stu-id="a8839-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="a8839-151">Konfigurasjoner kan bare slettes av konfigurasjonsleverandøren som opprettet dem.</span><span class="sxs-lookup"><span data-stu-id="a8839-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="a8839-152">Hvis konfigurasjonen er delt med en annen organisasjon, må du oppheve delingen av konfigurasjonen før du sletter den.</span><span class="sxs-lookup"><span data-stu-id="a8839-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
