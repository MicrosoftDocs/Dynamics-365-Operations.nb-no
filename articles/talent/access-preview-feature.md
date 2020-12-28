---
title: Behandle funksjoner
description: Dette emnet beskriver hvordan en administrator kan aktivere forhåndsvisningsfunksjonene i Microsoft Dynamics 365 Talent, og det viser hvilke funksjoner som er aktivert for forhåndsvisning.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.1.0, Talent
ms.openlocfilehash: d818e9e04ce88e5ab285ef8176334809447fb477
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462165"
---
# <a name="manage-features"></a><span data-ttu-id="4f3ea-103">Behandle funksjoner</span><span class="sxs-lookup"><span data-stu-id="4f3ea-103">Manage features</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f3ea-104">Som en del av vår kontinuerlige distribusjonen av funksjonalitet for administrasjon av menneskelig kapital (HCM) for Microsoft Dynamics 365 Human Resources vil vi at kunder får nye funksjoner så snart som mulig.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-104">As part of our continuous rollout of human capital management (HCM) capabilities for Microsoft Dynamics 365 Human Resources, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="4f3ea-105">Administratorer kan se og bruke forhåndsvisning av funksjoner i miljøet.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="4f3ea-106">Disse funksjonene er nesten klar for generelle tilgjengeligheten og har gjennomgått omfattende testing.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="4f3ea-107">Vi er bare ute etter en endelig runde med tilbakemelding og godkjenning før vi gjør dem generelt tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-107">We're just looking for a final round of customer feedback and validation before we release them for general availability.</span></span>

<span data-ttu-id="4f3ea-108">Dette emnet beskriver hvordan du kan aktivere forhåndsvisningsfunksjonene, og det viser hvilke funksjoner som er tilgjengelige for forhåndsvisning.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-108">This topic describes how you can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="4f3ea-109">Denne listen oppdateres etter funksjoner som er frigitt til generelle tilgjengeligheten og nye funksjoner som utgis for å forhåndsvise.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="4f3ea-110">Det gis ingen varsling når nye funksjoner er frigitt til å forhåndsvise.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="4f3ea-111">Brukere starter bare for å se funksjonene.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-111">Users will just start to see the features.</span></span> <span data-ttu-id="4f3ea-112">Hvis du vil ha mer informasjon om nye funksjoner i Talent, kan du se [Hva er nytt eller endret i Dynamics 365 Talent](./whats-new.md) og [Produktmerknader for Dynamics 365 og Power Platform](https://docs.microsoft.com/business-applications-release-notes).</span><span class="sxs-lookup"><span data-stu-id="4f3ea-112">For more information about new features in Talent, see [What's new or changed in Dynamics 365 Talent](./whats-new.md) and [Dynamics 365 and Power Platform Release Notes](https://docs.microsoft.com/business-applications-release-notes).</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="4f3ea-113">Aktivere eller deaktivere forhåndsvisning av funksjoner</span><span class="sxs-lookup"><span data-stu-id="4f3ea-113">Enable or disable preview features</span></span>

<span data-ttu-id="4f3ea-114">Hvis du vil ha tilgang til forhåndsvisningsfunksjoner, må du først aktivere dem i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-114">To access preview features, you must first enable them in your environment.</span></span> <span data-ttu-id="4f3ea-115">Aktivering eller deaktivering av forhåndsvisningsfunksjoner er miljøspesifikt.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-115">Enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f3ea-116">Når du aktiverer innstillingen **Forhåndsvisningsfunksjoner**, aktiverer du forhåndsvisningsfunksjoner for alle brukere i organisasjonen som er i miljøet.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-116">When you turn on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="4f3ea-117">Når du deaktiverer innstillingen, kan du deaktivere forhåndsvisningsfunksjoner og gjøre dem utilgjengelig for brukerne.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-117">When you turn off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="4f3ea-118">Forhåndsvisningsfunksjoner har begrenset støtte i Talent.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="4f3ea-119">Du kan bruke færre personvern- og sikkerhetstiltak, og de er ikke inkludert i Talent-servicenivåavtalen (SLA).</span><span class="sxs-lookup"><span data-stu-id="4f3ea-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement (SLA).</span></span> <span data-ttu-id="4f3ea-120">Du bør ikke bruke forhåndsvisningsfunksjoner til å behandle personlige data (det vil si all informasjon som kan identifisere deg), eller til å behandle andre data som er gjenstand for juridiske eller samsvarskrav.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="attract"></a><span data-ttu-id="4f3ea-121">Attract</span><span class="sxs-lookup"><span data-stu-id="4f3ea-121">Attract</span></span>

1. <span data-ttu-id="4f3ea-122">Logg på Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-122">Sign in to Microsoft Dynamics 365 Talent: Attract.</span></span>
2. <span data-ttu-id="4f3ea-123">På **Oppsett**-menyen (tannhjulssymbolet) i øvre høyre hjørne, velg **Administrasjonssenter**.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-123">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span>
3. <span data-ttu-id="4f3ea-124">På fanen **Funksjonsbehandling** velger du alternativet ved siden av **Forhåndsvisningsfunksjoner**, slik at det blir blått og viser **På**.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-124">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue and says **On**.</span></span>

    ![Aktivere forhåndsvisningsfunksjoner i Attract](./media/attract-enable-preview-features.png)

4. <span data-ttu-id="4f3ea-126">Velg eller avbryt valget av individuelle forhåndsvisningsfunksjoner.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-126">Select or cancel the selection of individual preview features.</span></span> <span data-ttu-id="4f3ea-127">Hvis du ikke gjør noe, aktiveres alle tilgjengelige forhåndsvisningsfunksjoner.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-127">If you do nothing, all available preview features are enabled.</span></span>
5. <span data-ttu-id="4f3ea-128">Oppdater nettleseren for å begynne å se de nye funksjonene.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-128">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="4f3ea-129">Alle brukere som allerede er pålogget, ser funksjonene neste gang de logger på, eller de kan oppdatere nettleseren for å vise funksjonene umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-129">Any users who are already signed in will see the features the next time they sign in, or they can refresh their browser to see the features immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="4f3ea-130">Noen forhåndsvisningsfunksjoner kan kreve ekstra konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-130">Some preview features might require additional configuration.</span></span> <span data-ttu-id="4f3ea-131">Følg koblingene ved siden av forhåndsvisningsfunksjonen for å fullføre oppsettet av den.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-131">Follow the links next to the preview feature to complete the setup for it.</span></span>

## <a name="feedback"></a><span data-ttu-id="4f3ea-132">Tilbakemelding</span><span class="sxs-lookup"><span data-stu-id="4f3ea-132">Feedback</span></span>

<span data-ttu-id="4f3ea-133">Vi hører gjerne fra deg om din erfaring med noen av disse forhåndsvisningsfunksjonene.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-133">We want to hear from you about your experience with any of these preview features.</span></span> <span data-ttu-id="4f3ea-134">Vi oppfordrer deg til å postere regelmessig tilbakemelding på følgende områder når du bruker denne eller andre funksjoner:</span><span class="sxs-lookup"><span data-stu-id="4f3ea-134">We encourage you to regularly post your feedback on the following sites as you use these or any other features:</span></span>

- <span data-ttu-id="4f3ea-135">[Fellesskap](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – dette området er en flott ressurs der brukere kan diskutere brukstilfeller, spørsmål og få hjelp til fellesskapet.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-135">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="4f3ea-136">Gi oss beskjed om funksjoner du vil se i produktet, eller si fra om eventuelle endringer du mener vi bør gjøre i eksisterende funksjoner.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-136">Let us know about features that you want to see in the product, or let us know about any changes you think we should make to existing features.</span></span> <span data-ttu-id="4f3ea-137">Foreslå produktideer på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="4f3ea-137">Suggest product ideas on the following sites:</span></span>

    - [<span data-ttu-id="4f3ea-138">Attract-ideer</span><span class="sxs-lookup"><span data-stu-id="4f3ea-138">Attract ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="4f3ea-139">Onboard-ideer</span><span class="sxs-lookup"><span data-stu-id="4f3ea-139">Onboard ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

<span data-ttu-id="4f3ea-140">Sørg for at du ikke tar med personlige data (informasjon som kan identifisere deg) i tilbakemeldingene eller innsendingene av produktgjennomgang.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-140">Make sure that you don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="4f3ea-141">Innsamlet informasjon kan analyseres ytterligere, og den brukes ikke til å svare på forespørsler under gjeldende personvernlover.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-141">Collected information might be analyzed further and isn't used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="4f3ea-142">Personopplysninger som samles inn separat under disse programmene, er underlagt [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="4f3ea-142">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="4f3ea-143">Bokmerk dette emnet, og kom deretter tilbake ofte for å holde deg oppdatert om nye forhåndsvisningsfunksjoner etter hvert som vi gir dem ut.</span><span class="sxs-lookup"><span data-stu-id="4f3ea-143">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f3ea-144">Se også</span><span class="sxs-lookup"><span data-stu-id="4f3ea-144">See also</span></span>

- [<span data-ttu-id="4f3ea-145">Prøv eller kjøp Talent-apper</span><span class="sxs-lookup"><span data-stu-id="4f3ea-145">Try or buy Talent apps</span></span>](https://dynamics.microsoft.com/talent/overview/)
- [<span data-ttu-id="4f3ea-146">Hva er nytt eller endret i Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="4f3ea-146">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="4f3ea-147">Lanseringsplaner</span><span class="sxs-lookup"><span data-stu-id="4f3ea-147">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="4f3ea-148">Få kundestøtte for Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="4f3ea-148">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
