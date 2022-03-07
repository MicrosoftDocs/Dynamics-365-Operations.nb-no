---
title: Angi ferdigheter
description: Jobber og ledere kan angi ferdigheter i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b24d37292a2e9749fb2fde06b9f03fcd13db0bbe
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076608"
---
# <a name="enter-skills"></a>Angi ferdigheter

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan angi målkompetanse eller faktisk kompetanse for arbeidere, søkere eller kontakter i Dynamics 365 Human Resources. En målkompetanse er en kompetanse en person ønsker å oppnå. En faktisk kompetanse er en kompetanse en person har.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Opprette en arbeidsflyt for å godkjenne kompetanse automatisk

Hvis du vil legge inn kompetanse uten å kreve godkjenning, må du opprette en arbeidsflyt for å godkjenne kompetanse automatisk.

> [!NOTE]
> Kompetanse som angis av ansatte, krever alltid ledergodkjenning. Denne arbeidsflyten godkjenner bare automatisk kompetanse som angis av ledere på vegne av arbeiderne.

1. I arbeidsområdet **Personaladministrasjon** velger du **Koblinger**.

2. Under **Oppsett** velger du **Personalarbeidsflyter**.

3. Velg **Ny**.

4. Velg **Arbeiderkompetanse** i ruten **Opprett arbeidsflyt**.

   [![Velge arbeidsflyt for arbeiderkompetanse](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Velg **Åpne** i dialogboksen **Åpne denne filen?**. Angi påloggingsinformasjon når du blir spurt.

6. Velg arbeidsflytelementet **Godkjenn ferdigheter** i redigeringsprogrammet, og dra det til lerretet.

   [![Velge arbeidsflytelementet Godkjenn ferdigheter](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Koble **Start**-elementet til elementet **Godkjenn ferdigheter 1**, og koble deretter elementet **Godkjenn ferdigheter 1** til **Slutt**-elementet. Det kan hende at du må rulle ned for å se **Slutt**-elementet. Du kan dra det nærmere de andre elementene.

   [![Koble arbeidsflytelementer](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Dobbeltklikk arbeidsflytelementet **Godkjenn ferdigheter 1**, og høyreklikk **Trinn 1**-elementet. Høyreklikk trinn **Trinn 1**-elementet, og velg deretter **Egenskaper**.

9. Velg **Betingelse**-vinduet på venstre navigasjonslinje i **Egenskap**-vinduet.

10. Velg **Kjør bare dette trinnet når følgende betingelse er oppfylt**.

11. Velg **Legg til betingelse**. Velg **Ansattselvbetjeningsferdigheter** etter **Hvor**, og velg deretter **Ansattselvbetjeningsferdigheter.Person**. Etter **er,** velg **felt**, og velg deretter **Bruker til person-forhold. Person**.

    [![Angi betingelse](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Velg **Tilordning** på venstre navigasjonslinje.

13. Velg **Hierarki** i kategorien **Tilordningstype**.

14. Velg **Lederhierarki** i feltet **Hierarkitype:** i kategorien **Hierarkivalg**.

    [![Angi lederhierarki](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Velg **Lukk**, velg **Arbeidsflyt** i opprettelsesarbeidsflyten, og velg deretter **Lagre og lukk**.

Hvis du vil ha mer informasjon om hvordan du oppretter arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Angi kompetanse for en arbeider

1. Velg en arbeider.

2. Velg **Person** på handlingslinjen til **Person**, og velg deretter **Kompetanse**.

3. Fyll ut følgende felt for hver kompetanse på **Kompetanse**-siden:

   - **Kompetanse**: Velg en kompetanse.
   - **Nivåtype** : Velg **Faktisk** for en kompetanse arbeideren allerede har, eller velg **Mål** for en kompetanse som arbeideren arbeider mot.
   - **Nivå** : Velg et nivå for arbeiderens kompetanse.
   - **Nivådato**: Velg en dato i kalenderverktøyet.
   - **Eksaminator**: Velg om nødvendig en eksaminator fra listen. Du kan filtrere søket.
   - **År med erfaring**: Angi år med erfaring.
   - **Verifisert**: Hvis kompetansen er kontrollert, merker du av for dette.
   - **Kontrollert av** : Angi navnet på kontrolløren.

4. Når du er ferdig med å angi ferdigheter, velger du **Lagre**.

## <a name="see-also"></a>Se også

[Konfigurere kompetanse](hr-develop-skills.md)<br>
[Kompetansesøk](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]