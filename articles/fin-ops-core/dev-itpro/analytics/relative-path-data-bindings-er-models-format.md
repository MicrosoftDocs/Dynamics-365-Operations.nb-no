---
title: Bruke en relativ bane i databindinger for ER-modeller og -formater
description: Med verktøyet for elektronisk rapportering (ER) kan brukere definere elektroniske formatstrukturer og deretter beskrive hvordan disse strukturene skal fylles ved hjelp av data og algoritmer som finnes i programmet.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2940d99243ac52ee0d56a1c4423c4f0250f42f57
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091778"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="03b06-103">Bruke en relativ bane i databindinger for ER-modeller og -formater</span><span class="sxs-lookup"><span data-stu-id="03b06-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="03b06-104">Med verktøyet for elektronisk rapportering (ER) kan brukere definere elektroniske formatstrukturer og deretter beskrive hvordan disse strukturene skal fylles ved hjelp av data og algoritmer som finnes i programmet.</span><span class="sxs-lookup"><span data-stu-id="03b06-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="03b06-105">Hvis du vil ha mer informasjon, kan du se [Opprette ER-konfigurasjoner (elektronisk rapportering)](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="03b06-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="03b06-106">Hvis du vil angi dataflyten for å hente Finance and Operations-data og bruke dem til å generere et elektronisk dokument, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="03b06-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="03b06-107">Bind konfigurerte datakilder til elementer i den utformede domenespesifikke datamodellen.</span><span class="sxs-lookup"><span data-stu-id="03b06-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="03b06-108">Modellstrukturen og de valgte datakildene kan være del av en kompleks hierarkisk struktur.</span><span class="sxs-lookup"><span data-stu-id="03b06-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="03b06-109">Endelige bindinger kan på grunn av dette være ganske store og inneholde mange elementer av forskjellige typer (for eksempel relasjoner, tabeller og metoder).</span><span class="sxs-lookup"><span data-stu-id="03b06-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="03b06-110">Bindingene kan bli mindre lesbare og svært vanskelige å se gjennom og forstå, særlig for ikke-eiere.</span><span class="sxs-lookup"><span data-stu-id="03b06-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="03b06-111">Bind datamodellelementer til formatkomponenter for å definere hvilke data som skal fylles inn fra datamodellen i det genererte formatets utdata.</span><span class="sxs-lookup"><span data-stu-id="03b06-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="03b06-112">Funksjonen for relativ bane har blitt utgitt for å forbedre anvendeligheten av ER-tilordningsutforminger.</span><span class="sxs-lookup"><span data-stu-id="03b06-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="03b06-113">Alternativet for relativ bane er som standard aktivert for nye forekomster av programmet der ER-utformingsopplevelsen er gjeldende (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="03b06-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="03b06-114">Vi implementerte parameteren for relativ bane, slik at brukerne kan fortsette å bruke hele banen når de arbeider med denne presentasjonen av ER-bindinger.</span><span class="sxs-lookup"><span data-stu-id="03b06-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="03b06-115">[![Brukerparametere](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="03b06-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="03b06-116">Når parameteren for bruk av relativ bane er aktivert, erstatter ett @-tegn banen til det overordnede elementet i bindingen for det gjeldende modellelementet.</span><span class="sxs-lookup"><span data-stu-id="03b06-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="03b06-117">Hele bindingsbanen blir kortere, noe som gjør hele tilordningen tydeligere og enklere å forstå.</span><span class="sxs-lookup"><span data-stu-id="03b06-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="03b06-118">I de fleste tilfeller kreves ingen ytterligere rulling i ER-utformingen for å vise alle bindingene for datamodellen.</span><span class="sxs-lookup"><span data-stu-id="03b06-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="03b06-119">[![Modelltilordningsutforming](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="03b06-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="03b06-120">Når du begynner å utforme et nytt ER-uttrykk, trenger du bare å angi ett tegn for å definere en binding til et felt i det overordnede elementet.</span><span class="sxs-lookup"><span data-stu-id="03b06-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="03b06-121">[![Formeldesigner](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="03b06-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="03b06-122">Når du beslutter å endre datakilden for det overordnede modellelementet og bruker absolutt bane, må du binde dette modellelementet på nytt manuelt, i tillegg til alle nestede elementer, til en ny datakilde.</span><span class="sxs-lookup"><span data-stu-id="03b06-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="03b06-123">Når bruk av relativ bane er aktivert og du velger en ny datakilde som skal bindes til et overordnet element, kan du velge et alternativ for å binde alle nestede elementer på nytt automatisk for det overordnede elementet med ett klikk.</span><span class="sxs-lookup"><span data-stu-id="03b06-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="03b06-124">[![Melding om å erstatte eksisterende bane](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="03b06-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="03b06-125">Hvis du bekrefter at nestede elementer skal bindes på nytt, blir det nye overordnede elementet lagt i banen til hvert nestede element som inneholder det eksisterende overordnede elementet.</span><span class="sxs-lookup"><span data-stu-id="03b06-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="03b06-126">Denne funksjonen ødelegger ikke bakoverkompatibiliteten til ER-rammeverket.</span><span class="sxs-lookup"><span data-stu-id="03b06-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="03b06-127">Alle tidligere utformede ER-konfigurasjoner fungerer med denne nye funksjonen, og ingen oppgraderinger eller konverteringer er nødvendige.</span><span class="sxs-lookup"><span data-stu-id="03b06-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="03b06-128">Alle endringer som forårsakes av masseendring av bindinger for nestede elementer i modelltilordninger, lagres riktig i konfigurasjonsdelta (sporing av endringer).</span><span class="sxs-lookup"><span data-stu-id="03b06-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="03b06-129">Dermed kan kundene rebasere den avledede versjonen av modelltilordninger til en hvilken som helst ny basisversjon av den som er endret ved hjelp av denne nye funksjonen.</span><span class="sxs-lookup"><span data-stu-id="03b06-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>
