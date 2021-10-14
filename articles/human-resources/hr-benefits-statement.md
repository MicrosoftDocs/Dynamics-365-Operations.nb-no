---
title: Fordelserklæring
description: Rapporten Fordelserklæring forklarer fordelene som en ansatt er registrert med i øyebliket.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 46f7358684502a4bf05854fbcb5cca9a1eb2c87c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548061"
---
# <a name="benefit-statement"></a>Fordelserklæring

Rapporten **Fordelserklæring** inneholder en erklæring om fordelene som en ansatt er registrert med i øyeblikket. En ansatt kan få tilgang til rapporten direkte eller av fordelsadministratoren. **Fordelserklæringen** inneholder en liste over den  ansattes innmeldingsfordeler, dekningsalternativer, kostnader og eventuelle avhengige eller mottakere som er registrert. Erklæringen kan skrives ut for én enkelt arbeider eller flere arbeidere.

> [!NOTE]
Funksjonen **Fordelserklæring** må være aktivert i arbeidsområdet **Funksjonsbehandling**. For at du skal kunne gjøre dette, må funksjonen **Fordelsstyring** aktiveres i Funksjonsbehandling. 


## <a name="importing-the-benefit-statement"></a>Importere fordelserklæringen 

Du må importere **fordelserklæringen** ved hjelp av rapportkonfigurasjon før **fordelserklæringen** blir tilgjengelig. Følg fremgangsmåten nedenfor for å gjøre dette:

1.  Gå til arbeidsområdet **Systemadministrasjon**.

2.  Velg flisen **Elektronisk rapportering**.

3.  Gå til **Konfigurasjonsleverandører**, og velg **Repositorier**.

  ![Valg av Repositorier.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Velg **Personale** fra listen, og velg deretter **Åpne**.

    ![Konfigurasjonsrepositorier.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Velg **fordelserklæringsmodellen** i ruten til venstre, og utvid den slik at **formatet for fordelserklæring** vises.

6.  Velg **fordelserklæringsformat** i ruten til venstre.

7.  Til høyre på skjermen finnes det en **Versjoner**-hurtigfane. Velg **Import**.

    ![Hurtigfanen Versjoner.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Generere fordelserklæringen som en PDF-fil

Som standard skrives **fordelserklæringen** ut som et Microsoft Word-dokument. Hvis du vil skrive ut i et PDF-format, må du konfigurere PDF-alternativet i mål **Mål for elektronisk rapportering**. 

1. Du gjør dette ved å gå til arbeidsområdet **Systemadministrasjon** > **Elektronisk rapportering** > **Relaterte koblinger** > **Mål for elektronisk rapportering**.

1.  Velg **Ny**.

2.  I feltet **Referanse** velger du **Fordelserklæringsformat**.

3.  På **Filmål**-hurtigfanen velger du **Ny**.

4.  I **Navn**-feltet skriver du inn **Fordelserklæring (PDF)**.

5.  I feltet **Navn på filkomponent** velger du **Fordelserklæring**.

6.  Merk av for **Konverter til PDF**.

7.  Velg **Innstillinger** fra menyelementet. 

    ![Filmål.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Velg hurtigfanen **Fil**, og velg deretter **Aktivert**.

9.  Velg **OK**.
   
> [!NOTE]
> Fordelsbehandlingsfunksjonen er i forhåndsvisningstilstand. Det er et kjent problem når du bruker innstillingen for e-postmål i rapporten **Mål for elektroniske rapportering**. Du kan få en feilmelding, og e-posten vil ikke bli sendt.

**Fordelserklæringen** kan genereres fra følgende sider:

-   **Arbeidsområde for fordelsbehandling** > **Koblinger** > **Rapporter** > **Fordelserklæring**

-   **Ansatte (eldre skjema)** > **fanen Personlig informasjon** > **Fordelserklæring**

-   **Strømlinjeformet ansattoppføring** > **Fordelsrapporter** > **Fordelserklæring**

-   **Ansattselvbetjening** > **Fordeler** > **Vis fordelserklæring**

> [!NOTE]
>  Tilgang til **fordelserklæringen** i **Ansattselvbetjening** styres av rettigheten **Vis fordelserklæring**. Dette er under plikten **fordeler for ansattselvbetjening**. Denne rettigheten gis til ansatte som standard.

## <a name="report-contents"></a>Rapportinnhold

**Fordelserklæringen** skriver ut bekreftede planvalg for den ansatte, inkludert eventuelle fradragsplaner. Bildet nedenfor viser et eksempel på denne rapporten. 

![Fordelserklæringsrapport.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Rapporten viser **Plan**, **Dekningsalternativ**, **Ansattkostnader** og **Arbeidsgiverkostnad**. Rapporten viser også eventuelle avhengige av dekning. Hvis planen har mottakere tilknyttet seg, vises mottakerne og deres distribusjonsprioritet og prosent.

**Fordelserklæring**-rapporten kan skrives ut for flere ansatte samtidig ved hjelp av hurtigfanen **Poster som skal inkluderes** på **Fordelserklæring**-siden.
