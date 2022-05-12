---
title: Power BI-innhold for abonnementsfakturering
description: Dette emnet beskriver hva som er inkludert i Microsoft Power BI-innholdet for abonnementsfakturering.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: fad96bdaf60e7772e9ea1ff937435b0274303505
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645423"
---
# <a name="subscription-billing-power-bi-content"></a>Power BI-innhold for abonnementsfakturering

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hva som er inkludert i Microsoft Power BI-innholdet for abonnementsfakturering. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet. 

## <a name="overview"></a>Oversikt

Power BI-innholdet for abonnementsfakturering ble opprettet for abonnementsfaktureringsassistenter og -ledere. Det inneholder viktige abonnementsfaktureringsmåledata, for eksempel månedlig gjentakende omsetning (MRR) for faktureringsplaner, og den fallende saldoen og vannfallsinformasjonen for utsettelsesplaner. Den bruker data fra faktureringsplaner og utsatte planer for å gi en oversikt over gjentakende inntekter og omsetning.

Power BI-innholdet har følgende tre faner, som inneholder totalt fire analytiske rapporter: 

- **Analyse – MRR** – Denne fanen inneholder rapporten om **månedlig gjentakende fakturering** og rapporten om **Fakturaplandetaljer**.
- **Analyse – vannfall** – Denne fanen inneholder rapporten om **Inntektsvannfall**.
- **Analyse – fallende saldo** – Denne fanen inneholder rapporten **Fallende saldo**.

## <a name="view-data-on-the-analytical-reports"></a>Vis data i analyserapportene

Før du kan vise data i analyserapportene, må du kjøre en periodisk prosess som genererer rapporteringsdataene for hver rapport. Disse dataene som rapportene krever, må genereres fordi de ikke lagres direkte i databasen. 

1. Gå til **Abonnementsfakturering \> Regelmessig kontraktfakturering \> Periodiske oppgaver \> Satsvis behandling av MRR-analyserapport**, og følg denne fremgangsmåten:

    1. Angi et datointervall på ikke mer enn tre år.
    2. Valgfritt: Definer en gjentakende satsvis prosessjobb for å oppdatere dataene periodisk.
    3. Velg **OK**.

2. Når kjøringen av den satsvise jobben er fullført, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetsbutikk** og oppdater mengdemålingen for **MRR-rapporten**. 
3. Gå til **Abonnementsfakturering \> Inntekts- og utgiftsutsettelser \> Periodiske oppgaver \> Satsvis behandling av vannfallsanalyserapport**, og følg denne fremgangsmåten:

    1. Angi en startdato og en sluttdato som ikke strekker seg over mer enn 26 perioder. 
    2. Hvis du vil vise prognoser for beløp i tidligere perioder i gjeldende periode, setter du alternativet **Forutse tidligere beløp i nåværende periode** til **Ja**.
    3. Valgfritt: Definer en gjentakende satsvis prosessjobb for å oppdatere dataene periodisk.
    4. Velg **OK**. 

4. Når kjøringen av den satsvise jobben er fullført, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetsbutikk** og oppdater mengdemålingen for **vannfallsrapporten**.
5. Gå til **Abonnementsfakturering \> Inntekts- og utgiftsutsettelser \> Periodiske oppgaver \> Satsvis behandling av fallende saldoanalyserapport**, og følg denne fremgangsmåten:

    1. Angi en startdato og en sluttdato som ikke strekker seg over mer enn 26 perioder. 
    2. Hvis du vil vise prognoser for beløp i tidligere perioder i gjeldende periode, setter du alternativet **Forutse tidligere beløp i nåværende periode** til **Ja**.
    3. Valgfritt: Definer en gjentakende satsvis prosessjobb for å oppdatere dataene periodisk.
    4. Velg **OK**.

6. Når kjøringen av den satsvise jobben er fullført, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetsbutikk** og oppdater mengdemålingen for **fallende saldorapport**.

## <a name="accessing-the-power-bi-content"></a>Tilgang til Power BI-innholdet

Power BI-innholdet for abonnementsfakturering vises i arbeidsområdet for **abonnementsfakturering**.
