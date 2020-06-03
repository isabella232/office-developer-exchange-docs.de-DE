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
description: Das FractionalPageItemView-Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Elementen, die in einer FindItem-Anforderung zurückgegeben werden.
ms.openlocfilehash: cbf45838558873dc5846823c2d1b26cf2c8af514
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461310"
---
# <a name="fractionalpageitemview"></a><span data-ttu-id="99a46-103">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="99a46-103">FractionalPageItemView</span></span>

<span data-ttu-id="99a46-104">Das **FractionalPageItemView** -Element beschreibt, wo die ausgelagerte Ansicht beginnt und die maximale Anzahl von Elementen, die in einer [FindItem](finditem.md) -Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="99a46-104">The **FractionalPageItemView** element describes where the paged view starts and the maximum number of items returned in a [FindItem](finditem.md) request.</span></span> 
  
[<span data-ttu-id="99a46-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="99a46-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="99a46-106">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="99a46-106">FractionalPageItemView</span></span>](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="99a46-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="99a46-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99a46-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="99a46-108">Attributes and elements</span></span>

<span data-ttu-id="99a46-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="99a46-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99a46-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="99a46-110">Attributes</span></span>

|<span data-ttu-id="99a46-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="99a46-111">**Attribute**</span></span>|<span data-ttu-id="99a46-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99a46-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99a46-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="99a46-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="99a46-114">Gibt die maximale Anzahl von Ergebnissen an, die in der [FindItem](finditem.md) -Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="99a46-114">Identifies the maximum number of results to return in the [FindItem](finditem.md) response.</span></span> <span data-ttu-id="99a46-115">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="99a46-115">This attribute is optional.</span></span> <span data-ttu-id="99a46-116">Wenn dieses Attribut nicht angegeben wird, gibt der Aufruf alle verfügbaren Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="99a46-116">If this attribute is not specified, the call will return all available items.</span></span>  <br/> |
|<span data-ttu-id="99a46-117">**Zähler**</span><span class="sxs-lookup"><span data-stu-id="99a46-117">**Numerator**</span></span> <br/> |<span data-ttu-id="99a46-118">Stellt den Zaehler des Bruchs Offsets vom Anfang des Resultsets dar.</span><span class="sxs-lookup"><span data-stu-id="99a46-118">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="99a46-119">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="99a46-119">This attribute is required.</span></span> <span data-ttu-id="99a46-120">Der Zähler muss gleich oder kleiner als der Nenner sein.</span><span class="sxs-lookup"><span data-stu-id="99a46-120">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="99a46-121">Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer oder gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="99a46-121">This attribute must represent an integral value that is equal to or greater than zero.</span></span>  <br/> <span data-ttu-id="99a46-122">Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="99a46-122">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="99a46-123">**Nenner**</span><span class="sxs-lookup"><span data-stu-id="99a46-123">**Denominator**</span></span> <br/> |<span data-ttu-id="99a46-124">Stellt den Nenner des Bruchs Offsets vom Anfang der Gesamtzahl der Elemente in der Ergebnisgruppe dar.</span><span class="sxs-lookup"><span data-stu-id="99a46-124">Represents the denominator of the fractional offset from the start of the total number of items in the result set.</span></span> <span data-ttu-id="99a46-125">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="99a46-125">This attribute is required.</span></span> <span data-ttu-id="99a46-126">Dieses Attribut muss einen ganzzahligen Wert darstellen, der größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="99a46-126">This attribute must represent an integral value that is greater than one.</span></span>  <br/> <span data-ttu-id="99a46-127">Weitere Informationen finden Sie weiter unten in diesem Thema unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="99a46-127">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="99a46-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99a46-128">Child elements</span></span>

<span data-ttu-id="99a46-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="99a46-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="99a46-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99a46-130">Parent elements</span></span>

|<span data-ttu-id="99a46-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="99a46-131">**Element**</span></span>|<span data-ttu-id="99a46-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99a46-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99a46-133">FindItem</span><span class="sxs-lookup"><span data-stu-id="99a46-133">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="99a46-134">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="99a46-134">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="99a46-135">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="99a46-135">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99a46-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99a46-136">Remarks</span></span>

<span data-ttu-id="99a46-137">Der Offset der Seitenansicht vom Anfang der Gruppe gefundener Elemente wird durch einen Bruch beschrieben.</span><span class="sxs-lookup"><span data-stu-id="99a46-137">The paged view offset from the start of the set of found items is described by a fraction.</span></span> <span data-ttu-id="99a46-138">Der Bruch, der durch die Attribute **Zaehler** und **Nenner** definiert ist, beschreibt, wo die Informationsseite beginnt.</span><span class="sxs-lookup"><span data-stu-id="99a46-138">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="99a46-139">Wenn der **Zähler** beispielsweise vier und der **Nenner** gleich fünf ist, beginnt die Seite mit den zurückgegebenen Informationen bei einem Eintrag, der sich auf vier Fünftel der Methode in der Ergebnismenge befand.</span><span class="sxs-lookup"><span data-stu-id="99a46-139">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="99a46-140">Wenn der Bruch auf 0 (null) ausgewertet wird, wird der Anfang des Resultsets angegeben.</span><span class="sxs-lookup"><span data-stu-id="99a46-140">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="99a46-141">Wenn der Bruch zu 1 ausgewertet wird, gibt dies das Ende der Ergebnismenge an.</span><span class="sxs-lookup"><span data-stu-id="99a46-141">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="99a46-142">Der Bruch stellt den Startpunkt der Seite dar, nicht wie viele Ergebnisse in der Ergebnismenge zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="99a46-142">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="99a46-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="99a46-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="99a46-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="99a46-144">Example</span></span>

<span data-ttu-id="99a46-145">Das folgende Beispiel zeigt eine [FindItem](finditem.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="99a46-145">The following example shows a [FindItem](finditem.md) request.</span></span> <span data-ttu-id="99a46-146">Die Anforderung gibt Elemente aus den Suchergebnissen zurück, die nach dem zweiten Drittel aller Elemente in der Ergebnismenge beginnen.</span><span class="sxs-lookup"><span data-stu-id="99a46-146">The request returns items from the search results that start after the second third of all the items in the result set.</span></span> 
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="99a46-147">Wenn das Resultset beispielsweise neun Elemente enthält, gibt die ausgelagerte Ansicht bis zu 12 Elemente zurück, beginnend bei dem Element, das zwei Drittel der Methode in zum Resultset gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="99a46-147">For example, if the result set contains nine items, the paged view will return up to 12 items, starting at the item found two-thirds of the way in to the result set.</span></span> <span data-ttu-id="99a46-148">In diesem Fall beginnt die Seite mit dem siebten Element.</span><span class="sxs-lookup"><span data-stu-id="99a46-148">In this case, the page starts at the seventh item.</span></span> <span data-ttu-id="99a46-149">Die Seite enthält das siebte, achte und neunte Element.</span><span class="sxs-lookup"><span data-stu-id="99a46-149">The page will contain the seventh, eighth, and ninth items.</span></span> <span data-ttu-id="99a46-150">Wenn der Zähler auf NULL festgelegt ist, gibt die Seitenansicht alle Elemente in der Ergebnismenge zurück, solange die Zahl kleiner als das **MaxEntriesReturned** -Attribut ist.</span><span class="sxs-lookup"><span data-stu-id="99a46-150">If the numerator is set to zero, the page view will return all the items in the result set as long as the number is less than the **MaxEntriesReturned** attribute.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="99a46-151">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="99a46-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99a46-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="99a46-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="99a46-153">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="99a46-153">Schema Name</span></span>  <br/> |<span data-ttu-id="99a46-154">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="99a46-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="99a46-155">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="99a46-155">Validation File</span></span>  <br/> |<span data-ttu-id="99a46-156">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="99a46-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="99a46-157">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="99a46-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="99a46-158">False</span><span class="sxs-lookup"><span data-stu-id="99a46-158">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99a46-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99a46-159">See also</span></span>



[<span data-ttu-id="99a46-160">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="99a46-160">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="99a46-161">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="99a46-161">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

