---
title: Komme i gang med Globalt lagerregnskap
description: Dette emnet beskriver hvordan du kommer i gang med Globalt lagerregnskap.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301704"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="608a2-103">Komme i gang med Globalt lagerregnskap</span><span class="sxs-lookup"><span data-stu-id="608a2-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="608a2-104">Ved hjelp av Globalt lagerregnskap kan du utføre flere lagerregnskap i Globalt lagerregnskap-finanskontoer du har definert.</span><span class="sxs-lookup"><span data-stu-id="608a2-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="608a2-105">Du må knytte hver finanskonto for Globalt lagerregnskap til en *konvensjon*.</span><span class="sxs-lookup"><span data-stu-id="608a2-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="608a2-106">En konvensjon er en samling av følgende typer regnskapspolicyer:</span><span class="sxs-lookup"><span data-stu-id="608a2-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="608a2-107">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="608a2-107">Cost object</span></span>
- <span data-ttu-id="608a2-108">Målingsgrunnlag for inndata</span><span class="sxs-lookup"><span data-stu-id="608a2-108">Input measurement basis</span></span>
- <span data-ttu-id="608a2-109">Kostnadsflytforutsetning</span><span class="sxs-lookup"><span data-stu-id="608a2-109">Cost flow assumption</span></span>
- <span data-ttu-id="608a2-110">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="608a2-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="608a2-111">Selv etter at du har aktivert Globalt lagerregnska, kan du fremdeles utføre lagerregnskap i Microsoft Dynamics 365 Supply Chain Management, som vanlig.</span><span class="sxs-lookup"><span data-stu-id="608a2-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="608a2-112">Globalt lagerregnskap er et tillegg.</span><span class="sxs-lookup"><span data-stu-id="608a2-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="608a2-113">Hvis du vil gjøre funksjonene tilgjengelige, må du installere det fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="608a2-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="608a2-114">Du kan velge å evaluere det i et testmiljø før du aktiverer det for produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="608a2-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="608a2-115">Globalt lagerregnskap støtter for øyeblikket ikke alle kostnadsstyringsfunksjonene som er innebygd i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="608a2-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="608a2-116">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="608a2-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="608a2-117">Slik får du offentlig forhåndsversjon av Globalt lagerregnskap</span><span class="sxs-lookup"><span data-stu-id="608a2-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="608a2-118">Hvis du vil bruke Globalt lagerregnskap, må du ha et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø).</span><span class="sxs-lookup"><span data-stu-id="608a2-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="608a2-119">I tillegg må du kjøre Supply Chain Management versjon 10.0.19 eller senere.</span><span class="sxs-lookup"><span data-stu-id="608a2-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="608a2-120">Hvis du vil registrere deg for offentlig forhåndsversjon av Globalt lagerregnskap, kan du sende LCS-miljø-IDen med e-post til [Globalt lagerregnskap-teamet](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="608a2-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="608a2-121">Når du er godkjent for programmet, sender teamet deg en oppfølgings-e-post som inneholder en betanøkkel for Globalt lagerregnskap og tjenesteendepunktene.</span><span class="sxs-lookup"><span data-stu-id="608a2-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="608a2-122">Når du har mottatt betanøkkelen, kan du [installere tillegget](#install).</span><span class="sxs-lookup"><span data-stu-id="608a2-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="608a2-123">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="608a2-123">Licensing</span></span>

<span data-ttu-id="608a2-124">Globalt lagerregnskap lisensieres sammen med standardfunksjonene for lagerregnskap som er tilgjengelig for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="608a2-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="608a2-125">Du trenger ikke kjøpe en tilleggslisens for å bruke Globalt lagerregnskap.</span><span class="sxs-lookup"><span data-stu-id="608a2-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="608a2-126">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="608a2-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="608a2-127">Konfigurer Microsoft Power Platform-integrering</span><span class="sxs-lookup"><span data-stu-id="608a2-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="608a2-128">Før du kan aktivere tilleggfunksjonalitet, må du integrere med Microsoft Power Platform ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="608a2-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="608a2-129">Åpne LCS-miljøet der du vil legge til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="608a2-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="608a2-130">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="608a2-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="608a2-131">Velg **Oppsett**-knappen i delen **Power Platform-integrering**.</span><span class="sxs-lookup"><span data-stu-id="608a2-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="608a2-132">Merk av for avmerkingsboksen i dialogboksen for **Oppsett av Power Platform-miljø**, og velg deretter **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="608a2-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="608a2-133">Vanligvis tar oppsettet mellom 60 og 90 minutter.</span><span class="sxs-lookup"><span data-stu-id="608a2-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="608a2-134">Når oppsettet av Microsoft Power Platform-miljøet er fullført, viser siden navnet på miljøet.</span><span class="sxs-lookup"><span data-stu-id="608a2-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="608a2-135">I tillegg viser delen **Power Platform-integrering** setningen "Power Platform-miljøoppsettet er fullført."</span><span class="sxs-lookup"><span data-stu-id="608a2-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="608a2-136">Globalt lagerregnskap krever ikke et program med dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="608a2-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="608a2-137">Hvis du vil ha mer informasjon, kan du se [Konfigurere etter miljødistribusjon](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="608a2-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="608a2-138">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="608a2-138">Set up Dataverse</span></span>

<span data-ttu-id="608a2-139">Før du definerer Dataverse, kan du legge til serviceprinsippene for Globalt lagerregnskap i leietakeren ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="608a2-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="608a2-140">Installer Azure AD-modul for Windows PowerShell v2 som beskrevet i [Installere Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="608a2-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="608a2-141">Kjør følgende PowerShell-kommando.</span><span class="sxs-lookup"><span data-stu-id="608a2-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="608a2-142">Deretter oppretter du programbrukere for Globalt lagerregnskap i Dataverse ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="608a2-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="608a2-143">Åpne URL-adressen for Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="608a2-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="608a2-144">Gå til **Avansert innstilling \> System \> Sikkerhet \> Brukere** og opporett en appbruker.</span><span class="sxs-lookup"><span data-stu-id="608a2-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="608a2-145">Bruk **Vis**-feltet til å endre sidevisningen til *Programbrukere*.</span><span class="sxs-lookup"><span data-stu-id="608a2-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="608a2-146">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="608a2-146">Select **New**.</span></span>
1. <span data-ttu-id="608a2-147">Angi **Program-ID**-feltet til *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="608a2-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="608a2-148">Velg **Tilordne rolle**, og velg deretter *Systemadministrator*.</span><span class="sxs-lookup"><span data-stu-id="608a2-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="608a2-149">Hvis det finnes en rolle kalt *Common Data Service-bruker*, velger du den også.</span><span class="sxs-lookup"><span data-stu-id="608a2-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="608a2-150">Gjenta de forrige trinnene, men sett feltet **Program-ID** til *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="608a2-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="608a2-151">Hvis du vil ha mer informasjon, kan du se [Opprette en appbruker](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="608a2-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="608a2-152">Hvis standardspråket for Dataverse-installasjonen ikke er engelsk, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="608a2-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="608a2-153">Gå til **Avanserte innstillinger \> Administrasjon \> Språk**.</span><span class="sxs-lookup"><span data-stu-id="608a2-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="608a2-154">Velg *Engelsk* (*LanguageCode=1033*), og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="608a2-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="608a2-155">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="608a2-155">Install the add-in</span></span>

<span data-ttu-id="608a2-156">Følg denne fremgangsmåten for å installere tillegget, slik at du kan bruke Globalt lagerregnskap.</span><span class="sxs-lookup"><span data-stu-id="608a2-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="608a2-157">[Registrer deg](#sign-up) for offentlig forhåndsversjon av Globalt lagerregnskap.</span><span class="sxs-lookup"><span data-stu-id="608a2-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="608a2-158">Logg på [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="608a2-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="608a2-159">Gå til **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="608a2-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="608a2-160">Velg plusstegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="608a2-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="608a2-161">I **Kode** -feltet angir du betanøkkelen for tillegget for Globalt lagerregnskap.</span><span class="sxs-lookup"><span data-stu-id="608a2-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="608a2-162">(Du skal ha mottatt betanøkkelen via e-post da du registrerte deg.)</span><span class="sxs-lookup"><span data-stu-id="608a2-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="608a2-163">Velg **Fjern blokkering**.</span><span class="sxs-lookup"><span data-stu-id="608a2-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="608a2-164">Åpne LCS-miljøet der du vil legge til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="608a2-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="608a2-165">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="608a2-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="608a2-166">Gå til **Power Platform-integreringen**, og velg **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="608a2-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="608a2-167">Merk av for avmerkingsboksen i dialogboksen for **Oppsett av Power Platform-miljø**, og velg deretter **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="608a2-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="608a2-168">Vanligvis tar oppsettet mellom 60 og 90 minutter.</span><span class="sxs-lookup"><span data-stu-id="608a2-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="608a2-169">Når oppsettet av Microsoft Power Platform-miljøet er fullført, går du til hurtigkategorien **Miljøtillegg** og velger **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="608a2-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="608a2-170">Velg **Globalt lagerregnskap**.</span><span class="sxs-lookup"><span data-stu-id="608a2-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="608a2-171">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="608a2-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="608a2-172">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="608a2-172">Select **Install**.</span></span>
1. <span data-ttu-id="608a2-173">I hurtigfanen **Miljøtillegg** skal du se at Globalt lagerrenskap blir installert.</span><span class="sxs-lookup"><span data-stu-id="608a2-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="608a2-174">Etter noen minutter skal statusen endres fra *Installerer* til *Installert*.</span><span class="sxs-lookup"><span data-stu-id="608a2-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="608a2-175">(Det kan hende du må oppdatere siden for å se denne endringen.) På dette tidspunktet er Globalt lagerregnskap klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="608a2-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="608a2-176">Defininere integreringen</span><span class="sxs-lookup"><span data-stu-id="608a2-176">Set up the integration</span></span>

<span data-ttu-id="608a2-177">Følg denne fremgangsmåten for å sette opp integreringen mellom Globalt lagerregnskap og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="608a2-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="608a2-178">Logg på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="608a2-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="608a2-179">Gå til **Systemadministrasjon \> Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="608a2-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="608a2-180">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="608a2-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="608a2-181">I kategorien **Alle** søker du etter funksjonen som kalles *Globalt lagerregnskap*.</span><span class="sxs-lookup"><span data-stu-id="608a2-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="608a2-182">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="608a2-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="608a2-183">Gå til **Globalt lagerregnskap \> Oppsett \> Parametere for Globalt lagerregnskap \> Integreringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="608a2-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="608a2-184">I feltene **Datatjenesteendepunkt** og **Endepunkt for Globalt lagerregnskap** angir du URL-adressene fra e-postmeldingen som Globalt lagerregnskap-teamet sendte da du registrerte deg for forhåndsvisningen.</span><span class="sxs-lookup"><span data-stu-id="608a2-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="608a2-185">Globalt lagerregnskap er nå klart til bruk.</span><span class="sxs-lookup"><span data-stu-id="608a2-185">Global Inventory Accounting is now ready to use.</span></span>
