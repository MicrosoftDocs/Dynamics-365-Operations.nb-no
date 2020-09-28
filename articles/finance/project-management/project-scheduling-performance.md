---
title: Ytelse for planlegging av prosjektressurs
description: Dette emnet inneholder informasjon om hvordan du kan forbedre ytelsen til ressursplanlegging for et stort antall prosjekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760629"
---
# <a name="project-resource-scheduling-performance"></a>Ytelse for planlegging av prosjektressurs

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Det kan oppstå ytelsesproblemer knyttet til ressursplanlegging når antall prosjekter blir tusenvis. Hvis du vil forbedre ressursplanleggingsytelsen, finnes det en funksjon som gjør det mulig for brukere å redusere tiden det tar å starte ressurstilgjengelighetsskjemaet. Dette fjerner mer spesifikt den oppsamlede synkroniseringsprosessen for ressurskapasitet og bruker tabellen **ResProjectResource** til å øke hastigheten på ressursoppslaget. Merk at tabellen **ResRollup** ikke lenger vil bli brukt.

> [!IMPORTANT]
> Hvis det finnes en avhengighet av den oppsamlede synkroniseringsprosessen for ressurskapasitet eller tabellen **ResProjectResource**, må du ikke bruke denne funksjonen.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktiver ytelsesforbedring for ressursplanlegging
Fullfør trinnene nedenfor for å aktivere ytelsesforbedring for ressursplanlegging.

1. Gå til **Funksjonsbehandling** > **Alle**, og i funksjonslisten finner du **funksjonen Aktiver ytelsesforbedring for prosjektressursplanlegging** .
2. Velg **Aktiver nå**.

> [!NOTE]
> Hvis du ikke finner funksjonen i listen, velger du **Se etter oppdateringer** for å oppdatere listen.

3. Oppdater nettleseren, og gå deretter til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Synkroniser kapasitet for ressurskalendere på tvers av alle firmaer**.
4. Sett **Fjern eksisterende kapasitetsposter** til **Ja** for å fjerne tidligere data. Hvis du vil generere trinnvise data, seter du verdien til **Nei**.
5. I feltet **Periodekode** velger du perioden det skal genereres data i. Hvis du velger en periodekode, trenger du ikke å definere en start- og sluttdato.
6. Hvis du lar feltet **Periodekode** stå tomt, må du velge bestemte start- og sluttdatoer for å generere data.
7. Velg **OK**.

 > [!NOTE]
 > Dette distribuerer generelle data til tabellen **ResCalendarCapacity** på tvers av alle firmaer i miljøet, så den satsvise jobben må bare kjøres i én juridisk enhet. Dataene i denne satsvise jobben er nødvendige for å beregne ressurskapasitet via den tilknyttede kalenderen.

8. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Fyll ut prosjektressurser på tvers av alle firmaer** og velg deretter **OK**. Dette er dataoppgraderingsskriptet for generelle data i tabellene **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**. Verdiene for feltet **PSAPRojSchedRole.RootActivity** oppdateres også. Hvis dette ikke kjøres, vil du få en advarsel når du prøver å utføre ressursplanleggingsoperasjoner.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Deaktiver ytelsesforbedring for ressursplanlegging

1. Gå til **Funksjonsbehandling** > **Alle** og søk etter **funksjonen Aktiver ytelsesforbedring for prosjektressursplanlegging** .
2. Velg funksjonen, og velg deretter **Deaktiver**.
3. Oppdater nettleseren.
4. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Kapasitetsynkronisering** > **Synkroniser opprullinger av ressurskapasitet**.
5. På siden **Synkronisering av opprulling av kapasitet** setter du **Fjern eksisterende kapasitetsposter** til **Ja** for å fjerne tidligere data. Hvis du vil generere trinnvise data, seter du verdien til **Nei**.
6. I feltet **Periodekode** velger du perioden det skal genereres data i. Hvis du velger en periodekode, trenger du ikke å definere en start- og sluttdato.
7. Hvis du lar feltet **Periodekode** stå tomt, må du velge bestemte start- og sluttdatoer for å generere data.
8. Velg **OK**.

> [!NOTE]
> Dette distribuerer generelle data til tabellen **ResRollup** på tvers av alle firmaer i miljøet, så den satsvise jobben må bare kjøres i én juridisk enhet. Denne satsvise jobben er nødvendig for alle visninge av typen **Ressurstilgjengelighet**. Hvis denne satsvise jobben ikke kjøres, vil **ResRollup-** dataene bli generert direkte, noe som kan ta tid.
