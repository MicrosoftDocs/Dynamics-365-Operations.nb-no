---
title: Vanlige spørsmål om klient
description: Denne artikkelen gir svar på vanlige spørsmål om Finance and Operations-klienten.
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a7d311bfcd65e23e4062f105435d05cb1ceda6b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567046"
---
# <a name="client-faq"></a><span data-ttu-id="cace4-103">Vanlige spørsmål om klient</span><span class="sxs-lookup"><span data-stu-id="cace4-103">Client FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cace4-104">Denne artikkelen gir svar på vanlige spørsmål om Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="cace4-104">This article provides answers to frequently asked questions about the Finance and Operations client.</span></span>

## <a name="why-arent-symbols-loaded"></a><span data-ttu-id="cace4-105">Hvorfor lastes ikke symboler inn?</span><span class="sxs-lookup"><span data-stu-id="cace4-105">Why aren't symbols loaded?</span></span>

<span data-ttu-id="cace4-106">Sikkerhetsinnstillingene for nettleseren kan hindre at symbolene lastes inn på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="cace4-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="cace4-107">Prøv denne fremgangsmåten for å løse dette problemet:</span><span class="sxs-lookup"><span data-stu-id="cace4-107">To resolve this issue, try the following steps:</span></span>

- <span data-ttu-id="cace4-108">Hvis du opplever dette problemet i Internet Explorer, klikker du **Verktøy** og deretter **Alternativer for Internett**.</span><span class="sxs-lookup"><span data-stu-id="cace4-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span> <span data-ttu-id="cace4-109">I dialogboksen Alternativer for Internett i fanen **Personvern** klikker du **Egendefinert nivå** og kontrollerer at alternativet **Nedlasting av skrifter** er valgt.</span><span class="sxs-lookup"><span data-stu-id="cace4-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
- <span data-ttu-id="cace4-110">Hvis ikke må du kanskje legge til nettstedet for appen i listen over klarerte områder.</span><span class="sxs-lookup"><span data-stu-id="cace4-110">Otherwise, you might have to add the app site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="cace4-111">Jeg savner båndet fra Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="cace4-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="cace4-112">Kan jeg holde fanene i handlingsruten åpne hele tiden?</span><span class="sxs-lookup"><span data-stu-id="cace4-112">Can I keep Action Pane tabs open all the time?</span></span>

<span data-ttu-id="cace4-113">Vi planlegger å implementere denne funksjonen snart.</span><span class="sxs-lookup"><span data-stu-id="cace4-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="cace4-114">Brukere kan da velge å holde fanene i handlingsruter åpen hele tiden.</span><span class="sxs-lookup"><span data-stu-id="cace4-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="cace4-115">Ellers skjules fanene når de ikke er i bruk, slik at det blir mer plass til siden på skjermen.</span><span class="sxs-lookup"><span data-stu-id="cace4-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a><span data-ttu-id="cace4-116">Hvorfor vises det av og til ulike hurtigmenyer når jeg høyreklikker?</span><span class="sxs-lookup"><span data-stu-id="cace4-116">Why do I sometimes see different shortcut menus when I right click?</span></span>

<span data-ttu-id="cace4-117">Hvis du høyreklikker i et redigerbart felt (eller hvis tekst er merket), vises nettleserens hurtigmeny.</span><span class="sxs-lookup"><span data-stu-id="cace4-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="cace4-118">Denne menyen gir deg tilgang til kommandoene **Klipp ut**, **Kopier** og **Lim inn**.</span><span class="sxs-lookup"><span data-stu-id="cace4-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="cace4-119">Vi kan ikke bygge inn disse kommandoene på hurtigmenyene fordi nettlesere av sikkerhetsmessige årsaker ikke gir oss programmatisk tilgang til utklippstavlen i systemet.</span><span class="sxs-lookup"><span data-stu-id="cace4-119">We can't embed these commands into the shortcut menus because, for security reasons, browsers don't allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="cace4-120">Hvis du høyreklikker en feltetikett eller verdien til en skrivebeskyttet kontroll, vises hurtigmenyen.</span><span class="sxs-lookup"><span data-stu-id="cace4-120">If you right-click a field label or the value of a read-only control, you'll see the shortcut menu.</span></span>

<span data-ttu-id="cace4-121">For å gjøre tastaturtilgang enklere planlegger vi å implementere en hurtigtast som åpner hurtigmenyen.</span><span class="sxs-lookup"><span data-stu-id="cace4-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality"></a><span data-ttu-id="cace4-122">Hvor er funksjonen Vis detaljer?</span><span class="sxs-lookup"><span data-stu-id="cace4-122">Where is the View details functionality?</span></span>

<span data-ttu-id="cace4-123">Alternativet **Vis detaljer** er tilgjengelig på ulike måter:</span><span class="sxs-lookup"><span data-stu-id="cace4-123">The **View details** option is available in a couple of ways:</span></span>

- <span data-ttu-id="cace4-124">Hvis en kontroll har **Vis detaljer**-funksjonalitet, og hvis kontrollen har en verdi, vises denne verdien som en hyperkobling.</span><span class="sxs-lookup"><span data-stu-id="cace4-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="cace4-125">Du kan klikke hyperkoblingen for å åpne en side som inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="cace4-125">You can click the hyperlink to open a page that contains additional details.</span></span>
- <span data-ttu-id="cace4-126">**Vis detaljer** er også et alternativ på hurtigmenyer.</span><span class="sxs-lookup"><span data-stu-id="cace4-126">**View details** is also an option on shortcut menus.</span></span> <span data-ttu-id="cace4-127">Hvis du vil ha mer informasjon om når hurtigmenyer vises når du høyreklikker, kan du se den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="cace4-127">For more information about when shortcut menus are displayed when you right-click, see the previous section.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]