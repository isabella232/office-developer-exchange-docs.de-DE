---
title: AggregateOn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AggregateOn
api_type:
- schema
ms.assetid: 9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb
description: Das AggregateOn-Element darstellt, die Eigenschaft, die verwendet wird, um die Reihenfolge der gruppierten Elemente für eine gruppierte FindItem Resultset zu bestimmen.
ms.openlocfilehash: fe14de23e6a4c90d826200cae927427acfccc3c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757247"
---
# <a name="aggregateon"></a><span data-ttu-id="832c0-103">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="832c0-103">AggregateOn</span></span>

<span data-ttu-id="832c0-104">Das **AggregateOn** -Element darstellt, die Eigenschaft, die verwendet wird, um die Reihenfolge der gruppierten Elemente für eine gruppierte FindItem Resultset zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="832c0-104">The **AggregateOn** element represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span> 
  
- [<span data-ttu-id="832c0-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="832c0-105">FindItem</span></span>](finditem.md)  
- [<span data-ttu-id="832c0-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="832c0-106">GroupBy</span></span>](groupby.md)
- [<span data-ttu-id="832c0-107">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="832c0-107">AggregateOn</span></span>](aggregateon.md)
  
```xml
<AggregateOn>
   <FieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <IndexedFieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <ExtendedFieldURI/>
</AggregateOn>
```
 
<span data-ttu-id="832c0-108">**AggregateOnType**</span><span class="sxs-lookup"><span data-stu-id="832c0-108">**AggregateOnType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="832c0-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="832c0-109">Attributes and elements</span></span>

<span data-ttu-id="832c0-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="832c0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="832c0-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="832c0-111">Attributes</span></span>

|<span data-ttu-id="832c0-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="832c0-112">**Attribute**</span></span>|<span data-ttu-id="832c0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="832c0-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="832c0-114">**Aggregate**</span><span class="sxs-lookup"><span data-stu-id="832c0-114">**Aggregate**</span></span> <br/> | <span data-ttu-id="832c0-115">Gibt den maximalen oder den minimalen Wert der Eigenschaft identifiziert durch das [FieldURI](fielduri.md) -Element, das für die Reihenfolge der Gruppen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="832c0-115">Indicates the maximum or minimum value of the property identified by the [FieldURI](fielduri.md) element that is used for ordering the groups of items.</span></span><br/><br/><span data-ttu-id="832c0-116">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="832c0-116">The following are the possible values:</span></span>  <br/><br/><span data-ttu-id="832c0-117">-Minimum</span><span class="sxs-lookup"><span data-stu-id="832c0-117">- Minimum</span></span>  <br/><span data-ttu-id="832c0-118">-Maximum</span><span class="sxs-lookup"><span data-stu-id="832c0-118">- Maximum</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="832c0-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="832c0-119">Child elements</span></span>

|<span data-ttu-id="832c0-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="832c0-120">**Element**</span></span>|<span data-ttu-id="832c0-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="832c0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="832c0-122">FieldURI</span><span class="sxs-lookup"><span data-stu-id="832c0-122">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="832c0-123">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="832c0-123">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="832c0-124">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="832c0-124">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="832c0-125">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="832c0-125">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="832c0-126">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="832c0-126">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="832c0-127">Bezeichnet die extended MAPI-Eigenschaften zum Abrufen oder festlegen, oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="832c0-127">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="832c0-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="832c0-128">Parent elements</span></span>

|<span data-ttu-id="832c0-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="832c0-129">**Element**</span></span>|<span data-ttu-id="832c0-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="832c0-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="832c0-131">GroupBy</span><span class="sxs-lookup"><span data-stu-id="832c0-131">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="832c0-132">Gibt beliebige Gruppen für FindItem Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="832c0-132">Specifies arbitrary groupings for FindItem queries.</span></span>  <br/> <span data-ttu-id="832c0-133">Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem/GroupBy`</span><span class="sxs-lookup"><span data-stu-id="832c0-133">The following is the XPath expression to this element:  `/FindItem/GroupBy`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="832c0-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="832c0-134">Remarks</span></span>

<span data-ttu-id="832c0-135">Der [Vorgang FindItem](finditem-operation.md) können gruppierte Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="832c0-135">The [FindItem operation](finditem-operation.md) can return grouped results.</span></span> <span data-ttu-id="832c0-136">Innerhalb einer gruppierten Ergebnisse werden alle Elemente, die den gleichen Wert für einen bestimmten Gruppierungseigenschaft aufweisen zusammengefasst und als untergeordnete Elemente dieser Gruppe vorgelegt.</span><span class="sxs-lookup"><span data-stu-id="832c0-136">Within grouped results, all items that have the same value for a given grouping property are gathered together and presented as children of that group.</span></span> <span data-ttu-id="832c0-137">Wenn Sie nach Absender gruppiert, sind beispielsweise alle E-mails organisiert, separate basierend auf in Gruppen, ob sie vom Absender A, B Absender usw. sind.</span><span class="sxs-lookup"><span data-stu-id="832c0-137">For example, if you group by sender, all e-mails are organized into separate groups based on whether they are from sender A, sender B, and so on.</span></span> <span data-ttu-id="832c0-138">Diese Gruppen sind untergeordnete Elemente der Gruppe der Absender.</span><span class="sxs-lookup"><span data-stu-id="832c0-138">These groups are children of the sender group.</span></span> 
  
<span data-ttu-id="832c0-139">Jede dieser Gruppen innerhalb der Gruppe Absender enthält eine Auflistung von Elementen, wie die tatsächlichen e-Mail-Nachrichten, die von einem einzelnen Absender stammt.</span><span class="sxs-lookup"><span data-stu-id="832c0-139">Each of the groups within the sender group contains a collection of items, such as the actual e-mails that came from each sender.</span></span> <span data-ttu-id="832c0-140">Sie können das [SortOrder](sortorder.md) -Element zum Sortieren der Elemente in einer Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="832c0-140">You can use the [SortOrder](sortorder.md) element to sort the items within a group.</span></span> <span data-ttu-id="832c0-141">Sortieren Sie die Eigenschaftswerte eines Elements auf der Grundlage Gruppen müssen Sie jedoch Aggregation verwenden.</span><span class="sxs-lookup"><span data-stu-id="832c0-141">To sort the groups based on an item's property values, however, you must use aggregation.</span></span> 
  
<span data-ttu-id="832c0-142">Mit Aggregation basiert die Reihenfolge der Gruppen auf eine bestimmte Eigenschaft der Elemente in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="832c0-142">With aggregation, the order of groups is based on a specific property of the items within the group.</span></span> <span data-ttu-id="832c0-143">Wenn Sie zum Sortieren der Elemente in einer Gruppe Aggregation verwenden, müssen Sie eine repräsentative-Eigenschaft, um die Gruppen sortieren identifizieren.</span><span class="sxs-lookup"><span data-stu-id="832c0-143">When you use aggregation to sort items within a group, you must identify a representative property by which to sort the groups.</span></span> <span data-ttu-id="832c0-144">Das **AggregateOn** -Element können Sie die repräsentative-Eigenschaft angeben.</span><span class="sxs-lookup"><span data-stu-id="832c0-144">You can use the **AggregateOn** element to specify the representative property.</span></span> 
  
<span data-ttu-id="832c0-145">Wenn eine repräsentative Eigenschaft identifiziert wird, wird das **aggregierte** Attribut verwendet, um anzugeben, ob die Gruppen nach die maximale oder den minimalen Wert der angegebenen Eigenschaft sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="832c0-145">When a representative property is identified, the **Aggregate** attribute is used to indicate whether the groups are sorted according to the maximum or the minimum value of the identified property.</span></span> <span data-ttu-id="832c0-146">Wenn das **Aggregate** -Attribut auf Maximum festgelegt ist, werden die Gruppen sortiert beginnend mit dem größten Wert für die **AggregateOn** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="832c0-146">If the **Aggregate** attribute is set to Maximum, the groups are sorted beginning with the largest value for the **AggregateOn** property.</span></span> <span data-ttu-id="832c0-147">Wenn das **Aggregate** -Attribut auf mindestens festgelegt ist, werden die Gruppen sortiert beginnend mit dem kleinsten Wert für die **AggregateOn** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="832c0-147">If the **Aggregate** attribute is set to Minimum, the groups are sorted beginning with the smallest value for the **AggregateOn** property.</span></span> 
  
<span data-ttu-id="832c0-148">Angenommen, wenn Sie eine gruppierte Abfrage FindItem, ausstellen, Gruppieren nach Absender möchten, aber Sie die Gruppen, damit die Gruppe mit den neuesten e-Mail-Nachricht im Vordergrund ist bestellen möchten, Sie können Gruppieren nach Absender und Aggregat auf Datum/Uhrzeit mit **aggregierte** empfangen -Attribut des Maximum.</span><span class="sxs-lookup"><span data-stu-id="832c0-148">For example, if you want to issue a FindItem grouped query, grouping by sender, but you want to order the groups so that the group with the most recent e-mail message is on top, you can group by sender and aggregate on date/time received with an **Aggregate** attribute of Maximum.</span></span> 
  
<span data-ttu-id="832c0-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="832c0-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="832c0-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="832c0-150">Example</span></span>

<span data-ttu-id="832c0-151">Das folgende Beispiel zeigt einen gruppierten FindItem Anforderung und Antwort.</span><span class="sxs-lookup"><span data-stu-id="832c0-151">The following example shows a grouped FindItem request and response.</span></span> <span data-ttu-id="832c0-152">Das Beispiel zeigt eine Anforderung zum Zurückgeben von Elementen, die von der **ConversationTopic** -Eigenschaft gruppiert.</span><span class="sxs-lookup"><span data-stu-id="832c0-152">The example shows a request to return items grouped by the **ConversationTopic** property.</span></span> <span data-ttu-id="832c0-153">Zwei Gruppen, A und B werden in absteigender Reihenfolge basierend auf den Höchstwert der [DateTimeReceived](datetimereceived.md) -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="832c0-153">Two groups, A and B, are returned in descending order based on the maximum value of the [DateTimeReceived](datetimereceived.md) property.</span></span> 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="message:ConversationTopic"/>
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AdditionalProperties>    
      </ItemShape>
      <IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="20" Offset="0"/>
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="message:ConversationTopic"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
<!-- EXAMPLE RESPONSE -->
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>B</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAH=" ChangeKey="CQAAABY" />
                    <t:DateTimeReceived>2006-09-14T23:59:18Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnAHR=" ChangeKey="CQAAAw" />
                    <t:DateTimeReceived>2006-09-15T00:00:24Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnA==" ChangeKey="CQAAJXT" />
                    <t:DateTimeReceived>2006-09-15T00:22:45Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>A</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAAA==" ChangeKey="CQCJNe" />
                    <t:DateTimeReceived>2006-09-14T23:56:12Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQWgAA==" ChangeKey="CQAACJV6" />
                    <t:DateTimeReceived>2006-09-14T23:57:33Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAAA==" ChangeKey="CQA6CJXw" />
                    <t:DateTimeReceived>2006-09-15T00:23:31Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="832c0-154">Verwenden Sie zum Sortieren der Elemente in einer Gruppe das [SortOrder](sortorder.md) -Element ein.</span><span class="sxs-lookup"><span data-stu-id="832c0-154">To sort the items in a group, use the [SortOrder](sortorder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="832c0-155">Die Element-IDs und Ändern von Schlüsseln wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="832c0-155">The item identifiers and change keys have been shortened to preserve readability.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="832c0-156">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="832c0-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="832c0-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="832c0-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="832c0-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="832c0-158">Schema Name</span></span>  <br/> |<span data-ttu-id="832c0-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="832c0-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="832c0-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="832c0-160">Validation File</span></span>  <br/> |<span data-ttu-id="832c0-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="832c0-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="832c0-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="832c0-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="832c0-163">False</span><span class="sxs-lookup"><span data-stu-id="832c0-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="832c0-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="832c0-164">See also</span></span>

- [<span data-ttu-id="832c0-165">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="832c0-165">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="832c0-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="832c0-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="832c0-167">Finding Items</span><span class="sxs-lookup"><span data-stu-id="832c0-167">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

