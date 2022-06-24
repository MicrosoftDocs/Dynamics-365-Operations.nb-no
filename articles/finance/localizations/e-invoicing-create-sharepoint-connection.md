---
title: Konfigurere en SharePoint-tilkobling
description: Denne artikkelen beskriver hvordan du konfigurerer en tilkobling slik at elektronisk fakturering får tilgang til et Microsoft SharePoint-område.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fb4258190b9480c1302060dd7b75145f80bb7f18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856587"
---
# <a name="configure-a-sharepoint-connection"></a>Konfigurere en SharePoint-tilkobling

[!include [banner](../includes/banner.md)]

Tjenesten for elektronisk fakturering kan lese filer fra Microsoft SharePoint-mapper og laste opp filer til SharePoint. For å sikre at elektronisk fakturering kan få tilgang til et bestemt SharePoint-område, må du gi tjenesten for elektronisk fakturering legitimasjonen for området. For å sikre at legitimasjonen lagres på en sikker måte, må du ikke angi den direkte. Lagre den i stedet i et Azure-nøkkelhvelv, og oppgi en Azure Key Vault-hemmelighet.

## <a name="grant-access-to-a-sharepoint-folder"></a>Gi tilgang til en SharePoint-mappe

1. Opprett en appregistrering i leieren der Regulatory Configuration Service (RCS) er installert.

    1. Logg på [Azure-portalen](https://portal.azure.com/).
    2. Gå til **Appregistreringer**.
    3. Velg **Ny registrering**.
    4. Angi et navn, for eksempel **SharePoint-app for elektronisk fakturering**, og fullfør registreringen.
    5. Velg den nye appregistreringen.
    6. Aktiver alternativet **Tillat offentlige klientflyter** i fanen **Autentisering**.
    4. Velg **Ny klienthemmelighet** for å opprette en klienthemmelighet i fanen **Sertifikater og hemmeligheter**.
    5. Kopier verdien til hemmeligheten som ble opprettet.

    Følg disse retningslinjene:

    - Ikke bruk samme appregistrering for ulike tjenester.
    - Følg [anbefalingene for passordpolicy](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Konfigurer rotasjon av passord. Under rotasjonen oppretter du en ny klienthemmelighet for appregistreringen, oppdaterer nøkkelhvelvet og sletter deretter den gamle hemmeligheten.

2. Lagre verdiene **Hemmelighet for appregistrering** og **Program-ID (klient)** som to nye hemmeligheter i nøkkelhvelvet i oppsettet for miljøet for elektronisk fakturering.
3. Legg til hemmelighetene du opprettet, i Key Vault-parameterne i oppsettet for miljøet for elektronisk fakturering i RCS.
4. Gi tilgang til SharePoint i Azure-portalen. Dette trinnet skal fullføres av leieradministratoren.

    1. Velg appregistreringen du opprettet.
    2. I fanen **API-tillatelser** velger du **Legg til en tillatelse**.
    3. Velg **Microsoft Graph (Programtillatelser)** \> **Sites.Selected**.
    4. Velg **Gi administratorsamtykke for \<user&nbsp;name\>**.
    5. Gå gjennom **Status**-feltet for å sikre at tillatelser er gitt.

        ![Tillatelser gitt i fanen API-tillatelser.](media/configured-permissions.jpg)

    6. Åpne [Graph Explorer – Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer), og logg deg på.
    7. Velg **hent SharePoint-område basert på relativ bane til området** under **SharePoint-områder** i fanen **Eksempelspørringer** i den venstre ruten.
    8. Fyll ut parameterne **\{host-name\}** og **\{server-relative-path\}**. Du kan for eksempel fylle inn `<domain>.sharepoint.com` for **\{host-name\}** og `sites/<siteName>` for **\{server-relative-path\}**.

        > [!NOTE]
        > For standard nettsted lar du parameteren **\{server-relative-path\}** være tom.

    9. Velg **Kjør spørring**, og lagre resultatet.
    10. Konfigurer følgende spørring.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        I denne spørringen er **\{site-id\}** verdien til **id**-noden fra det forrige spørringssvaret.

        Her er forespørselsteksten.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        I denne forespørselsteksten er **\{app-id\}** verdien for **Program-ID (klient)**, og **\{app-name\}** er **Programnavn**-verdien.

        ![POST-spørring.](media/app-id-query.jpg)

    11. Velg **Åpne tillatelsespanelet** i fanen **Endre tillatelser**, og velg deretter **Områder** \> **Sites.FullControl.All** \> **Samtykke**.
    12. Velg **Kjør spørring**.

Tjenesten for elektronisk fakturering har nå tilgang til SharePoint-området.
