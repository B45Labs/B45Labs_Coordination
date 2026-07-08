# B45 Labs · Coordination – Third-Party Notices

**Last updated:** 2026-07-08
**Applies to:** B45 Labs · Coordination v2.0.0 (Revit 2023, 2024, 2025, 2026, 2027 builds)

This document lists the third-party components redistributed with the
B45 Labs · Coordination installer and their applicable licenses.

B45 Labs' own assemblies (`B45Labs_Coordination.dll`, `B45Labs.Shared.dll`,
`B45Labs.Connect.Sdk.dll`, `B45Labs.Connect.Contracts.dll`) are proprietary and
are not listed here. Platform components — the **Autodesk Revit API**
(`RevitAPI.dll`, `RevitAPIUI.dll`, referenced via the community
`Revit_All_Main_Versions_API_x64` NuGet package) and the **Microsoft .NET
runtime** — are referenced where present on the user's machine and are **not**
redistributed by this installer.

---

## Redistributed third-party libraries

| Component | Version | License | Source |
|---|---:|---|---|
| BouncyCastle.Cryptography | 2.5.0 | MIT | https://github.com/bcgit/bc-csharp |
| ClosedXML | 0.104.2 | MIT | https://github.com/ClosedXML/ClosedXML |
| ClosedXML.Parser | 1.0.0 | MIT | https://github.com/ClosedXML/ClosedXML.Parser |
| DocumentFormat.OpenXml | 3.1.1 | MIT | https://github.com/dotnet/Open-XML-SDK |
| ExcelNumberFormat | 1.1.0 | MIT | https://github.com/andersnm/ExcelNumberFormat |
| RBush | 4.0.0 | MIT | https://github.com/viceroypenguin/RBush |
| Microsoft.Extensions.DependencyInjection.Abstractions | 8.0.x | MIT | https://github.com/dotnet/runtime |
| Microsoft.Extensions.Logging.Abstractions | 8.0.x | MIT | https://github.com/dotnet/runtime |
| Newtonsoft.Json | 13.0.3 | MIT | https://www.newtonsoft.com/json |
| PdfSharp (incl. Charting, BarCodes, Cryptography, Quality, Shared, Snippets, System, WPFonts) | 6.2.4 | MIT | https://github.com/empira/PDFsharp |
| SixLabors.Fonts | 1.0.0 | Apache-2.0 | https://github.com/SixLabors/Fonts |
| System.Data.SQLite (`System.Data.SQLite.dll` + `SQLite.Interop.dll`) | 1.0.119 | Public Domain / SQLite License | https://www.sqlite.org |
| System.IO.Packaging | 8.0.x | MIT | https://github.com/dotnet/runtime |
| System.Security.Cryptography.Pkcs | 8.0.x | MIT | https://github.com/dotnet/runtime |
| WeCantSpell.Hunspell | 7.0.1 | MIT | https://github.com/aarondandy/WeCantSpell.Hunspell |

> The **Revit 2023 / 2024** (net48) builds additionally ship the following
> Microsoft compatibility packages, all **MIT**-licensed and sourced from
> https://github.com/dotnet/runtime: `Microsoft.Bcl.AsyncInterfaces`,
> `Microsoft.Bcl.HashCode`, `System.Buffers`, `System.Memory`,
> `System.Numerics.Vectors`, `System.Runtime.CompilerServices.Unsafe`,
> `System.Security.AccessControl`, `System.Security.Principal.Windows`, and
> `System.Threading.Tasks.Extensions`. They are absent from the net8 / net10
> (Revit 2025 / 2026 / 2027) builds, where the runtime provides them natively.

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
- BouncyCastle.Cryptography — Copyright (c) The Legion of the Bouncy Castle Inc. (https://www.bouncycastle.org)
- ClosedXML / ClosedXML.Parser — Copyright (c) ClosedXML contributors
- DocumentFormat.OpenXml — Copyright (c) .NET Foundation and Contributors
- ExcelNumberFormat — Copyright (c) Anders Marzi Tornblad
- RBush — Copyright (c) viceroypenguin and contributors
- Newtonsoft.Json — Copyright (c) James Newton-King
- PdfSharp — Copyright (c) empira Software GmbH
- WeCantSpell.Hunspell — Copyright (c) Aaron Dandy
- Microsoft.Extensions.* / System.* / Microsoft.Bcl.* — Copyright (c) .NET Foundation and Contributors

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
