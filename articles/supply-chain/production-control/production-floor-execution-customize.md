---
title: Tilpass grensesnittet for produksjonsutførelse
description: Dette emnet beskriver hvordan du utvider gjeldende skjemaer eller oppretter nye skjemaer og knapper i grensesnittet for produksjonsutførelse.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790986"
---
# <a name="customize-the-production-floor-execution-interface"></a>Tilpass grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Utviklere kan utvide sine egne skjemaer eller opprette nye skjemaer og knapper i grensesnittet for produksjonsutførelse. Når du har lagt til koden for disse nye elementene, kan administratorer eller produksjonssjefer enkelt legge dem til grensesnittet ved hjelp av standard konfigurasjonskontroller.

Her er for eksempel noen av de mulige løsningene hvis det trengs nye kolonner i et hovedskjema:

- Utvid `JmgProductionFloorExecutionMainGrid`-skjemaet, og legg til de ønskede feltene.
- Opprett et nytt skjema, og legg det til som en ny hovedvisning (fane).

## <a name="add-a-new-button-action"></a>Legg til en ny knapp (handling)

Hvis du vil legge til en ny knapp (handling), følger du denne fremgangsmåten for å opprette en klasse som implementerer den egendefinerte handlingen.

1. Opprett en ny klasse med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, der:

    - `<ExtensionPrefix>` unikt identifiserer løsningen, vanligvis ved å bruke firmanavnet.
    - `<ActionName>` er et unikt navn for klassen. Det identifiserer vanligvis handlingen.

1. Den nye klassen må utvide `JmgProductionFloorExecutionAction`-klassen.
1. Overstyr alle nødvendige metoder.

Se for eksempel på koden for følgende klasser:

- `JmgProductionFloorExecutionBreakAction` – En klasse for en enkel handling som ikke trenger noen poster.
- `JmgProductionFloorExecutionReportFeedbackAction` – En klasse som gir mer kompleks funksjonalitet.

Når du er ferdig, vises den nye knappen (handlingen) automatisk på siden **Utform faner** i Microsoft Dynamics 365 Supply Chain Management. Der kan du (eller en administrator eller produksjonssjef) enkelt legge den til på den primære eller sekundære verktøylinjen, på samme måte som du kan legge til standardknappene. For instruksjoner, se [Utform grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Legg til en ny hovedvisning

1. Opprett et nytt skjema med ønskede elementer og funksjonalitet. Legg merke til at dette skjemaet er et nytt skjema, ikke en utvidelse. Gi skjemaet navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, der:

    - `<ExtensionPrefix>` unikt identifiserer løsningen, vanligvis ved å bruke firmanavnet.
    - `<FormName>` er et unikt navn for skjemaet.

1. Opprett et menyelement med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Opprett en utvidelse med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, der `getMainMenuItemsList`-metoden utvides ved å legge til det nye menyelementet i listen. Koden nedenfor viser et eksempel.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Når du er ferdig, vises den nye hovedvisningen automatisk i kombinasjonsboksen **Hovedvisning** på siden **Utform faner** i Supply Chain Management. Der kan du (eller en administrator eller produksjonssjef) enkelt legge den til på nye eller eksisterende faner, på samme måte som du kan legge til standard hovedvisninger. For instruksjoner, se [Utform grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Legg til en detaljvisning

1. Opprett et nytt skjema med ønskede elementer og funksjonalitet. Legg merke til at dette skjemaet er nytt, ikke en utvidelse. Gi skjemaet navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, der: 

    - `<ExtensionPrefix>` unikt identifiserer løsningen, vanligvis ved å bruke firmanavnet.
    - `<FormName>` er et unikt navn for skjemaet.

1. Opprett et menyelement med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Opprett en utvidelse med navnet `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, der `getDetailsMenuItemList`-metoden utvides ved å legge til det nye menyelementet i listen.

Når du er ferdig, vises den nye detaljvisningen automatisk i kombinasjonsboksen **Detaljvisning** på siden **Utform faner** i Supply Chain Management. Der kan du (eller en administrator eller produksjonssjef) enkelt legge den til på nye eller eksisterende faner, på samme måte som du kan legge til standard detaljvisninger. For instruksjoner, se [Utform grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Legg til et numerisk tastatur i et skjema eller en dialogboks

Følgende eksempel viser hvordan du legger til numeriske tastaturer i et skjema.

1. Antall kontroller for numeriske tastaturer som hvert skjema inneholder, må være likt antallet numeriske tastaturer i dette skjemaet.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Konfigurer virkemåten for hver kontroll for numerisk tastatur, og koble hver kontroll for numerisk tastatur til en skjemadel for numerisk tastatur.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Bruk et numerisk tastatur som en popup-dialogboks

Følgende eksempel viser en måte for konfigurering av en kontroll for numerisk tastatur for en popup-dialogboks.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Følgende eksempel viser en måte for å kalle opp popup-dialogboksen for numerisk tastatur.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>Tilleggsressurser

- [Utforme grensesnittet for produksjonsutførelse](production-floor-execution-styles.md)
- [Utforme grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md)
