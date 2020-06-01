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
description: Das AggregateOn-Element stellt die Eigenschaft dar, die verwendet wird, um die Reihenfolge von gruppierten Elementen für ein gruppiertes FindItem-Resultset festzulegen.
ms.openlocfilehash: 04359c187ef11538d64f8f0d3ea2fe84bc3d048b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463566"
---
# <a name="aggregateon"></a><span data-ttu-id="b6024-103">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="b6024-103">AggregateOn</span></span>

<span data-ttu-id="b6024-104">Das **AggregateOn** -Element stellt die Eigenschaft dar, die verwendet wird, um die Reihenfolge von gruppierten Elementen für ein gruppiertes FindItem-Resultset festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b6024-104">The **AggregateOn** element represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span> 
  
- [<span data-ttu-id="b6024-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="b6024-105">FindItem</span></span>](finditem.md)  
- [<span data-ttu-id="b6024-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="b6024-106">GroupBy</span></span>](groupby.md)
- [<span data-ttu-id="b6024-107">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="b6024-107">AggregateOn</span></span>](aggregateon.md)
  
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
 
<span data-ttu-id="b6024-108">**AggregateOnType**</span><span class="sxs-lookup"><span data-stu-id="b6024-108">**AggregateOnType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b6024-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6024-109">Attributes and elements</span></span>

<span data-ttu-id="b6024-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6024-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6024-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6024-111">Attributes</span></span>

|<span data-ttu-id="b6024-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b6024-112">**Attribute**</span></span>|<span data-ttu-id="b6024-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6024-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6024-114">**Aggregate**</span><span class="sxs-lookup"><span data-stu-id="b6024-114">**Aggregate**</span></span> <br/> | <span data-ttu-id="b6024-115">Gibt den maximalen oder minimalen Wert der Eigenschaft an, die durch das [FieldURI](fielduri.md) -Element identifiziert wird, das für die Sortierung der Gruppen von Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6024-115">Indicates the maximum or minimum value of the property identified by the [FieldURI](fielduri.md) element that is used for ordering the groups of items.</span></span><br/><br/><span data-ttu-id="b6024-116">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b6024-116">The following are the possible values:</span></span>  <br/><br/><span data-ttu-id="b6024-117">-Minimum</span><span class="sxs-lookup"><span data-stu-id="b6024-117">- Minimum</span></span>  <br/><span data-ttu-id="b6024-118">-Maximum</span><span class="sxs-lookup"><span data-stu-id="b6024-118">- Maximum</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b6024-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6024-119">Child elements</span></span>

|<span data-ttu-id="b6024-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6024-120">**Element**</span></span>|<span data-ttu-id="b6024-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6024-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6024-122">FieldURI</span><span class="sxs-lookup"><span data-stu-id="b6024-122">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="b6024-123">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="b6024-123">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="b6024-124">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="b6024-124">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="b6024-125">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="b6024-125">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="b6024-126">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="b6024-126">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="b6024-127">Identifiziert erweiterte MAPI-Eigenschaften zum Abrufen, festlegen oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6024-127">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6024-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6024-128">Parent elements</span></span>

|<span data-ttu-id="b6024-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6024-129">**Element**</span></span>|<span data-ttu-id="b6024-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6024-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6024-131">GroupBy</span><span class="sxs-lookup"><span data-stu-id="b6024-131">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="b6024-132">Gibt willkürliche Gruppierungen für FindItem-Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="b6024-132">Specifies arbitrary groupings for FindItem queries.</span></span>  <br/> <span data-ttu-id="b6024-133">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/FindItem/GroupBy`</span><span class="sxs-lookup"><span data-stu-id="b6024-133">The following is the XPath expression to this element:  `/FindItem/GroupBy`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6024-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6024-134">Remarks</span></span>

<span data-ttu-id="b6024-135">Der [FindItem-Vorgang](finditem-operation.md) kann gruppierte Ergebnisse zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b6024-135">The [FindItem operation](finditem-operation.md) can return grouped results.</span></span> <span data-ttu-id="b6024-136">In gruppierten Ergebnissen werden alle Elemente, die den gleichen Wert für eine bestimmte Gruppierungseigenschaft aufweisen, zusammen gesammelt und als untergeordnete Elemente dieser Gruppe dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b6024-136">Within grouped results, all items that have the same value for a given grouping property are gathered together and presented as children of that group.</span></span> <span data-ttu-id="b6024-137">Wenn Sie beispielsweise nach Absender gruppieren, werden alle e-Mails abhängig davon, ob Sie von Absender a, Absender B und so weiter sind, in separaten Gruppen organisiert.</span><span class="sxs-lookup"><span data-stu-id="b6024-137">For example, if you group by sender, all e-mails are organized into separate groups based on whether they are from sender A, sender B, and so on.</span></span> <span data-ttu-id="b6024-138">Diese Gruppen sind untergeordnete Elemente der Absendergruppe.</span><span class="sxs-lookup"><span data-stu-id="b6024-138">These groups are children of the sender group.</span></span> 
  
<span data-ttu-id="b6024-139">Jede der Gruppen innerhalb der Absendergruppe enthält eine Sammlung von Elementen, beispielsweise die tatsächlichen e-Mails, die von jedem Absender stammen.</span><span class="sxs-lookup"><span data-stu-id="b6024-139">Each of the groups within the sender group contains a collection of items, such as the actual e-mails that came from each sender.</span></span> <span data-ttu-id="b6024-140">Sie können das Sortier [Reihenfolge](sortorder.md) -Element verwenden, um die Elemente innerhalb einer Gruppe zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="b6024-140">You can use the [SortOrder](sortorder.md) element to sort the items within a group.</span></span> <span data-ttu-id="b6024-141">Um die Gruppen basierend auf den Eigenschaftswerten eines Elements zu sortieren, müssen Sie jedoch Aggregation verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6024-141">To sort the groups based on an item's property values, however, you must use aggregation.</span></span> 
  
<span data-ttu-id="b6024-142">Bei Aggregation basiert die Reihenfolge der Gruppen auf einer bestimmten Eigenschaft der Elemente in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b6024-142">With aggregation, the order of groups is based on a specific property of the items within the group.</span></span> <span data-ttu-id="b6024-143">Wenn Sie mithilfe von Aggregation Elemente innerhalb einer Gruppe Sortieren, müssen Sie eine repräsentative Eigenschaft angeben, nach der die Gruppen sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b6024-143">When you use aggregation to sort items within a group, you must identify a representative property by which to sort the groups.</span></span> <span data-ttu-id="b6024-144">Sie können das **AggregateOn** -Element verwenden, um die Representative-Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b6024-144">You can use the **AggregateOn** element to specify the representative property.</span></span> 
  
<span data-ttu-id="b6024-145">Wenn eine repräsentative Eigenschaft identifiziert wird, wird das **Aggregate** -Attribut verwendet, um anzugeben, ob die Gruppen entsprechend dem maximalen oder dem kleinsten Wert der angegebenen Eigenschaft sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6024-145">When a representative property is identified, the **Aggregate** attribute is used to indicate whether the groups are sorted according to the maximum or the minimum value of the identified property.</span></span> <span data-ttu-id="b6024-146">Wenn das **Aggregate** -Attribut auf Maximum festgelegt ist, werden die Gruppen beginnend mit dem größten Wert für die **AggregateOn** -Eigenschaft sortiert.</span><span class="sxs-lookup"><span data-stu-id="b6024-146">If the **Aggregate** attribute is set to Maximum, the groups are sorted beginning with the largest value for the **AggregateOn** property.</span></span> <span data-ttu-id="b6024-147">Wenn das **Aggregate** -Attribut auf Minimum festgelegt ist, werden die Gruppen beginnend mit dem kleinsten Wert für die **AggregateOn** -Eigenschaft sortiert.</span><span class="sxs-lookup"><span data-stu-id="b6024-147">If the **Aggregate** attribute is set to Minimum, the groups are sorted beginning with the smallest value for the **AggregateOn** property.</span></span> 
  
<span data-ttu-id="b6024-148">Wenn Sie beispielsweise eine FindItem-gruppierte Abfrage ausgeben möchten, die nach Absender gruppiert wird, Sie die Gruppen jedoch so sortieren möchten, dass die Gruppe mit der neuesten e-Mail-Nachricht im Vordergrund ist, können Sie nach Absender und Aggregat nach Datum/Uhrzeit, die mit einem **Aggregate** -Attribut von Maximum empfangen wurde, gruppieren.</span><span class="sxs-lookup"><span data-stu-id="b6024-148">For example, if you want to issue a FindItem grouped query, grouping by sender, but you want to order the groups so that the group with the most recent e-mail message is on top, you can group by sender and aggregate on date/time received with an **Aggregate** attribute of Maximum.</span></span> 
  
<span data-ttu-id="b6024-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b6024-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="b6024-150">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b6024-150">Example</span></span>

<span data-ttu-id="b6024-151">Das folgende Beispiel zeigt eine gruppierte FindItem-Anforderung und-Antwort.</span><span class="sxs-lookup"><span data-stu-id="b6024-151">The following example shows a grouped FindItem request and response.</span></span> <span data-ttu-id="b6024-152">Das Beispiel zeigt eine Anforderung zum Zurückgeben von Elementen, die von der **ConversationTopic** -Eigenschaft gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6024-152">The example shows a request to return items grouped by the **ConversationTopic** property.</span></span> <span data-ttu-id="b6024-153">Zwei Gruppen, A und B, werden in absteigender Reihenfolge basierend auf dem Höchstwert der [DateTimeReceived](datetimereceived.md) -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b6024-153">Two groups, A and B, are returned in descending order based on the maximum value of the [DateTimeReceived](datetimereceived.md) property.</span></span> 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
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
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="b6024-154">Wenn Sie die Elemente in einer Gruppe sortieren möchten, verwenden Sie das Sortier [Reihenfolge](sortorder.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="b6024-154">To sort the items in a group, use the [SortOrder](sortorder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b6024-155">Die Element-IDs und Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b6024-155">The item identifiers and change keys have been shortened to preserve readability.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b6024-156">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b6024-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6024-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6024-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b6024-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b6024-158">Schema Name</span></span>  <br/> |<span data-ttu-id="b6024-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b6024-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="b6024-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b6024-160">Validation File</span></span>  <br/> |<span data-ttu-id="b6024-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b6024-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b6024-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b6024-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6024-163">False</span><span class="sxs-lookup"><span data-stu-id="b6024-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6024-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6024-164">See also</span></span>

- [<span data-ttu-id="b6024-165">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b6024-165">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="b6024-166">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b6024-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="b6024-167">Finding Items</span><span class="sxs-lookup"><span data-stu-id="b6024-167">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

