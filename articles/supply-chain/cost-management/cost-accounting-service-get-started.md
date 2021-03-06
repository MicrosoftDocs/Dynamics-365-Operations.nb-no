---
title: Komme i gang med kostnadsregnskaptjenesten (privat forhåndsversjon)
description: Dette emnet inneholder lisensdetaljer og installasjonsinstruksjoner for tjenesten for kostnadsregnskap.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: b6756e3745aa4596bd5d63ad15aaf4385cfc4813
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813201"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Komme i gang med kostnadsregnskaptjenesten (privat forhåndsversjon)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Funksjonaliteten som er nevnt i dette emnet, er tilgjengelige som en del av en privat forhåndsversjon. Innholdet i dette emnet og funksjonaliteten det beskriver, kan endres. Hvis du vil ha mer informasjon om forhåndsvisning versjoner, kan du se [Vanlige spørsmål om oppdatering av én versjonstjeneste](../../fin-ops-core/fin-ops/get-started/one-version.md).

Ved hjelp av tjenesten for kostnadsberegning kan du utføre flere lagerregnskapsforekomster i kostnadsregnskapsfinansene du har definert. Du knytter hver kostnadsregnskapsfinans til en *konvensjon*. En konvensjon er en samling av følgende typer regnskapspolicyer:

- Kostnadsobjekt
- Målingsgrunnlag for inndata
- Kostnadsflytforutsetning
- Kostnadselement

> [!NOTE]
> Selv etter at du har aktivert tjenesten for kostnadsregnskap, kan du fremdeles utføre lagerregnskap i Microsoft Dynamics 365 Supply Chain Management, som vanlig.

Kostregnskapstjenesten er et tillegg. Hvis du vil gjøre funksjonene tilgjengelige, må du installere det fra Microsoft Dynamics Lifecycle Services (LCS). Derfor kan du velge å evaluere den i et testmiljø før du aktiverer den for produksjonsmiljøer.

Tjenesten for kostnadsregnskap støtter for øyeblikket ikke alle funksjonene for kostnadsstyring som er innebygd i Dynamics 365 Supply Chain Management. Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig, oppfyller kravene dine.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Få tilgang til kostnadsregnskaptjenesten (privat forhåndsversjon)

> [!IMPORTANT]
> Hvis du vil bruke tjenesten for kostnadsregnskap, må du ha et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø), og du må kjøre Dynamics 365 Supply Chain Management versjon 10.0.11 eller senere.

Hvis du vil registrere deg for den private forhåndsversjonen av kostregnskapstjenesten, kan du sende ID-en din for LCS-miljø via e-post til [Kostnadsregnskaptjeneste (privat forhåndsversjon)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Når du er godkjent for programmet, sender vi deg en oppfølging via e-post som inneholder en betanøkkel for kostnadsregnskapstjenesten. Når du mottar betanøkkelen, kan du fortsette ved å [installere tillegget](#install).

## <a name="licensing"></a>Lisensiering

Kostregnskap-tjenesten lisensieres sammen med standardfunksjonene for lagerregnskap som er tilgjengelig for Supply Chain Management. Du trenger ikke kjøpe en tilleggslisens for å bruke tjenesten for kostnadsregnskap.

## <a name="install-the-add-in"></a><a name="install"></a>Installer tillegget

Hvis du vil bruke kostregnskap-tjenesten, kan du installere tillegget Supply Chain Management, som beskrevet i fremgangsmåten nedenfor.

1. [Registrer deg](#sign-up) for kostnadsregnskaptjenesten (privat forhåndsversjon).

1. Logg på LCS.

1. Gå til **Administrasjon av forhåndsvisningsfunksjoner**.

1. Velg plusstegnet (**+**).

1. I **Kode** -feltet angir du betanøkkelen for tillegget for kostregnskap-tjenesten. (Du burde ha mottatt nøkkelen via e-post.)

1. Velg **Fjern blokkering**.

1. Åpne LCS-miljøet der du vil legge til tjenesten.

1. Gå til **Detaljerte opplysninger**.

1. Bla ned til **Miljøtillegg**-hurtigfanen.

1. Velg **Installer et nytt tillegg**.

1. Velg **Tjeneste for kostnadsregnskap**.

1. Følg installasjonsveiledningen, og godta vilkårene.

1. Velg **Installer**.

1. I hurtigfanen **Miljøtillegg** skal du se at tjenesten for kostnadsregnskap blir installert. Etter noen minutter skal statusen endres fra **Installerer** til **Installert**. (Det kan hende du må oppdatere siden for å se denne endringen.) På dette tidspunktet er tjenesten for kostnadsregnskap klar til bruk.

## <a name="set-up-the-integration"></a>Defininere integreringen

Slik definerer du integreringen mellom kostregnskap-tjenesten og Dynamics 365 Supply Chain Management:

1. Gå til **Systemadministrasjon > Funksjonsbehandling**.

1. Velg **Se etter oppdateringer**.

1. Åpne fanen **Alle**, og søk etter funksjonen kalt *Tjeneste for kostnadsregnskap*.

1. Velg **Aktiver nå**.

1. Gå til **Kostnadsstyring > Tjeneste for kostnadsregnskap > Oppsett > Parametere for tjeneste for kostnadsregnskap > Integrasjonsparametere**.

1. I feltet **Program-ID** angir du følgende kode:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. I feltet **Datatjenesteendepunkt** angir du følgende URL-adresse:<br>https://operationsdataservice.operations365.dynamics.com/

1. I feltet **Endepunkt for tjeneste for kostnadsregnskap** angir du følgende URL-adresse:<br>https://costaccountingservice.operations365.dynamics.com/

1. Kostregnskap-tjenesten er nå klar for bruk.

## <a name="related-resources"></a>Relaterte ressurser

[Startside for tjeneste for kostnadsregnskap](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]