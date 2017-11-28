---
title: "Konfigurer og håndter billeder for Retail Modern POS"
description: "I denne artikel forklares de trin, der er involveret i oprettelse og håndtering af billeder til de forskellige enheder, der vises i Retail Modern POS (MPOS)."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed4a7044b577ed6af86f6803f6abd4f9b500b4e7
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Konfigurer og håndter billeder for Retail Modern POS

[!include[banner](includes/banner.md)]


I denne artikel forklares de trin, der er involveret i oprettelse og håndtering af billeder til de forskellige enheder, der vises i Retail Modern POS (MPOS).

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Konfigurere URL-adresse til mediebase og definere medieskabeloner for at konfigurere formatet for billed-URL-adresser
-------------------------------------------------------------------------------------------------

De billeder, der vises i Retail Modern POS (MPOS), skal være lagret eksternt, uden for Microsoft Dynamics 365 for Retail. De er typisk placeret i et CRM (content management system), CDN (content delivery network) eller på en medieserver. MPOS henter og viser derefter billeder til de relevante enheder som f.eks. produkter og kataloger ved at få adgang til destinations-URL-adressen. Hvis du vil hente disse billeder, der er placeret et eksternt sted, kræver MPOS, at billederne har det rigtige URL-adresseformat. Du kan konfigurere det påkrævede URL-formatet for billederne ved at oprette en værdi for **URL-adresse til mediebase** i kanalprofilen og bruge funktionen **Definer medieskabelon** for hver enhed. Du kan også overskrive standard-URL-formatet for en delmængde af enheder ved hjælp af funktionen **Rediger i Excel**. **Vigtig bemærkning:** I den aktuelle version af Dynamics 365 for Retail kan du ikke længere oprette URL-formatet ved hjælp af **Billede**-attribut-XML til MPOS i attributgruppen **Standard** for enheder. Hvis du er fortrolig med Microsoft Dynamics AX 2012 R3 og nu bruger den aktuelle version af Dynamics 365 for Retail, skal du sørge for altid at bruge den nye funktion **Definer medieskabelon** til at konfigurere billeder. Undlad at bruge eller ændre attributten **Billed** i attributgruppen **Standard** for enheder, herunder produkter. Ændringer, du foretager direkte i attributgruppen **Standard** for billeder, afspejles ikke. Denne indstilling deaktiveres i en fremtidig version. I følgende procedurer er billeder angivet for enheden Katalog som et eksempel. Disse procedurer garanterer, at den korrekte billeddestinationssti er angivet implicit for alle katalogbilleder, der bruger en fælles sti. Hvis du f.eks. har konfigureret en medieserver eller CDN eksternt, og billederne skal vises i MPOS for et givet lager, hjælper funktionen **Definer medieskabelon** dig med at indstille den sti, hvor MPOS kan søge efter og hente billederne. **Bemærk!** I dette eksempel med demodata er medieserveren installeret på Retail Server. Du kan imidlertid have dem hvor som helst uden for Dynamics 365 for Retail.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Konfigurere URL-adresse til mediebase til en kanal

1.  Åbn Dynamics 365 for Retail HQ-portalen.
2.  Klik på **Detail** &gt; **Konfiguration af kanal** &gt; **Kanalprofiler**. [![kanalprofil1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  I den kanalprofil, din butik bruger til MPOS, skal du opdatere feltet **URL-adresse til mediebase** med basis-URL-adressen til din medieserver eller CDN. Basis-URL-adressen er den første del af URL-adressen, der er fælles for billedmapper for forskellige enheder.[![kanalprofil2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Definere medieskabelonen for en enhed

1.  Klik på **Detail** &gt; **Administration af kataloger** &gt; **Katalogbilleder**.
2.  Klik på **Definer medieskabelon** på siden **Katalogbilleder** i handlingsruden. I dialogboksen **Definer medieskabelon** skal du i feltet **Enhed** vælge **Katalog** som standard.
3.  Angiv den resterende sti for billedplaceringen i oversigtspanelet **Mediesti**. Mediestien understøtter **LanguageID** som en variabel. For demodataene kan du for eksempel oprette en **Kataloger**-mappe for alle katalogbilleder under URL-adresse til mediebase til din medieserver (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Du kan have en mappe til hvert sprog, f.eks. da-DK eller fr-FR, og kopiere de relevante billeder i hver mappe. Hvis du ikke har forskellige billeder til de forskellige sprog, kan du udelade variablen **LanguageID** fra din mappestruktur og pege direkte på mappen Kataloger, der indeholder katalogbillederne. **Bemærk:** Den aktuelle version af Dynamics 365 for Retail understøtter **{LanguageId}**-token for enhederne Katalog, Produkt og Kategori. (**{LanguageID}**-tokenen understøttes ikke for enhederne Debitor og Arbejder i henhold til den eksisterende standard, der har været gældende siden Microsoft Dynamics AX 6.x.)
4.  For billeder gælder det, at filnavnformatet er hard-coded til katalognavnet og ikke kan ændres. Omdøb derfor dine billeder, så de har det relevante katalognavn, så du kan sikre, at MPOS håndterer dem korrekt.
5.  I feltet **Filtypenavn** skal du vælge det forventede filtypenavn, afhængigt af hvilken type billeder du har. For demodataene er katalogbillederne for eksempel indstillet til .jpg-filtypenavnet. (Billedfilerne omdøbes også, så de får katalognavne).
6.  Klik på **OK**.
7.  For at kontrollere, at medieskabelon til billeder er blevet gemt korrekt, skal du klikke på  **Definer medieskabelon** på siden **Katalogbilleder**. For at validere skabelonen uden at lukke dialogboksen **Definer medieskabelon** skal du bruge oversigtspanelet **Generér billed-URL-adresser til Excel**. Kontrollere udseendet af billed-URL-adressen, og kontrollér, at URL-adressen er i overensstemmelse med standardskabelonen, der blev nævnt tidligere. Dialogboksen **Definer medieskabelon** har implicit angivet billedstien for alle katalogbilleder, der bruger denne fælles URL-adressesti. Denne URL-sti gælder for alle katalogbilleder, medmindre de overskrives. Den første del af billedstien er taget fra den URL-adresse til mediebase, du har angivet i kanalprofilen. Den resterende del af stien er taget fra den sti, du har defineret i medieskabelonen. De to dele er sammenføjet for at give den fulde URL-adressen til billedets placering. Et katalog i demodataene hedder f.eks. Fabrikam Base Catalog. Procesnavnet skal derfor være Fabrikam Base Catalog.jpg, så den bruger det katalognavn og .jpg-filtypenavn, der er konfigureret i skabelonen. I så fald vil bliver URL-adressen efter sammenføjning være https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg.
8.  Kør synkroniseringsjobbene for at skubbe den nye skabelon til kanaldatabasen, så MPOS kan bruge skabelonen til at få adgang til billederne.
9.  Hvis du vil opdatere medieskabelonen for katalogbilleder på kanalsiden, skal du sørge for at køre **Katalogjob 1150** fra **Retail-IT** &gt; **Distributionsplan**.[![katalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Vise eksempel af et billede fra enhedsniveau
1.  Du kan få vist det billede, der bruger billedets URL-adresse, der er afledt fra medieskabelonen, fra siden for enhedselementet i HQ. I dette eksempel skal du gå til det relevante katalog og derefter klikke på **Medie** &gt; **Billeder** i handlingsruden. Brug rullelisten til at vælge forskellige butikker, der kan have forskellige kanalprofiler.
2.  Hvis du vil redigere eller fjerne den implicitte medieskabelon, skal du vende tilbage til dialogboksen **Definer medieskabelon** på siden **Katalogbilleder**.
3.  Du kan bruge knapperne **Tilføj** og **Fjern** til manuelt at ændre den sti, der er baseret på den implicitte skabelon og anvendt til et bestemt billede. Du kan finde flere oplysninger i afsnittet "Overskrivning af medier skabelonen for enhed varer" senere i denne artikel.
4.  Når du er færdig med at vise et billede og foretage ændringer, du kræver, skal du starte MPOS-forekomsten for den relevante butik og se, om katalogbillederne vises.[![katalog4](./media/catalog4.png)](./media/catalog4.png)

**Bemærk!** Du kan bruge samme procedure for de fem enheder, der understøttes: arbejder, kunde, katalog, kategori og produkter. "Katalogprodukter" (produkter, der er angivet på katalogniveauet) og "Kanalprodukter" (produkter, der er angivet på kanalniveauet) bruger den medieskabelon, der er angivet for produktenheden. Du kan vælge antallet af produktbilleder, der skal vises pr. produkt, for medieskabelonen Produkter. Du kan også angive standardbilledet for et bestemt produkt. På denne måde kan du forhindre tomme billeder i MPOS og styre, hvilket billede der bruges som standardbilledet for en produktvare. Hvert produkt har fem billeder i eksemplet nedenfor, og det første billede er angivet som standardbilledet. Variantprodukter behandles på samme måde som masterprodukter. Filnavnet på billedfilen skal være baseret på produktnummeret. Nogle tegn er også escaped, mens filnavnet genereres. Det er derfor en god ide at kontrollere filnavnet ved at bruge afsnittet **Generér billed-URL-adresser til Excel**. [![prods](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Synkroniseringsjob, der skal sendes til en medieskabelon til kanalsiden
For alle fem understøttede enheder (arbejder, kunder, katalog, kategori og produkter) gælder det, at hver gang du opdaterer dialogboksen **Definer medieskabelon** for at oprette et billede, skal du sørge for, at du kører katalogjobbet (1150) fra **Retail IT** &gt; **Distributionsplan**. Dette job give den opdaterede medieskabelon mulighed for at blive synkroniseret med kanalen og anvendt af MPOS. Kør katalogjobbet (1150), når du foretager en af følgende ændringer:

-   Du opdaterer medieskabelonen til katalogbilledet **Katalogbilleder** &gt; **Definer medieskabelon**.
-   Du opdaterer medieskabelonen til medarbejderbilledet **Medarbejderbilleder** &gt; **Definer medieskabelon**.
-   Du opdaterer medieskabelonen til kundebilledet **Kundebilleder** &gt; **Definer medieskabelon**.
-   Du opdaterer medieskabelonen til produktbilledet **Produktbilleder** &gt; **Definer medieskabelon**.
-   Du opdaterer medieskabelonen til kategoribilledet **Kategoribilleder** &gt; **Definer medieskabelon**. Du skal også publicere kanalen.

## <a name="overwriting-the-media-template-for-entity-items"></a>Overskrive medieskabelonen for enhedselementer
Som du har lært i forrige afsnit, understøtter medieskabelonen for en bestemt enhed kun én fælles sti. Denne sti er baseret på den URL-adresse til mediebase, der er konfigureret, og mediestien, der er defineret. Men i mange tilfælde ønsker en forhandler at kunne bruge billeder fra forskellige kilder for en delmængde af elementer i en enhed. En butik bruger for eksempel en selvhostet medieserver til ét sæt katalogbilleder, men bruger CDN URL-adresser til et andet sæt. Hvis du vil overskrive billed-URL-adresser, der er baseret på en medieskabelon til enhedsbilleder på enhedsniveau, kan du bruge Rediger i Excel og funktionen Manuel redigering på siden **Eksempel**.

### <a name="overwrite-by-using-edit-in-excel"></a>Overskrive ved hjælp af Rediger i Excel

1.  Klik på **Detail** &gt; **Administration af kataloger** &gt; **Katalogbilleder**.
2.  Klik på **Definer medieskabelon** på siden **Katalogbilleder**. I dialogboksen **Definer medieskabelon** skal du i feltet **Enhed** vælge **Katalog**.
3.  Bemærk billedplaceringen i oversigtspanelet **Mediesti**.
4.  Klik på **Generer** i oversigtspanelet **Generér billed-URL-adresser til Excel**. **Vigtigt!** Når medieskabelonen ændres, skal du klikke på **Generer**, før du kan bruge funktionen Rediger i Excel. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Du ser nu et eksempel på billed-URL-adresser, der blev genereret ud fra den senest gemte medieskabelon. [![excel2](./media/excel2.png)](./media/excel2.png) **Bemærk!** De URL-adresser, der er genereret for Excel, bruger stien og konventionerne fra den medieskabelon, der er defineret. Disse konventioner omfatter konventioner for filnavne. Det forventes, at du har konfigureret de fysiske billeder uden for Dynamics 365 for Retail, og billederne kan hentes fra de URL-adresser, der er afledt fra den medieskabelon, du definerede tidligere. Du kan overskrive disse afledte URL-adresser ved hjælp af funktionen Rediger i Excel.
5.  Klik på **Rediger i Excel**.
6.  Når Microsoft Excel-regnearket er åbnet, skal du klikke på **Aktivér redigering**, når du bliver bedt om.
7.  Når du bliver bedt om det, skal du klikke på **Har tillid til dette tilføjelsesprogram** i højre rude og vente på, at installationen af tilføjelsesprogrammet er fuldført. [![Har tillid til dette tilføjelsesprogram](./media/excel4.jpg)](./media/excel4.jpg)
8.  Hvis du bliver bedt om at logge på, kan du angive de legitimationsoplysninger, du brugte til at logge på HQ. [![Logonprompt](./media/excel5.png)](./media/excel5.png)
9.  Når du er logget på, bør du kunne se en liste over billed-URL-adresser til de forskellige katalogposter.
10. Du redigerer, tilføjer og fjerner billed-URL-adresserne for forskellige elementer på enhed.
11. Du kan overskrive billed-URL-adresser for alle enheder undtagen produkter. Rediger den eksisterende billed-URL-adresse, så den bruger den nye URL-adresse til billedet, og opdater filnavnet med det nye filnavn for billedfilen. Filnavnet skal være entydigt for at sikre, at posten er entydig. [![Overskrive billed-URL-adresser i Excel](./media/excel6.jpg)](./media/excel6.jpg) **Bemærk!** Når du overskriver billed-URL-adresser for Produkter-enheder ved hjælp af funktionen Rediger i Excel-funktioner eller enhedselementsiden, viser MPOS altid alle medieskabelonernes billed-URL-adresser med de overskrevne billed-URL-adresser.
12. Når du har foretaget dine ændringer, skal du klikke på **Udgiv i Excel** for at oprette en ny eksplicit tilknytningspost.
13. Gå tilbage til HQ, og klik på **OK**.
14. Kør de relevante synkroniseringsjobbet for enheden, og se eksemplet på enhedssiden eller i MPOS.

#### <a name="creating-new-records"></a>Oprette nye poster

Du kan opretter nye poster i Excel. Sørg imidlertid for, at du angiver de rigtige oplysninger. Hvis du for eksempel vil oprette en ny post til et katalog, skal du sørge for, at katalog-id'et og katalognavnet er korrekt og også angive et entydigt filnavn. Det entydige filnavn er meget vigtigt, fordi entydigheden af poster i Excel valideres ved udgivelsen. Kopier først oplysningerne fra det katalog, du vil oprette en ny post for, og kopier posten. Du skal blot opdatere filnavnet og URL-adressen, da resten af oplysningerne forbliver de samme. Hvis du vil oprette nye poster for Produkt-enhedselementer, skal du bruge den samme grundlæggende fremgangsmåde. Kopiér en eksisterende post for produktet, du vil oprette en ny post for, fra Excel-regnet , og udskrift derefter billed-URL-adressen og -filnavnet. Sørg for, at filnavnet er entydigt.

#### <a name="deleting-an-existing-record"></a>Slette en eksisterende post

Det er kun overskrevne billed-URL-poster, der kan slettes. Når et billede er slettet, og synkroniseringen er fuldført, vises billedet ikke længere på siden **Eksempel** eller i MPOS. Billed-URL-poster, der er afledt fra medieskabelonen, kan ikke slettes, fordi disse poster altid hver gang er afledt fra medieskabelonen.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Overskrive fra eksempelsiden på enhedsniveau

For alle enheder med undtagelse af produkter gælder det, at du kan overskrive billed-URL-adressen for et givet enhedselement på enhedselementniveauet på siden **Eksempel**. Brug enhedssiden "Katalogprodukter" til Produkter. Dette eksempel viser, hvordan du overskriver et katalogbillede.

1.  Klik på **Kataloger** &gt; **Medie** &gt; **Billeder**, og vælg det katalogbillede, der skal opdateres.
2.  Klik på **Tilføj**, og angiv billedets URL-adresse for at overskrive URL-adressen til medieskabelonen.
3.  Hvis dette billede skal vises i MPOS for kataloget, kan du angive det som standardbilledet.
4.  Klik på **OK**. Billedets URL-adresse er opdateret for dette katalogbillede, og der vises et eksempel. [![forhåndsvisning3](./media/preview3.png)](./media/preview3.png)
5.  Du kan også se billedeksemplet for alle overskrevne billed-URL-adresser på gallerisiden **Katalogbilleder**.

**[![forhåndsvisning4](./media/preview-4.png)](./media/preview-4.png) Bemærk!** Galleriet viser i øjeblikket ikke billedeksempler for billed-URL-adresser til medieskabeloner. For enhederne Katalog, Arbejder, Debitor og Kategori og gælder det, at hvis brugeren eksplicit angiver en URL-adresse via denne side, anbefaler vi, at du angiver, hvilket billede der er standardbilledet, da Retail Server-klienter kun ét billede pr. katalog, debitor, arbejder og kategori. Hvis brugeren ikke angiver et standardbillede, bestemmer systemet standardbilledet og sender den til detailtjenestekaldefunktionen (MPOS eller Ecommerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Overskrive billedets URL-adresse for katalogbilleder fra eksempelsiden

Hvis du vil overskrive URL-adresse for katalogproduktbilleder, skal du bruge siden **Eksempel**. Du kan ikke bruge funktionen Rediger i Excel.

1.  Hvis du vil overskrive produktbilleder på et katalogniveau, skal du vælge et katalog og derefter vælge det produkt, billedet skal overskrives for.
2.  Klik på **Attributter**.
3.  Vælg **billede** på den næste side, og klik derefter på **Rediger**. Siden **Eksempel** åbnes som en skyderdialogboks.
4.  Klik på **Tilføj**, og Overskriv billedets URL-adresse med en ny URL-adresse.
5.  Klik på **OK**. Du kan nu se eksemplet på det nye billede og kan angive det som standardbilledet.

**[![kat3](./media/cat3.png)](./media/cat3.png) Bemærk!** Når kategoribilledet er blevet tilknyttet, skal du udgive kanalen og køre kanaljobbet for at sikre, at ændringerne udgives i kanaldatabasen.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Konfigurere billeder, der skal vises i offlinetilstand for MPOS
MPOS kan køre i onlinetilstand (når MPOS har oprettet forbindelse til Retail Server) eller i offlinetilstand (når der er ingen Retail Server eller netværksforbindelse, og transaktioner er gemt i en lokal offlinedatabase). Når MPOS kører i offlinetilstand, kan den ikke hente billeder fra den eksterne billedserveren for at vise Retail-Server, fordi Retail Server-forbindelsen blev afbrudt. Du kan imidlertid stadig oprette billeder, så de vises, når MPOS køres i offlinetilstand.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Konfigurere produktbilleder, der skal vises i offlinetilstand for MPOS

De produktbilleder, der skal bruges i offlinetilstand, kan konfigureres ved at overføre det nødvendige fysiske billede til det grundlæggende produktbillede.

1.  Klik på **Administration af produktoplysninger** &gt; **Produkter** &gt; **Produkter**.
2.  Vælg det produkt, offlinebilledet skal indstilles for.
3.  Klik på **Rediger**, og klik derefter på pilen i højre hjørne for at få vist den højre rude.
4.  I oversigtspanelet **Produktbillede** skal du klikke på **Skift billede** og overføre det fysiske billede, der skal bruges til det valgte produkt i offlinetilstand.
5.  Gem og luk siden.
6.  Mens MPOS er i onlinetilstand, skal katalogjobbet køres i HQ for at sikre, at dataene sendes mindst én gang til offlinedatabasen.
7.  Sæt MPOS i offlinetilstand. Du skulle nu kunne se det billede, du overførte for det specifikke produkt i HQ. [![offline1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Konfigurere katalog-, kategori-, medarbejder- og debitorbilleder, der skal vises i offlinetilstand for MPOS

Katalog-, kategori-, arbejder og debitorbilleder, der skal bruges i offlinetilstand, kan konfigureres ved at tilføje det krævede billedes destinationslink til galleriet og indstille billedet som standardbilledet for den valgte enhed.

1.  Gå til kataloget, og klik derefter på **Medie** &gt; **Billeder** i handlingsruden.
2.  Følg trinnene i afsnittet "**Overskriv fra eksempelsiden på enhedsniveau**" for at tilføje URL-adressen til det eksterne billede.
3.  Marker billedet som standardbilledet for kataloget ved at markere afkrydsningsfeltet i forhold til det billede, der vises i gitteret.
4.  Kør katalogjobbet. Dette billede bruges nu som et offlinebillede for det katalog i MPOS.
5.  Følg en lignende proces for andre enheder som f.eks. kategori, medarbejder og debitor.

[![offline2](./media/offline2.png)](./media/offline2.png)    




