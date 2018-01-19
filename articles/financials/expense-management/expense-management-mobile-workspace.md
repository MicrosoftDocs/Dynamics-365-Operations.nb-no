---
title: "Det mobile arbeidsområdet Reiseregning og utlegg"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for reiseregning og utlegg. Dette arbeidsområdet lar brukere registrere og laste opp en kvittering, slik at de kan knytte det til en reiseregningsrapport senere. Brukere kan også raskt opprette en utgiftslinje ved hjelp av en tilknyttet mottak, og opprette og administrer reiseregninger."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: bbbe37330e16a079b817dfe04f4a47f046263e88
ms.contentlocale: nb-no
ms.lasthandoff: 12/01/2017

---

# <a name="expense-management-mobile-workspace"></a>Mobilt arbeidsområde for reiseregninger og utlegg

[!include[banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet for **reiseregning og utlegg**. Dette arbeidsområdet lar brukere registrere og laste opp en kvittering, slik at de kan knytte det til en reiseregningsrapport senere. Brukere kan også raskt opprette en utgiftslinje ved hjelp av en tilknyttet mottak, og opprette og administrer reiseregninger. Godkjennere kan også bruke det mobile arbeidsområdet for **reiseregninger og utlegg** til å vise utgifter som er tilordnet til dem, og enten godkjenne eller avvise de reiseregninger.


Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations.


## <a name="overview"></a>Oversikt

Mange organisasjoner krever at en kopi av en kvittering knyttes til en reiserelaterte eller forretningsrelatert reiseregningsrapport som en ansatt sender inn for refusjon. Dette mobile arbeidsområdet for **reiseregning og utlegg** lar brukere raskt opprette nye utgiftslinjer på mobilenheten etter eget valg, ved hjelp av et tilknyttet bilde av en kvittering. Brukere kan også ta et bilde av en kvittering, og deretter knytte den til en reiseregningsrapport senere. Ansatte kan også opprette og administrere sine reiseregninger, og deretter sende dem til godkjenning og refundering ved hjelp av mobilenheten.


Det mobile arbeidsområdet for **reiseregninger og utlegg** lar brukere utføre disse oppgavene:

- Ta et bilde av en kvittering og laste den opp til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Du kan deretter knytte bildet til en reiseregningsrapport senere.
- Laste opp en fil som en registrerte kvitteringer. Du kan deretter knytte filen til en reiseregningsrapport senere.
- Opprette en ny utgiftslinje ved hjelp av en tilknyttet kvittering. Du kan deretter legge til linjeelementet i en reiseregningsrapport senere, og sende den inn til godkjenning og refusjon.

Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, kan du også bruke disse funksjonene:

- Opprett en ny reiseregningsrapport.
- Legge ved kredittkorttransaksjoner og andre utgifter som er opprettet i en reiseregningsrapport.
- Opprett nye utgifter for en reiseregningensrapport.
- Knytte en kvittering til en utgift for reiseregninger, enten ved å ta et bilde av mottaket, eller ved å laste opp en fil som en registrerte kvitteringer.
- Avhengig av firmaets utgiftspolicy, kan du legge til listen over gjester i en utgift.
- Avhengig av firmaets utgiftspolicy, kan du spesifisere utgiftene.
- Sende en reiseregning til godkjenning og refusjon.
- Godkjenne eller avvise reiseregninger som du har tilordnet godkjenner for.

## <a name="prerequisites"></a>Forutsetninger
Forutsetningene varierer avhengig av hvilken versjon av Microsoft Dynamics 365 som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 
Hvis Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Reiseregninger og utlegg**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere
Hvis Microsoft Dynamics 365 for Operations versjon 1611 med plattformoppdatering 3 eller senere er distribuert i organisasjonen, må systemansvarlig oppfylle følgende forutsetninger. 

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementere KB 4019015.</td>
<td>Systemansvarlig</td>
<td>KB 4019015 er en X++-oppdatering eller metadatahurtigreparasjon som inneholder det mobile arbeidsområdet <strong>Reiseregning og utlegg</strong>. Systemadministrator må følge trinnene nedenfor for å implementere KB 4019015.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Last ned hurtigreparasjonen for metadata fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installer hurtigreparasjonen for metadata</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opprett en distribuerbar pakke</a> som inneholder modellene <strong>ApplicationSuite</strong> og <strong>ExpenseMobile</strong>, og laste deretter opp den distribuerbare pakken til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Bruk den distribuerbare pakken</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publiser det mobile arbeidsområdet for <strong>reiseregninger og utlegg</strong>.</td>
<td>Systemansvarlig</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laste ned og installere Dynamics 365 for Operations-mobilappen
Last ned og installer mobilappen Dynamics 365 for Unified Operations:

- [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen
1. Start appen på mobilenheten.
2. Skriv inn URL-adressen for Dynamics 365.
4. Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
5. Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.


[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Registrere en kvittering ved å bruke det mobile arbeidsområdet reiseregning og utlegg

1. Åpne arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. Velg **Registrer kvittering**.
3. Velg **Ta bilde** eller **Velg bilde**.
4. Følg ett av disse trinnene:

    - Hvis du har valgt **Ta bilde**, følger du denne fremgangsmåten:

        1. Du kobles til kameraet på mobilenheten, slik at du kan ta et bilde av kvitteringen. Når du har tatt et bilde, velger du **OK** for å godta bildet.
        2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle merknader.

    - Hvis du har valgt **Velg bilde**, følger du denne fremgangsmåten:

        1. Velg et bilde i listen.
        2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle merknader.

5. Velg **Ferdig**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Angi utgifter raskt ved å bruke det mobile arbeidsområdet reiseregning og utlegg
1. Åpne arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. Velg **Hurtig utgiftsregistrering**.
3. Velg kategorien for utgiften. Du ser en liste over utgifter som er lastet inn i appen for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis kategorien ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter utgiftskategori, eller bytt til å søke etter utgiftstype.
4. Angi transaksjonsdatoen for utgiften.
5. Valgfritt: Angi forhandleren for utgiften.
6. Angi utgiftsbeløpet.
7. Angi valutaen for utgiften. Du ser en liste over valutakoder som er lastet inn i appen for frakoblet bruk. 400 valutaer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis valutaen ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter valuta, eller bytt til å søke etter navn.
8. Velg **Ta bilde** eller **Velg bilde**.
9. Følg ett av disse trinnene:

    - Hvis du velger **Ta bilde**, kobles du til kameraet på mobilenheten, slik at du kan ta et bilde av kvitteringen. Når du har tatt et bilde, velger du **OK** for å godta bildet.
    - Hvis du valgte **Velg bilde**, velge du et bilde i listen.

10. Velg **Ferdig**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Godkjenne en utgiftsrapport ved å bruke utgiften management mobil arbeidsområdet (hvis du bruker oppdateringen fra juli 2017)
1. Åpne arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. **Utgiftsgodkjenninger** viser hvor mange rapporter som er tilordnet til deg for godkjenning. Nummeret blir oppdatert hvert 30. minutt. Velg **Utgiftsgodkjenninger**.

    Listen over reiseregninger som er tilordnet til deg for godkjenning, vises.
    
3. Velg en reiseregning til å vise utgiftsdetaljene for den.
4. Velg en utgift til å vise detaljene for den. Informasjonen som vises for en utgift omfatter alle kvitteringer, gjester og spesifiseringsdetaljer.
5. Gå tilbake til siden **Reiseregning** og velg å godkjenne eller avvise reiseregningsrapporten.
6. Skriv inn eventuelle kommentarer for godkjenningshandlingen.
7. Velg **Ferdig**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Opprette en ny reiseregningsrapport og sende den til godkjenning ved å bruke det mobile arbeidsområdet for reiseregninger (hvis du bruker oppdateringen fra juli 2017)
1. Åpne arbeidsområdet **Reiseregning og utlegg** på mobilenheten.
2. Velg **Utgiftsoppføring**.
3. Velg **Ny rapport**, eller velg en eksisterende rapport i listen.
4. Angi formålet og eventuell tilleggsinformasjon som er tilgjengelig for nye reiseregningsrapporter. Denne informasjonen varierer, avhengig av den måten reiseregninger er konfigurert for firmaet.
5. Velg **Ferdig**.
6. Hvis du vil legge til eksisterende utgifter, for eksempel kredittkorttransaksjoner, i reiseregningsrapporten, velger du **Vedlegg**.
7. Velg én eller flere utgifter i listen.
8. Velg **Ferdig**.
9. Hvis du vil legge til en ny utgift i reiseregningen, velger du **Ny utgift**.
10. Velg kategorien for utgiften. Du ser en liste over utgifter som er lastet inn i appen for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis kategorien ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter utgiftskategori, eller bytt til å søke etter utgiftstype.
11. Valgfritt: Angi forhandleren for utgiften.
12. Angi transaksjonsdatoen for utgiften.
13. Angi utgiftsbeløpet.
14. Angi valutaen for utgiften. Du ser en liste over valutakoder som er lastet inn i appen for frakoblet bruk. 400 valutaer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis valutaen ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter valuta, eller bytt til å søke etter navn.
15. Velg **Ferdig**.
16. Hvis du vil legge til flere detaljer i utgiften, velger du **Legg til flere detaljer**. Feltene som er tilgjengelige, avhenger av konfigurasjonen av reiseregning for firmaet.
17. Hvis firmapolicy krever en kvittering for utgiften, velger du **Kvitteringer**, og gjør deretter følgende:

    1. Velg **Registrer kvittering** eller **Legg ved kvittering**.
    2. Følg ett av disse trinnene:

        - Hvis du har valgt **Registrer kvittering**, følger du denne fremgangsmåten:

            1. Velg **Ta bilde** eller **Velg bilde**.
            2. Følg ett av disse trinnene:

                - Hvis du har valgt **Ta bilde**, følger du denne fremgangsmåten:

                    1. Du kobles til kameraet på mobilenheten, slik at du kan ta et bilde av kvitteringen. Når du har tatt et bilde, velger du **OK** for å godta bildet.
                    2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle merknader.

                - Hvis du har valgt **Velg bilde**, følger du denne fremgangsmåten:

                    1. Velg et bilde i listen.
                    2. Valgfritt: Angi et navn for bildet, og skriv inn eventuelle merknader.

            3.  Velg **Ferdig**.

        - Hvis du har valgt **Legg ved kvittering**, følger du denne fremgangsmåten:

            1.  Velg ett eller flere bilder i listen.
            2.  Velg **Ferdig**.

    3. Velg **Tilbake**-knappen for å gå tilbake til reiseregningsdetaljene.

18. Hvis firmapolicy krever gjester for utgiften, velger du **Gjester**, og gjør deretter følgende:

    1. Velg **Gjest**, **Tidligere gjester** eller **Medarbeidere**.
    2. Følg ett av disse trinnene:

        - Hvis du har valgt **Gjest**, følger du denne fremgangsmåten:

            1. Angi navnet på gjesten.
            2. Valgfritt: Angi organisasjonen og/eller landet til gjesten.
            3. Valgfritt: Angi tittelen til gjesten.
            4. Velg **Ferdig**.

        - Hvis du har valgt **Tidligere gjester**, følger du denne fremgangsmåten:

            1. Velg én eller flere tidligere gjester i listen. Du ser en liste over tidligere gjester du har lagt til i tidligere reiseregninger, som lastes inn i programmet ditt for bruk i frakoblet modus. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis den tidligere gjesten ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter navn, eller bytt til å søke etter organisasjon, land eller tittel.
            2. Velg **Ferdig**.

        - Hvis du har valgt **Medarbeidere**, følger du denne fremgangsmåten:

            1. Velg én eller flere medarbeidere i listen. Du kan se en liste over medarbeidere som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis medarbeideren ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter navn, eller bytt til å søke etter bedrift eller tittel.
            2. Velg **Ferdig**.

    3. Velg **Tilbake**-knappen for å gå tilbake til reiseregningsdetaljene.

19. Hvis firmapolicy krever at utgiften skal være spesifisert, velger du **Spesifiser**, og gjør deretter følgende:

    1. Velg den første datoen som skal spesifiseres.
    2. Velg **Legg til spesifisering**.
    3. Velg underkategorien for utgiftsspesifiseringen. Du ser en liste over utgiftsunderkategorier som er lastet inn i appen for frakoblet bruk. 50 varer blir lastet inn som standard, men en utvikler kan endre dette antallet. Utviklere kan se [Mobil plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) for mer informasjon. Hvis underkategorien ikke finnes i listen, velger du **Søk** for å utføre en online-søk. Søk etter navn på underkategori for utgift.
    4. Angi transaksjonensbeløpet for spesifiseringen.
    5. Rediger transaksjonsdatoen hvis det er nødvendig.
    6. Velg **Ferdig**.
    7. Gjenta de foregående trinnene til du har lagt til alle spesifiseringer for den valgte datoen.
    8. For flere dag, kan du velge **Kopier til neste dag** for å kopiere spesialiseringene til neste dag. Du kan også velge datoen som skal spesifiseres, og deretter legge til spesifiseringer slik du gjorde for den første datoen.
    9. Når du er ferdig med å spesifisere utgiften, velger du **Tilbake**-knappen for å gå tilbake til reiseregningsdetaljene.

20. Velg **Tilbake**-knappen for å gå tilbake til siden **Reiseregning**.
21. Gjenta de foregående trinnene til du har lagt til alle utgifter.
22. Velg **Send**.
23. Skriv inn eventuelle kommentarer for godkjenneren.
24. Velg **Ferdig**.

