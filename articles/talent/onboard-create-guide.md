---
title: Opprette og sende en veiledning for jobbintroduksjon med Dynamics 365 Talent – Onboard
description: Dette emnet forklarer hvordan du bruker Microsoft Dynamics 365 Talent – Onboard-appen til å opprette en jobbintroduksjonsveiledning for nyansatte. Denne oppgaven er et viktig første skritt i en ansettelse-til-pensjonering-strategi for administrasjon av menneskelig kapital (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2371d86165390503312c2848842acf4745a8ed7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462091"
---
# <a name="create-and-send-an-onboarding-guide"></a>Opprette og sende en innebygd veiledning for jobbintroduksjon

[!include [banner](includes/banner.md)]

Med Microsoft Dynamics 365 Talent: Onboard kan du opprette jobbintroduksjonsveiledninger fra maler som du har opprettet selv, fra maler som er tilgjengelige i et galleri, eller fra bunnen av.

Når du har opprettet en jobbintroduksjonsveiledning, kan du sende den til en nyansatt. Alternativt kan du sende den til flere nyansatte som du angir i en Microsoft Excel-fil som du laster ned fra Onboard-appen.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Opprette en jobbintroduksjonsveiledning fra en mal og sende den til én nyansatt

1. Velg **Maler** på menyen til venstre.
2. Under **Mine maler** velger du malen du vil konfigurere som jobbintroduksjonsveiledning for den nyansatte.
3. Rediger malen som du ønsker. Husk å lagre arbeidet underveis.
4. Når du er ferdig med å redigere malen, **velger du** Opprett veiledning.

    [![Opprette en veiledning for jobbintroduksjon fra en mal](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. I vinduet **Opprett en veiledning** under **Hvem introduserer du** skriver du inn navnet eller e-postadressen til den nyansatte. Hvis den nyansatte ikke finnes i systemet ennå, velger du **Legg til nå** og angir den ansattes informasjon.

    ![[Legge inn informasjon for innføringsveiledningen](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. Under **Når starter de** velger du en startdato.
7. Hvis veiledningen for jobbintroduksjon skal sendes automatisk til den nyansatte på en bestemt dato, må du kontrollere at alternativet **Planlegg en dato for automatisk sending** er slått på, og deretter velge den automatiske sendedatoen. Hvis du vil sende veiledningen med en gang, deaktiverer du alternativet **Planlegg en dato for automatisk sending**.
8. Velg **Ferdig**.
9. Når du er ferdig med å redigere veiledningen for jobbintroduksjon, velger du **Send** i øvre høyre hjørne. Følg deretter ett av disse trinnene:

    - Hvis du vil sende den nyansatte en kobling til veiledningen for jobbintroduksjon, velger du **kopier en kobling** og velger deretter **Kopier**.
    - Hvis du vil tilpasse e-posten for jobbintroduksjonsveiledningen før du sender den, velger du **Tilpass e-posten før sending**, velger **Neste**, tilpasser e-posten som du ønsker, og velger deretter **Send**.
    - Hvis du vil sende e-posten uten å tilpasse den, velger du **Neste** og velger deretter **Send**.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Opprette en jobbintroduksjonsveiledning fra en mal og sende den til flere nyansatte

Med Onboard kan du sende en jobbintroduksjonsveiledning til flere nyansatte samtidig.

1. Velg **Maler** på menyen til venstre.
2. Under **Mine maler** velger du malen du vil konfigurere som jobbintroduksjonsveiledning for de nyansatte.
3. Rediger malen som du ønsker. Husk å lagre arbeidet underveis.
4. Når du er ferdig med å redigere malen, **velger du** Opprett veiledning.
5. I vinduet **Opprett en veiledning** velger du **Trenger du å introdusere flere personer samtidig**.

    [![Opprette en veiledning for jobbintroduksjon for flere nyansatte](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. Velg **mal for nyansettelse**.
7. Etter at XLSX-filen er lastet ned, velger du **Åpne**, angir ansattes informasjon i Excel-arbeidsboken og lagrer arbeidsboken.

    [![Laste ned Excel-malen for å sende veiledningen for jobbintroduksjon til flere nyansatte](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Før du kan redigere arbeidsboken, må du velge **Aktiver redigering** i Excel.
    > 
    > [![Aktivere redigering](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Dra Excel-arbeidsboken til det angitte området i vinduet **Opprett flere veiledninger**, eller klikk hvor som helst i området for å søke etter filen på datamaskinen.

    [![Dra den redigerte arbeidsboken](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. Når du er ferdig med å redigere veiledningen for jobbintroduksjon, velger du **Send** i øvre høyre hjørne. Følg deretter ett av disse trinnene:

    - Hvis du vil sende de nyansatte en kobling til veiledningen for jobbintroduksjon, velger du **kopier en kobling** og velger deretter **Kopier**.
    - Hvis du vil tilpasse e-posten for jobbintroduksjonsveiledningen før du sender den, velger du **Tilpass e-posten før sending**, velger **Neste**, tilpasser e-posten som du ønsker, og velger deretter **Send**.
    - Hvis du vil sende e-posten uten å tilpasse den, velger du **Neste** og velger deretter **Send**.

## <a name="create-a-guide-without-using-a-template"></a>Opprette en veiledning uten å bruke mal

Du trenger ikke alltid å opprette en veiledning fra en mal. Hvis du foretrekker det, kan du opprette en veiledning fra bunnene av i stedet.

1. På menyen til venstre velger du **Veiledninger**, og deretter velger du **Legg til**-knappen (plusstegnet \[**+**\]).
2. I vinduet **Opprett en veiledning** under **Hvem introduserer du** skriver du inn navnet eller e-postadressen til den nyansatte. Hvis den nyansatte ikke finnes i systemet ennå, velger du **Legg til nå** og angir den ansattes informasjon.

    ![[Legge inn informasjon for innføringsveiledningen](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. Under **Når starter de** velger du en startdato.
4. Hvis veiledningen for jobbintroduksjon skal sendes automatisk til den nyansatte på en bestemt dato, må du kontrollere at alternativet **Planlegg en dato for automatisk sending** er slått på, og deretter velge den automatiske sendedatoen. Hvis du vil sende veiledningen med en gang, deaktiverer du alternativet **Planlegg en dato for automatisk sending**.
5. Velg **Ferdig**.

## <a name="save-a-guide-as-a-template"></a>Lagre en veiledning som mal

Du kan lagre en jobbintroduksjonsveiledning som mal. På denne måten kan du spare tid når du skal opprette flere jobbintroduksjonsveiledninger senere.

1. Velg **Veiledninger** på menyen til venstre.
2. Velg **Mer**-knappen (ellipsen \[**...**\]) for veiledningen du vil opprette en mal fra, og velg deretter **Lagre som mal**.

    ![[Lagre en jobbintroduksjonsveiledning som mal](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. Skriv inn et navn på den nye malen i vinduet **Lagre som en ny mal**, og velg deretter **Lagre**.

## <a name="next-steps"></a>Neste trinn

- [Redigere veiledninger og maler for jobbintroduksjon](./onboard-edit-guides-templates.md)
- [Dele innhold med andre bidragsytere](./onboard-share-template.md)
- [Vise statusen for oppgaver og jobbintroduksjonsmedarbeidere](./onboard-view-status.md)
- [Opprette ansettelsesteam i Onboard](./onboard-create-team.md)

### <a name="see-also"></a>Se også

- [Prøve eller kjøpe Onboard-appen](https://dynamics.microsoft.com/talent/onboard/)
- [Hva er nytt eller endret i Dynamics 365 Talent](./whats-new.md)
- [Lanseringsplaner](https://docs.microsoft.com/business-applications-release-notes/index)
- [Få kundestøtte for Microsoft Dynamics 365 Talent](./talent-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]