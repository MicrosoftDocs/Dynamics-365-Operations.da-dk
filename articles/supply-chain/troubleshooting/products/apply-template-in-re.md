---
title: Du kan ikke anvende en skabelon på et frigivet produkt
description: Du kan ikke anvende en skabelon på et frigivet produkt.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026364"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Du kan ikke anvende en skabelon til at oprette et frigivet produkt

KB-nummer: 4612097

## <a name="symptoms"></a>Symptomer

Når du opretter et nyt frigivet produkt ved hjælp af dialogboksen **Nyt frigivet produkt**, kan du vælge en skabelon. Skabelonen skal indeholde standardindstillinger for mange felter i det nye frigivne produkt. Nogle eller alle felter er dog ikke indstillet, når du har valgt skabelonen.

## <a name="cause"></a>Årsag

På mange sider i Microsoft Dynamics 365 Supply Chain Management kan du oprette en skabelon, der fastlægger de første indstillinger for de poster, der vises på disse sider. Du kan oprette en af disse skabeloner ved at vælge **Postoplysninger** under fanen **Indstillinger** i handlingsruden. Frigivne produkter er dog meget mere komplekse end de fleste andre typer poster. Du kan vælge **Postoplysninger** på siden **Frigivne produkter** for at oprette en skabelon, og selvom du kan vælge denne skabelon, når du opretter et frigivet produkt, indeholder skabelonen ikke de forventede feltværdier for det nye frigivne produkt. Derfor kan du ikke bruge skabeloner med "postoplysninger" til frigivne produkter. Du skal i stedet oprette dedikerede produktskabeloner.

## <a name="resolution"></a>Løsning

Når du vil oprette en produktskabelon, skal du bruge menuen **Skabelon** under fanen **Produkt** i handlingsruden og ikke knappen **Postoplysninger** under fanen **Indstillinger**.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg **Skabelon** under fanen **Produkt** i gruppen **Ny** i handlingsruden, og vælg derefter enten **Opret personlig skabelon** eller **Opret delt skabelon** efter behov.
