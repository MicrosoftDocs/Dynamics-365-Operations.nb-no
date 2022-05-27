---
title: Gjøre et spørsmål avhengig av svaret på det forrige spørsmålet
description: Med betingede spørsmål kan du angi hvilket oppfølgingsspørsmål som skal vises til respondenten, avhengig av svaret på det forrige spørsmålet.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f7d55b577478f3156a8299fc2f827ab3bb60f1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686089"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Gjøre et spørsmål avhengig av svaret på det forrige spørsmålet


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Med betingede spørsmål kan du angi hvilket oppfølgingsspørsmål som skal vises til respondenten, avhengig av svaret på det forrige spørsmålet. Hvis du for eksempel spør Foretrekker du kaffe eller te, kan et logisk oppfølgingsspørsmål bestemmes avhengig av om respondenten velger kaffe eller te som et svar. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="find-the-existing-questionnaire"></a>Søk etter det eksisterende spørreskjemaet
1. Gå til **Spørreskjema** > **Utform** > **Spørreskjemaer**.
2. Velg spørreskjemaet WorkFH i listen.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Legg til alle spørsmålene og underspørsmålene i spørreskjemaet
1. Klikk på **Spørsmål**.
2. Klikk på **Ny**.
3. Velg spørsmål nummer 00016 i **Spørsmål**-feltet.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk på **Lagre**.
7. Lukk siden.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Angi sekvensen for spørreskjemaet til Betinget og gjør spørsmålet avhengig av det aktuelle spørsmålet
1. Klikk på **Rediger**.
2. Utvid **Oppsett**-delen.
3. Velg Betinget i **Spørsmålsrekkefølge**-feltet.
4. Klikk på **Betinget**-spørsmålet.
5. Velg Spørsmål\Forklar hvorfor du besvarte det forrige spørsmålet slik du gjorde i treet.
6. Velg spørsmål 00009 i **Hovedspørsmål**-feltet.
7. Klikk på koblingen i den valgte raden i listen.
8. Angi svarsekvens-ID-en for svaralternativet som du vil gjøre spørsmålet avhengig av, i **Svar**-feltet. Angi for eksempel 1 for det første svaralternativet.
9. Klikk på **Lagre**.
10. I treet velger du Spørsmål\Jeg betales rettferdig for arbeidet jeg gjør.
    * Legg merke til at spørsmålstreet er oppdatert for å vise avhengigheten.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
