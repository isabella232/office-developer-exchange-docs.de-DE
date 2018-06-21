---
title: DelegateUserResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUserResponseMessageType
api_type:
- schema
ms.assetid: 3dc9552c-1e2d-40ac-a137-827883c2bb88
description: Das DelegateUserResponseMessageType-Element enthält die Antwortnachricht für ein einzelnes Stellvertreter.
ms.openlocfilehash: ac99e0ca219fc1f1e117f9288d895e27a1df4700
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19757900"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="47576-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="47576-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="47576-104">Das **DelegateUserResponseMessageType** -Element enthält die Antwortnachricht für ein einzelnes Stellvertreter.</span><span class="sxs-lookup"><span data-stu-id="47576-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="47576-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="47576-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="47576-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="47576-106">Attributes and elements</span></span>

<span data-ttu-id="47576-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="47576-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47576-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="47576-108">Attributes</span></span>

<span data-ttu-id="47576-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="47576-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47576-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47576-110">Child elements</span></span>

|<span data-ttu-id="47576-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="47576-111">**Element**</span></span>|<span data-ttu-id="47576-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47576-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47576-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="47576-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="47576-114">Enthält einen beschreibenden Text für den Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="47576-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="47576-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="47576-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="47576-116">Enthält einen Fehlercode, der den jeweiligen Fehler identifiziert, bei dem die Anforderung auftrat.</span><span class="sxs-lookup"><span data-stu-id="47576-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="47576-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="47576-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="47576-118">Derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="47576-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="47576-119">Es enthält einen Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="47576-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="47576-120">MessageXml</span><span class="sxs-lookup"><span data-stu-id="47576-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="47576-121">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="47576-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="47576-122">Beauftragte Benutzer</span><span class="sxs-lookup"><span data-stu-id="47576-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="47576-123">Identifiziert einen einzelnen Delegaten, der in einer Antwort der Stellvertretung Management zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="47576-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="47576-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47576-124">Parent elements</span></span>

|<span data-ttu-id="47576-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="47576-125">**Element**</span></span>|<span data-ttu-id="47576-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47576-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47576-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="47576-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="47576-128">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Delegaten Management-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="47576-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47576-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47576-129">Remarks</span></span>

<span data-ttu-id="47576-130">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47576-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47576-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="47576-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47576-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="47576-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="47576-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="47576-133">Schema Name</span></span>  <br/> |<span data-ttu-id="47576-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="47576-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="47576-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="47576-135">Validation File</span></span>  <br/> |<span data-ttu-id="47576-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="47576-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="47576-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="47576-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="47576-138">False</span><span class="sxs-lookup"><span data-stu-id="47576-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47576-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47576-139">See also</span></span>

- [<span data-ttu-id="47576-140">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47576-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="47576-141">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47576-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="47576-142">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47576-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="47576-143">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47576-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="47576-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="47576-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

