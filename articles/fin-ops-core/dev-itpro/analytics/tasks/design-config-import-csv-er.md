---
title: Designe ER-konfigurationer til at importere data fra eksterne CSV-filer
description: Brug denne procedure til at designe konfigurationer af elektronisk rapportering for at importere data i en Finance and Operations-app fra en ekstern fil i CSV-format.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b42f0cf8c7260c85d405a5dfdcd50323ffee4d4528b982997a802b859ab8327b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747265"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>Designe ER-konfigurationer til at importere data fra eksterne CSV-filer

[!include [banner](../../includes/banner.md)]

Brug denne procedure til at designe konfigurationer til elektronisk rapportering (ER) for at importere data til programmet fra en ekstern fil i CSV-format. I denne procedure skal du oprette de nødvendige ER konfigurationer for eksempelfirmaet Litware, Inc. For at fuldføre disse trin skal du først fuldføre trinnene i proceduren "ER Oprette en konfigurationsudbyder og markere den som aktiv".

Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler. Disse trin kan udføres ved hjælp af USMF-datasættet.

Du skal også hente og gemme følgende filer lokalt: [Eksempel på elektronisk rapportering i Dynamics 365 Finance](https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Du kan konfigurere en proces til at importere eksterne filer i XML-, TXT- eller CSV-format til tabeller i programmet. Først skal du oprette en abstrakt datamodel, der repræsenterer de importerede data fra en forretningsmæssig betragtning – der oprettes en konfiguration af ER-datamodellen til dette. Derefter skal du definere strukturen for den importerede fil, der knyttes til designede datamodel, som metoden til at overføre data fra filen til den abstrakte datamodel – der oprettes en ER-formatkonfiguration til dette. Derefter skal ER-datamodelkonfigurationen udvides med en ny modeltilknytning, der beskriver, hvordan dataene fra den importerede fil og de bevarede data fra den abstrakte datamodel bruges til at opdatere programtabeller og dataenheder.
    * De følgende trin viser, hvordan eksternt registrerede leverandørers posteringer bliver importeret fra den eksterne CSV-fil til senere brug i kreditorudligningen for 1099-formularer.
    * Kontrollér, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".
2. Klik på Rapporteringskonfigurationer.
3. Anvend filteret '1099-betalingsmodel'. Hvis du allerede har fuldført proceduren "Oprette krævede konfigurationer til import af data fra en ekstern fil til elektronisk rapportering (ER)" og konfigurationen '1099-betalingsmodel' er tilgængelig i konfigurationstræet, skal du springe alle trin i den næste underordnede opgave.

## <a name="add-a-new-er-model-configuration"></a>Tilføj en ny ER-modelkonfiguration

1. I stedet for at oprette en ny model, der understøtter dataimporten, kan du indlæse filen 1099model.xml, som du tidligere har downloadet. Denne fil indeholder den brugerdefinerede datamodel af kreditortransaktioner. Denne datamodel er allerede knyttet til de nødvendige datakomponenter.
2. Klik på Udveksling.
3. Klik på Indlæs fra XML-fil.
4. Klik på Gennemse, og naviger til filen 1099model.xml, som du tidligere har downloadet.
5. Klik på OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Tilføj en ny ER-formatkonfiguration, der understøtter dataimport

1. Vælg "1099-betalingsmodel" i træet.
2. Klik på Opret konfiguration for at åbne dialogboksen.
3. Skriv "Format baseret på datamodel 1099-betalingsmodel" i feltet Ny.
4. Vælg Ja i feltet Understøtter dataimport.
5. Tryk på tasten ESC for at lukke denne side.
    * I stedet for at oprette et nyt ER-format, der understøtter dataimport, kan du indlæse filen 1099formatcsv.xml, som du tidligere har downloadet. Denne fil indeholder det krævede ER-format, der definerer strukturen på den indgående CSV-fil, og tilknytningen af denne struktur til datamodellen for kreditorernes transaktioner.
6. Klik på Udveksling.
7. Klik på Indlæs fra XML-fil.
    * Klik på Gennemse, og naviger til filen 1099formatcsv.xml, som du tidligere har downloadet.
8. Klik på OK.
9. Udvid "1099-betalingsmodel" i træet.
10. Vælg "1099-betalingsmodel\For import af kreditorers transaktioner (CSV)" i træet.

## <a name="review-format-settings"></a>Gennemse formatindstillinger

1. Klik på Designer.
2. Klik på Udvid/skjul.
3. Slå "Vis detaljer" til.
    * Det designede format repræsenterer den forventede struktur i den eksterne fil i CSV-format.
4. Vælg 'Indgående:Fil\Rod: Sekvens' i træet.
    * Indstillingen 'Ny linje - Windows (CR LF)' er valgt i feltet 'Specialtegn' for rodelementet af typen SEKVENS. Baseret på denne indstilling skal hver linje i parsingfilen betragtes som en separat post.
5. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..*` i træet.
    * For Rod\linjeelementet af typen SEKVENS er indstillingen 'Én mange' valgt i feltet 'Multiplicitet'. Baseret på denne indstilling vises mindst én linje i parsingfilen.
6. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case` i træet.
    * Bemærk, at rod\linje\typer-elementet af typen SAG er blevet tilføjet som det element, der er indlejret i rod\linje-sekvensen. Da dette CASE-element indeholder 3 indlejrede sekvenselementer, forudsætter denne indstilling, at vi forventer at opfylde 3 forskellige typer linjer i parsingfilen.
7. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1` i træet.
    * Rod\linje\typer\hoved-elementet af typen SEKVENS indeholder det indlejrede STRENG-element, hvis værdi er defineret som den faste strengværdi. Denne sekvens fortolker overskriftlinjen i parsingfilen.
8. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)` i træet.
    * Rod\linje\typer\post-elementet af typen SEKVENS er konfigureret til at fortolke posteringslinjerne. Bemærk, at tegnindstillingen 'Brugerdefineret afgrænsningstegn' er konfigureret som et komma. Det betyder, at kommaet bruges som separator i et felt for denne type linje i parsingfilen.
    * Bemærk, at der er føjet flere indlejrede elementer med forskellige datatyper til rod\linje\typer\post-elementet til fortolkning af posteringslinjerne som adskilte felter. Bemærk, at indstillingen 'Tilbudsprogram' er konfigureret som 'Ingen'. Det betyder, at i parsingfilen betragtes alle felter af denne type, som om de ikke har omsluttende tegn.
9. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime` i træet.
    * For eksempel er rod\linje\typer\post\TransactionDate-elementet af typen DATETIME konfigureret til at hente posteringens værdi for dato og klokkeslæt fra parsingfilen i formatet 'M/d/åååå'.
10. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1` i træet.
    * Bemærk, at rod\linje\typer\post\CountryCode-elementet af typen STRENG er konfigureret med indstillingen 'Nul én' i feltet 'Multiplicitet'. Med denne indstilling betragtes værdien af feltet CountryCode i parsinglinjen som valgfri.
11. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,)` i træet.
    * Bemærk, at rod\linje\typer\post\bemærkning-elementet af typen SEKVENS er blevet konfigureret med indstillingen 'Alle' i feltet 'Tilbudsprogram' og dobbelte anførselstegn feltet 'Anførselstegn'. Det betyder, at alle felter i denne type linjer i parsingfilen (beskrevet af de indlejrede elementer: tekst af typen STRENG) anses for at være omgivet af dobbelte anførselstegn.
12. Vælg `Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1` i træet.
    * Rod\linje\typer\ikke-fortolket-element af typen SEKVENS er konfigureret til at fortolke de posteringslinjer for den struktur, som ikke svarer til den struktur, der er beskrevet ovenfor, i det overordnede CASE-element.

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Gennemse indstillingen for formattilknytningen til datamodellen

1. Klik på Knyt format til model.
    * Modeltilknytningen 'Tilknytning til model fra CSV-format' beskriver dataflowet for dataoverførslen fra den indgående CSV-file til datamodellen.
2. Klik på Designer.
3. Udvid 'format' i træet.
    * Bemærk, at det designede format vises her som en datakildekomponent.
4. Udvid 'format\Indgående: File(Incoming)' i træet.
5. Udvid 'format\Indgående: File(Incoming)\Rod: Sequence(Root)' i træet.
6. Udvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)` i træet.
7. Udvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)` i træet.
8. Udvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)` i træet.
9. Udvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data` i træet.
10. Udvid `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode)` i træet.
11. Vælg `format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate)` i træet.
    * Bemærk, at de krævede og valgfrie formatelementer, f.eks. TransactionDate og CountryCode, ser anderledes ud i den foruddefinerede 'format'-datakildekomponent.
12. Udvid "Transaktioner= '$both'" i træet.
    * Bemærk, at elementerne i det format, der definerer strukturen i den importerede fil, er bundet til elementerne i datamodellen. Baseret på disse bindinger gemmes indholdet af den importerede CSV-fil på kørselstidspunktet i den eksisterende datamodel. Læg mærke til bindingen af CountryRegion-elementet. For ethvert transaktionselement i den indgående fil, der ikke har en landekodeværdi angivet, anvendes standardlandekoden "USA" i datamodellen.
13. Slå "Vis detaljer" til.
14. Klik på fanen Valideringer.
15. Klik på Søg.
16. Skriv "kreditor" i feltet Søg.
17. Klik på Find næste.
    * Denne formattilknytning kan indeholde brugerdefineret logik til at kontrollere nøjagtigheden af de importerede data fra en forretningsmæssig betragtning. Hvis strukturen i en linje i den importerede fil baseret på indstillingen ikke svarer til hverken hovedlinjens eller posteringslinjens struktur, informerer en advarsel i infologgen brugeren om dette og angiver posteringens løbenummer i filen.
18. Luk siden.

## <a name="run-the-format-mapping"></a>Kør formattilknytningen

Til testformål skal du udføre formattilknytningen ved hjælp af filen 1099entriescsv.csv, som du tidligere har hentet. Det genererede output viser data, der importeres fra den valgte CSV-fil og udfylder den brugerdefinerede datamodel ved den faktiske import.

1. Klik på Kør.
    * Klik på Gennemse, og naviger til filen 1099entriescsv.csv, som du tidligere har downloadet.
2. Klik på OK.
    * Bemærk, advarselsmeddelelserne om linjer, der ikke accepteres. Linje 4 indeholder den indgående værdi, der præsenteres i det ikke-acceptable format, mens linje 7 ikke indeholder posteringsbemærkningsteksten i dobbelte anførselstegn.
    * Gennemgå outputtet i XML-format, som viser de data, der er importeret fra den valgte fil og overført til datamodellen. Bemærk, at alle 7 linjer i den importerede CSV-fil blev behandlet. Linje 1 i de indeholdte felters titel blev sprunget over, 4 transaktioner blev fortolket korrekt, og 2 transaktioner blev genkendt som ikke-gyldige.
3. Luk siden.
4. Luk siden.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]