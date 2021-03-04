---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en dobbel skriving-tilkobling mellom et nytt Finance and Operations-miljø og et nytt Dataverse-miljø fra Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683531"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Oppsett av dobbel skriving fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet forklarer hvordan du konfigurerer en dobbel skriving-tilkobling mellom et nytt Finance and Operations-miljø og et nytt Dataverse-miljø fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forutsetninger

Du må være administrator for å kunne konfigurere en tilkobling med dobbel skriving.

+ Du må ha tilgang til leieren.
+ Du må være administrator i både Finance and Operations-miljøer og Dataverse-miljøer.

## <a name="set-up-a-dual-write-connection"></a>Konfigurere en tilkobling med dobbel skriving

Hvis du vil konfigurere en tilkobling med dobbel skriving, gjør du følgende.

1. Gå til prosjektet I LCS.
2. Velg **Konfigurer** for å distribuere et nytt miljø.
3. Velg versjonen. 
4. Velg topologien. Hvis bare én topologi er tilgjengelig, velges den automatisk.
5. Fullfør de første trinnene i veiviseren for **distribusjonsinnstillinger**.
6. Følg deretter at av disse trinnene i fanen **Dataverse**:

    - Hvis et Dataverse-miljø allerede er klargjort for leieren, kan du velge det.

        1. Sett alternativet **Konfigurere Dataverse** til **Ja**.
        2. I feltet **tilgjengelige miljøer** velger du miljøet som skal integreres med Finance and Operations-dataene. Listen inneholder alle miljøer der du har administrative rettigheter.
        3. Merk av for **Godta** for å angi at du godtar vilkårene og betingelsene.

        ![Dataverse-fanen når et Dataverse-miljø allerede er klargjort for leieren](../dual-write/media/lcs_setup_1.png)

    - Hvis leieren ikke allerede har et Dataverse-miljø, blir et nytt miljø klargjort.

        1. Sett alternativet **Konfigurere Dataverse** til **Ja**.
        2. Skriv inn et navn for Dataverse-miljøet.
        3. Velg regionen som miljøet skal distribueres i.
        4. Velg standard språk og valuta for miljøet.

            > [!NOTE]
            > Du kan ikke endre språket og valutaen senere.

        5. Merk av for **Godta** for å angi at du godtar vilkårene og betingelsene.

        ![Dataverse-kategorien når leieren ikke allerede har et Dataverse-miljø](../dual-write/media/lcs_setup_2.png)

7. Fullfør resten av trinnene i veiviseren for **Distribusjonsinnstillinger**.
8. Når miljøet har statusen **Distribuert**, åpner du siden for miljødetaljer. Delen **Dataverse-miljøinformasjon** viser navnene på Finance and Operations-miljøet og Dataverse-miljøet som er koblet.

    ![Delen Dataverse-miljøinformasjon](../dual-write/media/lcs_setup_3.png)

9. En administrator av Finance and Operations-miljøet må logge på LCS og velge **Kobling til CDS for apper** for å fullføre koblingen. Siden for miljødetaljer viser administratorens kontaktinformasjon.

    Når koblingen er fullført, oppdateres statusen til **Miljøkoblingen er fullført**.

10. Hvis du vil åpne arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet og kontrollere hvilke maler som er tilgjengelige, velger du **Kobling til CDS for apper**.

    ![Knappen Kobling til CDS for apper i delen Dataverse-miljøinformasjon](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Du kan ikke koble fra miljøer ved hjelp av LCS. Hvis du vil oppheve koblingen til et miljø, åpner du arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet, og deretter velger du **Koble fra**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]