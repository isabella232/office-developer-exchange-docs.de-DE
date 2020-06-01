---
title: EncryptedSharedFolderDataCollection
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderDataCollection
api_type:
- schema
ms.assetid: 25c6ae87-bbb9-4dd5-a85a-d669fcea137f
description: Das EncryptedSharedFolderDataCollection-Element enthält eine Sammlung von Datenstrukturen, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.
ms.openlocfilehash: e8ed9221952892abda7b4eac62b16cdc4976c6e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461268"
---
# <a name="encryptedsharedfolderdatacollection"></a><span data-ttu-id="283a3-103">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="283a3-103">EncryptedSharedFolderDataCollection</span></span>

<span data-ttu-id="283a3-104">Das **EncryptedSharedFolderDataCollection** -Element enthält eine Sammlung von Datenstrukturen, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="283a3-104">The **EncryptedSharedFolderDataCollection** element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 <span data-ttu-id="283a3-105">**ArrayOfEncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="283a3-105">**ArrayOfEncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="283a3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="283a3-106">Attributes and elements</span></span>

<span data-ttu-id="283a3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="283a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="283a3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="283a3-108">Attributes</span></span>

<span data-ttu-id="283a3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="283a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="283a3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="283a3-110">Child elements</span></span>

|<span data-ttu-id="283a3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="283a3-111">**Element**</span></span>|<span data-ttu-id="283a3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="283a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="283a3-113">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="283a3-113">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="283a3-114">Enthält die verschlüsselten Daten, die ein Client verwenden kann, um die Freigabe seiner Kalender-oder Kontaktdaten für andere Clients zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="283a3-114">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="283a3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="283a3-115">Parent elements</span></span>

|<span data-ttu-id="283a3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="283a3-116">**Element**</span></span>|<span data-ttu-id="283a3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="283a3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="283a3-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="283a3-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="283a3-119">Definiert eine Antwort auf eine [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="283a3-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="283a3-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="283a3-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="283a3-121">Enthält den Status und das Ergebnis einer einzelnen [GetSharingMetadata-Vorgang](getsharingmetadata-operation.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="283a3-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="283a3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="283a3-122">Remarks</span></span>

<span data-ttu-id="283a3-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="283a3-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="283a3-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="283a3-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="283a3-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="283a3-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="283a3-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="283a3-126">Schema Name</span></span>  <br/> |<span data-ttu-id="283a3-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="283a3-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="283a3-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="283a3-128">Validation File</span></span>  <br/> |<span data-ttu-id="283a3-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="283a3-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="283a3-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="283a3-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="283a3-131">False</span><span class="sxs-lookup"><span data-stu-id="283a3-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="283a3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="283a3-132">See also</span></span>

- [<span data-ttu-id="283a3-133">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="283a3-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="283a3-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="283a3-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

