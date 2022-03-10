---
title: Testinstrumenter for kvalitetsstyring
description: Dette emnet beskriver hvordan du oppretter testinstrumenter som kan brukes for tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d80a4f784a43e0d83d1f5b42f6740ef6da3add1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565909"
---
# <a name="quality-management-test-instruments"></a>Testinstrumenter for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter testinstrumenter som kan brukes for tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du bruker siden **Testinstrumenter** til å definere og vise detaljer om enhetene som brukes til å utføre tester på kvalitetsordrer. Testinstrumenter er valgfrie. De kan imidlertid hjelpe kvalitetsarbeidere med å vite hvilket verktøy eller hvilket verktøy de bør bruke til å utføre en bestemt test.

## <a name="test-instrument-example"></a>Eksempel på testinstrument

Du utfører ulike tester på elektriske komponenter. Noen tester er for spenningsutgangen for komponentene, én test er for temperaturen, og én test er for vekten. Forskjellige verktøy, enheter eller utstyr brukes til å utføre hver test. En spenningsmåler brukes for eksempel brukes til å måle spenning, et termometer for å måle temperatur og en vekt brukes til å måle vekten. Du kan konfigurere hver av disse enhetene som et testinstrument, og angi måleenheten som testresultatene skal registreres i. Resultater fra denne spenningsmåleren registreres for eksempel i volt, resultater fra termometeret registreres i grader og resultater fra vekten registreres i pund eller kilogram.

## <a name="create-a-test-instrument"></a>Opprette et testinstrument

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testinstrumenter**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Testinstrument** – Angi en unik ID eller et unikt navn for testinstrumentet.
    - **Beskrivelse** – Angi en detaljert beskrivelse av testinstrumentet.
    - **Enhet** – Velg enheten som instrumentet måler resultater i. **Presisjon**-feltet angis automatisk, basert på enheten du velger.

1. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser

- [Kvalitetsstyringstest](quality-tests.md)
- [Testgrupper for kvalitetsstyring](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
