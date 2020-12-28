---
title: Arbeidstidskalendere
description: Dette emnet beskriver driftskalendere i Dynamics 365 Human Resources og hvordan du definerer kalendere.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: e77cc8921f2a8cfa1a48fda589fd20aae00e0fd4
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690082"
---
# <a name="working-time-calendars"></a>Arbeidstidskalendere

Driftskalenderen lar deg opprette en kalender med timer og dager som de ansatte arbeider i organisasjonen. Kalendere brukes til å strømlinjeforme forespørsler om fridager som standard i timer eller dager. Når en ansatt sender en forespørsel om fridager, trenger de ikke trenger å tenke på helligdager og stengetider, som er behandlet for dem gjennom driftskalenderen.

## <a name="setting-up-a-working-time-calendar"></a>Definere en driftskalender

Kalendere inkluderer detaljer for generering, dagene og timene du vil inkludere, dagene i kalenderen, arbeidstider for disse dagene, i tillegg til registrerte ansatte. 

Følg denne fremgangsmåten for å definere en kalender:

1. På siden **Organisasjonsstyring** klikker du **Kalendere**.

2. I handlingsruten velger du **Ny** og angir et navn og en beskrivelse.

3. Velg arbeidsdager for organisasjonen og angi arbeidstiden.

4. Legg til helligdager og stengetider ved hjelp av **Legg til**-knappen.

5. Angi navnet og beskrivelsen for helligdager og stengetider, for eksempel offentlige høytidsdager eller helligdager. Angi datoene for helligdager og lukninger. Lagre listen over helligdager og lukninger, og lukk siden.

6. Velg listen over helligdager og lukninger fra rullegardinmenyen.

7. Hvis de ansatte har tid de ikke arbeider, for eksempel lunsj eller pauser, legger du til disse også. Velg **Fritid**, og skrive inn et navn og tidsomfanget. Lukk siden. 

8. Klikk **Legg til** for å legge til fritid i kalenderen.

9. I kategorien **Dager** velger du **Generer** for å generere dagene i kalenderen. Angi datoområdet for kalenderen. Dagene og arbeidstidene genereres basert på arbeidsdagene og klokkeslettene som er definert under genereringsalternativene, sammen med datoene du valgte.

10. Hvis du vil tilordne en kalender til ansatte, velger du **Tilordne til ansatte** i handlingsruten. Velg de ansatte du vil tilordne denne kalenderen til, og klikk deretter **Tilordne**.

Ansatte trenger ikke å ha kalendere som er tilordnet. Hvis det er definert en arbeidstidskalender, utelates fridager automatisk fra forespørselen. Mengden, i timer eller dager, er som standard arbeidstiden som er definert i kalenderen. Hvis en ansatt ikke har en kalender som er tilordnet, er alle dager tilgjengelige for fritid og fritidsmengden er ikke standard for forespørselen. 
