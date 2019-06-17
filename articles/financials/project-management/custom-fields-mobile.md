<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="nb-NO">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på IOS og Android</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dette emnet inneholder vanlige mønstre for bruk av utvidelser for implementering av egendefinerte felt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på IOS og Android</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Dette emnet inneholder vanlige mønstre for bruk av utvidelser for implementering av egendefinerte felt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Følgende emner dekkes:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De forskjellige datatypene som det egendefinerte feltrammeverket støtter</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vise skrivebeskyttede eller redigerbare felt i timeregistreringsoppføringer og lagre brukerleverte verdier tilbake til databasen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vise skrivebeskyttede felt i timeregistreringshodet</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Integrere annen egendefinert forretningslogikk for å angi standardverdier i felt og utføre tilleggsvalidering</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Målgruppe</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dette emnet er ment for utviklere som integrerer sine egendefinerte felt i Microsoft Dynamics 365 Project Timesheet-mobilapplikasjonen som er tilgjengelig for Apple iOS og Google Android.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det antas at leserne er kjent med funksjonene for utvikling og prosjekttimeregistrering i X++.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datakontrakt – TSTimesheetCustomField X++-klasse</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Klassen <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> er X++-datakontraktklassen som representerer informasjon om et egendefinert felt for timeregistreringsfunksjonalitet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det blir sendt lister over de egendefinerte feltobjektene både på TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for å vise egendefinerte felt i mobilappen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> – timeregistreringshodekontrakten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> – kontrakten for timeregistreringstransaksjonen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Grupper av disse objektene som har samme prosjektinformasjon og <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept>-verdi, utgjør en linje.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="0" state="translated">fieldBaseType (typer)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Egenskapen <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> i <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept>-objektet bestemmer typen av feltet som vises i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Følgende <bpt id="p1">**</bpt>Typer<ept id="p1">**</ept>-verdier som støttes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="0" state="translated">Typer-verdi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Type</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Notater</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="0" state="translated">Streng (og Opplisting)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Feltet vises som et tekstfelt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Heltall</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verdien vises som et tall uten desimaler.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kommatall</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Verdien vises som et tall med desimaler.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis du vil vise den reelle verdien som en valuta i appen, bruker du <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>-egenskapen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Du kan bruke egenskapen <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> til å angi antall desimaler som vises.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dato</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Datoformater bestemmes av brukerens innstilling for <bpt id="p1">**</bpt>Dato, klokkeslett og nummerformat<ept id="p1">**</ept>, som er angitt under <bpt id="p2">**</bpt>Innstillinger for språk og land/område<ept id="p2">**</ept> i <bpt id="p3">**</bpt>Brukeralternativer<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Boolsk</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis egenskapen <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> ikke er angitt på <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept>-objektet, gis det et fritekstfelt til brukeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Egenskapen <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> kan brukes til å angi den maksimale strenglengden som brukere kan angi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis egenskapen <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> er angitt på <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept>-objektet, er disse listeelementene de eneste verdiene brukerne kan velge ved å bruke alternativknappene (valgknapper).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">I dette tilfellet kan strengfeltet fungere som en opplistingsverdi for brukeroppføring.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis du vil lagre verdien i databasen som en opplisting, kan du manuelt tilordne strengverdien tilbake til opplistingsverdien før du lagrer databasen ved hjelp av kommandokjeden (se delen "Bruke kommandokjede på klassen TSTimesheetEntryService for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="0" state="translated">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Du kan bruke denne egenskapen til å formatere reelle verdier som valuta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne fremgangsmåten gjelder bare når <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept>-verdien er <bpt id="p2">**</bpt>Kommatall<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – Ingen formatering brukes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Formaterer verdien som valuta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Når valutaformatering er aktiv, kan <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept>-feltet brukes til å sende valutakoden som skal vises i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Verdien er en skrivebeskyttet verdi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Feltet <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> inneholder pengebeløpet som skal lagres i databasen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="0" state="translated">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Du kan bruke denne egenskapen til å angi hvor det egendefinerte feltet skal vises i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – Feltet vises i <bpt id="p2">**</bpt>Vis flere detaljer<ept id="p2">**</ept>-delen i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Begge feltene er alltid skrivebeskyttet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – Feltet vil vises etter alle medfølgende linjefelt på timeregistreringsoppføringer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Disse feltene kan enten være redigerbare eller skrivebeskyttet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="0" state="translated">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne egenskapen identifiserer feltet når verdiene som appen gir, lagres tilbake til databasen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="0" state="translated">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Denne egenskapen identifiserer feltet når verdiene som appen gir, lagres tilbake til databasen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="0" state="translated">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sett denne egenskapen til <bpt id="p1">**</bpt>Ja<ept id="p1">**</ept> for å angi at feltet i timeregistreringsdelen skal være redigerbar av brukere.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sett egenskapen til <bpt id="p1">**</bpt>Nei<ept id="p1">**</ept> for å skrivebeskytte feltet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="0" state="translated">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Sett denne egenskapen til <bpt id="p1">**</bpt>Ja<ept id="p1">**</ept> for å angi at feltet i timeregistreringsdelen skal være obligatorisk.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="0" state="translated">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne egenskapen angir etiketten som vises ved siden av feltet i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="0" state="translated">stringOptions (List of Strings)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne egenskapen gjelder bare når <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er satt til <bpt id="p2">**</bpt>Streng<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> er angitt, angis strengverdiene som er tilgjengelige for valg via alternativknapper (valgknapper), av strengene i listen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis ingen strenger angis, tillates fritekstregistrering i strengfeltet (se delen "Bruke kommandokjede på klassen TSTimesheetEntryService for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for et eksempel).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="0" state="translated">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne egenskapen angir den maksimale lengden for et strengfelt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Den gjelder bare når <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er satt til <bpt id="p2">**</bpt>Streng<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne egenskapen angir antall desimaler som vises for et reelt felt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Den gjelder bare når <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> er satt til <bpt id="p2">**</bpt>Kommatall<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne egenskapen kontrollerer i hvilken rekkefølge de egendefinerte feltene vises i appen når mer enn ett egendefinert felt er angitt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Felt som har lavere tall, vises først.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="0" state="translated">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">For felt av typen <bpt id="p1">**</bpt>Boolsk<ept id="p1">**</ept> sender denne egenskapen den boolske verdien for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="0" state="translated">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">For felt av typen <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> sender denne egenskapen den globalt unike identifikatoren (GUID) for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="0" state="translated">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">For felt av typen <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> sender denne egenskapen int64-verdien for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">For felt av typen <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> sender denne egenskapen int-verdien for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="0" state="translated">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">For felt av typen <bpt id="p1">**</bpt>Kommatall<ept id="p1">**</ept> sender denne egenskapen kommatallverdien for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">For felt av typen <bpt id="p1">**</bpt>Streng<ept id="p1">**</ept> sender denne egenskapen strengverdien for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det brukes også for felt av typen <bpt id="p1">**</bpt>Kommatall<ept id="p1">**</ept> som formateres som valuta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">For disse feltene brukes egenskapen til å sende valutakoden til appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="0" state="translated">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">For felt av typen <bpt id="p1">**</bpt>Dato<ept id="p1">**</ept> sender denne egenskapen datoverdien for feltet mellom serveren og appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vise og lagre et egendefinert felt i timeregistreringsdelen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nedenfor vises et skjermbilde fra mobilappen for en timeregistreringsoppretting.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Den viser medfølgende felt og et egendefinert felt i delen "Tidsoppføring" som kalles "Teststreng" med opplistingsverdien "andre alternativ" som allerede er angitt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Egendefinert felt for teststreng i appen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nedenfor vises et skjermbilde fra mobilappen til brukeren som velger et av opplistingsalternativene som er tilgjengelig for det egendefinerte feltet "Teststreng".</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De to alternativene er "Første alternativ" og "Andre alternativ", som vises som alternativknapper.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det andre alternativet er allerede valgt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Alternativknapper (valgknapper) for det egendefinerte feltet Teststreng</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Utvid TSTimesheetLine-tabellen, slik at den har et egendefinert felt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">I vanlige scenarioer er det sannsynlig at dataene for et egendefinert felt i delen timeregistreringsoppføring blir lagret i TSTimesheetLine-tabellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det kan imidlertid brukes andre tabeller hvis dataene kan hentes basert på en TSTimesheetTrans-post som oppgis, eller hvis det ikke finnes en bestemt postkontekst (hvis for eksempel feltet er angitt som skrivebeskyttet i prosjektparameterne).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legg merke til at egendefinerte felt ikke trenger å ha noen reservedatabaseposter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">De kan genereres dynamisk basert på X++-logikk.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne fremgangsmåten kan være nyttig i skrivebeskyttede scenarioer (se delen "Bruke kommandokjede på klassen TSTimesheetDetails, metoden buildCustomFieldListForHeader for å fylle ut timeregistreringsdetaljer" for et eksempel på dynamisk genererte egendefinerte feltverdier.)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Nedenfor vises et skjermbilde fra Visual Studio i applikasjonsobjekttreet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det viser en utvidelse av TSTimesheetLine-tabellen med TestLineString-feltet lagt til som et egendefinert felt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Linjestreng</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bruk kommandokjede på buildCustomFieldList-metoden til TSTimesheetSettings-klassen for å vise et felt i delen timeregistreringsoppføring</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne koden kontrollerer visningsinnstillingene for feltet i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det kontrollerer for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken inndeling feltet vises i.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Følgende eksempel viser et strengfelt på tidsoppføringer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Dette feltet har to alternativer, <bpt id="p1">**</bpt>Første alternativ<ept id="p1">**</ept> og <bpt id="p2">**</bpt>Andre alternativ<ept id="p2">**</ept>, som er tilgjengelige via alternativknapper (valgknapper).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Feltet i appen er knyttet til <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept>-feltet som legges til i TSTimesheetLine-tabellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legg merke til bruken av <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept>-metoden for å forenkle initialiseringen av de egendefinerte feltegenskapene: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> og <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Du kan også angi disse parameterne manuelt slik du vil.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Bruke kommandokjede på buildCustomFieldListForEntry-metoden til TSTimesheetEntry-klassen for å angi verdier i en timeregistreringsoppføring</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Metoden <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> brukes til å angi verdier på de lagrede timeregistreringslinjene i mobilappen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Den bruker en TSTimesheetTrans-post som en parameter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Felt fra denne posten kan brukes til å fylle ut den egendefinerte feltverdien i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Bruk kommandokjeden på TSTimesheetEntryService-klassen til å lagre en timeregistreringsoppføring fra appen tilbake til databasen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis du vil lagre et egendefinert felt tilbake til databasen i vanlig bruk, må du utvide flere metoder:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Metoden <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> brukes til å fastsette om linjeposten er endret av brukeren i appen og må lagres til databasen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis ytelse ikke er av betydning, kan denne metoden forenkles, slik at den alltid returnerer <bpt id="p1">**</bpt>sann<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Metodene <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> og <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> kan utvides, slik at de angir verdier i TSTimesheetLine-databaseposten fra TSTimesheetEntry-datakontraktposten som er angitt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">I eksemplet nedenfor ser du hvordan tilordningen mellom databasefeltet og oppføringsfeltet utføres manuelt via via X++-kode.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Metoden <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> kan også utvides hvis det egendefinerte feltet som er tilordnet <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept>-objektet, må skrive tilbake til TSTimesheetLineweek-databasetabellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Det følgende eksemplet lagrer verdien <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> eller <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> som brukeren velger, i databasen som en rå-strengverdi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis databasefeltet er et felt av typen <bpt id="p1">**</bpt>Opplisting<ept id="p1">**</ept>, kan disse verdiene tilordnes til en opplistingsverdi manuelt og deretter lagres til et opplistingsfelt i databasetabellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Vise et egendefinert felt i topptekstdelen for timeregistrering</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Nedenfor vises et skjermbilde fra mobilappen til en bruker som viser en timeregistrering.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Knappen "Mer informasjon" er valgt i øvre høyre hjørne for å vise alternativet "Vis flere detaljer".</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Vis flere detaljer-kommando</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Nedenfor vises et skjermbilde fra mobilappen som viser "Mer"-delen av en timeregistrering.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Et egendefinert felt kalt "Utnyttelsesrate for denne timeregistreringen (beregnet egendefinert felt)" er lagt til i topptekstdelen for timeregistrering.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">En skrivebeskyttet verdi på "0,667" angis for det egendefinerte feltet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Mer-del</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Utvid TSTimesheetTable-tabellen, slik at den har et egendefinert felt</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">I vanlige scenarioer er det sannsynlig at dataene for et egendefinert felt i topptekstdelen hentes fra TSTimesheetHeader-tabellen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">Det kan imidlertid brukes andre tabeller hvis dataene kan hentes basert på en TSTimesheetTable-post som oppgis, eller hvis det ikke finnes en bestemt postkontekst (hvis for eksempel feltet er angitt som skrivebeskyttet i prosjektparameterne).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Legg merke til at egendefinerte felt ikke trenger å ha noen reservedatabaseposter.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">De kan genereres dynamisk basert på X++-logikk.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Eksemplet nedenfor viser denne fremgangsmåten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Felt i topptekstinndelingen er alltid skrivebeskyttet i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Bruke kommandokjede på buildCustomFieldList-metoden til TSTimesheetSettings-klassen for å vise et felt i topptekstdelen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Denne koden kontrollerer visningsinnstillingene for feltet i appen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Det kontrollerer for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken inndeling feltet vises i.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Følgende eksempel viser en beregnet verdi i hodedelen i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Bruke kommandokjede på buildCustomFieldListForHeader-metoden til TSTimesheetDetails-klassen for å fylle ut timeregistreringsdetaljer</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Metoden <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> brukes til å fylle ut timeregistreringshodedetaljene i mobilappen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Den bruker en TSTimesheetTable-post som en parameter.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Felt fra denne posten kan brukes til å fylle ut den egendefinerte feltverdien i appen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Følgende eksempel leser ikke verdier fra databasen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">I stedet brukes X++-logikk til å generere en beregnet verdi som deretter vises i appen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Andre muligheter for konfigurerbarhet/utvidelse</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Legge til ekstra validering for appen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Eksisterende logikk for timeregistreringsfunksjonalitet på databasenivå vil fremdeles fungere som forventet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis du vil avbryte fullføringen av lagre- eller send-operasjoner og vise en bestemt feilmelding, kan du legge til <bpt id="p1">**</bpt>iverksett feil("melding til bruker")<ept id="p1">**</ept> i koden via en kommandokjedeutvidelse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Her er tre eksempler på nyttige utvidelsesmetoder:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> i TSTimesheetLine-tabellen returnerer <bpt id="p2">**</bpt>usann<ept id="p2">**</ept> under en lagringsoperasjon for en timeregistreringslinje, vises en feilmelding i mobilappen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Hvis <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> i TSTimesheetTable-tabellen returnerer <bpt id="p2">**</bpt>usann<ept id="p2">**</ept> under innsending av timeregistrering i appen, vises en feilmelding for brukeren.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Logikk som fyller ut felt (for eksempel <bpt id="p1">**</bpt>Linjeegenskap<ept id="p1">**</ept>) under <bpt id="p2">**</bpt>sett inn<ept id="p2">**</ept>-metoden i TSTimesheetLine-tabellen, vil fortsatt kjøre.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Skjule og merke medfølgende felt som skrivebeskyttet via konfigurasjon</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Fra prosjektparameterne kan du gjøre medfølgende felt skrivebeskyttet eller skjult i mobilappen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Angi alternativene i delen <bpt id="p1">**</bpt>Mobile timeregistreringer<ept id="p1">**</ept> i kategorien <bpt id="p2">**</bpt>Timeregistrering<ept id="p2">**</ept> på siden <bpt id="p3">**</bpt>Parametere for prosjektstyring og regnskap<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Prosjektparametere</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Endre aktivitetene som er tilgjengelige for valg via utvidelser</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Aktivitetene som er tilgjengelige for valg for et prosjekt, fylles ut via metodene <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> og <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> i <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept>-klassen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Du kan bruke kommandokjeden til å endre denne virkemåten, slik at den samsvarer med forretningsscenarioet for aktivitetene som er tilgjengelige for valg for et bestemt prosjekt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Angi en standard prosjektkategori for timeregistreringsoppføringer</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Registrering av en standard prosjektkategori i timeregistreringsoppføringer forekommer på tre nivåer.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Du kan bruke kommandokjeden til å utvide virkemåten på hvilke som helst eller alle disse nivåene for å oppnå den ønskede atferden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Følgende hierarki brukes:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Appen prøver å plassere standardkategori fra prosjektressursen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">Denne standardkategorien er angitt i metodene <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> og <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> i <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept>-klassen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Hvis standardkategorien ikke er angitt på prosjektressursnivå, prøver appen å hente den fra prosjektaktiviteten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Denne standardkategorien angis i metoden <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> i klassen <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Hvis standardkategorien ikke er angitt på prosjektaktivitetsnivå, hentes standardkategorien fra prosjektparametrene.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Denne standardkategorien angis i metoden <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> i klassen <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>