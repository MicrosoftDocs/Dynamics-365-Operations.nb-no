---
title: Commerce-nettprat med Omnikanal for Customer Service-modul
description: Denne artikkelen beskriver Commerce-nettprat med Omnikanal for Customer Service-modulen i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: e4a004b929138f0a04c19d6a94278cfad6e83303
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346392"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Commerce-nettprat med Omnikanal for Customer Service-modul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikkelen beskriver *Commerce-nettprat med Omnikanal for Customer Service*-modulen i Microsoft Dynamics 365 Commerce.

I Commerce-versjon 10.0.29 er en ny Commerce-nettprat med Omnikanal for Customer Service-modulen lagt til i Commerce-modulbiblioteket. Funksjonen Commerce-nettprat tilbyr netthandelskunder med nettpratfunksjonene i Dynamics 365 Omnikanal for Customer Service, som inkluderer live agentstøtte for å hjelpe til med å løse kundespørringer, tilby kundeservice og tilrettelegge for salg for Commerce-kunder.

Ved hjelp av Commerce-nettpratfunksjonen kan forhandlerne oppnå disse målene:

- Få bedre tilpasset kontakt med kundene for å forbedre kundetilfredshet.
- Forbedre kundeservice gjennom integreringen av menneskelig agent og selvbetjeningsnettpratroboter.
- Hjelp agenter med å få erfaring via profil, bestilling og innkjøp av data i sanntid som driver forbedringer og engasjement i driften.
- Få bedre kundetilfredshet for å øke salget.

Følgende funksjoner er tilgjengelige som en del av funksjonen Commerce-nettprat:

- Commerce-nettprat med Omnikanal for Customer Service
- Tillegget av **Commerce Call Center** som en programfane i agenterfaringen i Dynamics 365 Omnikanal for Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Forutsetninger for Omnikanal for Customer Service

Det er en forutsetning at du konfigurerer nettprat i kontrollprogrammet Omnikanal for kundeserviceadministrationog henter noen av parameterne for å konfigurere Commerce-nettpratfunksjonen. Hvis du vil ha instruksjoner, kan du se [Konfigurere en nettpratkanal](/dynamics365/customer-service/set-up-chat-widget).

Når du har konfigurert nettprat i kontrollprogrammet Omnikanal for kundeserviceadministrasjon, får du et skript som ligner på eksemplet nedenfor.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Kopier dette skriptet, fordi du trenger verdiene i det for å konfigurere nettpratmodulen.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Obligatoriske felter for Commerce-nettprat med Omnikanal for Customer Service

Følgende tabell viser skriptverdiene fra kontrollprogrammet Omnikanal for kundeserviceadministrasjon, som kreves for å konfigurere Commerce-nettprat med Omnikanal for Customer Service-modulen.

| Kontrollprogramegenskap | Beskrivelse |
| ------------- |--------------|
| Skriptkilde | Verdien for **src** i skriptet for nettpratkontrollprogram. |
| ID for dataapp | Verdien for **data-app-id** i skriptet for nettpratkontrollprogram. |
| Dataorganisasjons-ID | Verdien for **data-org-id** i skriptet for nettpratkontrollprogram. |
| Nettadresse for dataorganisasjon | Verdien for **data-org-url** i skriptet for nettpratkontrollprogram. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Konfigurer Commerce-nettprat for netthandelsområdet

En anbefalt måte å implementere nettprat for netthandel på er å legge til Commerce-nettprat med Omnikanal for Customer Service-modulen i det delte hodefragmentet som brukes på netthandelsidene.

Følg denne fremgangsmåten for å legge til nettpratmodulen på nettstedets hodefragment i Commerce-områdebygger.

1. Gå til **Fragmenter** i områdebygger for nettstedet.
1. Velg **Ny**.
1. I dialogboksen **Velg et fragment** velger du **Commerce-nettprat med Omnikanal for Customer Service**-modulen, angir et navn på fragmentet og velger deretter **OK**.
1. I disposisjonsvisningen velger du sporet **Msdyn365 cs-nettpratkontakt**.
1. Følg denne fremgangsmåten i ruten **Nettprategenskaper** til høyre:

    1. I feltet **Skriptkilde** angir du den **src**-verdien du hentet fra Omnikanal for Customer Service-skriptet.
    1. I feltet **Dataapp-ID** angir du den **data-app-id**-verdien du hentet fra Omnikanal for Customer Service-skriptet.
    1. I feltet **Dataorganisasjons-ID** angir du den **data-org-id**-verdien du hentet fra Omnikanal for Customer Service-skriptet.
    1. I feltet **Nettadresse for dataorganisasjon** angir du den **data-org-url**-verdien du hentet fra Omnikanal for Customer Service-skriptet.

    ![Opprett et Commerce-nettpratmodulfragment i Commerce-områdebygger.](media/Commerce-chat-creating-new-fragment.png)

1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.
1. Gå til **Fragmenter** og åpne hodefragmentet for området.
1. I **Standardbeholder**-sporet i modulen velger du ellipsen (**…**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg moduler** velger du nettpratfragmentet du opprettet tidligere, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Legg til Commerce headquarters som en programfane for Omnikanal for Customer Service

Du kan legge til en programfane for Commerce headquarters i Omnikanal for Customer Service. Live agenter kan deretter bruke brukergrensesnittet for Omnikanal for Customer Service-agentopplevelsen for å få enkel tilgang til Dynamics 365 Commerce Customer Service-modulen som inneholder kontekstuell informasjon for kunden sammen med salgsordreinformasjonen. I tillegg kan kundeserviceagenter legge inn nye ordrer, starte returer og kontrollere ordrestatusinformasjonen.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Opprett en ny programfane som laster Commerce headquarters i en iFrame-modul 

Følg denne fremgangsmåten for å opprette en ny programfane som laster Commerce headquarters i en iFrame-modul.

1. Åpne [Power Apps Maker Portal](https://make.powerapps.com).
1. Velg **Apper** i navigasjonsruten til venstre.
1. Velg **Administrasjonssenter for Customer Service**.
1. Gå til **Agentopplevelse**.
1. Velg **Administrer** for **Programfanemaler**.
1. Opprett en ny programfane av typen **Tredjepartsnettsted**. Se [Administrer for programfanemaler](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter) for instruksjoner.
1. Under **Parametere** i **Verdi**-feltet til parameteren **Nettsted** skriver du inn følgende nettadresse, der `<YourOrganizationHeadquartersURL>` og `<LegalEntityname>` erstattes med de aktuelle verdiene. Omnikanalkundeservice leser **{AccountNumber}** fra nettpratkonteksten. La derfor **{AccountNumber}** være som den er.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. La **Verdi**-feltet for **data**-parameteren være tomt.

![Opprett en programfane i Dynamics 365 Omnikanal Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Aktiver en ny programfane for kundeagenter i Dynamics 365 Omnikanal for Customer Service

Følg denne fremgangsmåten for å aktivere en ny programfane for kundeagenter i Dynamics 365 Omnikanal for Customer Service.
    
1. Åpne [Power Apps Maker Portal](https://make.powerapps.com).
1. Velg **Apper** i navigasjonsruten til venstre.
1. Velg **Administrasjonssenter for Customer Service**.
1. Gå til **Kundeservice \> Arbeidsstrømmer**.
1. Åpne arbeidsstrømmen du har opprettet for agentene, og velg deretter **Standardøkter** under **Avanserte innstillinger**.
1. Velg **Legg til eksisterende programfane** under **Programfaner**, og legg deretter til den nye programfanen du opprettet tidligere. Dette trinnet sørger for at en programfane som laster Commerce headquarters i en iFrame-modul, vises når en agent mottar en innkommende nettpratsamtale fra netthandelsområdet.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Legge til kontekstvariabler i Dynamics 365 Omnikanal for Customer Service

Følg denne fremgangsmåten for å legge til kontekstvariabler i Dynamics 365 Omnikanal for Customer Service.

1. Åpne [Power Apps Maker Portal](https://make.powerapps.com).
1. Velg **Apper** i navigasjonsruten til venstre.
1. Velg **Administrasjonssenter for Customer Service**.
1. Gå til **Kundeservice \> Arbeidsstrømmer**.
1. Åpne arbeidsstrømmen du har opprettet for agentene, og gå til **Kontekstvariabel** under **Avanserte innstillinger**.
1. Velg **Rediger**, og legg deretter til **AccountNumber** som en kontekstvariabel av **teksttypen**. Denne variabelen vil hjelpe Commerce headquarters med å laste inn kundeinformasjon med samsvarende kontonumre.

> [!NOTE]
> Hvis du vil lese e-postadressene og navnene til de signerte brukerne fra en netthandelskanal, kan du legge til **e-post** og **navn** som kontekstvariabler av **teksttypen**, i tillegg til kontekstvariabelen **AccountNumber**.
