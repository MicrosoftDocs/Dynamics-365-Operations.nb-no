---
title: Brukeren ble ikke funnet i Personvelger i Attract eller Onboard
description: Dette emnet forklarer hva du gjør når brukere i leieren i selskapet ikke vises i Personvelger i Dynamics 365 Talent – Attract eller Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551939"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a><span data-ttu-id="b4bbb-103">Brukeren ble ikke funnet i Personvelger i Attract eller Onboard</span><span class="sxs-lookup"><span data-stu-id="b4bbb-103">User not found in People Picker in Attract or Onboard</span></span>
[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="b4bbb-104">Avgang</span><span class="sxs-lookup"><span data-stu-id="b4bbb-104">Issue</span></span>

<span data-ttu-id="b4bbb-105">Noen gyldige brukere i Microsoft Azure Active Directory (Azure AD) for leier vises ikke når du søker etter navnet i Personvelger i Dynamics 365 Talent: Attract eller Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="b4bbb-106">Årsak</span><span class="sxs-lookup"><span data-stu-id="b4bbb-106">Cause</span></span>

<span data-ttu-id="b4bbb-107">Enkelte brukertyper støttes ikke i Attract og Onboard.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="b4bbb-108">Kontroller at brukeren ikke er en Azure AD B2B-gjestebruker (bedrift til bedrift).</span><span class="sxs-lookup"><span data-stu-id="b4bbb-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="b4bbb-109">"Brukertype"-informasjon finnes i Azure Active Directory-bladet på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="b4bbb-110">Hvis du vil ha mer informasjon om Azure B2B, se [Hva er gjestebrukertilgang i Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="b4bbb-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="b4bbb-111">For ikke-B2B-brukere er det enkelte brukere som kan ha en ufullstendig "Brukertype"-egenskap i **Bruker**-objektet.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="b4bbb-112">Dette kan bekreftes og løses ved hjelp av Azure AD Powershell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="b4bbb-113">Hvis du vil ha mer informasjon, kan du se [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="b4bbb-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="b4bbb-114">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="b4bbb-114">Resolution</span></span>

<span data-ttu-id="b4bbb-115">For å fullføre fremgangsmåten nedenfor for å løse problemet må du ha "Global administrator"-tillatelser på Azure Active Directory-leieren eller tillatelser for **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="b4bbb-116">For å bekrefte "Brukertype" for den aktuelle brukeren.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="b4bbb-117">Kommandoen returnerer følgende informasjon.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="b4bbb-118">Merk **Brukertype**-egenskapen for brukeren.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="b4bbb-119">Hvis **Brukertype** er tom, for eksempel ikke "Medlem" eller "Gjest", kan du oppdatere den **Brukertype** ved hjelp av kommandoen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b4bbb-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
