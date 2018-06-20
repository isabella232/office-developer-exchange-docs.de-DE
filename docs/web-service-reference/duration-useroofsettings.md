---
title: Dauer (' UserOofSettings ')
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: Das Dauer-Element gibt die Dauer, die außerhalb der Abwesenheitsstatus (OOF) aktiviert ist, wenn das Element OofState auf geplante Tasks festgelegt ist.
ms.openlocfilehash: 62a5492372fd80173d58e965376b7c8c466825a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758119"
---
# <a name="duration-useroofsettings"></a><span data-ttu-id="a1543-103">Dauer (' UserOofSettings ')</span><span class="sxs-lookup"><span data-stu-id="a1543-103">Duration (UserOofSettings)</span></span>

<span data-ttu-id="a1543-104">Das **Dauer** -Element gibt die Dauer, die außerhalb der Abwesenheitsstatus (OOF) aktiviert ist, wenn das Element [OofState](oofstate.md) **geplant**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1543-104">The **Duration** element specifies the duration that the out of office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 <span data-ttu-id="a1543-105">**Duration**</span><span class="sxs-lookup"><span data-stu-id="a1543-105">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1543-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a1543-106">Attributes and elements</span></span>

<span data-ttu-id="a1543-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a1543-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1543-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a1543-108">Attributes</span></span>

<span data-ttu-id="a1543-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a1543-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1543-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1543-110">Child elements</span></span>

|<span data-ttu-id="a1543-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1543-111">**Element**</span></span>|<span data-ttu-id="a1543-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1543-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1543-113">StartTime</span><span class="sxs-lookup"><span data-stu-id="a1543-113">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="a1543-114">Stellt den Anfang des Zeitraums mit dem Abwesenheitsstatus in festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1543-114">Represents the start of the time span set with an OOF status.</span></span> <span data-ttu-id="a1543-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1543-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="a1543-116">EndTime</span><span class="sxs-lookup"><span data-stu-id="a1543-116">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="a1543-117">Stellt das Ende der Zeitspanne, die mit dem Abwesenheitsstatus in festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1543-117">Represents the end of the time span set with an OOF status.</span></span> <span data-ttu-id="a1543-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1543-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a1543-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1543-119">Parent elements</span></span>

|<span data-ttu-id="a1543-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a1543-120">**Element**</span></span>|<span data-ttu-id="a1543-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1543-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1543-122">' UserOofSettings '</span><span class="sxs-lookup"><span data-stu-id="a1543-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="a1543-123">Gibt die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a1543-123">Specifies the OOF settings.</span></span>  <br/><br/><span data-ttu-id="a1543-124">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a1543-124">The following is the XPath expression to this element:</span></span><br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="a1543-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="a1543-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="a1543-126">Enthält die OOF-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a1543-126">Contains the OOF settings.</span></span><br/><br/><span data-ttu-id="a1543-127">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a1543-127">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[<span data-ttu-id="a1543-128">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="a1543-128">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="a1543-129">Definiert die Antwortnachricht Out of Office (ABWESEND) und eine Dauer für das Senden der Antwortnachricht für ein Postfach.</span><span class="sxs-lookup"><span data-stu-id="a1543-129">Defines the Out of Office (OOF) response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1543-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1543-130">Remarks</span></span>

<span data-ttu-id="a1543-131">Die **Dauer** ist auch der Typ für die Elemente [DetailedSuggestionsWindow](detailedsuggestionswindow.md) [Zeitfenster](timewindow.md)und [OutOfOffice](outofoffice.md) .</span><span class="sxs-lookup"><span data-stu-id="a1543-131">The **Duration** type is also the type for the [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [TimeWindow](timewindow.md), and [OutOfOffice](outofoffice.md) elements.</span></span> 
  
<span data-ttu-id="a1543-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a1543-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="a1543-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a1543-133">Example</span></span>

<span data-ttu-id="a1543-134">Im folgenden Beispiel wird eine Anforderung [SetUserOofSettings Vorgang](setuseroofsettings-operation.md) legt die [OofState](oofstate.md) auf **aktiviert**, die internen und externen OOF-Nachrichten und die Dauer der OOF für 10 Tage.</span><span class="sxs-lookup"><span data-stu-id="a1543-134">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, the internal and external OOF messages, and sets the duration of OOF for 10 days.</span></span>
  
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
        <SetByLegacyClient>false</SetByLegacyClient>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="a1543-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a1543-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1543-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1543-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a1543-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a1543-137">Schema Name</span></span>  <br/> |<span data-ttu-id="a1543-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a1543-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="a1543-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a1543-139">Validation File</span></span>  <br/> |<span data-ttu-id="a1543-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a1543-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a1543-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a1543-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="a1543-142">False</span><span class="sxs-lookup"><span data-stu-id="a1543-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1543-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1543-143">See also</span></span>

- [<span data-ttu-id="a1543-144">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a1543-144">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)  
- [<span data-ttu-id="a1543-145">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a1543-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

