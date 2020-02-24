---
title: Oppslag for utvidet elektronisk rapporteringsformat (ER)
description: Dette emnet beskriver hvordan en ER-formatreferanse kan settes opp i ER-formatoppslaget når det påkrevde formatet er lagret i det globale repositoriet.
author: NickSelin
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c72335d7d83934146f827ef0bb568b79a585a7a5
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015336"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Tillate brukere å konfigurere en ER-formatreferanse som forespør et format fra det globale repositoriet

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Du kan bruke [Elektronisk rapportering](general-electronic-reporting.md)-rammeverket (ER) til å konfigurere [formater](general-electronic-reporting.md#FormatComponentOutbound) for utgående dokumenter i samsvar med lovkravene i forskjellige land/regioner. Du kan også bruke ER-rammeverket for å konfigurere [formater](general-electronic-reporting.md#FormatComponentInbound) for analyse av inngående dokumenter og bruke informasjonen fra disse dokumentene til å legge til eller oppdatere applikasjonsdata. Hvert av disse formatene kan brukes i Dynamics 365 Finance-forekomsten for håndtering av inngående eller utgående forretningsdokumenter som en del av en viss forretningsprosess. 

Vanligvis må du angi hva slags ER-format som må brukes i en bestemt forretningsprosess. Hvis du vil gjøre dette, velger du ett enkelt ER-format i et oppslagsfelt som er konfigurert som del av forretningsprosesspesifikke parametere. Disse oppslagsfeltene implementeres vanligvis ved å bruke riktig API for ER-rammeverket. Hvis du vil ha mer informasjon, kan du se [ER-rammeverks-API – kode for å vise et formatkartleggingsoppslag](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Når du konfigurerer [utenrikshandelparametere](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), må du for eksempel sette opp referansene til individuelle ER-formater som skal brukes til å generere Intrastat-deklarasjonen og Intrastat-deklarasjonskontrollrapporten. Skjermbildene nedenfor viser hvordan ER-formater-oppslagsfeltet ser ut på **Utenrikshandelparametere**-siden.

Hvis gjeldende Finans-forekomst ikke inneholder noen ER-formater relatert til Intrastat-forretningsprosess, vil dette oppslagsfeltet være tomt.

[![Utenrikshandelsparametere-siden](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Hvis gjeldende Finans-forekomst inneholder ER-formater relatert til Intrastat-forretningsprosess, tilbyr dette oppslagsfeltet ER-formatene.

[![Utenrikshandelsparametere-siden](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Dette oppslaget tilbyr bare ER-formater som allerede er importert til gjeldende Finans-forekomst. Hvis du vil [importere](./tasks/er-import-configuration-lifecycle-services.md) ER-løsninger til gjeldende Finans-forekomst, må du ha tillatelser for å kjøre den aktuelle funksjonen til ER-rammeverket som støtter [livssyklusen](general-electronic-reporting-manage-configuration-lifecycle.md) til ER-løsninger som inneholder ER-formater.

Fra og med i Finans-versjonen 10.0.9 (utgitt april 2020) har brukergrensesnittet til ER-formatoppslaget som implementeres ved bruk av ER-rammeverks-API-et, utvidet. Du kan fortsatt velge de eksisterende ER-formatene, som **Velg formatkonfigurasjon**-hurtigfanen. I tillegg til dette tilbyr det utvidede oppslaget det nye alternativet for å søke etter bestemte ER-formater i det globale repositoriet (GR). Alle ER-formatene i det globale repositoriet tilbys på **Importer fra global database**-hurtigfanen.

[![Utenrikshandelsparametere-siden](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Tilsvarende som for **Velg formatkonfigurasjon**-hurtigfanen viser **Importer fra globalt repositorium**-hurtigfanen bare ER-formatene som er aktuelle for forretningsprosessen som et ER-format er valgt for i dette oppslagsfeltet. I dette eksempelet er det genereringen av Intrastat-deklarasjon. ER-formatet gjelder for selskapet som brukeren for øyeblikket er logget på, avhengig av selskapets landskontekst.

Når du velger et ER-format på **Import fra globalt repositorium**-hurtigfanen, importeres det valgte ER-formatets [konfigurasjon](general-electronic-reporting.md#Configuration) fra det globale repositoriet til gjeldende Finans-forekomst.

[![Utenrikshandelsparametere-siden](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Hvis importen fullføres, lagres referansen til det importerte ER-formatet så i dette oppslagsfeltet. Vær oppmerksom på følgende: Når du åpner det globale repositoriet (GR) for første gang, må du følge koblingen til registrering for [Regulatory Configuration Service](https://aka.ms/rcs) (RCS), som brukes til å styre tilgangen til GR-lageret.

[![Utenrikshandelsparametere-siden](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Som standard viser **Importer fra globalt repositorium**-hurtigfanen listen over ER-formater fra den midlertidige lagringsplassen, som opprettes automatisk basert på GR-innholdet for ytelsesforbedringer. Dette skjer når **Importer fra globalt repositorium**-hurtigfanen åpnes for første gang, noe som kan ta flere sekunder.

Hvis du ikke ser det påkrevde ER-formatet på **Importer fra globalt repositorium**-hurtigfanen, men du er sikker på at dette ER-formatet er lagret i GR, velger du **Synkroniser**-alternativet. Dette oppdaterer den midlertidige lagringsplassen og synkroniserer den med det gjeldende innholdet i det globale repositoriet.

## <a name="feature-activation"></a>Funksjonsaktivering

Tilgjengeligheten til denne funksjonaliteten styres av funksjonen **Utvidet oppslag av ER-formatkonfigurasjoner som muliggjør sending av spørring til det globale repositoriet** i **Funksjonsadministrering**. Denne funksjonen er aktivert som standard.

[![Funksjonsadministrering-siden](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Sikkerhetshensyn

**Oppretthold konfigurasjonsrepositorier**-rettigheten (**ERMaintainSolutionRepositories**) styrer tilgangen til det globale repositoriet for en bruker som åpner ER-formatoppslaget med den aktiverte **Importer fra globalt repositorium**-hurtigfanen. Hvis du vil la brukere få tilgang til GR-innholdet fra ER-formatoppslagene, må du endre sikkerhetsinnstillingene ved å gi **ERMaintainSolutionRepositories**-rettigheten til brukere enten direkte eller ved å benytte allerede tilordnede roller og plikter.

Følgende skjermbilde viser hvordan denne rettigheten kan gis til brukere som har fått tilordnet **Regnskapsfører**-rollen. Denne rollen gjør det mulig for brukere å konfigurere utenrikshandelparametere og sette opp referanser til ER-formatene i feltene **Filformatkartlegging** og **Rapportformatkartlegging** på **Utenrikshandelparametere**-siden.

[![Sikkerhetskonfigurasjon-siden](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Begrensninger

Tilgang til det globale repositoriet i ER-formatoppslaget støttes foreløpig bare for valg av ER-formater som brukes til å generere utgående dokumenter.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Hvorfor får jeg ikke tilgang til det globale repositoriet fra ER-formatoppslaget?

Hvis du har aktivert **Utvidet oppslag av ER-formatkonfigurasjoner som muliggjør sending av spørring til det globale repositoriet**-funksjonen på **Funksjonsadministrering**-siden, men brukere ikke kan se ER-formater på **Importer fra globalt repositorium**-hurtigfanen og **Synkroniser**-alternativet er synlig, men deaktivert, sørger du for at **Oppretthold konfigurasjonsrepositorier**-rettigheten (**ERMaintainSolutionRepositories**) er gitt til brukeren. Kontakt systemadministratoren for å få denne rettigheten.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Rammeverks-API for elektronisk rapportering (ER)](er-apis-app73.md)
- [Administrere konfigurasjonslivssyklus for elektronisk rapportering (ER)](general-electronic-reporting-manage-configuration-lifecycle.md)
