---
title: Definere tilordningen for salgsordrestatusfeltene
description: Dette emnet beskriver hvordan du definerer salgsordrestatusfeltene for dobbelt skriving.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829291"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a>Definere tilordningen for salgsordrestatusfeltene

[!include [banner](../../includes/banner.md)]

Feltene som angir salgsordrestatus, har forskjellige opplistingsverdier i Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Det kreves tilleggsoppsett for å tilordne disse feltene med dobbelt skriving.

## <a name="fields-in-supply-chain-management"></a>Felt i Supply Chain Management

I Supply Chain Management viser to felt statusen for salgsordren. Feltene du må tilordne, er **Status** og **Dokumentstatus**.

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

## <a name="fields-in-sales"></a>Felt i Sales

I Sales viser to felt statusen for ordren. Feltene du må tilordne, er **Status** og **Behandlingsstatus**.

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

Hvis du vil konfigurere tilordningen for salgsordrestatusfeltene, må du aktivere attributtene **IsSOPIntegrationEnabled** og **isIntegrationUser**.

Følg denne fremgangsmåten for å aktivere attributtet **IsSOPIntegrationEnabled**.

1. I en webleser kan du gå til `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Erstatt **\<test-name\>** med firmaets kobling til Sales.
2. På siden som åpnes, finner du **organizationid**, og noter verdien.

    ![Finne organizationid](media/sales-map-orgid.png)

3. I Sales åpner du leserkonsollen og kjører følgende skript: Bruk **organizationid**-verdien fra trinn 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kode i leserkonsollen](media/sales-map-script.png)

4. Kontroller at **IsSOPIntegrationEnabled** er satt til **sann**. Bruk URL-adressen fra trinn 1 til å kontrollere verdien.

    ![Kontroller at IsSOPIntegrationEnabled er satt til sann](media/sales-map-integration-enabled.png)

Følg denne fremgangsmåten for å aktivere attributtet **isIntegrationUser**.

1. I Sales kan du gå til **Innstilling \> Tilpasning \> Tilpass systemet**, velge **Brukerenhet** og deretter åpne **Skjema \> Bruker**.

    ![Åpne brukerskjemaet](media/sales-map-user.png)

2. I Feltutforsker finner du **Modusen Integreringsbruker** og dobbeltklikker den for å legge den til i skjemaet. Lagre endringene.

    ![Legge til feltet Integreringsbruker i skjemaet](media/sales-map-field-explorer.png)

3. I Sales går du til **Innstilling \> Sikkerhet \> Brukere** og endrer visningen fra **Aktiverte brukere** til **Programbrukere**.

    ![Endre visning fra Aktiverte brukere til Programbrukere](media/sales-map-enabled-users.png)

4. Velg de to oppføringene for **DualWrite IntegrationUser**.

    ![Liste over programbrukere](media/sales-map-user-mode.png)

5. Endre verdien for feltet **Integreringsbruker** til **Ja**.

    ![Endre verdien for feltet Integreringsbruker](media/sales-map-user-mode-yes.png)

Salgsordrene er nå tilordnet.
