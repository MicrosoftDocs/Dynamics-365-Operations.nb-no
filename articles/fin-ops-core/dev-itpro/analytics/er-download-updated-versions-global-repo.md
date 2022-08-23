---
title: Importere oppdaterte versjoner av ER-konfigurasjoner
description: Denne artikkelen forklarer hvordan du importerer oppdaterte versjoner av elektroniske rapporteringskonfigurasjoner (ER) fra det globale repositoriet for konfigurasjonstjenesten.
author: kfend
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 0eef9c9a112fd58a43f6c3a85163ccf44bea3d61
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292654"
---
# <a name="import-updated-versions-of-er-configurations"></a>Importere oppdaterte versjoner av ER-konfigurasjoner

[!include [banner](../includes/banner.md)]

[Repositorier](general-electronic-reporting.md#Repository) for elektronisk rapportering (ER) brukes til å dele [ER-konfigurasjoner](general-electronic-reporting.md#Configuration). Du kan [importere](download-electronic-reporting-configuration-lcs.md) ER-konfigurasjonene fra forskjellige repositorier til din forekomst av Microsoft Dynamics 365 Finance. Når du importerer ER-konfigurasjoner, kan [konfigurasjonsleverandører](general-electronic-reporting.md#Provider) publisere nye versjoner av repositorier, slik at de kan deles.

Denne artikkelen forklarer hvordan du importerer oppdaterte versjoner av ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten. Hvis du vil ha mer informasjon, kan du se [Microsoft Dynamics 365 Finance – Regulatory Services, konfigurasjonstjeneste](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Se gjennom tilgjengelige oppdaterte versjoner

1. Logg på Finance med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Importer versjonsoppdateringer av konfigurasjoner**.

    ![Side for lokaliseringskonfigurasjoner.](./media/er-download-updated-versions-global-repo1.png)

4. I dialogboksen **Importer versjonsoppdateringer for elektroniske rapporteringskonfigurasjoner**, i **Kjøremodus**-feltet, velger du **Vis bare tilgjengelige oppdateringer**. Velg deretter **OK**. 

    ![Kjøremodus-feltet satt til Bare vis tilgjengelige oppdateringer.](./media/er-download-updated-versions-global-repo2.png)

5. Se gjennom meldingene du mottar. Disse meldingene inneholder følgende informasjon om ER-konfigurasjonene i gjeldende Finance-forekomst, og hvordan de sammenlignes med innholdet i det globale repositoriet:

    - Totalt antall ER-konfigurasjoner
    - ER-konfigurasjoner som ikke finnes i det globale repositoriet
    - ER-konfigurasjoner der den nyeste versjonen allerede er tilgjengelig i gjeldende Finance-forekomst. (Hvis du vil vise hele listen over disse ER-konfigurasjonene, velger du **Meldingsdetaljer**-koblingen.)

        ![Meldingen «Nyeste versjoner av følgende konfigurasjoner er allerede importert» og meldingsdetaljer](./media/er-download-updated-versions-global-repo3.png)

    - ER-konfigurasjoner der den nyeste versjonen er tilgjengelig i det globale repositoriet og kan importeres til gjeldende Finance-forekomst. (Hvis du vil vise hele listen over disse ER-konfigurasjonene, velger du **Meldingsdetaljer**-koblingen.)

        ![Meldingen «Tilgjengelige oppdateringer» og meldingsdetaljer](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Importer tilgjengelige oppdaterte versjoner

1. Logg på Finance med én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Importer versjonsoppdateringer av konfigurasjoner**.
4. I dialogboksen **Importer versjonsoppdateringer for elektroniske rapporteringskonfigurasjoner**, i **Kjøremodus**-feltet velger du **Importer nyeste oppdateringer** for å importere de nyeste versjonene av ER-konfigurasjoner fra det globale repositoriet til gjeldende Finance-forekomst.
5. Hvis du vil planlegge en satsvis jobb for importen, angir du **Satsvis behandling**-alternativet til **Ja** i **Kjør i bakgrunnen**-hurtigfanen. Hvis du vil gjenta importen regelmessig, kan du konfigurere den nødvendige gjentakelsen.

    ![Kjøre modus-feltet satt til Importer nyeste oppdateringer.](./media/er-download-updated-versions-global-repo5.png)

6. Velg **OK**.
7. Følg ett av disse trinnene for å finne ut hvilke konfigurasjonsversjoner som er importert:

    - Hvis du kjører importen interaktivt i stedet for å bruke en satsvis jobb, kan du se gjennom meldingene du mottar.

        ![Meldinger mottatt under en interaktiv importkjøring.](./media/er-download-updated-versions-global-repo6.png)

    - Hvis du kjører importen i satsvis modus, følger du denne fremgangsmåten:

        1. Gå til **Felles** \> **Forespørsler** \> **Satsvise jobber** \> **Mine satsvise jobber**.
        2. Finn og velg jobben **Importer versjonsoppdateringer for elektroniske rapporteringskonfigurasjoner**, og velg **Logg over satsvis jobb** i handlingsruten i **Satsvis jobb**-fanen for å vise jobbloggen.
        3. På **Logg for satsvis jobb**-siden velger du **Logg**. Velg **Meldingsdetaljer**-koblingen i meldingen du mottar, for å vise jobbloggen.

        ![Jobblogg.](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Vi anbefaler ikke at du planlegger en regelmessig satsvis jobb for å importere oppdaterte versjoner av ER-konfigurasjoner direkte fra det globale repositoriet til et produksjonsmiljø, fordi de importerte versjonene umiddelbart vil være tilgjengelige for bruk. Bruk i stedet denne fremgangsmåten til å distribuere versjoner av ER-konfigurasjoner til et sandkassemiljø. De kan evalueres i sandkassemiljøet før de distribueres til et produksjonsmiljø.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
