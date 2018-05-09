---
title: "Vise sider side ved side ved å bruke ikonet Åpne i nytt vindu"
description: Denne artikkelen beskriver hvordan du viser sider side-ved-side i Microsoft Dynamics 365 for Finance and Operations.
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b0ffd313e0f1d50f35235d3a48f8715bb6c8de7b
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a><span data-ttu-id="e86ed-103">Vise sider side ved side ved å bruke ikonet Åpne i nytt vindu</span><span class="sxs-lookup"><span data-stu-id="e86ed-103">Display pages side-by-side using the Open in New Window icon</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e86ed-104">Denne artikkelen beskriver hvordan du viser sider side-ved-side i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e86ed-104">This article explains how to display pages side-by-side in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="e86ed-105">Microsoft Dynamics 365 for Finance and Operations kan gjøre det enklere å utføre oppgaver på en effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="e86ed-105">Microsoft Dynamics 365 for Finance and Operations helps you perform tasks efficiently.</span></span> <span data-ttu-id="e86ed-106">I noen tilfeller vil du kanskje vise flere sider side ved side for å fullføre en oppgave raskt.</span><span class="sxs-lookup"><span data-stu-id="e86ed-106">In some cases, you may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="e86ed-107">Du vil for eksempel kanskje validere eller registrere linjer i flere journaler.</span><span class="sxs-lookup"><span data-stu-id="e86ed-107">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="e86ed-108">Vanligvis vil du måtte gå frem og tilbake mellom siden som viser en liste over journaler, og siden som viser linjer for en bestemt journal.</span><span class="sxs-lookup"><span data-stu-id="e86ed-108">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="e86ed-109">Funksjonen **Åpne i nytt vindu** gjør at du kan vise disse sidene side ved side, slik at du kan gjøre oppgavene raskt.</span><span class="sxs-lookup"><span data-stu-id="e86ed-109">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span> 

<span data-ttu-id="e86ed-110">La oss fortsette med eksemplet ovenfor. Når du viser linjene, kan du klikke ikonet **Åpne i nytt vindu**.</span><span class="sxs-lookup"><span data-stu-id="e86ed-110">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span> 

<span data-ttu-id="e86ed-111">[![åpne-i-nytt-vindu-ikon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="e86ed-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span> 

<span data-ttu-id="e86ed-112">Når du klikker ikonet **Åpne i nytt vindu**, åpnes linjesiden i et nytt popup-nettleservindu, og det opprinnelige nettleservinduet navigeres tilbake i historikken til siden der listen over journaler vises.</span><span class="sxs-lookup"><span data-stu-id="e86ed-112">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="e86ed-113">Du kan dermed vise begge sidene side ved side.</span><span class="sxs-lookup"><span data-stu-id="e86ed-113">You can then display both pages side-by-side.</span></span> <span data-ttu-id="e86ed-114">Når du er ferdig med å vise en journal, kan du endre den valgte journalen på journallistesiden, og dermed vises linjene i den nylig valgte journalen automatisk på linjesiden i popup-vinduet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-114">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span> 

<span data-ttu-id="e86ed-115">[![sider-vist-side-om-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="e86ed-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span> 

<span data-ttu-id="e86ed-116">Den dynamiske koblingen og oppdateringen skjer på grunn av relasjonene mellom dataene som ligger bak disse sidene.</span><span class="sxs-lookup"><span data-stu-id="e86ed-116">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="e86ed-117">Hvis systemet ikke er klar over relasjonen mellom dataene, oppdateres ikke popup-vinduet automatisk som svar på en endring i vinduet det stammer fra.</span><span class="sxs-lookup"><span data-stu-id="e86ed-117">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span> 

<span data-ttu-id="e86ed-118">Noen sider har flere visninger, for eksempel Rutenettvisning, Topptekstvisning og Detaljvisning.</span><span class="sxs-lookup"><span data-stu-id="e86ed-118">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="e86ed-119">Ikonet **Åpne i nytt vindu** fører til at hele siden åpnes i det nye nettleservinduet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-119">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="e86ed-120">Derfor kan du ikke ha to visninger av den samme siden side-ved-side ved hjelp av funksjonen **Åpne i nytt vindu**.</span><span class="sxs-lookup"><span data-stu-id="e86ed-120">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="e86ed-121">Nesten alle slike sider har imidlertid en navigasjonsliste du kan bruke til å bytte mellom poster og få en lignende opplevelse.</span><span class="sxs-lookup"><span data-stu-id="e86ed-121">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span> 

<span data-ttu-id="e86ed-122">Før du bruker funksjonen **Åpne i nytt vindu**, konfigurerer du popup-blokkeringen i nettleseren slik at den tillater popup-vinduer fra URL-adressen til området for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e86ed-122">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the Finance and Operations site.</span></span> <span data-ttu-id="e86ed-123">Du kan for eksempel tillate popup-vinduer fra "\*.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="e86ed-123">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span> 

<span data-ttu-id="e86ed-124">Funksjonen **Åpne i nytt vindu** er bare tilgjengelig når det er flere sider åpne i vinduet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-124">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="e86ed-125">I tillegg lukkes popup-vinduet automatisk når ingen flere sider er åpne (det vil si når den siste siden lukkes i dette vinduet).</span><span class="sxs-lookup"><span data-stu-id="e86ed-125">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="e86ed-126">Finance and Operations lukker også åpne sider når du går til et annet område i programmet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-126">Finance and Operations also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="e86ed-127">Hvis du har popup-vinduer åpne og går til et annet område i programmet, lukkes derfor popup-vinduene automatisk fordi sidene i disse vinduene ble lukket av systemet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-127">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span> 

<span data-ttu-id="e86ed-128">Den øverste linjen i popup-vinduene viser informasjon om firmaet siden ble åpnet i, og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-128">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="e86ed-129">Popup-vinduene er også avhengig av hovednettleservinduet for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e86ed-129">The pop-up windows also rely on the main Finance and Operations browser window.</span></span> <span data-ttu-id="e86ed-130">Hvis hovedvinduet lukkes eller oppdateres, blir alle åpne popup-vinduer skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-130">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="e86ed-131">Dette betyr at du kan fortsatt kan vise informasjonen i disse vinduene, men du kan ikke bruke dem.</span><span class="sxs-lookup"><span data-stu-id="e86ed-131">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>




