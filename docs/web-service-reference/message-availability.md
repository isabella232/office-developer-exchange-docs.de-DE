---
title: Message (Verfügbarkeit)
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
description: Das Message-Element enthält die Abwesenheitsantwort (Out of Office).
ms.openlocfilehash: 13d118422ccb5a2897c21b6d124f170bf461dbf6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467004"
---
# <a name="message-availability"></a><span data-ttu-id="78ddc-103">Message (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="78ddc-103">Message (Availability)</span></span>

<span data-ttu-id="78ddc-104">Das **Message** -Element enthält die Abwesenheitsantwort (Out of Office).</span><span class="sxs-lookup"><span data-stu-id="78ddc-104">The **Message** element contains the out of Office (OOF) response.</span></span> 
  
```xml
<Message/> 
```

 <span data-ttu-id="78ddc-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78ddc-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78ddc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78ddc-106">Attributes and elements</span></span>

<span data-ttu-id="78ddc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78ddc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78ddc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78ddc-108">Attributes</span></span>

<span data-ttu-id="78ddc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="78ddc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78ddc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78ddc-110">Child elements</span></span>

<span data-ttu-id="78ddc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="78ddc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78ddc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78ddc-112">Parent elements</span></span>

|<span data-ttu-id="78ddc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="78ddc-113">**Element**</span></span>|<span data-ttu-id="78ddc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78ddc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78ddc-115">InternalReply</span><span class="sxs-lookup"><span data-stu-id="78ddc-115">InternalReply</span></span>](internalreply.md) <br/> | <span data-ttu-id="78ddc-116">Enthält die Abwesenheitsnachricht, die an andere Benutzer in der Domäne des Absenders gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="78ddc-116">Contains the OOF message sent to other users in the sender's domain.</span></span> <br/> <br/>  <span data-ttu-id="78ddc-117">Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="78ddc-117">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[<span data-ttu-id="78ddc-118">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="78ddc-118">ExternalReply</span></span>](externalreply.md) <br/> | <span data-ttu-id="78ddc-119">Enthält die Abwesenheitsnachricht, die an Adressen außerhalb der Domäne des Absenders gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="78ddc-119">Contains the OOF message that is sent to addresses outside the sender's domain.</span></span>  <br/> <br/> <span data-ttu-id="78ddc-120">Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="78ddc-120">The following are the possible XPath expressions to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[<span data-ttu-id="78ddc-121">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="78ddc-121">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="78ddc-122">Enthält eine Abwesenheitsnachricht und die für die Nachricht verwendete Sprache.</span><span class="sxs-lookup"><span data-stu-id="78ddc-122">Contains an OOF message and the language used for the message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78ddc-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="78ddc-123">Text value</span></span>

<span data-ttu-id="78ddc-124">Ein Textwert ist erforderlich, um die Abwesenheitsnachricht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="78ddc-124">A text value is required to set the OOF message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78ddc-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78ddc-125">Remarks</span></span>

<span data-ttu-id="78ddc-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="78ddc-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="78ddc-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="78ddc-127">Example</span></span>

<span data-ttu-id="78ddc-128">Im folgenden Beispiel einer [SetUserOofSettings-Vorgangs](setuseroofsettings-operation.md) Anforderung wird die [OofState](oofstate.md) auf " **aktiviert**" festgelegt, die Dauer von OOF auf 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="78ddc-128">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="78ddc-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="78ddc-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78ddc-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="78ddc-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78ddc-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78ddc-131">Schema Name</span></span>  <br/> |<span data-ttu-id="78ddc-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="78ddc-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="78ddc-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78ddc-133">Validation File</span></span>  <br/> |<span data-ttu-id="78ddc-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78ddc-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78ddc-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="78ddc-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="78ddc-136">False</span><span class="sxs-lookup"><span data-stu-id="78ddc-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78ddc-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78ddc-137">See also</span></span>

- [<span data-ttu-id="78ddc-138">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="78ddc-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="78ddc-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="78ddc-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

