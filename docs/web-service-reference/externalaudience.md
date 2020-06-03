---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: Das ExternalAudience-Element legt fest oder enthält einen Wert, der bestimmt, an wen externe Abwesenheit (Out of Office, OOF) Nachrichten gesendet werden.
ms.openlocfilehash: b3fcebd9042b07bb9a8294196799ef2a13d78bdd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530600"
---
# <a name="externalaudience"></a><span data-ttu-id="eb119-103">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="eb119-103">ExternalAudience</span></span>

<span data-ttu-id="eb119-104">Das **ExternalAudience** -Element legt fest oder enthält einen Wert, der bestimmt, an wen externe Abwesenheit (Out of Office, OOF) Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb119-104">The **ExternalAudience** element sets or contains a value that determines to whom external Out of Office (OOF) messages are sent.</span></span> 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 <span data-ttu-id="eb119-105">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="eb119-105">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb119-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eb119-106">Attributes and elements</span></span>

<span data-ttu-id="eb119-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb119-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb119-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eb119-108">Attributes</span></span>

<span data-ttu-id="eb119-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb119-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb119-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb119-110">Child elements</span></span>

<span data-ttu-id="eb119-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb119-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb119-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb119-112">Parent elements</span></span>

|<span data-ttu-id="eb119-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb119-113">**Element**</span></span>|<span data-ttu-id="eb119-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb119-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb119-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="eb119-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="eb119-116">Gibt die Abwesenheitseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="eb119-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="eb119-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="eb119-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="eb119-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="eb119-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="eb119-119">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="eb119-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="eb119-120">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="eb119-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb119-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="eb119-121">Text value</span></span>

<span data-ttu-id="eb119-122">Für dieses Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eb119-122">A text value is required for this element.</span></span> <span data-ttu-id="eb119-123">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb119-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="eb119-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="eb119-124">**Value**</span></span>|<span data-ttu-id="eb119-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb119-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb119-126">**Keine**</span><span class="sxs-lookup"><span data-stu-id="eb119-126">**None**</span></span> <br/> |<span data-ttu-id="eb119-127">E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten keine externe Abwesenheitsnachrichten Antwort.</span><span class="sxs-lookup"><span data-stu-id="eb119-127">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="eb119-128">**Bezeichnet**</span><span class="sxs-lookup"><span data-stu-id="eb119-128">**Known**</span></span> <br/> |<span data-ttu-id="eb119-129">E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten nur dann eine externe Abwesenheitsnachrichten Antwort, wenn sich der Absender in der Exchange-Informationsspeicher Kontaktliste des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="eb119-129">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="eb119-130">**All**</span><span class="sxs-lookup"><span data-stu-id="eb119-130">**All**</span></span> <br/> |<span data-ttu-id="eb119-131">E-Mail-Absender außerhalb der Organisation des Postfachbenutzers, die Nachrichten an den Benutzer senden, erhalten eine externe Abwesenheitsnachrichten Antwort.</span><span class="sxs-lookup"><span data-stu-id="eb119-131">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb119-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb119-132">Remarks</span></span>

<span data-ttu-id="eb119-133">Dieses Element hat denselben Typ wie das [AllowExternalOof](allowexternaloof.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="eb119-133">This element shares the same type as the [AllowExternalOof](allowexternaloof.md) element.</span></span> 
  
<span data-ttu-id="eb119-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="eb119-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="eb119-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eb119-135">Example</span></span>

<span data-ttu-id="eb119-136">Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird die OoFState auf " **aktiviert**" festgelegt, die externe Benutzergruppe auf " **all**" festgelegt, die Dauer von OOF auf 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb119-136">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the external audience to **All**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="eb119-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="eb119-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb119-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb119-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb119-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eb119-139">Schema Name</span></span>  <br/> |<span data-ttu-id="eb119-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="eb119-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb119-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eb119-141">Validation File</span></span>  <br/> |<span data-ttu-id="eb119-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb119-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb119-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eb119-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb119-144">False</span><span class="sxs-lookup"><span data-stu-id="eb119-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb119-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb119-145">See also</span></span>



[<span data-ttu-id="eb119-146">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eb119-146">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="eb119-147">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eb119-147">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

