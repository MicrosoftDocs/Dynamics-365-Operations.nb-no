---
title: Avanserte innstillinger for Invoice Capture-løsning
description: Denne artikkelen gir informasjon om avanserte innstillinger i Invoice capture-løsningen.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691200"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Avanserte innstillinger for Invoice Capture-løsning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen gir informasjon om avanserte innstillinger i Invoice capture-løsningen.

## <a name="create-additional-connections-for-channels"></a>Opprette flere tilkoblinger for kanaler

Du må opprette tilkoblinger til e-post eller fillagring for å aktivere overvåking av innkommende fakturaer fra ulike kanaler. Du må registrere tilkoblinger i begynnelsen for å gi tilgang til automatiserte flyter som brukes i løsningen.

Følgende tilkoblingstyper brukes til å importere fakturaer:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Kanalen for fakturaimport vil bruke tilkoblingene i ytterligere konfigurasjonstrinn. Før brukere kan opprette en kanal for en bestemt tilkobling, må **Administrator**-sikkerhetsrollen gis til dem, og de må opprette tilkoblinger.

Hvis du vil opprette tilkobling til Microsoft Dataverse, følger du disse trinnene.

1. Gå til **Administrasjonssystem \> Standardløsning**.
2. Velg **Ny**, og velg deretter **Tilkoblingsreferanse**.
3. I **Visningsnavn**-feltet angir du et navn.
4. Velg **Microsoft Dataverse** som tilkobling.
5. Hvis du konfigurerer tilkoblingen for første gang, velger du **Ny tilkobling**.
6. I dialogboksen som vises, oppretter du en Dataverse-tilkobling, og deretter velger du **Opprett**.
7. Angi Dataverse-kontoen og -passordet.
8. Når valideringen er bestått, kan du gå til tilkoblingssiden, velge **Oppdater**, velge kontoen og deretter velge **Opprett**.

Hvis du vil opprette en e-post- eller fillagringstilkobling, følger du disse trinnene.

1. På siden **Tilkoblingsoppretting** i feltet **Tilkoblingstype** velger du **Office 365 Outlook**.
2. For en e-posttilkobling kan du velge **Outlook.com** eller **Office 365 Outlook** som tilkobling. For en fillagringstilkobling kan du velge **OneDrive** eller **SharePoint**.

Hvis du vil se gjennom eksisterende tilkoblinger, kan du gå til **Standardløsning \> Objekter \> Tilkoblingsreferanser**. Brukeren som oppretter kanaler, bør ha minst én Dataverse-tilkobling i tillegg til bestemte e-post- eller fillagringstilkoblinger. Oppretteren av den nye kanalen må være eier av tilkoblingen.
