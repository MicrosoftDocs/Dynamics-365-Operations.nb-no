---
title: Definere parameterne for et ER-format per juridisk enhet
description: Dette emnet forklarer hvordan du kan konfigurere parametere for et ER-format per juridisk enhet.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681478"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="613b3-103">Definere parameterne for et ER-format per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="613b3-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="613b3-104">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="613b3-104">Prerequisites</span></span>

<span data-ttu-id="613b3-105">Hvis du vil fullføre disse trinnene, må du først fullføre trinnene i emnet [Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="613b3-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="613b3-106">Hvis du vil fullføre eksemplene i dette emnet, må du ha tilgang til Microsoft Dynamics 365 Finance (Finance) for en av de følgende rollene:</span><span class="sxs-lookup"><span data-stu-id="613b3-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="613b3-107">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="613b3-107">Electronic reporting developer</span></span>
- <span data-ttu-id="613b3-108">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="613b3-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="613b3-109">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="613b3-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="613b3-110">Importere ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="613b3-110">Import ER configurations</span></span>

1.  <span data-ttu-id="613b3-111">Logg på miljøet.</span><span class="sxs-lookup"><span data-stu-id="613b3-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="613b3-112">Velg **Elektronisk rapportering** på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="613b3-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="613b3-113">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="613b3-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="613b3-114">Importerer, til den gjeldende forekomsten av Finance, konfigurasjonene du eksporterte fra Regulatory Configuration Services (RCS) mens du fullfører trinnene i emnet [Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="613b3-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="613b3-115">Følg denne fremgangsmåten for hver ER-konfigurasjon i følgende rekkefølge: datamodell, modelltilordning og formater.</span><span class="sxs-lookup"><span data-stu-id="613b3-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="613b3-116">Velg **Exchange \> Last inn fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="613b3-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="613b3-117">Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.</span><span class="sxs-lookup"><span data-stu-id="613b3-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="613b3-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="613b3-118">Select **OK**.</span></span>
    
    <span data-ttu-id="613b3-119">Følgende illustrasjon viser konfigurasjonene du trenger når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="613b3-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Siden ER-konfigurasjoner](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="613b3-121">Definer parametere for DEMF-selskapet</span><span class="sxs-lookup"><span data-stu-id="613b3-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="613b3-122">Du kan bruke ER-rammeverket til å definere programspesifikke parametere for et ER-format.</span><span class="sxs-lookup"><span data-stu-id="613b3-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="613b3-123">Velg den juridiske enheten **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="613b3-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="613b3-124">I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="613b3-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="613b3-125">På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="613b3-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="613b3-127">På siden **Programspesifikke parametere** kan du konfigurere reglene for **Velger**-datakilden for **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="613b3-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="613b3-128">Hvis det grunnleggende ER-formatet vil inneholde flere datakilder for **Oppslag**-typen, må du velge ønsket datakilde i **Oppslag**-hurtigfanen før du kan begynne med å konfigurere regelsettet for datakilden.</span><span class="sxs-lookup"><span data-stu-id="613b3-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="613b3-129">For hver datakilde kan du konfigurere egne regler for hver versjon av det valgte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="613b3-130">Hele settet med regler for alle oppslagsdatakilder som er tilgjengelige i den valgte versjonen av det grunnleggende ER-formatet, utgjør programspesifikke parametere for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="613b3-131">Velg versjon **1.1.1** av ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="613b3-132">Velg **Legg til** på hurtigfanen **Betingelser**.</span><span class="sxs-lookup"><span data-stu-id="613b3-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="613b3-133">Klikk på rullegardinpilen i **Kode**-feltet for den nye posten for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="613b3-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="613b3-134">Oppslaget viser listen over avgiftskoder for valg.</span><span class="sxs-lookup"><span data-stu-id="613b3-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="613b3-135">Denne listen er returnert av **Model.Data.Tax**-datakilden som er konfigurert i det grunnleggende ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="613b3-136">Siden denne datakilden inneholder **navn** -feltet, vises navnet på hver avgiftskode i oppslaget.</span><span class="sxs-lookup"><span data-stu-id="613b3-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="613b3-138">Velg mva-koden **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="613b3-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="613b3-139">Klikk på rullegardinpilen i **Oppslagsresultat**-feltet for den nye posten for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="613b3-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="613b3-140">Oppslaget presenterer listen med verdier for formatopplistingen for TaxationLevel for utvalg.</span><span class="sxs-lookup"><span data-stu-id="613b3-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="613b3-141">Legg merke til at hvis tysk er valgt som foretrukket språk for brukeren du er logget på som, vil etikettene for verdiene i oppslaget være på tysk, forutsatt at de er oversatt i grunnleggende ER-format.</span><span class="sxs-lookup"><span data-stu-id="613b3-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="613b3-142">Hvis etiketten til en oppslagsdatakilde for eksempel er oversatt, vil denne etiketten vises på brukerens foretrukne språk i **Oppslag**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="613b3-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="613b3-144">Velg **Vanlig avgift**-verdien.</span><span class="sxs-lookup"><span data-stu-id="613b3-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="613b3-145">Når du legger til denne posten, definerer du følgende regel: Hver gang **Velger**-oppslagsdatakilden blir forespurt, og **VAT19** mva-koden sendes som et argument, returneres **vanlig avgift** som forespurt avgiftsnivå.</span><span class="sxs-lookup"><span data-stu-id="613b3-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="613b3-146">Velg **Legg til**, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="613b3-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="613b3-147">I **Kode**-feltet velger du avgiftskoden **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="613b3-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="613b3-148">Velg **Vanlig avgift**-verdien i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="613b3-149">Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="613b3-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="613b3-150">I **Kode**-feltet velger du avgiftskoden **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="613b3-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="613b3-151">Velg **Redusert avgift**-verdien i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="613b3-152">Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="613b3-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="613b3-153">I **Kode**-feltet velger du avgiftskoden **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="613b3-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="613b3-154">Velg **Redusert avgift**-verdien i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="613b3-155">Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="613b3-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="613b3-156">I **Kode**-feltet velger du avgiftskoden **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="613b3-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="613b3-157">Velg **Ingen avgift**-verdien i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="613b3-158">Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="613b3-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="613b3-159">I **Kode**-feltet velger du avgiftskoden **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="613b3-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="613b3-160">Velg **Ingen avgift**-verdien i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="613b3-161">Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="613b3-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="613b3-162">I **Kode**-feltet velger du **\*Ikke tom\***-alternativet.</span><span class="sxs-lookup"><span data-stu-id="613b3-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="613b3-163">Velg **Annet**-verdien i **Oppslagsresultat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="613b3-164">Ved å legge til den siste posten definerer du følgnde regel: Her gang avgiftskoden som sendes som et argument, ikke oppfyller noen av de tidligere reglene, returnerer oppslagsdatakilden **Annet** som forespurt avgiftsnivå.</span><span class="sxs-lookup"><span data-stu-id="613b3-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="613b3-166">Velg **Fullført** i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="613b3-167">Når du kjører en ER-formatversjon som har statusen **fullført** eller **delt**, må dette settet med regler være i **fullført**-tilstand.</span><span class="sxs-lookup"><span data-stu-id="613b3-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="613b3-168">Hvis ikke vil utføringen av det grunnleggende ER-formatet bli avbrutt når formatet prøver å laste inn data fra dette regelsettet mens data **Velger**-oppslagsdatakilden kjøres.</span><span class="sxs-lookup"><span data-stu-id="613b3-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="613b3-169">Når du kjører en ER-formatversjon som har statusen **utkast**, kan det grunnleggende ER-formatet få tilgang til dette regelsettet, uavhengig av tilstanden.</span><span class="sxs-lookup"><span data-stu-id="613b3-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="613b3-170">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="613b3-170">Select **Save**.</span></span>
18. <span data-ttu-id="613b3-171">Lukk siden **Programspesifikke parametere**.</span><span class="sxs-lookup"><span data-stu-id="613b3-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="613b3-172">Kjør ER-formatet i DEMF firmaet</span><span class="sxs-lookup"><span data-stu-id="613b3-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="613b3-173">I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="613b3-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="613b3-174">Velg **Kjør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="613b3-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="613b3-175">I dialogboksen som vises, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="613b3-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="613b3-176">Last ned utdraget som er generert, og lagre det lokalt.</span><span class="sxs-lookup"><span data-stu-id="613b3-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="613b3-177">I det genererte utdraget legger du merke til at sammendraget av **InVAT7**-avgiftskoden er lagt på **Redusert**-nivået, og sammendragene av **VAT19** og **InVA19**-avgiftskodene er lagt på **vanlig** nivå.</span><span class="sxs-lookup"><span data-stu-id="613b3-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="613b3-178">Denne virkemåten bestemmes av konfigurasjonen i det juridisk enhetensavhengige regelsettet.</span><span class="sxs-lookup"><span data-stu-id="613b3-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="613b3-179">Gå til **Avgift \> Indirekte avgifter \> Merverdiavgift \> Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="613b3-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="613b3-180">Velg mva-koden **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="613b3-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="613b3-181">I handlingsruten i kategorien **Mva-kode** i **Forespørsler**-gruppen velger du **Postert merverdiavgift** for å vise informasjon om avgiftsverdien og brukt avgiftssats per avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="613b3-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Siden Postert merverdiavgift](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="613b3-183">Lukk siden Postert merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="613b3-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="613b3-184">Definer parametere for USMF-selskapet</span><span class="sxs-lookup"><span data-stu-id="613b3-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="613b3-185">Velg den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="613b3-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="613b3-186">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="613b3-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="613b3-187">I konfigurasjonstreet utvider du elementet **Modell for å lære om parameterkall**, utvid elementet **Format for å lære om parameterkall**, og velg formatet **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="613b3-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="613b3-188">På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="613b3-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="613b3-189">Velg versjon **1.1.1** av det valgte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="613b3-190">Velg **Legg til** på hurtigfanen **Betingelser**.</span><span class="sxs-lookup"><span data-stu-id="613b3-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="613b3-191">Klikk på rullegardinpilen i **Kode**-feltet for den nye posten for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="613b3-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="613b3-192">Oppslaget viser nå en liste over mva-koder for **USMF** selskapsavgiften for valg.</span><span class="sxs-lookup"><span data-stu-id="613b3-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="613b3-194">Velg mva-koden **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="613b3-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="613b3-195">Velg **Ingen avgift**-verdien i **Oppslagsresultat**-feltet for den nye posten.</span><span class="sxs-lookup"><span data-stu-id="613b3-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="613b3-196">Velg **Legg til** på nytt.</span><span class="sxs-lookup"><span data-stu-id="613b3-196">Select **Add** again.</span></span>
11. <span data-ttu-id="613b3-197">I **Kode**-feltet for den nye posten velger du **\*Ikke tom\***-alternativet.</span><span class="sxs-lookup"><span data-stu-id="613b3-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="613b3-198">Velg **Vanlig avgift**-verdien i **Oppslagsresultat**-feltet for den nye posten.</span><span class="sxs-lookup"><span data-stu-id="613b3-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="613b3-199">Velg **Fullført** i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="613b3-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="613b3-200">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="613b3-200">Select **Save**.</span></span>

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="613b3-202">Lukk siden **Programspesifikke parametere**.</span><span class="sxs-lookup"><span data-stu-id="613b3-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="613b3-203">Kjør ER-formatet i USMF firmaet</span><span class="sxs-lookup"><span data-stu-id="613b3-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="613b3-204">I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="613b3-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="613b3-205">Velg **Kjør** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="613b3-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="613b3-206">I dialogboksen som vises, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="613b3-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="613b3-207">Last ned utdraget som er generert, og lagre det lokalt.</span><span class="sxs-lookup"><span data-stu-id="613b3-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="613b3-208">Legg merke til at du nå har brukt det samme ER-formatet på nytt for en annen juridisk enhet i det genererte uttrykket, men uten å gjøre noen justeringer i ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="613b3-209">Bruk juridisk enhetsavhengige parametere på nytt</span><span class="sxs-lookup"><span data-stu-id="613b3-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="613b3-210">Eksportere parametere</span><span class="sxs-lookup"><span data-stu-id="613b3-210">Export parameters</span></span>

1.  <span data-ttu-id="613b3-211">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="613b3-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="613b3-212">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="613b3-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="613b3-213">I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.</span><span class="sxs-lookup"><span data-stu-id="613b3-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="613b3-214">På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="613b3-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="613b3-215">Velg versjon **1.1.1** av ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="613b3-216">Velg **Eksporter** på handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="613b3-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="613b3-217">Last ned filen som er generert, og lagre det lokalt.</span><span class="sxs-lookup"><span data-stu-id="613b3-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="613b3-218">Det konfigurerte settet med programspesifikke parametere er nå eksportert som en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="613b3-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="613b3-219">Importere parametere</span><span class="sxs-lookup"><span data-stu-id="613b3-219">Import parameters</span></span>

1.  <span data-ttu-id="613b3-220">Velg versjon **1.1.2** av ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="613b3-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="613b3-221">Velg **Importer** på handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="613b3-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="613b3-222">Velg **Ja** for å bekrefte at du vil overstyre de eksisterende programspesifikke parameterne for denne formatversjonen.</span><span class="sxs-lookup"><span data-stu-id="613b3-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="613b3-223">Velg **Bla gjennom** for å finne filen som inneholder de eksporterte programspesifikke parameterne for versjon **1.1.1.**.</span><span class="sxs-lookup"><span data-stu-id="613b3-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="613b3-224">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="613b3-224">Select **OK**.</span></span>

    <span data-ttu-id="613b3-225">Versjon **1.1.2** av ER-formatet har nå samme programspesifikke parametere som du opprinnelig konfigurerte for versjon **1.1.1.**.</span><span class="sxs-lookup"><span data-stu-id="613b3-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="613b3-226">Legg merke til at de programspesifikke parameterne for et ER-format er juridisk enhetsavhengig.</span><span class="sxs-lookup"><span data-stu-id="613b3-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="613b3-227">Hvis du vil bruke de programspesifikke parameterne som ble konfigurert for én juridisk enhet på nytt i en annen juridisk enhet, må du eksportere dem mens du er logget på den første juridiske enheten, og deretter importere dem etter at du har logget på den andre juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="613b3-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="613b3-228">Du kan også bruke denne fremgangsmåten til å overføre ER-formatrelaterte programspesifikke parametere som opprinnelig ble konfigurert i én forekomst av Finance til en annen forekomst av Finance.</span><span class="sxs-lookup"><span data-stu-id="613b3-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="613b3-229">Vær oppmerksom på at hvis du konfigurerer programspesifikke parametere for én versjon av et ER-format og importerer en høyere versjon av samme format til gjeldende Finance-forekomst, vil ikke de eksisterende programspesifikke parameterne brukes for den importerte versjonen.</span><span class="sxs-lookup"><span data-stu-id="613b3-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="613b3-230">Vær også oppmerksom på at når du velger en fil for import, sammenlignes strukturen til programspesifikke parametere i den aktuelle filen med strukturen til den tilsvarende datakilden for **Oppslag**-typen i ER-formatet som er valgt for import.</span><span class="sxs-lookup"><span data-stu-id="613b3-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="613b3-231">Importen utføres når strukturen til hver programspesifikk parameter samsvarer med strukturen til den tilsvarende datakilden i ER-formatet som er valgt for import.</span><span class="sxs-lookup"><span data-stu-id="613b3-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="613b3-232">Hvis strukturene ikke samsvarer, får du en advarsel som sier at importen ikke kan utføres.</span><span class="sxs-lookup"><span data-stu-id="613b3-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="613b3-233">Hvis du fremtvinger importen som skal utføres, ryddes det opp i de eksisterende programspesifikke parameterne for det valgte ER-formatet, og du må definere dem fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="613b3-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="613b3-234">Relasjon mellom programspesifikke parametere og et ER-format</span><span class="sxs-lookup"><span data-stu-id="613b3-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="613b3-235">Forholdet mellom et ER-format og de programspesifikke parameterne etableres av ER-formatets forekomstuavhengige unike identifikasjonskode.</span><span class="sxs-lookup"><span data-stu-id="613b3-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="613b3-236">Når du fjerner et ER-format fra Finance, beholdes derfor de programspesifikke parameterne som er konfigurert for ER-formatet, i den gjeldende forekomsten av Finance.</span><span class="sxs-lookup"><span data-stu-id="613b3-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="613b3-237">Du kan få tilgang til dem når det grunnleggende ER-formatet blir importert på nytt til denne forekomsten av Finance.</span><span class="sxs-lookup"><span data-stu-id="613b3-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="613b3-238">Få tilgang til programspesifikke parametere ved hjelp av ER-rammeverket</span><span class="sxs-lookup"><span data-stu-id="613b3-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="613b3-239">I det forrige eksemplet har du fått tilgang til programspesifikke parametere i et ER-format ved hjelp av ER-rammeverket.</span><span class="sxs-lookup"><span data-stu-id="613b3-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="613b3-240">Denne fremgangsmåten gir deg ikke muligheten til å begrense tilgangen til programspesifikke parametere i et spesielt ER-format.</span><span class="sxs-lookup"><span data-stu-id="613b3-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="613b3-241">Hvis du må bruke slike restriksjoner, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="613b3-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="613b3-242">Bruk et eksisterende **ERSolutionAppSpecificParametersDesigner**-menyelement, eller implementer ditt eget **ERSolutionAppSpecificParametersDesigner**-menyelement.</span><span class="sxs-lookup"><span data-stu-id="613b3-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual studio-side](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="613b3-244">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="613b3-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="613b3-245">Opprett en ny menyelementknapp, og koble den til den tilsvarende posten fra **ERSolutionTable**-tabellen ved å sette **Datakilde**-egenskapen til **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="613b3-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual studio-side](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="613b3-247">Opprett en enkel knapp, og overstyr **Klikket**-metoden, som vist i følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="613b3-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="613b3-248">Ved å bruke denne fremgangsmåten kan du angi en unik løsnings-ID (definert via **GUID**-verdien) for å gi tilgang til de programspesifikke parameterne for bare et spesifikt ER-format og underordnede kopier som er avledet fra det.</span><span class="sxs-lookup"><span data-stu-id="613b3-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="613b3-249">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="613b3-249">Additional resources</span></span>

[<span data-ttu-id="613b3-250">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="613b3-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="613b3-251">Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="613b3-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
