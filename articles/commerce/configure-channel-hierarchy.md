---
title: Konfigurere en kanal for å bruke et kanalnavigasjonshierarki
description: Denne artikkelen beskriver hvordan du konfigurerer en kanal for å bruke et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: b15e6eee86880f0315f42b34056385f718cc6bf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280400"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Konfigurere en kanal for å bruke et kanalnavigasjonshierarki


[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer en kanal for å bruke et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Kanalnavigeringshierarkier organiserer produkter i kategorier, slik at produktene kan blas gjennom på et e-handelsområde eller på salgsstedet. Detaljhandels- og nettkanaler må konfigureres med kanalnavigeringshierarkier.

## <a name="configure-the-channel"></a>Konfigurere kanalen

Følg denne fremgangsmåten for å konfigurere en kanal for å bruke et kanalnavigasjonshierarki:

1. I navigasjonsruten går du til **Moduler \> Retail og Commerce \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg kanalen skal konfigureres.
1. I handlingsruten velger du **Angi attributtmetadata**.
1. I rullegardinlisten **Kategorihierarki** velger du aktuelt kanalnavigeringshierarki.
1. Velg **Lagre** i handlingsruten.
1. Under **Attributtgruppe** legger du til eventuelle attributtgrupper som skal være globale attributter for alle noder.

Følgende bilde viser hvordan du konfigurerer en kanal for å bruke et kanalnavigasjonshierarki:

![Eksempel på kanalkonfigurasjon.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Angi attributtmetadata

Ved å angi attributtmetadataene kan du konfigurere attributter for hver node.

Gjør følgende for å konfigurere attributtmetadata.

1. I handlingsruten velger du **Angi attributtmetadata**.
1. For hver node velger du **Kanalproduktattributter**.
1. Sett **Vis attributter i kanal** til **Ja** og **Kan justeres** til **Ja** for å aktivere presiseringer i denne kanalen.
1. Når du har konfigurert hver node slik du ønsker, velger du **Lagre**-knappen i **handlingsruten** for å lagre.
1. Velg **X** i øvre høyre hjørne for å avslutte dette skjermbildet og tilbake til siden **Kanalkategorier og produktattributter**.

Følgende bilde viser et eksempelsett med kanalproduktattributter konfigurert på en kanalkategorinode.

![Kanalattributter på en kanalkategorinode.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Publiser endringer

Før endringene kan tre i kraft, må du publisere endringene.

Hvis du vil publisere endringer, gjør du følgende.

1. Velg **Publiser kanaloppdateringer** i handlingsruten.
1. Velg **OK** i **Publiser kanaloppdateringer**.

Bildet nedenfor viser hvordan du publiserer kanaloppdateringer.

![Publiser kanaloppdateringer.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Opprett et hierarki for kanalnavigasjon](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
