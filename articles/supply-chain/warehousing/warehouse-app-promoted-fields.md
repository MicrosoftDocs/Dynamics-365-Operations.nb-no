---
title: Konfigurere forfremmede felt for trinn i mobilappen Warehouse Management
description: Dette emnet beskriver hvordan du forfremmer og uthever bestemt informasjon for trinn i oppgaveflytene for mobilappen Warehouse Management.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 117730fd7b744e0462e10468e32a13203d0695bf
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901852"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Konfigurere forfremmede felt for trinn i mobilappen Warehouse Management

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until GA with 10.0.23 -->

> [!IMPORTANT]
> Funksjonene som er beskrevet i dette emnet, gjelder bare for den nye mobilappen Warehouse Management. De påvirker ikke den gamle lagerappen, som nå er avskrevet.

Dette emnet beskriver hvordan du forfremmer og uthever bestemt informasjon for trinn i oppgaveflytene for mobilappen Warehouse Management. Denne funksjonen kan hjelpe arbeiderne med å fokusere på de viktigste feltene når de arbeider gjennom en flyt. For hvert trinn i hver prosess kan administratorer velge hvilke felt som skal fremmes, og hvilke felt som skal utheves.

## <a name="enable-promoted-fields-in-your-system"></a>Aktivere forfremmede felt i systemet

Før du kan definere forfremmede felt, må du fullføre fremgangsmåten nedenfor for å aktivere de nødvendige funksjonene og generere de nødvendige feltnavnene i mobilappen Warehouse Management.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
1. I [**Funksjonsadministrering**-arbeidsområdet](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiverer du funksjonen som er oppført på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Trinnvise instruksjoner i lagerapp*

    Hvis du vil ha mer informasjon om funksjonen *Trinnvise instruksjoner i lagerapp*, kan du se [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](mobile-app-titles-instructions.md). Denne funksjonen er en forutsetning for funksjonen *Forfremmede felter for lagerapp*.

1. Aktiver funksjonen som vises på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Forfremmede felter for lagerapp*

    Denne funksjonen er funksjonen som er beskrevet i dette emnet.

1. Oppdater feltnavnene i mobilappen Warehouse Management ved å gå til **Lagerstyring \> Oppsett \> Mobile device \> Navn på lagerappfelt**, og velg **Opprett standardoppsett**. For mer informasjon, se [Konfigur felter for mobilappen Lagerstyring](configure-app-field-names-priorities-warehouse.md).
1. Gjenta det forrige trinnet for hver juridiske enhet (firma) der du bruker mobilappen Warehouse Management.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigurere forfremmede felt fra en menyspesifikk overstyring

Bruk fremgangsmåten nedenfor for å konfigurere forfremmede felt.

1. Opprett en menyspesifikk overstyring for den relevante menyen og trinnet som beskrevet i [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](mobile-app-titles-instructions.md).
1. Finn kombinasjonen av verdier for **Trinn-ID** og **Menyelementnavn** som du ønsker å redigere, og velg deretter verdien i kolonnen **Trinn-ID**.
1. På siden som i hurtigfanen **Valgte forfremmede felter**, velger du **Velg felt** på verktøylinjen.
1. Velg feltene du vil fremme, i dialogboksen **Forfremmede felter**. Du kan også utheve opptil to av de valgte feltene. Uthevede felt vises med fet skrift i mobilappen Warehouse Management. Når du velger felt, må du ta i betraktning at noen skjermbilder kan være store nok til å bare vise ett eller to forfremmede felt. Hvis du vil ha et eksempel som viser hvordan du bruker disse innstillingene, kan du se scenariet senere i dette emnet.

    > [!NOTE]
    > Listen **Tilgjengelige felt** er begrenset til feltene som kan vises for menyelementet. Andre faktorer (for eksempel varesammensetning) bestemmer imidlertid om et felt faktisk vises i mobilappen Warehouse Management. Hvis du har konfigurert de forfremmede feltene, vises bare de valgte feltene på hovedsiden i mobilappen Warehouse Management. Arbeidere kan imidlertid fremdeles vise de gjenværende feltene ved å skrive over detaljer.

1. Velg **OK** for å bruke innstillingene. De valgte feltene vises nå i hurtigfanen **Valgte forfremmede felter**.

## <a name="example-scenario"></a>Eksempelscenario

### <a name="enable-sample-data"></a>Aktivere eksempeldata

Hvis du vil bruke de angitte eksempelpostene og verdiene til å arbeide deg gjennom dette scenariet, må du bruke et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigurere salgsplukking med forfremmede trinn i nummerskilttrinnet

I denne fremgangsmåten definerer du forfremmede og merkede felt for menyelementet **Salgsplukking** i nummerskilttrinnet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Trinn formobilenhet**.
1. Finn trinn-IDen med navnet *LicensePlateId*, og velg det.
1. Velg **Legg til trinnkonfigurasjon** i handlingsruten.
1. I rullegardinlisten bruker du **Menyelement**-feltet til å finne og velge *Salgsplukking*.
1. Velg **OK**.
1. Detaljsiden for overstyringen som du akkurat opprettet, vises. På hurtigfanen **Valgte forfremmede felter** velger du **Velg felt** på verktøylinjen.
1. I dialogboksen **Forfremmede felter** kan du velge feltene du vil forfremme og utheve. I listen **Tilgjengelige felt** finner og velger du følgende felt, og bruker knappene til å flytte dem til listen **Valgte felt**:

    - Lokasjon
    - Artikkel
    - Produktnavn
    - Beholdningsstatus

1. Bruk pil opp eller pil ned til å tilpasse rekkefølgen på feltene i listen **Valgte felt**. Feltene vises i den rekkefølgen du angir her, i mobilappen Warehouse Management.
1. Velg **Lokasjon**-feltet, og velg deretter **Uthev**.
1. Velg **OK** for å lagre konfigurasjonen.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Vis de forfremmede feltene i mobilappen Warehouse Management

I denne fremgangsmåten åpner du mobilappen Warehouse Management og går gjennom trinnene for å vise feltene du forfremmet og uthevet i den forrige fremgangsmåten.

1. I Microsoft Dynamics 365 Supply Chain Management oppretter du en salgsordre som krever et plukktrinn for å plukke fra en lokasjon som spores med nummerskilt. Deretter frigir du salgsordren til lageret. Noter deg arbeids-ID-en som genereres.
1. Åpne mobilappen Warehouse Management, og logg på lager 24. (I standard demodata logger du deg på ved å bruke *24* som bruker-ID og *1* som passord.)
1. Velg **Utgående**-menyen, og velg deretter menyelementet **Salgsplukking**.
1. Følg instruksjonene for dataoppføring på skjermen for å angi arbeids-IDen som ble generert i trinn 1.
1. I trinnet som inneholder teksten **Skann et nummerskilt**, skal du se endringene du har gjort på detaljsiden. Feltene vises i den rekkefølgen du angir for de forfremmede feltene, og **Lokasjon**-feltet vises med fete typer.
