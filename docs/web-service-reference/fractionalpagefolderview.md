---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: Das FractionalPageFolderView-Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Ordnern, die in einer FindFolder-Anforderung zurückgegeben werden.
ms.openlocfilehash: a8627c6277b49655d3933679128b844118633cda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463069"
---
# <a name="fractionalpagefolderview"></a><span data-ttu-id="24656-103">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="24656-103">FractionalPageFolderView</span></span>

<span data-ttu-id="24656-104">Das **FractionalPageFolderView** -Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Ordnern, die in einer [FindFolder](findfolder.md) -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24656-104">The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request.</span></span> 
  
[<span data-ttu-id="24656-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="24656-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="24656-106">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="24656-106">FractionalPageFolderView</span></span>](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="24656-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="24656-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24656-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="24656-108">Attributes and elements</span></span>

<span data-ttu-id="24656-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="24656-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24656-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="24656-110">Attributes</span></span>

|<span data-ttu-id="24656-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="24656-111">**Attribute**</span></span>|<span data-ttu-id="24656-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24656-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24656-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="24656-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="24656-114">Gibt die maximale Anzahl von Ergebnissen an, die in der [FindFolder](findfolder.md) -Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24656-114">Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response.</span></span> <span data-ttu-id="24656-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="24656-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="24656-116">**Zähler**</span><span class="sxs-lookup"><span data-stu-id="24656-116">**Numerator**</span></span> <br/> |<span data-ttu-id="24656-117">Stellt den Zaehler des Bruchs Offsets vom Anfang des Resultsets dar.</span><span class="sxs-lookup"><span data-stu-id="24656-117">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="24656-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="24656-118">This attribute is required.</span></span> <span data-ttu-id="24656-119">Der Zähler muss gleich oder kleiner als der Nenner sein.</span><span class="sxs-lookup"><span data-stu-id="24656-119">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="24656-120">Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer oder gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="24656-120">This attribute must represent an integral value that is equal to or greater than zero.</span></span> <span data-ttu-id="24656-121">Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="24656-121">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="24656-122">**Nenner**</span><span class="sxs-lookup"><span data-stu-id="24656-122">**Denominator**</span></span> <br/> |<span data-ttu-id="24656-123">Stellt den Nenner des Bruchs Offsets vom Anfang der Gesamtzahl der Ordner im Resultset dar.</span><span class="sxs-lookup"><span data-stu-id="24656-123">Represents the denominator of the fractional offset from the start of the total number of folders in the result set.</span></span> <span data-ttu-id="24656-124">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="24656-124">This attribute is required.</span></span> <span data-ttu-id="24656-125">Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="24656-125">This attribute must represent an integral value that is greater than one.</span></span> <span data-ttu-id="24656-126">Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="24656-126">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="24656-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24656-127">Child elements</span></span>

<span data-ttu-id="24656-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="24656-128">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24656-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24656-129">Parent elements</span></span>

|<span data-ttu-id="24656-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="24656-130">**Element**</span></span>|<span data-ttu-id="24656-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24656-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24656-132">FindFolder</span><span class="sxs-lookup"><span data-stu-id="24656-132">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="24656-133">Definiert eine Anforderung zum Identifizieren von Ordnern in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="24656-133">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="24656-134">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="24656-134">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24656-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24656-135">Remarks</span></span>

<span data-ttu-id="24656-136">Der Offset der Seitenansicht vom Anfang der Gruppe gefundener Ordner wird durch einen Bruch beschrieben.</span><span class="sxs-lookup"><span data-stu-id="24656-136">The paged view offset from the start of the set of found folders is described by a fraction.</span></span> <span data-ttu-id="24656-137">Der Bruch, der durch die Attribute **Zaehler** und **Nenner** definiert ist, beschreibt, wo die Informationsseite beginnt.</span><span class="sxs-lookup"><span data-stu-id="24656-137">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="24656-138">Wenn der **Zähler** beispielsweise vier und der **Nenner** gleich fünf ist, beginnt die Seite mit den zurückgegebenen Informationen bei einem Eintrag, der sich auf vier Fünftel der Methode in der Ergebnismenge befand.</span><span class="sxs-lookup"><span data-stu-id="24656-138">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="24656-139">Wenn der Bruch auf 0 (null) ausgewertet wird, wird der Anfang des Resultsets angegeben.</span><span class="sxs-lookup"><span data-stu-id="24656-139">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="24656-140">Wenn der Bruch zu 1 ausgewertet wird, gibt dies das Ende der Ergebnismenge an.</span><span class="sxs-lookup"><span data-stu-id="24656-140">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="24656-141">Der Bruch stellt den Startpunkt der Seite dar, nicht wie viele Ergebnisse in der Ergebnismenge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="24656-141">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="24656-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="24656-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24656-143">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="24656-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24656-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="24656-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="24656-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="24656-145">Schema Name</span></span>  <br/> |<span data-ttu-id="24656-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="24656-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="24656-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="24656-147">Validation File</span></span>  <br/> |<span data-ttu-id="24656-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="24656-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="24656-149">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="24656-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="24656-150">False</span><span class="sxs-lookup"><span data-stu-id="24656-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24656-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24656-151">See also</span></span>



[<span data-ttu-id="24656-152">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24656-152">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="24656-153">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="24656-153">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

