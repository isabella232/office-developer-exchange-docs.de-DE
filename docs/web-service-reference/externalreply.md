---
title: ExternalReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalReply
api_type:
- schema
ms.assetid: cbcfa469-242c-4f98-8f4f-2c9bcbe69f5a
description: Das ExternalReply-Element enthält die Abwesenheitsantwort, die an Adressen außerhalb der Domäne des Empfängers oder der vertrauenswürdigen Domänen gesendet wird.
ms.openlocfilehash: c3381979e5e6aad51f9ae2bb3e661003ef793be6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458761"
---
# <a name="externalreply"></a><span data-ttu-id="4f74b-103">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="4f74b-103">ExternalReply</span></span>

<span data-ttu-id="4f74b-104">Das **ExternalReply** -Element enthält die Abwesenheitsantwort, die an Adressen außerhalb der Domäne des Empfängers oder der vertrauenswürdigen Domänen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f74b-104">The **ExternalReply** element contains the out of office (OOF) response that is sent to addresses outside the recipient's domain or trusted domains.</span></span> 
  
```XML
<ExternalReply>
   <Message/>
</ExternalReply>
```

 <span data-ttu-id="4f74b-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="4f74b-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f74b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f74b-106">Attributes and elements</span></span>

<span data-ttu-id="4f74b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f74b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f74b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f74b-108">Attributes</span></span>

|<span data-ttu-id="4f74b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4f74b-109">**Attribute**</span></span>|<span data-ttu-id="4f74b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f74b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f74b-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="4f74b-111">xml:lang</span></span>  <br/> |<span data-ttu-id="4f74b-112">Gibt die Sprache an, die in der **ExternalReply** -Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f74b-112">Specifies the language used in the **ExternalReply** message.</span></span> <span data-ttu-id="4f74b-113">Die möglichen Werte für dieses Attribut werden durch IETF RFC 3066 definiert.</span><span class="sxs-lookup"><span data-stu-id="4f74b-113">The possible values for this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f74b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f74b-114">Child elements</span></span>

|<span data-ttu-id="4f74b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f74b-115">**Element**</span></span>|<span data-ttu-id="4f74b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f74b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f74b-117">Message (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="4f74b-117">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="4f74b-118">Enthält die Abwesenheitsantwort.</span><span class="sxs-lookup"><span data-stu-id="4f74b-118">Contains the OOF response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f74b-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f74b-119">Parent elements</span></span>

|<span data-ttu-id="4f74b-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f74b-120">**Element**</span></span>|<span data-ttu-id="4f74b-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f74b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f74b-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="4f74b-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="4f74b-123">Gibt die Abwesenheitseinstellungen an.</span><span class="sxs-lookup"><span data-stu-id="4f74b-123">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="4f74b-124">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="4f74b-124">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="4f74b-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="4f74b-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="4f74b-126">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4f74b-126">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="4f74b-127">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="4f74b-127">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f74b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f74b-128">Remarks</span></span>

<span data-ttu-id="4f74b-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4f74b-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="4f74b-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4f74b-130">Example</span></span>

<span data-ttu-id="4f74b-131">Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird die [OofState](oofstate.md) auf **Enabled**festgelegt, die Dauer OOF auf 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f74b-131">The following example of a SetUserOofSettings request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="4f74b-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4f74b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f74b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f74b-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f74b-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f74b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4f74b-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4f74b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f74b-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f74b-136">Validation File</span></span>  <br/> |<span data-ttu-id="4f74b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f74b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f74b-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f74b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f74b-139">False</span><span class="sxs-lookup"><span data-stu-id="4f74b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f74b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f74b-140">See also</span></span>



[<span data-ttu-id="4f74b-141">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4f74b-141">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

