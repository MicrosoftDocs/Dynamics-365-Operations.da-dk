---
title: Oprette ER-krævede konfigurationer til at importere data fra en ekstern fil
description: Følgende trin beskriver, hvordan en bruger i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe ER-konfigurationer for at importere data i Dynamics 365 for Finance and Operations Enterprise Edition-applikationen fra en ekstern fil.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6675f35c9ec163a620e63af32ecdbff02197d3c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551178"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>Oprette ER-krævede konfigurationer til at importere data fra en ekstern fil

[!include [task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe ER-konfigurationer for at importere data i Dynamics 365 for Finance and Operations Enterprise Edition-applikationen fra en ekstern fil. I dette eksempel skal du oprette de nødvendige ER konfigurationer for eksempelfirmaet Litware, Inc. For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "ER Oprette en konfigurationsudbyder og markere den som aktiv". Disse trin kan udføres ved hjælp af USMF-datasættet. Du skal også downloade og gemme følgende filer lokalt ved hjælp af links fra emnet Oversigt over elektronisk rapportering (https://go.microsoft.com/fwlink/?linkid=852550):: 1099model.xml, 1099format.xml, 1099entries.xml, 1099entries.xlsx.

    * ER giver erhvervsbrugere mulighed for at konfigurere processen med at importere eksterne datafiler til tabeller i Dynamics 365 for Finance and OperationsEnterprise Edition i enten. XML eller .TXT-format. Først skal der designes en abstrakt datamodel og en konfiguration af en ER-datamodel til at repræsentere de data, som du importerer. Dernæst skal du definere strukturen af den fil, som du importerer, og den metode, du vil bruge til at overføre dataene fra filen til den abstrakte datamodel. Konfigurationen af det ER-format, der knyttes til den designede datamodel, skal være oprettet for den pågældende abstrakte datamodel. Derefter skal konfigurationen af datamodellen udvides med en tilknytning, der beskriver, hvordan de importerede data bevares som abstrakte datamodeldata, og hvordan de bruges til at opdatere tabeller i Dynamics 365 for Finance and Operations Enterprise Edition.  Konfiguration af ER-datamodellen skal føjes til en ny modeltilknytning, der beskriver bindingen af datamodellen til programmets destinationer.  
    * I følgende scenario vises funktionerne til ER-dataimport. Dette omfatter kreditorposteringer, der spores eksternt og derefter importeres i Dynamics 365 for Finance and Operations Enterprise edition for at blive rapporteret senere i kreditorudligningen for 1099-formularer.   

## <a name="add-a-new-er-model-configuration"></a>Tilføj en ny ER-modelkonfiguration
1. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
    * Kontrollér, at konfigurationsudbyderen for eksempelvirksomheden Litware, Inc. er tilgængelig og markeret som aktiv. Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".   
2. Klik på Rapporteringskonfigurationer.
    * I stedet for at oprette en ny model, der understøtter dataimporten, kan du indlæse filen, 1099model.xml, som du tidligere har downloadet. Denne fil indeholder den brugerdefinerede datamodel af kreditortransaktioner. Denne datamodel er knyttet til de Dynamics 365 for Finance and Operations Enterprise edition-datakomponenter, der er i AOT-dataenheden.   
3. Klik på Udveksling.
4. Klik på Indlæs fra XML-fil.
    * Klik på Gennemse, og naviger til filen 1099model.xml, som du tidligere har downloadet.  
5. Klik på OK.
6. Vælg "1099-betalingsmodel" i træet.

## <a name="review-data-model-settings"></a>Gennemgå datamodelindstillinger
1. Klik på Designer.
    * Denne model er udviklet til at vise kreditorens transaktioner fra virksomhedens synspunkt og er adskilt fra implementeringen i Dynamics 365 for Finance and Operations Enterprise edition.   
2. Udvid "1099-MISC" i træet.
3. Vælg "1099-MISC\Transaktioner" i træet.
4. Udvid "1099-MISC\Transaktioner" i træet.
    * Transaktionselementet i denne model viser de individuelle transaktioner. De underordnede elementer bruges til at angive de nødvendige oplysninger, som kreditorkonto- og transaktionsdato for hver transaktion.   
5. Luk siden.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Tilføj en ny ER-formatkonfiguration, der understøtter dataimport
    * Trinnene i denne underopgave viser, hvordan der kan oprettes en ny formatkonfiguration til at administrere import af data fra eksterne filer.   
1. Klik på Opret konfiguration for at åbne dialogboksen.
2. Skriv "Format baseret på datamodel 1099-betalingsmodel" i feltet Ny.
3. Vælg Ja i feltet Understøtter dataimport.
4. Tryk på tasten ESC for at lukke denne side.
    * I stedet for at oprette et nyt format, der understøtter dataimporten, kan du indlæse filen 1099format.xml, som du tidligere har downloadet. Denne fil indeholder den definerede struktur på den fil, du importerer, og tilknytningen af strukturen til den brugerdefinerede datamodel for kreditorers transaktioner.   
5. Klik på Udveksling.
6. Klik på Indlæs fra XML-fil.
    * Klik på Gennemse, og naviger til filen 1099format.xml, som du tidligere har downloadet.  
7. Klik på OK.
8. Udvid "1099-betalingsmodel" i træet.
9. Vælg "1099-betalingsmodel\Format for import af kreditorers posteringer" i træet.

## <a name="review-format-settings"></a>Gennemse formatindstillinger
1. Klik på Designer.
2. Slå "Vis detaljer" til.
3. Klik på Udvid/skjul.
4. Klik på Udvid/skjul.
    * Det designede format repræsenterer den forventede struktur i den eksterne fil. Denne fil skal være i XML-format og have udligningsrodelementet. Hver kreditortransaktion er repræsenteret med det transaktionselement, der er defineret til at have en nul-til-mange multiplicitet. Dette betyder, at den indgående fil kan indeholde mellem nul og mange transaktioner. Indlejrede elementer i elementet "transaktion" repræsenterer attributter for en enkelt transaktion. Bemærk, at alle attributter, undtagen land, er markeret som obligatoriske, hvilket betyder, at de skal være i importfilen.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Gennemse indstillingerne for formattilknytningen til datamodellen
1. Klik på Knyt format til model.
    * Tilknytningen "For import af kreditorers transaktioner" indeholder dataoverførselsregler fra den indgående XML-fil til den valgte del af den brugerdefinerede datamodel, der defineres ved at vælge 1099-MISC-definitionen.  
2. Klik på Designer.
3. Slå "Vis detaljer" til.
4. Udvid "format: Post" i træet.
5. Vælg "format: Post" i træet.
    * Bemærk, at det designede format vises her som en datakildekomponent.  
6. Udvid "format: Post\*udligning: XML-element 1..1 (udligning): Post" i træet.
7. Udvid "format: Post\*udligning: XML-element 1..1 (udligning): Post\transaktion: XML-element 0..* (transaktion): Postliste" i træet.
8. Udvid "format: Post\*udligning: XML-element 1..1 (udligning): Post\transaktion: XML-element 0..* (transaktion): Postliste\*kreditor: XML-element 1..1 (kreditor): Post" i træet.
9. Udvid "format: Post\*udligning: XML-element 1..1 (udligning): Post\transaktion: XML-element 0..* (transaktion): Postliste\land: XML-element 0..1 (land): Post" i træet.
10. Vælg "format: Post\*udligning: XML-element 1..1 (udligning): Post\transaktion: XML-element 0..* (transaktion): Postliste\*kreditor: XML-element 1..1 (kreditor): Post" i træet.
    * Bemærk, at præsentationen af obligatoriske og valgfri formateringselementer er forskellig i den foruddefinerede "format"-datakildekomponent.  
11. Udvid "Transaktioner: Postliste = format.settlement.'$enumerated" i træet.
    * Bemærk, at elementerne i det format, der definerer strukturen i den importerede fil, er bundet til elementerne i den brugerdefinerede datamodel. Baseret på disse bindinger gemmes indholdet af den importerede XML-fil på kørselstidspunktet i den eksisterende datamodel. Læg mærke til bindingen af landeelementet. For ethvert transaktionselement i den indgående fil, der ikke har et sådant element, anvendes standardlandekoden "USA" i datamodellen.  
12. Klik på fanen Valideringer.
    * Denne formattilknytning kan indeholde brugerdefineret logik til at kontrollere nøjagtigheden af de importerede data fra en forretningsmæssig betragtning. F.eks. genereres der en advarsel i infologgen baseret på indstillingen for enhver transaktion i importfilen uden en defineret landekode, der oplyser brugeren om sagen med angivelse af transaktionens løbenummer.  
13. Luk siden.

## <a name="run-the-format-mapping-to-the-data-model"></a>Kør formattilknytning til datamodellen
    * Udfør denne formattilknytning af testformål. Brug filen 1099entries.xml, som du tidligere har downloadet. Du kan eksportere denne fil fra projektmappen 1099entries.xlsx, der bruges til at administrere kreditortransaktioner. Det genererede output importeres fra den valgte XML-fil og udfylder den brugerdefinerede datamodel ved den faktiske import.  
1. Klik på Kør.
    * Klik på Gennemse, og naviger til filen 1099entries.xml, som du tidligere har downloadet.  
2. Klik på OK.
    * Bemærk advarslen om en manglende landekode for en transaktion i den importerede fil.  
    * Gennemgå outputtet i XML-format, som viser de data, der er importeret fra den valgte fil og overført til datamodellen.   
3. Luk siden.
4. Luk siden.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Gennemse indstillingerne for modeltilknytningen til destinationerne
1. Vælg "1099-betalingsmodel" i træet.
2. Klik på Designer.
3. Klik på Tilknyt model til datakilde.
    * Tilknytningen for import af manuelle 1099-transaktioner er defineret med retningstypen Til destination. Dette betyder, at den er angivet for at understøtte dataimport og indeholder indstillingen af de regler, der definerer hvordan den importerede eksterne fil og de bevarede abstrakte datamodeldata bruges til at opdatere tabeller i programmet Dynamics 365 for Finance and Operations Enterprise edition.  
4. Klik på Designer.
5. Udvid "model: Datamodel 1099-betalingsmodel" i træet.
6. Udvid "model: Datamodel 1099-betalingsmodel\Transaktioner: Postliste" i træet.
    * Bemærk, at den designede model vises her som et datakildeelement. På kørselstidspunktet indeholder den de data, der importeres fra den eksterne fil. Der blev tilføjet flere tabeller som datakildeelementer for at sikre, at de importerede data er kompatible med dataene i det aktuelle program, herunder om kreditorkontoen for importtransaktionen er tilgængelig i systemet, om kombinationen af de importerende lande- og statskoder findes osv.  
7. Vælg "model: Datamodel 1099-betalingsmodel\Transaktioner: Postliste\$failed: Beregnet felt = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean" i træet.
8. Klik på Rediger.
9. Klik på Rediger formel.
    * Når mindst én validering mislykkes for en enkelt importeret transaktion, markeres denne transaktion som mislykket med datakildeattributten "$failed".  
10. Luk siden.
11. Klik på Annuller.
12. Vælg "tax1099trans: Table 'VendSettlementTax1099'-poster = model.Validated" i træet.
13. Klik på Rediger destination.
    * Denne ER-destination blev tilføjet for at angive, hvordan de importerede data opdaterer programmets tabeller. I denne situation er datatabellen VendSettlementTax1099 valgt. Da posthandlingen Indsæt er valgt, indsættes de importerede transaktioner i tabellen VendSettlementTax1099. Bemærk, at en enkelt modeltilknytning kan indeholde flere destinationer. Det betyder, at de importerede data kan bruges til at opdatere flere af programmets tabeller på én gang. Tabeller, visninger og dataenheder kan bruges som ER-destinationer.   
    * Hvis tilknytningen bliver kaldt fra et punkt i programmet Dynamics 365 for Finance and Operations Enterprise Edition (f.eks. knap eller menupunkt), der er udviklet specifikt til denne handling, skal ER-destinationen markeres som integrationspunktet. I dette eksempel er punktet ERTableDestination#VendSettlementTax1099.  
14. Klik på Annuller.
15. Klik på Vis alle.
16. Klik på Vis kun tilknyttede.
17. Udvid "tax1099trans: Table "VendSettlementTax1099"-poster = model.Validated" i træet.
    * Bemærk, at det datakildeelement, der indeholder de eneste bekræftede transaktioner, er bundet til den oprettede destination. Du kan filtrere de importerede transaktioner for at springe over dem, der ikke er kompatible med programmets data.  
18. Vælg "failed: Table "VendSettlementTax1099Entity"-poster = model.Failed" i træet.
19. Klik på fanen Valideringer.
    * Denne modeltilknytning kan indeholde brugerdefineret logik til at kontrollere nøjagtigheden af de importerede data fra de eksisterende programdata. Baseret på den nuværende indstilling genereres der f.eks. en advarsel i infologgen for enhver transaktion i den importerede fil med en kreditorkonto, der ikke er i systemet, der oplyser brugeren om sagen og angiver den forkerte kreditorkontokode.  
    * Bemærk, at indstillingen Efter-valideringshandling kan bruges til hver validering til at angive, om importen skal fortsættes eller stoppes, såvel som om de allerede udførte indsættelser/opdateringer kan bevares eller skal rulles tilbage.  
20. Klik på Vis kun tilknyttede.
21. Klik på Vis alle.
22. Luk siden.
    * Udfør denne modeltilknytning for at teste det designede format og modeltilknytninger. Brug filen 1099entries.xml. Data fra den valgte fil importeres i systemet.  
23. Klik på Kør.
    * Bemærk, at dialogboksen ikke indeholder nogen yderligere spørgsmål om den formattilknytning, der skal bruges til at fortolke den importerede fil og derefter overføre data til datamodellen. Dette skyldes, at der i øjeblikket kun er ét format, der bruger denne model, der er markeret som designet til at understøtte dataimport.  
    * Definer bilags-id'et for at skelne de importerede transaktioner fra andre transaktioner, der er muligvis allerede er angivet manuelt eller importeret.  
24. I feltet Angiv bilags-id skal du skrive "IMPORT-001".
    * Søg efter filen "1099entries.xml".  
25. Klik på OK.
    * En liste over genererede advarsler indeholder oplysninger om forkerte kreditorkonti, en forkert 1099-rubrik, manglende landekoderne osv. Sammenlign denne liste over advarsler med det indhold, som indgår i kørslen af XML-filen.  
26. Luk siden.
27. Luk siden.
28. Luk siden.
29. Luk siden.
30. Gå til Kreditor > Periodiske opgaver > 1099-skat > Kreditorudligning for 1099.
    * Denne formular viser de samlede transaktioner i tabellen Tax1099Summary, der er oprettet ud fra de importerede transaktioner.  
31. I feltet Fra dato skal du angive datoen til "2000-01-01".
32. Klik på Manuelle 1099-transaktioner.
    * Denne form indeholder en liste over transaktioner, der blev tilføjet manuelt, og dem, vi lige har importeret.  
33. Åbn kolonnefilteret Bilag.
34. Angiv en filterværdi for "IMPORT-001" på feltet "Bilag" ved hjælp af filteroperatoren "begynder med".

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Gennemse forholdet mellem model og formattilknytninger
1. Luk siden.
2. Luk siden.
3. Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.
4. Klik på Rapporteringskonfigurationer.
5. Vælg "1099-betalingsmodel" i træet.
    * Antag, at du vil understøtte import af de samme data, men fra en fil i .TXT-format.   
6. Klik på Opret konfiguration for at åbne dialogboksen. 
7. Skriv "Format baseret på datamodel 1099-betalingsmodel" i feltet Ny.
8. Skriv "Importer data fra TXT-fil" i feltet Navn.
9. Vælg Ja i feltet Understøtter dataimport.
10. Klik på Opret konfiguration.
11. Klik på Designer.
12. Klik på Knyt format til model.
13. Klik på Ny.
14. Indtast eller vælg en værdi i feltet Definition.
    * Vælg en "1099-MISC"-indstilling.  
15. Skriv "Importer data fra TXT-fil" i feltet Navn.
16. Skriv "Importer data fra TXT-fil" i feltet Beskrivelse.
17. Klik på Gem.
18. Luk siden.
19. Luk siden.
20. Klik på Rediger.
    * Hvis du installerede hotfix "KB 4012871 understøttelse af TYSK model-tilknytninger i adskilte konfigurationer med en mulighed for at angive forskellige forudsætninger for at installere dem på forskellige versioner af Dynamics 365 for Finance and Operations Enterprise Edition" (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871), skal du udføre næste trin "Slå flaget 'Standard for model-tilknytning' til" for den angivne formatkonfiguration. Ellers skal du springe næste trin over.  
21. Vælg Ja i feltet Standard for modeltilknytning.
22. Vælg "1099-betalingsmodel" i træet.
23. Klik på Designer.
24. Klik på Tilknyt model til datakilde.
25. Klik på Kør.
    * Hvis du installerede hotfix "KB 4012871 understøttelse af TYSK model-tilknytninger i adskilte konfigurationer med en mulighed for at angive forskellige forudsætninger for at installere dem på forskellige versioner af Dynamics 365 for Finance and Operations, Enterprise Edition (https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871), skal du vælge den foretrukne modeltilknytning i opslagsfeltet. Hvis du endnu ikke har installeret hotfixet, skal du gå til næste trin, da tilknytningen allerede er valgt af definitionen af standardformatkonfigurationen.  
    * Hvis du ikke har installeret hotfixet, KB 4012871, skal du være opmærksom på, at dialogboksen indeholder et yderligere spørgsmål om modeltilknytning, der bruges til at fortolke den fil, du importerer. Dataene overføres derefter fra dialogboksen til datamodellen. I øjeblikket kan du vælge, hvilken formattilknytning der skal anvendes, afhængigt af den filtype du vil importere.  
    * Hvis du planlægger at kalde denne modeltilknytning fra et punkt i Dynamics 365 for Finance and Operations Enterprise edition, der er udviklet specifikt til handlingen, skal ER-destinationen og formattilknytningen være markeret som en del af integrationen.  
26. Klik på Annuller.
27. Luk siden.
28. Luk siden.

