---
title: Status for produktlivscyklus
description: En status for produktlivscyklus dokumenter livscyklusstatus for et frigivet produkt eller en produktvariant.
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: cvocph
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 33130a4061f22335aeeffa69c478b693604393a9
ms.openlocfilehash: a57f306ba02c5758c39c4bd29d9a4fa0d7efbcd3
ms.contentlocale: da-dk
ms.lasthandoff: 12/20/2017

---

# <a name="product-lifecycle-state"></a>Status for produktlivscyklus 

[!include[banner](../includes/banner.md)]


En status for produktlivscyklus dokumenter livscyklusstatus for et frigivet produkt eller en produktvariant. Status for produktlivscyklus defineres af brugeren, typisk en produktchef eller produktmasterdatachef. Bestemte virksomhedsprocesser, f.eks. ved varedisponering, kan blive påvirket af en bestemt livscyklusstatus.   
 
Et frigivet produkt eller en produktvariant kan knyttes til en status for produktlivscyklus, der dokumenterer, hvilken livscyklusstatus et bestemt produkt eller en produktvariant har. Du kan definere et ubegrænset antal produktlivscyklusstatusser ved at tildele et tilstandsnavn og en beskrivelse. Du kan vælge én livscyklusstatus som standardstatus for nye frigivne produkter. Frigivne produktvarianter nedarver deres status for produktlivscyklus fra deres frigivne produktmaster ved oprettelse. Når du ændrer livscyklusstatussen for en frigivet produktmaster, kan du vælge at opdatere alle eksisterende varianter, der har samme oprindelige status.  

## <a name="create-a-new-product-lifecycle-state"></a>Opret en ny status for produktlivscyklus 
 
- Når du vil oprette en ny status for produktlivscyklus, skal du afspille eller læse opgaveguiden **Opret en ny status for produktlivscyklus**. 

-  Når du vil oprette en standardstatus for produktlivscyklus, skal du afspille eller læse opgaveguiden **Opret en standardstatus for produktlivscyklus**.   

## <a name="associate-product-lifecycle-states-to-released-products"></a>Knytte status for produktlivscyklus til frigivne produkter  

Der er flere måder til at knytte en status for produktlivscyklus til frigivne produkter eller produktvarianter.

-  Ved oprettelse af et nyt frigivet produkt tildeles **Status for produktlivscyklus**-standarden automatisk. 
-  Ved frigivelse af et produkt til en juridisk enhed tildeles **Status for produktlivscyklus**-standarden automatisk. 
-  Ved frigivelse af en produktvariant til en juridisk enhed tildeles den **Status for produktlivscyklus**, der er knyttet til den frigivne produktmaster i denne juridiske enhed, automatisk til den nye variant. 

Du kan opdatere status for produktlivscyklus manuelt ved hjælp af: 

-    Listesiden **Frigivne produkter** eller **Detaljevisning**. 
-  Listesiden **Frigivne produktvarianter** eller **Detaljevisning**. 
-  Finde forældede produkter eller produktvarianter baseret på behov og tilknytte en livscyklusstatus.  

Du kan finde detaljerede oplysninger om, hvordan du tilknytter statusser for produktlivscyklus, ved at afspille eller læse følgende to opgaveguider.

-  Hvis du vil knytte en status for produktlivscyklus til en frigivet produktmaster, af du afspille eller læse opgaveguiden **Tildel en status for produktlivscyklus til en frigivet produktmaster**. 

-  Hvis du vil knytte en status for produktlivscyklus til et frigivet produkt, af du afspille eller læse opgaveguiden **Tildel en status for produktlivscyklus til et frigivet produkt**. 

## <a name="impact-on-master-planning"></a>Påvirkning af varedisponering 

Statussen for produktlivscyklus har kun ét kontrolflag: **Er aktiv for planlægning**. Som standard er dette indstillet til **Ja** for alle oprettede statusser for produktlivscyklus, men det kan ændres til **Nej**. Når det er indstillet **Nej**, er de tilknyttede frigivne produkter eller frigivne produktvarianter: 

-  Udelukket fra varedisponering. 
-  Udelukket fra beregning af styklisteniveau. 

Du kan finde detaljerede oplysninger om, hvordan du kan bruge statusser for produktlivscyklus til at udelukke produkter fra varedisponering og beregning af styklisteniveau, ved at afspille eller læse opgaveguiden **Opret en status for produktlivscyklus for at udelukke produkter fra varedisponering**.

> [!NOTE]
> Af hensyn til ydeevnen anbefales du at knytte alle forældede frigivne produkter eller produktvarianter, især når du arbejder med ikke-genanvendelige produktkonfigurationsvarianter, til en status for produktlivscyklus, der er deaktiveret for varedisponering.  
 
## <a name="default-migration-import-and-export"></a>Standardoverførsel, - import og -eksport 

Statusser for produktlivscyklus understøttes ikke af dataenheder, og livscyklusstatussen kan ikke indstilles til en variabel status via de frigivne produktdataenheder.

-  Ved overførsel fra tidligere frigivelser er livscyklusstatussen for alle produkter og produktvarianter tom.  
-  Når frigivne produkter importeres via en dataenhed, anvendes standardlivscyklusstatussen ved oprettelse.  
-  Når frigivne produktvarianter importeres via en dataenhed, importeres produktlivscyklusstatussen for den frigivne produktmaster.   
 
## <a name="find-obsolete-products-and-products-variants"></a>Finde forældede produkter og produktvarianter 
 
Du kan køre en simuleringsanalyse for at finde forældede frigivne produkter eller produktvarianter og derefter opdatere deres status for produktlivscyklus. For at finde forældede produkter skal du afspille og læse opgaveguiden **Find forældede produktvarianter, og tildel en status for produktlivscyklus**. Denne opgaveguiden viser, hvordan du finder forældede frigivne produkter eller produktvarianter, og hvordan du knytter en status for produktlivscyklus til de forældede produkter. Guiden viser også, hvordan du kan få vist resultaterne af simuleringen og vurdere, hvor mange produkter og produktvarianter der skal knyttes til en ny status for produktlivscyklus, når du kører opdateringen uden simulering.  
 
Hvis du kører analysen i en simuleringstilstand, vises de produkter og produktvarianter, der er identificeret som forældet, i en bestemt formular, hvor de nemt kan evalueres. Analysen søges efter posteringer og bestemte masterdata for at identificere produkter, der ikke er behov for i en variabel periode, og som ikke har nogen masterdata, der kan medføre behov. Nye frigivne produkter inden for en variabel periode kan udelukkes fra analysen. Når analysesimuleringen returnerer det forventede resultat, kan brugeren køre analysen og indstille en ny status for produktlivscyklus til alle produkter, der er angivet som forældede af analysen.  
 
> [!NOTE]
> Bemærk, at alle analyser og opdateringer skal udføre inden for den samme juridiske enhed.  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Kriterier for valg og opdatering af frigivne produkter eller produktvarianter 
 
Brug følgende kriterier til at vælge og opdatere frigivne produkter og produktvarianter: 

-    Statussen for produktlivscyklus for produktet eller produktvarianten skal være forskellig fra den nye ønskede status. 
-  Produktet eller produktvarianten blev oprettet for nogle dage siden baseret på antallet af dage, du angiver i valgdialogboksen. 
-  Der er ingen åbne produktionsordrer (= status < afsluttet) for produktet eller produktvarianten. 
-  Der er ingen åbne lagertransaktioner (= statusafgang ReservPhysical til QuotationIssue eller statustilgang Registreret til QuotationReceipt) for produktet eller produktvarianten. 
-  Der er ingen lagertransaktioner inden for de sidste dage for produktet eller produktvarianten. 
-  Der er ingen fremtidig behovs- eller forsyningsprognose for produktet eller produktvarianten.  
-  Der er ikke angivet noget minimumlagerniveauet i varedisponering for produktet eller produktvarianten. 
-  Der er ingen aktiv kanban-regel for fast antal for produktet eller produktvarianten.  
-  Der er ingen serviceordrelinje for produktet eller produktvarianten. 
-  Der er ingen aktive eller fremtidige salgs- eller købsaftalelinjer for produktet eller produktvarianten. 
-  Produktet eller produktvarianten bruges ikke i en stykliste, der er knyttet til en ikke-udløbet godkendt styklisteversion for et produkt eller variant, der er aktiv for planlægning.

## <a name="related-topics"></a>Relaterede emner

-  Opret en ny status for produktlivscyklus
-  Oprette en ny standardstatus for produktlivscyklus
-  Tildele en status for produktlivscyklus til en frigivet produktmaster
-  Tildele en status for produktlivscyklus til et frigivet produkt
-  Finde forældede produktvarianter og tildele en status for produktlivscyklus
-  Oprette en status for produktlivscyklus for at udelukke produkter fra varedisponering

