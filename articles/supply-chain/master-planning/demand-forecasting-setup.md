---
title: Oppsett av behovsprognose
description: Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser.
author: ChristianRytt
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f71d7a1ef2e8b6a113124d3fb17f1681d62aed9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575758"
---
# <a name="demand-forecasting-setup"></a>Oppsett av behovsprognose

[!include [banner](../includes/banner.md)]

Dette emnet beskriver konfigurasjonsoppgavene du må utføre for å klargjøre behovsprognoser.  

Oppsettoppgavene omfatter å konfigurere følgende data og parametere.

## <a name="item-allocation-keys"></a>Varefordelingsnøkler

En behovsprognose beregnes for en vare og dimensjonene bare hvis varen er en del av en varefordelingsnøkkel. Denne regelen brukes for å gruppere et stort antall varer, slik at behovsprognoser kan opprettes raskere. Varefordelingsnøkkelprosenten ignoreres når behovsprognoser genereres. Prognoser opprettes basert på bare historiske data.

En vare og dimensjonene må være en del av bare én varefordelingsnøkkel hvis varefordelingsnøkkelen brukes under oppretting av prognose.

Hvis du vil legge til en lagerenhet (SKU) i en varefordelingsnøkkel, gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Varefordelingsnøkler**. Bruk siden **Tilordne varer** for å tilordne et element til en fordelingsnøkkel.

## <a name="intercompany-planning-groups"></a>Grupper for konsernintern planlegging

Behovsprognose genererer prognoser på tvers av firmaer. I Dynamics 365 Supply Chain Management grupperes firmaer som er planlagt sammen, i én konsernintern planleggingsgruppe. Hvis du vil angi per firma hvilke varefordelingsnøkler som skal vurderes for behovsprognose, knytter du en varefordelingsnøkkel til det konserninterne planleggingsgruppemedlemmet ved å gå til **Hovedplanlegging \> Oppsett \> Konserninterne planleggingsgrupper**.

Hvis ingen varefordelingsnøkler er tilordnet til medlemmer av konsernintern planleggingsgruppe, beregnes en behovsprognose som standard for alle varer som er tilordnet til alle varefordelingsnøkler fra alle firmaer. Flere filtreringsalternativer for firmaer og varefordelingsnøkler er tilgjengelig på siden **Generer statistisk basislinjeprognose**.

Se gjennom antall varer som er prognostisert. Unødvendige varer kan føre til økte kostnader når du bruker Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Parametere for behovsprognose

Hvis du vil definere parametere for behovsprognose, kan du gå til **Hovedplanlegging \> Oppsett \> \> Behovsprognose \> Parametere for behovsprognose**. Fordi behovsprognose kjører mellom firmaer er oppsettet globalt. Dette betyr at oppsettet brukes for alle selskaper.

Behovsprognose genererer prognosen i antall. Enheten som antallet som skal uttrykkes i, må derfor angis i feltet **Behovsprognoseenhet**. Måleenheten må være unik for å hjelpe å sikre at aggregering og prosentvis fordeling gir mening. Hvis du vil ha mer informasjon om aggregering og prosentvis fordeling, se [Gjøre manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md). For hver måleenhet som skal brukes for lagerføringsenheter som er inkludert i behovsprognose, kontrollerer du at det er en regel for konvertering for måleenheten og den generelle måleenheten for prognose. Når prognosegenerering kjøres, logges listen over varer som ikke har en konvertering av måleenhet, slik at du lett kan korrigere oppsettet.

Behovsprognose kan brukes til å beregne både avhengig og uavhengig behov. Hvis for eksempel bare boksen **Salgsordre** er merket, og hvis alle varene som vurderes for behovsprognose er varer som selges, beregner systemet uavhengig behov. Kritiske delkomponenter kan imidlertid legges til i varefordelingsnøkler og inkluderes i behovsprognose. I så fall, hvis boksen **Produksjonslinje** er merket, beregnes en avhengige prognose.

Det finnes to metoder for å opprette en basislinjeprognose. Du kan bruke Prognose modeller på toppen av historiske data, eller du kan bare kopiere over historiske data til prognosen. Feltet **Strategi for prognosegenerering** lar deg velge mellom disse to metodene. For å bruke prognosemodeller velg **Azure Machine Learning**.

Ved å velge **Prognosedimensjoner** i den venstre ruten på siden **Parametere for behovsprognose** du kan også velge settet for prognosedimensjoner som skal brukes når behovsprognosen genereres. En prognosedimensjon angir detaljnivået som prognosen er definert for. Firma, område og varefordelingsnøkkel er obligatoriske prognosedimensjoner, men du kan også generere prognoser på nivåene for lageret, lagerstatus, kundegruppe, kundekonto, land/område, tilstand, og varen pluss alle varedimensjoner.

Du kan legge til prognosedimensjoner i listen over dimensjonene som skal brukes for behovsprognose, når som helst. Du kan også fjerne prognosedimensjoner fra listen. Manuelle justeringer går imidlertid tapt hvis du legger til eller fjerner en prognosedimensjon.

Ikke alle varer fungerer på samme måte fra et behovsprognoseperspektiv. Lignende varer kan grupperes i én varefordelingsnøkkel, og parametere, for eksempel transaksjonstyper og prognosemetodeinnstillinger, kan angis per varefordelingsnøkkel. Velg **Varefordelingsnøkler** i den venstre ruten på siden **Parametere for behovsprognose**.

Hvis du vil generere prognosen, bruker Supply Chain Management en Machine Learning-webtjeneste. Hvis du vil koble til tjenesten, må du angi informasjonen nedenfor hvis du logger deg på Microsoft Azure Machine Learning Studio (klassisk):

- API-nøkkel (application programming interface) for webtjenesten
- URL-adresse til webtjenestesluttpunkt
- Azure-lagringskontonavn
- Azure-lagringskontonøkkel

> [!NOTE]
> Azure-lagringskontonavnet og -nøkkel kreves bare hvis du bruker en egendefinert lagring-konto. Hvis du distribuerer den lokale versjonen, må du ha en konto for egendefinert lagring på Azure, slik at Machine Learning får tilgang til historiske data.

Hvis du vil opprette behovsprediksjoner, kan du distribuere din egen tjeneste ved å bruke Machine Learning Studio eller behovsprognoseeksperimenter for Supply Chain Management. Instruksjoner for distribusjon av behovsprognoseeksperimenter som en webtjeneste er tilgjengelige i Supply Chain Management. På siden **Parametere for behovsprognose** åpner du **Azure Machine Learning**-fanen.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Innstillinger for behovsprognose for Machine Learning-tjenesten

Hvis du vil vise parametere som kan konfigureres for behovsprognosetjenesten, kan du gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Prognosealgoritmeparametere**. Siden **Prognosealgoritmeparametere** viser standardverdiene for parameterne. Du kan overskrive disse parameterne ved å gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Parametere for behovsprognose**, der du kan gjøre følgende:

- Bruk kategorien **Generelt** til å overskrive parameterne globalt.
- Bruk kategorien **Varetildelingsnøkler** til å overskrive parameterne per varetildelingsnøkkel. Parametere som er overskrevet med en varefordelingsnøkkel påvirker bare prognosen for varer som er knyttet til denne varefordelingsnøkkelen.

### <a name="forecast-algorithm-parameters"></a>Prognosealgoritmeparametere

På **Varetildelingsnøkler**-fanen på siden **Parametere for behovsprognose** kan du bruke hurtigkategorien for **Prognosealgoritmeparametere** til å tilordne prognosealgoritmeparametere for varetildelingsnøkkelen som for øyeblikket er valgt i rutenettet til venstre. Bruk knappene **Legg til** og **Fjern** på verktøylinjen for å fastsette den nødvendige samlingen med parametere. For hver parameter i listen velger du en av følgende verdier i **Navn**-feltet, og deretter angir du en passende verdi i **Verdi**-feltet:

- **Konfidensnivåprosent** – Et konfidensintervall består av et verdiområde som fungerer som gode estimater for behovsprognosen. En konfidensnivåprosent på 95 % angir at det er 5 % risiko for at det fremtidige behovet faller utenfor området for konfidensintervallet.
- **Fremtving sesongavhengighet** – Angir om modellen skal tvinges til å bruke en bestemt type sesongavhengighet. Gjelder bare for ARIMA og ETS. Alternativer: AUTO (standard), INGEN, ADDITIVE, MULTIPLIKATIV.
- **Prognosemodell** – Alternativer: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALLE. Hvis du vil velge best mulig tilpasningsmodell, bruker du **ALLE**.
- **Maksimal prognoseverdi** – Angir den største verdien som kan brukes for prognoser. Format: +1E[n] eller numerisk konstant.
- **Minste prognoseverdi** – Angir den minste verdien som kan brukes for prognoser. Format: -1E[n] eller numerisk konstant.
- **Mangler verdierstatning** – Angir hvordan hull i historiske data fylles. Alternativer: numerisk verdi, GJENNOMSNITT, FORRIGE, INTERPOLERT LINEÆR, INTERPOLERT POLYNOMISK.
- **Mangler verdierstatningsområde** – Angir om verdierstatning bare gjelder for datoområdet for hvert enkelt detaljattributt eller for hele datasettet. Følgende alternativer er tilgjengelige for oppretting av datoområdet som systemet bruker til å fylle ut huller i historiske data:

  - GLOBAL – Systemet bruker hele datoområdet for alle detaljattributter.
  - HISTORY_DATE_RANGE – Systemet bruker et bestemt datoområde som er definert av feltene **Fra dato** og **Til dato** i **Historisk horisont**-feltgruppen i dialogboksen **Generer statistisk basislinjeprognose**.
  - GRANULARITY_ATTRIBUTE – Systemet bruker datoområdet til det behandlede detaljattributtet.

  > [!NOTE]
  > Et detaljattributt er en kombinasjon av prognosedimensjoner som prognosen utføres mot. Du kan definere prognosedimensjoner på siden **Parametere for behovsprognose**.

- **Tips om sesongavhengighet** – For sesongbaserte data angir du et tips til prognosemodellen for å forbedre prognosenøyaktigheten. Format: heltall, som representerer antallet perioder som et behovsmønster gjentar seg selv etter. Fyll for eksempel inn 6 for data som gjentar seg selv hver sjette måned.
- **Prosentandel testsettstørrelse** – Prosentandel historiske data som skal brukes som et testsett for beregning av prognosenøyaktighet.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over behovsprognose](introduction-demand-forecasting.md)
- [Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)
- [Foreta manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
