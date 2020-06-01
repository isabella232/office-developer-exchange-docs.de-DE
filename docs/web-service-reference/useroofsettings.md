---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: Das UserOofSettings-Element gibt die Abwesenheit (Out of Office, OOF) Einstellungen an.
ms.openlocfilehash: 417c3d5061a6229d41eb57f72e89f03213acf460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461905"
---
# <a name="useroofsettings"></a><span data-ttu-id="ee6c1-103">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ee6c1-103">UserOofSettings</span></span>

<span data-ttu-id="ee6c1-104">Das **UserOofSettings** -Element gibt die Abwesenheit (Out of Office, OOF) Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-104">The **UserOofSettings** element specifies the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="ee6c1-105">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="ee6c1-105">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
  
[<span data-ttu-id="ee6c1-106">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="ee6c1-106">UserOofSettings</span></span>](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 <span data-ttu-id="ee6c1-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="ee6c1-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee6c1-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ee6c1-108">Attributes and elements</span></span>

<span data-ttu-id="ee6c1-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee6c1-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ee6c1-110">Attributes</span></span>

<span data-ttu-id="ee6c1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee6c1-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ee6c1-112">Child elements</span></span>

|<span data-ttu-id="ee6c1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ee6c1-113">**Element**</span></span>|<span data-ttu-id="ee6c1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ee6c1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee6c1-115">OofState</span><span class="sxs-lookup"><span data-stu-id="ee6c1-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="ee6c1-116">Legt den Abwesenheitsstatus des Benutzers fest.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-116">Sets the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="ee6c1-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="ee6c1-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="ee6c1-118">Legt fest oder enthält einen Wert, der bestimmt, an wen externe Abwesenheitsnachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-118">Sets or contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="ee6c1-119">Dauer (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="ee6c1-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="ee6c1-120">Gibt die Dauer an, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-120">Specifies the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="ee6c1-121">Wenn das [OofState](oofstate.md) -Element auf **aktiviert** oder **deaktiviert**festgelegt ist, wird der Wert dieses Elements ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="ee6c1-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="ee6c1-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="ee6c1-123">Enthält die Abwesenheitsantwort, die an andere Benutzer in der Domäne des Benutzers oder an vertrauenswürdigen Domänen gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-123">Contains the OOF response sent to other users in the user's domain or trusted domains.</span></span>  <br/> |
|[<span data-ttu-id="ee6c1-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="ee6c1-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="ee6c1-125">Enthält die Abwesenheitsantwort, die an Adressen außerhalb der Domäne des Empfängers oder vertrauenswürdiger Domänen gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ee6c1-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ee6c1-126">Parent elements</span></span>

|<span data-ttu-id="ee6c1-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="ee6c1-127">**Element**</span></span>|<span data-ttu-id="ee6c1-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ee6c1-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee6c1-129">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="ee6c1-129">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="ee6c1-130">Enthält die Argumente, die zum Festlegen der Abwesenheitseinstellungen und Nachrichten eines Postfachbenutzers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-130">Contains the arguments used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="ee6c1-131">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ee6c1-131">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee6c1-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee6c1-132">Remarks</span></span>

<span data-ttu-id="ee6c1-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="ee6c1-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ee6c1-134">Example</span></span>

<span data-ttu-id="ee6c1-135">Im folgenden Beispiel einer SetUserOofSettings-Anforderung wird die OoFState auf **Enabled**festgelegt, die Dauer von OOF für 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee6c1-135">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
```xml
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

## <a name="element-information"></a><span data-ttu-id="ee6c1-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ee6c1-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee6c1-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee6c1-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ee6c1-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ee6c1-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ee6c1-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ee6c1-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="ee6c1-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ee6c1-140">Validation File</span></span>  <br/> |<span data-ttu-id="ee6c1-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ee6c1-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ee6c1-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ee6c1-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee6c1-143">False</span><span class="sxs-lookup"><span data-stu-id="ee6c1-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee6c1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee6c1-144">See also</span></span>

- [<span data-ttu-id="ee6c1-145">SetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ee6c1-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

