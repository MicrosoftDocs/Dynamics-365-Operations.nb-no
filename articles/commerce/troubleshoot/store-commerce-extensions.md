---
title: Feilsøk utvidelsesproblemer med Store Commerce-tillegget
description: Denne artikkelen beskriver hvordan du feilsøker utvidelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: b440183e255e05c4f93a4f11106be2967163ff74
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169024"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Feilsøk utvidelsesproblemer med Store Commerce-tillegget

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du feilsøker utvidelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

## <a name="extensions-packages-arent-loaded"></a>Utvidelsespakker lastes ikke inn

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Utvidelsespakker vises ikke på siden Salgssted \> Innstillinger

Det kan hende at utløsere for Commerce Runtime (CRT) ikke er oppdatert til å inkludere utvidelsespakken, eller at de ikke er distribuert. Hvis du vil ha mer informasjon, kan du se [Utvidelsesmuligheter og utløsere for Commerce Runtime (CRT)](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Utvidelsespakker vises på siden Salgssted \> Innstillinger, men manifestet lastes ikke inn

Bekreft at utvidelsespakkene finnes i mappen **C:\\Programfiler\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions**. Hvis pakkene finnes, skal det finnes en **Salgssted**-mappe der som inneholder manifestet.

Hvis det ikke finnes en **Salgssted**-mappe, bekrefter du at Store Commerce-prosjektet refererer til utvidelsesprosjektet for salgsstedet (POS) på riktig måte. Valider prosjektreferansebanen, og kontroller at den finnes. 

I eksempelillustrasjonen nedenfor har installeringsprosjektet problemer med det refererte utvidelsesprosjektet.

![Referansen for Store Commerce-installeringsprosjektet er ikke gyldig.](media/ReferenceNotValid.png)

Hvis referansen for utvidelsesprosjektet er lagt til på riktig måte, skal det ikke være noe advarsels- eller avhengighetsproblem i installeringsprosjektet, som vist i eksemplet nedenfor.

![Referansen for Store Commerce-installeringsprosjektet er gyldig.](media/ReferenceValid.png)
