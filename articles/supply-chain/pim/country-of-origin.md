---
title: Opprinnelsesland
description: Mange organisasjoner utsteder sertifikater til sine leverandører for å sikre at produkter oppfyller bestemte sertifiseringsstandarder. Disse sertifikatene avhenger ofte av opprinnelseslandet. Dette emnet gir informasjon om funksjonen for opprinnelsesland, der du kan koble et produkt til opprinnelsesland og holde oversikt over produktsertifiseringer.
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fde4211e4449c28eda8ac7a23ddfc346d2c7e8359d9e473821bdefe76db65616
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739784"
---
# <a name="country-of-origin"></a>Opprinnelsesland

[!include [banner](../includes/banner.md)]

Mange organisasjoner utsteder sertifikater til sine leverandører for å sikre at produkter oppfyller bestemte sertifiseringsstandarder. Disse sertifikatene avhenger ofte av opprinnelseslandet. I opprinnelseslandet kan du koble et produkt til opprinnelsesland og holde oversikt over produktsertifiseringer.

## <a name="turn-on-the-country-of-origin-feature"></a>Aktivere funksjonen for opprinnelsesland

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Behandling av produktinformasjon*
- **Funksjonsnavn:** *Funksjon for administrasjon av opprinnelsesland*

## <a name="configure-source-and-destination-countries"></a>Konfigurere kilde- og målland

Før du utsteder et sertifikat for et produkt må du koble produktet til mållandet og opprinnelseslandet.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland \> Regler for opprinnelsesland**.
2. Velg et eksisterende landsoppsett for å redigere, eller velg **Ny** i handlingsruten for å opprette et nytt landsoppsett.
3. Angi følgende verdier for det valgte eller nye landet.

    | Felt | beskrivelse |
    |---|---|
    | Varenummer | Velg varenummeret for produktet. |
    | Målland | Velg landet du sender produktet til. |
    | Opprinnelsesland | Velg landet du sender produktet fra. |

Formålet med dette oppsettet er å hjelpe deg med å generere en stykklisterapport der du kan ta med opprinnelseslandet for hver del som kilde- og mållandene er angitt for. Denne rapporten vil hjelpe deg med å få et helhetlig bilde av stedet der delene kommer fra, og hvor de skal.

## <a name="keep-track-of-vendor-certificates"></a>Holde oversikt over leverandørsertifikater

Du kan bruke siden for **Leverandørsertifikater for opprinnelsesland** til å holde oversikt over sertifikater som du utsteder til leverandører.

Du må bestemme hvilke sertifikatdokumenter du skal utstede, og hvordan de skal rapportere dem til kunder. Denne funksjonen hjelper deg med å holde orden på sertifikatene. Du kan også velge om de aktuelle sertifikatnumrene skal vises på fakturaer, følgesedler og/eller ordrebekreftelser.

Gjør følgende for å konfigurere sertifikatinformasjon.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Opprinnelsesland \> Leverandørsertifikater for opprinnelsesland**.
2. Velg et eksisterende sertifikatoppsett for å redigere, eller velg **Ny** i handlingsruten for å opprette et nytt sertifikatoppsett.
3. Angi følgende innstillinger for det valgte eller nye sertifikatet.

    | Felt | beskrivelse |
    |---|---|
    | Leverandørnummer | Velg leverandøren som du utstedte sertifikatet til. |
    | Varenummer | Velg varen som du utstedte sertifikatet for. |
    | Land/område | Mållandet eller -området der du må bruke dette sertifikatet. |
    | Sertifikatnummer | Angi identifikasjonsnummeret for sertifikatet du har utstedt. |
    | Gyldighet | Velg den første datoen når det gjeldende sertifikatet er gyldig.|
    | Utløp | Velg den siste datoen når det gjeldende sertifikatet er gyldig. |
    | Skriv ut på faktura | Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på fakturaer som er adressert til det angitte landet i det angitte datoområdet. |
    | Skrive ut på følgeseddel | Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på følgesedler som er adressert til det angitte landet i det angitte datoområdet. |
    | Skriv ut på salgsordre | Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på salgsordrer som er adressert til det angitte landet i det angitte datoområdet. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Ta med opprinnelsesland på stykklisterapporter

Når du genererer en stykklisterapport, kan du ta med opprinnelseslandet for hver del du angav kilde- og målland for, på siden **Regler for opprinnelsesland**.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg eller opprett et produkt for å åpne siden **Detaljer om frigitt produkt**.
1. I handlingsruten, i fanen **Utvikling** i **Stykkliste**-gruppen, velger du **Designer**.
1. I handlingsruten velger du **Stykkliste \> Skriv ut** på siden som vises.
1. I dialogboksen **Stykklistelinjer** angir du feltet **Målland** til mållandet du vil vise i rapporten.
1. Velg **OK**.

En rapport som viser informasjon om opprinnelsesland for hver del, genereres og vises. Her er et eksempel på rapporten.

![Rapport for opprinnelsesland.](media/country-of-origin-report.png "Rapport for opprinnelsesland")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]