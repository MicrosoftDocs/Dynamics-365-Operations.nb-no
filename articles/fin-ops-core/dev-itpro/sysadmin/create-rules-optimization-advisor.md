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
# <a name="create-rules-for-optimization-advisor"></a>Opprette regler for optimaliseringsrådgiver

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter nye regler for **optimaliseringsrådgiver**. Du kan for eksempel opprette en ny regel som identifiserer tilbudsforespørselssakene som har en tom tittel. Bruk av titler på saker gjør dem lett å kjenne igjen og søkbare. Dette eksemplet som er ganske enkelt, viser hva som kan oppnås med optimaliseringsregler. 

En *regel* er en sjekk av programdata. Hvis betingelsen som denne regelen evaluerer, er oppfylt, opprettes salgsmuligheter for å optimalisere prosesser eller forbedre data. Salgsmulighetene kan brukes, og eventuelt virkningen av handlingene kan måles. 

Hvis du vil opprette en ny regel for **optimaliseringsrådgiver**, legger du til en ny klasse som utvider den abstrakte **SelfHealingRule**-klassen, implementerer **IDiagnosticsRule**-grensesnittet og dekoreres av **DiagnosticRule**-attributtet. Klassen må også ha en metode som er dekorert med **DiagnosticsRuleSubscription**-attributtet. Etter konvensjonen utføres dette i **opportunityTitle**-metoden, som diskuteres senere. Denne nye klassen kan legges til en egendefinert modell med en avhengighetsforhold til **SelfHealingRules**-modellen. I eksemplet nedenfor kalles regelen som implementeres **RFQTitleSelfHealingRule**.

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

**SelfHealingRule**-abstraktklassen har abstrakte metoder som må implementeres i arveklasser. Kjernen er **evaluer**-metoden, som returnerer en liste over salgsmuligheter som er identifisert av regelen. Salgsmuligheter kan være per juridisk enhet, eller kan gjelde for hele systemet.

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

Metoden ovenfor gjentas over firmaer og velger tilbudsforespørselstilfeller med tomme titler i **findRFQCasesWithEmptyTitle**-metoden. Hvis minst ett slikt tilfelle blir funnet, opprettes en firmaspesifikk salgsmulighet med **getOpportunityForCompany**-metoden. Legg merke til at feltet **Data** i **SelfHealingOpportunity**-tabellen er av typen **Beholder**, og kan derfor inneholde alle data som er relevante for logikken som gjelder denne regelen. Angivelse av **OpportunityDate** med gjeldende tidsangivelse registrerer tidspunktet for den siste evalueringen av salgsmuligheten.  

Salgsmuligheter kan også være på tvers av firmaer. I så fall er ikke løkken over firmaer nødvendig og salgsmuligheten må opprettes med **getOpportunityAcrossCompanies**-metoden. 

Koden nedenfor viser **findRFQCasesWithEmptyTitle**-metoden, som returnerer ID-ene til tilbudsforespørselssakene som har tomme titler.

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

To metoder til som må implementeres, er **opportunityTitle** og **opportunityDetails**. Den første returnerer en kort tittel for salgsmuligheten, sistnevnte returnerer en detaljert beskrivelse av salgsmuligheten, som også kan inneholde data.

Tittelen som returneres av **opportunityTitle**, vises under **Optimaliseringssalgsmulighet**-kolonnen i **Optimaliseringsrådgiver**-arbeidsområdet. Den vises også som overskrift for sideruten som viser mer informasjon om salgsmuligheten. Etter konvensjonen dekoreres denne metoden med **DiagnosticRuleSubscription**-attributtet, som bruker følgende argumenter: 

* **Diagnoseområde** – En opplisting av typen **DiagnosticArea** som beskriver hvilket området i programmet regelen tilhører, for eksempel **DiagnosticArea::SCM**. 

* **Regelnavn** – En streng med regelnavnet. Dette vil vises **Regelnavn**-kolonnen i **Valideringsregel for diagnostikk**-skjemaet (**DiagnosticsValidationRuleMaintain**). 

* **Kjøringsfrekvens** – En opplisting av typen **DiagnosticRunFrequency** som beskriver hvor ofte regelen skal kjøres, som **DiagnosticRunFrequency::Daily**. 

* **Regelbeskrivelse** – En streng med en mer detaljert beskrivelse av regelen. Dette vil vises **Regelbeskrivelse**-kolonnen i **Valideringsregel for diagnostikk**-skjemaet (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> **DiagnosticRuleSubscription**-attributtet er påkrevd for at regelen skal virke. Vanligvis brukes det på **opportunityTitle**, men det kan dekorere alle metoder i klassen.

Nedenfor finner du en eksempelimplementering. Rå-strenger brukes for enkelthetens skyld, men en riktig implementering krever etiketter. 

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

Beskrivelsen returnert av **opportunityDetails** vises i sideruten, som viser mer informasjon om salgsmuligheten. Dette tar **SelfHealingOpportunity**-argumentet, som er **Data**-felt som kan brukes til å gi flere detaljer om salgsmuligheten. I eksemplet returnerer metoden ID-ene til tilbudsforespørselstilfellene med tom tittel. 

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

De to gjenværende abstrakte metodene for å implementere, er **provideHealingAction** og **securityMenuItem**. 

**provideHealingAction** returnerer sann hvis en healing-handling angis, ellers returneres usann. Hvis sann returneres, må metoden **performAction** implementeres, ellers vil det oppstod en feil. **performAction**-metoden tar et **SelfHealingOpportunity**-argumentet, der dataene kan brukes for handlingen. I eksemplet åpner handlingen **PurchRFQCaseTableListPage**, for manuell korrigering. 

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

Avhengig av detaljene i regelen kan det være mulig å ta en automatisk handling ved hjelp av salgsmulighetsdataene. I dette eksemplet kan systemet generere titler for tilbudsforespørselstilfeller automatisk. 

**securityMenuItem** returnerer navnet på et handlingsmenyelement slik at regelen er bare synlig for brukere som har tilgang til handlingsmenyelementet. Sikkerhet kan kreve at spesifikke regler og muligheter bare er tilgjengelige for autoriserte brukere. I eksemplet er det bare brukere med tilgang til **PurchRFQCaseTitleAction** som kan vise salgsmuligheten. Legg merke til at dette handlingsmenyelementet ble opprettet for dette eksemplet, og ble lagt til som et inngangspunkt for **PurchRFQCaseTableMaintain**-sikkerhetsrettigheten. 

> [!NOTE]
> Menyelementet må være et handlingsmenyelement for at sikkerhet skal fungere riktig. Andre menyelementtyper, for eksempel **Vis menyelementer**, fungerer ikke riktig.

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Når regelen er kompilert, utfør den neste jobben slik at den vises i brukergrensesnittet.

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

Regelen vil vises i **Valideringsregel for diagnostikk**-skjemaet, som er tilgjengelig fra **Systemadministrasjon** > **Periodiske oppgaver** > **Vedlikehold valideringsregel for diagnostikk**. Hvis du vil at det skal evalueres, går du til **Systemadministrasjon** > **Periodiske oppgaver** > **Planlegg valideringsregel for diagnostikk** og velg frekvens for regelen, for eksempel **Daglig**. Klikk **OK**. Gå til **Systemadministrasjon** > **Optimaliseringsrådgiver** for å vise den nye salgsmuligheten. 

Eksemplet nedenfor er en kodesnutt med skjelettet til en regel, inkludert alle nødvendige metoder og attributter. Det hjelper deg med å komme i gang med å skrive nye regler. Etikettene og handlingsmenyelementer som brukes i eksemplet, brukes bare til demonstrasjonsformål.

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

Hvis du vil ha mer informasjon, se den korte YouTube-videoen: [Optimaliseringsrådgiver i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
