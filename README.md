# KarateGen - Karate DSL Code Generator

A premium JetBrains IDE plugin for generating [Karate DSL](https://github.com/karatelabs/karate) code from various API specification formats.

![Plugin Icon](src/main/resources/META-INF/pluginIcon.svg)

## Overview

KarateGen simplifies the process of creating Karate DSL test scripts by automatically converting:
- cURL commands
- Postman collections
- Swagger/OpenAPI specifications

This plugin helps API testers and developers save time by generating Karate test templates from existing API documentation or commands.

## Features

- **Convert cURL commands to Karate DSL** - Paste any cURL command and get equivalent Karate code
- **Convert Postman collections to Karate DSL** - Import your Postman collections and convert them to Karate tests
- **Convert Swagger/OpenAPI specifications to Karate DSL** - Generate tests from your API documentation
- **Easy-to-use interface** - Simple UI with copy-to-clipboard functionality
- **Offline fallback** - Basic conversion works even without internet connection

## Requirements

- IntelliJ IDEA 2024.2 or newer (Community or Ultimate edition)
- Java 21 or newer

## Installation

1. Open your JetBrains IDE (IntelliJ IDEA)
2. Go to **Settings/Preferences > Plugins**
3. Click on the **Marketplace** tab
4. Search for "KarateGen"
5. Click **Install**
6. Restart your IDE when prompted

## Usage

1. Open your project in IntelliJ IDEA
2. Look for the KarateGen tool window on the right side of your IDE
3. Select the source format (curl, postman, swagger) from the dropdown
4. Paste your API specification in the input area
5. Click "Generate code to Karate"
6. The generated Karate DSL code will appear in the result area
7. Click "Copy to Clipboard" to use the generated code in your project

## Examples

### Converting a cURL command

Input:
```
curl -X POST "https://api.example.com/users" -H "Content-Type: application/json" -d '{"name":"John","email":"john@example.com"}'
```

Output:
```
# Generated Karate script
Given url 'https://api.example.com/users'
And headers {
  Content-Type: 'application/json',
}
And request {"name":"John","email":"john@example.com"}
When method POST
Then status 200
```

## Licensing

KarateGen is licensed under a proprietary license. All rights reserved.

Unauthorized use, distribution, or modification is prohibited. For licensing inquiries, please contact chancaysergio@gmail.com.

The plugin is distributed as a premium product with a subscription model through the JetBrains Marketplace. This subscription covers:

- Access to the cloud-based conversion service
- Premium support
- Regular updates and new features

A free trial is available to test the plugin before purchasing.

## End User License Agreement (EULA)

By installing and using this plugin, you agree to the terms of the [EULA](EULA.md) and the [GPL-3.0 License](LICENSE).

## Support

For support, feature requests, or bug reports, please contact:
- Email: chancaysergio@gmail.com
- GitHub: https://github.com/sercheo87

## Acknowledgments

- [Karate DSL](https://github.com/karatelabs/karate) - The awesome API testing framework
- [JetBrains](https://www.jetbrains.com/) - For their excellent IDE and plugin ecosystem
