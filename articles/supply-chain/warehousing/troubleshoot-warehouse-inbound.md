---
title: Feilsøke innkommende lageroperasjoner
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920993"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Feilsøke innkommende lageroperasjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Jeg får følgende feilmelding: Kvalitetsordre %1 er generert. Finner ikke gruppeprofil. Kontroller konfigurasjonen.

### <a name="issue-description"></a>Problembeskrivelse

Denne feilmeldingen er knyttet til en mottaksprosess der kvalitetsstyring (QMS) er aktivert. Avhengig av konfigurasjonene i miljøet ditt kan flere detaljer om transaksjonen som genererer feilmeldingen, hjelpe deg med å løse problemet.

### <a name="issue-resolution"></a>Problemløsning

Først kontrollerer du konfigurasjonen for [gruppeplukking](set-up-cluster-picking.md) og kontrollerer at gruppeprofilene er riktig konfigurert. Du kan ikke bruke et menyelement på mobilenheten for gruppeplukking med mindre gruppeprofiler er konfigurert. Avhengig av miljøet kan det være at du også må se gjennom andre tilknyttede konfigurasjoner.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Mottak av kombinerte nummerskilter virker ikke for noen disposisjonskode, bortsett fra Kredit.

### <a name="issue-description"></a>Problembeskrivelse

Når **Handling**-feltet for en disposisjonskode er satt til *Kredit* eller *Svinn*, kan du bare bruke menyelementet [Mottak av kombinerte nummerskilter](mixed-license-plate-receiving.md) til å behandle returnerte varer.

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket er det bare [disposisjonskoder](../service-management/set-up-disposition-codes.md) der **Handling**-feltet er satt til *Kredit* eller *Svinn*, som støttes for mottak av kombinerte nummerskilter.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Når jeg kjører den periodiske oppgaven Oppdater produktkvitteringer, bekreftes ubekreftede bestillinger.

### <a name="issue-description"></a>Problembeskrivelse

Når du har kjørt den periodiske oppgaven *Oppdater produktkvitteringer*, bekrefter systemet automatisk ubekreftede bestillinger som har lagertransaksjonsstatusen *Registrert*.

### <a name="issue-resolution"></a>Problemløsning

En ny inngående lastbehandlingsfunksjon, *Overmottak for lastantall*, løser dette problemet. Hvis du aktiverer denne funksjonen, går du til arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktiverer følgende funksjoner (i rekkefølgen de er oppført):

1. Knytt bestillingsbeholdningstransaksjoner til belastning
1. Overmottak for belastningsantall

Hvis du vil ha mer informasjon, kan du se [Poster registrerte produktantall mot bestillinger](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Når jeg registrerer innkommende ordrer, får jeg følgende feilmelding: "Antallet er ikke gyldig."

### <a name="issue-description"></a>Problembeskrivelse

Hvis feltet **Grupperingspolicy for nummerskilt** er satt til *Brukerdefinert* for et menyelement på en mobilenhet som brukes til å registrere innkommende ordrer, får du en feilmelding ("Antallet er ikke gyldig"), og du kan ikke fullføre registreringen.

### <a name="issue-cause"></a>Feilårsak

Når *Brukerdefinert* brukes som en grupperingspolicy for nummerskilt, deler systemet det innkommende lageret i separate nummerskilt, som angitt av enhetsseriegruppen. Hvis parti- eller serienumre brukes til å spore varen som mottas, må antallene i hvert parti eller hver serie angis per nummerskilt som er registrert. Hvis antallet som er angitt for et nummerskilt, overskrider antallet som fortsatt må mottas for gjeldende dimensjoner, får du feilmeldingen.

### <a name="issue-resolution"></a>Problemløsning

Når du registrerer en vare ved hjelp av et menyelement for mobilenhet der feltet **Grupperingspolicy for nummerskilt** er satt til *Brukerdefinert*, kan systemet kreve at du bekrefter eller angir numre på nummerskilt, partinumre eller serienumre.

På bekreftelsessiden for nummerskiltet viser systemet antallet som er tilordnet for gjeldende nummerskilt. På parti- eller seriebekreftelsessidene vil systemet vise antallet som fortsatt må mottas på gjeldende numerskilt. Det inkluderer også et felt der du kan angi antallet som skal registreres for denne kombinasjonen av nummerskilt og parti- eller serienummer. I så fall må du sørge for at antallet som blir registrert for nummerskiltet, ikke overskrider antallet som fortsatt må mottas.

Hvis det genereres for mange lisensavtaler ved innkommende ordreregistrering, kan verdien i feltet **Grupperingspolicy for numerskilt** endres til *Gruppering av nummerskilt*, en ny enhetssekvensgruppe kan tilordnes varen, eller alternativet **Gruppering av nummerskilt** for enhetssekvensgruppen kan deaktiveres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
