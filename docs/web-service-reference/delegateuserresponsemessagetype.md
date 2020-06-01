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
description: Das DelegateUserResponseMessageType-Element enthält die Antwortnachricht für einen einzelnen Delegate-Benutzer.
ms.openlocfilehash: d7addac2ef05d50e0043490ac20d299ece7d577b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457382"
---
# <a name="delegateuserresponsemessagetype"></a><span data-ttu-id="c4093-103">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="c4093-103">DelegateUserResponseMessageType</span></span>

<span data-ttu-id="c4093-104">Das **DelegateUserResponseMessageType** -Element enthält die Antwortnachricht für einen einzelnen Delegate-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c4093-104">The **DelegateUserResponseMessageType** element contains the response message for a single delegate user.</span></span> 
  
```xml
<DelegateUserResponseMessageType>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DelegateUser/>
</DelegateUserResponseMessageType>
```

<span data-ttu-id="c4093-105">**DelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c4093-105">**DelegateUserResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c4093-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c4093-106">Attributes and elements</span></span>

<span data-ttu-id="c4093-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c4093-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4093-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c4093-108">Attributes</span></span>

<span data-ttu-id="c4093-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4093-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4093-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4093-110">Child elements</span></span>

|<span data-ttu-id="c4093-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4093-111">**Element**</span></span>|<span data-ttu-id="c4093-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4093-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4093-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="c4093-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="c4093-114">Enthält eine Textbeschreibung des Status der Antwort.</span><span class="sxs-lookup"><span data-stu-id="c4093-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="c4093-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c4093-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="c4093-116">Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c4093-116">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="c4093-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c4093-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="c4093-118">Wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="c4093-118">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="c4093-119">Sie enthält den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="c4093-119">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="c4093-120">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="c4093-120">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="c4093-121">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="c4093-121">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="c4093-122">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="c4093-122">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="c4093-123">Identifiziert einen einzelnen Delegaten, der in einer Antwort zum Delegieren der Verwaltung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4093-123">Identifies a single delegate that is returned in a delegate management response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c4093-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c4093-124">Parent elements</span></span>

|<span data-ttu-id="c4093-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="c4093-125">**Element**</span></span>|<span data-ttu-id="c4093-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4093-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4093-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="c4093-127">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="c4093-128">Enthält die Antwortnachrichten für eine Verwaltungsanforderung für Exchange Webdienste Delegate.</span><span class="sxs-lookup"><span data-stu-id="c4093-128">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4093-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4093-129">Remarks</span></span>

<span data-ttu-id="c4093-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c4093-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4093-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c4093-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4093-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4093-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c4093-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c4093-133">Schema Name</span></span>  <br/> |<span data-ttu-id="c4093-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c4093-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c4093-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4093-135">Validation File</span></span>  <br/> |<span data-ttu-id="c4093-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c4093-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c4093-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c4093-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4093-138">False</span><span class="sxs-lookup"><span data-stu-id="c4093-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4093-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4093-139">See also</span></span>

- [<span data-ttu-id="c4093-140">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4093-140">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="c4093-141">GetDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4093-141">GetDelegate operation</span></span>](getdelegate-operation.md) 
- [<span data-ttu-id="c4093-142">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4093-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="c4093-143">RemoveDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4093-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)
- [<span data-ttu-id="c4093-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c4093-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

