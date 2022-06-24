---
title: Flytt NF-e XML-filer som vedlegg
description: Denne artikkelen beskriver hvordan du flytter NF-e XML-filer ut av Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-databasen og gjør dem tilgjengelige som vedlegg i stedet.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877904"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Flytt NF-e XML-filer som vedlegg

[!include [banner](../includes/banner.md)] 


Når elektroniske regnskapsdokumenter (NF-e) utstedes, opprettes og lagres XML-filer i Microsoft Dynamics 365 Finance- og Dynamics 365 Supply Chain Management-databaser. I Brasil kan du bruke funksjonen **Flytt NF-e XML som vedlegg** til å frigjøre databaseområdet som disse XML-filene forbruker.

Når det gjelder etablering av et bestemt datointervall og regnskap, flytter funksjonen NF-e XML-filene fra Finance- eller Supply Chain Management-databasen til Blob Storage fra Azure-abonnementet ditt. Denne flyttingen gjør at filene bare er tilgjengelige som vedlegg. Når XML-filene har blitt flyttet til Blob Storage, slettes de opprinnelige filene fra Finance- eller Supply Chain Management-databasen. Derfor frigjøres databaseområdet der disse filene brukes.

Følg denne fremgangsmåten for å aktivere funksjonen **Flytt NF-e XML som vedlegg**.

1. Åpne arbeidsområdet **Funksjonsbehandling** i Finance eller Supply Chain Management.
2. På **Alle**-fanen søker du etter og velger funksjonen **Flytt NF-e XML som vedlegg**.
3. Velg **Aktiver nå**.

Følg denne fremgangsmåten for å flytte NF-e XML-filer som vedlegg.

1. Gå til **Kunder** \> **Regnskapsdokumenter** \> **Elektroniske regnskapsdokumenter** \> **Flytt NF-e XML som vedlegg**.
2. Velg start- og sluttdato i feltene **Fra dato** og **Til dato**.
3. Angi en verdi i feltet **Regnskapsfirma-ID**.
4. Velg **OK**.

> [!IMPORTANT]
> Prosessen er ikke reversibel. Når du har flyttet NF-e XML-filene , kan brukerne bare vise dem ved å velge **Vedlegg** øverst på siden **Regnskapsdokument**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
