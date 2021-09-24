---
title: ServerVersion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a
description: Das ServerVersion-Element stellt die Versionsnummer des Computers dar, auf dem Microsoft Exchange Server ausgeführt wird.
ms.openlocfilehash: bc7f9daa62e628e41f7541a609550e90af211928
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527377"
---
# <a name="serverversion-pox"></a>ServerVersion (POX)

Das **ServerVersion-Element** stellt die Versionsnummer des Computers dar, auf dem Microsoft Exchange Server ausgeführt wird. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md)
- [Konto (POX)](account-pox.md)
- [Protokoll (POX)](protocol-pox.md)
- [ServerVersion (POX)](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die Exchange Serverversionsnummer dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der **ServerVersion-Wert** ist nur gültig, wenn das [Type (POX)-Element](type-pox.md) gleich EXCH oder EXPR ist. Der **ServerVersion-Wert** ist eine hexadezimale Zahl, die majorVersion, MinorVersion und MajorBuildNumber des Servers enthält. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein **ServerVersion-Wert** verdeckt, der in einer AutoErmittlungsantwort zurückgegeben wird, um MajorVersion, MinorVersion und MajorBuildNumber abzurufen und anzuzeigen. In diesem Beispiel können Sie einen Hexadezimalwert für den **ServerVersion-Wert** eingeben. Wenn kein **ServerVersion-Wert** eingegeben wird, wird der **ServerVersion-Standardwert** 738180DA verwendet. 
  
```csharp
static void Main(string[] args)
{
    // Convert a ServerVersion value that is returned from an Autodiscover request.
    // The value is a hex value and can be converted to the MajorVersion, MinorVersion,
    // and MajorBuildNumber.
    Console.WriteLine("Enter ServerVersion returned from the Autodiscover (eg. 738180DA) and Enter.");
    Console.WriteLine("To use the default ServerVersion of 738180DA, just hit Enter.");
    // Get the hexadecimal ServerVersion value.
    string serverversionhex = Console.ReadLine();
    // If nothing is entered, use the default server version of "738180DA"
    if (serverversionhex == "")
    {
        serverversionhex = "738180DA";
    }
    Console.WriteLine("ServerVersion (Hex) = " + serverversionhex);
    string serverversionbinary = Convert.ToString(Convert.ToInt32(serverversionhex, 16), 2);
    // The ServerVersion (binary) should be 32 bits in length. If the 
    // server version in binary is a length of 31 characters, the leading
    // zero has been removed in the conversion process. Put the missing zero back.
    if (serverversionbinary.Length == 31)
    {
        serverversionbinary = String.Concat("0", serverversionbinary);
    }
    Console.WriteLine("ServerVersion (bin) = " + serverversionbinary);
    // The first 4 bits represent a number used for comparison against  
    // older version number structures. You can ignore this.
    // The next 6 bits represent the major version number.
    int majorversion = Convert.ToInt32(serverversionbinary.Substring(4, 6), 2);
    Console.WriteLine("MajorVersion: " + majorversion);
    // The next 6 bits represent the minor version number.
    int minorversion = Convert.ToInt32(serverversionbinary.Substring(10, 6), 2);
    Console.WriteLine("MinorVersion: " + minorversion);
    
    // The next bit represent a flag - you can ignore this.
    // The next 15 bits represent the major build number.
    int majorbuild = Convert.ToInt32(serverversionbinary.Substring(17, 15), 2);
    Console.WriteLine("MajorBuildVersion: " + majorbuild);
    Console.WriteLine("\n\nPress any key to continue");
    Console.ReadKey();
}
```

## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

