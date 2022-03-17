---
title: Fullføre, publisere og rulle ut en globaliseringsfunksjon
description: Dette emnet inneholder informasjon om livssyklusen for globaliseringsfunksjoner.
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
ms.openlocfilehash: a842a3ba31c0a8e0d80ad1856d9d6d861a8514ea
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371663"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Fullføre, publisere og rulle ut en globaliseringsfunksjon

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Versjoner av funksjonen for elektronisk fakturering

Funksjoner for elektronisk fakturering er versjonsstyrt. Når det opprettes en ny versjon, økes versjonsnummeret automatisk.

Funksjonsversjoner av elektronisk fakturering følger en livssyklus med opptil tre statuser:

- **Utkast** – Når en funksjonsversjon har denne statusen, kan du redigere konfigurasjonsattributtene og alle artefaktene (for eksempel filformatkonfigurasjoner).
- **Fullført** – Denne statusen angir at du er ferdig å redigere funksjonsversjonen og ikke har tenkt å gjøre flere oppdateringer av den. Når en funksjonsversjon har denne statusen, kan du ikke lenger redigere den eller noen av komponentene dens.
- **Publisert** – Denne statusen angir at funksjonsversjonen er publisert i det globale repositoriet som er knyttet til organisasjonen. Når en funksjonsversjon har denne statusen, kan du ikke lenger redigere den eller noen av komponentene dens.

Du kan angi en **Gyldig fra**-dato for en ny versjon av en funksjon for elektronisk fakturering. Du kan dermed definere en standardversjon som kan brukes, eller som kan skrives over når funksjonen rulles ut til tjenestemiljøet.

Hvis du vil endre statusen for en versjon av en funksjon for elektronisk fakturering, følger du disse trinnene.

1. Logg deg på kontoen for Regulatory Configuration Service (RCS).
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
3. Velg funksjonen for elektronisk fakturering på venstre side på siden **Funksjoner for elektronisk fakturering**.
4. Velg versjonen i **Versjoner**-fanen til høyre på siden.
5. Velg **Endre status**, og velg deretter **Fullført** (hvis nåværende status er **Utkast**) eller **Publisert** (hvis nåværende status er **Fullført**).
6. Velg **Ja** i meldingsboksen for å bekrefte forespørselen.

Den manuelle endringen fra statusen **Fullført** til statusen **Publisert** er valgfri. Versjoner av funksjonen for elektronisk fakturering oppdateres automatisk til statusen **Publisert** når de rulles ut til tjenestemiljøet.

Du kan spore statusen i kolonnen **Funksjonsversjonsstatus** i **Versjoner**-fanen.

## <a name="deploy-feature-versions"></a>Rulle ut funksjonsversjoner

I RCS bruker du kommandoen **Distribuer** til å publisere en versjon av en funksjon for elektronisk fakturering i måltjenestemiljøet eller det tilkoblede programmet.

1. Velg funksjonen for elektronisk fakturering på venstre side på siden **Funksjoner for elektronisk fakturering**.
2. I **Versjoner**-fanen til høyre på siden velger du versjonen av funksjonen for elektronisk fakturering du vil rulle ut til tjenestemiljøet eller det tilkoblede programmet. Den valgte versjonen må ha statusen **Fullført** eller **Publisert**.
3. Velg **Distribuer**, og velg deretter ett eller begge av følgende alternativer for å definere målet for distribusjonen:

    - **Tilkoblet program** – Konfigurasjonen som leveres av programoppsettet, er skrevet i forekomsten av Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management som tidligere var tilknyttet den.
    - **Tjenestemiljø** – Versjonen av funksjonen for elektronisk fakturering distribueres til tjenestemiljøet. Elektronisk fakturering er da klar til å motta og behandle elektroniske dokumenter som Finance eller Supply Chain Management sender.

> [!NOTE]
> Du endrer vanligvis parameterne for ER-funksjonen (elektronisk fakturering) som må rulles ut til tjenestemiljøet. Det blir sjelden endringer av det tilkoblede programmet. Du bør bare rulle ut nye versjoner til det tilkoblede programmet når du endrer de tilsvarende parameterne for programmet.

Du kan finne ut om en bestemt versjon av en funksjon for elektronisk fakturering er rullet ut til et bestemt miljø, ved å gå gjennom informasjonen i **Miljøer**-fanen.

## <a name="remove-feature-versions"></a>Fjerne funksjonsversjoner

I RCS kan du velge **Avbryt** for å fjerne en bestemt versjon av funksjonen for elektronisk fakturering fra et tjenestemiljø hvis den ble rullet ut der.

> [!IMPORTANT]
> **Avbryt**-knappen fungerer bare for tjenestemiljøer. Den fjerner ikke noe fra det tilkoblede programmet for den gjeldende funksjonen for elektronisk fakturering.

## <a name="rebase-electronic-invoicing-features"></a>Rebasere funksjoner for elektronisk fakturering

Når én funksjon for elektronisk fakturering er avledet fra en annen, kan du velge **Rebaser** for å oppdatere den avledede funksjonen med endringene som er gjort i den opprinnelige (overordnede) funksjonen.

Følg denne fremgangsmåten hvis du vil rebasere en avledet versjon av en funksjon du har opprettet.

1. Hent den nyeste versjonen av funksjonen ved å importere den fra det globale repositoriet. Hvis du vil ha mer informasjon, kan du se [Importer funksjon fra globalt repositorium](e-invoicing-import-feature-global-repository.md).
2. I listen over funksjoner velger du funksjonen som skal rebaseres.
3. I **Versjon**-fanen velger du **Ny** for å opprette en utkastversjon.
4. Velg **Rebaser**.
5. I dialogboksen **Rebaser** velger du versjonen av funksjonen du vil rebasere til.
6. Velg **OK**.
7. Se gjennom funksjonskomponentene, og foreta eventuelle endringer etter behov.
8. Velg **Endre status** for å fullføre den rebaserte funksjonen. Når rebaseringen er fullført, kan du utføre flere handlinger.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Få en bestemt versjon av funksjoner for elektronisk fakturering

Når du oppretter en ny versjon av en funksjon for elektronisk fakturering, oppretter systemet en kopi av den nyeste funksjonsversjonen. Hvis du vil bruke en tidligere versjon av funksjonen som basis for en ny versjon, velger du versjonen, og deretter velger du **Hent denne versjonen**. Det opprettes en ny utkastversjon av funksjonen som er en kopi av den valgte versjonen.
