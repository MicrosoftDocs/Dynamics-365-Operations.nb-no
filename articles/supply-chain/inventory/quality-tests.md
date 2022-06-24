---
title: Kvalitetsstyringstester
description: Denne artikkelen beskriver hvordan du oppretter tester som kan brukes for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac67ee97a4890c646daefa6b09feae25c4f15d0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857612"
---
# <a name="quality-management-tests"></a>Kvalitetsstyringstester

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter tester som kan brukes for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du bruker **Tester**-siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner. Du kan tilordne én eller flere individuelle tester til en testgruppe. I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene. Målingsverdier brukes for kvantitative tester. For kvalitative tester brukes testvariabler.

- For kvantitative tester er **Type**-feltet satt til *Heltall* eller *Brøk*. En måleenhet er også angitt. Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.
- For kvalitative tester er **Type**-feltet satt til *Alternativ*. Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene. Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.

Du kan også tilordne et testinstrument til en test. Testinstrumenter kreves imidlertid ikke for å opprette og bruke tester med kvalitetsordrer. Hvis du vil ha mer informasjon, kan du se [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md).

Du kan også velge å angi en enhet for en test for å angi måleenheten som testresultatene registreres i. En test for temperatur kan for eksempel inneholde en enhet på enten grader Fahrenheit eller grader Celsius.

## <a name="example-of-a-test"></a>Eksempel på en test

Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test for materialkvalitet og en kvalitativ test for emballasjeskade. Firmaet angir tilleggsinformasjon om den kvalitative testen for å definere testvariabelen (for eksempel skadet emballasje) og resultatene. Firmaet bruker **Testgrupper**-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon. Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.

## <a name="create-a-test"></a>Opprette en test

Følg trinnene nedenfor for å opprette en test.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Tester**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Test** – Angi en unik ID eller et unikt navn for testen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av testen.
    - **Type** – Velg typen resultater som testen produserer. Velg *Brøk* eller *Heltall* for kvantitative tester. Velg *Alternativ* for kvalitative tester.
    - **Testinstrument** – Velg et [testinstrument](quality-test-instruments.md) som skal brukes for testen.
    - **Enhet** – Hvis du valgte *Brøk* eller *Heltall* i **Type**-feltet (det vil si hvis testen er en kvantitativ test), velger du måleenheten som testresultatene skal registreres i.

1. Lukk siden.

> [!NOTE]
> Etter at du har lagret en test, kan du ikke lenger redigere **Type**-feltet i rutenettet. Hvis du må endre typen testresultat som skal registreres for en test, velger du **Endre type kvalitetstest** i handlingsruten. I dialogboksen **Endre type kvalitetstest** setter du **Ny type**-feltet til ønsket type, og velger deretter **OK** for å lukke dialogboksen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)
- [Testvariabler for kvalitetsstyring](quality-test-variables.md)
- [Kvalitetstilknytninger](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
