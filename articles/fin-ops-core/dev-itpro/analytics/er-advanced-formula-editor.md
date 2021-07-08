---
title: Redigeringsprogram med avansert formel for elektronisk rapportering
description: Dette emnet beskriver hvordan redigeringsprogrammet med avansert formel kan brukes til å konfigurere uttrykk i modellkartlegging av og formatkomponenter i elektronisk rapportering (ER).
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270713"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="88b27-103">Redigeringsprogram med avansert formel for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="88b27-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88b27-104">I tillegg til det [Elektronisk rapportering-basert](general-electronic-reporting.md) [formelredigeringsprogram](general-electronic-reporting-formula-designer.md) kan du bruke redigeringsprogrammet med avansert formel for elektronisk rapportering til å forbedre opplevelsen av konfigurering av uttrykk for elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="88b27-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="88b27-105">Det avanserte redigeringsprogrammet er nettleserbasert og drives av [Monaco-redigeringsprogrammet](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="88b27-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="88b27-106">De mest brukte avanserte redigeringsfunksjonene er beskrevet i dette emnet:</span><span class="sxs-lookup"><span data-stu-id="88b27-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="88b27-107">Autoformatering av kode</span><span class="sxs-lookup"><span data-stu-id="88b27-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="88b27-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="88b27-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="88b27-109">Kodefullføring</span><span class="sxs-lookup"><span data-stu-id="88b27-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="88b27-110">Kodenavigering</span><span class="sxs-lookup"><span data-stu-id="88b27-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="88b27-111">Kodestrukturering</span><span class="sxs-lookup"><span data-stu-id="88b27-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="88b27-112">Søk og erstatt</span><span class="sxs-lookup"><span data-stu-id="88b27-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="88b27-113">Datainnliming</span><span class="sxs-lookup"><span data-stu-id="88b27-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="88b27-114">Syntaksfargelegging</span><span class="sxs-lookup"><span data-stu-id="88b27-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="88b27-115"><a name="ActivateAdvEditor">Aktivere redigeringsprogrammet med avansert formel</a></span><span class="sxs-lookup"><span data-stu-id="88b27-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="88b27-116">Fullfør følgende trinn for å begynne å bruke redigeringsprogrammet med avansert formel i forekomsten av Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="88b27-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="88b27-117">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="88b27-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="88b27-118">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="88b27-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="88b27-119">I delen **Kjøringssporing** i dialogboksen **Brukerparametere** setter du parameteren **Aktiver redigeringsprogram med avansert formel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="88b27-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="88b27-120">[![Dialogboksen Brukerparametere, parameteren Aktiver redigeringsprogram med avansert formel er merket](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="88b27-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="88b27-121">Vær oppmerksom på at denne parameteren er brukerspesifikk og selskapsspesifikk.</span><span class="sxs-lookup"><span data-stu-id="88b27-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="88b27-122">Fra og med Microsoft Dynamics 365 Finance versjon 10.0.19 kan du styre hvilke ER-formelredigeringsprogram som tilbys som standard.</span><span class="sxs-lookup"><span data-stu-id="88b27-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="88b27-123">Fullfør fremgangsmåten nedenfor for å aktivere det avanserte formelredigeringsprogrammet for alle brukere og firmaer i gjeldende finansforekomst.</span><span class="sxs-lookup"><span data-stu-id="88b27-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="88b27-124">Åpne arbeidsområdet **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="88b27-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="88b27-125">Finn og velg funksjonen **Angi det avanserte formelredigeringsprogrammet for ER som standard for alle brukere** i listen, og velg deretter **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="88b27-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="88b27-126">Gå til **Organisasjonsstyring** > **Elektronisk rapportering** > **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="88b27-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="88b27-127">På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="88b27-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="88b27-128">I dialogboksen **Brukerparametere** finner du parameteren **Deaktiver avansert formelredigering**, og kontroller at den er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="88b27-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="88b27-129">[![Dialogboksen Brukerparametere, parameteren Deaktiver redigeringsprogram med avansert formel er merket](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="88b27-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="88b27-130">Verdiene til parameterne **Aktiver avansert formelredigeringsprogram** og **Deaktiver avansert formelredigering** holdes separate for hver bruker og tilbys i dialogboksen **Brukerparametere**, avhengig av statusen til funksjonen **Angi det avanserte formelredigeringsprogrammet for ER som standard for alle brukere**.</span><span class="sxs-lookup"><span data-stu-id="88b27-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="88b27-131"><a name="Autoformatting">Autoformatering av kode</a></span><span class="sxs-lookup"><span data-stu-id="88b27-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="88b27-132">Når du skriver et sammensatt uttrykk som består av flere rader med kode, blir innrykket for en ny angitt linje automatisk basert på innrykket for den forrige raden.</span><span class="sxs-lookup"><span data-stu-id="88b27-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="88b27-133">Du kan velge linjer og endre det tilhørende innrykket ved å skrive inn **Tab** eller **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="88b27-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="88b27-134">[![GIF av ER-formelredigeringsprogrammet som viser valg av linjer og endring av innrykk](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="88b27-135">Med autoformatering kan du holde hele uttrykket velformatert for å gjøre ytterligere vedlikehold enklere samt for å forenkle forståelsen av den konfigurerte logikken.</span><span class="sxs-lookup"><span data-stu-id="88b27-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="88b27-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="88b27-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="88b27-137">Redigeringsprogrammet kan fullføre ord for å hjelpe deg å skrive uttrykk raskere og unngå skrivefeil.</span><span class="sxs-lookup"><span data-stu-id="88b27-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="88b27-138">Når du begynner å legge til ny tekst, tilbyr redigeringsprogrammet automatisk en liste med funksjoner som støttes i ER-funksjonene, som inneholder tegnene du har angitt.</span><span class="sxs-lookup"><span data-stu-id="88b27-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="88b27-139">Du kan også utløse IntelliSense på et hvilket som helst sted i et konfigurert uttrykk ved å skrive inn **Ctrl+mellomrom**.</span><span class="sxs-lookup"><span data-stu-id="88b27-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="88b27-140">[![GIF av ER-formelredigeringsprogrammet som viser utløsning av IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="88b27-141"><a name="CodeCompletion">Kodefullføring</a></span><span class="sxs-lookup"><span data-stu-id="88b27-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="88b27-142">Redigeringsprogrammet utfører automatisk kodefullføring ved å:</span><span class="sxs-lookup"><span data-stu-id="88b27-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="88b27-143">Sette inn en avsluttende hakeparentes når du angir en innledende hakeparentes, slik at markøren beholdes inne i parentesene.</span><span class="sxs-lookup"><span data-stu-id="88b27-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="88b27-144">Sette inn det andre anførselstegnet når det første er angitt, slik at markøren beholdes inne i anførselstegnene</span><span class="sxs-lookup"><span data-stu-id="88b27-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="88b27-145">Sette inn det andre doble anførselstegnet når det første er angitt, slik at markøren beholdes inne i anførselstegnene</span><span class="sxs-lookup"><span data-stu-id="88b27-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="88b27-146">[![GIF av ER-formelredigeringsprogram som viser at redigeringsprogrammet fullfører koden automatisk](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="88b27-147">Når du peker til den innlagte parentesen, utheves det andre parentesen automatisk for å vise konstruksjonen de støtter.</span><span class="sxs-lookup"><span data-stu-id="88b27-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="88b27-148"><a name="CodeNavigation">Kodenavigering</a></span><span class="sxs-lookup"><span data-stu-id="88b27-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="88b27-149">Du kan finne påkrevde symboler eller linjer i uttrykket ved å skrive inn **Gå til**-kommandoen ved hjelp av kommandopaletten eller hurtigmenyen.</span><span class="sxs-lookup"><span data-stu-id="88b27-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="88b27-150">Hvis du for eksempel vil hoppe til linje **8**, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="88b27-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="88b27-151">Trykk på **Ctrl+G**, angi verdien **8** og trykk deretter på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="88b27-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="88b27-152">- eller -</span><span class="sxs-lookup"><span data-stu-id="88b27-152">-or-</span></span>

- <span data-ttu-id="88b27-153">Trykk på **F1**, skriv inn **G**, velg **Gå til linje**, angi verdien **8** og trykk deretter på **Enter**.</span><span class="sxs-lookup"><span data-stu-id="88b27-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="88b27-154">[![GIF av ER-formelredigeringsprogrammet som viser hvordan du finner deler av et uttrykk ved hjelp av kommandopaletten](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="88b27-155"><a name="CodeStructuring">Kodestrukturering</a></span><span class="sxs-lookup"><span data-stu-id="88b27-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="88b27-156">Koden for enkelte funksjoner, for eksempel [IF](er-functions-logical-if.md) eller [CASE](er-functions-logical-case.md), struktureres automatisk.</span><span class="sxs-lookup"><span data-stu-id="88b27-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="88b27-157">Du kan utvide og skjule alle ønskede foldeområder av denne koden for å redusere den redigerbare delen av et uttrykk, for å fokusere bare på delen som krever din oppmerksomhet.</span><span class="sxs-lookup"><span data-stu-id="88b27-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="88b27-158">Fold / Opphev folding-kommandoene kan brukes til det.</span><span class="sxs-lookup"><span data-stu-id="88b27-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="88b27-159">Hvis du for eksempel vil folde alle områder, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="88b27-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="88b27-160">Trykk på **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="88b27-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="88b27-161">- eller -</span><span class="sxs-lookup"><span data-stu-id="88b27-161">-or-</span></span>

- <span data-ttu-id="88b27-162">Trykk på **F1**, trykk på **FO**, velg **Fold alle** og trykk deretter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="88b27-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="88b27-163">Hvis du vil oppheve folding av alle områder, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="88b27-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="88b27-164">Trykk på **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="88b27-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="88b27-165">- eller -</span><span class="sxs-lookup"><span data-stu-id="88b27-165">-or-</span></span>
  
- <span data-ttu-id="88b27-166">Trykk på **F1**, skriv inn **UN**, velg **Opphev folding av alle** og trykk deretter på **Enter**</span><span class="sxs-lookup"><span data-stu-id="88b27-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="88b27-167">[![GIF av ER-formelredigeringsprogrammet som viser hvordan koden foldes ut](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="88b27-168"><a name="FindAndReplace">Søk og erstatt</a></span><span class="sxs-lookup"><span data-stu-id="88b27-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="88b27-169">Hvis du vil søke etter forekomster av bestemt tekst, velger du teksten i uttrykket og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="88b27-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="88b27-170">Trykk på **Ctrl+F** og trykk deretter på **F3** for å finne den neste forekomsten av den valgte teksten, eller trykk på **Shift+F3** for å finne den forrige forekomsten.</span><span class="sxs-lookup"><span data-stu-id="88b27-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="88b27-171">- eller -</span><span class="sxs-lookup"><span data-stu-id="88b27-171">-or-</span></span>
  
- <span data-ttu-id="88b27-172">Trykk på **F1**, skriv inn **F** og velg deretter påkrevd alternativ for å finne den merkede teksten.</span><span class="sxs-lookup"><span data-stu-id="88b27-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="88b27-173">Hvis du vil erstatte forekomster av en bestemt tekst, velger du teksten i uttrykket og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="88b27-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="88b27-174">Trykk på **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="88b27-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="88b27-175">Angi den alternative teksten, og velg erstatningsalternativet for å erstatte den valgte teksten eller alle forekomstene av denne teksten i det gjeldende uttrykket.</span><span class="sxs-lookup"><span data-stu-id="88b27-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="88b27-176">- eller -</span><span class="sxs-lookup"><span data-stu-id="88b27-176">-or-</span></span>
  
- <span data-ttu-id="88b27-177">Trykk på **F1**, skriv inn **R** og velg deretter påkrevd alternativ for å erstatte den merkede teksten.</span><span class="sxs-lookup"><span data-stu-id="88b27-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="88b27-178">Angi den alternative teksten, og velg erstatningsalternativet for å erstatte den valgte teksten eller alle forekomstene av denne teksten i det gjeldende uttrykket.</span><span class="sxs-lookup"><span data-stu-id="88b27-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="88b27-179">Hvis du vil endre alle forekomster av en bestemt tekst, velger du teksten i uttrykket og gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="88b27-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="88b27-180">Trykk på **CTRL+F2** og angi deretter den alternative teksten.</span><span class="sxs-lookup"><span data-stu-id="88b27-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="88b27-181">- eller -</span><span class="sxs-lookup"><span data-stu-id="88b27-181">-or-</span></span>
  
- <span data-ttu-id="88b27-182">Trykk på **F1**, skriv inn **C** og velg deretter påkrevd alternativ for å endre den merkede teksten.</span><span class="sxs-lookup"><span data-stu-id="88b27-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="88b27-183">Angi den alternative teksten.</span><span class="sxs-lookup"><span data-stu-id="88b27-183">Enter the alternative text.</span></span>

<span data-ttu-id="88b27-184">[![GIF av ER-formelredigeringsprogrammet som viser søk og erstatt](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="88b27-185"><a name="DataPasting">Innliming av datakilder og funksjoner</a></span><span class="sxs-lookup"><span data-stu-id="88b27-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="88b27-186">Du kan velge **Legg til datakilde**, som utfører innliming til det gjeldende uttrykket av en datakilde som er valgt på venstre **Datakilde** i-panel.</span><span class="sxs-lookup"><span data-stu-id="88b27-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="88b27-187">Tilsvarende kan du velge **Legg til funksjonen**, som utfører innliming til det gjeldende uttrykket av en funksjon som er valgt på høyre **Funksjoner**-panel.</span><span class="sxs-lookup"><span data-stu-id="88b27-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="88b27-188">Hvis du bruker ER-formelredigeringsprogrammet, vil en valgt funksjon eller en valgt datakilde alltid bli limt inn på slutten av det konfigurerte uttrykket.</span><span class="sxs-lookup"><span data-stu-id="88b27-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="88b27-189">Når du bruker ER-redigeringsprogrammet med avansert formel kan en valgt funksjon eller en valgt datakilde limes inn til en hvilken som helst del av det konfigurerte uttrykket.</span><span class="sxs-lookup"><span data-stu-id="88b27-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="88b27-190">Du må bruke markøren for å angi hvor du vil lime inn dataene.</span><span class="sxs-lookup"><span data-stu-id="88b27-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="88b27-191">[![GIF av ER-redigeringsprogrammet som viser hvordan du legger til en datakilde og limer inn en funksjon](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="88b27-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="88b27-192"><a name="SyntaxColorization">Syntaksfargelegging</a></span><span class="sxs-lookup"><span data-stu-id="88b27-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="88b27-193">Forskjellige farger brukes for øyeblikket til å utheve følgende deler av uttrykk:</span><span class="sxs-lookup"><span data-stu-id="88b27-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="88b27-194">Teksten i doble parenteser som kan representere en etikett-ID for en tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="88b27-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="88b27-195">[![ER-formelredigeringsprogram](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="88b27-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="88b27-196">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="88b27-196">Limitations</span></span>

<span data-ttu-id="88b27-197">Redigeringsprogrammet støttes for øyeblikket i følgende nettlesere:</span><span class="sxs-lookup"><span data-stu-id="88b27-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="88b27-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="88b27-198">Chrome</span></span>
- <span data-ttu-id="88b27-199">Edge</span><span class="sxs-lookup"><span data-stu-id="88b27-199">Edge</span></span>
- <span data-ttu-id="88b27-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="88b27-200">Firefox</span></span>
- <span data-ttu-id="88b27-201">Opera</span><span class="sxs-lookup"><span data-stu-id="88b27-201">Opera</span></span>
- <span data-ttu-id="88b27-202">Safari</span><span class="sxs-lookup"><span data-stu-id="88b27-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88b27-203">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="88b27-203">Additional resources</span></span>

- [<span data-ttu-id="88b27-204">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="88b27-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="88b27-205">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="88b27-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="88b27-206">Monaco-redigeringsprogram</span><span class="sxs-lookup"><span data-stu-id="88b27-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
