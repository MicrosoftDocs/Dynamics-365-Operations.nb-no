---
title: Aktivere Azure Active Directory-godkjenning for POS-pålogging
description: Dette emnet forklarer hvordan du konfigurerer påloggingsopplevelsen for Microsoft Dynamics 365 Commerce salgssted (POS) slik at den bruker Azure Active Directory-godkjenning.
author: boycezhu
manager: annbe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 4f5a02348e8cef44424ae5d6a49de02d762ba245
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410041"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="81458-103">Aktivere Azure Active Directory-godkjenning for POS-pålogging</span><span class="sxs-lookup"><span data-stu-id="81458-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="81458-104">Mange kunder som bruker Microsoft Dynamics 365 Commerce, bruker også andre Microsoft Cloud-tjenester, og de kan bruke Azure Active Directory (Azure AD) til å administrere brukerlegitimasjon for disse tjenestene.</span><span class="sxs-lookup"><span data-stu-id="81458-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="81458-105">I slike tilfeller vil kundene kanskje bruke samme Azure AD-konto på tvers av programmer.</span><span class="sxs-lookup"><span data-stu-id="81458-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="81458-106">Dette emnet forklarer hvordan du konfigurerer påloggingsopplevelsen for Commerce salgssted (POS) slik at den bruker Azure AD-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="81458-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="81458-107">Konfigurere Azure AD-godkjenning</span><span class="sxs-lookup"><span data-stu-id="81458-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="81458-108">Hvis du vil gjøre Azure AD tilgjengelig som godkjenningsmetode for POS-pålogging for en butikk, må du konfigurere innstillingene for butikkens funksjonalitetsprofil og deretter bruke denne innstillingen på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="81458-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="81458-109">Hvis du vil konfigurere en funksjonalitetsprofil, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="81458-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="81458-110">Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Salgsstedsoppsett** \> **Salgsstedsprofiler** \> **Funksjonalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="81458-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="81458-111">Velg funksjonalitetsprofilen du vil endre.</span><span class="sxs-lookup"><span data-stu-id="81458-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="81458-112">I hurtigfanen **Funksjoner**, i delen **Stabspålogging på salgssted**, endrer du verdien i feltet**Metode for påloggingsgodkjenning** fra **ID og passord for personale** til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="81458-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="81458-113">Alle funksjonalitetsprofiler bruker som standard **ID og passord for personale** som godkjenningsmetode for POS.</span><span class="sxs-lookup"><span data-stu-id="81458-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="81458-114">Derfor må du endre verdien i feltet **Metode for påloggingsgodkjenning** hvis du vil bruke Azure AD.</span><span class="sxs-lookup"><span data-stu-id="81458-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="81458-115">Hver detaljhandelsbutikk som er koblet til den valgte funksjonalitetsprofilen, påvirkes av denne endringen.</span><span class="sxs-lookup"><span data-stu-id="81458-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="81458-116">Følg denne fremgangsmåten for å bruke innstillingene på salgsstedsklienter.</span><span class="sxs-lookup"><span data-stu-id="81458-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="81458-117">Gå til **Retail og Commerce** \> **IT for Retail og Commerce** \> **Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="81458-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="81458-118">Kjør distribusjonsplanen **1070** (**Kanalkonfigurasjon**).</span><span class="sxs-lookup"><span data-stu-id="81458-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="81458-119">Azure AD-godkjenning krever en Internett-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="81458-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="81458-120">Den vil ikke fungere når salgssted er i frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="81458-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="81458-121">For øyeblikket støtter ikke **Lederoverstyring**-funksjonen Azure AD som godkjenningsmetode.</span><span class="sxs-lookup"><span data-stu-id="81458-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="81458-122">Det kreves en operatør-ID og et passord selv om Azure AD er konfigurert som godkjenningsmetode for salgsstedspålogging.</span><span class="sxs-lookup"><span data-stu-id="81458-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="81458-123">Knytt en Azure AD-konto til en arbeider</span><span class="sxs-lookup"><span data-stu-id="81458-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="81458-124">Før en butikkarbeider kan bruke en Azure AD-konto til å logge seg på POS-programmet, må Azure AD-kontoen knyttes til denne arbeideren.</span><span class="sxs-lookup"><span data-stu-id="81458-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="81458-125">Følg denne fremgangsmåten for å knytte en Azure AD-konto til en arbeider.</span><span class="sxs-lookup"><span data-stu-id="81458-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="81458-126">Gå til **Detaljhandel og handel** \> **Ansatte** \> **Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="81458-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="81458-127">Åpne detaljersiden for en arbeider.</span><span class="sxs-lookup"><span data-stu-id="81458-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="81458-128">I handlingsruten, i kategorien **Commerce** i gruppen **Ekstern identitet** velger du **Tilknytt eksisterende identitet**.</span><span class="sxs-lookup"><span data-stu-id="81458-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="81458-129">I dialogboksen **Bruk eksisterende eksterne ID** velger du **Søk ved hjelp av e-post**, angir en Azure AD-e-postadresse og velger **Søk**.</span><span class="sxs-lookup"><span data-stu-id="81458-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="81458-130">Velg den returnerte Azure AD-kontoen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="81458-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="81458-131">Feltene **Alias**, **UPN** og **Ekstern underidentifikator** i kategorien **Commerce** på arbeiderens detaljside fylles ut.</span><span class="sxs-lookup"><span data-stu-id="81458-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81458-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="81458-132">Additional resources</span></span>

[<span data-ttu-id="81458-133">Definere funksjonalitet for utvidet pålogging MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="81458-133">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="81458-134">Opprette en funksjonalitetsprofil for Retail</span><span class="sxs-lookup"><span data-stu-id="81458-134">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="81458-135"> Konfigurere en arbeider</span><span class="sxs-lookup"><span data-stu-id="81458-135">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
