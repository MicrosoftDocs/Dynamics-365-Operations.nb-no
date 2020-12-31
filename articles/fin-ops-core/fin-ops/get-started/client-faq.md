---
title: Vanlige spørsmål om klient
description: Denne artikkelen gir svar på vanlige spørsmål om Finance and Operations-klienten.
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1925c23891a637ba9e9666538323274819692a06
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692924"
---
# <a name="client-faq"></a><span data-ttu-id="ae50d-103">Vanlige spørsmål om klient</span><span class="sxs-lookup"><span data-stu-id="ae50d-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae50d-104">Denne artikkelen gir svar på vanlige spørsmål om Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="ae50d-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="ae50d-105">Hvorfor lastes ikke symboler inn?</span><span class="sxs-lookup"><span data-stu-id="ae50d-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="ae50d-106">Sikkerhetsinnstillingene for nettleseren kan hindre at symbolene lastes inn på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="ae50d-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="ae50d-107">Prøv denne fremgangsmåten for å løse dette problemet:</span><span class="sxs-lookup"><span data-stu-id="ae50d-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="ae50d-108">Hvis du opplever dette problemet i Internet Explorer, klikker du **Verktøy** og deretter **Alternativer for Internett**.</span><span class="sxs-lookup"><span data-stu-id="ae50d-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="ae50d-109">I dialogboksen Alternativer for Internett i kategorien **Personvern** klikker du **Egendefinert nivå** og kontrollerer at alternativet **Nedlasting av skrifter** er valgt.</span><span class="sxs-lookup"><span data-stu-id="ae50d-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="ae50d-110">Hvis ikke må du kanskje legge til nettstedet for appen i listen over klarerte områder.</span><span class="sxs-lookup"><span data-stu-id="ae50d-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="ae50d-111">Jeg savner båndet fra Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="ae50d-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="ae50d-112">Kan jeg holde fanene i handlingsruten åpne hele tiden?</span><span class="sxs-lookup"><span data-stu-id="ae50d-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="ae50d-113">Vi planlegger å implementere denne funksjonen snart.</span><span class="sxs-lookup"><span data-stu-id="ae50d-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="ae50d-114">Brukere kan da velge å holde fanene i handlingsruter åpen hele tiden.</span><span class="sxs-lookup"><span data-stu-id="ae50d-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="ae50d-115">Ellers skjules fanene når de ikke er i bruk, slik at det blir mer plass til siden på skjermen.</span><span class="sxs-lookup"><span data-stu-id="ae50d-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="ae50d-116">Hvorfor vises det av og til ulike hurtigmenyer når jeg høyreklikker?</span><span class="sxs-lookup"><span data-stu-id="ae50d-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="ae50d-117">Hvis du høyreklikker i et redigerbart felt (eller hvis tekst er merket), vises nettleserens hurtigmeny.</span><span class="sxs-lookup"><span data-stu-id="ae50d-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="ae50d-118">Denne menyen gir deg tilgang til kommandoene **Klipp ut**, **Kopier** og **Lim inn**.</span><span class="sxs-lookup"><span data-stu-id="ae50d-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="ae50d-119">Vi kan ikke bygge inn disse kommandoene på hurtigmenyene fordi nettlesere av sikkerhetsmessige årsaker ikke gir oss programmatisk tilgang til utklippstavlen i systemet.</span><span class="sxs-lookup"><span data-stu-id="ae50d-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="ae50d-120">Hvis du høyreklikker en feltetikett eller verdien til en skrivebeskyttet kontroll, vises hurtigmenyen.</span><span class="sxs-lookup"><span data-stu-id="ae50d-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="ae50d-121">For å gjøre tastaturtilgang enklere planlegger vi å implementere en hurtigtast som åpner hurtigmenyen.</span><span class="sxs-lookup"><span data-stu-id="ae50d-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="ae50d-122">Hvor er funksjonen Vis detaljer?</span><span class="sxs-lookup"><span data-stu-id="ae50d-122">Where is the View details functionality?</span></span>

<span data-ttu-id="ae50d-123">Alternativet **Vis detaljer** er tilgjengelig på ulike måter:</span><span class="sxs-lookup"><span data-stu-id="ae50d-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="ae50d-124">Hvis en kontroll har **Vis detaljer**-funksjonalitet, og hvis kontrollen har en verdi, vises denne verdien som en hyperkobling.</span><span class="sxs-lookup"><span data-stu-id="ae50d-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="ae50d-125">Du kan klikke hyperkoblingen for å åpne en side som inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="ae50d-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="ae50d-126">**Vis detaljer** er også et alternativ på hurtigmenyer.</span><span class="sxs-lookup"><span data-stu-id="ae50d-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="ae50d-127">Hvis du vil ha mer informasjon om når hurtigmenyer vises når du høyreklikker, kan du se den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="ae50d-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>
