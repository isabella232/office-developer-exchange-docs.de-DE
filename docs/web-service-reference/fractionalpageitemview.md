---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: Das FractionalPageItemView-Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Elementen in einer Anforderung FindItem zurückgegeben.
ms.openlocfilehash: 38c35d2b68dabfca1a43ab034deaf72c47b0ea66
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758534"
---
# <a name="fractionalpageitemview"></a><span data-ttu-id="8281f-103">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="8281f-103">FractionalPageItemView</span></span>

<span data-ttu-id="8281f-104">Das **FractionalPageItemView** -Element wird beschrieben, in der Seitenansicht startet und die maximale Anzahl von Elementen in einer Anforderung [FindItem](finditem.md) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8281f-104">The **FractionalPageItemView** element describes where the paged view starts and the maximum number of items returned in a [FindItem](finditem.md) request.</span></span> 
  
[<span data-ttu-id="8281f-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="8281f-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="8281f-106">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="8281f-106">FractionalPageItemView</span></span>](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="8281f-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="8281f-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8281f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8281f-108">Attributes and elements</span></span>

<span data-ttu-id="8281f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8281f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8281f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="8281f-110">Attributes</span></span>

|<span data-ttu-id="8281f-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8281f-111">**Attribute**</span></span>|<span data-ttu-id="8281f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8281f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8281f-113">**"MaxEntriesReturned"**</span><span class="sxs-lookup"><span data-stu-id="8281f-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="8281f-114">Gibt die maximale Anzahl der in der Antwort [FindItem](finditem.md) zurückzugebender Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="8281f-114">Identifies the maximum number of results to return in the [FindItem](finditem.md) response.</span></span> <span data-ttu-id="8281f-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="8281f-115">This attribute is optional.</span></span> <span data-ttu-id="8281f-116">Wenn dieses Attribut nicht angegeben ist, gibt der Aufruf alle verfügbaren Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="8281f-116">If this attribute is not specified, the call will return all available items.</span></span>  <br/> |
|<span data-ttu-id="8281f-117">**Zähler**</span><span class="sxs-lookup"><span data-stu-id="8281f-117">**Numerator**</span></span> <br/> |<span data-ttu-id="8281f-118">Stellt den Zähler für den Bruch Offset vom Anfang des Resultsets dar.</span><span class="sxs-lookup"><span data-stu-id="8281f-118">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="8281f-119">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8281f-119">This attribute is required.</span></span> <span data-ttu-id="8281f-120">Der Zähler muss kleiner oder gleich der Nenner.</span><span class="sxs-lookup"><span data-stu-id="8281f-120">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="8281f-121">Dieses Attribut muss es sich um einen ganzzahligen Wert darstellen, der gleich oder größer als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="8281f-121">This attribute must represent an integral value that is equal to or greater than zero.</span></span>  <br/> <span data-ttu-id="8281f-122">Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8281f-122">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="8281f-123">**Nenner**</span><span class="sxs-lookup"><span data-stu-id="8281f-123">**Denominator**</span></span> <br/> |<span data-ttu-id="8281f-124">Stellt dar, die als Nenner für den Bruch Offset ab dem Anfang der Gesamtanzahl der Elemente im Resultset.</span><span class="sxs-lookup"><span data-stu-id="8281f-124">Represents the denominator of the fractional offset from the start of the total number of items in the result set.</span></span> <span data-ttu-id="8281f-125">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8281f-125">This attribute is required.</span></span> <span data-ttu-id="8281f-126">Dieses Attribut muss auf einen ganzzahligen Wert darstellen, der größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="8281f-126">This attribute must represent an integral value that is greater than one.</span></span>  <br/> <span data-ttu-id="8281f-127">Weitere Informationen finden Sie unter "Hinweise" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="8281f-127">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8281f-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8281f-128">Child elements</span></span>

<span data-ttu-id="8281f-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="8281f-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8281f-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8281f-130">Parent elements</span></span>

|<span data-ttu-id="8281f-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="8281f-131">**Element**</span></span>|<span data-ttu-id="8281f-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8281f-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8281f-133">FindItem</span><span class="sxs-lookup"><span data-stu-id="8281f-133">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="8281f-134">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="8281f-134">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="8281f-135">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="8281f-135">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8281f-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8281f-136">Remarks</span></span>

<span data-ttu-id="8281f-137">Der Seitenansicht Offset vom Beginn des Satzes von gefundenen Elemente wird durch eine Bruchzahl beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8281f-137">The paged view offset from the start of the set of found items is described by a fraction.</span></span> <span data-ttu-id="8281f-138">Der Anteil, die durch die **Zähler** und **Nenner** Attribute definiert ist, beschreibt, an die Seite mit Informationen beginnt.</span><span class="sxs-lookup"><span data-stu-id="8281f-138">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="8281f-139">Wenn **Zähler** vier und **Nenner** fünf entspricht, befindet die Seite der zurückgegebenen Informationen beginnt am einen Eintrag vier Fünftel die Art und Weise in der Ergebnismenge.</span><span class="sxs-lookup"><span data-stu-id="8281f-139">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="8281f-140">Wenn die Teiler gleich 0 (null) ausgewertet wird, gibt an, dass den Anfang des die Ergebnisse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8281f-140">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="8281f-141">Wenn der Bruchteil eines ergibt, gibt an, dass das Ende des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="8281f-141">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8281f-142">Der Anteil den Anfangspunkt der Seite darstellt, werden nicht wie viele Ergebnisse im Resultset zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8281f-142">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="8281f-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8281f-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="8281f-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8281f-144">Example</span></span>

<span data-ttu-id="8281f-145">Das folgende Beispiel zeigt eine [FindItem](finditem.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8281f-145">The following example shows a [FindItem](finditem.md) request.</span></span> <span data-ttu-id="8281f-146">Die Anforderung gibt Elemente zurück, aus den Suchergebnissen aus, die hinter der zweiten dritte der alle Objekte in der Ergebnismenge gestartet.</span><span class="sxs-lookup"><span data-stu-id="8281f-146">The request returns items from the search results that start after the second third of all the items in the result set.</span></span> 
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="8281f-147">Beispielsweise gibt das Resultset neun Elemente enthält, die Seitenansicht bis zu 12 Elementen, beginnend bei der gefundene Element zwei Drittel der Art und Weise in der Ergebnismenge zurück.</span><span class="sxs-lookup"><span data-stu-id="8281f-147">For example, if the result set contains nine items, the paged view will return up to 12 items, starting at the item found two-thirds of the way in to the result set.</span></span> <span data-ttu-id="8281f-148">In diesem Fall wird die Seite das siebten Element gestartet.</span><span class="sxs-lookup"><span data-stu-id="8281f-148">In this case, the page starts at the seventh item.</span></span> <span data-ttu-id="8281f-149">Die Seite wird die siebte achten und neunten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="8281f-149">The page will contain the seventh, eighth, and ninth items.</span></span> <span data-ttu-id="8281f-150">Wenn der Zähler 0 (null) festgelegt ist, gibt die Seitenansicht alle Elemente zurück, im Resultset als die Anzahl kleiner als das Attribut **"MaxEntriesReturned"** ist.</span><span class="sxs-lookup"><span data-stu-id="8281f-150">If the numerator is set to zero, the page view will return all the items in the result set as long as the number is less than the **MaxEntriesReturned** attribute.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8281f-151">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8281f-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8281f-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="8281f-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8281f-153">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8281f-153">Schema Name</span></span>  <br/> |<span data-ttu-id="8281f-154">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8281f-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8281f-155">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8281f-155">Validation File</span></span>  <br/> |<span data-ttu-id="8281f-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8281f-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8281f-157">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8281f-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="8281f-158">False</span><span class="sxs-lookup"><span data-stu-id="8281f-158">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8281f-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8281f-159">See also</span></span>



[<span data-ttu-id="8281f-160">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8281f-160">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="8281f-161">Finding Items</span><span class="sxs-lookup"><span data-stu-id="8281f-161">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

