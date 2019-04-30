---
title: Fakturasamsvar for leverandører
description: Fakturasamsvar for leverandører er prosessen med å sjekke samsvar mellom leverandørfakturaen, bestillingen og produktkvitteringsinformasjonen.
author: abruer
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a1f7e16064a954bb22dc233a77bf28747f7f11
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/25/2019
ms.locfileid: "896954"
---
# <a name="accounts-payable-invoice-matching"></a>Fakturasamsvar for leverandører

[!include [banner](../includes/banner.md)]

Fakturasamsvar for leverandører er prosessen med å sjekke samsvar mellom leverandørfakturaen, bestillingen og produktkvitteringsinformasjonen.

Ved dokumentsamsvar kalles forskjeller mellom disse dokumentene samsvarende avvik. Samsvarende avvik blir sammenlignet med toleransen som er angitt. Hvis et samsvarsavvik er større enn toleranseprosenten eller -beløpet, vises ikoner for samsvarsavvik på siden Leverandørfaktura og på siden Fakturahistorikk og samsvarende detaljer. 

Du legger for eksempel inn en bestilling med én varelinje på 1 000 batterier til en pris av 1,00 per stykk. Bestillingen blir godkjent og sendt til leverandøren. Leverandøren sender 1 000 batterier, og du legger inn en produktkvittering på 1 000 batterier til en pris på 1,00 per stykk. Lagerkostnaden for batteriene blir oppdatert med denne prisen. 

Det ankommer en faktura med på 1 000 batterier til en pris av 1,10 per stykk. Policyen for den juridiske enheten din tillatter en 5 prosents nettopristoleranse for denne varekategorien. En pris på 1,05 ville vært akseptabelt, men 1,10 er det ikke. Når du legger inn fakturainformasjon, identifiseres et avvik i prissamsvaret, og du kan lagre fakturaen til avviket er løst.

Du kan bruke følgende typer fakturasamsvar for leverandører:

-   Samsvar av fakturatotaler – Tilpass det totale beløpet på fakturaen til det totale beløpet i bestillingen. Denne typen fakturakontroll inneholder færrest detaljer slik at du kan bruke dette alternativet til å definere kontroller som begrenser tiden det tar for staben å se gjennom informasjon om fakturakontroll.
-   Toveis samsvar – Sammenligner prisinformasjonen på fakturaen med prisinformasjonen på bestillingen.
-   Treveis samsvar – Sammenligner prisinformasjonen på fakturaen med prisinformasjonen på bestillingen. Sammenlign også antallsinformasjonen på fakturaen med antallsinformasjonen på produktkvitteringene som er valgt for fakturaen.
-   Samsvar av tillegg – Sammenlign tilleggsinformasjonen (beløp) på fakturaen med tilleggsinformasjonen (beløp) på bestillingen.

> [!NOTE]
> Andre typer fakturavalidering kan fullføres ved hjelp av leverandørfakturapolicyer. 

Toveis samsvar og treveis samsvar sammenligner alltid prisinformasjon med enhetsprisen. Du kan også konfigurere disse samsvarspolicyene for å sammenligne prisinformasjon med pristotalen.
-   Nettoenhetspriskontroll – Sammenlign prisinformasjon for toveis samsvar eller treveis samsvar ved å sammenligne netto enhetspris for hver linje på fakturaen med tilhørende netto enhetspris i bestillingen. Netto enhetspris fastsettes med følgende formel: nettobeløpet for linjen / antallet for linjen.
-   Pristotalkontroll – Sammenlign prisinformasjon for toveis samsvar eller treveis samsvar ved å sammenligne nettobeløpet (pristotal) for hver linje på fakturaen med tilhørende nettobeløp på bestillingen. Nettobeløpet fastsettes med følgende formel: *(Enhetspris \* Linjeantall) + Linjetillegg - Linjerabatter*. Når samlet pris tilpasses til prosent, sammenligner systemet verdier ved hjelp av transaksjonsvalutaen. Når samlet pris tilpasses til beløp, sammenligner systemet verdiene ved hjelp av regnskapsvalutaen.

Fakturakontrollberegninger utføres vanligvis automatisk når du redigerer leverandørfakturaer på siden Leverandørfaktura. Du kan også utføre fakturakontroll ved forespørsel, etter behov. Fakturakontroll ved behov kontrolleres for den juridiske enheten av Oppdater fakturahodestatus automatisk på siden Leverandørparametere på Fakturavalidering-fanen. Fakturakontroll kan også utføres som en del av en fakturavurderingsprosess. Du kan vise resultatene av fakturakontroll på Leverandørfaktura-siden og relaterte fakturakontrollsider.

## <a name="invoice-totals-matching"></a> Samsvar av fakturatotaler
Du kan bruke kontroll av fakturatotaler som hjelp for å sørge for at totale fakturabeløp ikke avviker fra forventede beløp med mer enn et godkjent avvik. Seks totaler sammenlignes på Samsvar av fakturatotaler-detaljsiden, som vist i følgende tabell. Hvis den tillatte toleransen for samsvar av fakturatotaler er 20 %, betraktes 100 %-avviksprosenten for det totale rabattbeløpet som et samsvarsavvik.

| Total-feltet    | Faktisk fakturatotal | Forventet fakturatotal | Avvikprosent | Samsvarsstatus |
|----------------|----------------------|------------------------|---------------------|--------------|
| Saldo        | 495,00               | 495,00                 | 0 %                  | Sendt       |
| Sluttrabatt | 0,00                 | 9,90                   | 100 %                | Mislykket       |
| Gebyrer        | 64,90                | 64,90                  | 0 %                  | Sendt       |
| Merverdiavgift      | 139,98               | 137,50                 | 2 %                  | Sendt       |
| Avrund      | 0,00                 | 0,00                   | 0 %                  | Sendt       |
| Fakturabeløp | 699,88               | 687,50                 | 2 %                  | Sendt       |

Samsvar av fakturatotaler kontrolleres for den juridiske enheten av Samsvar fakturatotaler (på/av) på siden Leverandørparametere. Samsvar utføres på de forventede fakturatotalene og de faktiske fakturatotalene. De forventede fakturatotaler beregnes basert på prisene, tilleggene og informasjon om merverdiavgift fra bestillingen og antallet på fakturaen.

## <a name="two-way-price-totals-matching"></a> Toveis, samsvar av pristotal
Bruk toveis samsvar for å sikre at avviket mellom prisinformasjon på bestillingen og fakturaen er innenfor de akseptable avvikene. Du kan sammenligne prisinformasjon for nettobeløpet for hver linje på fakturaen, og alle ventende og tidligere posterte fakturalinjer, med nettobeløpet for den tilhørende bestillingslinjen. Dette kalles samsvar av pristotal. 

Samsvar av pristotaler kan baseres på en prosent, et beløp eller en prosent og et beløp. 

Hvis en toleranseprosent for total innkjøpspris er angitt, sammenlignes fem felt, som vist i følgende tabell. Fordi toleranseprosent for total innkjøpspris er 10 %, representerer avviksprosenten for pristotalen på 50 % et samsvarsavvik.

| Samsvarsstatus | Nettobeløp på faktura | Forventet nettobeløp | Total innkjøpspris uten samsvar (avviksbeløp) | Total innkjøpsprisprosent uten samsvar (avviksprosent) | Toleranseprosent for total innkjøpspris |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Sendt       | 105,00             | 100,00              | 5,00                                             | 5 %                                                              | 10 %                                    |
| Mislykket       | 150,00             | 100,00              | 50,00                                            | 50 %                                                             | 10 %                                    |

Hvis et toleransebeløp for kjøpspristotal er angitt, sammenlignes fem felt, som vist i følgende tabell. Fordi toleransebeløpet for total innkjøpspris er 100,00, representerer avviksbeløpet for pristotalen på 105,00 et samsvarsavvik.

| Samsvarsstatus | Nettobeløp på faktura | Forventet nettobeløp | Total innkjøpspris uten samsvar (avviksbeløp) | Total innkjøpspris i regnskapsvaluta uten samsvar (avviksbeløp) | Toleranse for total innkjøpspris |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Sendt       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Mislykket       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Hvis samsvar for pristotaler er definert med en prosenttoleranse og et toleransebeløp, noen ganger kalt et Må ikke overstige-beløp, vurderes begge toleranser når det evalueres om en linje har samsvarsavvik. Hvis enten prosenten eller beløpet er større enn toleransen, som vist i linjene 150,00 og 205,00 i tabellen nedenfor, har linjen et samsvarsavvik.

| Samsvarsstatus | Nettobeløp på faktura | Forventet nettobeløp | Total innkjøpsprisprosent uten samsvar (avviksprosent) | Toleranseprosent for total innkjøpspris | Total innkjøpspris i regnskapsvaluta uten samsvar (avviksbeløp) | Toleranse for total innkjøpspris |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Sendt       | 105,00             | 100,00              | 5 %                                                              | 10 %                                    | 5,00                                                                    | 100,00                         |
| Mislykket       | 150,00             | 100,00              | 50 %                                                             | 10 %                                    | 50,00                                                                   | 100,00                         |
| Mislykket       | 205,00             | 100,00              | 105 %                                                            | 10 %                                    | 105,00                                                                  | 100,00                         |

Toveis samsvar kontrolleres for den juridiske enheten av feltet Linjekontrollpolicy på siden Leverandørparametere. Avhengig av valget i feltet Tillat overstyring av kontrollpolicy kan du velge toveis samsvar for en bestemt leverandør, vare eller kombinasjon av vare og leverandør på siden Kontrollpolicy, og for en bestemt bestilling på siden Bestilling.

Pristotalkontroll utføres for den juridiske enheten av feltet Tilpass samlet pris på siden Leverandørparametere. Toleranseprosenten og -beløpet for total innkjøpspris (må-ikke-overskride-beløp) er også angitt på denne siden.

## <a name="two-way-net-unit-price-matching"></a> Toveis nettoenhetspriskontroll
Bruk toveis samsvar for å sikre at avviket mellom prisinformasjon på bestillingen og fakturaen er innenfor de akseptable avvikene. Du kan sammenligne prisinformasjon for nettoenhetsprisen for hver vare på fakturaen. Dette kalles nettoenhetspriskontroll. 

Ni linjebeløp sammenlignes på Fakturakontrolldetaljer-siden, som vist i følgende tabell. Hvis den tillatte pristoleransen for nettoenhetspriskontroll er 10 %, betraktes 22,61 %-avviket for nettoenhetsprisen som et samsvarsavvik.

| Linje-felt                    | Fakturaverdi | Bestillingsverdi | Avvikprosent | Samsvarsstatus |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Enhetspris                    | 55,40         | 55,38                | 0 %                  | Sendt       |
| Prisenhet                    | 1,00          | 1,00                 | 0 %                  | Sendt       |
| Innkjøpstillegg          | 50,00         | 0,00                 | 100 %                | Mislykket       |
| Rabatt                      | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Rabattprosent              | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Samkjøpsrabatt            | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Samkjøpsrabatt i prosent | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Nettobeløp                    | 271,60        | 221,52               | 22,61 %              | Mislykket       |
| Nettoenhetspris                | 67,9000       | 55,3800              | 22,61 %              | Mislykket       |

Toveis samsvar kontrolleres for den juridiske enheten av feltet Linjekontrollpolicy på siden Leverandørparametere. Avhengig av valget i feltet Tillat overstyring av kontrollpolicy kan du velge toveis samsvar for en bestemt leverandør, vare eller kombinasjon av vare og leverandør på siden Kontrollpolicy, og for en bestemt bestilling på siden Bestilling. 

Nettoenhetspriskontroll utføres for den juridiske enheten av feltet Aktiver validering av fakturakontroll på siden Leverandørparametere. Toleranseprosenter for netto enhetspris kan konfigureres for varer, varegrupper, leverandører, leverandørgrupper, kombinasjoner av varer og leverandører eller juridisk enhet ved hjelp av siden Pristoleranser.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> Toveis pristotalkontroll og nettoenhetspriskontroll
Du kan bruke pristotalkontroll og nettoenhetspriskontroll sammen. Dette eksemplet antar følgende konfigurasjon:

-   Netto enhetspristoleranse for USB-enhetsvaren er 10 %.
-   Toleransen for pristotalkontroll for den juridiske enheten er 15 % eller 500,00.

Bestillingen inneholder følgende linje.

| Varenummer | Antall | Enhetspris | Nettobeløp |
|-------------|----------|------------|------------|
| USB-enhet   | 1 000    | 10,00      | 10 000,00  |

Tre fakturaer registreres, som vist i følgende tabell. Det finnes et fakturasamsvarsavvik for faktura 3 fordi avviket på 1 880,00 er større enn toleransebeløpet for total innkjøpspris på 500,00. For samsvar av pristotal inkluderer fakturaens nettobeløp alle tidligere posterte fakturaer i tillegg til fakturaen du arbeider med for øyeblikket.

| Varenummer          | Antall | Enhetspris | Nettobeløp | Prissamsvar | Pristotalsamsvar |
|----------------------|----------|------------|------------|-------------|-------------------|
| Faktura 1: USB-enhet | 800      | 10,80      | 8 640,00   | Sendt      | Sendt            |
| Faktura 2: USB-enhet | 100      | 10,80      | 1 080,00   | Sendt      | Sendt            |
| Faktura 3: USB-enhet | 200      | 10,80      | 2 160,00   | Sendt      | Mislykket            |
| Sum                |          |            | 11 880,00  |             |                   |

## <a name="three-way-matching"></a>Treveis samsvar

Bruk treveis samsvar for å sikre at avviket mellom prisinformasjonen på bestillingen og fakturaen er innenfor de akseptable avvikene, og for å kontrollere at antallet på fakturaen samsvarer med antallet på de tilsvarende produktkvitteringene.

De samme linjebeløpene sammenlignes på Fakturakontrolldetaljer-siden som for toveis samsvar. I tillegg kontrolleres antallet på fakturaen med produktkvitteringsantallet som er mottatt. Hvis fakturaantallet er forskjellig fra det samsvarte produktkvitteringsantallet, finnes det en feil i antallssamsvar.

| Linje-felt                    | Fakturaverdi | Bestillingsverdi | Avvikprosent | Samsvarsstatus |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Enhetspris                    | 55,40         | 55,38                | 0 %                  | Sendt       |
| Prisenhet                    | 1,00          | 1,00                 | 0 %                  | Sendt       |
| Innkjøpstillegg          | 50,00         | 0,00                 | 100 %                | Mislykket       |
| Rabatt                      | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Rabattprosent              | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Samkjøpsrabatt            | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Samkjøpsrabatt i prosent | 0,00          | 0,00                 | 0 %                  | Sendt       |
| Nettobeløp                    | 271,60        | 221,52               | 22,61 %              | Mislykket       |
| Nettoenhetspris                | 67,9000       | 55,3800              | 22,61 %              | Mislykket       |

| Linje-felt                     | Fakturaverdi | Samsvarsstatus |
|--------------------------------|---------------|--------------|
| Fakturaantall               | 4,00          |              |
| Totalt produktkvitteringer samsvart | 0,00          | Mislykket       |

Treveis samsvar kontrolleres for den juridiske enheten av feltet Linjekontrollpolicy på siden Leverandørparametere. Avhengig av valget i feltet Tillat overstyring av kontrollpolicy kan du velge treveis samsvar for en bestemt leverandør, vare eller kombinasjon av vare og leverandør på siden Kontrollpolicy, og for en bestemt bestilling på siden Bestilling.

## <a name="charges-matching"></a> Samsvar av tillegg
Du kan bruke samsvar av tillegg som hjelp for å sørge for at tilleggsbeløp ikke avviker fra forventede beløp med mer enn en godkjent avviksprosent. Totalbeløpene for hver tilleggskode som gjelder for fakturaen og bestillingen, sammenlignes på siden Sammenlign verdier for tillegg - Faktura: som vist i følgende tabell. Hvis den tillatte toleransen for tilleggskoden er 25 %, betraktes 99999999999,99 %-avviksprosenten for lisenstilleggskoden som et samsvarsavvik.

> [!NOTE] 
> En avviksprosent på 99999999999,99 % betyr at det forventede beløpet basert på bestillingen er null, og det faktiske beløpet på fakturaen er en positiv verdi. 

| Status for tilleggssamsvar | Fakturagebyrkode | Faktisk total beregnet verdi | Forventet total beregnet verdi | Avvikbeløp | Avvikprosent | Toleranseprosent |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Mislykket               | Førerkort              | 25                            | 0                               | 25              | 99999999999,99 %  | 25 %                  |
| Sendt               | Frakt              | 200                           | 200                             | 0               | 0 %                  | 25 %                  |
| Mislykket               | Ekspeder             | 4                             | 2                               | 2               | 100 %                | 25 %                  |

Tilleggssamsvar kontrolleres for den juridiske enheten av Samsvar tillegg (på/av) på siden Leverandørparametere. Du kan definere avvikstoleranseprosenter for tillegg på siden Toleranser for tillegg.

> [!NOTE]
> Samsvar av tillegg utføres bare på tilleggskoder der Sammenlign bestillings- og fakturaverdi (på/av) velges på siden Tilleggskode.

## <a name="related-functionality"></a> Relatert funksjonalitet
Leverandørfakturaer er ofte basert på produktkvitteringer som representerer faktiske forsendelser, i stedet for på bestillinger. Noen ganger er det ikke samsvar mellom de fakturerte beløpene og beløpene på bestillingene, og noen ganger stemmer ikke det sendte antallet med det fakturerte antallet. Du kan behandle denne informasjonen på følgende måter:
-   Opprett en leverandørfaktura basert på produktkvitteringer. Produktkvitteringer blir automatisk foreslått for fakturaer, og du kan velge hvilke produktkvitteringer du vil bruke. Du kan også om nødvendig velge bestemte produktkvitteringslinjeelementer fra flere bestillinger.
-   Vise og godkjenne forskjeller i antall mellom det fakturerte antallet på fakturaen og det mottatte antallet på produktkvitteringen. Hvis det er forskjell, kan du lagre fakturaen og senere sammenligne den med en annen produktkvittering, eller endre det fakturerte antallet slik at det stemmer med det mottatte antallet.
-   Legge inn fakturabeløp som ikke ble tatt med i den opprinnelige bestillingen, slik at fakturainformasjonen samsvarer med fakturaen du har mottatt fra leverandøren. Du kan sammenligne tilleggene for bestillingene med tilleggene for fakturaene. Om nødvendig kan du legge til tillegg på fakturaer og tilordne dem til fakturalinjer.
-   Vise og godkjenne avvik i prissamsvar mellom netto enhetspris i fakturaen og netto enhetspris i bestillingen. Du kan definere pristoleranseprosenter for juridiske enheter, leverandører og varer. Hvis prisen i leverandørfakturalinjen ikke er innenfor den tillatte pristoleransen, kan du lagre fakturaen til den blir godkjent for postering, eller til du mottar en rettelse fra leverandøren.

Hvis du vil ha mer informasjon, se [Treveis kontrollpolicyer](three-way-matching-policies.md) og [Definere leverandørfakturakontroll for leverandører](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




