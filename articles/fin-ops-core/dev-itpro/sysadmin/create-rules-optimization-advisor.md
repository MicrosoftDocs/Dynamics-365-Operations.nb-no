---
title: Opprette regler for optimaliseringsrådgiver
description: Dette emnet beskriver hvordan du legger til nye regler i optimaliseringsrådgiver.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180996"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="370b4-103">Opprette regler for optimaliseringsrådgiver</span><span class="sxs-lookup"><span data-stu-id="370b4-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="370b4-104">Dette emnet forklarer hvordan du oppretter nye regler for **optimaliseringsrådgiver**.</span><span class="sxs-lookup"><span data-stu-id="370b4-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="370b4-105">Du kan for eksempel opprette en ny regel som identifiserer tilbudsforespørselssakene som har en tom tittel.</span><span class="sxs-lookup"><span data-stu-id="370b4-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="370b4-106">Bruk av titler på saker gjør dem lett å kjenne igjen og søkbare.</span><span class="sxs-lookup"><span data-stu-id="370b4-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="370b4-107">Dette eksemplet som er ganske enkelt, viser hva som kan oppnås med optimaliseringsregler.</span><span class="sxs-lookup"><span data-stu-id="370b4-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="370b4-108">En *regel* er en sjekk av programdata.</span><span class="sxs-lookup"><span data-stu-id="370b4-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="370b4-109">Hvis betingelsen som denne regelen evaluerer, er oppfylt, opprettes salgsmuligheter for å optimalisere prosesser eller forbedre data.</span><span class="sxs-lookup"><span data-stu-id="370b4-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="370b4-110">Salgsmulighetene kan brukes, og eventuelt virkningen av handlingene kan måles.</span><span class="sxs-lookup"><span data-stu-id="370b4-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="370b4-111">Hvis du vil opprette en ny regel for **optimaliseringsrådgiver**, legger du til en ny klasse som utvider den abstrakte **SelfHealingRule**-klassen, implementerer **IDiagnosticsRule**-grensesnittet og dekoreres av **DiagnosticRule**-attributtet.</span><span class="sxs-lookup"><span data-stu-id="370b4-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="370b4-112">Klassen må også ha en metode som er dekorert med **DiagnosticsRuleSubscription**-attributtet.</span><span class="sxs-lookup"><span data-stu-id="370b4-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="370b4-113">Etter konvensjonen utføres dette i **opportunityTitle**-metoden, som diskuteres senere.</span><span class="sxs-lookup"><span data-stu-id="370b4-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="370b4-114">Denne nye klassen kan legges til en egendefinert modell med en avhengighetsforhold til **SelfHealingRules**-modellen.</span><span class="sxs-lookup"><span data-stu-id="370b4-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="370b4-115">I eksemplet nedenfor kalles regelen som implementeres **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="370b4-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="370b4-116">**SelfHealingRule**-abstraktklassen har abstrakte metoder som må implementeres i arveklasser.</span><span class="sxs-lookup"><span data-stu-id="370b4-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="370b4-117">Kjernen er **evaluer**-metoden, som returnerer en liste over salgsmuligheter som er identifisert av regelen.</span><span class="sxs-lookup"><span data-stu-id="370b4-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="370b4-118">Salgsmuligheter kan være per juridisk enhet, eller kan gjelde for hele systemet.</span><span class="sxs-lookup"><span data-stu-id="370b4-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="370b4-119">Metoden ovenfor gjentas over firmaer og velger tilbudsforespørselstilfeller med tomme titler i **findRFQCasesWithEmptyTitle**-metoden.</span><span class="sxs-lookup"><span data-stu-id="370b4-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="370b4-120">Hvis minst ett slikt tilfelle blir funnet, opprettes en firmaspesifikk salgsmulighet med **getOpportunityForCompany**-metoden.</span><span class="sxs-lookup"><span data-stu-id="370b4-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="370b4-121">Legg merke til at feltet **Data** i **SelfHealingOpportunity**-tabellen er av typen **Beholder**, og kan derfor inneholde alle data som er relevante for logikken som gjelder denne regelen.</span><span class="sxs-lookup"><span data-stu-id="370b4-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="370b4-122">Angivelse av **OpportunityDate** med gjeldende tidsangivelse registrerer tidspunktet for den siste evalueringen av salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="370b4-123">Salgsmuligheter kan også være på tvers av firmaer.</span><span class="sxs-lookup"><span data-stu-id="370b4-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="370b4-124">I så fall er ikke løkken over firmaer nødvendig og salgsmuligheten må opprettes med **getOpportunityAcrossCompanies**-metoden.</span><span class="sxs-lookup"><span data-stu-id="370b4-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="370b4-125">Koden nedenfor viser **findRFQCasesWithEmptyTitle**-metoden, som returnerer ID-ene til tilbudsforespørselssakene som har tomme titler.</span><span class="sxs-lookup"><span data-stu-id="370b4-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="370b4-126">To metoder til som må implementeres, er **opportunityTitle** og **opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="370b4-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="370b4-127">Den første returnerer en kort tittel for salgsmuligheten, sistnevnte returnerer en detaljert beskrivelse av salgsmuligheten, som også kan inneholde data.</span><span class="sxs-lookup"><span data-stu-id="370b4-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="370b4-128">Tittelen som returneres av **opportunityTitle**, vises under **Optimaliseringssalgsmulighet**-kolonnen i **Optimaliseringsrådgiver**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="370b4-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="370b4-129">Den vises også som overskrift for sideruten som viser mer informasjon om salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="370b4-130">Etter konvensjonen dekoreres denne metoden med **DiagnosticRuleSubscription**-attributtet, som bruker følgende argumenter:</span><span class="sxs-lookup"><span data-stu-id="370b4-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="370b4-131">**Diagnoseområde** – En opplisting av typen **DiagnosticArea** som beskriver hvilket området i programmet regelen tilhører, for eksempel **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="370b4-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="370b4-132">**Regelnavn** – En streng med regelnavnet.</span><span class="sxs-lookup"><span data-stu-id="370b4-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="370b4-133">Dette vil vises **Regelnavn**-kolonnen i **Valideringsregel for diagnostikk**-skjemaet (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="370b4-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="370b4-134">**Kjøringsfrekvens** – En opplisting av typen **DiagnosticRunFrequency** som beskriver hvor ofte regelen skal kjøres, som **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="370b4-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="370b4-135">**Regelbeskrivelse** – En streng med en mer detaljert beskrivelse av regelen.</span><span class="sxs-lookup"><span data-stu-id="370b4-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="370b4-136">Dette vil vises **Regelbeskrivelse**-kolonnen i **Valideringsregel for diagnostikk**-skjemaet (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="370b4-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="370b4-137">**DiagnosticRuleSubscription**-attributtet er påkrevd for at regelen skal virke.</span><span class="sxs-lookup"><span data-stu-id="370b4-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="370b4-138">Vanligvis brukes det på **opportunityTitle**, men det kan dekorere alle metoder i klassen.</span><span class="sxs-lookup"><span data-stu-id="370b4-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="370b4-139">Nedenfor finner du en eksempelimplementering.</span><span class="sxs-lookup"><span data-stu-id="370b4-139">The following is an example implementation.</span></span> <span data-ttu-id="370b4-140">Rå-strenger brukes for enkelthetens skyld, men en riktig implementering krever etiketter.</span><span class="sxs-lookup"><span data-stu-id="370b4-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="370b4-141">Beskrivelsen returnert av **opportunityDetails** vises i sideruten, som viser mer informasjon om salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="370b4-142">Dette tar **SelfHealingOpportunity**-argumentet, som er **Data**-felt som kan brukes til å gi flere detaljer om salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="370b4-143">I eksemplet returnerer metoden ID-ene til tilbudsforespørselstilfellene med tom tittel.</span><span class="sxs-lookup"><span data-stu-id="370b4-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="370b4-144">De to gjenværende abstrakte metodene for å implementere, er **provideHealingAction** og **securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="370b4-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="370b4-145">**provideHealingAction** returnerer sann hvis en healing-handling angis, ellers returneres usann.</span><span class="sxs-lookup"><span data-stu-id="370b4-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="370b4-146">Hvis sann returneres, må metoden **performAction** implementeres, ellers vil det oppstod en feil.</span><span class="sxs-lookup"><span data-stu-id="370b4-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="370b4-147">**performAction**-metoden tar et **SelfHealingOpportunity**-argumentet, der dataene kan brukes for handlingen.</span><span class="sxs-lookup"><span data-stu-id="370b4-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="370b4-148">I eksemplet åpner handlingen **PurchRFQCaseTableListPage**, for manuell korrigering.</span><span class="sxs-lookup"><span data-stu-id="370b4-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="370b4-149">Avhengig av detaljene i regelen kan det være mulig å ta en automatisk handling ved hjelp av salgsmulighetsdataene.</span><span class="sxs-lookup"><span data-stu-id="370b4-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="370b4-150">I dette eksemplet kan systemet generere titler for tilbudsforespørselstilfeller automatisk.</span><span class="sxs-lookup"><span data-stu-id="370b4-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="370b4-151">**securityMenuItem** returnerer navnet på et handlingsmenyelement slik at regelen er bare synlig for brukere som har tilgang til handlingsmenyelementet.</span><span class="sxs-lookup"><span data-stu-id="370b4-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="370b4-152">Sikkerhet kan kreve at spesifikke regler og muligheter bare er tilgjengelige for autoriserte brukere.</span><span class="sxs-lookup"><span data-stu-id="370b4-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="370b4-153">I eksemplet er det bare brukere med tilgang til **PurchRFQCaseTitleAction** som kan vise salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="370b4-154">Legg merke til at dette handlingsmenyelementet ble opprettet for dette eksemplet, og ble lagt til som et inngangspunkt for **PurchRFQCaseTableMaintain**-sikkerhetsrettigheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="370b4-155">Menyelementet må være et handlingsmenyelement for at sikkerhet skal fungere riktig.</span><span class="sxs-lookup"><span data-stu-id="370b4-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="370b4-156">Andre menyelementtyper, for eksempel **Vis menyelementer**, fungerer ikke riktig.</span><span class="sxs-lookup"><span data-stu-id="370b4-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="370b4-157">Når regelen er kompilert, utfør den neste jobben slik at den vises i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="370b4-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="370b4-158">Regelen vil vises i **Valideringsregel for diagnostikk**-skjemaet, som er tilgjengelig fra **Systemadministrasjon** > **Periodiske oppgaver** > **Vedlikehold valideringsregel for diagnostikk**.</span><span class="sxs-lookup"><span data-stu-id="370b4-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="370b4-159">Hvis du vil at det skal evalueres, går du til **Systemadministrasjon** > **Periodiske oppgaver** > **Planlegg valideringsregel for diagnostikk** og velg frekvens for regelen, for eksempel **Daglig**.</span><span class="sxs-lookup"><span data-stu-id="370b4-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="370b4-160">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="370b4-160">Click **OK**.</span></span> <span data-ttu-id="370b4-161">Gå til **Systemadministrasjon** > **Optimaliseringsrådgiver** for å vise den nye salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="370b4-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="370b4-162">Eksemplet nedenfor er en kodesnutt med skjelettet til en regel, inkludert alle nødvendige metoder og attributter.</span><span class="sxs-lookup"><span data-stu-id="370b4-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="370b4-163">Det hjelper deg med å komme i gang med å skrive nye regler.</span><span class="sxs-lookup"><span data-stu-id="370b4-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="370b4-164"> Etikettene og handlingsmenyelementer som brukes i eksemplet, brukes bare til demonstrasjonsformål.</span><span class="sxs-lookup"><span data-stu-id="370b4-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="370b4-165">Hvis du vil ha mer informasjon, se den korte YouTube-videoen: [Optimaliseringsrådgiver i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="370b4-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
