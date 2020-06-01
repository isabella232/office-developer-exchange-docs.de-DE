---
title: Recipients (ArrayOfSmtpAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: cf68417d-85cf-49e0-857a-f987d3675344
description: Das Recipients-Element gibt ein Array von Empfängern einer Nachricht an.
ms.openlocfilehash: 4c2478a81836c2e52baad9c928d112108679b837
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465506"
---
# <a name="recipients-arrayofsmtpaddresstype"></a><span data-ttu-id="bdbff-103">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="bdbff-103">Recipients (ArrayOfSmtpAddressType)</span></span>

<span data-ttu-id="bdbff-104">Das **Recipients** -Element gibt ein Array von Empfängern einer Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="bdbff-104">The **Recipients** element specifies an array of recipients of a message.</span></span> 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 <span data-ttu-id="bdbff-105">**ArrayOfSmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="bdbff-105">**ArrayOfSmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bdbff-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bdbff-106">Attributes and elements</span></span>

<span data-ttu-id="bdbff-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bdbff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdbff-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bdbff-108">Attributes</span></span>

<span data-ttu-id="bdbff-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bdbff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bdbff-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdbff-110">Child elements</span></span>

|<span data-ttu-id="bdbff-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdbff-111">**Element**</span></span>|<span data-ttu-id="bdbff-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdbff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdbff-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="bdbff-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="bdbff-114">Stellt die Simple Mail Transfer Protocol (SMTP) Empfängeradresse einer Kalender-oder Kontaktfreigabe Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="bdbff-114">Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdbff-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bdbff-115">Parent elements</span></span>

|<span data-ttu-id="bdbff-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bdbff-116">**Element**</span></span>|<span data-ttu-id="bdbff-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bdbff-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdbff-118">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="bdbff-118">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="bdbff-119">Definiert eine Anforderung zum Abrufen eines nicht transparenten Authentifizierungstokens, das die Freigabeeinladung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bdbff-119">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdbff-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdbff-120">Remarks</span></span>

<span data-ttu-id="bdbff-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bdbff-121">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdbff-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bdbff-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdbff-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdbff-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bdbff-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bdbff-124">Schema Name</span></span>  <br/> |<span data-ttu-id="bdbff-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bdbff-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bdbff-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bdbff-126">Validation File</span></span>  <br/> |<span data-ttu-id="bdbff-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bdbff-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bdbff-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bdbff-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="bdbff-129">False</span><span class="sxs-lookup"><span data-stu-id="bdbff-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdbff-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdbff-130">See also</span></span>



[<span data-ttu-id="bdbff-131">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bdbff-131">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="bdbff-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bdbff-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

