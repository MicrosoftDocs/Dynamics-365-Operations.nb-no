---
title: Bygge inn tredjepartsapper
description: Dette emnet forklarer hvordan du bygger inn tredjepartsapper for å øke produktets funksjonalitet.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d348683e0a2ed35f26830a6ce05c0bf9ca5970bd
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944850"
---
# <a name="embed-third-party-apps"></a><span data-ttu-id="54354-103">Bygge inn tredjepartsapper</span><span class="sxs-lookup"><span data-stu-id="54354-103">Embed third-party apps</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="54354-104">Mange kunder bruker en rekke programmer for å drive virksomheten sin.</span><span class="sxs-lookup"><span data-stu-id="54354-104">Many customers use a range of applications to run their business.</span></span> <span data-ttu-id="54354-105">Noen av disse programmene er tredjepartswebapper som fungerer sammen med Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="54354-105">Some of those applications are third-party web apps that work in conjunction with Finance and Operations apps.</span></span> <span data-ttu-id="54354-106">For å gi en mer sømløs brukeropplevelse kan du bruke funksjonen **Helside-apper (forhåndsvisning)** til å bygge inn disse tredjepartsappene direkte i Finance and Operations-appene dine (forutsatt at tredjepartsappene tillater at de legges inn).</span><span class="sxs-lookup"><span data-stu-id="54354-106">To provide a more seamless user experience, you can use the **(Preview) Full page apps** feature to embed those third-party apps directly into your Finance and Operations apps (provided that the third-party apps allow themselves to be embedded).</span></span> <span data-ttu-id="54354-107">På denne måten kan brukere få tilgang til webområder og apper som de krever, uten at de behøver å bytte kategorier eller vinduer.</span><span class="sxs-lookup"><span data-stu-id="54354-107">In this way, users can access the websites and apps that they require without having to switch tabs or windows.</span></span>

<span data-ttu-id="54354-108">Før du kan bygge inn tredjepartsapper i produktet, må du aktivere funksjonen **Helside-apper (forhåndsvisning)** i Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="54354-108">Before you can embed third-party apps into the product, you must turn on the **(Preview) Full page apps** feature in Feature management.</span></span> <span data-ttu-id="54354-109">Deretter kan du bruke en av følgende metoder til å bygge inn en tredjepartsapp eller et webområde.</span><span class="sxs-lookup"><span data-stu-id="54354-109">You can then use one of the following methods to embed a third-party app or website.</span></span> <span data-ttu-id="54354-110">Disse metodene er analoge til metodene som brukes til å bygge inn lerretsapper fra Microsoft Power Apps til Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="54354-110">These methods are analogous to the methods that are used to embed canvas apps from Microsoft Power Apps into Finance and Operations apps.</span></span>

- <span data-ttu-id="54354-111">Bygg inn appen eller webområdet på en eksisterende side som en ny kategoriside (pivotfane, hurtigfane, blad eller arbeidsområde).</span><span class="sxs-lookup"><span data-stu-id="54354-111">Embed the app or website on an existing page as a new tab page (pivot tab, FastTab, blade, or workspace section).</span></span>
- <span data-ttu-id="54354-112">Opprett en ny fullsideopplevelse for appen eller webområdet fra instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="54354-112">Create a new full-page experience for the app or website from the dashboard.</span></span>

## <a name="embed-a-website-on-an-existing-page"></a><span data-ttu-id="54354-113">Bygge inn et webområde på en eksisterende side</span><span class="sxs-lookup"><span data-stu-id="54354-113">Embed a website on an existing page</span></span>

<span data-ttu-id="54354-114">Bruk denne fremgangsmåten hvis du vil supplere en eksisterende side i systemet med en innebygd app.</span><span class="sxs-lookup"><span data-stu-id="54354-114">Use this procedure if you want to supplement an existing page in the system with an embedded app.</span></span>

1. <span data-ttu-id="54354-115">Åpne siden der du vil bygge inn appen.</span><span class="sxs-lookup"><span data-stu-id="54354-115">Open the page where you want to embed the app.</span></span>
2. <span data-ttu-id="54354-116">Åpne **Legg til en app**-ruten:</span><span class="sxs-lookup"><span data-stu-id="54354-116">Open the **Add an app** pane:</span></span>

    1. <span data-ttu-id="54354-117">Velg **Innstillinger** og deretter **Tilpass** for å åpne **Tilpassing**-verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="54354-117">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
    2. <span data-ttu-id="54354-118">Velg **Mer \> Legg til en app**.</span><span class="sxs-lookup"><span data-stu-id="54354-118">Select **More \> Add an app**.</span></span>

3. <span data-ttu-id="54354-119">Velg området på siden der du vil legge til appen.</span><span class="sxs-lookup"><span data-stu-id="54354-119">Select the region of the page where you want to add the app.</span></span> <span data-ttu-id="54354-120">Dette området må være en *kategoricontainer* for en pivotfane, hurtigfane, et blad eller et arbeidsområde.</span><span class="sxs-lookup"><span data-stu-id="54354-120">This region must be a *tab container* for a pivot tab, FastTab, blade, or workspace section.</span></span>
4. <span data-ttu-id="54354-121">Velg **webområde**.</span><span class="sxs-lookup"><span data-stu-id="54354-121">Select **Website**.</span></span>
5. <span data-ttu-id="54354-122">Konfigurer den innebygde appen:</span><span class="sxs-lookup"><span data-stu-id="54354-122">Configure the embedded app:</span></span>

    - <span data-ttu-id="54354-123">**Navn** – Angi teksten som skal vises for kategorien som inneholder den innebygde appen.</span><span class="sxs-lookup"><span data-stu-id="54354-123">**Name** – Enter the text that should be shown for the tab that contains the embedded app.</span></span> <span data-ttu-id="54354-124">Ofte vil du at denne teksten skal være navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="54354-124">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="54354-125">**URL-adresse** – Angi plasseringen for appen.</span><span class="sxs-lookup"><span data-stu-id="54354-125">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="54354-126">Av sikkerhetsmessige årsaker må URL-adressen bruke HTTPS (Hypertext Transfer Protocol Secure).</span><span class="sxs-lookup"><span data-stu-id="54354-126">For security reasons, the URL must use Hypertext Transfer Protocol Secure (HTTPS).</span></span>
    > - <span data-ttu-id="54354-127">Appen eller webområdet må konfigureres slik at selve appen kan bygges inn.</span><span class="sxs-lookup"><span data-stu-id="54354-127">The app or website must be configured to allow itself to be embedded.</span></span>

6. <span data-ttu-id="54354-128">Velg **Lagre** for å bygge inn appen på siden.</span><span class="sxs-lookup"><span data-stu-id="54354-128">Select **Save** to embed the app on the page.</span></span> <span data-ttu-id="54354-129">Appen legges til som den siste kategorien eller delen i gruppen.</span><span class="sxs-lookup"><span data-stu-id="54354-129">The app is added as the last tab or section in the group.</span></span>
7. <span data-ttu-id="54354-130">Bekreft at appen vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="54354-130">Confirm that the app appears as expected.</span></span> <span data-ttu-id="54354-131">Hvis appen ikke vises, kan du se delen [Feilsøking](#troubleshooting) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="54354-131">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>
8. <span data-ttu-id="54354-132">Åpne visningsvelgeren, og velg enten **Lagre** (hvis appen skal knyttes til gjeldende visning) eller **Lagre som** (for å lagre appen i en annen visning).</span><span class="sxs-lookup"><span data-stu-id="54354-132">Open the view selector, and select either **Save** (if the app should be associated with the current view) or **Save as** (to save the app to a different view).</span></span>

    <span data-ttu-id="54354-133">Hvis siden ikke har en visningsvelger (for eksempel hvis siden er en dialogboks eller et arbeidsområde), kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="54354-133">If the page doesn't have a view selector (for example, if the page is a dialog box or a workspace), you can skip this step.</span></span>

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a><span data-ttu-id="54354-134">Bygge inn et webområde som en helsideopplevelse fra instrumentbordet</span><span class="sxs-lookup"><span data-stu-id="54354-134">Embed a website as a full-page experience from the dashboard</span></span>

<span data-ttu-id="54354-135">Bruk denne fremgangsmåten hvis appen du vil bygge inn, ikke er relatert til en eksisterende side, eller hvis du bare vil ha en helsideopplevelse for appen i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="54354-135">Use this procedure if the app that you want to embed isn't related to an existing page, or if you just want a full-page experience for the app inside the Finance and Operations app.</span></span>

1. <span data-ttu-id="54354-136">Åpne instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="54354-136">Open the dashboard.</span></span>
2. <span data-ttu-id="54354-137">Velg og hold siden nede (eller høyreklikk), velg **Tilpass**, og velg deretter **Legg til en side**.</span><span class="sxs-lookup"><span data-stu-id="54354-137">Select and hold (or right-click) the page, select **Personalize**, and then select **Add a page**.</span></span>
3. <span data-ttu-id="54354-138">I ruten **Legg til en side** klikker du **Nettsted**.</span><span class="sxs-lookup"><span data-stu-id="54354-138">In the **Add a page** pane, select **Website**.</span></span>
4. <span data-ttu-id="54354-139">Konfigurer den innebygde appen:</span><span class="sxs-lookup"><span data-stu-id="54354-139">Configure the embedded app:</span></span>

    - <span data-ttu-id="54354-140">**Navn** – Angi teksten som skal vises på brikken som er lagt til for den innebygde appen i instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="54354-140">**Name** – Enter the text that should be shown on the tile that is added for the embedded app on the dashboard.</span></span> <span data-ttu-id="54354-141">Ofte vil du at denne teksten skal være navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="54354-141">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="54354-142">**URL-adresse** – Angi plasseringen for appen.</span><span class="sxs-lookup"><span data-stu-id="54354-142">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="54354-143">Av sikkerhetsmessige årsaker må URL-adressen bruke HTTPS.</span><span class="sxs-lookup"><span data-stu-id="54354-143">For security reasons, the URL must use HTTPS.</span></span>
    > - <span data-ttu-id="54354-144">Appen eller webområdet må konfigureres slik at selve appen kan bygges inn.</span><span class="sxs-lookup"><span data-stu-id="54354-144">The app or website must be configured to allow itself to be embedded.</span></span>

5. <span data-ttu-id="54354-145">Velg **Lagre** for å legge til appen på instrumentbordet som en ny flis.</span><span class="sxs-lookup"><span data-stu-id="54354-145">Select **Save** to add the app to the dashboard as a new tile.</span></span>
6. <span data-ttu-id="54354-146">Velg den nye flisen på instrumentbordet, og bekreft at appen vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="54354-146">Select the new tile on the dashboard, and confirm that the app appears as expected.</span></span> <span data-ttu-id="54354-147">Hvis appen ikke vises, kan du se delen [Feilsøking](#troubleshooting) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="54354-147">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>

## <a name="sharing-embedded-apps"></a><span data-ttu-id="54354-148">Dele innebygde apper</span><span class="sxs-lookup"><span data-stu-id="54354-148">Sharing embedded apps</span></span>

<span data-ttu-id="54354-149">Når du har bygd inn en app ved hjelp av en av metodene som er beskrevet i de forrige delene, kan det hende at du vil dele visningen med andre brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="54354-149">After you've embedded an app by using one of the methods that are described in the previous sections, you might want to share the view with other users in the system.</span></span> <span data-ttu-id="54354-150">Du kan dele en innebygd app på en av følgende måter:</span><span class="sxs-lookup"><span data-stu-id="54354-150">To share an embedded app, use one of the following methods:</span></span>

- <span data-ttu-id="54354-151">**Publiser visningen (anbefales):** Hvis den innebygde appen er lagret i en visning, er den anbefalte og foretrukne måten å dele den på å publisere visningen til brukere som har de riktige sikkerhetsrollene.</span><span class="sxs-lookup"><span data-stu-id="54354-151">**Publish the view (Recommended):** If the embedded app has been saved to a view, the recommended and preferred way to share it is to publish the view to users who have the appropriate security roles.</span></span> <span data-ttu-id="54354-152">Da vil alle brukere som har sikkerhetsroller som er målrettet av den publiserte visningen, se appen i Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="54354-152">Then, all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> <span data-ttu-id="54354-153">Hvis du vil ha mer informasjon om hvordan du publiserer en visning, kan du se [Publisere visninger](saved-views.md#publishing-views).</span><span class="sxs-lookup"><span data-stu-id="54354-153">For more information about how to publish a view, see [Publishing views](saved-views.md#publishing-views).</span></span>

    <span data-ttu-id="54354-154">Du kan også publisere en app som er innebygd som en helsideopplevelse fra instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="54354-154">You can also publish an app that has been embedded as a full-page experience from the dashboard.</span></span> <span data-ttu-id="54354-155">Velg og hold (eller høyreklikk) flisen som er tilknyttet appen, på instrumentbordet, velg **Tilpass**, og velg deretter **Publiser side**.</span><span class="sxs-lookup"><span data-stu-id="54354-155">On the dashboard, select and hold (or right-click) the tile that is associated with the app, select **Personalize**, and then select **Publish page**.</span></span> <span data-ttu-id="54354-156">For øyeblikket kan du bare publisere sikkerhetsroller.</span><span class="sxs-lookup"><span data-stu-id="54354-156">Currently, you can publish only to security roles.</span></span> <span data-ttu-id="54354-157">Muligheten til å publisere til juridiske enheter vil imidlertid vanligvis bli lagt til før funksjonen blir tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="54354-157">However, the capability to publish to legal entities will be added before the feature becomes generally available.</span></span>

- <span data-ttu-id="54354-158">**Kopier tilpasningen:** For sider som ikke støtter visninger (for eksempel dialogbokser eller arbeidsområder), eller for helsideapperfaring, kan du kopiere tilpasningen til de aktuelle brukerne.</span><span class="sxs-lookup"><span data-stu-id="54354-158">**Copy the personalization:** For pages that don't support views (for example, dialog boxes or workspaces), or for the full-page app experience, you can copy the personalization to the appropriate users.</span></span> <span data-ttu-id="54354-159">Hvis du vil ha mer informasjon, kan du se [Dele tilpasninger](personalize-user-experience.md#sharing-personalizations).</span><span class="sxs-lookup"><span data-stu-id="54354-159">For more information, see [Sharing personalizations](personalize-user-experience.md#sharing-personalizations).</span></span>

## <a name="viewing-embedded-apps"></a><span data-ttu-id="54354-160">Vise innebygde apper</span><span class="sxs-lookup"><span data-stu-id="54354-160">Viewing embedded apps</span></span>

<span data-ttu-id="54354-161">Hvis du vil vise en innebygd app på en side i Finance and Operations-apper, åpner du siden med den innebygde appen.</span><span class="sxs-lookup"><span data-stu-id="54354-161">To view an embedded app on a page in Finance and Operations apps, open the page that has the embedded app.</span></span> <span data-ttu-id="54354-162">Husk at innebygde apper på noen sider kan åpnes ved hjelp av **Power Apps**-knappen i standardhandlingsruten.</span><span class="sxs-lookup"><span data-stu-id="54354-162">Remember that, on some pages, embedded apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="54354-163">De kan også vises direkte på siden som en ny fane, hurtigfane eller et blad eller som en ny inndeling i et arbeidsområde.</span><span class="sxs-lookup"><span data-stu-id="54354-163">Alternatively, they might appear directly on the page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

## <a name="editing-or-removing-embedded-apps"></a><span data-ttu-id="54354-164">Redigere eller fjerne innebygde apper</span><span class="sxs-lookup"><span data-stu-id="54354-164">Editing or removing embedded apps</span></span>

<span data-ttu-id="54354-165">Når en app er innebygd på en side, kan det hende at du må redigere konfigurasjonen (for eksempel ved å endre deletiketten eller URL-adressen).</span><span class="sxs-lookup"><span data-stu-id="54354-165">After an app has been embedded on a page, you might have to edit its configuration (for example, by changing the section label or the URL).</span></span> <span data-ttu-id="54354-166">Det kan også hende at du må fjerne den fra siden.</span><span class="sxs-lookup"><span data-stu-id="54354-166">Alternatively, you might have to remove it from the page.</span></span> <span data-ttu-id="54354-167">Bruk en av fremgangsmåtene nedenfor for å redigere konfigurasjonen av en innebygd app eller fjerne den helt.</span><span class="sxs-lookup"><span data-stu-id="54354-167">Use one of the following procedures to edit the configuration of an embedded app or remove it completely.</span></span>

### <a name="apps-that-are-embedded-on-existing-pages"></a><span data-ttu-id="54354-168">Apper som er innebygd på eksisterende sider</span><span class="sxs-lookup"><span data-stu-id="54354-168">Apps that are embedded on existing pages</span></span>

1. <span data-ttu-id="54354-169">Åpne siden der appen er innebygd.</span><span class="sxs-lookup"><span data-stu-id="54354-169">Open the page where the app is embedded.</span></span>
2. <span data-ttu-id="54354-170">Velg **Innstillinger** og deretter **Tilpass** for å åpne **Tilpassing**-verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="54354-170">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
3. <span data-ttu-id="54354-171">Velg **Valg**-verktøyet, og velg deretter den innebygde appen.</span><span class="sxs-lookup"><span data-stu-id="54354-171">Select the **Select** tool, and then select the embedded app.</span></span>
4. <span data-ttu-id="54354-172">Hvis du vil redigere appen, gjør du de nødvendige endringene i konfigurasjonen og velger deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="54354-172">To edit the app, make the required changes to its configuration, and then select **Save**.</span></span>

    <span data-ttu-id="54354-173">Du kan også fjerne appen ved å velge **Slett**.</span><span class="sxs-lookup"><span data-stu-id="54354-173">Alternatively, to remove the app, select **Delete**.</span></span>

5. <span data-ttu-id="54354-174">Lagre eller publisere visningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="54354-174">Re-save or republish the view.</span></span> <span data-ttu-id="54354-175">Vær oppmerksom på at hvis du går ut av siden uten å lagre visningen eksplisitt, blir ingen av handlingene du utførte i **Rediger nettsted**-ruten, opprettholdt.</span><span class="sxs-lookup"><span data-stu-id="54354-175">Note that if you leave the page without explicitly saving the view, none of the actions that you performed in the **Edit website** pane will be maintained.</span></span>

### <a name="apps-that-are-embedded-from-the-dashboard"></a><span data-ttu-id="54354-176">Apper som er innebygd fra instrumentbordet</span><span class="sxs-lookup"><span data-stu-id="54354-176">Apps that are embedded from the dashboard</span></span>

1. <span data-ttu-id="54354-177">Åpne instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="54354-177">Open the dashboard.</span></span>
2. <span data-ttu-id="54354-178">Velg og hold (eller høyreklikk) flisen som er tilknyttet den innebygde appen, velg deretter **Tilpass**.</span><span class="sxs-lookup"><span data-stu-id="54354-178">Select and hold (or right-click) the tile that is associated with the embedded app, and then select **Personalize**.</span></span>
3. <span data-ttu-id="54354-179">Hvis du vil redigere appen, velger du **Rediger side**.</span><span class="sxs-lookup"><span data-stu-id="54354-179">To edit the app, select **Edit page**.</span></span> <span data-ttu-id="54354-180">I ruten **Rediger nettsted** gjør du de nødvendige endringene i appkonfigurasjonen og velger deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="54354-180">In the **Edit website** pane, make the required changes to the app configuration, and then select **Save**.</span></span>

    <span data-ttu-id="54354-181">Du kan også fjerne appen ved å velge **Fjern side**.</span><span class="sxs-lookup"><span data-stu-id="54354-181">Alternatively, to remove the app, select **Remove page**.</span></span>

## <a name="appendix"></a><span data-ttu-id="54354-182">Tillegg</span><span class="sxs-lookup"><span data-stu-id="54354-182">Appendix</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="54354-183">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="54354-183">Troubleshooting</span></span>

<span data-ttu-id="54354-184">Hvis et nettsted ikke blir gjengitt riktig etter at den er innebygd i en Finance and Operations-app, eller hvis du får en feilmelding som angir at URLen ble nektet en tilkobling, konfigureres webområdet sannsynligvis for å hindre at det ikke blir innebygd i en iframe.</span><span class="sxs-lookup"><span data-stu-id="54354-184">If a website isn't rendered correctly after it's embedded in a Finance and Operation app, or if you receive an error message that states that the URL was denied a connection, the website is probably configured to prevent itself from being embedded in an iframe.</span></span> <span data-ttu-id="54354-185">Følg denne fremgangsmåten for å finne ut om webområdet kan bygges inn.</span><span class="sxs-lookup"><span data-stu-id="54354-185">Follow these steps to determine whether the website can be embedded.</span></span>

1. <span data-ttu-id="54354-186">Åpne utviklerverktøyene for webleseren du bruker.</span><span class="sxs-lookup"><span data-stu-id="54354-186">Open the developer tools for the browser that you're using.</span></span>
2. <span data-ttu-id="54354-187">Finn og velg svar fra det innebygde området i fanen **Nettverk**.</span><span class="sxs-lookup"><span data-stu-id="54354-187">On the **Network** tab, find and select the response from the embedded site.</span></span>
3. <span data-ttu-id="54354-188">Se etter **alternativer for x-frame** i fanen **Svarhoder** i kategorien **Hoder**.</span><span class="sxs-lookup"><span data-stu-id="54354-188">On the **Headers** tab, under **Response Headers**, look for **x-frame-options**.</span></span> <span data-ttu-id="54354-189">Hvis **alternativer for x-frame** finnes i svarhodene og har verdien **DENY** eller **SAMEORIGIN**, kan webområdet ikke bygges inn på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="54354-189">If **x-frame-options** exists in the response headers, and has a value of **DENY** or **SAMEORIGIN**, the website can't currently be embedded.</span></span> <span data-ttu-id="54354-190">Du må samarbeide med eieren av appen for å gjøre det mulig å bygge den inn på en trygg måte.</span><span class="sxs-lookup"><span data-stu-id="54354-190">You will have to work with the owner of the app to enable it to be safely embedded.</span></span>

### <a name="developer-modeling-a-website-on-a-form"></a><span data-ttu-id="54354-191">[Utvikler] Modellere et webområde på et skjema</span><span class="sxs-lookup"><span data-stu-id="54354-191">[Developer] Modeling a website on a form</span></span>

<span data-ttu-id="54354-192">Selv om dette emnet har fokus på å bygge inn tredjepartsapper eller webområder gjennom tilpasning, kan utviklerne også bygge dem inn i et skjema ved hjelp av Visual Studio-utviklingserfaringen.</span><span class="sxs-lookup"><span data-stu-id="54354-192">Although this topic is focused on embedding third-party apps or websites through personalization, developers can also embed them in a form by using the Visual Studio development experience.</span></span> <span data-ttu-id="54354-193">Du kan bare legge til en **WebsiteHostControl**-kontroll i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="54354-193">Just add a **WebsiteHostControl** control to the form.</span></span> <span data-ttu-id="54354-194">Metadataegenskapene som er tilgjengelige for kontrollen, har de samme egenskapene som tilpasningserfaringen.</span><span class="sxs-lookup"><span data-stu-id="54354-194">The metadata properties that are available for the control provide the same capabilities as the personalization experience.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]