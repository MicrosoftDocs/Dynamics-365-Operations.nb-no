---
title: Utforme ER-konfigurasjoner for å fylle ut PDF-maler
description: Dette emnet gir informasjon om hvordan du utformer et format for elektronisk rapportering (ER) for å fylle ut en PDF-mal.
author: NickSelin
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7c1c21015a172d7ebaa3577d5d0e55c254ef871e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753294"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>Utforme ER-konfigurasjoner for å fylle ut PDF-maler

[!include[banner](../includes/banner.md)]

Prosedyren i dette emnet er eksempler som viser hvordan en bruker med rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering** kan konfigurere et format for elektronisk rapportering (ER) som genererer rapporter som PDF-filer ved å bruke utfyllbare PDF-dokumenter som rapportmaler. Disse trinnene kan utføres i et hvilket som helst firma med Dynamics 365 Finance eller Regulatory Configuration Services (RCS).

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du ha en av følgende tilgangstyper, avhengig av hvilken tjeneste du bruker for å fullføre prosedyrene i dette emnet:

- Tilgang til Finance for én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Tilgang til RCS for én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

Du må også fullføre prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Til slutt må du laste ned følgende filer.

| Innholdsbeskrivelse                       | Filnavn                                     |
|-------------------------------------------|-----------------------------------------------|
| Mal for den første siden i rapporten | [IntrastatReportTemplate1.pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Mal for andre sider i rapporten    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| Eksempel på ER-format – PDF                          | [Intrastat report (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| Eksempel på ER-format – Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Eksempel på datasett                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Utforme formatkonfigurasjonen

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få tilgang til listen over konfigurasjoner som leveres av Microsoft

1. Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.
2. Kontroller at leverandøren **Litware, Inc** er tilgjengelig og merket som aktiv.
3. Velg **Repositorier** på flisen for **Microsoft**-leverandør.

    > [!NOTE]
    > Hvis repositoriet av typen **LCS** finnes allerede, hopper du over resten av trinnene i denne prosedyren.

4. Velg **Legg til**.
5. Velg alternativet **LCS** i feltgruppen **Type konfigurasjonsrepositorium** i rullegardinboksen.
6. Velg **Opprett repositorium**.
7. Velg **OK**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Få modellkonfigurasjoner som leveres av Microsoft

1. Til venstre på siden **Konfigurasjonsrepositorier** velger du **Vis filtre**-knappen (traktsymbolet).
2. Legg til et filter for en verdi i **LCS** i **Type**-feltet, og bruk operatoren **begynner med**.
3. Velg **Bruk**.
4. Velg **Åpne**.
5. Velg **Intrastat-modell** i treet.
6. Velg versjon **1** på hurtigfanen **Versjoner**.

    > [!NOTE]
    > Hvis **Importer**-knappen på hurtigfanen **Versjoner** ikke er tilgjengelig, hopper du over resten av trinnene i denne prosedyren.

7. Velg **Import**.
8. Velg **Ja** for å bekrefte importen av den valgte versjonen av modellkonfigurasjonen for **Intrastat-modell**.

### <a name="create-a-new-format-configuration"></a>Opprette en ny formatkonfigurasjon

1. I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.
2. Velg **Intrastat-modell** i treet.
3. Velg **Opprett konfigurasjon**.

    > [!NOTE]
    > Hvis knappen **Opprett konfigurasjon** ikke er tilgjengelig, må du aktivere utformingsmodus på siden **Parametere for elektronisk rapportering**, som kan åpnes fra arbeidsområdet **Elektronisk rapportering**.

4. I rullegardinboksen i feltgruppen **Ny** velger du alternativet **Format basert på datamodell Intrastat**.
5. I **Navn**-feltet skriver du inn **Intrastat-rapport (PDF)**.
6. I **Beskrivelse**-feltet angir du **Intrastat-rapport i PDF-format**.

    > [!NOTE]
    > Den aktive konfigurasjonsleverandøren angis automatisk. Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen. Selv om andre leverandører kan bruke denne konfigurasjonen, kan de ikke vedlikeholde den.

7. Valgfritt: I **Formattype**-feltet kan du velge et bestemt format for elektronisk dokument. Hvis du velger **PDF**, vil ER-operasjonsdesigneren under utformingen bare tilby formatelementene som bare gjelder for dokumenter som genereres i PDF-format **(PDF\Fil**, **PDF\PDF-sammenslåing** osv.). Hvis du lar dette feltet stå tomt, vil et format for elektronisk dokument angis under utformingen i ER-operasjonsutformingen når det første formatelementet legges til. Hvis du for eksempel legger **til Excel\Fil** som det første formatelementet, vil ER-opersjonsdesigneren bare tilby formatelementene som bare gjelder for dokumenter som genereres i Excel-format (**Excel\Celle**, **Excel\Område** osv.). format.
8. Velg **Opprett konfigurasjon**.

En ny ER-formatkonfigurasjon opprettes. Du kan bruke utkastversjonen av denne konfigurasjonen til å lagre ER-formatkomponenten som er utformet for å generere elektroniske dokumenter i PDF-format.

### <a name="design-the-format-of-an-electronic-document"></a>Utforme formatet på et elektronisk dokument

I ER-formatkonfigurasjonen som du opprettet, skal du nå utforme ER-formatet som genererer rapporten **Intrastat-kontroll** i PDF-format. Den første siden i denne rapporten må vise et sammendrag av rapporten og detaljer om utenrikshandelstransaksjonene som det rapporteres om. De andre sidene må bare vise detaljer om utenrikshandelstransaksjonene som det rapporteres om. Fordi rapportsidene som genereres, må ha forskjellige oppsett, brukes to forskjellige maler i PDF-format i ER-formatet.

Åpne PDF-malene som du lastet ned, i et PDF-visningsprogram. Legg merke til at hver mal inneholder flere felt som må fylles ut. I hver mal vises detaljer om utenrikshandelstransaksjoner som 42 rader, der hver har ni felt. Radnummeret vises på slutten av hvert felts navn (for eksempel **Dato 1**...**Dato 42** og **Artikkel 1**...**Artikkel 42**).

Illustrasjonen nedenfor viser PDF-malen for den første siden i rapporten.

![Mal 1](media/rcs-ger-filloutpdf-template1.png)

Illustrasjonen nedenfor viser PDF-malen for de andre sidene i rapporten.

![Mal 2](media/rcs-ger-filloutpdf-template2.png)

1. Velg **Utforming** på siden **Konfigurasjoner**.
2. Velg **Legg til rot**.
3. Velg **PDF \> PDF-sammenslåing** i rullegardinlisten.

    Når du velger elementet **PDF-sammenslåing** som rotelement i formatet, vil alle PDF-dokumenter som genereres ved kjøring, bli slått sammen til ett endelig PDF-dokument. Hvis du bare trenger én PDF-mal for å generere alle nødvendige dokumenter ved hjelp av ER-formatet du utformer, kan du velge **PDF-fil** som rotelement.

4. Angi **Utdata** i **Navn**-feltet.
5. I **Språkinnstillinger**-feltet velger du **Brukerinnstillinger**. Rapporten vil bli generert på det foretrukne språket til brukeren som kjører den.
6. I **Kulturinnstillinger**-feltet velger du **Brukerinnstilling**. Verdier og datoer som vises på sidene i rapporten, formateres basert på den foretrukne nasjonale innstillingen til brukeren som kjører rapporten.
7. Velg **OK**.
8. Velg **Importer fra PDF** i kategorien **Importer** i handlingsruten.

    Når et utfyllbart PDF-dokument importeres som en mal for dette ER-formatet, opprettes alle de nødvendige ER-formatelementene (**PDF-fil**, **Feltgruppe** og **Felt**-elementer) automatisk i formatet som er utformet, basert på strukturen til PDF-dokumentet som importeres.

9. Velg **Bla gjennom**. Gå til og velg **IntrastatReportTemplate1.pdf**-filen du lastet ned tidligere som en forutsetning.
10. Velg **OK**.

    Den valgte filen lastes inn, og **Mal**-feltet i dialogboksen **Importer fra PDF** fylles ut.

11. Sett alternativet **Gruppefelt** til **Ja**. Hvis det valgte PDF-dokumentet inneholder noen feltgrupper, vil de bli brukt til å gruppere ER-formatelementene som opprettes. Et **feltgruppe**-formatelement vil bli opprettet for dette formålet.

    Hvis dette alternativet settes til **Nei**, opprettes de nødvendige ER-formatelementene som en flat liste med elementer som er nestet under **PDF-fil**-formatelementet som opprettes.

12. Velg **OK**.

    ![Dialogboksen Importer fra PDF](media/rcs-ger-filloutpdf-importtemplate.png)

13. Utvid **Utdata** i treet.

    Legg merke til at **PDF-fil**-komponenten er opprettet automatisk for å administrere opprettingen av den første siden i rapporten som genereres under kjøring.

14. Utvid **Utdata \> PDF-fil** i treet.

    Legg merke til at den strukturerte listen over formatelementer er opprettet automatisk i dette ER-formatet, basert på strukturen til det utfyllbare PDF-dokumentet som du importerte tidligere.

15. Velg **Utdata \> PDF-fil** i treet.
16. Angi **Side 1** i **Navn**-feltet.

    Dette formatelementet blir brukt til å generere den første siden i **Intrastat-kontroll**-rapporten. Denne siden viser et sammendrag av rapporten og detaljer om utenrikshandelstransaksjoner.

    Hvis du lar **Språkinnstillinger**-feltet stå tomt, vil innstillingen **Språkinnstillinger** for det overordnede **PDF-sammenslåing**-elementet bestemme språket i rapporten som genereres med dette formatelementet. Du kan velge en annen verdi for å overstyre innstillingen for det overordnede elementet.

    Hvis du lar **Kulturinnstillinger**-feltet stå tomt, vil innstillingen **Kulturinnstillinger** for det overordnede **PDF-sammenslåing**-elementet bestemme den nasjonale innstillingen i rapporten som genereres med dette formatelementet. Den nasjonale innstillingen bestemmer formatet på verdier og datoer på sidene i rapporten. Du kan velge en annen verdi for å overstyre innstillingen for det overordnede elementet.

17. Velg kategorien **Importer** i handlingsruten. Legg merke til at **Oppdater fra PDF**-knappen er blitt tilgjengelig for valgt formatelement, **PDF-fil**.

    Du kan bruke denne knappen til å importere den oppdaterte PDF-malen til det redigerte formatet. Når den oppdaterte PDF-malen importeres, vil listen over formatelementer bli endret tilsvarende:

    - For alle nye felt i den oppdaterte PDF-malen opprettes nye formatelementer i det redigerte ER-formatet.
    - Hvis den oppdaterte PDF-malen ikke lenger inneholder felt som svarer til eksisterende formatelementer i det redigerte ER-formatet, slettes disse formatelementene fra ER-formatet.

18. Velg **Vedlegg** i kategorien **Format**.

    Legg merke til at det importerte PDF-dokumentet legges ved det redigerte ER-formatet.

    ![Forhåndsvisning av PDF-vedlegg](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Fortsett å utforme dette formatet ved å importere den andre PDF-malen, legge til nødvendige bindinger til datakilder og så videre.
20. Velg **Lagre**.
21. Lukk siden.
22. Velg **Slett**.
23. Velg **Ja**.

Hvis du vil lære hvordan de nye formatelementene for **PDF-sammenslåing**, **PDF-fil**, **Feltgruppe** og **Felt** kan brukes til å generere dokumenter i PDF-format, kan du importere og analysere ER-eksempelformatet.

### <a name="import-the-format-configuration"></a>Importere formatkonfigurasjonen

Nå skal du importere ER-eksempelformatet som du lastet ned tidligere, slik at du kan generere **Intrastat-kontroll**-rapporten i PDF-format. Den første siden i rapporten må vise et sammendrag av rapporten og detaljer om utenrikshandelstransaksjonene som det rapporteres om. De andre sidene må bare vise detaljer om utenrikshandelstransaksjonene som det rapporteres om.

1. På **Konfigurasjoner**-siden velger du **Veksle \> Last fra XML-fil**.
2. Velg **Bla gjennom**. Gå til og velg **Intrastat report (PDF).version.1.1.xml**-filen du lastet ned tidligere som en forutsetning.
3. Velg **OK**.

## <a name="analyze-the-format-configuration"></a>Analysere formatkonfigurasjonen

### <a name="format-layout"></a>Formatoppsett

1. På **Konfigurasjoner**-siden velger du **Intrastat-modell \> Intrastat-rapport (PDF)** i treet.
2. Velg **Utforming**.
3. Velg **Vis detaljer**.
4. Utvid **Utdata: PDF-sammenslåing** i treet.

    Legg merke til at dette ER-formatet inneholder to **PDF-fil**-elementer, der hvert bruker ulik PDF-mal. Én mal brukes til å generere den første siden i rapporten i PDF-format, og den andre malen brukes til å generere de andre sidene.

5. Utvid **Utdata: PDF-sammenslåing \> Side 1: PDF-fil (IntrastatReportTemplate1)** i treet.
6. Utvid **Utdata: PDF-sammenslåing \> Side N: PDF-fil (IntrastatReportTemplate2)** i treet.

    Vær oppmerksom på at siden innholdet i de to PDF-malene er forskjellige, er også strukturen til de nestede formatelementene for de **to PDF-fil**-elementene forskjellige.

### <a name="format-mapping"></a>Formattilordning

1. Velg kategorien **Tilordning** på **Formatutforming**-siden.
2. Utvid **Sideveksling \> Sider** i treet.

    ![Formeldesigner-siden der modelltreet er utvidet](media/rcs-ger-filloutpdf-reviewformat.png)

    Vær oppmerksom på følgende detaljer:

    - Formatelementet **Utdata \> Side 1** av typen **PDF-fil** er ikke bundet til en datakilde, og uttrykket **Aktivert** for dette formatelementet er tomt. Derfor vil PDF-malen **IntrastatReportTemplate1** bli fylt ut bare én gang når et individuelt PDF-dokument genereres, ved kjøring.
    - Formatelementet **Utdata \> Side N** av typen **PDF-fil** er bundet til **Paging.PageN**-datakilden av typen **Postliste**, og **Aktivert**-uttrykket for dette formatelementet er tomt. Derfor vil PDF-malen **IntrastatReportTemplate2** bli fylt ut for hver post fra den bundne postlisten når et individuelt PDF-dokument genereres, ved kjøring.
    - Ettersom formatelementene **Side 1: PDF-fil** og **Side N: PDF-fil** er underordnet formatelementet **Utdata: PDF-sammenslåing**, vil alle PDF-dokumenter som fylles ut, slås sammen til ett endelig PDF-dokument.
    - Datakildene **Paging.Page1** og **Paging.PageN** konfigureres som filtre med poster fra datakilden **Paging.Pages**. Denne datakilden er konfigurert til å dele hele settet med utenrikshandelstransaksjoner i partier. Hvert parti inneholder opptil 42 poster. Følgende ER-uttrykk brukes til å dele transaksjonene i partier:

        SPLITLIST(Totals.CommodityRecord,42)

    - Datakilden **Paging.Pages** inneholder elementet **Paging.Pages.Enumerated** som returnerer detaljene for hver post som er inkludert i et parti. Disse detaljene omfatter postens rekkefølge i gjeldende parti (feltet **Paging.Pages.Enumerated.Number**). Feltet **Paging.Pages.Enumerated.Number** brukes i **Navn**-uttrykket for **PDF-felt**-formatelementer for dynamisk å genere et feltnavn som er basert på transaksjonsantallet i et parti. Feltnavnet som genereres, brukes deretter til å fylle ut det riktige PDF-feltet i PDF-malen som brukes.
    - Formatelementet **Utdata \> Side N \> Detaljer 2** av typen **PDF-gruppe** er bundet til datakilden **Paging.PageN.Enumerated** (eller **\@.Enumerated** hvis visningsmodusen **Relative path** brukes) av typen **Postliste**. Ved kjøring vil derfor de nestede elementene i denne PDF-gruppen fylles ut for hver post fra den bundne postlisten. På denne måten genereres de enkelte PDF-linjene stort sett når for hvert N. av 42 poster i **Paging.PageN.Enumerated**-listen følgende PDF-felt er utfylt: Dato N, Retning N, Artikkel N osv. I dette tilfellet ligner derfor virkemåten i dette **Feltgruppe**-formatelementet på virkemåten til formatlementene **XML \> Sekvens** og **Tekst \>Sekvens**.

3. Utvid **Utdata \> Side N \> Detaljer2** i treet.
4. Velg **Utdata \> Side N \> Detaljer 2 \> PageFooter** i treet.

    Legg merke til at **Navn**-attributtet for dette formatelementet er definert **som** PageFooter. Legg også merke til at **Navn**-uttrykket for formatelementet er tomt.

5. Velg **Utdata \> Side N \> Detaljer 2 \> Korrigering 1** i treet.

    Legg merke til at **Navn**-attributtet for dette formatelementet er definert som **Korrigering 1**. Legg også merke til at **Navn**-uttrykket for formatelementet defineres som **Paging.FldName("Correction",\@.Number)**.

![Formatutforming der tilordning er valgt](media/rcs-ger-filloutpdf-reviewformat2.png)

Legg merke til at **Felt**-formatelementet brukes til å fylle ut et enkelt felt i et utfyllbart PDF-dokument som er definert som en mal for det overordnede **PDF-fil**-formatelementet. Bindingen for **PDF-fil**-formatelementet eller de nestede elementene, hvis det har nestede elementer, angir verdien som angis i tilsvarende PDF-felt. Forskjellige egenskaper for **Felt**-formatelementet kan brukes til å angi hvilket PDF-felt som fylles ut av et individuelt formatelement:

- I kategorien **Format**, **Navn**-attributtet for formatelementet
- I kategorien **Tilordning**, **Navn**-uttrykket for formatelementet

Ettersom begge egenskapene er valgfrie for et **Felt**-formatelement, brukes følgende regler for å angi PDF-målfeltet:

- Hvis **Navn**-attributtet er tomt og **Navn**-uttrykket returnerer en tom streng ved kjøring, oppstår det et unntak ved kjøring for å varsle brukeren om at det ikke finnes et PDF-felt i PDF-malen som brukes, for å fylle ut PDF-dokumentet.
- Hvis **Navn**-attributtet er definert og **Navn**-uttrykket er tomt, vil PDF-feltet som har samme navn som **Navn**-attributtet for formatelementet, fylles ut.
- Hvis **Navn**-attributtet er definert og **Navn**-uttrykket er konfigurert, vil PDF-feltet som har samme navn som verdien som returneres av **Navn**-uttrykket for formatelementet, fylles ut.

> [!NOTE]
> En PDF-avmerkingsboks kan angis som valgt på følgende måter:
>
> - Når det tilsvarende **Felt**-formatelementet er bundet til et datakildefelt av datatypen **Boolsk** som har verdien **Sann**
> - Når det tilsvarende **Felt**-formatelementet inneholder et nestet **Streng**-formatelement som er bundet til et datakildefelt som har tekstverdien **1**, **Sann** eller **Ja**

## <a name="run-the-format-configuration"></a>Kjøre formatkonfigurasjonen

### <a name="import-the-format-configuration"></a>Importere formatkonfigurasjonen

Nå skal du laste inn eksempel-ER-formatet **Intrastat (import from Excel**). Dette formatet er utformet for å analysere en brukerdefinert Microsoft Excel-arbeidsbok som simulerer utenrikshandelstransaksjoner.

1. På **Konfigurasjoner**-siden velger du **Veksle \> Last fra XML-fil**.
2. Velg **Bla gjennom**. Gå til og velg filen **Intrastat (import from Excel).version.1.1.xml**-filen du lastet ned tidligere som en forutsetning.
3. Velg **OK**.
4. Velg **Intrastat-modell \> Intrastat (import from Excel)** i treet.
5. Velg **Rediger**.
6. Sett alternativet **Standard for modelltilordning** til **Ja**.

    > [!NOTE]
    > Hvis du tidligere har satt alternativet **Standard for modelltilordning** til **Ja** for **Intrastat-modell**-konfigurasjonen eller en annen konfigurasjon som er nestet under **Intrastat-modell**-konfigurasjonen, setter du dette alternativet til **Nei**.

    Når alternativet **Standard for modelltilordning** er satt til **Ja**, tilordnes det importerte ER-formatet **Intrastat (import from Excel)** som standard datakilde for **Intrastat-rapport (PDF)**-formatkonfigurasjonen. Når **Intrastat-rapport (PDF)**-formatkonfigurasjonen kjøres, vil innholdet i Excel-arbeidsboken som analyseres av ER-formatet **Intrastat (import from Excel)**, simulere utenrikshandelstransaksjoner som må rapporteres. Illustrasjonen nedenfor viser et eksempel på en Excel-arbeidsbok.

    ![Excel-arbeidsbok med eksempeldata](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Kjøre formatkonfigurasjonen

1. På **Konfigurasjoner**-siden velger du **Intrastat-modell \> Intrastat-rapport (PDF)** i treet.
2. Velg **Kjør**.
3. Velg **Bla gjennom**. Gå til og velg **Intrastat sample data.xlsx**-filen du lastet ned tidligere som en forutsetning.
4. Velg **OK**.
5. I **Rapportretning**-feltet velger du **Begge** for å fylle ut alle transaksjoner fra den importerte Excel-arbeidsboken i PDF-rapporten som genereres.
6. Velg **OK**.
7. Se gjennom PDF-dokumentet som er generert.

Illustrasjonen nedenfor viser et eksempel på den første siden i rapporten som genereres.

![Første side i den genererte rapporten](media/rcs-ger-filloutpdf-generatedreport.png)

Illustrasjonen nedenfor viser et eksempel på en annen side i rapporten som genereres.

![Annen side i den genererte rapporten](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a>Tilleggsressurser

- [ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format (november 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Utforme ER-konfigurasjoner for å generere rapporter i Word-format](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
