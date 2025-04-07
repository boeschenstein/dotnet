# .NET

- <https://github.com/boeschenstein/dotnet9>
- <https://github.com/boeschenstein/dotnet8>
- <https://github.com/boeschenstein/dotnet6>
- <https://github.com/boeschenstein/dotnet5>
-  C# vs .NET
  - C# = Language, .NET = Runtime <https://www.linkedin.com/pulse/understanding-difference-between-net-c-enfixo>
  - Comparison <https://positiwise.com/blog/difference-between-c-sharp-and-net>
  - C# <https://github.com/boeschenstein/csharp>
- nuget packages <https://github.com/boeschenstein/nuget>

## .NET Core 3: Channel (pub/sub)

- <https://medium.com/@anderson.buenogod/advanced-implementations-of-the-producer-consumer-pattern-with-channel-t-in-net-28aa94304561>
- <https://devblogs.microsoft.com/dotnet/an-introduction-to-system-threading-channels/>

## Language independence and language-independent components, CLS

- <https://github.com/dotnet/runtime/tree/main/src/libraries>

## Statements vs Expressions

- `Expression`: Something which evaluates to a value. Example: 1+2/x
- `Statement`: A line of code which does something. Example: GOTO 100

- <https://www.freecodecamp.org/news/statement-vs-expression-whats-the-difference-in-programming/>
- <https://stackoverflow.com/questions/19132/expression-versus-statement>

### Delete bin, obj, .vs folders

Add this to the end of your *.csproj files:

```xml
<Target Name="SpicNSpan"  AfterTargets="Clean">
	<!-- Remove obj folder -->
	<RemoveDir Directories="$(BaseIntermediateOutputPath)" />
	<!-- Remove bin folder -->
	<RemoveDir Directories="$(BaseOutputPath)" />
	<!-- .vs -->
	<RemoveDir Directories="$(SolutionDir).vs" />
</Target>
```

## Console

```cs
dotnet --list-sdks
dotnet --list-runtimes
```

## Docs

- Fundamentals <https://learn.microsoft.com/en-us/dotnet/fundamentals/>
- dotnet runtime code <https://github.com/dotnet/runtime/tree/main/src/libraries>
- <https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/>
  - `Naming Guidelines`: Provides guidelines for naming assemblies, namespaces, types, and members in class libraries.
  - `Type Design Guidelines`: Provides guidelines for using static and abstract classes, interfaces, enumerations, structures, and other types.
  - `Member Design Guidelines`: Provides guidelines for designing and using properties, methods, constructors, fields, events, operators, and parameters.
  - `Designing for Extensibility`: Discusses extensibility mechanisms such as subclassing, using events, virtual members, and callbacks, and explains how to choose the mechanisms that best meet your framework's requirements.
  - `Design Guidelines for Exceptions`: Describes design guidelines for designing, throwing, and catching exceptions.
  - `Usage Guidelines`: Describes guidelines for using common types such as arrays, attributes, and collections, supporting serialization, and overloading equality operators.
  - `Common Design Patterns`: Provides guidelines for choosing and implementing dependency properties and the dispose pattern.
- .NET 10 <https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-10/overview>
  
