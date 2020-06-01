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
description: Das UserID-Element identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.
ms.openlocfilehash: 68075e335383835ddce9575d85ba5fa945ed305c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455541"
---
# <a name="userid"></a><span data-ttu-id="f021e-103">UserId</span><span class="sxs-lookup"><span data-stu-id="f021e-103">UserId</span></span>

<span data-ttu-id="f021e-104">Das **UserID** -Element identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f021e-104">The **UserId** element identifies a delegate user or a user who has folder access permissions.</span></span> 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 <span data-ttu-id="f021e-105">**Useridtype**</span><span class="sxs-lookup"><span data-stu-id="f021e-105">**UserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f021e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f021e-106">Attributes and elements</span></span>

<span data-ttu-id="f021e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f021e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f021e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f021e-108">Attributes</span></span>

<span data-ttu-id="f021e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f021e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f021e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f021e-110">Child elements</span></span>

|<span data-ttu-id="f021e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f021e-111">**Element**</span></span>|<span data-ttu-id="f021e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f021e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f021e-113">SID</span><span class="sxs-lookup"><span data-stu-id="f021e-113">SID</span></span>](sid.md) <br/> |<span data-ttu-id="f021e-114">Stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) dar.</span><span class="sxs-lookup"><span data-stu-id="f021e-114">Represents the security descriptor definition language (SDDL) form of the security identifier (SID).</span></span>  <br/> |
|[<span data-ttu-id="f021e-115">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="f021e-115">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="f021e-116">Stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für den Stellvertretungszugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f021e-116">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="f021e-117">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f021e-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="f021e-118">Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste oder eines Stellvertreter Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f021e-118">Defines the display name of a folder, contact, distribution list, or delegate user.</span></span>  <br/> |
|[<span data-ttu-id="f021e-119">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="f021e-119">DistinguishedUser</span></span>](distinguisheduser.md) <br/> |<span data-ttu-id="f021e-120">Identifiziert anonyme und Standardbenutzerkonten für den Stellvertretungszugriff.</span><span class="sxs-lookup"><span data-stu-id="f021e-120">Identifies Anonymous and Default user accounts for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="f021e-121">ExternalUserIdentity</span><span class="sxs-lookup"><span data-stu-id="f021e-121">ExternalUserIdentity</span></span>](externaluseridentity.md) <br/> |<span data-ttu-id="f021e-122">Identifiziert einen externen stellvertretungsbenutzer oder einen externen Benutzer mit Ordnerzugriffsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="f021e-122">Identifies an external delegate user or an external user who has folder access permissions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f021e-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f021e-123">Parent elements</span></span>

|<span data-ttu-id="f021e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f021e-124">**Element**</span></span>|<span data-ttu-id="f021e-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f021e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f021e-126">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="f021e-126">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="f021e-127">Bezeichnet einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f021e-127">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f021e-128">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="f021e-128">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="f021e-129">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="f021e-129">Defines the access that a user has to a folder.</span></span>  <br/> |
|[<span data-ttu-id="f021e-130">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="f021e-130">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="f021e-131">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner.</span><span class="sxs-lookup"><span data-stu-id="f021e-131">Defines the access that a user has to a Calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="f021e-132">UserIds</span><span class="sxs-lookup"><span data-stu-id="f021e-132">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="f021e-133">Enthält ein Array von Delegate-Benutzern, die aus dem Postfach eines Prinzipals abgerufen oder daraus entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f021e-133">Contains an array of delegate users to get or remove from a principal's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f021e-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="f021e-134">Text value</span></span>

<span data-ttu-id="f021e-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="f021e-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f021e-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f021e-136">Remarks</span></span>

<span data-ttu-id="f021e-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f021e-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f021e-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f021e-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f021e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f021e-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f021e-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f021e-140">Schema Name</span></span>  <br/> |<span data-ttu-id="f021e-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f021e-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="f021e-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f021e-142">Validation File</span></span>  <br/> |<span data-ttu-id="f021e-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f021e-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f021e-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f021e-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="f021e-145">False</span><span class="sxs-lookup"><span data-stu-id="f021e-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f021e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f021e-146">See also</span></span>



[<span data-ttu-id="f021e-147">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f021e-147">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="f021e-148">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f021e-148">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="f021e-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f021e-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="f021e-150">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="f021e-150">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

