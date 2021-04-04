---
title: Sende ER-måltype per e-post
description: Dette emnet forklarer hvordan du konfigurerer et e-postmål for hver MAPPE- eller FIL-komponent i et ER-format (Elektronisk rapportering).
author: NickSelin
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0a8ee5c16e2292481e24ada4853eed9a6824ef2d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562028"
---
# <a name="email-er-destination-type"></a>Sende ER-måltype per e-post

[!include [banner](../includes/banner.md)]

Når et ER-format (Elektronisk rapportering) kjøres, kan du generere ett eller flere utgående dokumenter. **Mappe**- eller **Fil**-formatkomponenter brukes i ER-formater for å angi strukturen til utgående dokumenter. Du kan konfigurere et e-postmål for disse komponenttypene for å sende utgående dokumenter som e-postvedlegg.

Du kan konfigurere en e-postmål for hver **mappe**- eller **fil**-komponent i et ER-format. I dette tilfellet **sendes hvert utgående dokument med e-post enkeltvis**. Basert på denne målinnstillingen leveres et generert dokument som et vedlegg til en e-post. 

> [!NOTE]
> Hvis det ikke genereres et dokument fordi det **Aktiverte**-uttrykket for den relevante **Fil**-komponenten er konfigurert til å returnere en **Falsk** boolsk verdi, sendes det ingen e-post, selv om målet for en e-post er konfigurert og aktivert for komponenten.

Du kan også [gruppere](#grouping) flere **Mappe** eller **Fil**-komponenter sammen og deretter konfigurere et e-postmål for alle komponentene i gruppen. I dette tilfellet blir alle utgående dokumenter som generert av komponenter som tilhører gruppen **er sendt som flere vedlegg i én enkelt e-post**. Basert på denne målinnstillingen leveres hvert genererte dokument som et vedlegg i én enkelt e-post.

> [!NOTE]
> Hvis minst ett dokument er generert av en **Fil**-komponent i en gruppe komponenter, sendes det en e-post. Hvis det ikke genereres et dokument av grupperte komponenter fordi **Aktivert**-uttrykket for hver **Fil**-komponent er konfigurert til å returnere en **Falsk** boolsk verdi, sendes det ingen e-post, selv om målet for en e-post er konfigurert og aktivert for den gruppen med komponenter.
>
> **E-post** er det eneste målet som kan konfigureres for en gruppe av komponenter. Hvis du vil levere et dokument som er sendt via e-post, basert på innstillingen for e-postmål for en gruppe, legger du til én målpost til, velg ønsket komponent, og konfigurerer deretter et annet mål for denne posten.

Flere grupper med komponenter kan konfigureres for én enkelt ER-formatkonfigurasjon. På denne måten kan du konfigurere et e-postmål for hver gruppe med komponenter, og et e-postmål for hver komponent.

## <a name="configure-an-email-destination"></a>Konfigurere et e-postmål

Hvis du vil sende en utdatafil eller flere utdatafiler via e-post, går du til siden **Mål for elektronisk rapportering** og hurtigfanen **Fildestinasjon** og velger en komponent eller komponentgruppe i rutenettet, og deretter velger du **Innstillinger**. I dialogboksen **Innstillinger for mål** som vises, i fanen **E-post**, setter du alternativet **Aktivert** til **Ja**. Du kan deretter angi e-postmottakere og redigere emnet og brødteksten i e-postmeldingen. Du kan enten definere konstant tekst for e-postemnet og meldingsteksten, eller du kan bruke ER-[formler](er-formula-language.md) for å opprette e-posttekster dynamisk.

Du kan konfigurere e-postadresser for ER på to måter. Konfigurasjonen kan fullføres på samme måte som Utskriftsbehandling-funksjonen fullfører den, eller du kan løse en e-postadresse ved å bruke en direkte referanse til ER-konfigurasjonen via en formel.

[![Sette alternativet Enabled til Ja for et e-postmål](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Typer e-postadresser

Hvis du velger **Rediger** ved siden av **Til**- eller **Kopi**-feltet i dialogboksen **Målinnstillinger**, vises dialogboksen **E-post til**. Velg **Legg til**, og velg deretter typen e-postadresse som skal brukes. To typer støttes for øyeblikket: **E-post for utskriftsbehandling** og **E-post for konfigurasjon**.

[![Velge type e-postadresse](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>E-post for utskriftsbehandling

Hvis du velger **E-post for utskriftsbehandling** som typen e-postadresse, kan du angi faste e-postadresser i dialogboksen **E-post til** ved å angi følgende felt:

- Velg feltet **E-postkilde** og deretter **Ingen**.
- I feltet for **Flere e-postadressene, atskilt med ";"** angir du de faste e-postadressene.

Du kan også hente e-postadresser fra kontaktdetaljene for parten du genererer et utgående dokument for. Hvis du vil bruke e-postadresser som ikke er faste, går du til feltet **E-postkilde** og velger [rollen](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) til parten for et filmål. Følgende roller støttes:

- Kunde
- Leverandør
- Prospekt
- Kontakt
- Konkurrent
- Worker
- Søker
- Potensiell leverandør
- Sperret leverandør

Hvis du for eksempel vil konfigurere et e-postmål for et ER-format som brukes til å behandle leverandørbetalinger, velger du **Leverandør**-rollen.

Når du har valgt den ønskede rollen, velger du **Bind**-knappen (kjedesymbol) ved siden av feltet **Kildekonto for e-post** for å åpne siden for [formelutforming](general-electronic-reporting-formula-designer.md). Du kan deretter bruke denne siden til å konfigurere en formel som returnerer, ved kjøretid, kontonummeret til parten som er tilordnet den konfigurerte rollen, fra det behandlede dokumentet til e-postdestinasjonen.

> [!NOTE]
> Formler er spesifikke for ER-konfigurasjonen.

På siden **Formelutforming**, i feltet **Formel**, angir du en dokumentspesifikk referanse til en støttet rolle. I stedet for å skrive inn referansen, går du til ruten **Datakilde** og velger datakildenoden som representerer en konto for den konfigurerte rollen, og deretter velger du **Legg til datakilde** for å oppdatere formelen. Hvis du for eksempel konfigurerer e-postmålet for konfigurasjonen **ISO 20022 Kredittoverføring** som brukes til å behandle leverandørbetalinger, er noden som representerer en leverandørkonto `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Konfigurere en e-postkildekonto](./media/er_destinations-emaildefineaddresssource.gif)

Hvis kontonumrene til den konfigurerte rollen er unike for hele forekomsten av Microsoft Dynamics 365 Finance, kan feltet for **firma for e-postkilde** i dialogboksen **E-post til** være tomt.

Du kan også ha en situasjon der forskjellige parter i den [globale adresseboken](../../fin-ops/organization-administration/overview-global-address-book.md) er registrert i forskjellige firmaer ([juridiske enheter](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) på en slik måte at alle bruker samme kontonummer til å fylle den konfigurerte rollen. I dette tilfellet er ikke kontonumrene for den konfigurerte rollen unike for hele Finance-forekomsten. Derfor, for å eksplisitt velge en part, kan du ikke angi bare et kontonummer. Du må også angi firmaet som parten er registrert for, i området, for å fylle den konfigurerte rollen. Velg **Bind**-knappen (kjedesymbol) ved siden av feltet for **Firma for e-postkilde** i dialogboksen **E-post til** for å åpne siden for [Formeldesigner](general-electronic-reporting-formula-designer.md). Du kan deretter bruke denne siden til å konfigurere en formel som returnerer, ved kjøretid, koden til firmaet som den ønskede kilden må finnes i området til.

> [!TIP]
> Hvis du må bruke firmakoden til å kjøre et ER-format, men ER-formatet ikke gir noen datakilde som firmakoden kan hentes fra, konfigurerer du `GetCurrentCompany()`-formelen ved å bruke den innebygde ER-funksjonen [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formler er spesifikke for ER-konfigurasjonen.

Hvis du vil angi hvilke typer e-postadresser som må brukes ved kjøring, går du til dialogboksen **E-post til** og velger **Rediger** ved siden av **Til**-feltet for å åpne nedtrekksdialogboksen **Tilordne e-postadresse**. Deretter angir du følgende felt:

- I feltet **Formål** velger du ønsket formål. Bare e-postadresser til de valgte formålene fra kontakter av den oppdagede parten vil bli brukt.
- Angi alternativet **Primærkontakt** til **Ja** for å bruke en e-postadresse som er konfigurert for den oppdagede parten som den primære e-postadressen.

> [!NOTE]
> Hvis det er valgt formål i feltet **Formål**, og alternativet **Primærkontakt** er satt til **Ja** samtidig, vil alle e-postmeldinger som oppfyller minst ett konfigurert kriterium, bli brukt under kjøring.

### <a name="configuration-email"></a>E-post for konfigurasjon

Velg **Konfigurer e-post** som e-postadressetype hvis konfigurasjonen du bruker, har en node i datakildene som returnerer enten én e-postadresse eller flere e-postadresser som er atskilt med semikolon (;). Du kan bruke [datakilder](general-electronic-reporting.md#FormatComponentOutbound) og [funksjoner](er-formula-language.md#functions) i formeldesigneren for å hente en riktig formatert e-postadresse eller riktig formaterte e-postadresser som er atskilt med semikolon. Hvis du for eksempel bruker **ISO 20022 Kredittoverføring**-konfigurasjonen, er noden som representerer den primære e-postadressen for en leverandør fra leverandørens kontaktopplysninger som følgebrevet skal sendes til, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurere en e-postadressekilde](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Gruppere formatkomponenter

Hvis du vil gruppere formatkomponenter, går du til siden **Mål for elektronisk rapportering** i hurtigfanen **Filmål** og velger **Gruppe**.

**E-post** er det eneste tidligere konfigurerte målet som fremdeles er tilgjengelig for de valgte komponentene. Ingen andre tidligere konfigurerte mål er tilgjengelige, fordi de vurderes som ikke for en gruppe med komponenter. Du vil bli varslet om disse endringene etter behov.

Posten du la til tidligere, regnes som overskriften i gruppen som opprettes. Denne overskriftsposten inneholder s-postmålinnstillingene for gruppen. Andre poster er gruppemedlemmer som vil bruke e-postmålinnstillingene for gruppens overskriftspost.

Hvis du vil dele opp gruppen for formatkomponenter, går du til hurtigfanen **Filmål** og velger du en post som hører til gruppen, og deretter velger du **Del opp gruppe**.

- Hvis du velger en overskriftspost, blir hele gruppen deles opp.
- Hvis du velger en medlemspost, og det er den siste medlemsposten i en gruppe, blir hele gruppen deles opp.
- Hvis du velger en medlemspost som ikke er den siste medlemsposten i en gruppe, vil denne posten bli utelatt fra den gjeldende gruppen.

Følgende illustrasjon viser strukturen til et ER-format som ble konfigurert til å produsere en zippet utgående fil som inneholder et purrebrev og riktige kundefakturaer i PDF-format.

[![Struktur for et ER-format som genererer utgående dokumenter](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Følgende illustrasjon viser prosessen, som beskrevet i dette emnet, med gruppering av individuelle komponenter og aktivering av **E-post**-målet for den nye gruppen, slik at det sendes en purrenota sammen med riktig kundefaktura som e-postvedlegg.

[![Gruppere individuelle komponenter og aktivere e-postmålet](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]