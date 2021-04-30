---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d3f1fba05d944e78e4595018d190c3dc41e076
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907917"
---
# <a name="create-new-users"></a><span data-ttu-id="244b1-103">Opprette nye brukere</span><span class="sxs-lookup"><span data-stu-id="244b1-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="244b1-104">Før du får tilgang til Finance and Operations-apper, må du først legges til på **Bruker**-siden (**Systemadministrasjon \> Brukere \> Brukere**).</span><span class="sxs-lookup"><span data-stu-id="244b1-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="244b1-105">Brukere omfatter interne ansatte i organisasjonen eller eksterne kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="244b1-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="244b1-106">Brukere kan importeres eller legges til manuelt.</span><span class="sxs-lookup"><span data-stu-id="244b1-106">Users can be imported or added manually.</span></span> <span data-ttu-id="244b1-107">Alle brukere må lisensieres riktig for bruk i samsvar med forskriftene.</span><span class="sxs-lookup"><span data-stu-id="244b1-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="244b1-108">Hvis du vil ha informasjon om hvordan du kjøper og lisensierer for Finance and Operations-apper, kan du se [lisensieringsveiledningen for Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="244b1-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="244b1-109">Tilordne en lisens til en bruker</span><span class="sxs-lookup"><span data-stu-id="244b1-109">Assign a license to a user</span></span>
<span data-ttu-id="244b1-110">Systemadministratorer kan [tilordne lisenser til brukere](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [administrasjonssenteret for Microsoft 365](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="244b1-110">System admins can [assign licenses to users](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="244b1-111">Legge til en ekstern bruker i Azure AD og tilordne en lisens</span><span class="sxs-lookup"><span data-stu-id="244b1-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="244b1-112">Eksterne brukere må være representert i leierkatalogen (Azure Active Directory (Azure AD)), slik at de kan tilordnes lisenser.</span><span class="sxs-lookup"><span data-stu-id="244b1-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="244b1-113">Disse eksterne brukerne må legges til for leieren i Azure AD som gjestebrukere og deretter tilordnes de aktuelle lisensene.</span><span class="sxs-lookup"><span data-stu-id="244b1-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="244b1-114">Et krav for Finance and Operations-apper er at gjestebrukerens firma må bruke Azure AD.</span><span class="sxs-lookup"><span data-stu-id="244b1-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="244b1-115">Hvis du vil ha mer informasjon, kan du se [Legge til Azure Active Directory B2B-samarbeidsbrukere i Azure-portalen](/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="244b1-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="244b1-116">Importere nye brukere fra Azure AD</span><span class="sxs-lookup"><span data-stu-id="244b1-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="244b1-117">Gå til **Systemadministrasjon** \> **Brukere** \> **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="244b1-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="244b1-118">Velg **Importer brukere** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="244b1-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="244b1-119">Velg brukerne som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="244b1-119">Select the users to be imported.</span></span> <span data-ttu-id="244b1-120">Listen omfatter Azure AD-brukere som for øyeblikket ikke er brukere i dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="244b1-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="244b1-121">Velg **Importer brukere**.</span><span class="sxs-lookup"><span data-stu-id="244b1-121">Select **Import users**.</span></span>
5. <span data-ttu-id="244b1-122">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="244b1-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="244b1-123">Verdien i **Firma**-feltet angis basert på firmaet i gjeldende økt for administratoren. Etter importen må du tilordne aktuelle roller og organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="244b1-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="244b1-124">Hvis du vil ha mer informasjon, kan du se [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="244b1-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="244b1-125">Det kan også bli nødvendig å knytte brukeren til en **Person** og oppdatere brukeralternativer, for eksempel språk.</span><span class="sxs-lookup"><span data-stu-id="244b1-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="244b1-126">Legge til en ny bruker manuelt</span><span class="sxs-lookup"><span data-stu-id="244b1-126">Manually add a new user</span></span>
1. <span data-ttu-id="244b1-127">Gå til **Systemadministrasjon** \> **Brukere** \> **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="244b1-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="244b1-128">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="244b1-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="244b1-129">I **Bruker-ID**-feltet angir du en unik ID for brukeren.</span><span class="sxs-lookup"><span data-stu-id="244b1-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="244b1-130">Angi navnet på brukeren i **Brukernavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="244b1-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="244b1-131">I **Leverandør**-feltet:</span><span class="sxs-lookup"><span data-stu-id="244b1-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="244b1-132">Bruk standardverdien for interne brukere.</span><span class="sxs-lookup"><span data-stu-id="244b1-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="244b1-133">Eksempel: Azure AD-leieren med prefikset https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="244b1-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="244b1-134">Når det gjelder brukere uten Azure AD, for eksempel tjeneste-til-tjeneste-kontoer, angir du en enkel tekstverdi.</span><span class="sxs-lookup"><span data-stu-id="244b1-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="244b1-135">Eksempel: NA.</span><span class="sxs-lookup"><span data-stu-id="244b1-135">For example, NA.</span></span> <span data-ttu-id="244b1-136">Denne verdien bidrar til å unngå uriktige autentiseringsoppkall som kan føre til feil hvis det brukes en gyldig verdi for identitetsleverandør.</span><span class="sxs-lookup"><span data-stu-id="244b1-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="244b1-137">Når det gjelder eksterne brukere eller gjestebrukere, legger du til Azure AD-leiernavnet etter https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="244b1-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="244b1-138">I **E-post**-feltet angir du brukerens fulle e-postadresse / hovednavn for bruker.</span><span class="sxs-lookup"><span data-stu-id="244b1-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="244b1-139">Velg standard oppstartsfirma for brukeren i **Firma**-feltet.</span><span class="sxs-lookup"><span data-stu-id="244b1-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="244b1-140">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="244b1-140">Select **Save**.</span></span>

<span data-ttu-id="244b1-141">Verdiene for Identitetsleverandør og Telemetri-ID blir oppdatert basert på et [Microsoft Graph](/graph/overview)-kall når brukerposten lagres.</span><span class="sxs-lookup"><span data-stu-id="244b1-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="244b1-142">Telemetri-ID-en er basert på brukerens objekt-ID / sikkerhetsidentifikator (SID) i Azure AD.</span><span class="sxs-lookup"><span data-stu-id="244b1-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="244b1-143">Når du har lagt til en bruker, må du tilordne aktuelle roller og organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="244b1-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="244b1-144">Hvis du vil ha mer informasjon, kan du se [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="244b1-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="244b1-145">Det kan også bli nødvendig å knytte brukeren til en **Person** og oppdatere **Brukeralternativer**, for eksempel språk.</span><span class="sxs-lookup"><span data-stu-id="244b1-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="244b1-146">Endre en bruker-ID</span><span class="sxs-lookup"><span data-stu-id="244b1-146">Change a user ID</span></span>
<span data-ttu-id="244b1-147">Hvis du vil endre en bruker-ID, må du gi nøkkelen nytt navn i databasen.</span><span class="sxs-lookup"><span data-stu-id="244b1-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="244b1-148">Når du endrer en bruker-ID ved å bruke denne fremgangsmåten, endres alle relaterte brukerinnstillinger slik at den nye bruker-ID-en brukes.</span><span class="sxs-lookup"><span data-stu-id="244b1-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="244b1-149">Bruksinformasjonen i tabellen **SysLastValue** blir for eksempel oppdatert for å henvise til den nye bruker-ID-en.</span><span class="sxs-lookup"><span data-stu-id="244b1-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="244b1-150">Bruker-ID-en er primærnøkkelen i tabellen for brukerinformasjon.</span><span class="sxs-lookup"><span data-stu-id="244b1-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="244b1-151">Det kan ta litt tid å gi primærnøkkelen nytt navn for eksisterende brukere, fordi alle referanser til nøkkelen også oppdateres i databasen.</span><span class="sxs-lookup"><span data-stu-id="244b1-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="244b1-152">Gå til **Systemadministrasjon \> Brukere \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="244b1-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="244b1-153">Velg en bruker i listen, og velg **Alternativer \> Postinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="244b1-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="244b1-154">Velg **Gi nytt navn**.</span><span class="sxs-lookup"><span data-stu-id="244b1-154">Select **Rename**.</span></span>
4. <span data-ttu-id="244b1-155">Angi en ny og unik verdi for bruker-ID-en, og deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="244b1-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="244b1-156">Klikk på **Ja** for å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="244b1-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="244b1-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="244b1-157">Additional resources</span></span>

<span data-ttu-id="244b1-158">Hvis du vil ha flere alternativer for å implementere B2B-brukere, kan du se [Eksportere B2B-brukere til Azure AD](../implement-b2b.md).</span><span class="sxs-lookup"><span data-stu-id="244b1-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="244b1-159">Hvis du vil ha informasjon om forhåndskonfigurerte systemkontoer, kan du se [Forhåndskonfigurerte systemkontoer](../pre-configured-system-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="244b1-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]