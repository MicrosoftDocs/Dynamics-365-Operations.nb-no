---
title: Unngå avkorting av tekst i stillingshierarki og eksport til Visio
description: Dette emnet forklarer hvordan du løser et problem med avkortede navn på personer og stillinger i stillingshierarkiet i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20331b3a06301d10177fd0d5734f6e33994ef123
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693955"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Unngå avkorting av tekst i stillingshierarki og eksport til Visio


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Avgang**

Når en kunder viser stillingshierarkiet i Microsoft Dynamics 365 Human Resources, avkortes navnene på personer og stillinger. Derfor kan det være vanskelig å ta et skjermbilde eller skrive ut og distribuere hierarkiet.

![Stillingshierarki.](media/position-h.png)

**Årsak**

Denne virkemåten er standard.

**Løsning**

Dessverre kan ikke brukere endre størrelsen på teksten på en enkel måte. Du kan imidlertid eksportere stillingshierarkiet fra Human Resources og deretter importere det til Microsoft Visio. Selv om den følgende artikkelen ble skrevet for Microsoft Dynamics AX 2012, gjelder prosessen også for Human Resources: [Eksportere et stillingshierarki til Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Følg denne fremgangsmåten for å eksportere til Visio.

1. I Human Resources åpner du **Stillinger**-listesiden.

    Hvis du vil inkludere mer informasjon i organisasjonsstrukturdiagrammet, legger du til felt i **Stillinger**-listen, slik at de er tilgjengelige når du bruker **Veiviser for organisasjonskart** senere i denne fremgangsmåten.

2. I handlingsruten velger du Åpne i **Microsoft Office**-knappen, og deretter, under **Eksporter til Excel**, velger du **Stillinger**. Du kan også trykke på Ctrl+T.

    ![Eksportere listesiden Stillinger til Excel.](media/org-admin.png)

3. Lagre Excel-filen som blir eksportert.

    ![Eksportere til Excel-dialogboksen.](media/export-excel.png)

4. I Visio velger du **Visio - Opprett ny** og deretter **Arbeid**-malkategorien.

    ![Nytt diagram.](media/new.png)

5. Velg **Veiviser for organisasjonskart**, og velg deretter **Opprett**.

    ![Dialogboksen Veiviser for organisasjonskart.](media/orgchart-wizard.png)

6. Velg **Informasjon som allerede er lagret i en fil eller database**, og velg deretter **Neste**.

    ![Veiviser for organisasjonskart 1.](media/orgchart-wizard7.png)

7. Velg **En tekst-, Org Plus- (\*.txt) eller Excel-fil**, og velg deretter **Neste**.

    ![Veiviser for organisasjonskart 2.](media/orgchart-wizard3.png)

8. Bla for å velge den eksporterte Excel-filen som inneholder stillingshierarkiet, og velg deretter **Neste**.

    ![Veiviser for organisasjonskart 3.](media/orgchart-wizard2.png)

9. Angi **Navn**-feltet til **Stilling**, sett feltet **Rapporter til** til **Rapporterer til stilling**, og velg deretter **Neste**.

    ![Veiviser for organisasjonskart 4.](media/orgchart-wizard1.png)

10. Velg feltene som skal vises på hver node, og velg deretter **Neste**.

    ![Veiviser for organisasjonskart 5.](media/orgchart-wizard5.png)

11. Legg til **Stilling**-kolonnen i listen **Figurdatafelt**, og velg deretter **Neste**.

    ![Veiviser for organisasjonskart 6.](media/orgchart-wizard6.png)

12. Bilder er ikke tilgjengelig. På neste side kan du derfor velge **Neste**.
13. Velg **Jeg vil at veiviseren skal dele opp organisasjonskartet over flere sider automatisk**.

    ![Veiviser for organisasjonskart 7.](media/orgchart-wizard4.png)

14. Velg **Fullfør**.

    Hvis det finnes stillinger som ikke er inkludert i strukturen, blir du bedt om å inkludere dem i diagrammet.

Diagrammet som genereres i Visio, viser hver leder i et eget regneark.

Basert på feltene som du valgte å ta med i diagrammet, viser hver node riktig informasjon når Visio-filen genereres.

![Hierarkidiagram.](media/hierarchy.png)

**Tilleggsalternativ**

I Human Resources kan du også bruke arbeidsområdet **Personer** til å vise informasjon relatert til hierarkiet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
