---
title: Brukersikkerhet for leverandørportal
description: Denne artikkelen forklarer hvordan du konfigurerer sikkerhet for eksterne leverandører som bruker leverandørportalen. Denne informasjonen i dette emnet gjelder bare for februar 2016- og mai 2016-versjonene av Dynamics AX.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68972e5ad773403001e5825dec57ff678a4e9b49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259848"
---
# <a name="vendor-portal-user-security"></a><span data-ttu-id="32ec7-104">Brukersikkerhet for leverandørportal</span><span class="sxs-lookup"><span data-stu-id="32ec7-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32ec7-105">Denne artikkelen forklarer hvordan du konfigurerer sikkerhet for eksterne leverandører som bruker leverandørportalen.</span><span class="sxs-lookup"><span data-stu-id="32ec7-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="32ec7-106">Denne informasjonen i dette emnet gjelder bare for februar 2016- og mai 2016-versjonene av Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="32ec7-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="32ec7-107">Funksjonen for leverandørportal er erstattet med utvidede leverandørsamarbeidsfunksjoner i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="32ec7-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="32ec7-108">Hvis du vil ha mer informasjon om hvordan du konfigurerer sikkerhet for leverandørsamarbeid, kan du se [Konfigurere og vedlikehold leverandørsamarbeid](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="32ec7-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="32ec7-109">Leverandørportalen viser et begrenset sett med informasjon om bestillinger for eksterne leverandører.</span><span class="sxs-lookup"><span data-stu-id="32ec7-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="32ec7-110">Det er viktig at du riktig definerer brukertillatelser for leverandørportalen i Microsoft Dynamics AX, slik at leverandører ikke får utilsiktet tilgang til mer informasjon i Dynamics AX-installasjonen.</span><span class="sxs-lookup"><span data-stu-id="32ec7-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="32ec7-111">**Viktig:** i motsetning til andre brukere, skal ikke eksterne leverandører rollen **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="32ec7-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="32ec7-112">Rollen **SystemUser** gir tilgang til et sett med rettigheter som ikke er egnet for eksterne brukere.</span><span class="sxs-lookup"><span data-stu-id="32ec7-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="32ec7-113">Definere leverandørportalbruker</span><span class="sxs-lookup"><span data-stu-id="32ec7-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="32ec7-114">Før du oppretter en brukerkonto for en person som skal bruke leverandørportalen, må du definere leverandøren for å tillate leverandørportalsamarbeid.</span><span class="sxs-lookup"><span data-stu-id="32ec7-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="32ec7-115">Bruk feltet **Bestillingssamarbeid** i **Generelt** fanen på **Leverandører** siden.</span><span class="sxs-lookup"><span data-stu-id="32ec7-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="32ec7-116">Eksterne leverandører som bruker leverandørportalen må ha følgende oppsett:</span><span class="sxs-lookup"><span data-stu-id="32ec7-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="32ec7-117">En brukerkonto for Microsoft Azure Active Directory (AAD) må være registrert for leverandøren på **Brukere**-siden i Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="32ec7-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="32ec7-118">Leverandøren må ha **Leverandør (ekstern)** sikkerhetsrollen, ikke **SystemUser** rollen.</span><span class="sxs-lookup"><span data-stu-id="32ec7-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="32ec7-119">**Obs!** Rollen **SystemUser** tildeles automatisk når du oppretter en ny brukerkonto i Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="32ec7-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="32ec7-120">Derfor må du fjerne denne rollen og bekrefte advarselsmeldingen som du mottar.</span><span class="sxs-lookup"><span data-stu-id="32ec7-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="32ec7-121">Leverandørbrukeren må ikke gis tillatelse til å legge til flere felt fra bestillingstabellene i visningen av Bestillingen.</span><span class="sxs-lookup"><span data-stu-id="32ec7-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="32ec7-122">På **Tilpassing** fanen, i **Brukere** fanen, angir du **Eksplisitt tilpasning tillatt** alternativet for brukeren som **Nei**.</span><span class="sxs-lookup"><span data-stu-id="32ec7-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="32ec7-123">Brukerkontoen må være tilknyttet en registrert kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="32ec7-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="32ec7-124">På siden **Brukere** velger du en kontaktperson i **Navn** feltet.</span><span class="sxs-lookup"><span data-stu-id="32ec7-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="32ec7-125">Personen som du velger, skal ha **Kontakt**-rollen for den aktuelle leverandøren.</span><span class="sxs-lookup"><span data-stu-id="32ec7-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="32ec7-126">Hvis samme person krever tilgang til leverandørportalen for flere leverandørkontoer (for ulike juridiske enheter, kanskje), må hver av denne personens kontoer være tilknyttet samme registrerte kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="32ec7-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="32ec7-127">Rollen **Leverandør (ekstern)** inneholder alle de grunnleggende funksjonene som kreves for å bruke funksjonene som er tilgjengelig i leverandørportalen.</span><span class="sxs-lookup"><span data-stu-id="32ec7-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="32ec7-128">Dette oppsettet hjelper med å garantere at brukergrensesnittet som den eksterne brukeren ser, fokuserer på det tiltenkte scenariet.</span><span class="sxs-lookup"><span data-stu-id="32ec7-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="additional-resources"></a><span data-ttu-id="32ec7-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="32ec7-129">Additional resources</span></span>
--------

[<span data-ttu-id="32ec7-130">Samarbeide med leverandører ved hjelp av leverandørportalen</span><span class="sxs-lookup"><span data-stu-id="32ec7-130">Collaborate with vendors by using the Vendor portal</span></span>](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]