---
title: Overføring til planleggingsoptimalisering for hovedplanlegging
description: Denne artikkelen gir informasjon om den nye hovedplanleggingsmotoren, planleggingsoptimalisering, og overføring fra den eksisterende motoren.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: dbbc58f0dcd833f63e84a73ac68ada60bd0c291d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739958"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Overføring til planleggingsoptimalisering for hovedplanlegging

[!include [banner](../includes/banner.md)]

Den innebygde hovedplanleggingsmotoren er planlagt å gjøres foreldet (avskrevet). Det erstattes av tillegget for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management. Denne artikkelen gir informasjon om innvirkning på nye og eksisterende distribusjoner. Det inneholder informasjon om nødvendige handlinger.

Planleggingsoptimalisering gjør at beregningen av hovedplanlegging skjer utenfor Supply Chain Management og den tilknyttede Azure SQL Database. Fordelene som er knyttet til planleggingsoptimalisering, omfatter forbedret ytelse og minimal virkning på SQL-databasen under kjøringer av hovedplanlegging. Siden raske planleggingskjøringer kan gjøres selv under kontortimer, kan planleggere umiddelbart reagere på behovs- eller parameterendringer.

Hvis du vil ha mer informasjon om planleggingsoptimalisering, kan du se [Systemarkitektur for hovedplanlegging](master-planning-architecture.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Avskriving av den eksisterende hovedplanleggingsmotoren

Microsoft holder på å gjøre den avskrevne hovedplanleggingsmotoren foreldet til fordel for planleggingsoptimalisering. Denne endringen påvirker alle skymiljøer. Lokale installasjoner påvirkes ikke. I versjon 10.0.16 og nyere vil du få en feilmelding hvis du kjører den avskrevne hovedplanleggingsmotoren uten å generere planlagte produksjonsordrer. Kjøringen av hovedplanleggingen vil imidlertid bli fullført til tross for feilmeldingen.

Hvis du vil ha mer informasjon om den avskrevne hovedplanleggingsmotoren, kan du se kunngjøringene i [Funksjoner som er fjernes eller avskrevet i Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Overføring, meldinger og unntak

Eiere av eksisterende miljøer som kjører den avskrevne hovedplanleggingsmotoren uten generering av planlagte produksjonsordrer, vil motta en e-post med detaljer om unntaksprosessen. Det anbefales at du samarbeider med en partner for å evaluere og planlegge migreringen til Planleggingsoptimalisering.

som nevnt vil du få en feilmelding i versjon 10.0.16 og nyere hvis du kjører den avskrevne hovedplanleggingsmotoren uten å generere planlagte produksjonsordrer. Denne feilmeldingen inneholder veiledning om overføring og instruksjoner for å be om et unntak.

### <a name="new-deployments"></a>Nye distribusjoner

Planleggingsoptimalisering må betraktes som den standard hovedplanleggingsmotor for alle nye distribusjoner i skyen. Generelt bør planleggingsoptimalisering brukes for alle nye distribusjoner som ikke genererer planlagte produksjonsordrer under hovedplanlegging. Hvis en ny distribusjon er avhengig av funksjonaliteten som planleggingsoptimalisering ikke støtter for øyeblikket, kan du be om et unntak slik at du kan fortsette å bruke den avskrevne hovedplanleggingsmotoren.

### <a name="existing-deployments"></a>Eksisterende distribusjoner

Eiere av eksisterende skybaserte distribusjon som er avhengige av hovedplanleggingen, bør planlegge å gå over til planleggingsoptimalisering. Hvis implementeringen er avhengig av funksjonaliteten som planleggingsoptimalisering ikke støtter for øyeblikket, kan du be om et unntak slik at du kan fortsette å bruke den avskrevne hovedplanleggingsmotoren.

For miljøer som bruker hovedplanleggingsprosesser som skal avskrives, sender Microsoft en e-post til miljøadministratoren. Denne e-posten vil gi informasjon om handlingene som kreves for å overføre, eller for å be om et unntak.

## <a name="the-exception-process"></a>Unntaksprosessen

Du kan be om et unntak hvis du må fortsette å bruke den avskrevne hovedplanleggingsmotoren, fordi forretningsprosessene er svært avhengige av minst én funksjon som for øyeblikket ikke er implementert i planleggingsoptimaliseringen. Hvis du vil ha en liste over tilgjengelige funksjoner, kan du se [Analyse for tilpassing av planleggingsoptimalisering](planning-optimization/planning-optimization-fit-analysis.md).

Unntak fra overføring til planleggingsoptimalisering er for øyeblikket bare relevante hvis hovedplanleggingsprosessen ikke inkluderer produksjon (det vil si planlagte produksjonsordrer som genereres av hovedplanlegging), og du trenger den avskrevne hovedplanleggingsmotoren etter versjon 10.0.15.

Når de nødvendige funksjonene blir tilgjengelige, vil Microsoft angi en respittperiode helt til unntaket utløper. Miljøadministratoren blir informert når de nødvendige funksjonene har blitt tilgjengelige og respittperiode har startet.

Følgende flytdiagram oppsummerer informasjonen som oppgis i denne artikkelen, slik at du raskt kan finne ut om du bør be om et unntak. Hvis du må be om et unntak, kan du fylle ut og sende inn [spørreskjemaet om migrering og unntak i Planleggingsoptimalisering](https://go.microsoft.com/fwlink/?linkid=2144962). Produktgruppen er ansvarlig for å evaluere og godkjenne hver unntaksforespørsel, så du sender forespørselen direkte til produktgruppen ved hjelp av koblingen som tilbys, og ikke opprett en støttebillett for den. Hvis forespørselen din avvises, må du ikke opprette en støtteforespørsel, fordi Microsoft Support ikke kan evaluere eller gi unntak på nytt.

![Unntaksflytskjema.](media/exception-diagram.png "Unntaksflytskjema")

> [!NOTE]
> Du kan bare be om et unntak for leiere som for øyeblikket inkluderer, eller kommer til å inkludere, et produksjonsmiljø, ikke bare for leiere med sandkassemiljøer. Hvis du må deaktivere unntaksfeilen for planleggingsoptimalisering i en infrastruktur som en tjeneste (IaaS), kjører du SQL-spørringen som følger med i [sandkassemiljøer](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandkassemiljøer

Kan jeg bruke den avskrevne hovedplanleggingsmotoren i sandkassemiljøet mitt? Trenger jeg et unntak?

**Svar:** Unntak er vanligvis ikke relevante for sandkassemiljøer fordi unntaksfeilen for planleggingsoptimalisering ikke hindrer den avskrevne hovedplanleggingsmotoren i å kjøre. Hvis imidlertid feilmeldingen forstyrrer deg, kan du deaktivere den i et IaaS-sandkassemiljø (ikke Service Fabric) ved å kjøre følgende spørring i databasen:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Lokale miljøer

Mitt miljø er lokalt. Trenger jeg et unntak?

**Svar:** Nei. Det kreves ikke et unntak for lokale miljøer. Du kan fortsette å bruke den avskrevne hovedplanleggingsmotoren. Miljøadministratoren blir informert hvis det er nødvendig å gjøre noe.

### <a name="production-scenarios"></a>Produksjonsscenarioer

Vi bruker planlagte produksjonsordrer, men jeg er bekymret over hva som skjer når vi oppgraderer til versjon 10.0.16. Må jeg foreta meg noe?

**Svar:** Du trenger ikke å bekymre deg. Du kan fortsette å bruke den avskrevne hovedplanleggingsmotoren i versjon 10.0.16. Det anbefales imidlertid at du vurderer om overføring til planleggingsoptimalisering kan starte med gjeldende funksjonalitet. Det anbefales også at du holder deg oppdatert om ny funksjonalitet.

### <a name="email-from-microsoft"></a>E-post fra Microsoft

Vår miljøadministrator mottok en e-post fra Microsoft. Denne e-posten angir at vi bør overføre til planleggingsoptimalisering eller be om et unntak. Må jeg foreta meg noe?

**Svar:** Ja. Miljøet ditt påvirkes med mindre du følger instruksjonene i e-postmeldingen. Du kan enten overføre til planleggingsoptimalisering innen datoen som er angitt, eller be om et unntak ved hjelp av koblingen i e-postmeldingen. Denne koblingen åpner et spørreskjema. Når du har fullført og sendt inn dette spørreskjemaet, vil du motta et svar via e-post. Selv om denne prosessen er manuell, prøver Microsoft å svare innen en uke etter at spørreskjemaet er sendt.

### <a name="error-messages"></a>Feilmeldinger

Jeg bruker versjon 10.0.16 eller nyere, og jeg får følgende feilmelding når jeg kjører hovedplanlegging. Er hovedplanleggingen blokkert?

> Du får denne feilmeldingen fordi den avskrevne hovedplanleggingsmotoren ble brukt til scenarioer som støttes av planleggingsoptimalisering. Du bør overføre til planleggingsoptimalisering nå, fordi den innebygde hovedplanleggingsmotoren er avskrevet. Legg merke til at denne hovedplanleggingskjøringen ble fullført.
>
> I tilfelle overføringen har sterke avhengigheter for ventende funksjoner, kan du be om et unntak for fortsatt bruk av den avskrevne hovedplanleggingsmotoren.
>
> Fyll ut følgende spørreskjema for å komme i gang og hvis det er relevant for forespørselsunntak fra overføring til planleggingsoptimalisering.

**Svar:** Nei, hovedplanlegging er ikke blokkert. Hovedplanleggingskjøringen er fullført, og du kan bruke resultatet på vanlig måte. Hvis du vil unngå å motta denne feilmeldingen under fremtidige hovedplanleggingskjøringer, må du imidlertid enten overføre til planleggingsoptimalisering umiddelbart eller be om et unntak ved hjelp av koblingen i feilmeldingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
