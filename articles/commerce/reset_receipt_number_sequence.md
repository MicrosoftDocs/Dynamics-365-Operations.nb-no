---
title: Tilbakestille kvitteringsnumre
description: Dette emnet beskriver hvordan du tilbakestiller kvitteringsnumrene som brukes for ulike handlinger på en ønsket dato (for eksempel regnskapsåret eller kalenderåret).
author: ShalabhjainMSFT
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Application update 10.0.9
ms.openlocfilehash: 855c39f15db6de8fac1f0cd4667eec485c70542b9aebde0d7085e2703f4609bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733875"
---
# <a name="reset-receipt-numbers"></a>Tilbakestille kvitteringsnumre 

[!include [banner](includes/banner.md)]

> [!NOTE]
> Du må velge **Uavhengig sekvens**-egenskapen for alle kvitteringstyper i funksjonalitetsprofilen før du bruker denne funksjonen. Systemtidssonen til enheten, der salgsstedet brukes, bør i tillegg samsvare med tilsvarende tidssone for lagring. På grunn av disse begrensningene anbefaler vi at du ikke bruker denne funksjonen i produksjon mens vi arbeider med å løse disse problemene i en fremtidig versjon. 

Forhandlere genererer kvitteringsnumre for ulike handlinger i butikken, for eksempel hentesalgstransaksjoner, returtransaksjoner, kundeordrer, tilbud og betalinger. Selv om forhandlere definerer sine egne kvitteringsformater, har noen land eller regioner reguleringer som angir begrensninger i disse kvitteringsformatene. Disse bestemmelsene kan for eksempel begrense antall tegn på kvitteringen, kreve etterfølgende kvitteringsnumre, begrense noen spesialtegn eller kreve tilbakestilling av kvitteringsnumre i begynnelsen av året. Microsoft Dynamics 365 Commerce gjør prosessen med å behandle kvitteringsnumre svært fleksibel, for å hjelpe forhandlere med å dekke forskriftsmessige krav. Dette emnet forklarer hvordan du bruker funksjonaliteten til å tilbakestille kvitteringsnumre.

I Commerce kan kvitteringsformater være alfanumeriske. Du kan plassere både statisk innhold og dynamisk innhold i dem. Statisk innhold inkluderer bokstaver, tall og spesialtegn. Dynamisk innhold inneholder ett eller flere tegn som representerer informasjon som butikknummer, terminalnummer, dato, måned, år og nummerserier som automatisk økes. Formatene er definert i delen **Kvitteringsnummerering** i funksjonalitetsprofilen. Tabellen nedenfor beskriver tegnene som representerer det dynamiske innholdet.

| Tegn | Beskrivelse |
|------------|-------------|
| L          | Tegnet **S** brukes for butikknummeret. Hvis for eksempel en butikk er nummerert HOUSTON1, viser formatet **SSS** "ON1" på kvitteringen. Formatet **SSSSS** viser "STON1" på kvitteringen. |
| T          | Tegnet **T** brukes for terminalnummeret. Hvis for eksempel en terminal er nummerert 0001, viser formatet **TTTT** "0001" på kvitteringen. |
| K          | Tegnet **C** brukes for stabs-ID-nummeret. Hvis for eksempel et stabsmedlem har ID-en 000160, viser formatet **CCCC** "0160" på kvitteringen. |
| ddd        | Tegnene **ddd** tilsvarer dagen i året, fra 1 til 366. 15. januar vises for eksempel formatet **ddd** "015" på kvitteringen. |
| MM         | Tegnene **MM** brukes for måneden med to sifre. I januar viser for eksempel formatet **MM** "01" på kvitteringen. |
| DD         | Tegnene **DD** brukes for dagen i måneden med to sifre. 15. januar viser for eksempel formatet **DD** "15" på kvitteringen. |
| YY         | Tegnene **YY** brukes for året med to sifre. I en hvilken som helst måned i året 2020, viser for eksempel formatet **YY** "20" på kvitteringen. |
| \#         | Et nummertegn (**\#**) brukes til sekvensiell nummerering. Formatet **####** viser for eksempel "0001", "0002", "0003" og så videre på kvitteringen. |

Du kan tilbakestille den sekvensielle nummereringen på kvitteringen på en bestemt dato. For den første transaksjonen som skjer etter klokken 12:00 på den valgte tilbakestillingsdatoen, tilbakestiller systemet kvitteringens nummerserie til 1. Du kan også angi om tilbakestillingen bare skal skje én gang, eller om den skal gjentas hvert år. Hvis årlig gjentakelse er angitt, skjer tilbakestillingen automatisk hvert år til forhandleren velger å stoppe den. 

Følg denne fremgangsmåten for å aktivere tilbakestilling.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**.
1. På hurtigfanen **Kvitteringsnummerering** velger du **Dato for tilbakestilling av nummer**.
1. I **Tilbakestillingsdato**-feltet i dialogboksen velger du en fremtidig dato når tilbakestillingen skal inntreffe.
1. I feltet **Type tilbakestilling av kvittering** velger du **Bare én gang** eller **Årlig**.
1. Velg **OK**.

![Velge en dato for tilbakestilling av kvittering.](media/Enable_receipt_reset.png "Velge en dato for tilbakestilling av kvittering")

Når du har valgt en dato, vises den i kolonnen **Neste tilbakestillingsdato for kvitteringsnummer**. Tilbakestillingsdatoen gjelder for alle kvitteringstransaksjonstyper. Derfor vil kvitteringsnummerserien bli tilbakestilt for alle kvitteringstyper.

Når tilbakestillingsdatoen ankommer, tilbakestilles kvitteringsnummeret for den første transaksjonen av hver type. I funksjonalitetsprofilen flyttes i tillegg tilbakestillingsdatoen fra kolonnen **Neste tilbakestillingsdato for kvitteringsnummer** til kolonnen **Gjeldende tilbakestillingsdato for kvitteringsnummer**. Denne endringen angir at hvis en kasse ikke brukes på tilbakestillingsdatoen, vil kvitteringsnummeret bli tilbakestilt neste gang kassen *brukes*. For eksempel, 3. desember 2019 velger du **1. januar 2020** som tilbakestillingsdato. 1. januar, når kassene gjør den første transaksjonen, tilbakestilles kvitteringsnummeret. Én kasse blir imidlertid ikke brukt i det hele tatt i desember og januar, men starter deretter å brukes i februar. I dette tilfellet, fordi det ble definert en tilbakestillingshandling, blir kvitteringsnummeret for denne kassen tilbakestilt når kassen gjør den første transaksjonen i februar.

Du kan bruke funksjonen **Fjern tilbakestillingsdato** til å fjerne fremtidige tilbakestillingsdatoer. Hvis tilbakestillingsdatoen inntraff i fortiden, kan du imidlertid ikke angre. Derfor vil tilbakestillingen fortsatt skje for alle kasser der tilbakestillingen ikke ennå har skjedd.

> [!NOTE]
> Avhengig av tilbakestillingsdatoen du velger, og kvitteringsformatet, kan du ha dupliserte mottaksnumre. Selv om salgsstedssystemet kan håndtere disse situasjonene, øker de tiden som kreves for å behandle returer, fordi salgsmedarbeiderne må velge mellom de duplikat kvitteringene. Andre komplikasjoner som er relatert til dataopprydding, kan forekomme hvis de duplikat kvitteringene ikke var en planlagt konsekvens. Derfor anbefaler vi at du bruker dynamiske datotegn (for eksempel **ddd**, **MM**, **DD** og **YY**) som hjelp til å hindre duplikate kvitteringsnumre etter en tilbakestilling.


[!INCLUDE[footer-include](../includes/footer-banner.md)]