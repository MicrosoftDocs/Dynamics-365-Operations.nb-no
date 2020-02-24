---
title: Redigeringsprogram med avansert formel for elektronisk rapportering
description: Dette emnet beskriver hvordan redigeringsprogrammet med avansert formel kan brukes til å konfigurere uttrykk i modellkartlegging av og formatkomponenter i elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d183f77da1dda0c4f04e4e48ab3db0133f494a55
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015333"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="c2e55-103">Redigeringsprogram med avansert formel for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="c2e55-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c2e55-104">I tillegg til det [Elektronisk rapportering-basert](general-electronic-reporting.md) [formelredigeringsprogram](general-electronic-reporting-formula-designer.md) kan du bruke redigeringsprogrammet med avansert formel for elektronisk rapportering til å forbedre opplevelsen av konfigurering av uttrykk for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="c2e55-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="c2e55-105">Det avanserte redigeringsprogrammet er nettleserbasert og drives av [Monaco-redigeringsprogrammet](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="c2e55-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="c2e55-106">De mest brukte avanserte redigeringsfunksjonene er beskrevet i dette emnet:</span><span class="sxs-lookup"><span data-stu-id="c2e55-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="c2e55-107">Autoformatering av kode</span><span class="sxs-lookup"><span data-stu-id="c2e55-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="c2e55-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="c2e55-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="c2e55-109">Kodefullføring</span><span class="sxs-lookup"><span data-stu-id="c2e55-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="c2e55-110">Kodenavigering</span><span class="sxs-lookup"><span data-stu-id="c2e55-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="c2e55-111">Kodestrukturering</span><span class="sxs-lookup"><span data-stu-id="c2e55-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="c2e55-112">Søk og erstatt</span><span class="sxs-lookup"><span data-stu-id="c2e55-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="c2e55-113">Datainnliming</span><span class="sxs-lookup"><span data-stu-id="c2e55-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="c2e55-114">Syntaksfargelegging</span><span class="sxs-lookup"><span data-stu-id="c2e55-114">Syntax colorization</span></span>](#SyntaxColorization)

## <span data-ttu-id="c2e55-115"><a name="ActivateAdvEditor">Aktivere redigeringsprogrammet med avansert formel</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="c2e55-116">Fullfør følgende trinn for å begynne å bruke redigeringsprogrammet med avansert formel i forekomsten av Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c2e55-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="c2e55-117">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="c2e55-118">På **Konfigurasjoner** -siden på handlingsruten, i **Konfigurasjoner** -fanen i **Avanserte innstillinger** -gruppen velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="c2e55-119">I **Brukerparametere** -dialogboksen, i **Kjøringssporing** -delen setter du **Aktiver redigeringsprogram med avansert formel**-parameteren til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="c2e55-120">[![Siden ER-konfigurasjoner](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="c2e55-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c2e55-121">Vær oppmerksom på at denne parameteren er brukerspesifikk og selskapsspesifikk.</span><span class="sxs-lookup"><span data-stu-id="c2e55-121">Be aware that this parameter is user specific and company specific.</span></span>

## <span data-ttu-id="c2e55-122"><a name="Autoformatting">Autoformatering av kode</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="c2e55-123">Når du skriver et sammensatt uttrykk som består av flere rader med kode, blir innrykket for en ny angitt linje automatisk basert på innrykket for den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="c2e55-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="c2e55-124">Du kan velge linjer og endre det tilhørende innrykket ved å skrive inn **Tab** eller **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="c2e55-125">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="c2e55-126">Med autoformatering kan du holde hele uttrykket velformatert for å gjøre ytterligere vedlikehold enklere samt for å forenkle forståelsen av den konfigurerte logikken.</span><span class="sxs-lookup"><span data-stu-id="c2e55-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <span data-ttu-id="c2e55-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="c2e55-128">Redigeringsprogrammet kan fullføre ord for å hjelpe deg å skrive uttrykk raskere og unngå skrivefeil.</span><span class="sxs-lookup"><span data-stu-id="c2e55-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="c2e55-129">Når du begynner å legge til ny tekst, tilbyr redigeringsprogrammet automatisk en liste med funksjoner som støttes i ER-funksjonene, som inneholder tegnene du har angitt.</span><span class="sxs-lookup"><span data-stu-id="c2e55-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="c2e55-130">Du kan også utløse IntelliSense på et hvilket som helst sted i et konfigurert uttrykk ved å skrive inn **Ctrl+mellomrom**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="c2e55-131">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <span data-ttu-id="c2e55-132"><a name="CodeCompletion">Kodefullføring</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="c2e55-133">Redigeringsprogrammet utfører automatisk kodefullføring ved å:</span><span class="sxs-lookup"><span data-stu-id="c2e55-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="c2e55-134">Sette inn en avsluttende hakeparentes når du angir en innledende hakeparentes, slik at markøren beholdes inne i parentesene.</span><span class="sxs-lookup"><span data-stu-id="c2e55-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="c2e55-135">Sette inn det andre anførselstegnet når det første er angitt, slik at markøren beholdes inne i anførselstegnene</span><span class="sxs-lookup"><span data-stu-id="c2e55-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="c2e55-136">Sette inn det andre doble anførselstegnet når det første er angitt, slik at markøren beholdes inne i anførselstegnene</span><span class="sxs-lookup"><span data-stu-id="c2e55-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="c2e55-137">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="c2e55-138">Når du peker til den innlagte parentesen, utheves det andre parentesen automatisk for å vise konstruksjonen de støtter.</span><span class="sxs-lookup"><span data-stu-id="c2e55-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <span data-ttu-id="c2e55-139"><a name="CodeNavigation">Kodenavigering</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="c2e55-140">Du kan finne påkrevde symboler eller linjer i uttrykket ved å skrive inn **Gå til**-kommandoen ved hjelp av kommandopaletten eller hurtigmenyen.</span><span class="sxs-lookup"><span data-stu-id="c2e55-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="c2e55-141">Hvis du for eksempel vil hoppe til linje **8**, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c2e55-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="c2e55-142">Trykk på **Ctrl+G**, angi verdien **8** og trykk deretter på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="c2e55-143">- eller -</span><span class="sxs-lookup"><span data-stu-id="c2e55-143">-or-</span></span>

- <span data-ttu-id="c2e55-144">Trykk på **F1**, skriv inn **G**, velg **Gå til linje**, angi verdien **8** og trykk deretter på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="c2e55-145">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <span data-ttu-id="c2e55-146"><a name="CodeStructuring">Kodestrukturering</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="c2e55-147">Koden for enkelte funksjoner, for eksempel [IF](er-functions-logical-if.md) eller [CASE](er-functions-logical-case.md), struktureres automatisk.</span><span class="sxs-lookup"><span data-stu-id="c2e55-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="c2e55-148">Du kan utvide og skjule alle ønskede foldeområder av denne koden for å redusere den redigerbare delen av et uttrykk, for å fokusere bare på delen som krever din oppmerksomhet.</span><span class="sxs-lookup"><span data-stu-id="c2e55-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="c2e55-149">Fold / Opphev folding-kommandoene kan brukes til det.</span><span class="sxs-lookup"><span data-stu-id="c2e55-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="c2e55-150">Hvis du for eksempel vil folde alle områder, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c2e55-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="c2e55-151">Trykk på **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="c2e55-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="c2e55-152">- eller -</span><span class="sxs-lookup"><span data-stu-id="c2e55-152">-or-</span></span>

- <span data-ttu-id="c2e55-153">Trykk på **F1**, trykk på **FO**, velg **Fold alle** og trykk deretter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="c2e55-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="c2e55-154">Hvis du vil oppheve folding av alle områder, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="c2e55-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="c2e55-155">Trykk på **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="c2e55-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="c2e55-156">- eller -</span><span class="sxs-lookup"><span data-stu-id="c2e55-156">-or-</span></span>
  
- <span data-ttu-id="c2e55-157">Trykk på **F1**, skriv inn **UN**, velg **Opphev folding av alle** og trykk deretter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="c2e55-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="c2e55-158">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <span data-ttu-id="c2e55-159"><a name="FindAndReplace">Søk og erstatt</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="c2e55-160">Hvis du vil søke etter forekomster av bestemt tekst, velger du teksten i uttrykket og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="c2e55-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c2e55-161">Trykk på **Ctrl+F** og trykk deretter på **F3** for å finne den neste forekomsten av den valgte teksten, eller trykk på **Shift+F3** for å finne den forrige forekomsten.</span><span class="sxs-lookup"><span data-stu-id="c2e55-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="c2e55-162">- eller -</span><span class="sxs-lookup"><span data-stu-id="c2e55-162">-or-</span></span>
  
- <span data-ttu-id="c2e55-163">Trykk på **F1**, skriv inn **F** og velg deretter påkrevd alternativ for å finne den merkede teksten.</span><span class="sxs-lookup"><span data-stu-id="c2e55-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="c2e55-164">Hvis du vil erstatte forekomster av en bestemt tekst, velger du teksten i uttrykket og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="c2e55-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c2e55-165">Trykk på **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="c2e55-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="c2e55-166">Angi den alternative teksten, og velg erstatningsalternativet for å erstatte den valgte teksten eller alle forekomstene av denne teksten i det gjeldende uttrykket.</span><span class="sxs-lookup"><span data-stu-id="c2e55-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="c2e55-167">- eller -</span><span class="sxs-lookup"><span data-stu-id="c2e55-167">-or-</span></span>
  
- <span data-ttu-id="c2e55-168">Trykk på **F1**, skriv inn **R** og velg deretter påkrevd alternativ for å erstatte den merkede teksten.</span><span class="sxs-lookup"><span data-stu-id="c2e55-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="c2e55-169">Angi den alternative teksten, og velg erstatningsalternativet for å erstatte den valgte teksten eller alle forekomstene av denne teksten i det gjeldende uttrykket.</span><span class="sxs-lookup"><span data-stu-id="c2e55-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="c2e55-170">Hvis du vil endre alle forekomster av en bestemt tekst, velger du teksten i uttrykket og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="c2e55-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="c2e55-171">Trykk på **CTRL+F2** og angi deretter den alternative teksten.</span><span class="sxs-lookup"><span data-stu-id="c2e55-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="c2e55-172">- eller -</span><span class="sxs-lookup"><span data-stu-id="c2e55-172">-or-</span></span>
  
- <span data-ttu-id="c2e55-173">Trykk på **F1**, skriv inn **C** og velg deretter påkrevd alternativ for å endre den merkede teksten.</span><span class="sxs-lookup"><span data-stu-id="c2e55-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="c2e55-174">Angi den alternative teksten.</span><span class="sxs-lookup"><span data-stu-id="c2e55-174">Enter the alternative text.</span></span>

<span data-ttu-id="c2e55-175">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <span data-ttu-id="c2e55-176"><a name="DataPasting">Innliming av datakilder og funksjoner</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="c2e55-177">Du kan velge **Legg til datakilde**, som utfører innliming til det gjeldende uttrykket av en datakilde som er valgt på venstre **Datakilde** i-panel.</span><span class="sxs-lookup"><span data-stu-id="c2e55-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="c2e55-178">Tilsvarende kan du velge **Legg til funksjonen**, som utfører innliming til det gjeldende uttrykket av en funksjon som er valgt på høyre **Funksjoner**-panel.</span><span class="sxs-lookup"><span data-stu-id="c2e55-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="c2e55-179">Hvis du bruker ER-formelredigeringsprogrammet, vil en valgt funksjon eller en valgt datakilde alltid bli limt inn på slutten av det konfigurerte uttrykket.</span><span class="sxs-lookup"><span data-stu-id="c2e55-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="c2e55-180">Når du bruker ER-redigeringsprogrammet med avansert formel kan en valgt funksjon eller en valgt datakilde limes inn til en hvilken som helst del av det konfigurerte uttrykket.</span><span class="sxs-lookup"><span data-stu-id="c2e55-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="c2e55-181">Du må bruke markøren for å angi hvor du vil lime inn dataene.</span><span class="sxs-lookup"><span data-stu-id="c2e55-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="c2e55-182">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="c2e55-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <span data-ttu-id="c2e55-183"><a name="SyntaxColorization">Syntaksfargelegging</a></span><span class="sxs-lookup"><span data-stu-id="c2e55-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="c2e55-184">Forskjellige farger brukes for øyeblikket til å utheve følgende deler av uttrykk:</span><span class="sxs-lookup"><span data-stu-id="c2e55-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="c2e55-185">Teksten i doble parenteser som kan representere en etikett-ID for en tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="c2e55-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="c2e55-186">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="c2e55-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2e55-187">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c2e55-187">Additional resources</span></span>

- [<span data-ttu-id="c2e55-188">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="c2e55-188">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="c2e55-189">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="c2e55-189">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="c2e55-190">Monaco-redigeringsprogram</span><span class="sxs-lookup"><span data-stu-id="c2e55-190">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
