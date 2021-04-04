---
title: Feilsøke problemer knyttet til løsningsbevissthet
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f9e02a6a5afe965a1707f0b04e1b4daedd4ec1df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566795"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="fc2ff-103">Feilsøke problemer knyttet til løsningsbevissthet</span><span class="sxs-lookup"><span data-stu-id="fc2ff-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="fc2ff-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fc2ff-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="fc2ff-105">Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.</span><span class="sxs-lookup"><span data-stu-id="fc2ff-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc2ff-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="fc2ff-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="fc2ff-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="fc2ff-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="fc2ff-108">Feil på siden Dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="fc2ff-108">Error on the Dual-write page</span></span>

<span data-ttu-id="fc2ff-109">På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="fc2ff-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="fc2ff-110">*Finner ikke enheten med\_navnet msdyn dualwriteentitymap med namemapping='Logisk i MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="fc2ff-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="fc2ff-111">Hvis du vil løse problemet, må du kontrollere at kjerneløsningen for dobbel skriving er installert i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fc2ff-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="fc2ff-112">Kjernløsningen for dobbel skriving er en forutsetning for løsningsbevissthet.</span><span class="sxs-lookup"><span data-stu-id="fc2ff-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]