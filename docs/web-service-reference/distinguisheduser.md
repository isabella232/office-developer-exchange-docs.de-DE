---
title: DistinguishedUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: Das DistinguishedUser-Element identifiziert anonyme und Standardbenutzerkonten für den Stellvertretungszugriff. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 922c36251290d7090cdafbed9e570144593ca97e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530733"
---
# <a name="distinguisheduser"></a><span data-ttu-id="85056-104">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="85056-104">DistinguishedUser</span></span>

<span data-ttu-id="85056-105">Das **DistinguishedUser** -Element identifiziert anonyme und Standardbenutzerkonten für den Stellvertretungszugriff.</span><span class="sxs-lookup"><span data-stu-id="85056-105">The **DistinguishedUser** element identifies Anonymous and Default user accounts for delegate access.</span></span> <span data-ttu-id="85056-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="85056-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 <span data-ttu-id="85056-107">**DistinguishedUserType**</span><span class="sxs-lookup"><span data-stu-id="85056-107">**DistinguishedUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85056-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="85056-108">Attributes and elements</span></span>

<span data-ttu-id="85056-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="85056-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85056-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="85056-110">Attributes</span></span>

<span data-ttu-id="85056-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="85056-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85056-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85056-112">Child elements</span></span>

<span data-ttu-id="85056-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="85056-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85056-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85056-114">Parent elements</span></span>

|<span data-ttu-id="85056-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="85056-115">**Element**</span></span>|<span data-ttu-id="85056-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85056-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85056-117">UserId</span><span class="sxs-lookup"><span data-stu-id="85056-117">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="85056-118">Identifiziert einen Stellvertreter Benutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="85056-118">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="85056-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="85056-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="85056-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="85056-120">Text value</span></span>

<span data-ttu-id="85056-121">Der Textwert **default** beschreibt die Standardeinstellung für Delegate-Benutzer, die dem Postfach des Prinzipals hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="85056-121">A text value of **Default** describes the default setting for delegate users who are added to the principal's mailbox.</span></span> <span data-ttu-id="85056-122">Der Textwert **Anonym** beschreibt die Stell Vertretungs Zugriffseinstellungen, die anonyme Benutzer für das Postfach des Prinzipals besitzen.</span><span class="sxs-lookup"><span data-stu-id="85056-122">A text value of **Anonymous** describes the delegate access settings that anonymous users have on the principal's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85056-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85056-123">Remarks</span></span>

<span data-ttu-id="85056-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="85056-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85056-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="85056-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85056-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="85056-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85056-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="85056-127">Schema Name</span></span>  <br/> |<span data-ttu-id="85056-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="85056-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="85056-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="85056-129">Validation File</span></span>  <br/> |<span data-ttu-id="85056-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85056-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85056-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="85056-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="85056-132">False</span><span class="sxs-lookup"><span data-stu-id="85056-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85056-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85056-133">See also</span></span>

- [<span data-ttu-id="85056-134">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85056-134">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="85056-135">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85056-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="85056-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="85056-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="85056-137">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="85056-137">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

