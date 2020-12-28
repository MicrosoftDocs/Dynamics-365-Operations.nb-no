---
title: Installere, konfigurere og oppdatere kundeportalen
description: Dette emnet inneholder lisensdetaljer og konfigurasjonsinstruksjoner for kundeportalen.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529536"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="add71-103">Installere, konfigurere og oppdatere kundeportalen</span><span class="sxs-lookup"><span data-stu-id="add71-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="add71-104">Lisenskrav</span><span class="sxs-lookup"><span data-stu-id="add71-104">Licensing requirements</span></span>

<span data-ttu-id="add71-105">For å implementere kundeportalen må du ha følgende lisenser:</span><span class="sxs-lookup"><span data-stu-id="add71-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="add71-106">**Power Apps-portaler** – denne lisensen kreves for å være vert for kundeportalen.</span><span class="sxs-lookup"><span data-stu-id="add71-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="add71-107">Portaler lisensieres basert på bruk.</span><span class="sxs-lookup"><span data-stu-id="add71-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="add71-108">Du finner mer informasjon i [Lisenskrav for Power Apps-portaler](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="add71-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="add71-109">**Dobbeltskriving** – du må ha de nødvendige lisensene for å kunne bruke to dobbeltskriving for Supply Chain Management-enheter.</span><span class="sxs-lookup"><span data-stu-id="add71-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="add71-110">Hvis du vil ha mer informasjon, kan du se [systemkravene for dobbeltskriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="add71-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="add71-111">Avhengigheter for dobbeltskriving og Power Apps-portaler</span><span class="sxs-lookup"><span data-stu-id="add71-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="add71-112">Kundeportalen er avhengig av Power Apps-portaler og dobbeltskriving, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="add71-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="add71-113">![Avhengigheter for kundeportal](media/customer-portal-elements.png "Avhengigheter for kundeportal")</span><span class="sxs-lookup"><span data-stu-id="add71-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="add71-114">Til forskjell fra andre funksjoner fra Supply Chain Management, ligger kundeportalmalen i Power Apps-portaler.</span><span class="sxs-lookup"><span data-stu-id="add71-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="add71-115">Kundeportalen er derfor begrenset av funksjonaliteten og mulighetene som leveres av Power Apps-portaler og enhetene i dobbeltskriving.</span><span class="sxs-lookup"><span data-stu-id="add71-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="add71-116">Nødvendig konfigurasjon for å aktivere kundeportalen</span><span class="sxs-lookup"><span data-stu-id="add71-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="add71-117">Når du er sikker på at du har de nødvendige lisensene, kan du konfigurere dobbeltskriving som beskrevet i [instruksjoner for innledende synkronisering med dobbeltskriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="add71-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="add71-118">Pass på at du aktiverer følgende enhetstilordninger i dobbeltskriving:</span><span class="sxs-lookup"><span data-stu-id="add71-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="add71-119">Overskrift for salgsordre</span><span class="sxs-lookup"><span data-stu-id="add71-119">Sales Order Header</span></span>
- <span data-ttu-id="add71-120">Salgsordredetaljer</span><span class="sxs-lookup"><span data-stu-id="add71-120">Sales Order Details</span></span>
- <span data-ttu-id="add71-121">kontakter</span><span class="sxs-lookup"><span data-stu-id="add71-121">Accounts</span></span>
- <span data-ttu-id="add71-122">Kontakter</span><span class="sxs-lookup"><span data-stu-id="add71-122">Contacts</span></span>
- <span data-ttu-id="add71-123">Produkter</span><span class="sxs-lookup"><span data-stu-id="add71-123">Products</span></span>

<span data-ttu-id="add71-124">Når denne installasjonen er fullført, kan du klargjøre kundeportalmalen.</span><span class="sxs-lookup"><span data-stu-id="add71-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="add71-125">Klargjøre kundeportalen</span><span class="sxs-lookup"><span data-stu-id="add71-125">Provision the Customer portal</span></span>

<span data-ttu-id="add71-126">Før du begynner, må du kontrollere at du allerede har fullført [den nødvendige konfigurasjonen](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="add71-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="add71-127">Deretter følger du disse trinnene for å klargjøre kundeportalen.</span><span class="sxs-lookup"><span data-stu-id="add71-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="add71-128">Gå til [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="add71-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="add71-129">Kontroller at du bruker miljøet der du har aktivert dobbeltskriving.</span><span class="sxs-lookup"><span data-stu-id="add71-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="add71-130">I **Opprett**-kategorien ruller du ned til **Start fra mal**-delen og velger malen som heter **Kundeportal**.</span><span class="sxs-lookup"><span data-stu-id="add71-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="add71-131">Følg instruksjonene på skjermen.</span><span class="sxs-lookup"><span data-stu-id="add71-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="add71-132">Når klargjøringen er fullført, får du tilgang til kundeportalen i **Dine apper**-delen av **Hjem**-siden.</span><span class="sxs-lookup"><span data-stu-id="add71-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="add71-133">Hvis du ikke har installert dobbeltskriveløsningen i miljøet du arbeider i, vil du få en feilmelding, og kundeportalen blir ikke klargjort.</span><span class="sxs-lookup"><span data-stu-id="add71-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="add71-134">Oppdatere kundeportalen</span><span class="sxs-lookup"><span data-stu-id="add71-134">Update the Customer portal</span></span>

<span data-ttu-id="add71-135">Du kan legge til flere funksjoner i kundeportalen senere.</span><span class="sxs-lookup"><span data-stu-id="add71-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="add71-136">Alle endringer som Microsoft gjør i de underliggende løsningskomponentene, vises automatisk i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="add71-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="add71-137">Nettstedet som er klargjort i miljøet ditt, vil imidlertid ikke automatisk gjenspeile endringer som gjøres i konfigurasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="add71-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="add71-138">Du må ta i bruk disse endringene manuelt ved å hente koden fra den nye malen og flette den sammen med det klargjorte nettstedet.</span><span class="sxs-lookup"><span data-stu-id="add71-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="add71-139">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="add71-139">Additional resources</span></span>

<span data-ttu-id="add71-140">Hvis du vil lære hvordan du kan definere og tilpasse kundeportalen, bør du starte med å se gjennom følgende dokumentasjon for den underliggende teknologien:</span><span class="sxs-lookup"><span data-stu-id="add71-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="add71-141">Dokumentasjon for Power Apps-portaler</span><span class="sxs-lookup"><span data-stu-id="add71-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="add71-142">Dokumentasjon for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="add71-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="add71-143">For å administrere portalene effektivt må du forstå Power Apps-portalene og Common Data Service-livssyklusen.</span><span class="sxs-lookup"><span data-stu-id="add71-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="add71-144">Hvis du vil ha mer informasjon, kan du se følgende ressurser:</span><span class="sxs-lookup"><span data-stu-id="add71-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="add71-145">Om portalens livssyklus</span><span class="sxs-lookup"><span data-stu-id="add71-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="add71-146">Oppgradere en portal</span><span class="sxs-lookup"><span data-stu-id="add71-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="add71-147">Overføre en portalkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="add71-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="add71-148">Administrasjon livssyklus for løsning: Dynamics 365 for Customer Engagement-apper</span><span class="sxs-lookup"><span data-stu-id="add71-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
