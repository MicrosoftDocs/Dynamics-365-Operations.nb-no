---
title: Definere tilordningen for salgsordrens statuskolonner
description: Dette emnet beskriver hvordan du definerer salgsordrestatuskolonnene for dobbel skriving.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: eb3e3e87f7615a289f019a5d47dbc596f0266aa5
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416582"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Definere tilordningen for salgsordrens statuskolonner

[!include [banner](../../includes/banner.md)]

Kolonnene som angir salgsordrestatus, har forskjellige opplistingsverdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Det kreves tilleggsoppsett for å tilordne disse kolonnene med dobbel skriving.

## <a name="columns-in-supply-chain-management"></a>Kolonner i Supply Chain Management

I Supply Chain Management viser to kolonner statusen for salgsordren. Kolonnene du må tilordne, er **Status** og **Dokumentstatus**.

**Status**-opplistingen angir den totale statusen til ordren. Denne statusen vises i ordrehodet.

**Status**-opplistingen har følgende verdier:

- Åpen ordre
- Levert
- Fakturert
- Annullert

**Dokumentstatus**-opplistingen angir det nyeste dokumentet som ble generert for ordren. Hvis for eksempel ordren er bekreftet, er dette dokumentet en salgsordrebekreftelse. Hvis en salgsordre er delvis fakturert, og den gjenværende linjen deretter blir bekreftet, forblir dokumentstatusen **Faktura**, fordi fakturaen genereres senere i prosessen.

**Dokumentstatus**-opplistingen har følgende verdier:

- Bekreftelse
- Plukkliste
- Følgeseddel
- Faktura

## <a name="columns-in-sales"></a>Kolonner i Salg

I Sales viser to kolonner statusen for ordren. Kolonnene du må tilordne, er **Status** og **Behandlingsstatus**.

**Status**-opplistingen angir den totale statusen til ordren. Det har følgende verdier:

- Aktive
- Sendt inn
- Oppfylt
- Fakturert
- Annullert

Opplistingen **Behandlingsstatus** ble innført, slik at statusen kan tilordnes mer nøyaktig ved hjelp av Supply Chain Management.

Følgende tabell viser tilordningen av **Behandlingsstatus** i Supply Chain Management.

| Behandlingsstatus   | Status i Supply Chain Management | Dokumentstatus i Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktive              | Åpen ordre                        | None                                       |
| Bekreftet           | Åpen ordre                        | Bekreftelse                               |
| Plukket              | Åpen ordre                        | Plukkliste                               |
| Delvis levert | Åpen ordre                        | Følgeseddel                               |
| Levert           | Levert                         | Følgeseddel                               |
| Delvis fakturert  | Levert                         | Faktura                                    |
| Fakturert            | Fakturert                          | Faktura                                    |
| Annullert           | Annullert                         | Gjelder ikke                             |

Følgende tabell viser tilordningen av **Behandlingsstatus** mellom Sales og Supply Chain Management.

| Behandlingsstatus   | Status i Sales | Status i Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Aktive              | Aktive          | Åpen ordre                        |
| Bekreftet           | Sendt inn       | Åpen ordre                        |
| Plukket              | Sendt inn       | Åpen ordre                        |
| Delvis levert | Aktive          | Åpen ordre                        |
| Delvis fakturert  | Aktive          | Åpen ordre                        |
| Delvis fakturert  | Oppfylt       | Levert                         |
| Fakturert            | Fakturert        | Fakturert                          |
| Annullert           | Annullert       | Annullert                         |

## <a name="setup"></a>Installasjon

Hvis du vil konfigurere tilordningen for salgsordrestatuskolonnene, må du aktivere attributtene **IsSOPIntegrationEnabled** og **isIntegrationUser**.

Følg denne fremgangsmåten for å aktivere attributtet **IsSOPIntegrationEnabled**.

1. I en webleser kan du gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Erstatt **\<test-name\>** med firmaets kobling til Sales.
2. På siden som åpnes, finner du **organizationid**, og noter verdien.

    ![Finne organizationid.](media/sales-map-orgid.png)

3. I Sales åpner du leserkonsollen og kjører følgende skript: Bruk **organizationid**-verdien fra trinn 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i leserkonsollen.](media/sales-map-script.png)

4. Kontroller at **IsSOPIntegrationEnabled** er satt til **sann**. Bruk URL-adressen fra trinn 1 til å kontrollere verdien.

    ![Kontroller at IsSOPIntegrationEnabled er satt til sann.](media/sales-map-integration-enabled.png)

Følg denne fremgangsmåten for å aktivere attributtet **isIntegrationUser**.

1. I Sales kan du gå til **Innstilling \> Tilpasning \> Tilpass systemet**, velge **Brukertabell** og deretter åpne **Skjema \> Bruker**.

    ![Åpne brukerskjemaet.](media/sales-map-user.png)

2. I Feltutforsker finner du **Modusen Integreringsbruker** og dobbeltklikker den for å legge den til i skjemaet. Lagre endringene.

    ![Legge til kolonnen Integreringsbruker i skjemaet.](media/sales-map-field-explorer.png)

3. I Sales går du til **Innstilling \> Sikkerhet \> Brukere** og endrer visningen fra **Aktiverte brukere** til **Programbrukere**.

    ![Endre visning fra Aktiverte brukere til Programbrukere.](media/sales-map-enabled-users.png)

4. Velg de to oppføringene for **DualWrite IntegrationUser**.

    ![Liste over programbrukere.](media/sales-map-user-mode.png)

5. Endre verdien for kolonnen **Integreringsbruker** til **Ja**.

    ![Endre verdien for kolonnen Integreringsbruker.](media/sales-map-user-mode-yes.png)

Salgsordrene er nå tilordnet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]