---
title: Oppdateringssporing for plassering
description: Dette emnet beskriver hvordan du definerer og kjører oppdateringssporingen for å plassere periodiske oppgave.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d8e2a42d8e12a5a9cf18e876b6f9e45ecb877881
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500029"
---
# <a name="update-tracking-for-put-away"></a>Oppdateringssporing for plassering

[!include [banner](../includes/banner.md)]

Den periodiske oppgaven *Oppdateringssporing for plassering* er utformet for å kjøres som en regelmessig satsvis jobb hver natt. Den identifiserer hvilke reiser som har mottatt alle lagertransaksjonene, og hvilke reiser som ikke har noen verdi for den faktiske sluttdatoen. Deretter settes den faktiske sluttdatoen til gjeldende dato etter behov.

*Containeraktiviteter* opprettes for hver *etappe* i reisen for hver *forsendelsescontainer*. Disse verdiene defineres av reisemalen som velges når det opprettes en reise. For hver post for containeraktiviteter kan det angis verdier for feltene **Startdato**, **Forventet sluttdato** og **Faktisk sluttdato**. Disse feltene kan oppdateres når bekreftelse er mottatt om at en etappe har begynt eller er fullført.

Informasjon som er relatert til bekreftede datoer, gis vanligvis av en tredjepart, for eksempel en speditør, fordi disse handlingene opprettholdes utenfor Microsoft Dynamics 365 Supply Chain Management. Informasjon fra en tredjepart er imidlertid ikke påkrevd for å spore ankomsten av varer fra en reiseetappe inn i lageret (som merket av plasseringen av varer). Sporing kan derfor bestemmes på grunnlag av informasjon i Dynamics 365 Supply Chain Management.

Følge denne fremgangsmåten for å definerer og kjører den periodiske oppgaven *Oppdateringssporing for plassering*.

1. Gå til **Netto innkjøpspris \> Periodiske oppgaver \> Oppdateringssporing for plassering**.
1. Angi følgende felter i **Parametere**-delen i dialogboksen **Oppdateringssporing for plassering**:

    - **Etappe** – Velg det unike identifikasjonsnavnet/-nummeret for den delen av en reise som du vil oppdatere sporing for. Den valgte verdien må representere ankomsten av reisen på lageret.
    - **Aktivitet** – Velg aktiviteten som ble påtatt i løpet av den valgte etappen. Disse verdiene tilordnes per arbeidsflytmallinje i sporingskontrollsenteret.

1. Hvis du vil begrense settet med poster som skal være med i oppdateringen, velger du **Filter**-knappen i hurtigfanen **Poster som skal inkluderes**. Det vises en standard dialogboks for spørring der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Supply Chain Management. Feltene her er skrivebeskyttet, og viser verdier som er knyttet til spørringen.
1. Konfigurer alternativer for satsvise jobber og planlegging etter behov i hurtigfanen **Kjør i bakgrunnen**, slik du kan gjøre for andre typer jobber i Supply Chain Management.
1. Velg **OK** for å bruke innstillingene og til å kjøre eller planlegge oppdateringen.
