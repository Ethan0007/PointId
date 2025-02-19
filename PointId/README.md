# PointId: _NuGet Library_
#### _A Unique Identifier Solution Beyond GUIDs_

[![NuGet Downloads](https://img.shields.io/nuget/dt/PointId.svg)](https://github.com/Ethan0007/PointId)
[![NuGet Version](https://img.shields.io/nuget/v/PointId.svg)](https://github.com/Ethan0007/PointId)    
```dotnet add package PointId --version 1.0.3```    

[![PointId](https://github.com/Ethan0007/PointId/blob/development/PointId/PointIcon.png)](https://github.com/Ethan0007/PointId/blob/development/PointId/PointIcon.png)


Introducing the PointId Library: A Unique Identifier Solution Beyond GUIDs
In today's digital landscape, generating unique identifiers for objects and entities is a common requirement across various applications. While GUIDs (Globally Unique Identifiers) have been a popular choice due to their vast uniqueness space, they come with their own set of limitations. Enter the PointId Library—a robust solution that generates unique identifiers by combining various system attributes. In this article, we’ll explore the features of the PointId library and how it compares to traditional GUIDs.

#### The Need for Unique Identifiers
Unique identifiers are essential in numerous scenarios, including database entries, transaction records, and API responses. GUIDs, while widely used, can sometimes be cumbersome due to their length and lack of inherent context. This is where the PointId library shines, offering a more contextually rich identifier.

#### What is the PointId Library?
The PointId Library is designed to create unique identifiers by leveraging several system attributes, such as:   
1. Machine Unique Identifier & Attribute: Obtained based on the operating system, whether Windows, Linux, or macOS.
2. Timestamp: The current time in milliseconds since Unix epoch.
3. Process ID: Identifies the specific process generating the identifier.
4. Counter: A simple counter to ensure uniqueness even when generated in quick succession.
5. Public IP & MAC Address: The device's public-facing IP for additional uniqueness and network identifier that adds another layer of uniqueness..

#### Key Features
Contextual Uniqueness: Unlike GUIDs, which are random, PointId identifiers incorporate meaningful information about the environment they were created in.    

- Easy Integration: The library is straightforward to use, making it easy to integrate into existing C# applications.
- Static Methods: All methods are static, ensuring that no instance creation is necessary for identifier generation.
- Robust Error Handling: The library gracefully handles errors when retrieving machine identifiers or network information.
```
    using PointId = PointGen.PointId;

    public class PointGuid
    {
        static void Main(string[] args)
        {
            var pointId = PointId.NewPointId();
        }
    }
```


#### Comparison with GUIDs
| Feature                | GUIDs                               | PointId Identifiers                      |
|-----------------------|-------------------------------------|----------------------------------------|
| Length                | 36 characters (128 bits)           | 48 characters (variable)              |
| Format                | Randomly generated                  | Contextual and systematic              |
| Uniqueness Source     | Randomness                          | Machine ID, timestamp, IP, MAC        |
| Human-Readability     | Low (alphanumeric)                  | Higher (structured format)             |
| Collision Risk        | Extremely low, but possible         | Minimal due to contextual uniqueness    |

#### Use Cases
The PointId library is ideal for:
- Logging: Unique identifiers for log entries that need to include contextual information about the machine and environment.
- Database Entries: Replacing GUIDs in database schemas with more informative identifiers.
- APIs: Generating unique transaction IDs that carry meaning for client-side debugging and tracing.

#### Unit Testing
[![PointId](https://github.com/Ethan0007/PointId/blob/development/PointId/UnitTest.png)](https://github.com/Ethan0007/PointId/blob/development/PointId/UnitTest.png)

#### License 
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
  Copyright (c) 2024 [Joever Monceda](https://github.com/Ethan0007)
Linkedin: [Joever Monceda](https://www.linkedin.com/in/joever-monceda-55242779/)  
  Medium: [Joever Monceda](https://medium.com/@joever.monceda/new-net-core-vuejs-vuex-router-webpack-starter-kit-e94b6fdb7481)  
  Twitter [@_EthanHunt07](https://twitter.com/_EthanHunt07)  
  Facebook: [Ethan Hunt](https://www.facebook.com/nethan.hound.3/)
