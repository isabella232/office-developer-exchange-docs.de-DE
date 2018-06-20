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
description: Das FractionalPageFolderView-Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Ordnern in einer Anforderung FindFolder zurückgegeben.
ms.openlocfilehash: 3cb5f8333634a0c484ae3ce6a6256631cff57cc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758531"
---
# <a name="fractionalpagefolderview"></a><span data-ttu-id="403b0-103">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="403b0-103">FractionalPageFolderView</span></span>

<span data-ttu-id="403b0-104">Das **FractionalPageFolderView** -Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Ordnern in einer Anforderung [FindFolder](findfolder.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="403b0-104">The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request.</span></span> 
  
[<span data-ttu-id="403b0-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="403b0-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="403b0-106">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="403b0-106">FractionalPageFolderView</span></span>](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="403b0-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="403b0-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="403b0-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="403b0-108">Attributes and elements</span></span>

<span data-ttu-id="403b0-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="403b0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="403b0-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="403b0-110">Attributes</span></span>

|<span data-ttu-id="403b0-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="403b0-111">**Attribute**</span></span>|<span data-ttu-id="403b0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="403b0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="403b0-113">**"MaxEntriesReturned"**</span><span class="sxs-lookup"><span data-stu-id="403b0-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="403b0-114">Gibt die maximale Anzahl der in der Antwort [FindFolder](findfolder.md) zurückzugebender Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="403b0-114">Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response.</span></span> <span data-ttu-id="403b0-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="403b0-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="403b0-116">**Zähler**</span><span class="sxs-lookup"><span data-stu-id="403b0-116">**Numerator**</span></span> <br/> |<span data-ttu-id="403b0-117">Stellt den Zähler für den Bruch Offset vom Anfang des Resultsets dar.</span><span class="sxs-lookup"><span data-stu-id="403b0-117">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="403b0-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="403b0-118">This attribute is required.</span></span> <span data-ttu-id="403b0-119">Der Zähler muss kleiner oder gleich der Nenner.</span><span class="sxs-lookup"><span data-stu-id="403b0-119">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="403b0-120">Dieses Attribut muss es sich um einen ganzzahligen Wert darstellen, der gleich oder größer als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="403b0-120">This attribute must represent an integral value that is equal to or greater than zero.</span></span> <span data-ttu-id="403b0-121">Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="403b0-121">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="403b0-122">**Nenner**</span><span class="sxs-lookup"><span data-stu-id="403b0-122">**Denominator**</span></span> <br/> |<span data-ttu-id="403b0-123">Stellt dar, die als Nenner für den Bruch Offset ab dem Anfang der Gesamtzahl der Ordner im Resultset.</span><span class="sxs-lookup"><span data-stu-id="403b0-123">Represents the denominator of the fractional offset from the start of the total number of folders in the result set.</span></span> <span data-ttu-id="403b0-124">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="403b0-124">This attribute is required.</span></span> <span data-ttu-id="403b0-125">Dieses Attribut muss auf einen ganzzahligen Wert darstellen, der größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="403b0-125">This attribute must represent an integral value that is greater than one.</span></span> <span data-ttu-id="403b0-126">Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="403b0-126">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="403b0-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="403b0-127">Child elements</span></span>

<span data-ttu-id="403b0-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="403b0-128">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="403b0-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="403b0-129">Parent elements</span></span>

|<span data-ttu-id="403b0-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="403b0-130">**Element**</span></span>|<span data-ttu-id="403b0-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="403b0-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="403b0-132">FindFolder</span><span class="sxs-lookup"><span data-stu-id="403b0-132">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="403b0-133">Definiert eine Anforderung zum Ordner in einem Postfach zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="403b0-133">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="403b0-134">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="403b0-134">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="403b0-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="403b0-135">Remarks</span></span>

<span data-ttu-id="403b0-136">Der Seitenansicht Offset vom Beginn des Satzes mit gefundenen Ordnern wird durch eine Bruchzahl beschrieben.</span><span class="sxs-lookup"><span data-stu-id="403b0-136">The paged view offset from the start of the set of found folders is described by a fraction.</span></span> <span data-ttu-id="403b0-137">Der Anteil, die durch die **Zähler** und **Nenner** Attribute definiert ist, beschreibt, an die Seite mit Informationen beginnt.</span><span class="sxs-lookup"><span data-stu-id="403b0-137">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="403b0-138">Wenn **Zähler** vier und **Nenner** fünf entspricht, befindet die Seite der zurückgegebenen Informationen beginnt am einen Eintrag vier Fünftel die Art und Weise in der Ergebnismenge.</span><span class="sxs-lookup"><span data-stu-id="403b0-138">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="403b0-139">Wenn die Teiler gleich 0 (null) ausgewertet wird, gibt an, dass den Anfang des die Ergebnisse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="403b0-139">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="403b0-140">Wenn der Bruchteil eines ergibt, gibt an, dass das Ende des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="403b0-140">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="403b0-141">Der Anteil den Anfangspunkt der Seite darstellt, werden nicht wie viele Ergebnisse im Resultset zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="403b0-141">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="403b0-142">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="403b0-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="403b0-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="403b0-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="403b0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="403b0-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="403b0-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="403b0-145">Schema Name</span></span>  <br/> |<span data-ttu-id="403b0-146">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="403b0-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="403b0-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="403b0-147">Validation File</span></span>  <br/> |<span data-ttu-id="403b0-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="403b0-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="403b0-149">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="403b0-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="403b0-150">False</span><span class="sxs-lookup"><span data-stu-id="403b0-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="403b0-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="403b0-151">See also</span></span>



[<span data-ttu-id="403b0-152">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="403b0-152">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="403b0-153">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="403b0-153">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

