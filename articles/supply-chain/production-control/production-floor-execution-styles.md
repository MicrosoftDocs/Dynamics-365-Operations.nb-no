---
title: Utform grensesnittet for produksjonsutførelse
description: Artikkelen beskriver hvordan du konfigurerer skjemakontroller slik at standard stiler for produksjonsgulvutførelse brukes på dem.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ad6ecd591353fe8ddc1a5b9049d65491fb58e98a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859147"
---
# <a name="style-the-production-floor-execution-interface"></a>Utform grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Artikkelen beskriver hvordan du konfigurerer skjemakontroller slik at standard stiler for produksjonsgulvutførelse brukes på dem.

## <a name="forms-and-dialogs"></a>Skjemaer og dialogbokser

Stiler kan bare brukes på et skjema eller en dialogboks hvis følgende krav er oppfylt:

- Hvis skjemaet skal ligne på et eksisterende skjema for fremdrift i rapporten, må navnet på skjemaet eller dialogboksen begynne med `JmgProductionFloorExecutionCustomInputDialog`.
- Skjemaet eller dialogboksen kan inneholde en detaljskjemadel. Hvis du vil bruke stiler på den, må navnet på detaljskjemadelen starte med `JmgProductionFloorExecutionCustomDetailsDialog`.
- Hvis skjemaet eller dialogboksen skal ha en enkel visning, må navnet på den enkle visningen starte med `JmgProductionFloorExecutionCustomDialog`. Eksempler på skjemaer som har enkel visning, inkluderer startskjemaet og skjemaet for indirekte aktivitet.
- Alle kontrollene i dialogboksen må konfigureres som beskrevet i denne artikkelen.

> [!IMPORTANT]
> Funksjonene som nevnes i de to første poengene til denne listen, krever Supply Chain Management versjon 10.0.19 eller senere.

Stiler kan bare brukes på **OK**-knappen i en dialogboks hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppenavnet starter med `OkButtonGroup`.

Stiler kan bare brukes på **Avbryt**-knapepn i en dialogboks hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppenavnet starter med `CancelButtonGroup`.

### <a name="header"></a>Hode

Illustrasjonen nedenfor viser et vanlig skjema- eller dialogbokshode.

![Vanlig skjema- eller dialogbokshode.](media/pfe-styles-header.png "Vanlig skjema- eller dialogbokshode")

I Visual Studio opprettes hoder ved hjelp av en struktur som den som vises i illustrasjonen nedenfor.

![Vanlig kodestruktur for oppretting av et hode.](media/pfe-styles-header-code-structure.png "Vanlig kodestruktur for oppretting av et hode")

Hvis du vil legge til tekst i hodet, bruker du kode som følgende eksempel.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Når du skriver hodekoden, bruker du følgende regler:

- Navnet på hovedgruppen må være `TableRowHeaderGroup`.
- Hver tekstblokk (atskilt med punkter) må starte med `HeaderFieldWithSeparatorText`.
- Ettertekstnavnet må starte med `HeaderFieldText`.
- `CaptionImage` kan hoppes over.

### <a name="progress-indicator"></a>Fremdriftsindikator

Du kan ta med en fremdriftsindikator, som vises til høyre for hodet. Illustrasjonen nedenfor viser en fremdriftsindikator.

![Vanlig fremdriftsindikator.](media/pfe-styles-header-progress.png "Vanlig fremdriftsindikator")

Hvis du vil vise fremdriftsindikatoren, må tekstfeltet ha navnet `ShowProgress`.

## <a name="grid"></a>Rutenett

Stiler brukes automatisk. Ingen spesifikk konfigurasjon er nødvendig.

Rutenettet må ha `TabularView`-en stil, og `run()`-metoden på det egendefinerte skjemaet må overskrives, fordi et nytt rutenett ikke støttes ennå. Legg til følgende kode

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Hvis du vil oppdatere data i en hovedvisning, kan det hende at du vil bruke noe som `this.parmParentForm().updateLayout();` i en `click`-metode for handlingen. (Hvis du vil ha et eksempel, kan du se på `JmgProductionFloorExecutionReportFeedbackAction`-klassen.) Bare sørg for at `parmDataSource` er angitt i `init`-metoden for det nye skjemaet (`formCaller.parmDataSource(this.dataSource(1));`). Hvis du vil ha et eksempel, kan du se på `JmgProductionFloorExecutionMainGrid`-skjemaet.

## <a name="card-view"></a>Kortvisning

Stiler kan bare brukes på kartvisningskontroller hvis følgende krav er oppfylt:

- Hver kortvisning ligger i en skjemagruppe.
- Gruppenavnet starter med `CardGroup` (for eksempel `CardGroupJobsView`).

Illustrasjonen nedenfor viser en kortvisning som ikke har kontroller i den.

![Kortvisning uten elementer.](media/pfe-styles-empty-card.png)

Illustrasjonene nedenfor viser kortvisninger som har kontroller i dem.

![Kort med elementer som viser Hz.](media/pfe-styles-elements.png)

![Kort med elementer for en vedlikeholdsforespørsel.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Forretningskort

Stiler kan bare brukes på forretningskortkontroller hvis følgende krav er oppfylt:

- Hver forretningskort ligger i en skjemagruppe.
- Gruppenavnet starter med `BusinessCardGroup` (for eksempel `BusinessCardGroupJobsList`).

Angi følgende egenskaper på forretningskortet:

- **Stil:** *liste*
- **Utvidet stil:** *cardList*
- **Flervalg:** *Nei*
- **Vis kolonneetiketter:** *Nei*

![Forretningskort.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Valgknapp

Stiler kan bare brukes på valgknapper hvis følgende krav er oppfylt:

- Hver valgknapp finnes i en skjemagruppe.
- Gruppenavnet starter med `RadioTextBelow` eller `RadioTextRight`, avhengig av hvor du vil at teksten skal vises.

Angi følgende egenskaper på valgknappen:

- **Veksle-knapp:** *Kontroll*
- **Veksleverdi:** *På* hvis valgknappen skal velges. Hvis ikke *Av*

Illustrasjonen nedenfor viser et eksempel der teksten vises under valgknappene.

![Valgknapper med tekst nedenfor.](media/pfe-styles-radio-text-below.png)

Illustrasjonen nedenfor viser et eksempel der teksten vises til høyre for valgknappene.

![Valgknapper med tekst til høyre.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Valgknapper i Internet Explorer

Valgknappstiler støttes ikke i Internet Explorer. Illustrasjonen nedenfor viser hvordan ralgknapper ser ut i Internet Explorer.

![Valgknapper i Internet Explorer.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Knapper

Stiler kan bare brukes på knapper hvis følgende krav er oppfylt:

- Hver gruppe av knapper finnes i en skjemagruppe. Alle knappene i gruppen vil ha samme stil.
- Det er ingen krav til navnet på gruppen.

Angi følgende egenskaper på knappene:

- **Knappevisning:** *TextWithImageLeft*.
- **Vanlig bilde:** Denne egenskapen kan ikke være tom. Bruk eksempel *CoffeeScript*.
- **Tekst:** Denne egenskapen kan ikke være tom. Bruk eksempel *Start Break*.
- **Bredde:** *Automatisk* eller *SizeToContent*
- **Høyde:** *Automatisk* eller *SizeToContent*

### <a name="primary-button"></a>Primærknapp

Stiler kan bare brukes på en primærknapp hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppenavnet starter med `DefaultButtonGroup` eller `PrimaryButtonGroup` (for eksempel `DefaultButtonGroup10`).

![Primærknapp.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>Sekundærknapp

Stiler kan bare brukes på en sekundærknapp hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppen kalles **Høyre-panel**, eller gruppenavnet begynner med `SecondaryButtonGroup`.

![Sekundærknapp.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Tredje gruppe-knapp

Stiler kan bare brukes på en tredje gruppe-knapp hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppen kalles **Venstre-panel**, eller gruppenavnet begynner med `ThirdButtonGroup`.

![Tredje gruppe-knapp.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Fjerde gruppe-knapp

Stiler kan bare brukes på en fjerde gruppe-knapp hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppenavnet starter med `FourthButtonGroup`.

Angi følgende egenskaper på knappen:

- **Knappevisning:** *TextOnly*.
- **Vanlig bilde:** Denne egenskapen må være tom.
- **Tekst:** Denne egenskapen kan ikke være tom. Bruk for eksempel *Vis* eller *Rediger*.
- **Bredde:** *Automatisk*.
- **Høyde:** *Automatisk*.

![Fjerde gruppe-knapp.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Flat-knapp

Stiler kan bare brukes på en flat-knapp hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppenavnet starter med `FlatButtonGroup`.

Angi følgende egenskaper på knappen:

- **Knappevisning:** *ImageOnly*.
- **Vanlig bilde:** Denne egenskapen kan ikke være tom. Bruk eksempel *CoffeeScript*.
- **Tekst:** Denne egenskapen må være tom.
- **Bredde:** *Automatisk* eller *SizeToContent*
- **Høyde:** *Automatisk* eller *SizeToContent*

![Flat-knapp.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Fortsett-knappen

Stiler kan bare brukes på en Fortsett-knapp hvis følgende krav er oppfylt:

- Knappen finnes i en skjemagruppe.
- Gruppenavnet starter med `ContinueButtonGroup`.

Angi følgende egenskaper på knappen:

- **Knappevisning:** *ImageOnly*.
- **Vanlig bilde:** *Forover*
- **Tekst:** Denne egenskapen må være tom.
- **Bredde:** *Automatisk* eller *SizeToContent*
- **Høyde:** *Automatisk* eller *SizeToContent*

![Fortsett-knappen.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Kombinasjonsboks

En kombinasjonsboks er en kombinasjon av tre kontroller: en inndatakontroll, en knapp som fjerner inndatakontrollen og en knapp som kjører et søk.

Stiler kan bare brukes på en kombinasjonsboks hvis følgende krav er oppfylt:

- Kombinasjonsboksen finnes i en skjemagruppe.
- Gruppenavnet starter med `Combobox`.
- I gruppen er den første kontrollen en `AxFormStringControl`-kontroll. Denne kontrollen viser den gjeldende verdien, og det er der brukeren angir den nødvendige verdien.
- Den andre kontrollen er en `CommonButton`-kontroll, og navnet begynner med `ClearButton`. Denne knappen må inneholde kode som bruker `enable`-egenskapen til å vise eller skjule knappen. Hvis du for eksempel vil vise eller skjule **Fjern**-knappen mens brukeren skriver inn informasjon i inndatakontrollen, kan du bruke følgende kode.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Du bør ha en metode der dataene angis i inndatakontrollen. Aktiver **Fjern**-knappen i den metoden. Her er et eksempel:

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    Bruk følgende kode for `clicked`-metoden for **Fjern**-knappen.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Angi verdien for inndatakontrollen, `AxFormStringControl`, når skjemaet initialiseres ved hjelp av `init`-metoden. Hvis verdien ikke er tom, aktiverer du **Fjern**-knappen. Hvis verdien er tom, deaktiverer du **Fjern**-knappen.

- Den tredje kontrollen er en `CommonButton`-kontroll, og navnet begynner med `SearchButton`.

Illustrasjonen nedenfor viser to kombinasjonsbokskontroller. Kombinasjonsboksen til venstre har en tom tekstboks, og **Fjern**-knappen er deaktivert. Kombinasjonsboksen til høyre har tekst i tekstboksen, og **Fjern**-knappen er aktivert.

![Kombinasjonsbokser med og uten Fjern-knapp.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Hurtigfilter

Hurtigfilterkontrollen legger til et søkefelt på siden. Du kan bruke stiler på et hurtigfilter hvis følgende krav er oppfylt:

- Hurtigfilteret finnes i en skjemagruppe.
- Gruppenavnet starter med `SearchInputGroup`.
- I gruppen er den første kontrollen en `QuickFilter`-kontroll. (Brukeren søkestrengen i denne kontrollen.)
- Den andre kontrollen er en `FormStaticTextControl` med navnet `NumberOfResults`. (Denne kontrollen er valgfri. Hvis den er inkludert, viser den antallet varer som blir funnet.)
- Den tredje kontrollen er en `CommonButton`-kontroll, og navnet begynner med `ClearButton`.

Illustrasjonen nedenfor viser to hurtigfilterkontroller. Hurtigfilteret til venstre har et tomt hurtigfilter, og antall resultater vil ikke være synlig. Hurtigfilteret til høyre inneholder en søkestreng og viser antall resultater.

![Eksempler på en hurtigfilterkontroll med og uten en søkestreng.](media/pfe-styles-quick-filter.png "Eksempler på en hurtigfilterkontroll med og uten en søkestreng")

## <a name="center-align-elements-on-a-tab"></a>Midtjuster elementer på en fane

Hvis du vil justere elementer i midten på en fane, må gruppenavnet starte med `TabContentGroup`, og gruppen må ha følgende egenskaper:

- **Breddemodus:** `SizeToAvailable`
- **Høydemodus:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Juster et rutenett, en detaljdel og et hurtigfilter

Hvis du vil ordne et tilpasset rutenett, en detaljdel og et hurtigfilter slik at de ligner på standardutformingen, må du huske følgende punkt når du setter dem sammen:

- Hvis rutenettet har et hurtigfilter, skal både rutenettet og hurtigfilteret være i gruppen som har et navn som begynner med `GridGroup`.
- Hvis du vil bruke stiler på en detaljdel, må gruppenavnet starte med `DetailInformationGroup`.

Illustrasjonen nedenfor viser et vanlig rutenett som inneholder et hurtigfilter og en detaljdel til høyre.

![Vanlig rutenett med et hurtigfilter og en detaljdel.](media/pfe-styles-align-grid.png "Vanlig rutenett med et hurtigfilter og en detaljdel")

I Visual Studio kan et rutenett, en detaljdel og et hurtigfilter opprettes ved hjelp av en struktur som den som vises i illustrasjonen nedenfor.

![Vanlig kodestruktur som justerer et rutenett, en detaljdel og et hurtigfilter.](media/pfe-styles-header-code-structure2.png "Vanlig kodestruktur som justerer et rutenett, en detaljdel og et hurtigfilter")

## <a name="additional-resources"></a>Tilleggsressurser

- [Tilpass grensesnittet for produksjonsutførelse](production-floor-execution-customize.md)
- [Utforme grensesnittet for produksjonsutførelse](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
