---
title: Opprette et nytt lageroppsett
description: Dette emnet beskriver hvordan du definerer informasjon om lokasjoner i et lager.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7882d0eee1ff599ade2dacc27edaf53dc149b27f53bfe9ba490bf53fd9399a97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759581"
---
# <a name="create-a-new-warehouse-layout"></a>Opprette et nytt lageroppsett

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du definerer informasjon om lokasjoner i et lager. Dette gjelder bare for lagrene som er opprettet ved hjelp av "grunnleggende lageraktiviteter" i lagermodulen, ikke for lagre som er opprettet i lagerstyringsmodulen. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-the-default-location-capacity"></a>Angi standard lokasjonskapasitet
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring**.
2. Velg fanen **Lokasjoner**.
3. Angi et nummer i **Standardbredde**-feltet.
4. Angi et nummer i **Standarddybde**-feltet.
5. Angi et tall i **Standardhøyde**-feltet.
6. Velg **Lagre**.
7. Lukk siden.

## <a name="define-the-location-name-format"></a>Definer formatet for plasseringsnavn
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Lageroppdeling > Lagre**.
2. Velg **Ny**.
3. Skriv inn en verdi i **Lager**-feltet.
4. Skriv inn en verdi i **Navn**-feltet.
5. Velg det ønskede oppslaget i **Område**-feltet.
6. Aktiver/deaktiver utvidelsen av delen **Lokasjonsnavn**. Alternativene i denne delen definerer standardformatet for lokasjonsnavn. I vårt eksempel skal vi ta med gangnummer, reolnummer og hyllenummer.  
7. Sett alternativet **Inkluder gang** til **Ja**.
8. Sett alternativet **Ta med reol** til **Ja**. 
9. I **Format**-feltet velger du en verdi for reolen.
10. Sett alternativet **Ta med hylle** til **Ja**.
11. I **Format**-feltet velger du en verdi for hyllen.

## <a name="define-warehouse-locations"></a>Definer lagerlokasjoner
1. Velg **Lager** i handlingsruten.
2. Velg **Lokasjonsveiviser**.
3. Velg **Neste**.
4. Fjern merkingen av alternativet **Utleveringsporter**
5. Fjern merkingen av alternativet **Bulklokasjoner**
6. Velg **Neste** til du kommer til alternativet for å velge **Fullfør**.
7. Lukk siden.
8. Oppdater siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]