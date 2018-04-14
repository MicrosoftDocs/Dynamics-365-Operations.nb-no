---
title: "Vanlige spørsmål for Finance and Operations-klienten"
description: "Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for Finance and Operations-klienten."
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6f65b0ea66b4ce876e4a7d1cbf7125b5241c1e20
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="finance-and-operations-client-faq"></a><span data-ttu-id="d07b9-103">Vanlige spørsmål for Finance and Operations-klienten</span><span class="sxs-lookup"><span data-stu-id="d07b9-103">Finance and Operations client FAQ</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d07b9-104">Denne artikkelen gir svar på vanlige spørsmål om Microsoft Dynamics 365 for Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="d07b9-104">This article provides answers to frequently asked questions about the Microsoft Dynamics 365 for Finance and Operations client.</span></span>

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a><span data-ttu-id="d07b9-105">Hvorfor blir ikke symboler lastet inn når jeg bruker Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="d07b9-105">Why aren't symbols loaded when I use Finance and Operations?</span></span>
-----------------------------------------------------------------

<span data-ttu-id="d07b9-106">Sikkerhetsinnstillingene for nettleseren kan hindre at symbolene lastes inn på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="d07b9-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="d07b9-107">Prøv denne fremgangsmåten for å løse dette problemet:</span><span class="sxs-lookup"><span data-stu-id="d07b9-107">To resolve this issue, try the following steps:</span></span>

-   <span data-ttu-id="d07b9-108">Hvis du opplever dette problemet i Internet Explorer, klikker du **Verktøy** og deretter **Alternativer for Internett**.</span><span class="sxs-lookup"><span data-stu-id="d07b9-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span>  <span data-ttu-id="d07b9-109">I dialogboksen Alternativer for Internett i kategorien **Personvern** klikker du **Egendefinert nivå** og kontrollerer at alternativet **Nedlasting av skrifter** er valgt.</span><span class="sxs-lookup"><span data-stu-id="d07b9-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
-   <span data-ttu-id="d07b9-110">Hvis ikke må du kanskje legge til nettstedet for Finance and Operations i listen over klarerte områder.</span><span class="sxs-lookup"><span data-stu-id="d07b9-110">Otherwise, you might have to add the Finance and Operations site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="d07b9-111">Jeg savner båndet fra Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="d07b9-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="d07b9-112">Kan jeg holde fanene i handlingsruten åpne hele tiden?</span><span class="sxs-lookup"><span data-stu-id="d07b9-112">Can I keep Action Pane tabs open all the time?</span></span>
<span data-ttu-id="d07b9-113">Vi planlegger å implementere denne funksjonen snart.</span><span class="sxs-lookup"><span data-stu-id="d07b9-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="d07b9-114">Brukere kan da velge å holde fanene i handlingsruter åpen hele tiden.</span><span class="sxs-lookup"><span data-stu-id="d07b9-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="d07b9-115">Ellers skjules fanene når de ikke er i bruk, slik at det blir mer plass til siden på skjermen.</span><span class="sxs-lookup"><span data-stu-id="d07b9-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="d07b9-116">Hvorfor vises det av og til ulike hurtigmenyer når jeg høyreklikker?</span><span class="sxs-lookup"><span data-stu-id="d07b9-116">Why do I sometimes see different shortcut menus when I right click?</span></span>
<span data-ttu-id="d07b9-117">Hvis du høyreklikker i et redigerbart felt (eller hvis tekst er merket), vises nettleserens hurtigmeny.</span><span class="sxs-lookup"><span data-stu-id="d07b9-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="d07b9-118">Denne menyen gir deg tilgang til kommandoene **Klipp ut**, **Kopier** og **Lim inn**.</span><span class="sxs-lookup"><span data-stu-id="d07b9-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="d07b9-119">Vi kan ikke bygge inn disse kommandoene på hurtigmenyene i Finance and Operations fordi nettlesere av sikkerhetsmessige årsaker ikke gir oss programmatisk tilgang til utklippstavlen i systemet.</span><span class="sxs-lookup"><span data-stu-id="d07b9-119">We can't embed these commands into the Finance and Operations shortcut menus because, for security reasons, browsers don’t allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="d07b9-120">Hvis du høyreklikker en feltetikett eller verdien til en skrivebeskyttet kontroll, vises hurtigmenyen for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d07b9-120">If you right-click a field label or the value of a read-only control, you'll see the Finance and Operations shortcut menu.</span></span>

<span data-ttu-id="d07b9-121">For å gjøre tastaturtilgang enklere planlegger vi å implementere en hurtigtast som åpner hurtigmenyen for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d07b9-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the Finance and Operations shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a><span data-ttu-id="d07b9-122">Hvor er funksjonen Vis detaljer i Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="d07b9-122">Where is the View details functionality in Finance and Operations?</span></span>
<span data-ttu-id="d07b9-123">Alternativet **Vis detaljer** er tilgjengelig på ulike måter:</span><span class="sxs-lookup"><span data-stu-id="d07b9-123">The **View details** option is available in a couple of ways:</span></span>

-   <span data-ttu-id="d07b9-124">Hvis en kontroll har **Vis detaljer**-funksjonalitet, og hvis kontrollen har en verdi, vises denne verdien som en hyperkobling.</span><span class="sxs-lookup"><span data-stu-id="d07b9-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="d07b9-125">Du kan klikke hyperkoblingen for å åpne en side som inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="d07b9-125">You can click the hyperlink to open a page that contains additional details.</span></span>
-   <span data-ttu-id="d07b9-126">**Vis detaljer** er også et alternativ på hurtigmenyer for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d07b9-126">**View details** is also an option on Finance and Operations shortcut menus.</span></span> <span data-ttu-id="d07b9-127">Hvis du vil ha mer informasjon om når hurtigmenyer for Finance and Operations vises når du høyreklikker, kan du se den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="d07b9-127">For more information about when Finance and Operations shortcut menus are displayed when you right-click, see the previous section.</span></span>





