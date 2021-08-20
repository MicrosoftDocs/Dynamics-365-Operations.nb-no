---
title: Funksjonen Opprett en ny elektronisk fakturering
description: Dette emnet beskriver hvordan du oppretter en ny funksjon for elektronisk fakturering når ingen konfigurerbar funksjon er tilgjengelig for landet eller området ditt som standard.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744941"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Funksjonen Opprett en ny elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny funksjon for elektronisk fakturering når ingen konfigurerbar funksjon er tilgjengelig for landet eller området ditt som standard.

Fullfør disse oppgavene for å opprette en ny funksjon for elektronisk fakturering:

1. Opprett en ny filformatkonfigurasjon ved å bruke fakturamodellkonfigurasjonen som følger med, og dra nytte av den eksisterende fakturatilordningen for funksjonen du vil opprette.
2. Legg til filformatkonfigurasjoner i funksjonskonfigurasjonene for elektronisk fakturering.
3. Opprett oppsettet for elektronisk faktureringsfunksjon.
4. Fullfør den nye funksjonen for elektronisk fakturering, og publiser den i det globale repositoriet for organisasjonen.
5. Distribuere den nye funksjonen for elektronisk fakturering til servicemiljø.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Opprett nye filformatkonfigurasjoner som er avledet fra den eksisterende fakturamodellen

I denne fremgangsmåten oppretter du filformatkonfigurasjonene som kreves for den nye funksjonen for elektronisk fakturering du vil opprette. Du kan opprette den elektroniske fakturafilformatkonfigurasjonen og alle andre filformatkonfigurasjoner som den nye funksjonen for elektronisk fakturering kan kreve.

Før du begynner denne fremgangsmåten, må du logge deg på RCS-kontoen (Regulatory Configuration Service).

1. I Microsoft Dynamics 365 Finance, i arbeidsområdet **Elektronisk rapportering** velger du **Repositorier** for konfigurasjonsleverandøren **Microsoft**.
2. Velg **Global**, velg **Åpne**, og velg deretter **Fakturamodell**-konfigurasjonen i venstre rute.

    > [!IMPORTANT]
    > For Brasil velger du i stedet modellkonfigurasjonen **Regnskapsdokumenter**.

3. Velg **Importer** i fanen **Konfigurasjoner**.
4. Lukk siden.
5. Lukk siden.
6. Velg flisen **Rapporteringskonfigurasjoner**, og velg deretter fakturamodellen du importerte.
7. Velg **Opprett konfigurasjon**, og velg deretter **Format basert på fakturakontekstmodell**.
8. Angi et navn og en beskrivelse for formatkonfigurasjonen.
9. Velg filutvidelsestypen i **Formattype**-feltet.
10. Velg **Opprett konfigurasjon** og velg deretter formatkonfigurasjonen du opprettet.
11. Velg **Utforming**, og bruk verktøyet for formatdesigner til å konfigurere filoppsettet slik at det oppfyller filformatspesifikasjonene.
12. Lukk siden.
13. I fanen **Versjoner** velger du **Endre status** \> **Fullfør**.
14. Velg **Endre status** \> **Del** for å publisere formatkonfigurasjonen i det globale repositoriet.

Den nye filformatkonfigurasjonen må deles med Microsoft-domenet før konfigurasjonen kan forbrukes av tjenesten for elektronisk fakturering.

1. Velg formatkonfigurasjonen du arbeider på. Statusen til konfigurasjonen må være **Delt**.
2. Velg **Avansert deling** \> **Globalt repositorium** i fanen **Versjoner**.
3. I fanen **Delt med** velger du **Organisasjon**.
4. I **Parametere**-feltet angir du **Microsoft.com** for å dele formatkonfigurasjonen med Microsoft-domenet.
5. Velg **OK**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Opprett den nye elektronisk faktureringsfunksjonen

1. I RCS i arbeidsområdet **Globaliseringsfunksjoner**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
2. Velg **Legg til**, og velg deretter **Ny funksjon**.
3. Angi et navn og en beskrivelse for den nye elektroniske faktureringsfunksjonen.
4. Velg **Opprett funksjon**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Legg til funksjonskonfigurasjoner for Elektronisk fakturering

1. Velg funksjonen for Elektronisk fakturering som du arbeider på.
2. I **Konfigurasjoner**-fanen velger du **Legg til**.
3. I **Konfigurasjoner**-rutenettet kan du bla gjennom og velge filformatkonfigurasjoner som funksjonen for elektronisk fakturering kan kreve for å generere filen for elektronisk faktura.
4. Velg **OK**.

## <a name="add-electronic-invoicing-feature-setups"></a>Legg til oppsett for funksjon for Elektronisk fakturering

1. Velg **Legg til** og velg deretter **Egendefinert oppsett** i fanen **Oppsett**.
2. Angi et navn og en beskrivelse for funksjonsoppsett.
3. Velg **Behandlingsforløp** i **Oppsetttype**-feltet.
4. Velg **Opprett**.
5. Velg oppsettet du arbeider på, og velg deretter **Rediger**.
6. Velg **Ny** i kategorien **Behandlingsforløp** for å legge til en forløpshandling. Hvis du vil ha mer informasjon om forløp, kan du se [Handlinger](e-invoicing-configuration-rcs.md#actions).
7. På fanen **Relevansregler** velger du **Ny** for å legge til setninger for relevansregler. Hvis du vil ha mer informasjon om relevansregler, kan du se [Relevansregler](e-invoicing-configuration-rcs.md#applicability-rules).
8. Velg **Ny** i fanen **Variabler** for å legge til variabler etter behov.
9. Velg **Lagre** og velg deretter **Valider** for å kontrollere konsekvensen til konfigurasjonen.
10. Lukk siden.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Distribuer funksjonen for elektronisk fakturering til servicemiljø

Hvis du vil ha mer informasjon om hvordan du fullfører denne oppgaven, kan du se [Distribuer funksjonen for elektronisk fakturering til servicemiljø](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Distribuer funksjonen for elektronisk fakturering til et tilkoblet program

Hvis du vil ha mer informasjon om hvordan du fullfører denne oppgaven, kan du se [Konfigurer programoppsettet](e-invoicing-get-started.md#configure-the-application-setup) og [Distribuer funksjonen for elektronisk fakturering til tilkoblet program](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
