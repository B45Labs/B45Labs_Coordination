# B45 Labs · Coordination – Third-Party Notices

**Last updated:** 2026-07-23
**Applies to:** B45 Labs | Coordination 3.0.0 (Revit 2023, 2024, 2025, 2026, 2027 builds)

> Version numbers below were read from the actual build output of all five configs on
> 2026-07-23, not from the csproj, so transitive packages are reflected as shipped.
> The Microsoft `Microsoft.Extensions.*`, `System.Security.Cryptography.Pkcs`,
> `System.IO.Packaging` and `Microsoft.Bcl.*` entries moved to 10.0.10 in response to the
> Autodesk App Store vulnerability scan of 2026-07-23. That bump also pulled three new
> transitive components into the payload, marked **(new)** below.

This document lists the third-party components redistributed with the
B45 Labs · Coordination installer and their applicable licenses.

B45 Labs' own assemblies (`B45Labs_Coordination.dll`, `B45Labs.Shared.dll`,
`B45Labs.Connect.Sdk.dll`, `B45Labs.Connect.Contracts.dll`) are proprietary and
are not listed here. Platform components: the **Autodesk Revit API**
(`RevitAPI.dll`, `RevitAPIUI.dll`, referenced via the community
`Revit_All_Main_Versions_API_x64` NuGet package) and the **Microsoft .NET
runtime**: are referenced where present on the user's machine and are **not**
redistributed by this installer.

---

## Redistributed third-party libraries

| Component | Version | License | Source |
|---|---:|---|---|
| BouncyCastle.Cryptography | 2.5.0 | MIT | https://github.com/bcgit/bc-csharp |
| ClosedXML | 0.104.2 | MIT | https://github.com/ClosedXML/ClosedXML |
| ClosedXML.Parser | 1.2.0 | MIT | https://github.com/ClosedXML/ClosedXML.Parser |
| DocumentFormat.OpenXml (incl. `DocumentFormat.OpenXml.Framework.dll`) | 3.1.1 | MIT | https://github.com/dotnet/Open-XML-SDK |
| ExcelNumberFormat | 1.1.0 | MIT | https://github.com/andersnm/ExcelNumberFormat |
| RBush | 4.0.0 | MIT | https://github.com/viceroypenguin/RBush |
| Microsoft.Bcl.Cryptography **(new)** | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| Microsoft.Extensions.DependencyInjection.Abstractions | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| Microsoft.Extensions.Logging.Abstractions | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| Newtonsoft.Json | 13.0.3 | MIT | https://www.newtonsoft.com/json |
| PdfSharp (incl. Charting, BarCodes, Cryptography, Quality, Shared, Snippets, System, WPFonts) | 6.2.4 | MIT | https://github.com/empira/PDFsharp |
| SixLabors.Fonts | 1.0.0 | Apache-2.0 | https://github.com/SixLabors/Fonts |
| System.Data.SQLite (`System.Data.SQLite.dll` + `SQLite.Interop.dll`) | 1.0.119 | Public Domain / SQLite License | https://www.sqlite.org |
| System.Diagnostics.DiagnosticSource **(new)** | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| System.Formats.Asn1 **(new)** | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| System.IO.Packaging | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| System.Security.Cryptography.Pkcs | 10.0.10 | MIT | https://github.com/dotnet/runtime |
| WeCantSpell.Hunspell | 7.0.1 | MIT | https://github.com/aarondandy/WeCantSpell.Hunspell |

> The **Revit 2023 / 2024** (net48) builds additionally ship the following
> Microsoft compatibility packages, all **MIT**-licensed and sourced from
> https://github.com/dotnet/runtime. They are absent from the net8 / net10
> (Revit 2025 / 2026 / 2027) builds, where the runtime provides them natively.
>
> | Component | Version |
> |---|---:|
> | `Microsoft.Bcl.AsyncInterfaces` | 10.0.10 |
> | `Microsoft.Bcl.HashCode` | 6.0.0 |
> | `System.Buffers` | 4.6.1 |
> | `System.Memory` | 4.6.3 |
> | `System.Numerics.Vectors` | 4.6.1 |
> | `System.Runtime.CompilerServices.Unsafe` | 6.1.2 |
> | `System.Security.AccessControl` | 6.0.1 |
> | `System.Security.Principal.Windows` | 5.0.0 |
> | `System.Threading.Tasks.Extensions` | 4.6.3 |
>
> `System.Security.AccessControl` and `System.Security.Principal.Windows` are the last
> versions Microsoft ever published for those packages; there is nothing newer to move to.

---

## License texts

### MIT License

Applies to BouncyCastle.Cryptography, ClosedXML, ClosedXML.Parser,
DocumentFormat.OpenXml, ExcelNumberFormat, RBush, Newtonsoft.Json, PdfSharp,
WeCantSpell.Hunspell, and the Microsoft `Microsoft.Extensions.*`, `System.*`, and
`Microsoft.Bcl.*` packages listed above.

```
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

Copyright holders (non-exhaustive):
- BouncyCastle.Cryptography: Copyright (c) The Legion of the Bouncy Castle Inc. (https://www.bouncycastle.org)
- ClosedXML / ClosedXML.Parser: Copyright (c) ClosedXML contributors
- DocumentFormat.OpenXml: Copyright (c) .NET Foundation and Contributors
- ExcelNumberFormat: Copyright (c) Anders Marzi Tornblad
- RBush: Copyright (c) viceroypenguin and contributors
- Newtonsoft.Json: Copyright (c) James Newton-King
- PdfSharp: Copyright (c) empira Software GmbH
- WeCantSpell.Hunspell: Copyright (c) Aaron Dandy
- Microsoft.Extensions.* / System.* / Microsoft.Bcl.*: Copyright (c) .NET Foundation and Contributors

### Apache License 2.0 (SixLabors.Fonts)

SixLabors.Fonts 1.0.0 is licensed under the **Apache License, Version 2.0**.
The full license text is available at https://www.apache.org/licenses/LICENSE-2.0.
It is redistributed here in unmodified binary form; the corresponding source is
available at https://github.com/SixLabors/Fonts.

Copyright (c) Six Labors.

### SQLite (System.Data.SQLite)

SQLite is in the **Public Domain**. The System.Data.SQLite ADO.NET wrapper is
distributed under the same terms. See https://www.sqlite.org/copyright.html.

---

## Questions

For questions about licensing or third-party components in
B45 Labs · Coordination, contact:

- **Vendor:** B45 Labs
- **Email:** support@b45labs.com
