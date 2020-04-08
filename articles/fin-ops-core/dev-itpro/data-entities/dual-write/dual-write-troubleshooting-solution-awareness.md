---
title: Feilsøke problemer knyttet til løsningsbevissthet
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172627"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="33a80-103">Feilsøke problemer knyttet til løsningsbevissthet</span><span class="sxs-lookup"><span data-stu-id="33a80-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="33a80-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="33a80-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="33a80-105">Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.</span><span class="sxs-lookup"><span data-stu-id="33a80-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33a80-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="33a80-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="33a80-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="33a80-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="33a80-108">Feil på siden Dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="33a80-108">Error on the Dual-write page</span></span>

<span data-ttu-id="33a80-109">På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="33a80-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="33a80-110">*Finner ikke enheten med\_navnet msdyn dualwriteentitymap med namemapping='Logisk i MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="33a80-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="33a80-111">Hvis du vil løse problemet, må du kontrollere at kjerneløsningen for dobbel skriving er installert i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="33a80-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="33a80-112">Kjernløsningen for dobbel skriving er en forutsetning for løsningsbevissthet.</span><span class="sxs-lookup"><span data-stu-id="33a80-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
