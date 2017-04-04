---
title: Oppsett av behovsprognose
description: "Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Oppsett av behovsprognose

Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser.  

Oppsettoppgavene omfatter å konfigurere følgende data og parametere.

## <a name="item-allocation-key"></a>Varefordelingsnøkkel
En behovsprognose beregnes for en vare og dimensjonene bare hvis varen er en del av en varefordelingsnøkkel. Denne regelen til å gruppere et stort antall elementer, slik at behovsprognoser kan opprettes raskt. Den vare viktige tildelingsprosenten ignoreres når etterspørselen prognoser genereres. Prognoser opprettes basert på bare historiske data. 

En vare og dimensjonene må være en del av bare én varefordelingsnøkkel hvis varefordelingsnøkkelen brukes under oppretting av prognose. 

Hvis du vil legge til (SKU) en stock keeping unit en varetildelingsnøkkel, kan du gå til **Master planning**&gt;**Setup**&gt;**etterspørselen prognoser**&gt;**vare fordelingsnøkler**. Bruk siden **Tilordne varer** for å tilordne et element til en fordelingsnøkkel.

## <a name="intercompany-planning-groups"></a>Grupper for konsernintern planlegging
Behovsprognose genererer prognoser på tvers av firmaer. I Microsoft Dynamics 365 for operasjoner grupperes selskaper som er planlagt sammen i én konserninterne planleggingsgruppen. Hvis du vil angi per firma, hvilke varetildelingsnøkler skal vurderes for etterspørselen prognoser, knytte en varetildelingsnøkkel til konserninterne planlegging medlemmer ved å gå til **Master planning**&gt;**Setup**&gt;**konserninterne planleggingsgrupper**. 

Hvis ingen Varetildelingsnøkler som er tilordnet til medlemmer av konsernintern planleggingsgruppe, beregnes en behovsprognose som standard for alle varer som er tilordnet alle varetildelingsnøkler fra alle Dynamics 365 for operasjoner selskaper. Flere filtreringsalternativer for firmaer og varefordelingsnøkler er tilgjengelig på siden **Generer statistisk basislinjeprognose**. 

Se gjennom antall varer som er prognostisert. Unødvendige varer kan føre til økte kostnader når du bruker Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Parametere for behovsprognose
Hvis du vil definere etterspørselen prognoser parametere, kan du gå til **Master planning**&gt;**Setup**&gt;**etterspørselen prognoser parametere**. Fordi behovsprognose kjører mellom firmaer er oppsettet globalt. Oppsettes brukes med andre ord for alle selskaper. 

Behovsprognose genererer prognosen i antall. Enheten som antallet som skal uttrykkes i, må derfor angis i feltet **Behovsprognoseenhet**. Måleenheten må være unik for å hjelpe å garantere at aggregering og prosentvis fordeling gir mening. Hvis du vil ha mer informasjon om aggregering og prosentvis fordeling, se [Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md). For hver måleenhet som skal brukes for lagerføringsenheter som er inkludert i behovsprognose, kontrollerer du at det er en regel for konvertering for måleenheten og den generelle måleenheten for prognose. Når prognosegenerering kjøres, logges listen over varer som ikke har en konvertering av måleenhet, slik at du lett kan korrigere oppsettet. 

Behovsprognose kan brukes til å beregne både avhengig og uavhengig behov. Hvis for eksempel bare boksen **Salgsordre** er merket, og hvis alle varene som vurderes for behovsprognose er varer som selges, beregner systemet uavhengig behov. Kritiske delkomponenter kan imidlertid legges til i varefordelingsnøkler og inkluderes i behovsprognose. I så fall, hvis boksen **Produksjonslinje** er merket, beregnes en avhengige prognose. 

Det finnes to metoder for å opprette en opprinnelig plan prognose i Dynamics 365 for operasjoner. Du kan bruke Prognose modeller på toppen av historiske data, eller du kan bare kopiere over historiske data til prognosen. Feltet **Strategi for prognosegenerering** lar deg velge mellom disse to metodene. For å bruke prognosemodeller velg **Azure Machine Learning**. 

Ved å klikke **Prognosedimensjoner** i den venstre ruten på siden **Parametere for behovsprognose** du kan også velge settet for prognosedimensjoner som skal brukes når behovsprognosen genereres. En prognosedimensjon angir detaljnivået som prognosen er definert for. Firma, område og varefordelingsnøkkel er obligatoriske prognosedimensjoner, men du kan også generere prognoser på nivåene for lageret, lagerstatus, kundegruppe, kundekonto, land/område, tilstand, og varen pluss alle varedimensjoner. 

Du kan legge til prognosedimensjoner i listen over dimensjonene som skal brukes for behovsprognose, når som helst. Du kan også fjerne prognosedimensjoner fra listen. Manuelle justeringer går imidlertid tapt hvis du legger til eller fjerner en prognosedimensjon. 

Ikke alle varer fungerer på samme måte fra et behovsprognoseperspektiv. Lignende varer kan grupperes i én varefordelingsnøkkel, og parametere, for eksempel transaksjonstyper og prognosemetodeinnstillinger, kan angis per varefordelingsnøkkel. Klikk **Varefordelingsnøkler** i den venstre ruten på siden **Parametere for behovsprognose**. 

Hvis du vil generere prognosen, bruker Dynamics 365 for operasjoner en maskin-læring på Internett. Hvis du vil koble til tjenesten, må du oppgi Dynamics 365 for operasjoner følgende informasjon hvis du logger på Microsoft Azure maskin Learning Studio:

-   API-nøkkel (application programming interface) for webtjenesten
-   URL-adresse til webtjenestesluttpunkt
-   Azure-lagringskontonavn
-   Azure-lagringskontonøkkel

**Obs!** Azure-lagringskontonavnet og -nøkkel kreves bare hvis du bruker en egendefinert lagring-konto. Hvis du distribuerer den lokale versjonen, må du ha en egendefinert lagring konto på Azure, slik at maskinen opplæring-tjenesten får tilgang til den historiske data. 

Hvis du vil opprette behov forutsigelser, kan du distribuere din egen service ved å bruke maskinen Learning Studio eller Dynamics-365 for operasjoner etterspørselen prognoser Eksperimenter. Instruksjoner for distribusjon av Dynamics-365 for operasjoner behov prognostisering Eksperimenter som en webtjeneste er tilgjengelig Dynamics 365 for operasjoner. På siden **Parametere for behovsprognose** klikker du **Azure Machine Learning** kategorien.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Innstillinger for Dynamics-365 for operasjoner krever prognostisering læring Telefakstjeneste
Hvis du vil vise parametere som kan konfigureres for Dynamics-365 for operasjoner krever prognostisering service, kan du gå til **hovedplanlegging**&gt;**Setup**&gt;**etterspørselen prognoser**&gt;**prognoser Algoritmeparametere**. Den **prognoser Algoritmeparametere** siden viser standardverdiene for parameterne. Du kan overskrive disse parameterne på den **etterspørselen prognoser parametere** siden. Bruk kategorien **Generelt** for å overskrive parameterne globalt, eller bruk kategorien **Varefordelingsnøkler** for å overskrive parameterne pr. varefordelingsnøkkel. Parametere som er overskrevet med en varefordelingsnøkkel påvirker bare prognosen for varer som er knyttet til denne varefordelingsnøkkelen.

<a name="see-also"></a>Se også
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


