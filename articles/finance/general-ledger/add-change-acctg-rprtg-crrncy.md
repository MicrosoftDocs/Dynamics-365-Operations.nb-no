---
title: Endre regnskaps- eller rapporteringsvalutaen
description: Dette emnet beskriver hvordan du endrer regnskaps- eller rapporteringsvalutaen, eller legger til en rapporteringsvaluta i finansoppsettet.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff5c38193e8469cb806c525b77809844847d6c92
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710899"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Endre regnskaps- eller rapporteringsvalutaen

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du endrer regnskaps- eller rapporteringsvalutaen, eller legger til en rapporteringsvaluta i finansoppsettet.

## <a name="symptom"></a>Symptom

Du vil endre regnskaps- eller rapporteringsvalutaen eller legge til en rapporteringsvaluta i finansoppsettet. Dette skjer vanligvis i følgende scenarioer:

- Feil regnskaps- eller rapporteringsvaluta ble angitt da en juridisk enhet ble konfigurert. Nå vil du endre valutaen.
- Det ble angitt en rapporteringsvaluta da en juridisk enhet ble konfigurert, men organisasjonen ønsker nå å fjerne rapporteringsvalutaen.
- Organisasjonen oppgraderer eller går over til Microsoft Dynamics 365 Finance og ønsker å endre regnskaps- eller rapporteringsvalutaen.

En organisasjon som ikke tidligere har brukt funksjonen Dobbel valuta, ønsker å begynne å bruke den. Dette problemet skjer vanligvis i følgende scenarioer.

- Ingen rapporteringsvaluta ble angitt da en juridisk enhet ble konfigurert. (En rapporteringsvaluta er valgfri.) Nå vil du legge til en rapporteringsvaluta.

## <a name="resolution"></a>Løsning

Det viktigste hensynet er om noen transaksjoner (faktisk eller budsjett) er postert i den juridiske enheten for finansoppsettet. **Du kan ikke endre regnskaps- eller rapporteringsvalutaen eller legge til en rapporteringsvaluta hvis noen transaksjoner (faktisk eller budsjett) er postert i den juridiske enheten.** Følg fremgangsmåten i en av delene nedenfor, avhengig av om transaksjonene er postert.

### <a name="no-transactions-have-been-posted"></a>Ingen transaksjoner er postert

1. Gå til **Økonomimodul \> Finansoppsett \> Finans** i den juridiske enheten du oppdaterer valutaer for.
2. Velg **Rediger** på siden **Finans**.
3. Velg regnskapsvalutaen og rapporteringsvalutaen som skal brukes for den juridiske enheten, på hurtigfanen **Valuta**.
4. Velg **Lagre**.

Hvis feltene for regnskapsvalutaen og rapporteringsvalutaen ikke er tilgjengelige på siden **Finans**, er en eller flere transaksjoner (faktisk eller budsjett) postert i den juridiske enheten. Derfor kan ikke valutaene endres. I dette tilfellet går du gjennom fremgangsmåten i den neste delen.

### <a name="transactions-have-been-posted"></a>Transaksjoner er postert

**Hvis transaksjoner er postert i den juridiske enheten, er den eneste måten å endre eller legge til regnskaps- og rapporteringsvalutaer på, å opprette en ny juridisk enhet som har de riktige valutaene.** For å gjøre denne prosessen enklere kan du ved hjelp av databehandling i systemet kopiere oppsettposter og hovedposter fra den gjeldende juridiske enheten til en ny juridisk enhet.

Endringer i regnskaps- og rapporteringsvalutaene er dyptgående. De påvirker ikke bare økonomimodulen, men også hver underfinans (kunder, leverandører, lager, prosjekt og så videre), alle løsninger for uavhengig programvareleverandør (ISV) og eventuelle utvidelser du har gjort som lagrer beløp.

Prosessen med å finne og oversette hvert beløp til ulike valutaer er underlagt feil. Derfor vil ikke teknikerteamet godkjenne et skript som endrer eller legger til regnskaps- og rapporteringsvalutaer. Før fantes det et verktøy for Microsoft Dynamics AX 2012 som lot deg endre eller legge til regnskaps- og rapporteringsvalutaer, men verktøyet ble avskrevet for både AX 2012 R3 og Finance.

Følg denne fremgangsmåten for å kopiere oppsett- og hoveddataene fra den gjeldende juridiske enheten til en ny juridisk enhet.

1. Gå til **Arbeidsområder \> Databehandling**.
2. Velg **Maler** under gruppen **Import/eksport**.
3. Kontroller at malene er tilgjengelige. Hvis ingen maler er tilgjengelige, velger du **Last inn standardmaler** og venter på at malene skal genereres.
4. Gå tilbake til arbeidsområdet **Databehandling**.
5. Velg **Kopier til juridisk enhet**.
6. Angi navn på og beskrivelse av gruppen.
7. Velg den juridiske enheten du vil kopiere data fra, i feltet **Juridisk kildeenhet**.
8. I hurtigfanen **Juridiske målenheter** velger du **Opprett juridiske enheter** for å opprette en ny juridisk enhet som du kan kopiere dataene for juridisk kildeenhet til. Velg **Velg eksisterende** for å kopiere data til en eksisterende juridisk enhet.
9. Valgfritt: Sett feltet **Kopier nummerserier** til **Ja**. (Dette trinnet anbefales når du kopierer data.)
10. Velg **Legg til mal** i området **Valgte enheter**.
11. Velg malen som skal brukes. Foreslåtte maler for en ny juridisk enhet omfatter **025 – Økonomimodul** og **Finans**. Vi anbefaler at du går gjennom alle de andre tilgjengelige malene for å finne ut om noen av dem gjelder for dine kravene.
12. Velg **Kopier til juridisk enhet** for å starte en partiprosess som oppretter de valgte enhetene og kopierer dem til den juridiske målenheten.
13. Når prosessen er fullført, men før noen transaksjoner posteres, kan du gå til finans og oppdatere regnskaps- og rapporteringsvalutaene slik det er beskrevet tidligere i dette emnet.

Hvis du har opprettet en ny juridisk enhet slik at du kan endre regnskaps- eller rapporteringsvalutaen, må du kontrollere at startsaldoene er omregnet fra valutaene i den gamle juridiske enheten til de nye valutaene.

Hvis du vil se en video som viser fremgangsmåten ovenfor, kan du se [Kopier til juridisk enhet](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
