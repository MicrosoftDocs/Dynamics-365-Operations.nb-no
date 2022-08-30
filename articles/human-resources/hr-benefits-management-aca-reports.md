---
title: Generere rapporter om Affordable Care Act i fordelsbehandling
description: Denne artikkelen beskriver hvordan fordelsbehandling sporer informasjon som er rapportert på skjema 1095-B og skjema 1095-C for employer mandate Affordable Care Act (ACA).
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a56fe2b3a25a300687d81702c52614a78f2a6f61
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336980"
---
# <a name="generate-aca-reports-in-benefits-management"></a>Generere ACA-rapporter i fordelsbehandling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Fordelsbehandling sporer informasjon som er rapportert på skjema 1095-B og skjema 1095-C for employer mandate Affordable Care Act (ACA). I likhet med ACA-rapporteringsfunksjonene på det gamle arbeidsområdet **Fordeler**, gjelder denne funksjonaliteten bare for juridiske enheter i USA.

Hvis du vil bruke denne funksjonen, må du først aktivere **Avansert fordelsbehandling**. Hvis du vil ha mer informasjon, inkludert viktige opplysninger om fordelsbehandling, kan du se [Aktivere eller deaktivere fordelsbehandling](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> Du kan bare bruke ACA-rapportering fra arbeidsområdet for **Fordelsbehandling** eller det gamle arbeidsområdet **Fordeler**, ikke fra begge. Hvis du for eksempel byttet til Fordelsbehandling, er ACA-rapportering bare tilgjengelig fra arbeidsområdet for **Fordelsbehandling**, ikke fra det gamle **Fordeler**-arbeidsområdet.
>
> Hvis du bytter til Fordelsbehandling midt i et registreringsår, må du konfigurere ansattdata på riktig måte for hele året i Fordelsbehandling. På denne måten sikrer du at du vil motta nøyaktig rapporteringsinformasjon for hele året.

## <a name="getting-started"></a>Komme i gang

Hvis du vil spore informasjon for 1095-skjemaer, må du først opprette én eller flere Affordable Care-dekningsgrupper. Disse gruppene angir følgende informasjon:

- Tilbudet om dekning som ble gitt til en ansatt
- Den ansattes del av den månedlige bonusen med lavest kostnad, hvis kostnaden er over den føderale fattigdomsgrensen
- Safe Harbor som brukes av arbeidsgiveren, dersom det er aktuelt

Affordable Care-dekningsgrupper hjelper deg med å administrere denne informasjonen for flere ansattposter som har de samme betingelsene. Du kan lett tilordne grupper til én eller flere ansatte.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Opprette eller redigere en Affordable Care-dekningsgruppe

1. I arbeidsområdet **Fordelsbehandling** velger du **Affordable Care-dekningsgruppe**.

    ![Velge Affordable Care-dekningsgruppe.](./media/hr-benefits-management-aca-coverage-group.png)

2. Velg **Ny** for å opprette en ny Affordable Care-dekningsgruppe eller **Rediger** for å endre en eksisterende gruppe.

    ![Velge Ny eller Rediger.](./media/hr-benefits-management-aca-new.png)

3. Angi følgende felt.

    | Felt | beskrivelse |
    |---|---|
    | Navn | Angi et navn for gruppen. |
    | beskrivelse | Angi en beskrivelse av gruppen. |
    | Tilbud om dekning | Dekningen som tilbys ansatte, deres ektefelle eller partner og deres avhengige. |
    | Ansattdel av kostnad | Beløpet som den ansatte er ansvarlig for. |
    | Gjeldende avsnitt, 4980H safe harbor | 4980H safe harbor-kode eller kode for overgangslettelse. |
    | Startmåned for plan | Velg kalendermåneden når fordelsplanåret starter. |
    | Gruppe gyldig fra | Den første datoen denne posten er gyldig. |
    | Gruppe gyldig til og med | Den siste datoen denne posten er gyldig. Hvis det ikke er noen utløpsdato, angir du **Aldri**. |

    ![Opprette en dekningsgruppe.](./media/hr-benefits-management-aca-new-group.png)

4. Velg **Lagre**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Tilordne flere ansatte til en Affordable Care-dekningsgruppe

1. I arbeidsområdet **Fordelsbehandling** velger du **Affordable Care-dekningsgruppe**.
2. Velg gruppen du vil tilordne ansatte til.
3. Velg **Massetilordning**.

    ![Velge Massetilordning.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Velg ansatte i listen, og velg **Tilordne**.

    ![Tilordne valgte ansatte til en gruppe.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Vedlikeholde flere versjoner av dekningalternativer

Du kan vedlikeholde flere versjoner av en hvilken som helst dekningsgruppe. Når noe endres i organisasjonen eller fordelene som tilbys, kan du holde gruppens informasjon oppdatert uten å måtte opprette en ny gruppe og tilordne ansatte til den på nytt.

Når du har opprettet Affordable Care-dekningsgrupper, kan du massetilordne ansatte til dem. Du kan også tilordne ansatte individuelt til grupper, og angi om ACA-informasjon skal spores og rapporteres.

Hvis du ikke trenger å spore og rapportere ACA-informasjon for en ansatt, kan du sette alternativet **Rapportdekning** til **Nei**. Du kan for eksempel ha deltidsansatte som ikke trenger ACA-rapportering.

### <a name="override-default-values-for-an-employee"></a>Overstyre standardverdier for en ansatt

For ansatte som er tilordnet en Affordable Care-dekningsgruppe, kan du endre følgende alternativer for måneder som krever ulike verdier:

- Tilbud om dekning
- Ansattdel av kostnad
- Gjeldende avsnitt, 4980H safe harbor

> [!NOTE]
> For 2020 ACA-rapporter må du rapportere både jobb- og hjemmepostnumre på skjema 1095-C. Verdier fylles ut automatisk basert på gjeldende aktive lokasjoner. Hvis en av lokasjonene var forskjellig i løpet av året, må du overstyre verdien. **Postnummer**-feltet (linje 17) for 1095-C-rapporten fylles bare ut hvis koden **Tilbud om dekning** inneholder **1L** til og med **1Q** følgende måte:
>
> - **1L, 1M eller 1N:** Postnummer for primær bosted
> - **1O, 1P, 1Q:** Postnummer for det primære arbeidsstedet

Følg denne fremgangsmåten for å angi unntak for verdier til en Affordable Care-dekningsgruppe.

1. I arbeidsområdet **Personaladministrasjon** velger du **Koblinger** og deretter **Arbeidere**.
2. Velg ansatt i listen.
3. I kategorien **Ansettelse** i delen **Mer informasjon** velger du **Affordable Care-dekning**.

    ![Endre alternativer for én ansatt.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Velg **Rediger**.
5. For hver måned som krever endringer, merker du av for **Overstyr standard**, og deretter endrer du de andre verdiene etter behov.

    ![Overstyre standardverdier.](./media/hr-benefits-management-aca-override-default.png)

6. Velg **Lagre**.

## <a name="report-health-care-coverage"></a>Rapportere helsedekning

Du må spore alle arbeidsgiver-sponsede, selvforsikret helsedekning for heltids- og deltidsansatte. Inkluder hver ansatt sammen med deres avhengige på 1095-C-rapporten for månedene de ble dekket.

Følg denne fremgangsmåten for å angi om en fordelsplan må rapporteres.

1. I arbeidsområdet **Fordelsbehandling**, velger du **Fordelsplaner**.
2. Velg fordelsplanen som skal rapporteres.
3. Velg **Rediger**.
4. Sett alternativet **Rapportert under Affordable Care Act** til **Ja**.

    ![Rapportere helsedekning.](./media/hr-benefits-management-aca-report-coverage.png)

5. Velg **Lagre**.

Hvis en ansatt velger helsedekning for en avhengig, bestemmes avhengiges dekningsperiode av datoen da den avhengige ble registrert eller fjernet. Dekningsdatoer for avhengige beregnes automatisk basert på perioden da den avhengige var kvalifisert og aktiv i en plan i løpet av registreringsåret.

## <a name="generate-1095-b-and-1095-c-forms"></a>Generere 1095-B- og 1095-C-skjemaer

Du kan også generere ACA 1095-B- og 1095-C-skjemaer, og distribuer dem deretter til alle ansatte. Du kan også generere skjema 1095-C elektronisk og de tilsvarende overføringsfilene for 1094-C som skal sendes til Internal Revenue Service (IRS).

1. I arbeidsområdet **Fordelsbehandling** velger du **ACA 1095-B-skjema** eller **ACA 1095-C-skjema**.
2. Endre parameterne etter behov, og velg deretter **OK**.

    > [!NOTE]
    > Hvis du skriver ut 1095-C-skjemaer for mer enn 500 ansatte, får du mer enn én PDF-fil. Det anbefales at du øker verdien til feltet **Maksimum filstørrelse** på siden **Parametere for dokumentstyring** til **150**. (Du kan åpne den siden raskt ved å bruke søkefeltet i navigasjonsfeltet.)
    >
    > ![Endre maksimumsfilstørrelse.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Hvis du vil kontrollere statusen til rapportene og vise dem, bruker du søkefeltet på navigasjonslinjen til å åpne siden **Elektroniske rapporteringsjobber**.

    ![Søke etter siden Elektroniske rapporteringsjobber.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Velg rapporten som skal vises, og velg deretter **Vis filer**.

    ![Viser filer.](./media/hr-benefits-management-aca-show-files.png)

5. Velg **Åpne**.

    ![Åpne en fil.](./media/hr-benefits-management-aca-open-file.png)

6. Åpne zip-filen i varslingsfeltet som vises nederst i webleservinduet, og velg deretter rapporten. Du kan vise eller skrive ut PDF-filen.

    ![Eksempel 1095-C-skjema.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>Vise ACA-dekningsinformasjon

Siden **Affordable Care-dekning for arbeidere** viser følgende informasjon:

- Ansatte som er tilordnet hver dekningsgruppe
- Ansatte som ikke må inkluderes i en rapport
- Ikke tilordnede ansatte

Følg disse trinnene for å vise informasjonen.

1. I arbeidsområdet **Fordelsbehandling** velger du **Affordable Care-dekning for arbeidere**.
2. Velg en gruppe i feltet **Gruppenavn**.

    ![Vise ACA-dekning.](./media/hr-benefits-management-aca-view-coverage.png)

Hvis noen av standardverdiene fra Affordable Care-dekningsgruppen har blitt overstyrt, vises en stjerne ved siden av verdien som ble endret. Hvis verdiene for alle tolv månedene er de samme, og ikke har blitt overstyrt, vises verdien i **Alle 12 måneder**-kolonnen.

Du kan vise ansatte som er merket som ikke ACA-rapporterbare, og som ikke vil kreve et skjema 1095-C. Velg **Ikke ACA-rapporterbar** i feltet **Filtrer etter**.

Du kan vise ansatte som ikke er tilordnet en gruppe, eller som er tilordnet til en utløpt gruppe. Velg **Ikke tilordnet eller utløpt gruppe** i **Filtrer etter**.

### <a name="export-to-excel"></a>Eksporter til Excel

Følg denne fremgangsmåten for å eksportere hvilke som helst av listene til Microsoft Excel.

1. Velg knappen **Åpne i Microsoft Office**.
2. Velg valget for **HCM Human Resources midlertidig tabell for intern bruk**.
3. Velg **Last ned**.

### <a name="view-aca-reportable-dependents"></a>Vise ACA-rapporterbare avhengige

Hvis du må rapportere dekkede personer fordi du gir selvforsikret dekning, kan du vise avhengige som dekkes av fordelsplaner, som er merket som **ACA-rapporterbar**. Velg **Vis avhengig dekning** i handlingsruten.

![Vise avhengig dekning.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Dekningsinformasjon for de ansattes avhengige vises.

![Avhengig dekning.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Siden viser bare fordelsplaner som er merket som **ACA-rapporterbare**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
