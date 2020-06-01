---
title: UpdateItem-Vorgang
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
description: Der UpdateItem-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern.
ms.openlocfilehash: c001b7656862144023e9704cb04e6b4c0030f9df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459391"
---
# <a name="updateitem-operation"></a><span data-ttu-id="6338c-103">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6338c-103">UpdateItem operation</span></span>

<span data-ttu-id="6338c-104">Der **UpdateItem** -Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6338c-104">The **UpdateItem** operation is used to modify the properties of an existing item in the Exchange store.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6338c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6338c-105">Remarks</span></span>

<span data-ttu-id="6338c-106">Sie können drei grundlegende Updateaktionen für ein Element durchführen.</span><span class="sxs-lookup"><span data-stu-id="6338c-106">You can perform three basic update actions on an item.</span></span> <span data-ttu-id="6338c-107">In der folgenden Tabelle sind die Aktionen aufgeführt, die Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="6338c-107">The following table lists the actions that you can perform.</span></span>
  
|<span data-ttu-id="6338c-108">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="6338c-108">**Action**</span></span>|<span data-ttu-id="6338c-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6338c-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6338c-110">Append</span><span class="sxs-lookup"><span data-stu-id="6338c-110">Append</span></span>  <br/> |<span data-ttu-id="6338c-111">Fügt einer vorhandenen Eigenschaft Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="6338c-111">Adds data to an existing property.</span></span> <span data-ttu-id="6338c-112">Mit dieser Aktion werden die aktuellen Daten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-112">This action preserves the current data.</span></span> <span data-ttu-id="6338c-113">Append gilt nicht für alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6338c-113">Append does not apply to all properties.</span></span>  <br/> |
|<span data-ttu-id="6338c-114">Satz</span><span class="sxs-lookup"><span data-stu-id="6338c-114">Set</span></span>  <br/> |<span data-ttu-id="6338c-115">Ersetzt Daten für eine Eigenschaft, wenn die Eigenschaft Daten enthält, oder erstellt die Eigenschaft und legt den Wert fest, wenn die Eigenschaft nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6338c-115">Replaces data for a property if the property contains data, or creates the property and sets its value if the property does not exist.</span></span> <span data-ttu-id="6338c-116">Die Aktion festlegen gilt nur für schreibbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6338c-116">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="6338c-117">Löschen</span><span class="sxs-lookup"><span data-stu-id="6338c-117">Delete</span></span>  <br/> |<span data-ttu-id="6338c-118">Entfernt eine Eigenschaft aus einem Element.</span><span class="sxs-lookup"><span data-stu-id="6338c-118">Removes a property from an item.</span></span> <span data-ttu-id="6338c-119">Dies unterscheidet sich vom Festlegen einer Eigenschaft auf einen leeren Wert.</span><span class="sxs-lookup"><span data-stu-id="6338c-119">This differs from setting a property to an empty value.</span></span> <span data-ttu-id="6338c-120">Wenn diese Aktion abgeschlossen ist, ist die Eigenschaft für das Element nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6338c-120">When this action is finished, the property does not exist for the item.</span></span> <span data-ttu-id="6338c-121">DELETE gilt nur für schreibbare Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6338c-121">Delete is only applicable to writable properties.</span></span>  <br/> |
   
<span data-ttu-id="6338c-122">Ein **UpdateItem** -Aufruf kann verwendet werden, um ein oder mehrere Elemente sowie eine oder mehrere Eigenschaften für jedes Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6338c-122">An **UpdateItem** call can be used to modify one or more items, and one or more properties on each item.</span></span> <span data-ttu-id="6338c-123">Das [ItemChanges](itemchanges.md) -Element enthält alle Änderungen, die im Rahmen dieses Aufrufs ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6338c-123">The [ItemChanges](itemchanges.md) element contains all the modifications that are to be performed as part of this call.</span></span> <span data-ttu-id="6338c-124">Das [ItemChange](itemchange.md) -Element, ein untergeordnetes Element des [ItemChanges](itemchanges.md) -Elements, stellt die Änderungen dar, die für ein einzelnes Element ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6338c-124">The [ItemChange](itemchange.md) element, a child of the [ItemChanges](itemchanges.md) element, represents the modifications to be performed on a single item.</span></span> <span data-ttu-id="6338c-125">Das [ItemChange](itemchange.md) -Element enthält eine Reihe von Updateaktionen, die für ein einzelnes Element ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="6338c-125">The [ItemChange](itemchange.md) element contains a set of update actions that can be performed on a single item.</span></span> <span data-ttu-id="6338c-126">Diese Änderungen sind im Update Element [(Element)](updates-item.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-126">These changes are contained in the [Updates (Item)](updates-item.md) element.</span></span> <span data-ttu-id="6338c-127">Das Element [ItemID](itemid.md) identifiziert das Element, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6338c-127">The [ItemId](itemid.md) element identifies the item to update.</span></span> <span data-ttu-id="6338c-128">Wenn Sie mehr als eine Eigenschaft für ein Element aktualisieren möchten, muss für jede Eigenschaft, die das Update erfordert, ein [setitemfield](setitemfield.md), [AppendToItemField](appendtoitemfield.md)oder [DeleteItemField](deleteitemfield.md) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6338c-128">To update more than one property on an item, a [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md), or [DeleteItemField](deleteitemfield.md) must be provided for each property that requires the update.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6338c-129">Update Aktionen werden in der Reihenfolge angewendet, in der Sie angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6338c-129">Update actions are applied in the order in which they are specified.</span></span> 
  
<span data-ttu-id="6338c-130">Für jede Änderung müssen Sie den Pfad der zu ändernden Eigenschaft und eine Darstellung dieses Elements mit dem neuen Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="6338c-130">For each change, you have to specify the path of the property to change and a representation of that item with its new value.</span></span> <span data-ttu-id="6338c-131">Die DELETE-Aktion unterscheidet sich geringfügig dadurch, dass nur der Pfad der zu löschenden Eigenschaft erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6338c-131">The delete action is slightly different in that only the path of the property that should be deleted is required.</span></span> <span data-ttu-id="6338c-132">Bei Aktionen zum Festlegen und Anfügen muss der angegebene Pfad auf dieselbe Eigenschaft verwiesen werden, die in der Elementdarstellung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="6338c-132">For set and append actions, the path that is specified must refer to the same property that is being set in the item representation.</span></span> <span data-ttu-id="6338c-133">Wenn sich diese unterscheiden, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6338c-133">If these differ, an error will be returned.</span></span>
  
<span data-ttu-id="6338c-134">Mit dem **UpdateItem** -Vorgang können die [Start](start.md) -und [Endzeit](end-ex15websvcsotherref.md) eines Exchange-Informationsspeicher Elements festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6338c-134">The **UpdateItem** operation can set the [Start](start.md) and [End ](end-ex15websvcsotherref.md) time of an Exchange store item.</span></span> <span data-ttu-id="6338c-135">In einer **UpdateItem** -Anforderung kann die [Startzeit](start.md) festgelegt werden, ohne auch die [Endzeit](end-ex15websvcsotherref.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6338c-135">In an **UpdateItem** request, the [Start](start.md) time can be set without also setting the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="6338c-136">Dies kann zu einem Fehler führen, wenn die [Startzeit](start.md) später als die [Endzeit](end-ex15websvcsotherref.md) ist.</span><span class="sxs-lookup"><span data-stu-id="6338c-136">This can cause an error if the [Start](start.md) time is later than the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="6338c-137">Beachten Sie, dass Clientanwendungen die [Endzeit](end-ex15websvcsotherref.md) anpassen müssen, wenn die [Startzeit](start.md) geändert wird, um die Dauer beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-137">Be aware that client applications must adjust the [End ](end-ex15websvcsotherref.md) time when the [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
<span data-ttu-id="6338c-138">Wenn ein einzelnes Kalenderelement als wiederkehrendes Master Kalenderelement aktualisiert wird, muss die [MeetingTimeZone](meetingtimezone.md) -Eigenschaft durch den **UpdateItem** -Vorgang festgelegt werden, um die ursprüngliche Zeitzone des Kalenderelements beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-138">When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) property must be set by the **UpdateItem** operation in order to preserve the calendar item's original time zone.</span></span> 
  
## <a name="setitemfield-request-example"></a><span data-ttu-id="6338c-139">Setitemfield-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6338c-139">SetItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="6338c-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6338c-140">Description</span></span>

<span data-ttu-id="6338c-141">Im folgenden Beispiel einer **UpdateItem** -Anforderung wird gezeigt, wie die Sensitivity-Eigenschaft für ein Element festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="6338c-141">The following example of an **UpdateItem** request shows how to set the sensitivity property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6338c-142">Code</span><span class="sxs-lookup"><span data-stu-id="6338c-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="6338c-143">Comments</span><span class="sxs-lookup"><span data-stu-id="6338c-143">Comments</span></span>

<span data-ttu-id="6338c-144">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-144">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="setitemfield-request-elements"></a><span data-ttu-id="6338c-145">Setitemfield-anforderungselemente</span><span class="sxs-lookup"><span data-stu-id="6338c-145">SetItemField Request Elements</span></span>

<span data-ttu-id="6338c-146">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6338c-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="6338c-147">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="6338c-147">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="6338c-148">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="6338c-148">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="6338c-149">ItemChange</span><span class="sxs-lookup"><span data-stu-id="6338c-149">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="6338c-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="6338c-150">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="6338c-151">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="6338c-151">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="6338c-152">SetItemField</span><span class="sxs-lookup"><span data-stu-id="6338c-152">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="6338c-153">FieldURI</span><span class="sxs-lookup"><span data-stu-id="6338c-153">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="6338c-154">Nachricht</span><span class="sxs-lookup"><span data-stu-id="6338c-154">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6338c-155">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="6338c-155">Sensitivity</span></span>](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a><span data-ttu-id="6338c-156">AppendToItemField-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6338c-156">AppendToItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="6338c-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6338c-157">Description</span></span>

<span data-ttu-id="6338c-158">Im folgenden Beispiel einer **UpdateItem** -Anforderung wird gezeigt, wie Text an die Body-Eigenschaft eines Elements angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6338c-158">The following example of an **UpdateItem** request shows how to append text to the body property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6338c-159">Code</span><span class="sxs-lookup"><span data-stu-id="6338c-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="6338c-160">Comments</span><span class="sxs-lookup"><span data-stu-id="6338c-160">Comments</span></span>

<span data-ttu-id="6338c-161">Die folgenden Eigenschaften unterstützen die Append-Aktion:</span><span class="sxs-lookup"><span data-stu-id="6338c-161">The following properties support the append action:</span></span>
  
- <span data-ttu-id="6338c-162">**message:ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="6338c-162">**message:ReplyTo**</span></span>
    
- <span data-ttu-id="6338c-163">**Element: Body**</span><span class="sxs-lookup"><span data-stu-id="6338c-163">**item:Body**</span></span>
    
- <span data-ttu-id="6338c-164">Alle Eigenschaften Recipient und Attendee Collection</span><span class="sxs-lookup"><span data-stu-id="6338c-164">All the recipient and attendee collection properties</span></span>
    
<span data-ttu-id="6338c-165">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-165">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="appendtoitemfield-request-elements"></a><span data-ttu-id="6338c-166">AppendToItemField-anforderungselemente</span><span class="sxs-lookup"><span data-stu-id="6338c-166">AppendToItemField Request Elements</span></span>

<span data-ttu-id="6338c-167">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6338c-167">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="6338c-168">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="6338c-168">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="6338c-169">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="6338c-169">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="6338c-170">ItemChange</span><span class="sxs-lookup"><span data-stu-id="6338c-170">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="6338c-171">ItemId</span><span class="sxs-lookup"><span data-stu-id="6338c-171">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="6338c-172">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="6338c-172">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="6338c-173">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="6338c-173">AppendToItemField</span></span>](appendtoitemfield.md)
    
- [<span data-ttu-id="6338c-174">FieldURI</span><span class="sxs-lookup"><span data-stu-id="6338c-174">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="6338c-175">Nachricht</span><span class="sxs-lookup"><span data-stu-id="6338c-175">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6338c-176">Body</span><span class="sxs-lookup"><span data-stu-id="6338c-176">Body</span></span>](body.md)
    
## <a name="deleteitemfield-request-example"></a><span data-ttu-id="6338c-177">DeleteItemField-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6338c-177">DeleteItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="6338c-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6338c-178">Description</span></span>

<span data-ttu-id="6338c-179">Im folgenden Beispiel einer **UpdateItem** -Anforderung wird gezeigt, wie eine Eigenschaft für ein Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6338c-179">The following example of an **UpdateItem** request shows how to delete a property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6338c-180">Code</span><span class="sxs-lookup"><span data-stu-id="6338c-180">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="6338c-181">Comments</span><span class="sxs-lookup"><span data-stu-id="6338c-181">Comments</span></span>

<span data-ttu-id="6338c-182">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-182">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="deleteitemfield-request-elements"></a><span data-ttu-id="6338c-183">DeleteItemField-anforderungselemente</span><span class="sxs-lookup"><span data-stu-id="6338c-183">DeleteItemField Request Elements</span></span>

<span data-ttu-id="6338c-184">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6338c-184">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="6338c-185">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="6338c-185">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="6338c-186">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="6338c-186">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="6338c-187">ItemChange</span><span class="sxs-lookup"><span data-stu-id="6338c-187">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="6338c-188">ItemId</span><span class="sxs-lookup"><span data-stu-id="6338c-188">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="6338c-189">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="6338c-189">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="6338c-190">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="6338c-190">DeleteItemField</span></span>](deleteitemfield.md)
    
- [<span data-ttu-id="6338c-191">FieldURI</span><span class="sxs-lookup"><span data-stu-id="6338c-191">FieldURI</span></span>](fielduri.md)
    
## <a name="successful-response-example"></a><span data-ttu-id="6338c-192">Beispiel für eine erfolgreiche Antwort</span><span class="sxs-lookup"><span data-stu-id="6338c-192">Successful response example</span></span>

### <a name="description"></a><span data-ttu-id="6338c-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6338c-193">Description</span></span>

<span data-ttu-id="6338c-194">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **UpdateItem** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6338c-194">The following example shows a successful response to an **UpdateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6338c-195">Code</span><span class="sxs-lookup"><span data-stu-id="6338c-195">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="6338c-196">Comments</span><span class="sxs-lookup"><span data-stu-id="6338c-196">Comments</span></span>

<span data-ttu-id="6338c-197">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6338c-197">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="6338c-198">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="6338c-198">Successful response elements</span></span>

<span data-ttu-id="6338c-199">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6338c-199">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="6338c-200">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="6338c-200">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="6338c-201">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="6338c-201">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="6338c-202">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6338c-202">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="6338c-203">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6338c-203">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="6338c-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="6338c-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="6338c-205">Elemente</span><span class="sxs-lookup"><span data-stu-id="6338c-205">Items</span></span>](items.md)
    
- [<span data-ttu-id="6338c-206">Message</span><span class="sxs-lookup"><span data-stu-id="6338c-206">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="6338c-207">ItemId</span><span class="sxs-lookup"><span data-stu-id="6338c-207">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="6338c-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6338c-208">See also</span></span>



[<span data-ttu-id="6338c-209">UpdateItem-Vorgang (Vorgang)</span><span class="sxs-lookup"><span data-stu-id="6338c-209">UpdateItem operation (task)</span></span>](updateitem-operation-task.md)
  
[<span data-ttu-id="6338c-210">UpdateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="6338c-210">UpdateItem operation (contact)</span></span>](updateitem-operation-contact.md)


- [<span data-ttu-id="6338c-211">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6338c-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6338c-212">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="6338c-212">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="6338c-213">Aktualisieren von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6338c-213">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

