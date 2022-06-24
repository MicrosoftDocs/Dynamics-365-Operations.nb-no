---
title: Utforme ER-uttrykk for å kalle programklassemetoder
description: Denne artikkelen beskriver hvordan du bruker den eksisterende programlogikken i konfigurasjoner for elektronisk rapportering på nytt ved å kalle opp nødvendige metoder for programklasser.
author: NickSelin
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fb0a9725d882fdc330d7adbb49bd3dcadf7805f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883632"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Utforme ER-uttrykk for å kalle programklassemetoder

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker den eksisterende programlogikken i [elektronisk rapportering (ER)](../general-electronic-reporting.md)-konfigurasjoner på nytt ved å kalle nødvendige metoder for programklasser i ER-uttrykk. Verdier til argumenter for oppkallsklasser kan defineres dynamisk ved kjøretid. Verdier kan for eksempel være basert på informasjon i analysedokumentet for å sikre at det er riktig.

I denne artikkelen skal du for eksempel utforme en prosess som analyserer innkommende bankkontoutdrag for en oppdatering av programdata. Du mottar de innkommende bankkontoutdragene som tekstfiler (TXT) som inneholder IBAN-koder (internasjonalt bankkontonummer). Som en del av prosessen med å importer bankkontoutdrag må du validere riktigheten av IBAN-koden ved hjelp av logikken som allerede finnes.

## <a name="prerequisites"></a>Forutsetninger

Fremgangsmåtene i denne artikkelen er ment for brukere som har blitt tilordnet rollen som **Systemansvarlig** eller **Utvikler av elektronisk rapportering**.

Prosedyrene kan fullføres ved hjelp av et hvilket som helst datasett.

For å fullføre dem må du laste ned og lagre følgende fil lokalt: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

I denne artikkelen skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet Litware, Inc. Før du kan fullføre prosedyrene i denne artikkelen, må du derfor fullføre følgende trinn:

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner** må du bekreftet av konfigurasjonsleverandøren for eksempelfirmaet **Litware, Inc.** er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i [Opprett konfigurasjonsleverandører og merk dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Importere en ny ER-konfigurasjon

1. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjonsleverandører**, velger du flisen **Microsoft**-konfigurasjonsleverandøren.
2. Velg **Repositorier**.
3. På siden **Lokaliseringsrepositorier** velger du **Vis filtre**.
4. Hvis du vil velge oppføringen for Globalt repositorium, legger du til et **Navn**-filterfelt.
5. Angi **Global** i **Navn**-feltet. Deretter velger du filteroperatoren **inneholder**.
6. Velg **Bruk**.
7. Velg **[Åpne](../er-download-configurations-global-repo.md#open-configurations-repository)** for å gå gjennom listen over ER-konfigurasjoner i det valgte repositoriet.
8. På siden **Konfigurasjonsrepositorium**, i konfigurasjonstreet, velger du **Betalingsmodell**.
9. På hurtigfanen **Versjoner**, hvis **Importer**-knappen er tilgjengelig, velger du den og velger deretter **Ja**.

    Hvis **Importer**-knappen ikke er tilgjengelig, har du allerede importert den valgte versjonen av ER-konfigurasjonen **Betalingsmodell**.

10. Lukk siden **Konfigurasjonsrepositorium**, og lukk deretter siden **Lokaliseringsrepositorier**.

## <a name="add-a-new-er-format-configuration"></a>Legg til en ny ER-formatkonfigurasjon

Legg til et nytt ER-format for å analysere innkommende bankkontoutdrag i TXT-format.

1. På siden **Lokaliseringskonfigurasjoner** velger du flisen **Rapporteringskonfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, velger du **Betalingsmodell**.
3. Velg **Opprett konfigurasjon**. 
4. Følg disse trinnene i rullegardinboksen:

    1. I **Ny**-feltet angir du **Format basert på datamodell PaymentModel**.
    2. I **Navn**-feltet skriver du inn **Importformat for bankkontoutdrag (eksempel)**.
    3. Velg **Ja** i feltet **Støtter dataimport**.
    4. Velg **Opprett konfigurasjon** for å fullføre opprettingen av konfigurasjonen.

## <a name="design-the-er-format-configuration--format"></a>Utforme ER-formatkonfigurasjonen – format

Utform et ER-format som representerer den forventet strukturen for den eksterne filen i TXT-format.

1. Velg **Utforming** for formatkonfigurasjonen **Importformat for bankkontoutdrag (eksempel)** som du la til.
2. På siden **Formatutforming** i formatstrukturtreet i venstre rute velger du **Legg til rot**.
3. Følg denne fremgangsmåten i dialogboksen som vises:

    1. I treet velger du **Tekst\\Sekvens** for å legge til en **Sekvens**-formatkomponent.
    2. I **Navn**-feltet skriver du inn **Rot**.
    3. Velg **Ny linje - Windows (CR LF)** i **Spesialtegn**-feltet. Basert på denne innstillingen, blir hver linje i analysefilen betraktet som en egen oppføring.
    4. Velg **OK**.

4. Velg **Legg til**.
5. Følg denne fremgangsmåten i dialogboksen som vises:

    1. Velg **Tekst\\Sekvens** i treet.
    2. Angi **Rader** i **Navn**-feltet.
    3. Velg **Én mange** i feltet **Multiplisitet**. Basert på denne innstillingen, forventes det at minst én linje vises i analysefilen.
    4. Velg **OK**.

6. I treet velger du **Rot\\Rader**, og deretter velger du **Legg til sekvens**.
7. Følg denne fremgangsmåten i dialogboksen som vises:

    1. Angi **Felter** i **Navn**-feltet.
    2. Velg **Nøyaktig én** i feltet **Multiplisitet**.
    3. Velg **OK**.

8. I treet velger du **Rot\\Rader\\Felter**, og deretter velger du **Legg til**.
9. Følg denne fremgangsmåten i dialogboksen som vises:

    1. Velg **Tekst\\Streng** i treet.
    2. Angi **IBAN** i **Navn**-feltet.
    3. Velg **OK**.

10. Velg **Lagre**.

Konfigurasjonen er nå satt opp slik at hver linje i analysefilen inneholder kun IBAN-koden.

![Formatkonfigurasjonen Importformat for bankkontoutdrag (eksempel) på Formatutforming-siden.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>Utforme ER-formatkonfigurasjonen – tilordning til en datamodell

Utform en ER-formattilordning som bruker informasjon fra analysefilen til å fylle ut en datamodell.

1. På siden **Formatutforming** velger du **Tilordne format til modell** i handlingsruten.
2. På siden **Tilordning av modell til datakilde** velger du **Ny** i handlingsruten.
3. I **Definisjon**-feltet velger du **BankToCustomerDebitCreditNotificationInitiation**.
4. I feltet **Navn** angir du **Tilordning til datamodell**.
5. Velg **Lagre**.
6. Velg **Utforming**.
7. På siden **Modelltilordningsutforming**, i treet **Datakildetyper**, velger du **Dynamics 365 for Operations\\Klasse**.
8. I **Datakilder**-delen velger du **Legg til rot** for å legge til en datakilde som kaller den eksisterende applogikken for validering av IBAN-koder.
9. Følg denne fremgangsmåten i dialogboksen som vises:

    1. I **Navn**-feltet skriver du inn **Sjekk\_koder**.
    2. I **Klasse**-feltet angir eller velger du **ISO7064**.
    3. Velg **OK**.

10. Følg disse trinnene i treet **Datakildetyper**.

    1. Utvid **format**-datakilden.
    2. Utvid **format\\Rot: Sequence(Root)**.
    3. Utvid **format\\Rot: Sequence(Root)\\Rader: Sequence 1..\* (Rader)**.
    4. Utvid **format\\Rot: Sequence(Root)\\Rader: Sequence 1..\* (Rader)\\Felter: Sequence 1..1 (Fields)**.

11. Følg disse trinnene i treet **Datamodell**.

    1. Utvid **Betalinger**-feltet for datamodellen.
    2. Utvid **Betalinger\\Creditor Account(CreditorAccount)**.
    3. Utvid **Betalinger\\Creditor Account(CreditorAccount)\\Identifikasjon**.
    4. Utvid **Betalinger\\Creditor Account(CreditorAccount)\\Identifikasjon\\IBAN**.

12. Følg denne fremgangsmåten for å binde komponenter i det konfigurerte formatet til datamodellfelter:

    1. Velg **format\\Rot: Sequence(Root)\\Rader: Sequence 1..\* (Rader)**.
    2. Velg **Betalinger**.
    3. Velg **Bind**. Basert på denne innstillingen blir hver linje i analysefilen betraktet som en egen betaling.
    4. Velg **format\\Rot: Sequence(Root)\\Rader: Sequence 1..\* (Rader)\\Felter: Sequence 1..1 (Felter)\\IBAN: String(IBAN)**.
    5. Velg **Betalinger\\Creditor Account(CreditorAccount)\\Identifikasjon\\IBAN**.
    6. Velg **Bind**. Basert på denne innstillingen blir **IBAN**-feltet for datamodellen fylt ut med verdien fra analysefilen.

    ![Binding av formatkomponenter til datamodellfelter på siden Modelltilordningsutforming.](../media/design-expressions-app-class-er-02.png)

13. På **Valideringer**-fanen følger du disse trinnene for å legge til en [valideringsregel](../general-electronic-reporting-formula-designer.md#Validation) som viser en feilmelding for enhver linje i analysefilen som inneholder en ugyldig IBAN-kode:

    1. Velg **Ny**, og velg deretter **Rediger betingelse**.
    2. På siden **Formelutforming** i **Datakilde**-treet utvider du datakilden **Sjekk\_koder** som representerer appklassen **ISO7064**, for å vise de tilgjengelige metodene for denne klassen.
    3. Velg **Sjekk\_koder\\verifyMOD1271\_36**.
    4. Velg **Legg til datakilde**.
    5. I **Formel**-feltet angir du følgende [uttrykk](../general-electronic-reporting-formula-designer.md#Binding): **Sjekk\_koder.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**.
    6. Velg **Lagre**, og lukk deretter siden.
    7. Velg **Rediger melding**.
    8. På **Formeltutforming**-siden i **Formel**-feltet skriver du inn **CONCATENATE("Ugyldig IBAN-kode er funnet:&nbsp;", format.Root.Rows.Fields.IBAN)**.
    9. Velg **Lagre**, og lukk deretter siden.

    Basert på disse innstillingene vil valideringsbetingelsen returnere *[FALSE](../er-formula-supported-data-types-primitive.md#boolean)* for en ugyldig IBAN-kode ved å kalle opp den eksisterende **verifyMOD1271\_36**-metoden for appklassen **ISO7064**. Legg merke til at verdien til IBAN-koden defineres dynamisk under kjøring som argumentet for kallmetoden basert på innholdet i tekstfilen for analyse.

    ![Valideringsregel på siden Modelltilordningsutforming.](../media/design-expressions-app-class-er-03.png)

14. Velg **Lagre**.
15. Lukk siden **Modelltilordningsutforming**, og lukk deretter siden **Tilordning av modell til datakilde**.

## <a name="run-the-format-mapping"></a>Kjøre formattilordningen

For testformål kan du kjøre formattilordningen ved å bruke filen SampleIncomingMessage.txt som du lastet ned tidligere. De genererte utdataene omfatter informasjon som er importert fra den valgte tekstfilen, og som sendes til den egendefinerte datamodellen under den reelle importen.

1. Velg **Kjør** på siden **Tilordning av modell til datakilde**.
2. På siden **Parametere for elektronisk rapport** velger du **Bla gjennom**. Bla til filen **SampleIncomingMessage.txt** som du lastet ned, og velg den.
3. Velg **OK**.
4. Legg merke til at siden **Tilordning av modell til datakilde** viser en feilmelding om en ugyldig IBAN-kode.

    ![Resultat av kjøring av formattilordningen på siden Tilordning av modell til datakilde.](../media/design-expressions-app-class-er-04.png)

5. Gå gjennom utdataene i XML-format, som representerer dataene som er importert fra den valgte filen og overført til datamodellen. Legg merke til at bare tre linjer i den importerte tekstfilen ble behandlet uten feil. IBAN-koden på linje 4 er ikke gyldig og ble hoppet over.

    ![XML-utdata.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
