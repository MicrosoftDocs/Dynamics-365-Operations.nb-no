---
title: Avstemme bankkontoutdrag med avansert bankavstemming
description: Funksjonen Avansert bankavstemming lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 Finance. Dette emnet beskriver avstemmingsprosessen.
author: moaamer
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: kfend
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27956cbc4d51c1b907138b49947b57a570d98da1
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727573"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Avstemme bankkontoutdrag med avansert bankavstemming

[!include [banner](../includes/banner.md)]

Funksjonen Avansert bankavstemming lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Dynamics 365 Finance. Dette emnet beskriver avstemmingsprosessen.  

## <a name="import-an-electronic-bank-statement"></a>Importere et elektronisk bankkontoutdrag

Du importerer bankkontoutdraget ved hjelp av handlingen **Importer utdrag** på siden **Bankkontoutdrag**. På bankkontoutdraget identifiseres bankkontoen av en kombinasjon av verdier som er angitt for bankkontodetaljene. Disse verdiene inkluderer banknavn, bankkontonummer, rutenummer, SWIFT-kode (Society for Worldwide Interbank Financial Telecommunication) og IBAN (International Bank Account nummer). 

Du kan laste opp et bankkontoutdrag som inneholder informasjon for én enkelt konto eller flere konti. Hvis det finnes flere kontoer, kan det være kontoene i andre juridiske enheter.

-   Hvis du vil importere én enkelt bankkontoutdragsfil for én enkelt konto, kan du sette alternativet **Importer utdrag for flere bankkontoer i alle juridiske enheter** til **Nei** og velge bankkontoen som er knyttet til utdraget. Klikk **Bla gjennom** for å velge den tilknyttede bankkontoutdragsfilen, og klikk deretter **Last opp**.
-   Hvis du vil importere én enkelt bankkontoutdragsfil for flere kontoer, setter du **Importer utdrag for flere bankkontoer i alle juridiske enheter** til **Ja**. Klikk **Bla gjennom** for å velge den tilknyttede bankkontoutdragsfilen, og klikk deretter **Last opp**.

Hvis alle setninger i den elektroniske filen ikke kan knyttes til en bankkonto, eller hvis den er tilknyttet flere bankkontoer ved hjelp av de identifiserende feltene, kan de ikke importeres. Andre setninger i filen kan imidlertid likevel importeres. Brukeren får deretter en melding om at import av bankkontoutdrag mislyktes for bestemte bankkontoer. Legg merke til at brukeren som importerer bankkontoutdragsfilen, må ha tilgang til en juridisk enhet for å importere utdrag for bankkontoer for den juridiske enheten. 

Du kan bruke en ZIP-fil til å laste opp flere utdragsfiler til Finance i én enkelt prosess. Hvis du vil importere flere bankkontoutdragsfiler for flere kontoer, kan du kombinere alle bankkontoutdragsfilene i en ZIP-fil. I dialogboksen **Importer bankkontoutdrag** setter du alternativet **Importer utdrag for flere bankkontoer i alle juridiske enheter** til **Ja**. Klikk **Bla gjennom** for å velge ZIP-filen som inneholder bankkontoutdragsfilene, og klikk deretter **Last opp**. Importprosessen gjenkjenner zip-filen og laster opp hver oppgave som er inkludert i den, uavhengig av den juridiske enheten for bankkontoen.

Alternativet **Avstem etter import** er tilgjengelig. Når du setter dette alternativet til **Ja**, validerer systemet automatisk bankkontoutdraget, oppretter ny bankavstemming og nytt regneark og kjører standard samsvarsregelsett når bankkontoutdraget lastes opp. Denne funksjonen automatiserer prosessen frem til der transaksjoner må kontrolleres manuelt.

## <a name="validate-the-bank-statement"></a>Validere bankkontoutdraget
Hvis du vil validere et utdrag, klikker du **Valider** på siden **Bankkontoutdrag**. Bankkontoutdrag må valideres før de kan avstemmes. Dette trinnet fullføres automatisk hvis du setter alternativet **Avstem etter import** til **Ja** på importtidspunktet. 

Validering av bankkontoutdrag kontrollerer følgende detaljer:

-   Bankkontoutdraget samsvarer med den valgte bankkontoen.
-   Valutaen for bankkontoutdraget samsvarer med valutaen for bankkontoen.
-   Startsaldoen for utdraget er lik avslutningssaldoen til det forrige utdraget for bankkontoen.
-   Datoen overlapper ikke med dato for et annet bankkontoutdrag for samme konto.
-   Det er ingen mellomrom i datoer for utdrag for bankkontoen.
-   Datoer på utdragslinjene er mellom fra- og til-dato på bankkontoutdraget.
-   Startsaldoen og summerte linjebeløp er lik sluttsaldoen.

Når valideringen er fullført, oppdateres statusen for bankkontoutdraget til **Validert**. Et bankkontoutdrag må valideres før det kan avstemmes.

## <a name="reconcile-the-bank-statement"></a>Avstemme bankkontoutdraget
Når du har importert et elektronisk bankkontoutdrag og validert utdraget på siden **Bankkontoutdrag**, kan du avstemme bankkontoutdraget ved hjelp av sidene **Bankavstemming** og **Bankavstemmingsregneark**. 

På siden **Bankavstemming** klikker du **Ny** for å opprette en ny avstemming, og deretter velger du bankkontoen for utdraget som ble importert. En bankkonto kan ha bare én åpen bankavstemming. Fristdatoen bestemmer bankkontoutdragstransaksjoner og Operations-banktransaksjoner som er inkludert i avstemmingsregnearket. Som standard brukes gjeldende systemdato som fristdato, men du kan endre datoen for avstemmingen. Gjenstående hodeinformasjonen hentes automatisk fra utdraget. Dette trinnet fullføres automatisk hvis du setter alternativet **Avstem etter import** til **Ja** på importtidspunktet. 

På siden **Bankavstemming** klikker du **Regneark** for å åpne siden **Bankavstemmingsregneark**. Hvis du setter alternativet **Avstem etter import** til **Ja**, kjøres Standard samsvarsregelsett automatisk for avstemmingen som standard. Hvis du vil kjøre samsvarsregler manuelt, klikker du **Kjør samsvarsregler** for å velge samsvarsregelsettene eller samsvarsreglene som skal kjøres mot banktransaksjonene. Hvis du har mange transaksjoner som skal behandles, kan du fullføre dette trinnet som en satsvis prosess. 

Siden **Bankavstemmingsregneark** har fire rutenett som inneholder transaksjoner. To øvre rutenettene viser transaksjonene fra bankkontoutdraget og Operations som ennå ikke er utlignet. To nedre rutenettene viser utlignede transaksjoner. Kategorien **Detaljer for bankkontoutdragstransaksjon** viser detaljer for ikke-avstemte bankkontoutdragstransaksjoner som er valgt i det øvre rutenettet. 

Det finnes tre måter for å utligne eller avstemme bankkontoutdragstransaksjoner:

-   Utligne transaksjoner med Operations-banktransaksjoner.
-   Utligne transaksjoner med en tilbakeføring for bankkontoutdragstransaksjon.
-   Merke transaksjonene som **Ny**, slik at de kan posteres senere som en banktransaksjon i Finance.

Hvis du vil utligne transaksjoner manuelt, velger du transaksjonene i rutenettet **Bankkontoutdragstransaksjoner**, velger tilsvarende transaksjoner i rutenettet **Operations-banktransaksjoner**, og klikker deretter **Samsvar**. De valgte transaksjonene flyttes fra øvre rutenett for ikke-utlignede transaksjoner til nedre rutenett for utlignede transaksjoner. I tillegg oppdateres utlignede og ikke-utlignede totalbeløp. Du kan ha transaksjonsutligninger av typen en-til-en, mange-til-en og mange-til-mange. Utligninger må følge reglene for tillatte datoforskjeller og tilordning av transaksjonstype. Disse reglene settes på siden **Parametere for kontant- og bankbehandling**.

Øredifferanser kan oppstå i avstemmingen. Du kan utligne én enkelt bankkontoutdragstransaksjon med én enkelt Operations-banktransaksjon som har øredifferanser, hvis øredifferansene er innenfor toleransebeløpet som er definert av feltet **Tillatt øredifferanse** for bankkontoen. Beløpet vises i feltet **Korreksjonsbeløp** i den samsvarende Operations-banktransaksjonen. Når bankavstemmingen er merket som avstemt, posteres rettelser automatisk ved hjelp av hovedkontoen som er definert i den tilknyttede banktransaksjonstypen. Rettelser støttes ikke for dokumenttypene **Sjekk** og **Innskudd**. 

Tilbakeføring for bankkontoutdragstransaksjon utlignes ved hjelp av avstemmingsregnearket. To utdragslinjer kan utlignes hvis beløpene er motsatt, og hvis én av transaksjonene er merket som en tilbakeføring. Du kan også definere en samsvarsregel for handlingen **Nullstill tilbakeføringsutdragslinjer**.

Tilbakeførte Operations-banktransaksjoner må avstemmes ved hjelp av siden **Operations-banktransaksjoner**. Du kan avstemme to Operations-banktransaksjoner sammen hvis dokumentene har samme bankkonto, dokumenttype og betalingsreferanse, og hvis de har motsatt beløp. Du kan også avstemme én enkelt annullert sjekk for å hindre at disse transaksjonene vises på avstemmingsregnearket. 

Hvis det finnes nye transaksjoner som er initiert av banken, for eksempel rente, avgifter og gebyrer som ennå ikke er i Finance, kan du legge dem til en journal som er knyttet til den valgte avstemmingen av bankkontoutdraget. Velg en bankkontoutdragstransaksjon i rutenettet **Bankkontoutdragstransaksjoner** for ikke-utlignede transaksjoner, og klikk deretter **Merk som ny**. Statusen for transaksjonene settes til **Ny**, og transaksjonen flyttes til rutenettet **Bankkontoutdragstransaksjoner** for utlignede transaksjoner. Du posterer transaksjoner som er merket som **Ny** senere, fra siden **Bankkontoutdrag**. 

Du kan oppheve avstemmingen av transaksjoner som ble feilaktig avstemt. Velg den avstemte bankkontoutdragstransaksjonen, og klikk deretter **Opphev samsvar**. Alle tilknyttede transaksjoner flyttes tilbake til det øvre rutenett for ikke-avstemte transaksjoner, og utlignede og ikke-utlignede totalbeløp oppdateres. 

Når du har fullført avstemningsprosessen, bør du markere regnearket for avstemming som avstemt.  Denne prosessen vil automatisk legge inn korreksjonsbeløp ved hjelp av kontoene som er angitt på siden **banktransaksjonstype**.  Bankavstemming for et utdrag kan markeres som avstemt når som helst, selv om det er linjer på bankkontoutdraget som ennå ikke er avstemt.  De ikke avstemte transaksjonene vil automatisk flyttes til neste arbeidsark for avstemmning, da ikke avstemte bankkontoutdragstransaksjoner skal avstemmes.  Vær oppmerksom på at når en bankkontudragavstemming er markert som avstemt, kan ikke det angres.  Avstemmingen vil ikke lenger kunne redigeres, og du vil ikke lenger ha mulighet til å gjøre oppdateringer til avstemmingen.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Postere nye transaksjoner som er tilknyttet den valgte avstemmingen
Bankkontoutdragstransaksjoner du merket som **Ny** på avstemmingsregnearket, posteres på siden **Bankkontoutdrag**. På siden **Bankkontoutdrag** velger du utdrags-ID for å vise utdragsdetaljene. På **Regnskap**-menyen kan du bruke alternativene **Vis distribusjoner** og **Vis regnskap** for å vise detaljene bak de nye transaksjonene og de tilhørende bankpostene. Velg alternativet **Poster** for å postere bankkontoutdragslinjer som er merket som **Ny** i økonomimodulen. Vær oppmerksom på at posteringer bare kan fullføres én gang per bankkontoutdrag.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
