---
title: UpdateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: Der Vorgang UpdateItem wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern.
ms.openlocfilehash: 009ba16315017c4418fbd71d49744015c4d6d1b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839377"
---
# <a name="updateitem-operation"></a><span data-ttu-id="ba051-103">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="ba051-103">UpdateItem operation</span></span>

<span data-ttu-id="ba051-104">Der Vorgang **UpdateItem** wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ba051-104">The **UpdateItem** operation is used to modify the properties of an existing item in the Exchange store.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba051-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba051-105">Remarks</span></span>

<span data-ttu-id="ba051-106">Sie können drei grundlegende Update-Aktionen für ein Element ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba051-106">You can perform three basic update actions on an item.</span></span> <span data-ttu-id="ba051-107">In der folgenden Tabelle sind die Aktionen aufgelistet, die Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ba051-107">The following table lists the actions that you can perform.</span></span>
  
|<span data-ttu-id="ba051-108">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="ba051-108">**Action**</span></span>|<span data-ttu-id="ba051-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba051-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba051-110">Anfügeabfrage</span><span class="sxs-lookup"><span data-stu-id="ba051-110">Append</span></span>  <br/> |<span data-ttu-id="ba051-111">Daten hinzugefügt auf eine vorhandene Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba051-111">Adds data to an existing property.</span></span> <span data-ttu-id="ba051-112">Diese Aktion wird die aktuellen Daten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-112">This action preserves the current data.</span></span> <span data-ttu-id="ba051-113">Fügen Sie gilt nicht für alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba051-113">Append does not apply to all properties.</span></span>  <br/> |
|<span data-ttu-id="ba051-114">Gruppe</span><span class="sxs-lookup"><span data-stu-id="ba051-114">Set</span></span>  <br/> |<span data-ttu-id="ba051-115">Daten für eine Eigenschaft ersetzt, wenn die Eigenschaft Daten enthält, oder die Eigenschaft erstellt und legt deren Wert fest, wenn die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ba051-115">Replaces data for a property if the property contains data, or creates the property and sets its value if the property does not exist.</span></span> <span data-ttu-id="ba051-116">Die Set-Aktion gilt nur für schreibbaren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba051-116">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="ba051-117">Löschen</span><span class="sxs-lookup"><span data-stu-id="ba051-117">Delete</span></span>  <br/> |<span data-ttu-id="ba051-118">Entfernt eine Eigenschaft eines Elements.</span><span class="sxs-lookup"><span data-stu-id="ba051-118">Removes a property from an item.</span></span> <span data-ttu-id="ba051-119">Dies unterscheidet sich von einer Eigenschaft auf einen leeren Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="ba051-119">This differs from setting a property to an empty value.</span></span> <span data-ttu-id="ba051-120">Wenn diese Aktion abgeschlossen ist, ist die Eigenschaft für das Element nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba051-120">When this action is finished, the property does not exist for the item.</span></span> <span data-ttu-id="ba051-121">Delete gilt nur für schreibbaren Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba051-121">Delete is only applicable to writable properties.</span></span>  <br/> |
   
<span data-ttu-id="ba051-122">Ein Aufruf **UpdateItem** kann verwendet werden, um ein oder mehrere Elemente und eine oder mehrere Eigenschaften für jedes Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ba051-122">An **UpdateItem** call can be used to modify one or more items, and one or more properties on each item.</span></span> <span data-ttu-id="ba051-123">Das [ItemChanges](itemchanges.md) -Element enthält alle Änderungen, die im Rahmen dieses Anrufs ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba051-123">The [ItemChanges](itemchanges.md) element contains all the modifications that are to be performed as part of this call.</span></span> <span data-ttu-id="ba051-124">Das [ItemChange](itemchange.md) -Element ein untergeordnetes Element des Elements [ItemChanges](itemchanges.md) stellt die Änderungen in ein einzelnes Element ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba051-124">The [ItemChange](itemchange.md) element, a child of the [ItemChanges](itemchanges.md) element, represents the modifications to be performed on a single item.</span></span> <span data-ttu-id="ba051-125">Das [ItemChange](itemchange.md) -Element enthält eine Reihe von Update-Aktionen, die für ein einzelnes Element ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba051-125">The [ItemChange](itemchange.md) element contains a set of update actions that can be performed on a single item.</span></span> <span data-ttu-id="ba051-126">Diese Änderungen werden in der [Updates (Element)](updates-item.md) -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-126">These changes are contained in the [Updates (Item)](updates-item.md) element.</span></span> <span data-ttu-id="ba051-127">Das [ItemId](itemid.md) -Element identifiziert das Element zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ba051-127">The [ItemId](itemid.md) element identifies the item to update.</span></span> <span data-ttu-id="ba051-128">Um mehr als eine Eigenschaft für ein Element zu aktualisieren, muss ein [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md)oder [DeleteItemField](deleteitemfield.md) für jede Eigenschaft angegeben werden, die das Update erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ba051-128">To update more than one property on an item, a [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md), or [DeleteItemField](deleteitemfield.md) must be provided for each property that requires the update.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ba051-129">Update-Aktionen werden in der Reihenfolge angewendet, in denen sie angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ba051-129">Update actions are applied in the order in which they are specified.</span></span> 
  
<span data-ttu-id="ba051-130">Für jede Änderung müssen Sie den Pfad der Eigenschaft, die geändert und einer Darstellung des betreffenden Elements mit den neuen Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="ba051-130">For each change, you have to specify the path of the property to change and a representation of that item with its new value.</span></span> <span data-ttu-id="ba051-131">Die Löschaktion wird geringfügig, nur der Pfad der Eigenschaft, die gelöscht werden sollen, erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ba051-131">The delete action is slightly different in that only the path of the property that should be deleted is required.</span></span> <span data-ttu-id="ba051-132">Für ein und Aktionen anfügen, der angegebenen Pfad muss verweisen auf dieselbe Eigenschaft, die in der Darstellung des Elements festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ba051-132">For set and append actions, the path that is specified must refer to the same property that is being set in the item representation.</span></span> <span data-ttu-id="ba051-133">Wenn sich diese unterscheiden, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba051-133">If these differ, an error will be returned.</span></span>
  
<span data-ttu-id="ba051-134">**UpdateItem** -Vorgang kann die Zeit [Start](start.md) und [End](end-ex15websvcsotherref.md) eines Exchange-Speicher-Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba051-134">The **UpdateItem** operation can set the [Start](start.md) and [End ](end-ex15websvcsotherref.md) time of an Exchange store item.</span></span> <span data-ttu-id="ba051-135">In einer Anforderung **UpdateItem** kann [die Startzeit](start.md) festgelegt werden, ohne auch [die Endzeit](end-ex15websvcsotherref.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ba051-135">In an **UpdateItem** request, the [Start](start.md) time can be set without also setting the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="ba051-136">Dies kann einen Fehler verursachen, wenn [die Startzeit](start.md) [die Endzeit](end-ex15websvcsotherref.md) liegt.</span><span class="sxs-lookup"><span data-stu-id="ba051-136">This can cause an error if the [Start](start.md) time is later than the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="ba051-137">Beachten Sie, dass Clientanwendungen [die Endzeit](end-ex15websvcsotherref.md) anpassen müssen, wenn [die Startzeit](start.md) geändert wird, um die Dauer beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-137">Be aware that client applications must adjust the [End ](end-ex15websvcsotherref.md) time when the [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
<span data-ttu-id="ba051-138">Wenn ein einzelnes Kalenderelement ein wiederkehrendes master Kalenderelement vertraut aktualisiert wird, muss die [MeetingTimeZone](meetingtimezone.md) -Eigenschaft, um das Kalenderelement ursprüngliche Zeitzone beibehalten durch den Vorgang **UpdateItem** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ba051-138">When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) property must be set by the **UpdateItem** operation in order to preserve the calendar item's original time zone.</span></span> 
  
## <a name="setitemfield-request-example"></a><span data-ttu-id="ba051-139">Anforderungsbeispiel SetItemField</span><span class="sxs-lookup"><span data-stu-id="ba051-139">SetItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="ba051-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba051-140">Description</span></span>

<span data-ttu-id="ba051-141">Im folgenden Beispiel wird einer Anforderung **UpdateItem** veranschaulicht, wie die Sensitivity-Eigenschaft für ein Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba051-141">The following example of an **UpdateItem** request shows how to set the sensitivity property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ba051-142">Code</span><span class="sxs-lookup"><span data-stu-id="ba051-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ba051-143">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ba051-143">Comments</span></span>

<span data-ttu-id="ba051-144">Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-144">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="setitemfield-request-elements"></a><span data-ttu-id="ba051-145">SetItemField Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="ba051-145">SetItemField Request Elements</span></span>

<span data-ttu-id="ba051-146">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ba051-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ba051-147">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ba051-147">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="ba051-148">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="ba051-148">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="ba051-149">ItemChange</span><span class="sxs-lookup"><span data-stu-id="ba051-149">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="ba051-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="ba051-150">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="ba051-151">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="ba051-151">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="ba051-152">SetItemField</span><span class="sxs-lookup"><span data-stu-id="ba051-152">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="ba051-153">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ba051-153">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="ba051-154">Message</span><span class="sxs-lookup"><span data-stu-id="ba051-154">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ba051-155">Vertraulichkeit</span><span class="sxs-lookup"><span data-stu-id="ba051-155">Sensitivity</span></span>](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a><span data-ttu-id="ba051-156">Anforderungsbeispiel AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="ba051-156">AppendToItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="ba051-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba051-157">Description</span></span>

<span data-ttu-id="ba051-158">Im folgenden Beispiel wird einer Anforderung **UpdateItem** veranschaulicht, wie Text an die Body-Eigenschaft für ein Element angefügt.</span><span class="sxs-lookup"><span data-stu-id="ba051-158">The following example of an **UpdateItem** request shows how to append text to the body property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ba051-159">Code</span><span class="sxs-lookup"><span data-stu-id="ba051-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ba051-160">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ba051-160">Comments</span></span>

<span data-ttu-id="ba051-161">Die folgenden Eigenschaften unterstützen die Append-Aktion:</span><span class="sxs-lookup"><span data-stu-id="ba051-161">The following properties support the append action:</span></span>
  
- <span data-ttu-id="ba051-162">**Meldung: ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="ba051-162">**message:ReplyTo**</span></span>
    
- <span data-ttu-id="ba051-163">**Textkörper:**</span><span class="sxs-lookup"><span data-stu-id="ba051-163">**item:Body**</span></span>
    
- <span data-ttu-id="ba051-164">Alle Empfänger und Teilnehmer-Auflistungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba051-164">All the recipient and attendee collection properties</span></span>
    
<span data-ttu-id="ba051-165">Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-165">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="appendtoitemfield-request-elements"></a><span data-ttu-id="ba051-166">AppendToItemField Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="ba051-166">AppendToItemField Request Elements</span></span>

<span data-ttu-id="ba051-167">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ba051-167">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ba051-168">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ba051-168">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="ba051-169">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="ba051-169">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="ba051-170">ItemChange</span><span class="sxs-lookup"><span data-stu-id="ba051-170">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="ba051-171">ItemId</span><span class="sxs-lookup"><span data-stu-id="ba051-171">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="ba051-172">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="ba051-172">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="ba051-173">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="ba051-173">AppendToItemField</span></span>](appendtoitemfield.md)
    
- [<span data-ttu-id="ba051-174">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ba051-174">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="ba051-175">Message</span><span class="sxs-lookup"><span data-stu-id="ba051-175">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ba051-176">Body</span><span class="sxs-lookup"><span data-stu-id="ba051-176">Body</span></span>](body.md)
    
## <a name="deleteitemfield-request-example"></a><span data-ttu-id="ba051-177">Anforderungsbeispiel DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="ba051-177">DeleteItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="ba051-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba051-178">Description</span></span>

<span data-ttu-id="ba051-179">Im folgenden Beispiel wird einer Anforderung **UpdateItem** veranschaulicht, wie eine Eigenschaft für ein Element zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ba051-179">The following example of an **UpdateItem** request shows how to delete a property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ba051-180">Code</span><span class="sxs-lookup"><span data-stu-id="ba051-180">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ba051-181">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ba051-181">Comments</span></span>

<span data-ttu-id="ba051-182">Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-182">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="deleteitemfield-request-elements"></a><span data-ttu-id="ba051-183">DeleteItemField Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="ba051-183">DeleteItemField Request Elements</span></span>

<span data-ttu-id="ba051-184">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ba051-184">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ba051-185">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="ba051-185">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="ba051-186">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="ba051-186">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="ba051-187">ItemChange</span><span class="sxs-lookup"><span data-stu-id="ba051-187">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="ba051-188">ItemId</span><span class="sxs-lookup"><span data-stu-id="ba051-188">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="ba051-189">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="ba051-189">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="ba051-190">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="ba051-190">DeleteItemField</span></span>](deleteitemfield.md)
    
- [<span data-ttu-id="ba051-191">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ba051-191">FieldURI</span></span>](fielduri.md)
    
## <a name="successful-response-example"></a><span data-ttu-id="ba051-192">Beispiel einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="ba051-192">Successful response example</span></span>

### <a name="description"></a><span data-ttu-id="ba051-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba051-193">Description</span></span>

<span data-ttu-id="ba051-194">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **UpdateItem** .</span><span class="sxs-lookup"><span data-stu-id="ba051-194">The following example shows a successful response to an **UpdateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="ba051-195">Code</span><span class="sxs-lookup"><span data-stu-id="ba051-195">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ba051-196">Kommentare</span><span class="sxs-lookup"><span data-stu-id="ba051-196">Comments</span></span>

<span data-ttu-id="ba051-197">Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba051-197">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="ba051-198">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="ba051-198">Successful response elements</span></span>

<span data-ttu-id="ba051-199">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ba051-199">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ba051-200">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ba051-200">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ba051-201">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="ba051-201">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="ba051-202">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ba051-202">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ba051-203">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ba051-203">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="ba051-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ba051-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ba051-205">Elemente</span><span class="sxs-lookup"><span data-stu-id="ba051-205">Items</span></span>](items.md)
    
- [<span data-ttu-id="ba051-206">Message</span><span class="sxs-lookup"><span data-stu-id="ba051-206">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="ba051-207">ItemId</span><span class="sxs-lookup"><span data-stu-id="ba051-207">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="ba051-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba051-208">See also</span></span>



[<span data-ttu-id="ba051-209">UpdateItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="ba051-209">UpdateItem operation (task)</span></span>](updateitem-operation-task.md)
  
[<span data-ttu-id="ba051-210">UpdateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="ba051-210">UpdateItem operation (contact)</span></span>](updateitem-operation-contact.md)


- [<span data-ttu-id="ba051-211">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ba051-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ba051-212">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="ba051-212">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="ba051-213">Aktualisieren der Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ba051-213">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

