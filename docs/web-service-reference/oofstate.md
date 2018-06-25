---
title: OofState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofState
api_type:
- schema
ms.assetid: 3c486a38-06da-4382-ad20-664d067d76ac
description: Das OofState-Element wird zum Abrufen oder Festlegen des Status des Benutzers Out of Office (OOF) verwendet.
ms.openlocfilehash: f97c050aec102b384fa4d98e6dee43befd4dc9ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830651"
---
# <a name="oofstate"></a><span data-ttu-id="d567b-103">OofState</span><span class="sxs-lookup"><span data-stu-id="d567b-103">OofState</span></span>

<span data-ttu-id="d567b-104">Das **OofState** -Element wird zum Abrufen oder Festlegen des Status des Benutzers Out of Office (OOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d567b-104">The **OofState** element is used to get or set the user's Out of Office (OOF) state.</span></span> 
  
```xml
<OofState>Disabled or Enabled or Scheduled</OofState>
```

 <span data-ttu-id="d567b-105">**OofState**</span><span class="sxs-lookup"><span data-stu-id="d567b-105">**OofState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d567b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d567b-106">Attributes and elements</span></span>

<span data-ttu-id="d567b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d567b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d567b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d567b-108">Attributes</span></span>

<span data-ttu-id="d567b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d567b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d567b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d567b-110">Child elements</span></span>

<span data-ttu-id="d567b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d567b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d567b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d567b-112">Parent elements</span></span>

|<span data-ttu-id="d567b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d567b-113">**Element**</span></span>|<span data-ttu-id="d567b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d567b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d567b-115">' UserOofSettings '</span><span class="sxs-lookup"><span data-stu-id="d567b-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="d567b-116">Gibt die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d567b-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="d567b-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d567b-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="d567b-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="d567b-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="d567b-119">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d567b-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="d567b-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d567b-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d567b-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d567b-121">Text value</span></span>

<span data-ttu-id="d567b-122">Ein Textwert ist erforderlich für das **OofState** -Element.</span><span class="sxs-lookup"><span data-stu-id="d567b-122">A text value is required for the **OofState** element.</span></span> <span data-ttu-id="d567b-123">Die folgende Liste enthält die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d567b-123">The following list contains the possible values for this element:</span></span> 
  
- <span data-ttu-id="d567b-124">**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="d567b-124">**Disabled**</span></span>
    
- <span data-ttu-id="d567b-125">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="d567b-125">**Enabled**</span></span>
    
- <span data-ttu-id="d567b-126">**Geplant**</span><span class="sxs-lookup"><span data-stu-id="d567b-126">**Scheduled**</span></span>
    
<span data-ttu-id="d567b-127">**Geplante** Wert gibt an, dass während eines Zeitraums vom [Dauer (' UserOofSettings ')](duration-useroofsettings.md) -Element identifiziert der Status ABWESEND auf **aktiviert** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d567b-127">A value of **Scheduled** indicates that the OOF status is set to **Enabled** during a time period identified by the [Duration (UserOofSettings)](duration-useroofsettings.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d567b-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d567b-128">Remarks</span></span>

<span data-ttu-id="d567b-129">Dieses Element ist in der SetUsersOofSettingRequest-Nachricht und die Nachricht GetUserOofSettingResponse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d567b-129">This element is required in both the SetUsersOofSettingRequest message and the GetUserOofSettingResponse message.</span></span>
  
<span data-ttu-id="d567b-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d567b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="d567b-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d567b-131">Example</span></span>

<span data-ttu-id="d567b-132">Im folgenden Beispiel wird eine Anforderung SetUserOofSettings ermöglicht die **OofState**.</span><span class="sxs-lookup"><span data-stu-id="d567b-132">The following example of a SetUserOofSettings request enables the **OofState**.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="d567b-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d567b-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d567b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d567b-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d567b-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d567b-135">Schema Name</span></span>  <br/> |<span data-ttu-id="d567b-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d567b-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="d567b-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d567b-137">Validation File</span></span>  <br/> |<span data-ttu-id="d567b-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d567b-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d567b-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d567b-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="d567b-140">False</span><span class="sxs-lookup"><span data-stu-id="d567b-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d567b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d567b-141">See also</span></span>



[<span data-ttu-id="d567b-142">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d567b-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="d567b-143">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d567b-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

