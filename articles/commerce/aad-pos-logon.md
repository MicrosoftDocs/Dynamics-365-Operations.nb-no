---
title: Aktivere Azure Active Directory-godkjenning for POS-pålogging
description: Dette emnet forklarer hvordan du konfigurerer påloggingsopplevelsen for Microsoft Dynamics 365 Commerce-salgssted (POS) slik at den bruker Azure Active Directory-godkjenning.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 234d19bb6659af07c65763e05671742b9581e244
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206685"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="b9e77-103">Aktiver godkjenning av Azure Active Directory for salgsstedspålogging</span><span class="sxs-lookup"><span data-stu-id="b9e77-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="b9e77-104">Mange kunder som bruker Microsoft Dynamics 365 Commerce, bruker også andre Microsoft Cloud-tjenester, og de kan bruke Azure Active Directory (Azure AD) til å administrere brukerlegitimasjon for disse tjenestene.</span><span class="sxs-lookup"><span data-stu-id="b9e77-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="b9e77-105">I slike tilfeller vil kundene kanskje bruke samme Azure AD-konto på tvers av programmer.</span><span class="sxs-lookup"><span data-stu-id="b9e77-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="b9e77-106">Dette emnet forklarer hvordan du konfigurerer påloggingsopplevelsen for Commerce salgssted (POS) slik at den bruker Azure AD-godkjenning.</span><span class="sxs-lookup"><span data-stu-id="b9e77-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="b9e77-107">Konfigurere Azure AD-godkjenning</span><span class="sxs-lookup"><span data-stu-id="b9e77-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="b9e77-108">Hvis du vil gjøre Azure AD tilgjengelig som godkjenningsmetode for POS-pålogging for en butikk, må du konfigurere innstillingene for butikkens funksjonalitetsprofil og deretter bruke denne innstillingen på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="b9e77-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="b9e77-109">Hvis du vil konfigurere en funksjonalitetsprofil, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="b9e77-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="b9e77-110">Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Salgsstedsoppsett** \> **Salgsstedsprofiler** \> **Funksjonalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="b9e77-111">Velg funksjonalitetsprofilen du vil endre.</span><span class="sxs-lookup"><span data-stu-id="b9e77-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="b9e77-112">I hurtigfanen **Funksjoner**, i delen **Stabspålogging på salgssted**, endrer du verdien i feltet **Metode for påloggingsgodkjenning** fra **ID og passord for personale** til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="b9e77-113">Alle funksjonalitetsprofiler bruker som standard **ID og passord for personale** som godkjenningsmetode for POS.</span><span class="sxs-lookup"><span data-stu-id="b9e77-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="b9e77-114">Derfor må du endre verdien i feltet **Metode for påloggingsgodkjenning** hvis du vil bruke Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b9e77-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="b9e77-115">Hver detaljhandelsbutikk som er koblet til den valgte funksjonalitetsprofilen, påvirkes av denne endringen.</span><span class="sxs-lookup"><span data-stu-id="b9e77-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="b9e77-116">Følg denne fremgangsmåten for å bruke innstillingene på salgsstedsklienter.</span><span class="sxs-lookup"><span data-stu-id="b9e77-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="b9e77-117">Gå til **Retail og Commerce** \> **IT for Retail og Commerce** \> **Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="b9e77-118">Kjør distribusjonsplanen **1070** (**Kanalkonfigurasjon**).</span><span class="sxs-lookup"><span data-stu-id="b9e77-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="b9e77-119">Azure AD-godkjenning krever en Internett-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="b9e77-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="b9e77-120">Den vil ikke fungere når salgssted er i frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="b9e77-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="b9e77-121">For øyeblikket støtter ikke **Lederoverstyring**-funksjonen Azure AD som godkjenningsmetode.</span><span class="sxs-lookup"><span data-stu-id="b9e77-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="b9e77-122">Det kreves en operatør-ID og et passord selv om Azure AD er konfigurert som godkjenningsmetode for salgsstedspålogging.</span><span class="sxs-lookup"><span data-stu-id="b9e77-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="b9e77-123">Knytt en Azure AD-konto til en arbeider</span><span class="sxs-lookup"><span data-stu-id="b9e77-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="b9e77-124">Før en butikkarbeider kan bruke en Azure AD-konto til å logge seg på POS-programmet, må Azure AD-kontoen knyttes til denne arbeideren.</span><span class="sxs-lookup"><span data-stu-id="b9e77-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="b9e77-125">Følg denne fremgangsmåten for å knytte en Azure AD-konto til en arbeider.</span><span class="sxs-lookup"><span data-stu-id="b9e77-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="b9e77-126">Gå til **Detaljhandel og handel** \> **Ansatte** \> **Arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="b9e77-127">Åpne detaljersiden for en arbeider.</span><span class="sxs-lookup"><span data-stu-id="b9e77-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="b9e77-128">I handlingsruten, i kategorien **Commerce** i gruppen **Ekstern identitet** velger du **Tilknytt eksisterende identitet**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="b9e77-129">I dialogboksen **Bruk eksisterende eksterne ID** velger du **Søk ved hjelp av e-post**, angir en Azure AD-e-postadresse og velger **Søk**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="b9e77-130">Velg den returnerte Azure AD-kontoen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9e77-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="b9e77-131">Feltene **Alias**, **UPN** og **Ekstern underidentifikator** i kategorien **Commerce** på arbeiderens detaljside fylles ut.</span><span class="sxs-lookup"><span data-stu-id="b9e77-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="b9e77-132">Når en arbeiderpost er oppdatert, for eksempel hvis en ny Azure AD-konto er tilknyttet, endres et passord eller hvis en adressebok for ansatte blir oppdatert, anbefales det at du kjører **1060** (**Personale**) distribusjonsplan for å synkronisere den nyeste ansattinformasjonen til kanalen.</span><span class="sxs-lookup"><span data-stu-id="b9e77-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="b9e77-133">På denne måten kan POS-appen hente de riktige dataene for brukergodkjenning og godkjenningskontroll.</span><span class="sxs-lookup"><span data-stu-id="b9e77-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9e77-134">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b9e77-134">Additional resources</span></span>

[<span data-ttu-id="b9e77-135">Definere funksjonalitet for utvidet pålogging MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="b9e77-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="b9e77-136">Opprette en funksjonalitetsprofil for Retail</span><span class="sxs-lookup"><span data-stu-id="b9e77-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="b9e77-137"> Konfigurere en arbeider</span><span class="sxs-lookup"><span data-stu-id="b9e77-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]