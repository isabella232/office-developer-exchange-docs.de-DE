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
description: Das Element ExternalAudience legt oder enthält einen Wert, der bestimmt, denen externe Out of Office (OOF) Testnachrichten gesendet werden.
ms.openlocfilehash: 836b0f6a5140a37e1584f571cb8e26534fe7a25f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758368"
---
# <a name="externalaudience"></a><span data-ttu-id="e6e66-103">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="e6e66-103">ExternalAudience</span></span>

<span data-ttu-id="e6e66-104">Das Element **ExternalAudience** legt oder enthält einen Wert, der bestimmt, denen externe Out of Office (OOF) Testnachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6e66-104">The **ExternalAudience** element sets or contains a value that determines to whom external Out of Office (OOF) messages are sent.</span></span> 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 <span data-ttu-id="e6e66-105">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="e6e66-105">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6e66-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e6e66-106">Attributes and elements</span></span>

<span data-ttu-id="e6e66-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e6e66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6e66-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6e66-108">Attributes</span></span>

<span data-ttu-id="e6e66-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6e66-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6e66-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6e66-110">Child elements</span></span>

<span data-ttu-id="e6e66-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6e66-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e6e66-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6e66-112">Parent elements</span></span>

|<span data-ttu-id="e6e66-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6e66-113">**Element**</span></span>|<span data-ttu-id="e6e66-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6e66-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6e66-115">' UserOofSettings '</span><span class="sxs-lookup"><span data-stu-id="e6e66-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="e6e66-116">Gibt die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="e6e66-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="e6e66-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e6e66-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="e6e66-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="e6e66-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="e6e66-119">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="e6e66-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="e6e66-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e6e66-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e6e66-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="e6e66-121">Text value</span></span>

<span data-ttu-id="e6e66-122">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e6e66-122">A text value is required for this element.</span></span> <span data-ttu-id="e6e66-123">Die folgende Tabelle enthält die möglichen Werte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="e6e66-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="e6e66-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e6e66-124">**Value**</span></span>|<span data-ttu-id="e6e66-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6e66-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6e66-126">**None**</span><span class="sxs-lookup"><span data-stu-id="e6e66-126">**None**</span></span> <br/> |<span data-ttu-id="e6e66-127">E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer werden keine externe OOF Nachricht beantwortet.</span><span class="sxs-lookup"><span data-stu-id="e6e66-127">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="e6e66-128">**Bekannte**</span><span class="sxs-lookup"><span data-stu-id="e6e66-128">**Known**</span></span> <br/> |<span data-ttu-id="e6e66-129">E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an den Benutzer nur eine externe OOF Nachrichtenantwort erhält, wenn der Absender in Exchange des Benutzers ist speichern Kontaktliste.</span><span class="sxs-lookup"><span data-stu-id="e6e66-129">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="e6e66-130">**All**</span><span class="sxs-lookup"><span data-stu-id="e6e66-130">**All**</span></span> <br/> |<span data-ttu-id="e6e66-131">E-Mail-Absender außerhalb der Organisation das des Postfachbenutzers, die Senden von Nachrichten an die Benutzer erhalten eine externe OOF Nachrichtenantwort.</span><span class="sxs-lookup"><span data-stu-id="e6e66-131">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6e66-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e6e66-132">Remarks</span></span>

<span data-ttu-id="e6e66-133">Dieses Element gibt den gleichen Datentyp wie das [AllowExternalOof](allowexternaloof.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="e6e66-133">This element shares the same type as the [AllowExternalOof](allowexternaloof.md) element.</span></span> 
  
<span data-ttu-id="e6e66-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e6e66-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="e6e66-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e6e66-135">Example</span></span>

<span data-ttu-id="e6e66-136">Im folgenden Beispiel wird eine Anforderung SetUserOofSettings legt die OoFState **aktiviert**, wird die externe Benutzergruppe auf **Alle**, wird die Dauer der OOF auf 10 Tage und die internen und externen Abwesenheitsnachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6e66-136">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the external audience to **All**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="e6e66-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e6e66-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6e66-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6e66-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6e66-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e6e66-139">Schema Name</span></span>  <br/> |<span data-ttu-id="e6e66-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e6e66-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6e66-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e6e66-141">Validation File</span></span>  <br/> |<span data-ttu-id="e6e66-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6e66-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6e66-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e6e66-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6e66-144">False</span><span class="sxs-lookup"><span data-stu-id="e6e66-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6e66-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6e66-145">See also</span></span>



[<span data-ttu-id="e6e66-146">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6e66-146">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="e6e66-147">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6e66-147">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

