---
title: Konfigurer Oppslag-datakilder for å bruke ER-programspesifikke parametere
description: Dette emnet forklarer hvordan du kan konfigurere Oppslag-datakilder i ER-formater (elektronisk rapportering) for å bruker parametere som er spesifikek for ER-programmet.
author: NickSelin
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 542580c859759c25da84589ec82495eb72bbcbe5
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853527"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Konfigurer Oppslag-datakilder for å bruke ER-programspesifikke parametere 

[!include[banner](../includes/banner.md)]

Parameterne som er spesifikke for [ER-prgrammet (elektronisk rapportering)](general-electronic-reporting.md), gjør det mulig for deg å konfigurere datafiltrering i et ER-format slik at det er basert på et sett med abstrakte regler. Dette settet med regler kan konfigureres til å bruke datakilden av **Oppslag**-typen som er tilgjengelig i et ER-format. Du kan deretter angi reelle regler utenfor reglene fra ER-komponentutformere ved hjelp av brukergrensesnittet som automatisk genereres basert på innstillingene for **Oppslag**-datakilden i det tilsvarende ER-formatet, og de gjeldende dataene for juridisk enhet. Til slutt får du tilgang til de angitte reglene av ER-formatets **Oppslag**-datakilde når dette ER-formatet kjøres.

> [!NOTE]
> Bruk de konfigurerte datakildene for det redigerbare ER-formatet til å angi hvilke programdata som skal brukes til å konfigurere reelle regler.

Bruk [ER-operasjonsutforming](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) til å hente en datakilde av **Oppslag**-typen inn i ER-formatet. Datakilden må konfigureres for å beskrive hvordan abstrakte regler ser ut, inkludert følgende:

   - Parametersettet for en bestemt datatype der det gis en verdi for å angi en enkelt regel.
   - Verditypen av en bestemt datatype som returneres av en enkelt regel når denne regelen regnes som den mest passende blant andre.

Du kan konfigurere følgende typer **Oppslag**-datakilder, avhengig av typen verdi som returneres av en konfigurert regel:

   - Bruk typen **Datamodell\Oppslag** når en modellnummereringsverdi må returneres.
   - Bruk typen **Dynamics 365 Operations\Oppslag** når en programnummereringsverdi eller en [utvidet datatype](../extensibility/extensible-edts.md)-verdi for programmet må returneres.
   - Bruk typen **Formatnummerering\Oppslag** når en formatnummereringsverdi må returneres.

Illustrasjonen nedenfor viser hvordan en formatnummerering kan konfigureres i ER-eksempelformatet.

   ![Viser en formatnummerering som et grunnlag for den konfigurerte oppslagsdatakilden](./media/er-lookup-data-sources-img1.gif)

Illustrasjonen nedenfor viser formatkomponentene som ble konfigurert til å rapportere forskjellige typer avgifter i en annen del av en generert rapport.

   ![Viser formatdelene for å rapportere forskjellige typer avgifter separat](./media/er-lookup-data-sources-img2.png)

Illustrasjonen nedenfor viser hvordan ER-operasjonsutforming tillater tilføyelse av en datakilde av typen **Formatnummerering\Oppslag**.  Den tilføyde datakilden konfigureres som returnering av en verdi for `List of taxation levels`-formatnummereringen.

   ![Legge til en ER-datakilde av typen Formatnummerering\Oppslag](./media/er-lookup-data-sources-img3.gif)

Illustrasjonen nedenfor viser hvordan den tilføyde datakilden konfigureres for å bruke **Kode**-feltet i **Model.Data.Tax**-oppføringslisten for **Modell**-datakilden som en parameter som må være angitt for alle konfigurerte regler.

![Konfigurere parametere for den tilføyde datakilden av typen Formatnummerering\Oppslag](./media/er-lookup-data-sources-img4.gif)

Den tilføyde `Model.Data.Tax`-datakilden konfigureres for å angi en avgiftskode for hver konfigurerte regel ved å få tilgang til poster i **TaxTable**-programtabellen.

   ![Gjennomgang av oppslagsdatakilden for ett firmat av typen Formatnummerering\Oppslag](./media/er-lookup-data-sources-img5.gif)

Du kan definere oppslagsreglene for det valgte ER-formatet ved å bruke grensesnittet som automatisk justeres etter strukturen til den konfigurerte datakilden. For øyeblikket krever dette grensesnittet at du for hver regel må angi den returnerte verdien som `List of taxation levels`-verdien for formatnummerering, i tillegg til mva-koden som en parameter.

   ![Sette opp reglene for den konfigurerte datakilden](./media/er-lookup-data-sources-img6.gif)

Illustrasjonen nedenfor viser hvordan `Model.Data.Summary.LevelByLookup`-datakilden av typen **Beregnet felt** kan konfigureres til å kalle den konfigurerte **Oppslag**-datakilden ved å oppgi de nødvendige parameterne. For å behandle dette kallet ved kjøretid går ER gjennom listen over konfigurerte regler i den definerte rekkefølgen for å finne den første regelen som oppfyller betingelsene som er angitt. I dette eksemplet er det regelen som inneholder avgiftskoden som samsvarer med den angitte. Da blir den mest passende regelen funnet, og opplistingsverdien som er konfigurert for regelen som blir funnet, blir returnert av denne datakilden.

> [!NOTE]
> Et unntak opprettes når ingen gjeldende regel blir funnet. Du kan forhindre disse unntakene ved å konfigurere flere regler på slutten av regellisten for å håndtere tilfeller når en ikke-konfigurert verdi eller ingen verdi oppgis. Bruk alternativene **\*Ikke tom\*** og **\*Tom\*** i henhold til dette.  
>
> ![Legge til en datakilde for å kalle den konfigurerte oppslagsdatakilden](./media/er-lookup-data-sources-img7.png)

Når du setter alternativet **Kryssfirma** til **Ja** for den redigerbare oppslagsdatakilden, legger du til en ny påkrevd **Firma**-parameter i settet med parametere for denne datakilden. Verdien til **Firma**-parameteren må angis ved kjøretid når oppslagsdatakilden kalles. Når firmakoden angis ved kjøretid, brukes reglene som er konfigurert for dette firmaet til å finne den mest passende regelen, og den tilsvarende verdien returneres. Illustrasjonen nedenfor viser hvordan du kan gjøre dette og hvordan settet med parametere for den redigerbare datakilden endres.

   ![Gjennomgang av oppslagsdatakilden for kryssfirma av typen Formatnummerering\Oppslag](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Velg hvert firma separat for å konfigurere regelsettet for denne oppslagsdatakilden for det redigerbare ER-formatet. Et unntak inntreffer ved kjøretid når kryssfirmaoppslaget kalles med koden til firmaet som oppslagsinnstillingen ikke ble fullført for.
>
> Pass på at du gir tillatelser for en bruker som kjører ER-formatet med **Oppslag**-datakilden for kryssfirma, for å få tilgang til dataene i hvert firma som er i omfanget av denne datakilden. Ellers opprettes det et unntak ved kjøretid.

De utvidede funksjonene i **Oppslag**-datakildene er tilgjengelige fra versjon 10.0.19. Når du setter alternativet **Utvidet** til **Ja** for den redigerbare oppslagsdatakilden, transformeres den konfigurerte oppslagsdatakilden til den strukturerte datakilden, som tilbyr de ytterligere funksjonene for å analysere det konfigurerte regelsettet. Illustrasjonen nedenfor viser denne transformasjonen.

   ![Gjennomgang av den strukturerte oppslagsdatakilden av typen Formatnummerering\Oppslag](./media/er-lookup-data-sources-img9.gif)

- Underelementet **Oppslag** er utformet som en funksjon for å finne den regelen som passer best, fra settet med konfigurerbare regler basert på settet med parametere som er angitt.
- Underelementet **IsLookupResultSet** er utformet som en funksjon for å godta den angitte verdien av den grunnleggende opplistingsdatakilden, og returnere den *boolske* verdien **Sann** når settet med regler inneholder minst én regel der den angitte opplistingsverdien ble konfigurert som en returnert verdi. Denne funksjonen returnerer den *boolske* verdien **Usann** når det ikke er konfigurert noen regler til å returnere den angitte opplistingsverdien.
- Underelementet **Innstilling** er utformet som en funksjon som returnerer settet med konfigurerte regler som poster i en postliste. De returnerte verdiene og settet med parametere for de konfigurerte reglene presenteres i hver returnerte post som felt for de relevante datatypene:

    - Den returnerte verdien presenteres som **Oppslagsresultat**-feltet.
    - De konfigurerte parameterne presenteres som felt som har navn på parametere (**Kode**-feltet i dette eksemplet).

Hvis du vil ha mer informasjon om hvordan du konfigurerer **Oppslag**-datakilden, kan du se [Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md). Hvis du vil lære hvordan du definerer oppslagsreglene, kan du se [Definere parameterne for et ER-format per juridisk enhet](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md)

[Definere parameterne for et ER-format per juridisk enhet](er-app-specific-parameters-set-up.md)
