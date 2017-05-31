---
title: "Tilbakeføre en leverandørbetaling"
description: "Denne artikkelen beskriver forskjellene mellom tilbakeføring, sletting, annullering og avvisning av en betaling. Den beskriver også de to metodene for å tilbakeføre en sjekk for leverandør."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4f8b77efabe0c002654dac0b80d721a79dc42003
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="reverse-a-vendor-payment"></a>Tilbakeføre en leverandørbetaling

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver forskjellene mellom tilbakeføring, sletting, annullering og avvisning av en betaling. Den beskriver også de to metodene for å tilbakeføre en sjekk for leverandør. 

Noen ganger når en leverandørbetaling er postert, må betalingen tilbakeføres. Tilbakeføring er forskjellig fra sletting, annullering eller avvisning av en betaling. Du kan bare slette en betaling hvis statusen er **Opprettet**. Denne statusen angir at betalingen er opprettet, men ennå ikke har blitt generert. Denne begrensningen gjelder alltid, uavhengig av valgt betalingsmåte. Du kan annullere ikke-posterte sjekker etter at de har blitt generert, men før de er bokført. Hvis den genererte betalingen utføres som en elektronisk pengeoverføring (EFT), kan du avvise betalingen før den posteres. Hvis du vil avvise en betaling, kan du endre **Betalingsstatus**-verdien. En betaling som er annullert eller avvist, kan genereres på nytt etter **Betalingsstatus**-verdien er endret tilbake til **Ingen**. 

Når en betaling er postert, brukes tilbakeføringer. Betalinger som gjøres elektronisk, kan ikke tilbakeføres etter at de er postert. I stedet må det opprettes en ny transaksjon for betalingsbeløpet for å få gjelden tilbake på leverandørens konto. Det finnes to metoder for å tilbakeføre posterte sjekker. I én metode posteres tilbakeføringer umiddelbart når du klikker **Betalingsannullering** på **Sjekk**-siden. I den andre metoden kan du klikke **Betalingsannullering** på **Sjekk**-siden, så sendes tilbakeføringen til journalen for banksjekkannullering i bankstyringen, der en kontrollør kan postere eller avvise tilbakeføringen. 

Hvis du vil vite hvilken metode organisasjonen din bruker, ser du siden **Parametere for kontant- og bankbehandling**. Hvis alternativet **Bruk vurderingsprosess for betalingsannulleringer** er satt til **Ja**, sendes tilbakeføringer til journalen for banksjekkannullering for gjennomgang. Tabellen nedenfor beskriver hva som skiller sjekkannuleringsmetodene fra hverandre.

| Hvis organisasjonen ikke går gjennom sjekkannulleringer før postering                                                                                                                                  | Hvis organisasjonen går gjennom sjekkannulleringer før postering                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sjekken tilbakeføres umiddelbart når du klikker **OK** på **Sjekk**-siden.                                                                                                                      | Sjekken tilbakeføres ikke umiddelbart. Det opprettes en sjekkannuleringsjournal for gjennomgang. Hvis journalen for tilbakeføring av sjekker slettes, kan sjekken tilbakeføres på nytt.                                                                                                                                                                                                                                                                |
| Regnskapsoppføringene for den opprinnelige sjekken blir tilbakeført.                                                                                                                                         | Finanskontoen fra regnskapsposten for den opprinnelig sjekken posteres kanskje ikke. Finansdimensjonene fra den opprinnelige sjekkens journal brukes som standardfinansdimensjoner i sjekkannulleringsjournalen. Du kan endre disse standardverdiene. Når sjekkannuleringsjournalen posteres, angis hovedkontoene for leverandører automatisk fra posteringsprofilene, som kan ha endret. |
| Regnskapsstrukturene som ble brukt da den opprinnelige sjekken ble bokført, brukes til å tilbakeføre sjekken, selv om kontostrukturen er endret. Kontokombinasjonen er ikke validert. | Hvis en kontostruktur endres etter at den opprinnelige sjekken ble postert, kreves kanskje en ny finansdimensjon for tilbakeføringen av sjekken. Denne finansdimensjonen vil kanskje ikke angis automatisk fra den opprinnelige betalingsjournalen. Kontokombinasjonen valideres når sjekkannuleringen er postert.                                                                                                        |
| Faste dimensjoner brukes ikke på tilbakeføringen, for å sikre at de samme finanskontoene tilbakeføres.                                                                                      | Faste dimensjoner brukes på journalen for sjekkannulering ved postering. Finansdimensjonsverdien finnes kanskje ikke i regnskapsoppføringen for den opprinnelige sjekken, avhengig av når den faste dimensjonen ble definert.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Tilbakeføre posterte sjekker uten å se gjennom dem
Hvis organisasjonen vil postere sjekkannulleringer umiddelbart når du klikker **Betalingsannullering** på **Sjekker**-siden. På siden **Parametere for kontant- og bankbehandling** angir du alternativet **Bruk vurderingsprosess for betalingsannulleringer** til **Nei**. På **Sjekker**-siden kan du velge sjekken som skal tilbakeføres, og velge **Betalingsannullering**. Du kan deretter skrive inn datoen og velge en årsak for tilbakeføringen.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Tilbakefør posterte sjekker etter å ha gått gjennom dem i journalen for sjekkannullering.
Hvis organisasjonen vil gjennomgå sjekkannulleringer før de posteres, kan du opprette en sjekkannuleringsjournal og deretter, på siden **Parametere for kontant- og bankbehandling**, angi alternativet **Bruk vurderingsprosess for betalingsannulleringer** til **Ja**. På **Sjekker**-siden kan du velge sjekken som skal tilbakeføres, og velge **Betalingsannullering**. Du kan deretter skrive inn datoen og velge en årsak for tilbakeføringen. Du må også velge et journalnavn for å opprette en journal i banksjekkannulleringen.

### <a name="review-a-reversal"></a>Gjennomgå en tilbakeføring

Hvis du er en bruker som gjennomgå tilbakeføringer, kan du enten godkjenne og postere journalen eller avvise tilbakeføringen ved å slette journalen. På siden **Journal for sjekkannulleringer** kan du velge tilbakeføringsjournalen du vil gå gjennom, og deretter klikke **Linjer**. Du kan gjennomgå den tilbakeførte sjekken, og deretter velge ett av følgende godkjenningsalternativer:

-   For å godkjenne og postere den tilbakeførte journalen klikker du **Poster** eller **Poster og overfør**.
-   Hvis du vil avvise tilbakeføringen, sletter du journalen for sjekkannullering.

> [!NOTE]
> Hvis du sletter journalen, fjernes tilbakeføringen fra systemet, men den opprinnelige sjekken forblir på **Sjekk**-siden. Statusen til sjekken vil ikke lenger være **Venter på annullering**.

## <a name="results-of-posting-a-reversal"></a>Resultater av å postere en tilbakeføring
Når du posterer en sjekktilbakeføring, skjer følgende:

-   Sjekkens status oppdateres til **Annullering**.
-   Hvis **Avstem**-alternativet ble valgt på tilbakeføringssiden under tilbakeføringen, blir sjekken avstemt (alternativet **Avstemt** er valgt) og vises ikke på **Kontoavstemming**-siden.
-   Tilbakeføringsbilaget blir postert mot den bankkontoen som sjekken ble utstedt fra, slik at bankokontosaldoen øker.
-   Bilaget blir postert til økonomimodulen.
-   Endringsdetaljene oppdateres i feltgruppen **History** på **Sjekk**-siden.

> [!NOTE] 
> Når du tilbakefører en sjekk som er utstedt for en konsernintern handelstransaksjon, kommer de motposterte oppføringene fra regnskapsoppsettet for konsernintern handel, ikke fra den opprinnelige transaksjonen. Hvis sjekken som ble tilbakeført, var utstedt for en leverandørbetaling, skjer også følgende:

-   Den opprinnelige betalingen fra fakturaen som betalingen ble utlignet mot, blir ikke gjeldende (utligningen blir tilbakeført).
-   Det blir postert en transaksjon mot leverandørkontoen for betalingstilbakeføringen, og den tilbakeførte betalingen utlignes mot den opprinnelige betalingen. Feltet **Siste utligningsbilag** på **Leverandørtransaksjoner**-siden for den opprinnelige leverandørbetalingen blir oppdatert slik at det gjenspeiler bilagsnummeret til den tilbakeførte transaksjonen.

Hvis sjekken som ble tilbakeført, var utstedt for en kunderefundering, skjer også følgende:

-   Det blir postert en transaksjon mot kundekontoen for betalingstilbakeføringen, og utligningen mellom den opprinnelige betalingen og dokumentet som betalingen opprinnelig ble utlignet mot, blir tilbakeført (det blir opprettet en negativ betaling).
-   Det blir brukt en betalingstilbakeføring på den opprinnelige betalingen. Feltet **Siste utligningsbilag** på **Kundetransaksjoner**-siden for den opprinnelige kundebetalingen blir oppdatert slik at det gjenspeiler bilagsnummeret til den tilbakeførte transaksjonen.





