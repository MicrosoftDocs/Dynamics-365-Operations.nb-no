---
title: Konfigurere og behandle bilder for moderne salgssted for detaljhandel
description: Denne artikkelen beskriver trinnene som er involvert i oppretting og administrasjon av bilder for de forskjellige enhetene som vises i det moderne salgsstedet for detaljhandel (MPOS).
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: e144b05ec516d297c3cf81081936d306b9cb9026
ms.contentlocale: nb-no
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Konfigurere og behandle bilder for moderne salgssted for detaljhandel

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver trinnene som er involvert i oppretting og administrasjon av bilder for de forskjellige enhetene som vises i det moderne salgsstedet for detaljhandel (MPOS).

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Sette opp primær URL-adresse for media og definere mediemaler for å konfigurere formatet for URL-adresser for bilde
-------------------------------------------------------------------------------------------------

Bildene som vises i moderne salgssted for detaljhandel (MPOS) må være vertsbasert eksternt, utenfor Microsoft Dynamics 365 for Operations - Retail. De er vanligvis vertsbasert i et innholdsbehandlingssystem, et nettverk for innholdslevering (CDN) eller på en mediaserver. MPOS henter og viser deretter bildene for de aktuelle enhetene, for eksempel produkter og kataloger, ved å åpne mål-URL-adressen. For å hente disse eksternt vertsbaserte bildene krever MPOS riktig URL-format for bildene. Du kan konfigurere det nødvendige URL-formatet for bildene ved å sette opp verdien for **Primær URL-adresse for media** i Kanalprofilen og bruke funksjonaliteten **Definer mal for medier** for hver enhet. Du kan også overskrive standard URL-formatet for et delsett av enheter ved hjelp av funksjonaliteten **Rediger i Excel**. **Viktig merknad:** I den gjeldende versjonen av Dynamics 365 for Operations kan du ikke lenger definere URL-formatet ved hjelp av **Bilde**-attributtet XML for MPOS i **Standard**-attributtgruppen for enhetene. Hvis du kjenner til Microsoft Dynamics AX 2012 R3 og nå bruker den gjeldende versjonen av Dynamics 365 for Operations, må du kontrollere at du alltid bruker den nye funksjonaliteten for **Definer mal for medier** til å sette opp bilder. Ikke bruk eller endre **Bilde**-attributtet i **Standard**-attributtgruppen for noen enheter, inkludert produkter. Endringer du gjør direkte i **Standard**-attributtgruppen for bilder gjenspeiles ikke. Dette alternativet deaktiveres i fremtidige versjoner. I prosedyrene nedenfor er bilder definert for enheten Katalog som et eksempel. Disse prosedyrene vil hjelpe med å garantere at den riktige bildemålbanen er implisitt definert for alle katalogbilder som bruker en felles bane. For eksempel hvis du har satt opp en media-server eller CDN eksternt, og vil at bildene skal vises i MPOS for en gitt butikk, hjelper **Definer mal for medier**-funksjonen deg med å sette banen der MPOS kan søke etter og hente bildene. **Obs!** For dette demodataeksemplet er medieserveren distribuert på detaljhandelsserveren. Du kan imidlertid ha den hvor som helst utenfor Dynamics 365 for Operations.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Sette opp primær URL-adresse for media for en kanal

1.  Åpne hurtigmenyen for HQ-portalen for Dynamics 365 for Operations.
2.  Klikk på **Detaljhandel og handel** &gt; **Kanaloppsett** &gt; **Kanalprofiler**. [![Kanalprofil1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  I Kanalprofilen som butikken bruker for MPOS, kan du oppdatere **Primær URL-adresse for media** feltet med den primære URL-adressen for media-serveren eller CDN. Den primære URL-adressen er den første delen av URL-adressen som er felles for alle bildemapper for ulike enheter.[![Kanalprofil2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Definere mediemalen for en enhet

1.  Klikk på **Detaljhandel og handel** &gt; **Katalogadministrasjon** &gt; **Katalogbilder**.
2.  På siden **Katalogbilder**, i handlingsruten klikker du **Definer mal for medier**. I dialogboksen **Definer mal for medier** i feltet **Enhet** skal **Katalog** være valgt som standard.
3.  På **Mediebane** hurtigfanen angir du gjenstående banen til bildeplasseringen. media banen Støtter **Støtter** som en variabel. For demodataene, kan du for eksempel opprette en **Kataloger** mappe for alle katalogbilder under Primær URL-adresse for media for media-serveren (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Du kan deretter har en mappe for hvert språk, for eksempel en-US eller fr-FR, og kopierer de riktige bildene under hver mappe. Hvis du ikke har forskjellige bilder for ulike språk, kan du hoppe over den **LanguageID** variabelen fra mappestrukturen og peke direkte til mappen kataloger som inneholder katalogbildene. **Obs!** den gjeldende versjonen av Dynamics AX støtter den **{LanguageId}** token for katalog-, produkt- og kategorienheter. (Den **{LanguageID}** token støttes ikke for kunde- og arbeiderenheter, i henhold til den eksisterende standarden som er effektive siden Microsoft Dynamics AX 6.x.)
4.  For bilder er filnavnformatet hardkodet til katalognavnet og kan ikke endres. Derfor gi nytt navn til bildene slik at de har riktig katalog-navn, for å garantere at MPOS behandler dem på riktig måte.
5.  I feltet **Filtype** velger du den forventede filtypen, avhengig av hvilken type bilder du har. For eksempel for demodataene er katalogen bildene satt til filtypen JPG. (Bildefilene har også endret navn slik at de har katalognavnene.)
6.  Klikk **OK**.
7.  For å validere at mediemalen for bilder er lagret på riktig måte, på siden **Katalogbilder** klikker du **Definer mal for medier** på nytt. For å validere malen uten å lukke **Definer mal for medier** dialogboksen kan du bruke **Generer bilde-URL-adresser for Excel** hurtigkategorien. Kontroller utseendet på bilde-URL-en, og kontroller at URL-adressen er i samsvar med standard malen som ble nevnt tidligere. Den **Definer mal for medier** dialogboksen har nå definert bildebanen implisitt for alle katalogbilder som bruker denne felles URL-banen. Denne URL-adressen gjelder for alle bilder i katalogen med mindre de overskrives. Den første delen av bildebanen hentes fra Primær URL-adresse for media som du definerte i Kanalprofilen. Den gjenstående delen av banen, hentes fra banen som du definerte i malen for mediet. De to delene slås sammen for å gi fullstendig URL-adressen til bildeplasseringen. En katalog i demodataene kalles for eksempel Fabrikam Base Catalog. Bildenavnet må derfor være Fabrikam Base Catalog.jpg slik at den bruker katalognavnet og JPG-filtypen som er konfigurert i malen. I så fall etter sammenkobling blir URL-adressen https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Kjør synkroniseringsjobbene for å overføre den nye malen til kanaldatabasen, slik at MPOS kan bruke malen til å få tilgang til bildene.
9.  Hvis du vil oppdatere media malen for katalogbilder på kanalsiden, må du huske å kjøre **Catalog Job 1150** fra **IT for detaljhandel** &gt; **Distribusjonsplan**.[![Katalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Forhåndsvisning av et bilde fra enhetsnivå
1.  Du kan forhåndsvise bildet som bruker URL-adressen for bildet som er avledet fra mediemalen fra siden for enhetsvaren i HK. I dette eksemplet kan du gå til den aktuelle katalogen, og deretter i handlingsruten, klikker du på **Medier** &gt; **Bilder**. Bruk fra rullegardinlisten for å velge forskjellige butikker som kan ha forskjellige kanalprofiler.
2.  Hvis du vil redigere eller fjerne den implisitte mediamalen, må du gå tilbake til den **Definer mal for medier** dialogboks for den **Katalogbilder** siden.
3.  Du kan bruke **Legg til** og **Fjern** knappene for å manuelt endre banen som er basert på den implisitte malen og brukes for et bestemt bilde. Hvis du vil ha mer informasjon, se delen "Overskrive media malen for varer i enheten" senere i denne artikkelen.
4.  Når du er ferdig med forhåndsvisning av et bilde og foreta eventuelle endringer du krever, starter du MPOS forekomsten for riktig butikk, og ser om katalogbildene vises.[![Katalog4](./media/catalog4.png)](./media/catalog4.png)

**Obs!** du kan bruke samme fremgangsmåte for alle de fem enhetene som støttes: arbeider, kunde, katalog, kategori og produkter. "Katalogprodukter" (produkter som er angitt på katalognivå) og "Kanalprodukter" (varer som er angitt på kanal-nivå) bruker mediemalen som er angitt for produktenheten. For produktmediemalen kan du velge hvor mange produktbilder som skal vises per produkt. Du kan også angi standardbildet for et bestemt produkt. På denne måten kan du unngå tomme bilder i MPOS og hjelpe med å kontrollere hvilket bilde som brukes som standardbilde for en produktvare. I eksemplet nedenfor har hvert produkt fem bilder, og det første bildet settes som standardbilde. Variantprodukter behandles på samme måte som hovedprodukter. Navnet på bildefilen skal baseres på produktnummer. Noen tegn er også escapet når filnavnet genereres. Det er derfor lurt å kontrollere navnet på filen ved hjelp av delen **Generer bilde-URL-adresser for Excel**. [![Prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Synkroniseringsjobber for å sende en mediemal til kanal-siden
For alle de fem støttede enhetene (arbeider, kunde, katalog, kategori og produkter), når du oppdaterer dialogboksen **Definer mal for medier** for å konfigurere et bilde, må du kontrollere at du kjører Catalog job (1150) fra **IT for detaljhandel** &gt; **Distribusjonsplan**. Denne jobben bil aktivere den oppdaterte mediamalen for synkronisering til kanalen, og bruk av MPOS. Kjør Catalog job (1150) etter at du gjør hvilken som helst av følgende endringer:

-   Du oppdaterer katalogbildemediamalen fra **Katalogbilder** &gt; **Definer mal for medier**.
-   Du oppdaterer ansattbildemediamalen fra **Ansattbilder** &gt; **Definer mal for medier**.
-   Du oppdaterer kundebildemediamalen fra **Kundebilde** &gt; **Definer mal for medier**.
-   Du oppdaterer produktbildemediamalen fra **Produktbilder** &gt; **Definer mal for medier**.
-   Du oppdaterer kategoribildemediamalen fra **Kategoribilder** &gt; **Definer mal for medier**. Du må også publisere kanalen.

## <a name="overwriting-the-media-template-for-entity-items"></a>Overskrive mediemalen for enhetsvarer
Som du lærte i forrige del, støtter media malen for en gitt enhet bare én felles bane. Denne banen er basert på primær URL-adresse for media som er konfigurert, og banen for mediet som er definert. I mange tilfeller vil imidlertid en forhandler skal ønske å bruke bilder fra forskjellige kilder for et delsett med varer i en enhet. For eksempel bruker en butikk medieserveren som egen vert for et sett med katalogbilder, men bruker CDN URL-adresser for et annet sett. Hvis du vil overskrive bilde-URL-adresser som er basert på en mediemal for enhetsbilder på enhetsnivå, kan du bruke kommandoen Rediger i Excel og manuell redigeringsfunksjonalitet fra siden **Forhåndsvisning**.

### <a name="overwrite-by-using-edit-in-excel"></a>Overskrive ved hjelp av Rediger i Excel

1.  Klikk på **Detaljhandel og handel** &gt; **Katalogadministrasjon** &gt; **Katalogbilder**.
2.  På siden **Katalogbilder** klikker du **Definer mal for medier**. I dialogboksen **Definer mal for medier** i feltet **Enhet** skal **Katalog** være valgt.
3.  På **Mediebane** hurtigkategorien legg merke bildeplasseringen.
4.  På den **Generer bilde-URL-adresser for Excel** hurtigkategorien, klikker du **Generer**. **Viktig:** når mediemalen endres, må du klikke **Generer** før du kan bruke funksjonalitet for Rediger i Excel. [![Excel1](./media/excel1.jpg)](./media/excel1.jpg) Du ser nå en forhåndsvisning av bilde URL-adressene som ble generert basert på den siste lagrede media-malen. [![Excel2](./media/excel2.png)](./media/excel2.png) **Obs!** URL-adressene som er generert for Excel, bruker banen og konvensjonene for mediemalen som er definert. Disse konvensjonene inkluderer konvensjoner for filnavn. Forventningen er at du har angitt de fysiske bildene utenfor Dynamics AX, og at bildene kan hentes fra URL-adressene som er avledet fra mediemalen som du tidligere har definert. Du kan overskrive disse avledede URL-adresser ved hjelp av kommandoen Rediger i Excel-funksjonalitet.
5.  Klikk **Rediger i Excel**.
6.  Når Microsoft Excel-regnearket åpnes, klikker du **Aktiver redigering** når du blir bedt om det.
7.  Når du blir bedt om det, klikker du **Klarer tillegget** i høyre rute, og vent til tillegget har fullført installasjonen. [![Klarer tillegget](./media/excel4.jpg)](./media/excel4.jpg)
8.  Hvis du blir bedt om å logge på, Skriv inn påloggingsinformasjonen du brukte til å logge på HK. [![Ledetekst for pålogging](./media/excel5.png)](./media/excel5.png)
9.  Når du har logget på, bør du kunne se en oversikt over bilde URL-adresser for de ulike katalogoppføringene.
10. Du redigere, legge til og fjerne bilde URL-adressene for forskjellige enhetsvarer.
11. Du kan overskrive bilde URL-adressene for alle enheter unntatt produkter. Endre eksisterende bilde-URL-EN, slik at den bruker den nye Måladressen for bildet, og oppdater filnavnet med det nye filnavnet for bildefilen. Filnavnet må være unikt for å garantere at posten er unik. [![Overskrive bilde URL-adresser i Excel](./media/excel6.jpg)](./media/excel6.jpg) **Obs!** Når du overskriver bilde-URL-adresser for produktenheter ved hjelp av kommandoen Rediger i Excel-funksjonalitet eller på enhetsvaresiden, viser MPOS alltid alle bilde-URL-adresser for mediemal sammen med de overskrevne bilde-URL-adressene.
12. Når du har gjort endringene, klikker du **Publiser i Excel** for å opprette en ny eksplisitt tilknytningsoppføring.
13. Gå tilbake til HK, og klikk **OK**.
14. Kjør de riktige synkroniseringsjobber for enheten, og sjekk forhåndsvisningen på enhetssiden eller i MPOS.

#### <a name="creating-new-records"></a>Oppretting av nye poster

Du kan opprette nye poster i Excel. Kontroller imidlertid at du oppgir riktig informasjon. Hvis du for eksempel vil opprette en ny oppføring for en katalog, må du kontrollere at katalog-IDen og katalognavn er riktige, og også gi et unikt navn. Unikt filnavn er svært viktig, fordi unikheten i poster i Excel blir validert under publisering. Kopier først detaljene fra katalogen som du vil opprette en ny post for, og kopier posten. Du må bare oppdatere filnavn og URL-adresse, fordi resten av informasjonen skal være den samme. Hvis du vil opprette nye produktenhetsvarer, bruker du den samme grunnleggende prosedyren. Kopier en eksisterende oppføring for produktet som du vil opprette en ny oppføring for, fra Excel-regnearket, og erstatt deretter bilde URL-adresse og filnavn. Kontroller at filnavnet er unikt.

#### <a name="deleting-an-existing-record"></a>Slette en eksisterende oppføring

Bare de overskrevne bilde URL-adressene kan slettes. Når et bilde er slettet og synkroniseringen er fullført, vil bildet ikke lenger vises på den **Forhåndsvisning** siden eller i MPOS. Bilde URL-adresseposter som er avledet fra mediemalen, kan ikke slettes, fordi disse postene er alltid avledet fra mediemalen hver gang.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Overskrive fra forhåndsvisningsside på enhetsnivå

For alle enheter unntatt produkter, kan du overskrive bilde URL-adressen for en gitt enhetsvare på enhetsvarenivå fra den **Forhåndsvisning** side. Du kan bruke enhetssiden "Katalogprodukter" for produkter. Dette eksemplet viser hvordan du skriver over et bilde i katalogen.

1.  Klikk på **Kataloger** &gt; **Medier** &gt; **Bilder**, og velg katalogbildet for å oppdatere.
2.  Klikk **Legg til**, og angi bilde-URL-EN for å overskrive mediamal-URL-adressen.
3.  Hvis du vil at bildet skal vises i MPOS for katalogen, kan du konfigurere den som Outlook-bildet.
4.  Klikk **OK**. Bilde-URL-en blir oppdatert for dette katalogbildet, og det vises en forhåndsvisning. [![Forhåndsvisning3](./media/preview3.png)](./media/preview3.png)
5.  Du kan også se forhåndsvisningen av bildet for alle overskrevne bilde-URL-adresser på **Katalogbilder** gallerisiden.

**[![Forhåndsvisning4](./media/preview-4.png)](./media/preview-4.png)Obs!** For øyeblikket viser ikke galleriet bildeforhåndsvisninger for bilde-URL-adresser for mediemaler. For enhetene katalog, arbeider, kunde og kategori, hvis brukeren eksplisitt angir en URL-adresse fra denne siden, anbefaler vi at du angir hvilket bilde er standardbilde, fordi Detaljhandelsserver-klienter viser bare ett bilde per katalog, kunde, arbeider og kategori. Hvis brukeren ikke angir et standardbilde, bestemmer systemet standardbildet og sender det til Detaljhandelstjeneste anroper (MPOS eller e-handel).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Overskrive bilde-URL-en for katalogproduktbildene fra siden Forhåndsvisning

For å overskrive bilde-URL-ene for katalogproduktbildene må du først bruke siden **Forhåndsvisning**. Du kan ikke bruke kommandoen Rediger i Excel-funksjonalitet.

1.  Hvis du vil overskrive produktbilder på et katalognivå, velger du en katalog, og velg deretter produktet å overskrive bildet for.
2.  Klikk **Attributter**.
3.  På neste side, velger du **Bilde**, og klikk deretter **Rediger**. Siden **Forhåndsvisning** åpnes som en glidebryterdialogboks.
4.  Klikk **Legg til**, og Overskriv bilde-URL-en med en ny URL-adresse.
5.  Klikk **OK**. Du nå se en forhåndsvisning av det nye bildet, og du kan angi det som standardbildet.

**[![Kat3](./media/cat3.png)](./media/cat3.png)Obs!** Etter kategoribildetilknytning må du publisere kanalen og kjøre kanaljobben for å bidra til å garantere at endringene publiseres til kanaldatabasen.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Definere bilder som skal vises i frakoblet modus for MPOS
MPOS kan kjøre i tilkoblet modus (når MPOS er koblet til Retail Server) eller i frakoblet modus (når det er ingen Retail-Server eller nettverkstilkobling, og transaksjonene er lagret i en lokal database frakoblet). Når MPOS kjøres i frakoblet modus, kan den kan ikke hente bilder fra den eksterne bildeserveren å vise fra Retail-Server, fordi Retail servertilkoblingen er brutt. Men kan du fremdeles sette opp bilder slik at de vises når MPOS kjøres i frakoblet modus.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Definere produktbilder som skal vises i frakoblet modus for MPOS

Produktbilder som må brukes i frakoblet modus kan defineres ved å laste opp nødvendige fysiske bilder inn i grunnlagsproduktbildet.

1.  Klikk på **Produktinformasjonsbehandling** &gt; **Produkter** &gt; **Produkter**.
2.  Velg produktet å angi det frakoblede bildet for.
3.  Klikk **Rediger**, og klikk deretter pilen i høyre hjørne for å vise den høyre ruten.
4.  På den **Produktbilde** hurtigkategorien, klikker du **Endre bilde**, og laster opp det fysiske bildet som skal brukes for det valgte produktet i frakoblet modus.
5.  Lagre og lukk siden.
6.  Mens MPOS er i tilkoblet modus, kan du kjøre katalogjobben i HK, for å være sikker på at dataene sendes minst én gang til den frakoblede databasen.
7.  Plasser MPOS i frakoblet modus. Du bør se bildet som du lastet opp for det aktuelle produktet i HK. [![Frakoblet1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Sette opp katalog, kategori, ansatt og kunde bilder som skal vises i frakoblet modus for MPOS

Katalog-, kategori-, ansatt- og kundebilder som skal brukes i frakoblet modus, kan defineres ved å legge til det nødvendige bildets målkobling til galleriet, og angi bildet som standardbildet for den valgte enheten.

1.  Gå til katalogen, og klikk deretter på **Medier** &gt; **Bilder** i handlingsruten.
2.  Følg trinnene i delen "**Overskrive fra forhåndsvisningsside på enhetsnivå**" for å legge til den eksterne URL-adressen.
3.  Merk dette bildet som standardbilde for katalogen ved å velge avmerkingsboksen mot bildet som vises i rutenettet.
4.  Kjør katalogjobben. Dette bildet vil nå brukes som det frakoblede bildet for denne katalogen i MPOS.
5.  Følg en lignende prosess for andre enheter, for eksempel kategori, ansatt og kunde.

[![Frakoblet2](./media/offline2.png)](./media/offline2.png)    




