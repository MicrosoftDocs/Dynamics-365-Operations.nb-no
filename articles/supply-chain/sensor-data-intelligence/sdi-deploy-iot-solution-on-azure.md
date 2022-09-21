---
title: Distribuer en IoT-løsning på Azure
description: Sensordataintelligens bruker data fra observasjoner som er koblet til Microsoft Azure. Denne artikkelen beskriver hvordan du distribuerer en IoT-løsning (Tingenes Internett) i Azure-abonnementet ditt.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 284aba91aa436ed1dfc02b5a93b4358ffc518017
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428471"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Distribuer en IoT-løsning på Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensordataintelligens bruker data fra observasjoner som er koblet til Microsoft Azure. For at Azure skal kunne hente data fra sensorer og dele dataene med Dynamics 365 Supply Chain Management, må du distribuere IoT-løsningen (Tingenes Internett) i Azure-abonnementet ditt. Arkitekturdiagrammet nedenfor gir en oversikt over løsningen og komponentene.

![Arkitekturdiagram for sensordataintelligens.](media/sdi-architecture.png "Arkitekturdiagram for sensordataintelligens")

Følg denne fremgangsmåten for å distribuere de nødvendige ressursene i Azure.

1. Logg deg på Supply Chain Management som en administrator.
1. Gå til **Systemadministrasjon \> Oppsett \> Sensordataintelligens \> Distribuer og koble til Azure-ressurser** for å åpne distribusjonsveiviseren.
1. Les informasjonen på **velkomstsiden**, og velg deretter **Neste**.
1. Les informasjonen på siden **Distribuer IoT-eksempelløsningen til Azure**. Gå deretter til **Instruksjoner**, og velg **Distribuer**.
1. En ny nettleserfane åpnes, og du blir tatt til Azure-portalen for distribuering av Azure-ressurser. Hvis du blir bedt om det, kan du logge deg på ved hjelp av legitimasjonen for Azure-abonnementet ditt.
1. Velg abonnementet ditt på siden **Egendefinert distribusjon**, i **Abonnement**-feltet.
1. Under **Ressursgruppe**-feltet velger du **Opprett ny** for å opprette en ressursgruppe for Azure-komponentene du vil distribuere.
1. I rullegardinlisten som vises, i **Navn**-feltet, angir du et navn på den nye ressursgruppen (for eksempel *IoT-demo*). Velg deretter **OK**.
1. Angi følgende felter:

    - **Ressursgruppe** – Velg ressursgruppen du nettopp opprettet.
    - **Område** – Velg et område, ideelt sett området der Supply Chain Management-miljøet er distribuert. Vær oppmerksom på at Azure-områdene har forskjellige priser. Du kan vise estimerte kostnader for området ditt ved å bruke [Sensordataintelligens-priskalkulatoren](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **URL-adresse til Supply Chain Management-miljø** – Angi URL-adressen til Supply Chain Management-miljøet.
    - **Bruk eksisterende Azure IoT Hub på nytt** – La denne avmerkingsboksen stå tom.

1. Velg **Neste: Se gjennom + Opprett**.
1. På siden **Egendefinert distribusjon** bekrefter du at valideringen er bestått, og deretter velger du **Opprett**.
1. Siden **Distribusjon pågår** sporer fremdriften til distribusjonen. Distribusjonsprosessen kan ta opptil 30 minutter. Når siden **Distribusjon pågår** angir at distribusjonen er fullført, velger du koblingen for ressursgruppenavnet for å åpne en side som viser listen over ressurser som distribueres i gruppen.
1. I ressurslisten finner du posten der **Type**-feltet er satt til *Administrert ID*. I **Navn**-kolonnen velger du navnet for å åpne detaljsiden for ressursen.
1. Kopier verdien i feltet **Klient-ID** (for eksempel ved å klikke på knappen **Kopier til utklippstavlen**).
1. Gå tilbake til nettleserfanen der Supply Chain Management kjører, *men ikke lukk fanen for Azure-portalen*. Veivisersiden **Distribuer IoT-eksempelløsningen til Azure** skal fortsatt være åpen. 
1. Velg **Neste**.
1. På siden **Koble til Azure-ressurser**, i feltet **Azure AD-appklient-ID**, limer du inn verdien for **Klient-ID** som du kopierte.
1. Gå tilbake til nettleserfanen der Azure-portalen er åpen, *men ikke lukk fanen for Supply Chain Management*. Siden med detaljer for ressursen skal fortsatt være åpen.
1. Velg **Tilbake**-knappen i nettleseren for å gå tilbake til listen over ressurser i den nye ressursgruppen.
1. I ressurslisten finner du posten der **Type**-feltet er satt til *Azure-buffer for Redis*. I **Navn**-kolonnen velger du navnet for å åpne detaljsiden for ressursen.
1. Velg **Tilgangsnøkler** i navigasjonsruten til venstre.
1. På siden **Tilgangsnøkler** kopierer du verdien som vises for **Primær tilkoblingsstreng (StackExchange.Redis)** (for eksempel ved å velge knappen **Kopier til utklippstavlen**).
1. Gå tilbake til nettleserfanen der Supply Chain Management kjører. Siden **Koble til Azure-ressurser** skal fremdeles være åpen.
1. I feltet **Tilkoblingsstreng for metrisk lagring av Redis** limer du inn verdien for **Primær tilkoblingsstreng (StackExchange.Redis)** som du kopierte.
1. Velg **Fullfør**.

Azure-ressurser for Sensordataintelligens distribueres nå i Azure-abonnementet ditt.

> [!NOTE]
> Du kan når som helst vise eller redigere tilkoblingsinformasjonen som er lagret i Supply Chain Management, ved å åpne siden **Parametere for sensordataintelligens**. For mer informasjon, se [Parametere for sensordataintelligens](sdi-parameters.md).
