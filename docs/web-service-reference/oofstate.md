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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830651"
---
# <a name="oofstate"></a><span data-ttu-id="09d09-103">OofState</span><span class="sxs-lookup"><span data-stu-id="09d09-103">OofState</span></span>

<span data-ttu-id="09d09-104">Das **OofState** -Element wird zum Abrufen oder Festlegen des Status des Benutzers Out of Office (OOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="09d09-104">The **OofState** element is used to get or set the user's Out of Office (OOF) state.</span></span> 
  
```xml
<OofState>Disabled or Enabled or Scheduled</OofState>
```

 <span data-ttu-id="09d09-105">**OofState**</span><span class="sxs-lookup"><span data-stu-id="09d09-105">**OofState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09d09-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="09d09-106">Attributes and elements</span></span>

<span data-ttu-id="09d09-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="09d09-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09d09-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="09d09-108">Attributes</span></span>

<span data-ttu-id="09d09-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="09d09-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09d09-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09d09-110">Child elements</span></span>

<span data-ttu-id="09d09-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="09d09-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09d09-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09d09-112">Parent elements</span></span>

|<span data-ttu-id="09d09-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="09d09-113">**Element**</span></span>|<span data-ttu-id="09d09-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09d09-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09d09-115">' UserOofSettings '</span><span class="sxs-lookup"><span data-stu-id="09d09-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="09d09-116">Gibt die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="09d09-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="09d09-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="09d09-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="09d09-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="09d09-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="09d09-119">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="09d09-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="09d09-120">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="09d09-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09d09-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="09d09-121">Text value</span></span>

<span data-ttu-id="09d09-122">Ein Textwert ist erforderlich für das **OofState** -Element.</span><span class="sxs-lookup"><span data-stu-id="09d09-122">A text value is required for the **OofState** element.</span></span> <span data-ttu-id="09d09-123">Die folgende Liste enthält die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="09d09-123">The following list contains the possible values for this element:</span></span> 
  
- <span data-ttu-id="09d09-124">**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="09d09-124">**Disabled**</span></span>
    
- <span data-ttu-id="09d09-125">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="09d09-125">**Enabled**</span></span>
    
- <span data-ttu-id="09d09-126">**Geplant**</span><span class="sxs-lookup"><span data-stu-id="09d09-126">**Scheduled**</span></span>
    
<span data-ttu-id="09d09-127">**Geplante** Wert gibt an, dass während eines Zeitraums vom [Dauer (' UserOofSettings ')](duration-useroofsettings.md) -Element identifiziert der Status ABWESEND auf **aktiviert** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="09d09-127">A value of **Scheduled** indicates that the OOF status is set to **Enabled** during a time period identified by the [Duration (UserOofSettings)](duration-useroofsettings.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="09d09-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09d09-128">Remarks</span></span>

<span data-ttu-id="09d09-129">Dieses Element ist in der SetUsersOofSettingRequest-Nachricht und die Nachricht GetUserOofSettingResponse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09d09-129">This element is required in both the SetUsersOofSettingRequest message and the GetUserOofSettingResponse message.</span></span>
  
<span data-ttu-id="09d09-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="09d09-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="09d09-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="09d09-131">Example</span></span>

<span data-ttu-id="09d09-132">Im folgenden Beispiel wird eine Anforderung SetUserOofSettings ermöglicht die **OofState**.</span><span class="sxs-lookup"><span data-stu-id="09d09-132">The following example of a SetUserOofSettings request enables the **OofState**.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="09d09-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="09d09-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09d09-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="09d09-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09d09-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="09d09-135">Schema Name</span></span>  <br/> |<span data-ttu-id="09d09-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="09d09-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="09d09-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="09d09-137">Validation File</span></span>  <br/> |<span data-ttu-id="09d09-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="09d09-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09d09-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="09d09-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="09d09-140">False</span><span class="sxs-lookup"><span data-stu-id="09d09-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09d09-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09d09-141">See also</span></span>



[<span data-ttu-id="09d09-142">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="09d09-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="09d09-143">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="09d09-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

