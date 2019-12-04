---
title: Spore kandidatkilder i Attract
description: Dette emnet inneholder informasjon om hvordan du sporer kilden for kandidatprofiler og søknader.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832674"
---
# <a name="track-candidate-sources-in-attract"></a>Spore kandidatkilder i Attract

[!include [banner](includes/banner.md)]

> [!NOTE] 
> Funksjonalitet som er nevnt i dette emnet, er tilgjengelig som en del av en forhåndsversjon. Innholdet og funksjonaliteten kan bli endret. Hvis du vil bruke denne funksjonen, kan du be administratoren om å aktivere den ved hjelp av **Administrasjonsinnstillinger** i Attract. En fremtidig versjon vil inneholde kilderapporteringssporing. Hvis du vil ha mer informasjon, se [Tilgang til forhåndsvisningsfunksjoner i Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

Når kandidater søker på en jobb, registrerer Attract automatisk kilden for søknadene og gir deg verdifull informasjon som hjelper deg å målrette rekrutteringsinnsatsen din. Rekrutteringspersoner og -ledere kan også velge en søknadskilde når en kandidat legges til manuelt til en jobb- eller talentsamling.

Du kan vise søknadskilden i søknadsaktivitetdetaljene i **Aktivitet**-kategorien og i søknadsloggen som er tilgjengelig under **Profil** i talensamlinger. Du kan finne en kandidats profilkilde i kandidatdetaljene i **Profil**-kategorien i både søknads- og talentsamlinger.

> [!NOTE] 
> Du finner prosessmaler i [tillegget for omfattende ansettelse](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Forhåndskonfigurerte kilder

Standardkildelisten inneholder vanlige søknadskilder. Noen kildetyper, som **Jobbtavle** og **Sosiale nettverk**, har flere kildedetaljer. **Sosiale nettverk** inkluderer eksempelvis Facebook og Twitter. Med kildetypen **Henvisning** kan du angi en intern ansatt som referanseperson. Standard kildeliste inneholder følgende forhåndskonfigurerte kilder:

-   Attract-karriereområde

-   Byrå

-   Rekrutteringsmesse

-   Firmamarkedsføring

-   Konferanser og varemesser

-   Profesjonelle foreninger

-   Jobbtavle

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Tidsskrifter og publikasjoner

-   Sosiale nettverk

    -   Facebook

    -   Twitter

-   Universitetsrekruttering

-   LinkedIn

-   Klassifisert

-   Henvisning

-   Lagt til av rekrutterer

-   Annet

## <a name="customize-the-source-list"></a>Tilpasse kildelisten 

Du kan utvide kildelisten for å inkludere ekstra søknadskilder. For å tilpasse denne listen følger du instruksjonene i [Utvide alternativsett i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Rediger **TalentSource**-enhet slik at den inkluderer flere kilder. 

For å unngå negativ påvirkning på brukergrensesnittet må du ikke redigere eller slette **TalentCategory**-opplistingsverdiene (ikke navn) for følgende:

- **Henvisning**
- **LinkedIn**
- **Annet**

I stedet kan du utvide **TalentSource**-opplistingen for å legge til andre kildetyper.
