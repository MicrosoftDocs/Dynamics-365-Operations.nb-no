---
title: Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER
description: Dette emnet beskriver hvordan du bruker verktøyet for elektronisk rapportering til å generere forretningsdokumenter som har innebygde bilder og figurer.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: bfa8137de7b782ba80a0d80c987a96c37b3a7d86
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361413"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER

[!include [banner](../includes/banner.md)]

Du kan bruke ER-verktøyet (Elektronisk rapportering) til å utforme rapporter som du kan kjøre for å generere nødvendige elektroniske dokumenter. Du kan bruke Microsoft Excel- eller Microsoft Word-dokumenter eller til å angi oppsettet til en rapport. Med ER-operasjonsutforming kan du legge ved et Excel- eller Word-dokument som en mal for rapporten. Følgende navngitte elementer i den tilknyttede malen er knyttet til formatelementene i ER-rapporten. Formatelementer i rapporten er bundet til datakilder. Disse elementene angir dataene som blir lagt inn i de genererte dokumentene under kjøring.

Denne nye funksjonaliteten går utover eksisterende ER-funksjoner for oppretting av dokumenter i Microsoft Office-formater. Hvis du vil ha mer informasjon, kan du spille av følgende oppgaveveiledninger: Du finner disse oppgaveveiledningene under 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)-forretningsprosessen.

- ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format
- ER Utforme en konfigurasjon for generering av rapporter i Microsoft WORD-format

## <a name="embed-an-image-in-an-excel-document"></a>Bygge inn et bilde i et Excel-dokument

### <a name="embed-an-image-in-an-excel-worksheet"></a>Bygge inn et bilde i et Excel-regneark

Først må du legge til en plassholder for bildet i et Excel-dokument. Åpne en Excel-arbeidsbok og legg til et bilde som en plassholder for bildet du vil legge til senere. Bruk deretter ER-verktøyet til å legge til en ny ER-formatkonfigurasjon for å ta med rapporten du utformer. Tilknytt Excel-arbeidsboken som en mal for rapportens format, og importer deretter innholdet i arbeidsboken til ER-formatet. Formatdefinisjonen opprettes automatisk. Bildeplassholderen du la til, vil bli inkludert i ER-formatdefinisjonen som et **CELLE**-element.

> [!NOTE]
> Du kan angi formatdefinisjonen manuelt i stedet for å importere den. Når du lagrer endringene, valideres formatet.

Deretter binder du **CELLE**-elementet i ER-formatet til feltet fra formatets datakilde som gir bildets data i binært format ved kjøretid. Når en ER-datamodell brukes som datakilde for et format, må datatypen for feltet være [Container](er-formula-supported-data-types-composite.md#container). For øyeblikket kan et ER-datamodellfelt som har datatypen [Container](er-formula-supported-data-types-composite.md#container), være bundet til mange typer datakilder som returnerer bilder i binært format. Du får tilgang til et felt i en datatabell og en fil som er knyttet til datatabellens post, ved hjelp av dokumentbehandlingsrammeverket.

> [!IMPORTANT]
> - Hvis du vil fylle ut bildeplassholderen i dokumentet du oppretter ved hjelp av Excel-malen, må ER-formatet inneholde **CELLE**-elementet som refererer til det navngitte bildeelementet i Excel-malen. Hvis ikke, vises det ingen plassholder for bilde i rapportens utdata. Hvis bindingen av et **CELLE**-element ikke returnerer noen data ved kjøretid, viser dokumentet som genereres, bildeplassholderen fra malen. Hvis du vil skjule et bilde i dokumentet du genererer, definerer du et **CELLE**-element og angir at **Aktivering**-uttrykket skal returnere verdien **USANN**.
> - I Excel-malen bruker du et unikt navn for hvert element. Disse elementene inkluderer bilder og celler. Hvis du dupliserer et elementnavn, vil innholdet i rapporten som genereres, være tvetydig og forvirrende.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Bygge inn bilder i toppteksten og bunnteksten i et Excel-regneark

Bruk Excel-arbeidsbokdokumentet som en mal for å angi oppsettet av en rapport. Arbeidsboken kan inneholde flere regneark, og hvert regneark kan utformes slik at det har en topptekst og en bunntekst. Excel støtter opptil tre bilder i toppteksten og bunnteksten i hvert regneark. Bildene kan justeres til venstre, høyre eller i midten.

I Finance-utgivelse 10.0.21 kan du administrere topp- og bunntekstbilder som genereres av en ER-løsning som har en Excel-mal.

Hvis du vil at et standardbilde skal vises i toppteksten eller bunnteksten i et generert dokument, kan du legge til et bilde i toppteksten eller bunnteksten i et regneark i en ER-mal. Hvis du vil ha tilgang til dette bildet i ER-formatet, må du legge til **Bilde**-komponenten under [topptekst](er-fillable-excel.md#header-component) eller [bunntekst](er-fillable-excel.md#footer-component)-komponenten i formatet. Konfigurer justeringen av **bilde**-komponenten etter behov. 

Du kan også bruke **bilde**-komponenten til å legge et bilde i toppteksten eller bunnteksten til et generert dokument ved kjøretid, selv om malen ikke inneholder et standardbilde. Hvis du vil angi medieinnholdet som skal legges inn i toppteksten eller bunnteksten til et generert dokument, som et nytt bilde eller en erstatning for et standardbilde, må du knytte **bilde**-komponenten til en datakilde av [Container](er-formula-supported-data-types-composite.md#container)-typen som representerer et bilde i binært format.

Hver **topptekst**- eller **bunntekst**-komponent kan inneholde én **bilde**-komponent for hver justering som støttes: **Venstre**, **Senter** og **Høyre**.

Ved hjelp av **Skaler høyden**-egenskapen for **bilde**-komponenten kan du bruke den konfigurerte bindingen til å kontrollere størrelsen på et bilde:

- Velg **Original** for å beholde den opprinnelige størrelsen på bildet.
- Velg **Relativ** for å skalere høyden på bildet i forhold til høyden på toppteksten eller bunnteksten som inneholder bildet.

    - I dette tilfellet må høyden på bildet defineres som en prosentdel av den overordnede toppteksten eller bunnteksten.
    - Hvis skaleringsverdien overskrider 100 prosent, kan bildet overlappe dataområdet i det tilsvarende regnearket.
    - Hvis høyden på bildet endres når skaleringen brukes, endres også bredden for å vedlikeholde bildets opprinnelige aspektsgrad.

- Velg **Absolutt** for å endre størrelsen på bildet i henhold til høyde- og breddeverdiene (i piksler) som angis ved utformingstidsprogrammet.

    - Hvis den angitte høyden overskrider høyden til den overordnede toppteksten eller bunnteksten, kan bildet overlappe dataområdet i det tilsvarende regnearket.

Du kan også bruke egenskapen **Aktivert** for **bilde**-komponenten til å kontrollere synligheten til et bilde som settes inn i et generert dokument ved hjelp av denne komponenten.

> [!NOTE]
> Du må bruke ER-formatdesigneren for å legge til en **bilde**-komponent i det redigerbare ER-formatet. Du kan ikke legge til komponenten når du bruker arbeidsområdet [Behandling av forretningsdokument](er-business-document-management.md) til å redigere malen til et forretningsdokument.

Hvis du vil lære mer om denne funksjonaliteten, kan du følge trinnene i [Utforme et ER-format for å generere en rapport i Excel-format med innebygde bilder i topptekster eller bunntekster](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Bygge inn en figur i et Excel-dokument

Først må du legge til en plassholder for figuren i et Excel-dokument. Åpne en Excel-arbeidsbok og velg **Figur**, **Tekstboks** eller **WordArt** som en plassholder for figuren. Bruk deretter ER-verktøyet til å legge til en ny ER-formatkonfigurasjon for å ta med rapporten du utformer. Tilknytt Excel-arbeidsboken som en mal for rapportens format, og importer deretter innholdet i arbeidsboken til ER-formatet. Formatdefinisjonen opprettes automatisk. Plassholderen for figur som du la til, blir tatt med i ER-formatdefinisjonen som et **CELLE**-element som refererer til det navngitte Excel-figurelementet.

> [!NOTE]
> Du kan angi formatdefinisjonen manuelt i stedet for å importere den. Når du lagrer endringene, valideres formatet.

Deretter binder du **CELLE**-elementet i ER-formatet til feltet fra formatets datakilde som gir dataene ved kjøretid. Disse dataene kan konverteres til en tekststreng. Når **CELLE**-elementet i ER-formatet refererer til et figurelement i Excel-malen som støtter tekst, vil teksten som angis gjennom denne bindingen ved kjøretid, vises i en figur i dokumentet som genereres.

> [!IMPORTANT]
> - Hvis du vil bruke Excel-malen som inneholder plassholder for figur til å generere et nytt dokument, må ER-formatet inneholde et **CELLE**-element som refererer til Excel-figurelementet. Hvis ikke, vises det ingen plassholder for figur i rapportens utdata. Hvis bindingen til et **CELLE**-element som refererer til det navngitte Excel-figurelementet, ikke returnerer noen data ved kjøretid, viser dokumentet som genereres, teksten i plassholderen for figur fra Excel-malen. Hvis du vil skjule en figur i dokumentet du genererer, definerer du et **CELLE**-element som refererer til den navngitte Excel-figuren og angir at **Aktivering**-uttrykket skal returnere verdien **USANN**.
> - I Excel-malen bruker du et unikt navn for hvert element. Disse elementene inkluderer figurer og celler. Hvis du dupliserer et elementnavn, vil innholdet i rapporten som genereres, være tvetydig og forvirrende.

## <a name="embed-an-image-in-a-word-document"></a>Bygge inn et bilde i et Word-dokument
> [!IMPORTANT]
> Du kan bruke ER-formatet på nytt som bruker en Excel-mal til å opprette dokumenter som inneholder innebygde bilder. I ER-formatet må du kontrollere at det er angitt et navn for **CELLE**-elementet som refererer til et navngitt bildeelement i Excel, og som er bundet til en datakilde som returnerer et bilde ved kjøretid.

Først må du konfigurere Word-dokumentets oppsett. Bruk kontrollen for **bildeinnhold** til å opprette en plassholder for det innebygde bildet. Hvis du vil ha tilgang til denne kontrollen, må du først gjøre fanen **Utvikler** synlig i Word-båndet.

Deretter sletter du Excel-malen fra ER-formatet og knytter Word-maldokumentet til. Oppdater referansen til malen og lagre endringene. Strukturen til det gjeldende ER-formatet lagres til Word-malen som en ny, egendefinert XML-del med navnet **Rapport**.

Deretter lagrer du Word-malen for gjeldende ER-format til den lokale datamaskinen. Åpne malen, og åpne **XML-tilordning**-ruten. Finn den egendefinerte XML-delen som kalles **Rapport**, og pek deretter til **CELLE**-elementet i ER-rapporten som er knyttet til en datakilde som returnerer et bilde i binært format. Tilordne denne XML-delens element til den valgte **bildeinnhold**-kontrollen og lagre endringene.

[![bygge inn bilder.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Til slutt sletter du Word-malen fra ER-formatet, og knytter Word-dokumentet som inneholder de tilordnede egendefinerte XML-delene. Oppdater formatreferansen til malen, og lagre endringene du har gjort i dette ER-formatet.

## <a name="more-information"></a>Mer informasjon
Hvis du vil bli kjent med detaljene i denne funksjonen, kan du spille av settet med oppgaveveiledninger, **ER Lage rapporter i MS Office-formater med innebygde bilder**. Disse oppgavehåndbokene viser hvordan du kan bygge inn bildene av en firmalogo og en autorisert persons signatur i betalingssjekkene som genereres ved hjelp av ER-verktøyet i Excel- og Word-dokumenter.

Tabellen nedenfor viser filene som kreves for å fullføre oppgaveveiledningene **ER Lage rapporter i MS Office-formater med innebygde bilder**. Last ned og lagre filene på den lokale datamaskinen.

| beskrivelse                                          | Filnavn                   |
|------------------------------------------------------|-----------------------------|
| ER-datamodellkonfigurasjon                          | [Modell for sjekker.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER-formatkonfigurasjon                              | [Utskriftsformat for sjekker.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Firmalogobilde                                   | [Firmalogo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Signaturbilde                                      | [Signaturbilde.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternativt signaturbilde                          | [Signaturbilde 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word-mal for utskrift av betalingssjekker  | [Sjekkmal Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel-mal for utskrift av betalingssjekker | [Sjekkmal.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Grafikken nedenfor gir et eksempel på testutskriften for en betalingskontroll som genereres fra Excel-malen.

[![Testutskrift av betalingskontroll.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
