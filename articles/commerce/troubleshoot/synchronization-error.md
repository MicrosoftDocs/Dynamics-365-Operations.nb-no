---
title: Synkroniseringsproblemer for asynkron ordre
description: Denne artikkelen beskriver vanlige årsaker til feil i oppretting av asynkron ordre i Microsoft Dynamics 365 Commerce og tilbyr feilsøkingstrinn for å hjelpe systembrukere og partnere med å forstå hva som gikk feil.
author: Shajain
ms.date: 11/30/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 27bccced3c07149fe1842524660447a49f86f3fc
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815763"
---
# <a name="asynchronous-order-synchronization-issues"></a>Synkroniseringsproblemer for asynkron ordre

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver vanlige årsaker til feil i oppretting av asynkron ordre i Microsoft Dynamics 365 Commerce og tilbyr feilsøkingstrinn for å hjelpe systembrukere og partnere med å forstå hva som gikk feil.

## <a name="symptom"></a>Symptom

Asynkrone ordrer som opprettes fra e-handel eller salgssted i Dynamics 365 Commerce, gjenspeiles ikke i Commerce headquarters.

## <a name="troubleshooting"></a>Feilsøking

Ordreopprettelse kan mislykkes i hovedkontoret av forskjellige årsaker, avhengig av stadiet som ordreopprettingsprosessen mislykkes under. Fremgangsmåten nedenfor går gjennom de mulige underliggende årsakene.

### <a name="validate-that-the-transaction-related-to-the-asynchronous-order-has-reached-headquarters"></a>Kontroller at transaksjonen relatert til den asynkrone ordren har nådd hovedkontoret

For e-handelordrer i hovedkontoret går du til **Detaljhandel og handel \> Forespørsler og rapporterer \> Nettbutikktransaksjoner**. Hvis du har et bekreftelsesnummer for ordren, filtrerer du transaksjonene ved å angi bekreftelsesnummeret i feltet **Kanalreferanse-ID** . Hvis du ikke har bekreftelsesnummeret, filtrerer du transaksjonene ved å angi kundekontonummeret.

For POS-ordrer åpner du siden **Butikktransaksjoner** og filtrerer postene etter kvitteringsnummer eller kundekontonummer. Hvis transaksjonen ikke blir funnet, kan du kjøre kanaltransaksjonsjobben **P-0001**, som synkroniserer transaksjoner fra kanalene til hovedkontoret. Hvis **P-0001-jobben** mislykkes, åpner du en støtteforespørsel for jobbfeilen. Hvis **P-0001**-jobben er vellykket, men transaksjonene fremdeles ikke vises i hovedkontoret, åpner du en støttebillett som inkluderer den aktuelle informasjonen.
 
### <a name="check-the-synchronization-status-if-the-transaction-is-present-in-headquarters-but-isnt-linked-with-a-sales-order"></a>Kontroller synkroniseringsstatusen hvis transaksjonen finnes i hovedkontoret, men ikke er tilknyttet en salgsordre

Hvis transaksjonen finnes i hovedkontoret, men salgsordren ikke er opprettet, kan du åpne siden **Nettbutikktransaksjoner** og velge hurtigkategorien **Synkroniseringsstatus**. Hvis jobben **Synkroniser ordrer** forsøkte å synkronisere denne transaksjonen, skal feltet **Status for ventende ordre** vise statusen **Vellykket** eller **Mislykket**. Hvis statusen er **Vellykket**, må salgsordrefeltet være til stede på denne transaksjonen. Hvis statusen er **Mislykket**, kan du vise feildetaljene i feltet **Ordrefeildetaljer** på hurtigfanen **Synkroniseringsstatus**. Hvis ingen av disse statusene vises, er det ikke gjort forsøk på å behandle transaksjonen. I dette tilfellet kan du velge **Synkroniser ordre** øverst på siden for å kjøre synkroniseringsjobben.

Kontroller at jobben **Synkroniser ordrer** er planlagt å kjøre periodisk, slik at asynkrone transaksjoner kan opprettes som ordrer i hovedkontoret.

De følgende delene gir informasjon om vanlige feil og forslag til løsning.

#### <a name="the-order-error-details-field-shows-the-following-error-message-number-sequence-has-been-exceeded"></a>Feltet Detaljer om ordrefeil viser følgende feilmelding: Nummerserien er overskredet

Nummerserier brukes til å opprette salgsordrer i hovedkontoret. Hvis alle numrene som er tillatt for en nummerserie, er fullstendige, genererer systemet denne feilmeldingen. Nummerserien som brukes til å opprette salgsordrer, finner du på **Kundeparametere \> Nummerserier \> Salgsordre**. Hvis du vil korrigere denne feilen, kan du korrigere den eksisterende nummerserien eller erstatte den med en ny nummerserie.

#### <a name="the-order-error-details-field-shows-the-following-error-message-there-must-be-a-default-payment-service-to-process-credit-card-transactions"></a>Feltet Detaljer om ordrefeil viser følgende feilmelding: Det må være en standard betalingstjeneste for å behandle kredittkorttransaksjoner

Hvis du vil korrigere denne feilen, bekrefter du at en standardbetaling er definert i hovedkontoret. Hvis ingen standardbetaling er definert, må du definere en. Gå til **Kunder \> Betalingsoppsett \> Betalingstjenester**, og kontroller at alternativet **Standardbehandler for nye kredittkort** er satt til **Ja** for én betalingstjeneste.
    
#### <a name="the-order-error-details-field-shows-an-account-structure-error-message"></a>Feltet Detaljer om ordrefeil viser en feilmelding om kontostrukturen

Teksten i feilmeldingen for kontostrukturen kan variere, slik eksemplene nedenfor viser. Feilene deler imidlertid en felles rotårsak som er knyttet til kontostrukturkonfigurasjonen.

- "Posteringsresultater for journalpartinummer 0009656328 bilag ARP-000959899 1.00 for bilagsnummer ARP-000959899 i firmaet usrt vil bli postert som en overbetaling eller underbetaling"
- "Posteringsresultater for journalpartinummer 0009656328 bilag ARP-000959899 bilag ARP-000959901 Kontostruktur for kombinasjonen 618160 er ikke gyldig for finanskontoen Delt hovedkonto for firma"
- "Posteringsresultater for journalpartinummer 0009656328 bilagsnummer ARP-000959899 bilag ARP-000959901 rapportert fra firmakontoer usrt"
- "Posteringsresultater for journalpartinummer 0009656328 bilagsnummer ARP-000959899 Posteringen er avbrutt"
    
Hvis du vil korrigere disse feilene, må du kontrollere om kontostrukturene er nøyaktig. Hvis du vil ha mer informasjon, kan du se [Konfigurere kontostrukturer](/dynamics365/finance/general-ledger/configure-account-structures).
    
Når feilen er rettet, velger du den mislykkede transaksjonen, og deretter velger du **Synkroniser ordre** øverst på siden for å kjøre synkroniseringsjobben.
    
#### <a name="other-types-of-errors-that-might-require-the-transaction-data-to-be-fixed"></a>Andre typer feil som kan kreve at transaksjonsdataene er faste

Hvis du vil korrigere andre typer feil som kanskje krever at transaksjonsdataene er faste, kan du bruke funksjonen Redigere og overvåke transaksjoner. Hvis du vil ha mer informasjon, kan du se [Redigere og overvåke transaksjoner](../edit-order-trans.md).
