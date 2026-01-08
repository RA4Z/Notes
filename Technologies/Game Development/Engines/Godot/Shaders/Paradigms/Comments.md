The [[Shading Language]] supports the same comment syntax as used in C# and C++, using `//` for single-line comments and `/* */` for multi-line comments:
```C
// Single-line comment.
int a = 2;  // Another single-line comment.

/*
Multi-line comment.
The comment ends when the ending delimiter is found
(here, it's on the line below).
*/
int b = 3;
```

Additionally, you can use documentation comments that are displayed in the inspector when hovering a shader parameter. Documentation comments are currently only supported when placed immediately above a `uniform` declaration. These documentation comments only support the **multiline** comment syntax and must use **two** leading asterisks (`/**`) instead of just one (`/*`):
```C
/**
 * This is a documentation comment.
 * These lines will appear in the inspector when hovering the shader parameter
 * named "Something".
 * You can use [b]BBCode[/b] [i]formatting[/i] in the comment.
 */
uniform int something = 1;
```

The asterisks on the follow-up lines are not required, but are recommended as per the [Shaders style guide](https://docs.godotengine.org/en/stable/tutorials/shaders/shaders_style_guide.html#doc-shaders-style-guide). These asterisks are automatically stripped by the inspector, so they won't appear in the tooltip