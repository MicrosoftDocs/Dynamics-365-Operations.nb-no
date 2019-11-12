---
title: Oppsett av behovsprognose
description: Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c689df9b00ad2d4ce161c6fdb1193f48cacbfcbc
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653517"
---
# <a name="demand-forecasting-setup"></a>Oppsett av behovsprognose

[!include [banner](../includes/banner.md)]

Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser.  

Oppsettoppgavene omfatter å konfigurere følgende data og parametere.

## <a name="item-allocation-key"></a>Varefordelingsnøkkel
En behovsprognose beregnes for en vare og dimensjonene bare hvis varen er en del av en varefordelingsnøkkel. Denne regelen brukes for å gruppere et stort antall varer, slik at behovsprognoser kan opprettes raskere. Varefordelingsnøkkelprosenten ignoreres når behovsprognoser genereres. Prognoser opprettes basert på bare historiske data. 

En vare og dimensjonene må være en del av bare én varefordelingsnøkkel hvis varefordelingsnøkkelen brukes under oppretting av prognose. 

Hvis du vil legge til en lagerenhet (SKU) i en varefordelingsnøkkel, gå til **Hovedplanlegging** &gt; **Oppsett** &gt; **Behovsprognose** &gt; **Varefordelingsnøkler**. Bruk siden **Tilordne varer** for å tilordne et element til en fordelingsnøkkel.

## <a name="intercompany-planning-groups"></a>Grupper for konsernintern planlegging
Behovsprognose genererer prognoser på tvers av firmaer. I Dynamics 365 Supply Chain Management grupperes firmaer som er planlagt sammen, i én konsernintern planleggingsgruppe. Hvis du vil angi per firma hvilke varefordelingsnøkler som skal vurderes for behovsprognose, knytter du en varefordelingsnøkkel til det konserninterne planleggingsgruppemedlemmet ved å gå til **Hovedplanlegging** &gt; **Oppsett** &gt; **Konserninterne planleggingsgrupper**. 

Hvis ingen varefordelingsnøkler er tilordnet til medlemmer av konsernintern planleggingsgruppe, beregnes en behovsprognose som standard for alle varer som er tilordnet til alle varefordelingsnøkler fra alle firmaer. Flere filtreringsalternativer for firmaer og varefordelingsnøkler er tilgjengelig på siden **Generer statistisk basislinjeprognose**. 

Se gjennom antall varer som er prognostisert. Unødvendige varer kan føre til økte kostnader når du bruker Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Parametere for behovsprognose
Hvis du vil definere parametere for behovsprognose, kan du gå til **Hovedplanlegging** &gt; **Oppsett** &gt; **Parametere for behovsprognose**. Fordi behovsprognose kjører mellom firmaer er oppsettet globalt. Oppsettes brukes med andre ord for alle selskaper. 

Behovsprognose genererer prognosen i antall. Enheten som antallet som skal uttrykkes i, må derfor angis i feltet **Behovsprognoseenhet**. Måleenheten må være unik for å hjelpe å garantere at aggregering og prosentvis fordeling gir mening. Hvis du vil ha mer informasjon om aggregering og prosentvis fordeling, se [Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md). For hver måleenhet som skal brukes for lagerføringsenheter som er inkludert i behovsprognose, kontrollerer du at det er en regel for konvertering for måleenheten og den generelle måleenheten for prognose. Når prognosegenerering kjøres, logges listen over varer som ikke har en konvertering av måleenhet, slik at du lett kan korrigere oppsettet. 

Behovsprognose kan brukes til å beregne både avhengig og uavhengig behov. Hvis for eksempel bare boksen **Salgsordre** er merket, og hvis alle varene som vurderes for behovsprognose er varer som selges, beregner systemet uavhengig behov. Kritiske delkomponenter kan imidlertid legges til i varefordelingsnøkler og inkluderes i behovsprognose. I så fall, hvis boksen **Produksjonslinje** er merket, beregnes en avhengige prognose. 

Det finnes to metoder for å opprette en basislinjeprognose. Du kan bruke Prognose modeller på toppen av historiske data, eller du kan bare kopiere over historiske data til prognosen. Feltet **Strategi for prognosegenerering** lar deg velge mellom disse to metodene. For å bruke prognosemodeller velg **Azure Machine Learning**. 

Ved å klikke **Prognosedimensjoner** i den venstre ruten på siden **Parametere for behovsprognose** du kan også velge settet for prognosedimensjoner som skal brukes når behovsprognosen genereres. En prognosedimensjon angir detaljnivået som prognosen er definert for. Firma, område og varefordelingsnøkkel er obligatoriske prognosedimensjoner, men du kan også generere prognoser på nivåene for lageret, lagerstatus, kundegruppe, kundekonto, land/område, tilstand, og varen pluss alle varedimensjoner. 

Du kan legge til prognosedimensjoner i listen over dimensjonene som skal brukes for behovsprognose, når som helst. Du kan også fjerne prognosedimensjoner fra listen. Manuelle justeringer går imidlertid tapt hvis du legger til eller fjerner en prognosedimensjon. 

Ikke alle varer fungerer på samme måte fra et behovsprognoseperspektiv. Lignende varer kan grupperes i én varefordelingsnøkkel, og parametere, for eksempel transaksjonstyper og prognosemetodeinnstillinger, kan angis per varefordelingsnøkkel. Klikk **Varefordelingsnøkler** i den venstre ruten på siden **Parametere for behovsprognose**. 

Hvis du vil generere prognosen, bruker Supply Chain Management en Machine Learning-webtjeneste. Hvis du vil koble til tjenesten, må du angi informasjonen nedenfor hvis du logger deg på Microsoft Azure Machine Learning Studio:

-   API-nøkkel (application programming interface) for webtjenesten
-   URL-adresse til webtjenestesluttpunkt
-   Azure-lagringskontonavn
-   Azure-lagringskontonøkkel

**Obs!** Azure-lagringskontonavnet og -nøkkel kreves bare hvis du bruker en egendefinert lagring-konto. Hvis du distribuerer den lokale versjonen, må du ha en konto for egendefinert lagring på Azure, slik at Machine Learning-tjenesten får tilgang til historiske data. 

Hvis du vil opprette behovsprediksjoner, kan du distribuere din egen tjeneste ved å bruke Machine Learning Studio eller behovsprognoseeksperimenter for Supply Chain Management. Instruksjoner for distribusjon av behovsprognoseeksperimenter som en webtjeneste er tilgjengelige i Supply Chain Management. På siden **Parametere for behovsprognose** klikker du **Azure Machine Learning** kategorien.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Innstillinger for behovsprognose for Machine Learning-tjenesten
Hvis du vil vise parametere som kan konfigureres for behovsprognosetjenesten, kan du gå til **Hovedplanlegging** &gt; **Oppsett** &gt; **Behovsprognose** &gt; **Prognosealgoritmeparametere**. Siden **Prognosealgoritmeparametere** viser standardverdiene for parameterne. Du kan overskrive disse parameterne på siden **Parametere for behovsprognose**. Bruk kategorien **Generelt** for å overskrive parameterne globalt, eller bruk kategorien **Varefordelingsnøkler** for å overskrive parameterne pr. varefordelingsnøkkel. Parametere som er overskrevet med en varefordelingsnøkkel påvirker bare prognosen for varer som er knyttet til denne varefordelingsnøkkelen.

### <a name="forecast-algorithm-parameters"></a>Prognosealgoritmeparametere

I kategorien **Tilordningsnøkler** kan du angi parameterne **Prognosealgoritmeparametere** for hver varefordelingsnøkkel. Følgende alternativer er tilgjengelige:
- **Konfidensnivåprosent**: Konfidensintervallet består av et verdiområde som fungerer som gode estimater for behovsprognosen. En konfidensnivåprosent på 95 % angir at det er 5 % risiko for at det fremtidige behovet faller utenfor området for konfidensintervallet.
- **Fremtving sesongavhengighet**: Angir om modellen skal tvinges til å bruke en bestemt type sesongavhengighet. Gjelder bare for ARIMA og ETS. Alternativer: AUTO (standard), INGEN, ADDITIVE, MULTIPLIKATIV.
- **Prognosemodell**: Alternativer: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALLE. Hvis du vil velge best mulig tilpasningsmodell, bruker du **ALLE**.
- **Maksimal prognoseverdi**: Angir den største verdien som kan brukes for prognoser. Format: +1E[n] eller numerisk konstant.
- **Minste prognoseverdi**: Angir den minste verdien som kan brukes for prognoser. Format: -1E[n] eller numerisk konstant.
- **Mangler verdierstatning**: Angir hvordan hull i historiske data fylles. Alternativer: numerisk verdi, GJENNOMSNITT, FORRIGE, INTERPOLERT LINEÆR, INTERPOLERT POLYNOMISK.
- **Mangler verdierstatningsområde**: Angir om verdierstatning bare gjelder for dataområdet for hvert enkelt detaljattributt eller for hele datasettet. Alternativer: GRANULARITY_ATTRIBUTE (standard), GLOBAL.
- **Tips om sesongavhengighet**: For sesongbaserte data angir du et tips til prognosemodellen for å forbedre prognosenøyaktigheten. Format: heltall, som representerer antallet perioder som et behovsmønster gjentar seg selv etter. Fyll for eksempel inn 6 for data som gjentar seg selv hver sjette måned.
- **Prosentandel testsettstørrelse**: Prosentandel historiske data som skal brukes som et testsett for beregning av prognosenøyaktighet. 

<a name="additional-resources"></a>Tilleggsressurser
--------

[Innføring i behovsprognoser](introduction-demand-forecasting.md)

[Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)

[Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)



