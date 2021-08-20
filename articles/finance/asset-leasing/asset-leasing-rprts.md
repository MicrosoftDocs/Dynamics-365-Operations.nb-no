---
title: Rapporter om aktivaleie
description: Dette emnet viser og gir en kort beskrivelse av rapportene som er tilgjengelige i Aktivaleie.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7044378a66ed9ff952f4579d375d59576fe09294fc158c000ab28a93f4173421
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739413"
---
# <a name="asset-leasing-reports"></a>Rapporter om aktivaleie

[!include [banner](../includes/banner.md)]

Dette emnet viser og gir en kort beskrivelse av rapportene som er tilgjengelige i Aktivaleie. Du viser de fleste rapportene ved å følge disse trinnene eller lignende trinn, som angitt. 

- Du viser de fleste rapportene om aktivaleie ved å gå til **Aktivaleie > Forespørsler og rapporter > Leierapporter** og deretter velge rapporten du vil vise. Når det gjelder rapportene som krever en annen valgbane, er fremgangsmåten for å åpne rapporten tatt med i beskrivelsen av denne rapporten. 
- Når du velger en rapport som skal skrives ut, åpnes en parameterside der du kan filtrere informasjon som tas med i rapporten. Angi filterkriterier, og velg deretter **OK** for å generere rapporten. Den genererte rapporten viser informasjon som faller innenfor filtrene du har angitt.

## <a name="asset-movement"></a>Flytting av aktiva
Rapporten for flytting av aktiva fungerer som en fremoverrullingsrapport for saldoene for bruksrettseiendel for hver leieavtale. Denne rapporten gjør at du kan vise aktivatransaksjonene for en leieavtale i løpet av en bestemt periode. Rapporten inneholder følgende felter. 

|     Rapportfelter                  |     Beskrivelse                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Startdato              |     Startdatoen for leieavtalens tidligste versjon.                     |   
|     Leietermin                     |     Leieperioden i leieavtalens tidligste versjon.                            |
|     Korttidsleie               |     Hvis leieavtalen er klassifisert som en avtale med korttidsleie, vises **Ja**.         |
|     Lavverdileie                |     Hvis leieavtalen er klassifisert som en avtale med lavverdileie, vises **Ja**.          |
|     Opprinnelig bruksrettseiendel     |     Den opprinnelige verdien til bruksrettseiendelen fra journaloppføringen for opprinnelig føring.      |
|     Startsaldo              |     Netto bokført verdi for bruksrettseiendel per **Fra dato**.                         |
|     Periodeavskrivningskostnad    |     Beløpet for avskrivningskostnad som er tatt innen datointervallet som er definert for rapporten.        |
|     Akkumulert avskrivning       |     Beløpet for akkumulert avskrivning per **Fra dato**.                               |
|     Verdiforringelse                     |     Verdiforringelsesbeløpet for aktivumet innen datointervallet som er definert for rapporten.               |
|     Endringer                  |     Mengden justeringer av bruksrettseiendelen mellom datoparametere.                            |
|     Netto bokført verdi                 |     Netto bokført sluttverdi for bruksrettseiendelen, som er netto av akkumulert avskrivning per **Til dato**.    |

## <a name="differences-report"></a>Avviksrapport
Rapporten om forskjeller viser forskjellene mellom informasjon som er lastet inn i rammeverket for import av leieavtale, og informasjon som finnes i systemet. Dermed kan du sammenligne det som er justert, oppdatert eller lagt til via rammeverket for import av leieavtale.  

Verdiene i rapporten varierer etter hvilken leieavtale som er valgt. Rapporten viser bare de feltene som er forskjellige fra det som er i systemet, og det som er i oppsamlingstabellene. Den gamle verdien er det som enten er i systemet, eller det som tidligere var i systemet, avhengig av om importprosessen er kjørt. Den nye verdien viser verdien i oppsamlingstabellen som vil erstatte den gamle verdien.

## <a name="five-years-undiscounted-payment-forecast"></a>Fem års ikke-rabattert betalingsprognose
Rapporten om fem års ikke-rabattert betalingsprognose viser de forventede ikke-rabatterte leiebetalingene som skal betales i løpet av de neste fem årene fra datoen som er angitt i rapportparameterne. Rapporten inneholder følgende felter. 

|     Rapportfelter         |     Beskrivelse                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Leiebeskrivelse     |     Leiebeskrivelsen fra leiehodet.                                                      |
|     Leie-ID              |     Den unike leie-ID-en.                                                                              |
|     Tablå                  |     Leietablået som er knyttet til tablå-ID-en.                                                         |
|     Klassifisering        |     Klassifiseringen av leieavtalen.                                                                  |
|     Posteringslag         |     Laget som denne leieavtalen skal posteres på.                                                         |
|     Valuta.              |     Valutaen for leieavtalen.                                                                        |
|     Gjeldende               |     Summen av alle leiebetalinger som skal betales i løpet av de neste 12 månedene fra rapporteringsdatoen.          |
|     13–24 måneder          |     Summen av alle leiebetalinger som skal betales mellom 13 og 24 måneder fra rapporteringsdatoen.           |
|     25–36 måneder          |     Summen av alle leiebetalinger som skal betales mellom 25 og 36 måneder fra rapporteringsdatoen.           |
|     37–48 måneder          |     Summen av alle leiebetalinger som skal betales mellom 37 og 48 måneder fra rapporteringsdatoen.           |
|     49–60 måneder          |     Summen av alle leiebetalinger som skal betales mellom 49 og 60 måneder fra rapporteringsdatoen.           |
|     Deretter            |     Summen av alle leiebetalinger som skal betales innen eller etter 61 måneder fra rapporteringsdatoen.              |

## <a name="gaap-cash-flows-report"></a>Rapport om GAAP-kontantstrømmer
Rapporten om GAAP-offentliggjøring oppfyller de amerikanske kravene til GAAP-offentliggjøring i 842-20-50-4(g)(1). Du kan vise denne rapporten ved å gå til **Aktivaleie > Forespørsler og rapporter > Informasjon > GAAP – kontantstrømmer**. 

|     Rapportfelter                                 |     Beskrivelse                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Fra dato <br> Til dato                        |     Definerer en rekke datoer som brukes til å begrense informasjonen som er inkludert i rapporten.      |
|     Juridisk enhet                                  |     Den juridiske enheten som er knyttet til leieavtalene.                                      |
|     Leietype                                    |     Klassifiseringen av leieavtalen som enten finansiell eller gjeldende.           |
|     Leie-ID                                      |     Den unike leie-ID-en.                                                      |
|     Leiebeskrivelse                             |     Leiebeskrivelsen fra leiehodet.                              |
|     Leietablå                                    |     Leietablået som linjen refererer til.                        |
|     Posteringslag                                 |     Hvert tablå som er knyttet til et anleggsmiddel, er definert for et bestemt posteringslag som inneholder det totale avskrivningsmålet.                          |
|     Leiegruppe                                   |     Gruppen som leieavtalen er knyttet til.                                     |
|     Valuta.                                      |     Forkortelsen for transaksjonsvalutaen som brukes. Alle rapporter vil konvertere transaksjonsvalutaen til rapporteringsvalutaen.                      |
|     Finansielle leieavtaler – gjeldende kontantstrømmer         |     Summen av alle posterte variable betalinger og alle rentebetalinger som er postert fra nedbetalingsplanen mellom datoparameterne.        |
|     Finansielle leieavtaler – finansielle kontantstrømmer           |     Summen av alle hovedbetalingene fra nedbetalingsplanen mellom datoparameterne.       |
|     Gjeldende leieavtaler – gjeldende kontantstrømmer       |     Summen av alle posterte leiebetalinger og posterte variable betalinger mellom datoparameterne.            |

## <a name="lease-balances-forecast"></a>Prognose for leiesaldoer
Leiesaldoprognosen viser informasjon direkte fra nedbetalingsplanen for gjeld og avskrivningsplanen for aktiva. Rapporten viser prognosebeløp for den forventede leieforpliktelsen og bruksrettseiendeler over en tidsperiode, inkludert alle forventede utgifter for disse leieavtalene. Rapporten inneholder følgende felter.

|     Rapportfelter                 |     Beskrivelse                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Startsaldo             |     Startsaldoen i leieavtalens nedbetalingsplan for perioden som inneholder startdatoen for rapporten.            |
|     Opprinnelig føring           |     Hvis startdatoen for leieavtalen er innenfor datointervallet som er definert for rapporten, viser denne kolonnen gjeldskontoverdien for journaloppføringen for opprinnelig føring.      |
|     Betalinger                      |     Summen av leieavtalens betalinger som er innenfor datointervallet som er definert for rapporten.                               |
|     Rente                      |     Summen av leieavtalens renteutgifter som er innenfor datointervallet som er definert for rapporten.                    |
|     Sluttsaldo                |     Gjeldssaldoen for leieavtalen per **Til dato**.                                                             |
|     Kortsiktig gjeld          |     Det kortsiktige gjeldsbeløpet i leieavtalens nedbetalingsplan per **Til dato**.                           |
|     Langsiktig gjeld           |     Det langsiktige gjeldsbeløpet i leieavtalens nedbetalingsplan per **Til dato**.                            |
|     Innledende netto bokført verdi      |     Innledende netto bokført verdi i leieavtalens avskrivningsplan for aktiva for perioden som inneholder startdatoen for rapporten.      |
|     Opprinnelig føring           |     Hvis startdatoen for leieavtalen er mellom rapportens datoparametere, viser denne kolonnen aktivakontoverdien for journaloppføringen for opprinnelig føring.            |
|     Avskrivningskostnad          |     Summen av leieavtalens avskrivningsutgifter som er innenfor datointervallet som er definert for rapporten.                  |
|     Sluttsaldo                |     Aktivasaldoen per leieavtalen per **Til dato**.                                                              |
|     Justering av egenkapital             |     Startsaldoen minus innledende netto bokført verdi.                                                             |

## <a name="lease-commencements-report"></a>Rapport om leieavtalestart
Rapporten om leieavtalestart viser alle leieavtaler som har startet innen et bestemt datointervall, inkludert saldoene for opprinnelig gjeld og bruksrettseiendel. Rapporten inneholder følgende felter. 

|     Rapportfelter                 |     Beskrivelse                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Startdato             |     Datoen for journaloppføringen for opprinnelig føring som ble postert for denne leieavtaleversjonen.         |
|     Opprinnelig gjeldsbeløp      |     Gjeldsbeløpet fra journaloppføringen for opprinnelig føring.                                  |
|     Opprinnelig aktivabeløp          |     Aktivabeløpet fra journaloppføringen for opprinnelig føring.                                      |

## <a name="lease-modification-report"></a>Rapport om leieavtaleendring
Rapporten om leieavtaleendring viser alle leieavtaler som er endret i et angitt datointervall. Rapporten viser også brukeren som justerte leieavtalen, og det totale gjeldsbeløpet som er justert. Rapporten inneholder følgende felter. 

|     Rapportfelter                 |     Beskrivelse           |
|---------------------------------  |-------------------------  |
|     Justert av                   |     Brukernavnet til personen som endret leieavtalen.                                |
|     Justeringsdato               |     Datoen journaloppføringen for justering ble postert.                        |
|     Justeringer                   |     Beløpet for enhver journaloppføring for justering som posteres i leieavtalens gjeldskonto mellom datoparameterne. Krediter vises som positive, mens debeter er negative.       |
|     Fortjeneste-/tapsbeløp            |     Beløpet for enhver journaloppføring for justering som posteres i leieavtalens fortjeneste-/tapskonto mellom datoparameterne. Krediter vises som positive, mens debeter er negative.       |
|     Tilbakeholdt overskudd             |     Beløpet for enhver journaloppføring for justering som posteres i leieavtalens tilbakeholdte overskudd mellom datoparameterne.      |
|     Saldo for avsluttende gjeld      |     Den resulterende gjeldssaldoen per justeringsdatoen for leieavtalen.           |

## <a name="lease-movement-report"></a>Rapport om leiebevegelse
Rapporten leiebevegelse fungerer som en fremoverrullingsrapport for leieforpliktelsessaldoene for hver leieavtale. Denne rapporten gjør at brukeren kan vise leieforpliktelsestransaksjonene for en leieavtale i løpet av en bestemt periode.

|     Rapportfelter             |     Beskrivelse                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Startdato         |     Startdatoen for leieavtalens tidligste versjon.    |
|     Leietermin                |     Leieperioden i leieavtalens tidligste versjon.           |
|     Gjenstående betalinger        |     Antall betalinger som ennå ikke er postert for leieavtalen.                       |
|     Startsaldo         |     Summen av alle transaksjoner som påvirker leieavtalens gjeld som forekom før rapportens startdato.             |
|     Opprinnelig føring       |     Beløpet i eventuell opprinnelig føringstransaksjon for leieavtalen som ble postert innen datointervallet som er definert for rapporten.     |
|     Betalinger                  |     Summen av leieavtalens betalingstransaksjoner som er postert innenfor datointervallet som er definert for rapporten. Verdiene i denne kolonnen vises som negative beløp etter hvert som betalingene reduserer leieavtalens gjeldssaldo.  |
|     Rente                  |     Summen av renteavsetningene som er postert mot leien innenfor datointervallet som er definert for rapporten.            |
|     Justeringer               |     Summen av leieavtalens posterte justeringstransaksjoner innenfor datointervallet som er definert for rapporten.                               |
|     Sluttsaldo            |     Saldoen for alle gjeldstransaksjonene for leieavtalen som er postert per **Til dato** for rapporten.                  |

## <a name="lease-transactions-report"></a>Rapport om leietransaksjoner
Forespørselen om leietransaksjoner viser alle journaloppføringene som er generert av Aktivaleie. Hver journaloppføring er koblet til tablå-ID-en den stammer fra. Dette gjør det enkelt å knytte journaloppføringen til den tilknyttede leieavtalen. Forespørselen om leietransaksjoner fungerer på en måte som ligner på siden **Bilagstransaksjoner** i Økonomimodul.

## <a name="weighted-average-discount-rate-report"></a>Rapport om avveid gjennomsnitt for rabattsats
Rapporten om avveid gjennomsnitt for rabattsats oppfyller de amerikanske kravene til GAAP-offentliggjøring i ASC 842-20-50-4(g)(4) for et avveid gjennomsnitt for rabattsats. Du kan vise denne rapporten ved å gå til **Aktivaleie > Forespørsler og rapporter > Informasjon > Avveid gjennomsnitt for rabattsats**. Rapporten inneholder følgende felter. 

|     Rapportfelter                     |     Beskrivelse                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Per dato                        |     Denne rapporten omfatter alle leieavtaler som har startet på eller før datoparameteren **Per**. Denne rapporten skal kjøres per siste dag i perioden som skal offentliggjøres.      |
|     Juridisk enhet                      |     Den juridiske enheten som er knyttet til leieavtalen.                           |
|     Leie-ID                          |     Den unike leie-ID-en.                                                  |
|     Leiebeskrivelse                 |     Leiebeskrivelsen fra leiehodet.                          |
|     Bestill                              |     Den bestemte tablåtypen for leieavtalen som vises.                                                                                                                                            |
|     Posteringslag                     |     Hvert tablå som er knyttet til et anleggsmiddel, er definert for et bestemt posteringslag som inneholder det totale avskrivningsmålet.      |
|     Leiegruppe                       |     Gruppen som leieavtalen tilhører.                                 |
|     Rabattsats                     |     Satsen som brukes til å rabattere leiebetalinger.                             |
|     Valuta.                          |     Forkortelsen for transaksjonsvalutaen som brukes. Alle rapporter vil konvertere transaksjonsvalutaen til rapporteringsvalutaen.  |
|     Gjenstående leiebetalinger          |     Totalbeløpet med ubetalte leiebetalinger fra betalingsplanen som gjenstår fra **Per**-datoen.            |
|     Gjenstående avveide betalinger       |     Leiebetalingene som gjenstår, multiplisert med rabattsatsen som brukes.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
