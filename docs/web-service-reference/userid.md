---
title: UserId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: UserId-Element identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner.
ms.openlocfilehash: 8e9867f5a8cdd62dd2dae55fbf527595ac14f46d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839445"
---
# <a name="userid"></a><span data-ttu-id="0f596-103">UserId</span><span class="sxs-lookup"><span data-stu-id="0f596-103">UserId</span></span>

<span data-ttu-id="0f596-104">**UserId** -Element identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner.</span><span class="sxs-lookup"><span data-stu-id="0f596-104">The **UserId** element identifies a delegate user or a user who has folder access permissions.</span></span> 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 <span data-ttu-id="0f596-105">**UserIdType**</span><span class="sxs-lookup"><span data-stu-id="0f596-105">**UserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f596-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0f596-106">Attributes and elements</span></span>

<span data-ttu-id="0f596-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0f596-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f596-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0f596-108">Attributes</span></span>

<span data-ttu-id="0f596-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0f596-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0f596-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f596-110">Child elements</span></span>

|<span data-ttu-id="0f596-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f596-111">**Element**</span></span>|<span data-ttu-id="0f596-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f596-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f596-113">SID</span><span class="sxs-lookup"><span data-stu-id="0f596-113">SID</span></span>](sid.md) <br/> |<span data-ttu-id="0f596-114">Stellt die Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID).</span><span class="sxs-lookup"><span data-stu-id="0f596-114">Represents the security descriptor definition language (SDDL) form of the security identifier (SID).</span></span>  <br/> |
|[<span data-ttu-id="0f596-115">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="0f596-115">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="0f596-116">Stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für Stellvertretungszugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f596-116">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="0f596-117">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="0f596-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="0f596-118">Definiert den Anzeigenamen eines Ordners, Kontakt, Verteilerliste oder Stellvertretungsbenutzers.</span><span class="sxs-lookup"><span data-stu-id="0f596-118">Defines the display name of a folder, contact, distribution list, or delegate user.</span></span>  <br/> |
|[<span data-ttu-id="0f596-119">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="0f596-119">DistinguishedUser</span></span>](distinguisheduser.md) <br/> |<span data-ttu-id="0f596-120">Anonyme und Benutzerkonten für Stellvertretungszugriff identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0f596-120">Identifies Anonymous and Default user accounts for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="0f596-121">ExternalUserIdentity</span><span class="sxs-lookup"><span data-stu-id="0f596-121">ExternalUserIdentity</span></span>](externaluseridentity.md) <br/> |<span data-ttu-id="0f596-122">Identifiziert eine externe Stellvertretungsbenutzers oder ein externer Benutzer, der über Zugriffsberechtigungen für Ordner verfügt.</span><span class="sxs-lookup"><span data-stu-id="0f596-122">Identifies an external delegate user or an external user who has folder access permissions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0f596-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f596-123">Parent elements</span></span>

|<span data-ttu-id="0f596-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0f596-124">**Element**</span></span>|<span data-ttu-id="0f596-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0f596-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f596-126">Beauftragte Benutzer</span><span class="sxs-lookup"><span data-stu-id="0f596-126">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="0f596-127">Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="0f596-127">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0f596-128">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="0f596-128">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="0f596-129">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0f596-129">Defines the access that a user has to a folder.</span></span>  <br/> |
|[<span data-ttu-id="0f596-130">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="0f596-130">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="0f596-131">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner.</span><span class="sxs-lookup"><span data-stu-id="0f596-131">Defines the access that a user has to a Calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="0f596-132">Benutzer-IDs</span><span class="sxs-lookup"><span data-stu-id="0f596-132">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="0f596-133">Enthält ein Array von Benutzer als Stellvertreter zum Abrufen oder aus einem Prinzipal Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="0f596-133">Contains an array of delegate users to get or remove from a principal's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0f596-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="0f596-134">Text value</span></span>

<span data-ttu-id="0f596-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="0f596-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0f596-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f596-136">Remarks</span></span>

<span data-ttu-id="0f596-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0f596-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f596-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0f596-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f596-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f596-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0f596-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0f596-140">Schema Name</span></span>  <br/> |<span data-ttu-id="0f596-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0f596-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="0f596-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0f596-142">Validation File</span></span>  <br/> |<span data-ttu-id="0f596-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0f596-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0f596-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0f596-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="0f596-145">False</span><span class="sxs-lookup"><span data-stu-id="0f596-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f596-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f596-146">See also</span></span>



[<span data-ttu-id="0f596-147">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0f596-147">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="0f596-148">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0f596-148">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="0f596-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0f596-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0f596-150">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="0f596-150">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

