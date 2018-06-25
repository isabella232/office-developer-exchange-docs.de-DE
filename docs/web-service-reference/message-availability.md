---
title: Nachricht (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 1eec24dd-c981-41f4-a2f0-c51d43f1d7c0
description: Message-Elements enthält Out-of-Antwort (Office, OOF).
ms.openlocfilehash: 9facd04767fdcc0fd9dfd84fc6badb1a7633d2b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830452"
---
# <a name="message-availability"></a><span data-ttu-id="3beb5-103">Nachricht (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="3beb5-103">Message (Availability)</span></span>

<span data-ttu-id="3beb5-104">**Message** -Elements enthält Out-of-Antwort (Office, OOF).</span><span class="sxs-lookup"><span data-stu-id="3beb5-104">The **Message** element contains the out of Office (OOF) response.</span></span> 
  
```xml
<Message/> 
```

 <span data-ttu-id="3beb5-105">**string**</span><span class="sxs-lookup"><span data-stu-id="3beb5-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3beb5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3beb5-106">Attributes and elements</span></span>

<span data-ttu-id="3beb5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3beb5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3beb5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3beb5-108">Attributes</span></span>

<span data-ttu-id="3beb5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3beb5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3beb5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3beb5-110">Child elements</span></span>

<span data-ttu-id="3beb5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3beb5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3beb5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3beb5-112">Parent elements</span></span>

|<span data-ttu-id="3beb5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3beb5-113">**Element**</span></span>|<span data-ttu-id="3beb5-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3beb5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3beb5-115">InternalReply</span><span class="sxs-lookup"><span data-stu-id="3beb5-115">InternalReply</span></span>](internalreply.md) <br/> | <span data-ttu-id="3beb5-116">Enthält die Abwesenheitsnachricht an andere Benutzer in die Domäne des Absenders gesendet.</span><span class="sxs-lookup"><span data-stu-id="3beb5-116">Contains the OOF message sent to other users in the sender's domain.</span></span> <br/> <br/>  <span data-ttu-id="3beb5-117">Im folgenden sind die möglichen XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3beb5-117">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[<span data-ttu-id="3beb5-118">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="3beb5-118">ExternalReply</span></span>](externalreply.md) <br/> | <span data-ttu-id="3beb5-119">Enthält die Abwesenheitsnachricht, die an Adressen außerhalb der Domäne des Absenders gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3beb5-119">Contains the OOF message that is sent to addresses outside the sender's domain.</span></span>  <br/> <br/> <span data-ttu-id="3beb5-120">Im folgenden sind die möglichen XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3beb5-120">The following are the possible XPath expressions to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[<span data-ttu-id="3beb5-121">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="3beb5-121">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="3beb5-122">Enthält eine Abwesenheitsnachricht und die Sprache für die Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3beb5-122">Contains an OOF message and the language used for the message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3beb5-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="3beb5-123">Text value</span></span>

<span data-ttu-id="3beb5-124">Ein Textwert ist erforderlich, um die Abwesenheitsnachricht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3beb5-124">A text value is required to set the OOF message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3beb5-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3beb5-125">Remarks</span></span>

<span data-ttu-id="3beb5-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3beb5-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="3beb5-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3beb5-127">Example</span></span>

<span data-ttu-id="3beb5-128">Im folgenden Beispiel wird eine Anforderung [SetUserOofSettings Vorgang](setuseroofsettings-operation.md) legt die [OofState](oofstate.md) auf **aktiviert**, wird die Dauer der OOF auf 10 Tage, und die internen und externen Abwesenheitsnachrichten.</span><span class="sxs-lookup"><span data-stu-id="3beb5-128">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="3beb5-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3beb5-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3beb5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3beb5-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3beb5-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3beb5-131">Schema Name</span></span>  <br/> |<span data-ttu-id="3beb5-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3beb5-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="3beb5-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3beb5-133">Validation File</span></span>  <br/> |<span data-ttu-id="3beb5-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3beb5-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3beb5-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3beb5-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="3beb5-136">False</span><span class="sxs-lookup"><span data-stu-id="3beb5-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3beb5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3beb5-137">See also</span></span>

- [<span data-ttu-id="3beb5-138">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3beb5-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="3beb5-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3beb5-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

